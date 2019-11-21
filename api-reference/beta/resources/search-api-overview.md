---
title: Использование API Поиска (Майкрософт) для запросов данных
description: С помощью API поиска приложения могут искать данные Office 365 в контексте пользователя, прошедшего проверку подлинности.
localization_priority: Priority
author: nmoreau
ms.prod: search
doc_type: resourcePageType
ms.openlocfilehash: afbb9ba469dad7751422902ea4a9876b6ca6b904
ms.sourcegitcommit: ef8eac3cf973a1971f8f1d41d75a085fad3690f0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/19/2019
ms.locfileid: "38704131"
---
# <a name="use-the-microsoft-search-api-to-query-data"></a>Использование API Поиска (Майкрософт) для запросов данных

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

С помощью API Поиска (Майкрософт) приложения могут запрашивать данные Office 365.

Поисковые запросы выполняются в контексте вошедшего пользователя, указанного [маркером доступа с делегированными разрешениями](/graph/auth-v2-user).

[!INCLUDE [search-api-preview](../../includes/search-api-preview-signup.md)]

## <a name="common-use-cases"></a>Основные варианты использования

API предоставляет метод [query](../api/search-query.md) для поиска данных в службе "Поиск (Майкрософт)". В этом разделе перечислены распространенные варианты использования с применением свойств, заданных в тексте запроса **query**.

Поисковые запросы выполняются от имени пользователя. Результаты поиска усекаются для применения правил контроля доступа к элементам.  Например, в контексте файлов разрешения для них оцениваются в составе поискового запроса. С помощью поиска пользователи не смогут получить доступ к тем элементам, которые недоступны им через API перечисления.

| Варианты использования | Свойства, определяемые в тексте запроса query |
|:------------------|:---------|
|[Поиск в области по типам объектов](#scope-search-based-on-entity-types)| **entityTypes** |
|[Результаты со страницы](#page-search-results) | **from** и **size** |
|[Получение наиболее релевантных электронных писем](#get-the-most-relevant-emails) | **enableTopResults** |
|[Получение выбранных свойств](#get-selected-properties) | **stored_fields** |
|[Использование KQL в терминах запросов](#keyword-query-language-kql-support) | **query** |
|[Поиск внешних файлов](/graph/search-concept-files)| **entityTypes** |
|[Поиск в определенном объекте contentSource (API индексирования)](/graph/search-concept-custom-types)| **contentSources** |

### <a name="scope-search-based-on-entity-types"></a>Поиск в области по типам объектов

Область действия поискового запроса определяется с помощью свойства **entityTypes** полезных данных запроса **query**.
Ниже перечислены поддерживаемые типы объектов.

- [event](event.md)
- [message](message.md)
- [driveItem](driveitem.md)
- [externalFile](externalfile.md)
- [externalItem](externalitem.md)

### <a name="page-search-results"></a>Результаты поиска на странице

Управляйте разбивкой результатов поиска на страницы, указав описанные ниже два свойства в тексте запроса **query**.

- **from** — целое значение, указывающее начальную точку (начиная с 0) для перечисления результатов поиска на странице. Значение по умолчанию равно 0.

- **size** — целое число, обозначающее количество результатов, возвращаемых для страницы. Значение по умолчанию: 25.

При поиске объекта **event** или **message** учитывайте указанные ниже ограничения.

- Значение **from** должно начинаться нуля для запроса первой страницы. В противном случае запрос возвращает ошибку HTTP 400 `Bad request`.
- Максимальное количество результатов на странице (**size**) составляет 200.
- Максимальное общее количество элементов, которые могут быть возвращены с разбивкой на страницы, составляет 1000.
- При превышении ограничений возвращается наилучший возможный отклик. Запрос не возвращает ошибку HTTP 400.

Рекомендации:

- В исходном запросе задайте меньший размер первой страницы. Например, задайте для свойства **from** значение 0, а для свойства **size** — 25.
- Для получения последующих страниц обновите свойства **from** и **size**. Вы можете увеличивать размер страницы в каждом последующем запросе. В приведенной ниже таблице показан пример.

    | Страница | from | size |
    |:-----|:-----|:-----|
    | 1    | 0 | 25 |
    | 2    | 25 | 50 |
    | 3    | 75 | 75 |
    | 4    | 150 | 100 |

### <a name="get-the-most-relevant-emails"></a>Получение наиболее релевантных электронных писем

Если при поиске объекта **message** задать для свойства **enableTopResults** значение `true`, возвращается гибридный список сообщений: первые три сообщения в отклике сортируются по релевантности, а остальные — по дате.

### <a name="get-selected-properties"></a>Получение выбранных свойств

При поиске объекта **externalItem** используйте свойство **stored_fields**, чтобы задать поля, возвращаемые в отклике.

Имена, указанные в свойстве **stored_fields**, должны быть управляемыми свойствами, поддерживающими извлечение. Эти имена свойств были настроены для подключения в центре администрирования клиента службы "Поиск (Майкрософт)".

### <a name="keyword-query-language-kql-support"></a>Поддержка языка KQL

Вы можете указать произвольный текст ключевых слов (например, `AND` и `OR`) и ограничения свойств в синтаксисе KQL в фактической строке поискового запроса (свойства **query** в тексте запроса **query**). Синтаксис и команда зависят от типов объектов (в свойстве **entityTypes**), указанных в тексте того же запроса **query**.

Свойства, доступные для поиска, зависят от типа объекта.

- [Свойства объекта message](/microsoft-365/compliance/keyword-queries-and-search-conditions#searchable-email-properties)
- [Свойства объекта driveItem](/microsoft-365/compliance/keyword-queries-and-search-conditions#searchable-site-properties)

## <a name="error-handling"></a>Обработка ошибок

API поиска возвращает отклики с ошибками, описанные в [определении объектов ошибок OData](http://docs.oasis-open.org/odata/odata-json-format/v4.01/cs01/odata-json-format-v4.01-cs01.html#sec_ErrorResponse), каждый из которых представляет собой объект JSON, содержащий код и сообщение.

<!---TODO Describe the know errors : bad requests.--->

## <a name="known-limitations"></a>Известные ограничения

На API поиска распространяются описанные ниже ограничения.

- Метод **query** определяется, чтобы разрешить передачу коллекции из одного или нескольких экземпляров **searchRequest**. Однако в настоящее время служба может обрабатывать только по одному экземпляру [searchRequest](./searchrequest.md) за раз.

- Ресурс [searchRequest](./searchrequest.md) поддерживает одновременную передачу объектов нескольких типов. Однако в настоящее время поддерживается только сочетание объектов **driveItem** и **externalFile**. Остальные сочетания недопустимы.

- Свойство **contentSource**, которое определяет используемое соединение, применимо, только если для свойства **entityType** задано значение `externalItem`.
<!--todo nmoreauteam Fix the link to ContentSource  pls provide the content source url--->

- API поиска не поддерживает настраиваемую сортировку и всегда сортирует результаты следующим образом:

  - результаты типов **message** и **event** сортируются по дате;

  - результаты типов **driveItem**, **externalFile** и **externalItem** сортируются по релевантности.