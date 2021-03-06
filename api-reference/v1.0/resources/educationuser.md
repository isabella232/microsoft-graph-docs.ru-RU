---
title: Тип ресурса educationUser
description: Пользователь в системе. Используемый для сферы образования вариант указания пользователя с тем же параметром `id`, который Microsoft Graph возвратит из конечной точки `/users`, не ограниченной сферой образования.
author: mmast-msft
localization_priority: Normal
ms.prod: education
doc_type: resourcePageType
ms.openlocfilehash: de21fabafaee8f11504da9cb41d2d35c7df869aa
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48069150"
---
# <a name="educationuser-resource-type"></a>Тип ресурса educationUser

Пространство имен: microsoft.graph

Пользователь в системе. Используемый для сферы образования вариант указания пользователя с тем же параметром `id`, который Microsoft Graph возвратит из конечной точки `/users`, не ограниченной сферой образования.
Этот объект предоставляет целевое подмножество свойств из основного объекта [user], а также добавляет ряд используемых для сферы образования свойств, таких как `primaryRole`, student и teacher.

## <a name="methods"></a>Методы

| Метод                                               | Возвращаемый тип                  | Описание                                                                   |
| :--------------------------------------------------- | :--------------------------- | :---------------------------------------------------------------------------- |
| [Получение educationUser](../api/educationuser-get.md)     | [educationUser]              | Считывание свойств и связей объекта **educationUser**.             |
| [Перечисление курсов](../api/educationuser-list-classes.md) | Коллекция [educationClass]  | Получение коллекции объектов **educationClass**, для которых пользователь является участником.    |
| [Перечисление учебных заведений](../api/educationuser-list-schools.md) | Коллекция [educationSchool] | Получение коллекции объектов **educationSchool**, для которых пользователь является участником. |
| [Получение пользователя](../api/educationuser-get-user.md)         | [user]                       | Получение простого каталога **user**, который соответствует этому объекту **educationUser**. |
| [Обновление](../api/educationuser-update.md)             | [educationUser]              | Обновление объекта **educationUser**.                                           |
| [удаление](../api/educationuser-delete.md);             | Нет                         | Удаление объекта **educationUser**.                                           |

## <a name="properties"></a>Свойства

| Свойство          | Тип                         | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :---------------- | :--------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| accountEnabled    | Boolean                      | Если учетная запись обеспечена — значение **true**, в противном случае — **false**. Это свойство обязательно указывать при создании пользователя. Поддерживает параметр $filter.                                                                                                                                                                                                                                                                                                                                                                                                    |
| assignedLicenses  | Коллекция [assignedLicense] | Лицензии, назначенные пользователю. Значение null не допускается.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| assignedPlans     | Коллекция [assignedPlan]    | Планы, назначенные пользователю. Только для чтения. Значение null не допускается.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| businessPhones    | Коллекция строк            | Номера телефонов пользователя. **Примечание.** Несмотря на то что это коллекция строк, для этого свойства можно задать только один номер.                                                                                                                                                                                                                                                                                                                                                                                                |
| createdBy         | [identitySet]                | Объект, который создал пользователя.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| department        | String                       | Название отдела, в котором работает пользователь. Поддерживает параметр $filter.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| displayName       | String                       | Имя пользователя, отображаемое в адресной книге. Обычно это сочетание имени, отчества и фамилии пользователя. Это свойство необходимо указывать при создании пользователя. Его невозможно удалить при обновлении. Поддерживает параметры $filter и $orderby.                                                                                                                                                                                                                                                           |
| externalSource    | `educationExternalSource`    | Источник для создания пользователя. Возможные значения: `sis` , `manual` .                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| givenName         | String                       | Простое имя пользователя. Поддерживает параметр $filter.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| id                | String                       | Уникальный идентификатор пользователя. Наследуется от [directoryObject](directoryobject.md). Ключ. Значение null не допускается. Только для чтения.                                                                                                                                                                                                                                                                                                                                                                                                          |
| mail              | String                       | SMTP-адрес пользователя, например "victor@contoso.onmicrosoft.com". Только для чтения. Поддерживает параметр $filter.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| mailingAddress    | [physicalAddress]            | Почтовый адрес пользователя.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| mailNickname      | String                       | Почтовый псевдоним для пользователя. Это свойство должно быть указано при создании пользователя. Поддерживает параметр $filter.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| middleName        | String                       | Отчество пользователя.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| mobilePhone       | String                       | Основной сотовый телефон пользователя.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| passwordPolicies  | String                       | Задает политики паролей для пользователя. Это значение является перечислением, которое может иметь одно из возможных значений: "Дисаблестронгпассворд", что позволяет использовать более слабые пароли по сравнению с политикой по умолчанию. Также можно указать "Дисаблепассвордекспиратион". Два значения можно указать одновременно. Пример: "DisablePasswordExpiration, DisableStrongPassword".                                                                                                                                                                      |
| passwordProfile   | [PasswordProfile]            | Задает профиль пароля для пользователя. Профиль содержит пароль пользователя. Это свойство обязательно указывать при создании пользователя. Пароль в профиле должен соответствовать минимальным требованиям, указанным в свойстве **passwordPolicies**. По умолчанию требуется надежный пароль.                                                                                                                                                                                                                             |
| preferredLanguage | String                       | Предпочитаемый язык для пользователя. Он должен быть представлен в формате ISO 639-1. Пример: "ru-RU".                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| primaryRole       | едукатионусерроле            | Роль по умолчанию для пользователя. Роль пользователя для отдельного курса может отличаться. Возможные значения: `student` , `teacher` . Поддерживает параметр $filter.                                                                                                                                                                                                                                                                                                                                                                             |
| provisionedPlans  | Коллекция [ProvisionedPlan] | Планы, подготовленные для пользователя. Только для чтения. Значение null не допускается.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| релатедконтактс   | Коллекция [релатедконтакт]  | Набор контактов, относящихся к пользователю.  Это необязательное свойство должно быть указано в предложении $select и может извлекаться только для отдельного пользователя.                                                                                                                                                                                                                                                                                                                                                                             |
| residenceAddress  | [physicalAddress]            | Адрес проживания пользователя.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| student           | [educationStudent]           | Если основная роль — student, этот блок будет содержать данные, касающиеся учащегося.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| surname           | String                       | Фамилия пользователя. Поддерживает параметр $filter.                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| teacher           | [educationTeacher]           | Если основная роль — преподаватель, этот блок будет содержать данные, характерные для преподавателя.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| usageLocation     | String                       | Двухбуквенный код страны (по стандарту ISO 3166). Свойство необходимо указывать для пользователей, которым будут назначены лицензии, в связи с законодательным требованием проверять доступность служб в странах или регионах. Примеры: "RU", "JP", "GB". Значение null не допускается. Поддерживает параметр $filter.                                                                                                                                                                                                                                                                |
| userPrincipalName | String                       | Имя участника-пользователя. Это имя для входа через Интернет по стандарту RFC 822. В соответствии с соглашением оно должно указывать на имя пользователя для электронной почты. Общий формат alias@domain, где домен должен присутствовать в коллекции проверенных доменов клиента. Это свойство обязательно указывать при создании пользователя. Доступ к проверенным доменам клиента можно получить с помощью свойства **verifiedDomains** объекта [organization](organization.md). Поддерживает параметры $filter и $orderby. |
| userType          | String                       | Строковое значение, с помощью которого можно классифицировать типы пользователей в каталоге, например "Участник" и "Гость". Поддерживает параметр $filter.                                                                                                                                                                                                                                                                                                                                                                                                        |

## <a name="relationships"></a>Связи

| Связь | Тип                         | Описание                                    |
| :----------- | :--------------------------- | :--------------------------------------------- |
| classes      | Коллекция [educationClass]  | Курсы пользователя. Допускается значение NULL.   |
| schools      | Коллекция [educationSchool] | Учебные заведения пользователя. Допускается значение NULL.   |
| assignments  | [educationAssignment]        | Список назначений для пользователя. Допускается значение null.    |
| user         | [user]                       | Пользователь каталога, соответствующий этому пользователю. |

>[!IMPORTANT]
>Ресурс **[educationAssignment]** является ресурсом версии/Beta. Если вы его используете, периодически просматривайте [журнал изменений](/graph/changelog). Когда ресурсы API Microsoft Graph освобождаются до конечной точки/V1.0, в журнале изменений указывается выпуск. Если ваше приложение использует ресурс **educationAssignment** , необходимо объявить URL-адреса базового запроса, как показано в следующем блоке кода:  
>
>```JavaScript
>var v1BaseUrl = "https://graph.microsoft.com/v1.0/education";
>var betaBaseUrl = "https://graph.microsoft.com/beta/education";  // for administrativeUnit and educationOrganization
>```

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.educationUser"
}-->

```json
{
  "id": "string",
  "accountEnabled": true,
  "assignedLicenses": [{"@odata.type": "microsoft.graph.assignedLicense"}],
  "assignedPlans": [{"@odata.type": "microsoft.graph.assignedPlan"}],
  "businessPhones": ["555-555-6568"],
  "department": "string",
  "displayName": "string",
  "givenName": "string",
  "middleName": "string",
  "surname": "string",
  "mail": "string",
  "mailNickname": "string",
  "mobilePhone": "string",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "externalSource": "string",
  "mailingAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "passwordPolicies": "string",
  "passwordProfile": {"@odata.type": "microsoft.graph.passwordProfile"},
  "preferredLanguage": "string",
  "primaryRole": "string",
  "provisionedPlans": [{"@odata.type": "microsoft.graph.provisionedPlan"}],
  "residenceAddress": {"@odata.type": "microsoft.graph.physicalAddress"},
  "student": {"@odata.type": "microsoft.graph.educationStudent"},
  "teacher": {"@odata.type": "microsoft.graph.educationTeacher"},
  "usageLocation": "string",
  "userPrincipalName": "string",
  "userType": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationUser resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Error: microsoft.graph.educationUser/assignments:
      Referenced type microsoft.graph.educationAssignment is not defined in the doc set! Potential suggestion: UNKNOWN",
    "Warning: /api-reference/v1.0/resources/educationuser.md/microsoft.graph.educationUser:
      Property 'relatedContacts' found in markdown table but not in resource definition."
  ],
  "tocPath": ""
}-->

[educationuser]: educationuser.md
[educationclass]: educationclass.md
[educationschool]: educationschool.md
[educationassignment]: /graph/api/resources/educationassignment?view=graph-rest-beta
[educationteacher]: educationteacher.md
[educationstudent]: educationstudent.md
[релатедконтакт]: relatedcontact.md
[PhysicalAddress]: physicaladdress.md
[Коллекция provisionedplan]: provisionedplan.md
[passwordprofile необходима]: passwordprofile.md
[Identity]: identityset.md
[Коллекция assignedplan]: assignedplan.md
[Коллекция assignedlicense]: assignedlicense.md
[user]: user.md
[directoryobject]: directoryobject.md

