---
title: Тип ресурса активности
description: Представляет одно действие в приложении — например, телепередача, документ или текущую кампанию в видеоигре. Когда пользователь наносит это действие, задействование регистрируется в виде элемента журнала, который указывает время начала и окончания для этого действия. По мере того как пользователь повторно перезапускается с этим действием, для одного действия пользователя записываются несколько элементов журнала.
localization_priority: Normal
ms.prod: project-rome
author: ailae
doc_type: resourcePageType
ms.openlocfilehash: c76df8bcc4334fc045b3841fad934f8749913381
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48037243"
---
# <a name="activity-resource-type"></a>Тип ресурса активности

Пространство имен: microsoft.graph

Представляет одно действие в приложении — например, телепередача, документ или текущую кампанию в видеоигре. Когда пользователь наносит это действие, задействование регистрируется в виде [элемента журнала](projectrome-historyitem.md) , который указывает время начала и окончания для этого действия. По мере того как пользователь повторно перезапускается с этим действием, для одного действия пользователя записываются несколько элементов журнала.

Вы можете использовать действия в Microsoft Graph, чтобы позволить пользователям возвращаться к тем, что они сделали в своем приложении, на нескольких устройствах. Действия, которые создает ваше приложение, отображаются на всех устройствах пользователей и предоставляются пользователям в виде глубоких ссылок на конкретные материалы в вашем приложении. Вы можете выразить определенный контент в вашем приложении как назначение, которое будет демонстрироваться в Windows, и доступно на устройствах iOS и Android с помощью уведомлений Кортаны.

Так как каждое приложение различается, лучше всего узнать, как сопоставить действия в приложении с действиями пользователей, которые будут отображаться в Кортане и временной шкале. Например, в играх могут создаваться действия для каждой кампании, приложения для создания документов могут создавать действия для каждого уникального документа, а бизнес-приложения могут создавать действия для каждого рабочего процесса.

Ваши действия пользователя будут демонстрироваться в Кортане и пользовательском интерфейсе на временной шкале Windows, что фокусируется на повышении производительности и эффективности пользователей, помогая им вернуться к содержимому, которое они работали в прошлое.

## <a name="methods"></a>Методы

|Метод | Возвращаемый тип | Описание|
|:------|:------------|:-----------|
|[Создание или замена действия](../api/projectrome-put-activity.md) | [действии](projectrome-activity.md) |Создает или заменяет существующее действие (UPSERT). Аппактивитид должен быть безопасным по URL-адресу (все символы, кроме зарезервированных символов RFC 2396, должны быть преобразованы в шестнадцатеричное представление), но исходный Аппактивитид не обязательно должен быть безопасным по URL-адресу. |
|[Удаление действия](../api/projectrome-delete-activity.md) | Содержимое отсутствует | Удаляет указанное действие для этого пользователя из приложения.|
|[Получение действий](../api/projectrome-get-activities.md) | Коллекция [действий](projectrome-activity.md) | Возвращает действия для вашего приложения для определенного пользователя.|
|[Получение последних действий](../api/projectrome-get-recent-activities.md) | Коллекция [действий](projectrome-activity.md) | Получает последние действия для приложения для определенного пользователя, отсортированные и основанные на недавно созданном или обновленном [historyitem](projectrome-historyitem.md).|

## <a name="properties"></a>Свойства

|Имя | Тип | Описание|
|:----|:-----|:-----------|
|усертимезоне | String | Необязательный параметр. Часовой пояс, в котором устройство пользователя, используемое для создания действия, было размещено во время создания действия; значения, предоставляемые как идентификаторы Олсона для поддержки представления на нескольких платформах.|
|createdDateTime | DateTimeOffset | Задается сервером. Дата и время в формате UTC, когда объект был создан на сервере. |
|lastModifiedDateTime | DateTimeOffset | Задается сервером. Дата и время в формате UTC, когда объект был изменен на сервере. |
|id | String | Идентификатор, созданный сервером, используемый для адресации URL-адресов.|
|аппактивитид | String | Обязательный. Уникальный идентификатор действия в контексте приложения, предоставленного вызывающим и неизменяемым после этого.|
|активитисаурцехост | String | Обязательный. URL-адрес домена, представляющий сопоставление удостоверений между платформами для приложения. Сопоставление хранится в виде JSON-файла, размещенного в домене или настраиваемого через центр разработки для Windows. JSON-файл называется Cross-Platform-App-Identifiers и размещается в корне домена HTTPS в домене верхнего уровня или включает поддомен. Примеры: https://contoso.com или https://myapp.contoso.com, но НЕ https://myapp.contoso.com/somepath. Для удостоверения приложения на нескольких платформах необходимо наличие уникального файла и домена (или дочернего домена). Например, для Word и PowerPoint требуется отдельный файл и домен.|
|appDisplayName | String | Необязательный параметр. Краткое текстовое описание приложения, которое используется для создания действия для использования в случаях, когда приложение не установлено на локальном устройстве пользователя.|
|активатионурл | String | Обязательный. URL-адрес, используемый для запуска действия в оптимальном собственном интерфейсе, представленном appId. Может запустить веб-приложение, если не существует собственного приложения.|
|фаллбаккурл | String | Необязательный параметр. URL-адрес, используемый для запуска действия в веб-приложении, если оно доступно.|
|contentUrl | String | Необязательный параметр. Используется в событии, когда содержимое может отображаться за преработкой в собственном или веб-интерфейсе веб-приложения (например, указатель на элемент в RSS-канале).|
|висуалелементс| [висуалинфо](../resources/projectrome-visualinfo.md) | Обязательно. Объект, содержащий информацию для отображения действий в пользовательском интерфейсе.|
|контентинфо | Нетипизированный объект JSON | Необязательный параметр. Настраиваемая часть расширяемого описания содержимого Data – JSON – LD в соответствии с синтаксисом [Schema.org](https://schema.org) .|
|expirationDateTime | DateTimeOffset | Задается сервером. DateTime в формате UTC, когда истечет срок действия объекта на сервере.|
|status | status | Задается сервером. Код состояния, используемый для идентификации допустимых объектов. Значения: активные, обновленные, удаленные, проигнорированы.|

## <a name="relationships"></a>Связи

|Связь | Тип | Описание|
|:------------|:-----|:-----------|
|Historyitem| Коллекция [активитихисторитем](../resources/projectrome-historyitem.md) | Необязательный параметр. Свойство NavigationProperty/вложение; свойство навигации для Historyitem действия.|

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "userTimezone",
    "appDisplayName",
    "fallbackUrl",
    "contentUrl",
    "contentInfo",
    "visualElements",
    "historyItems"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.userActivity",
  "@odata.annotations": [
    {
      "capabilities": {
        "countable": false,
        "selectable": false,
        "skippable": false
      }
    }
  ]
}-->

```json
{
    "appActivityId": "String",
    "activitySourceHost": "String (host name/domain/URL)",
    "userTimezone": "String",
    "appDisplayName": "String",
    "activationUrl": "String (URL)",
    "contentUrl": "String (URL)",
    "fallbackUrl": "String (URL)",
    "createdDateTime": "DateTimeOffset",
    "lastModifiedDateTime": "DateTimeOffset",
    "expirationDateTime": "DateTimeOffset",
    "id": "String",
    "status": "active | updated | deleted | ignored",
    "contentInfo": { "@odata.type": "microsoft.graph.Json" },
    "visualElements": { "@odata.type": "microsoft.graph.visualInfo" },
    "historyItems": [{ "@odata.type": "microsoft.graph.activityHistoryItem" }]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "activity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

