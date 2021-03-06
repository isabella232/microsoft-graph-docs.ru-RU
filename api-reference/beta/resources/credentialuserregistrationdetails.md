---
title: Тип ресурса Кредентиалусеррегистратиондетаилс
description: Представляет сведения об использовании функции автоматического сброса пароля и многофакторной проверки подлинности (MFA) для всех зарегистрированных пользователей.
localization_priority: Normal
author: khotz
ms.prod: reports
doc_type: resourcePageType
ms.openlocfilehash: 7194f1b849decddcca5d77bf0ebb9bbbd5974125
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48050024"
---
# <a name="credentialuserregistrationdetails-resource-type"></a>Тип ресурса Кредентиалусеррегистратиондетаилс

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет сведения об использовании функции автоматического сброса пароля и многофакторной проверки подлинности (MFA) для всех зарегистрированных пользователей. Сведения включают сведения о пользователе, состояние регистрации и используемый способ проверки подлинности.

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип | Описание |
|:-------------|:------------|:------------|
| [Список Кредентиалусеррегистратиондетаилс](../api/reportroot-list-credentialuserregistrationdetails.md) | Коллекция Кредентиалусеррегистратиондетаилс | Получение списка объектов [кредентиалусеррегистратиондетаилс](../resources/credentialuserregistrationdetails.md) для определенного клиента.
 |

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
| аусмесодс | Коллекция Регистратионаусмесод | Представляет способ проверки подлинности, зарегистрированный пользователем. Возможные значения: `email` , `mobilePhone` ,, `officePhone` `securityQuestion` (только для самостоятельного сброса пароля), `appNotification` `appCode` и `alternateMobilePhone` (поддерживается только при регистрации). |
| id | Строка | Уникальный идентификатор действия. Только для чтения.|
| Поддержка | Boolean | Указывает, готов ли пользователь к выполнению самостоятельного сброса пароля или MFA. |
| isEnabled | Boolean | ИндиЦиатес, разрешено ли пользователю выполнять сброс пароля самостоятельно. |
| исмфарегистеред | Boolean | ИндиЦиатес, зарегистрирован ли пользователь для MFA. |
| Регистрация | Boolean | Указывает, зарегистрировал ли пользователь какие бы то ни было методы проверки подлинности для самостоятельного сброса пароля. |
| userDisplayName | String | Предоставляет имя пользователя для соответствующего пользователя. |
| userPrincipalName | String | Предоставляет имя участника пользователя для соответствующего пользователя. |

## <a name="relationships"></a>Связи

Отсутствуют.

## <a name="json-representation"></a>Представление в формате JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.credentialUserRegistrationDetails",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "id" : "String",
  "userPrincipalName":"String",
  "userDisplayName": "String",
  "authMethods": ["string"],
  "isRegistered" : false,
  "isEnabled" : true,
  "isCapable" : false,
  "isMfaRegistered" : true
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "credentialUserRegistrationDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


