---
title: Получение educationSynchronizationProfile
description: Извлечение профиля синхронизации данных school в клиентов на основе идентификатора.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 47757956db9e93bb13f4167ef330c7b79d7851b1
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29530183"
---
# <a name="get-an-educationsynchronizationprofile"></a><span data-ttu-id="b4e9a-103">Получение educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="b4e9a-103">Get an educationSynchronizationProfile</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="b4e9a-104">Получение в школе данных [синхронизации профилей](../resources/educationsynchronizationprofile.md) на основе идентификатора клиента.</span><span class="sxs-lookup"><span data-stu-id="b4e9a-104">Retrieve a school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant based on the identifier.</span></span>

## <a name="permissions"></a><span data-ttu-id="b4e9a-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="b4e9a-105">Permissions</span></span>
<span data-ttu-id="b4e9a-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b4e9a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b4e9a-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="b4e9a-108">Permission type</span></span> | <span data-ttu-id="b4e9a-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="b4e9a-109">Permissions (from least to most privileged)</span></span> |
|:-----------|:----------|
| <span data-ttu-id="b4e9a-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b4e9a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b4e9a-111">EduAdministration.Read EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b4e9a-111">EduAdministration.Read, EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="b4e9a-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="b4e9a-112">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="b4e9a-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b4e9a-113">Not supported.</span></span>|
|<span data-ttu-id="b4e9a-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="b4e9a-114">Application</span></span>| <span data-ttu-id="b4e9a-115">EduAdministration.Read.All EduAdministration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4e9a-115">EduAdministration.Read.All, EduAdministration.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b4e9a-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="b4e9a-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /synchronizationProfiles/{id}
```

## <a name="request-headers"></a><span data-ttu-id="b4e9a-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="b4e9a-117">Request headers</span></span>
| <span data-ttu-id="b4e9a-118">Имя</span><span class="sxs-lookup"><span data-stu-id="b4e9a-118">Name</span></span>       | <span data-ttu-id="b4e9a-119">Тип</span><span class="sxs-lookup"><span data-stu-id="b4e9a-119">Type</span></span> | <span data-ttu-id="b4e9a-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b4e9a-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b4e9a-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="b4e9a-121">Authorization</span></span>  | <span data-ttu-id="b4e9a-122">string</span><span class="sxs-lookup"><span data-stu-id="b4e9a-122">string</span></span>  | <span data-ttu-id="b4e9a-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b4e9a-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b4e9a-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="b4e9a-125">Request body</span></span>
<span data-ttu-id="b4e9a-126">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="b4e9a-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="b4e9a-127">Ответ</span><span class="sxs-lookup"><span data-stu-id="b4e9a-127">Response</span></span>
<span data-ttu-id="b4e9a-128">Успешно завершена, этот метод возвращает `200 OK` код ответа и объект [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="b4e9a-128">If successful, this method returns a `200 OK` response code and an [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b4e9a-129">Пример</span><span class="sxs-lookup"><span data-stu-id="b4e9a-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b4e9a-130">Запрос</span><span class="sxs-lookup"><span data-stu-id="b4e9a-130">Request</span></span>
<span data-ttu-id="b4e9a-131">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="b4e9a-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_educationSynchronizationProfile"
}-->
```http
GET https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}
```

##### <a name="response"></a><span data-ttu-id="b4e9a-132">Ответ</span><span class="sxs-lookup"><span data-stu-id="b4e9a-132">Response</span></span>
<span data-ttu-id="b4e9a-133">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="b4e9a-133">The following is an example of the response.</span></span> 

><span data-ttu-id="b4e9a-p103">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="b4e9a-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSynchronizationProfile",
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 2487

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/synchronizationProfiles/$entity",
    "displayName": "Test Profile",
    "state": "provisioned",
    "id": "86904b1e-c7d0-4ead-b13a-98f11fc400ee",
    "dataProvider": {
        "@odata.type": "microsoft.graph.educationCsvDataProvider",
        "customizations": {
            "student": {
                "optionalPropertiesToSync": [
                    "State ID",
                    "Middle Name"
                ],
                "synchronizationStartDate": "0001-01-01T00:00:00Z",
                "isSyncDeferred": false,
                "allowDisplayNameUpdate": false
            },
            "teacher": {
                "optionalPropertiesToSync": [
                    "State ID",
                    "Teacher Number",
                    "Status",
                    "Middle Name",
                    "Secondary Email",
                    "Title",
                    "Qualification"
                ],
                "synchronizationStartDate": "0001-01-01T00:00:00Z",
                "isSyncDeferred": false,
                "allowDisplayNameUpdate": false
            },
            "studentEnrollment": {
                "optionalPropertiesToSync": [],
                "synchronizationStartDate": "0001-01-01T00:00:00Z",
                "isSyncDeferred": false,
                "allowDisplayNameUpdate": false
            },
            "teacherRoster": {
                "optionalPropertiesToSync": [],
                "synchronizationStartDate": "0001-01-01T00:00:00Z",
                "isSyncDeferred": false,
                "allowDisplayNameUpdate": false
            }
        }
    },
    "identitySynchronizationConfiguration": {
        "@odata.type": "microsoft.graph.educationIdentityCreationConfiguration",
        "userDomains": [
            {
                "appliesTo": "student",
                "name": "testschool.edu"
            },
            {
                "appliesTo": "teacher",
                "name": "testschool.edu"
            }
        ]
    },
    "licensesToAssign": 
         [
            {
                "@odata.type": "microsoft.graph.educationSynchronizationLicenseAssignment",
                "appliesTo": "teacher",
                "skuIds": [
                    "6fd2c87f-b296-42f0-b197-1e91e994b900"
                ]
            },
            {
                "@odata.type": "microsoft.graph.educationSynchronizationLicenseAssignment",
                "appliesTo": "student",
                "skuIds": [
                    "6fd2c87f-b296-42f0-b197-1e91e994b900"
                ]
            }
        ]
}
```
<!--
{
  "type": "#page.annotation",
  "suppressions": [
    "Error: /api-reference/beta/api/educationsynchronizationprofile-get.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
