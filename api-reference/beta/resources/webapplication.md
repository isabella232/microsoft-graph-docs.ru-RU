---
title: Тип ресурса "приложение"
description: Указывает параметры для веб-приложения.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: sureshja
ms.openlocfilehash: af9f183011ee8774387288f8d02c4bade8352f6b
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48033520"
---
# <a name="webapplication-resource-type"></a>Тип ресурса "приложение"

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Указывает параметры для веб-приложения.

## <a name="properties"></a>Свойства

| Свойство | Тип | Описание |
|:---------|:-----|:------------|
| `homePageUrl` | String | Главная или начальная страница приложения. |
| `implicitGrantSettings` | [имплиЦитгрантсеттингс](implicitgrantsettings.md)| Указывает, может ли это веб-приложение запрашивать маркеры, используя неявный поток OAuth 2,0. |
| `logoutUrl` | String | Указывает URL-адрес, используемый службой проверки подлинности корпорации Майкрософт для выхода пользователя с помощью [основного канала](https://openid.net/specs/openid-connect-frontchannel-1_0.html), [обратного канала](https://openid.net/specs/openid-connect-backchannel-1_0.html) или протоколов выхода SAML. |
| `redirectUris` | Коллекция String | Задает URL-адреса, по которым маркеры пользователей отправляются для входа, или URI перенаправления, для которых отправляются коды авторизации OAuth 2,0 и маркеры доступа. |

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.webApplication"
}-->

```json
{
  "homePageUrl": "String",
  "implicitGrantSettings": {"@odata.type": "microsoft.graph.implicitGrantSettings"},
  "logoutUrl": "String",
  "redirectUris": ["String"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "webApplication resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


