---
title: Тип ресурса identityProvider
description: Представляет поставщиков удостоверений в клиенте Azure Active Directory и клиенте Azure AD B2C.
localization_priority: Priority
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: namkedia
ms.openlocfilehash: 8f8adb3911b5912644356771f1b228880021ca94
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "48401430"
---
# <a name="identityprovider-resource-type"></a>Тип ресурса identityProvider

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет поставщиков удостоверений с [внешними удостоверениями](/azure/active-directory/external-identities/) для клиента Azure Active Directory и клиента Azure AD B2C.

Для сценариев Azure AD B2B в клиенте Azure AD типом поставщика удостоверений может быть Google или Facebook.

Настройка поставщика удостоверений в клиенте Azure AD позволяет применять новые гостевые сценарии Azure AD B2B. Например, в организации есть ресурсы в Microsoft 365, которыми нужно поделиться с пользователем Gmail. Для проверки подлинности и доступа к документам пользователь Gmail использует данные учетной записи Google.

В клиенте Azure AD B2C типом поставщика удостоверений может быть Майкрософт, Google, Facebook, Amazon, LinkedIn, Twitter или любой [openIdConnectProvider](../resources/openidconnectprovider.md). В предварительной версии доступны следующие поставщики удостоверений: Weibo, QQ, WeChat и GitHub.

Настройка поставщика удостоверений в клиенте Azure AD B2C позволяет пользователям регистрироваться и входить с помощью учетных записей социальных сетей или настраиваемого поставщика, поддерживающего OpenID Connect, в приложении. Например, приложение может использовать Azure AD B2C, чтобы разрешить пользователям регистрироваться в службе с помощью учетной записи Facebook или собственного поставщика удостоверений, соответствующего протоколу OIDC.


Если это настраиваемый поставщик удостоверений OpenID Connect с `OpenIDConnect` в качестве `type`, он представляется с помощью типа ресурса [openIdConnectProvider](../resources/openidconnectprovider.md), наследуемого от типа ресурса identityProvider. 

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип  |Описание|
|:---------------|:--------|:----------|
|[Перечисление](../api/identityprovider-list.md)|Коллекция объектов identityProvider|Получение всех поставщиков удостоверений, настроенных в клиенте.|
|[Создание](../api/identityprovider-post-identityproviders.md)|identityProvider|Создание поставщика удостоверений.|
|[Получение](../api/identityprovider-get.md) |identityProvider|Получение свойств поставщика удостоверений.|
|[Обновление](../api/identityprovider-update.md)|Нет|Обновление поставщика удостоверений.|
|[Удаление](../api/identityprovider-delete.md)|Нет|Удаление поставщика удостоверений.|
|[Перечисление доступных типов поставщиков](../api/identityprovider-list-availableprovidertypes.md)|Коллекция String|Получение всех доступных типов поставщиков удостоверений.|

## <a name="properties"></a>Свойства

|Свойство|Тип|Описание|
|:---------------|:--------|:----------|
|clientId|String|Идентификатор клиента для приложения, полученный при регистрации приложения с помощью поставщика удостоверений. Это поле обязательно для заполнения.|
|clientSecret|Строка|Секрет клиента для приложения, полученный при регистрации приложения с помощью поставщика удостоверений. Только для записи. Операция чтения возвращает "\*\*\*\*". Это поле обязательно для заполнения.|
|id|String|Идентификатор поставщика удостоверений.|
|name|String|Отображаемое имя поставщика удостоверений.|
|type|Строка|Тип поставщика удостоверений является обязательным полем.<ul>Для сценария B2B:<li/>Google<li/>Facebook</ul><ul>Для сценария B2C:<li/>Майкрософт<li/>Google<li/>Amazon<li/>LinkedIn<li/>Facebook<li/>GitHub<li/>Twitter<li/>Weibo<li/>QQ<li/>WeChat<li/>OpenIDConnect</ul>|

### <a name="where-to-get-the-client-id-and-secret"></a>Где взять идентификатор и секрет клиента

Для каждого поставщика удостоверений существует процесс создания регистрации приложения. Например, пользователи создают регистрацию приложения с помощью Facebook на сайте [developers.facebook.com](https://developers.facebook.com/). Получившийся идентификатор и секрет клиента можно передать для [создания identityProvider](../api/identityprovider-post-identityproviders.md). После этого каждый объект пользователя в каталоге можно объединить с любым поставщиком удостоверений клиента для проверки подлинности. Это позволяет пользователям входить путем ввода учетных данных на странице входа поставщика удостоверений. Маркер от поставщика удостоверений проверяется с помощью Azure AD перед выпуском клиентом маркера для приложения.

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.identityProvider"
} -->

```json
{
    "id": "String",
    "type": "String",
    "name": "String",
    "clientId": "String",
    "clientSecret": "String"
}
```