---
title: Тип ресурса Цертификатебаседаусконфигуратион
description: Представляет коллекцию центров сертификации.
localization_priority: Normal
author: adimitui
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: d6afa60a48522596754bb1991f2e9982d4a8ed8c
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "48401794"
---
# <a name="certificatebasedauthconfiguration-resource-type"></a>Тип ресурса Цертификатебаседаусконфигуратион

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Проверка подлинности на основе сертификатов обеспечивает проверку подлинности Azure Active Directory с помощью сертификата клиента на устройстве Windows, Android или iOS при подключении учетной записи Exchange Online к:

- Мобильные приложения Майкрософт, такие как Outlook и Word
- Клиенты Exchange ActiveSync (EAS)

Настройка этой функции исключает необходимость ввода имени пользователя и пароля в определенные приложения электронной почты и приложения Microsoft Office на мобильном устройстве.

Настройка проверки подлинности на основе сертификатов обеспечивается через коллекцию центров сертификации. Центры сертификации используются для установки доверенной цепочки сертификатов, что позволяет клиентам выполнять проверку подлинности с помощью Azure Active Directory с помощью сертификата клиента.

Узнайте больше о [проверке подлинности на основе сертификатов в Azure Active Directory](/azure/active-directory/authentication/active-directory-certificate-based-authentication-get-started).

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип | Описание |
|:-------------|:------------|:------------|
| [Список Цертификатебаседаусконфигуратион](../api/certificatebasedauthconfiguration-list.md) | [certificateBasedAuthConfiguration](certificatebasedauthconfiguration.md) | Перечисление свойств коллекции **цертификатебаседаусконфигуратион** . |
| [Получение Цертификатебаседаусконфигуратион](../api/certificatebasedauthconfiguration-get.md) | [certificateBasedAuthConfiguration](certificatebasedauthconfiguration.md) | Чтение свойств объекта **цертификатебаседаусконфигуратион** . |
| [Создание Цертификатебаседаусконфигуратион](../api/certificatebasedauthconfiguration-post-certificatebasedauthconfiguration.md) | [certificateBasedAuthConfiguration](certificatebasedauthconfiguration.md) | Создание нового объекта **цертификатебаседаусконфигуратион** . |
| [Удаление Цертификатебаседаусконфигуратион](../api/certificatebasedauthconfiguration-delete.md) | Нет | Удаление объекта **цертификатебаседаусконфигуратион** . |

>[!NOTE]
>Обновление Церфикатебаседаусконфигуратион не поддерживается. Чтобы изменить Церфикатебаседаусконфигуратион, сначала удалите его, а затем создайте новый Церфикатебаседаусконфигуратион.

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|цертификатеаусоритиес|Коллекция [цертификатеаусорити](certificateauthority.md)|Коллекция центров сертификации, которая создает доверенную цепочку сертификатов.|
|id|String|Уникальный идентификатор конфигурации проверки подлинности на основе сертификатов. Только для чтения.|

## <a name="relationships"></a>Связи

Нет

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.certificateBasedAuthConfiguration",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "certificateAuthorities": {"@odata.type": "collection(microsoft.graph.certificateAuthority)"},
  "id": "String (identifier)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "certificateBasedAuthConfiguration resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->