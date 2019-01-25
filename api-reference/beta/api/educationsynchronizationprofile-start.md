---
title: Запуск синхронизации после загрузки файлов educationSynchronizationProfile
description: Проверьте файлы, отправленные в конкретных школа профиль синхронизации данных клиента. Если проверка выполнена успешно, в профиле будет запустить синхронизацию. В противном случае ответ будет содержать ошибки и предупреждения. Если ответ содержит ошибки, не запустится синхронизации. Если ответ содержит только предупреждения, будет запущен процесс синхронизации.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 1447178e80d30058b415345aea83dce4390e6bcf
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29512355"
---
# <a name="start-sync-after-uploading-files-to-an-educationsynchronizationprofile"></a><span data-ttu-id="4278e-107">Запуск синхронизации после загрузки файлов educationSynchronizationProfile</span><span class="sxs-lookup"><span data-stu-id="4278e-107">Start sync after uploading files to an educationSynchronizationProfile</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="4278e-108">Проверьте файлы, загруженные в конкретных школа данных [синхронизации профилей](../resources/educationsynchronizationprofile.md) в клиентов.</span><span class="sxs-lookup"><span data-stu-id="4278e-108">Verify the files uploaded to a specific school data [synchronization profile](../resources/educationsynchronizationprofile.md) in the tenant.</span></span> <span data-ttu-id="4278e-109">Если проверка выполнена успешно, в профиле будет запустить синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="4278e-109">If the verification is successful, synchronization will start on the profile.</span></span> <span data-ttu-id="4278e-110">В противном случае ответ будет содержать ошибки и предупреждения.</span><span class="sxs-lookup"><span data-stu-id="4278e-110">Otherwise, the response will contain errors and warnings.</span></span> <span data-ttu-id="4278e-111">Если ответ содержит ошибки, не запустится синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4278e-111">If the response contains errors, the synchronization will not start.</span></span> <span data-ttu-id="4278e-112">Если ответ содержит только предупреждения, будет запущен процесс синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4278e-112">If the response contains only warnings, synchronization will start.</span></span>

> <span data-ttu-id="4278e-113">**Примечание:** Этот метод используется только в том случае, если поставщик данных имеет тип [educationcsvdataprovider](../resources/educationcsvdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="4278e-113">**Note:** Use this method only when the data provider is of type [educationcsvdataprovider](../resources/educationcsvdataprovider.md).</span></span> <span data-ttu-id="4278e-114">Кроме того свойство профиля в состоянии необходимо подготовить к работе с прежде чем можно будет начать.</span><span class="sxs-lookup"><span data-stu-id="4278e-114">Also, the profile's state property needs to be provisioned before it can be started.</span></span> <span data-ttu-id="4278e-115">Опрос объект профиля, чтобы проверить значение свойства состояний.</span><span class="sxs-lookup"><span data-stu-id="4278e-115">Poll the profile object to check its state property.</span></span>

## <a name="permissions"></a><span data-ttu-id="4278e-116">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4278e-116">Permissions</span></span>
<span data-ttu-id="4278e-p104">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4278e-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="4278e-119">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="4278e-119">Permission type</span></span> | <span data-ttu-id="4278e-120">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4278e-120">Permissions</span></span> |
|:-----------|:----------|
| <span data-ttu-id="4278e-121">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="4278e-121">Delegated (work or school account)</span></span> | <span data-ttu-id="4278e-122">EduAdministration.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4278e-122">EduAdministration.ReadWrite</span></span> |
|<span data-ttu-id="4278e-123">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="4278e-123">Delegated (personal Microsoft account</span></span>|<span data-ttu-id="4278e-124">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4278e-124">Not supported.</span></span>|
|<span data-ttu-id="4278e-125">Для приложений</span><span class="sxs-lookup"><span data-stu-id="4278e-125">Application</span></span>|<span data-ttu-id="4278e-126">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4278e-126">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4278e-127">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="4278e-127">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /synchronizationProfiles/{id}/start
```

## <a name="request-headers"></a><span data-ttu-id="4278e-128">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="4278e-128">Request headers</span></span>
| <span data-ttu-id="4278e-129">Имя</span><span class="sxs-lookup"><span data-stu-id="4278e-129">Name</span></span>       | <span data-ttu-id="4278e-130">Тип</span><span class="sxs-lookup"><span data-stu-id="4278e-130">Type</span></span> | <span data-ttu-id="4278e-131">Описание</span><span class="sxs-lookup"><span data-stu-id="4278e-131">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="4278e-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="4278e-132">Authorization</span></span>  | <span data-ttu-id="4278e-133">string</span><span class="sxs-lookup"><span data-stu-id="4278e-133">string</span></span>  | <span data-ttu-id="4278e-p105">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="4278e-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4278e-136">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="4278e-136">Request body</span></span>
<span data-ttu-id="4278e-137">Не указывайте тело запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="4278e-137">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="4278e-138">Ответ</span><span class="sxs-lookup"><span data-stu-id="4278e-138">Response</span></span>
<span data-ttu-id="4278e-139">В случае успешного выполнения этот метод возвращает код отклика `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="4278e-139">If successful, this method returns a `200 OK` response code.</span></span> <span data-ttu-id="4278e-140">Если неудачно, возвращается `400 Bad Request`.</span><span class="sxs-lookup"><span data-stu-id="4278e-140">If unsuccessful, it returns a `400 Bad Request`.</span></span> <span data-ttu-id="4278e-141">Ответ содержит коллекцию объектов [educationFileSynchronizationVerificationMessage](../resources/educationfilesynchronizationverificationmessage.md) как часть тела ответа, если найдены ошибки и предупреждения.</span><span class="sxs-lookup"><span data-stu-id="4278e-141">The response contains a collection of [educationFileSynchronizationVerificationMessage](../resources/educationfilesynchronizationverificationmessage.md) objects as part of the response body if any errors or warnings were found.</span></span>

## <a name="example"></a><span data-ttu-id="4278e-142">Пример</span><span class="sxs-lookup"><span data-stu-id="4278e-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4278e-143">Запрос</span><span class="sxs-lookup"><span data-stu-id="4278e-143">Request</span></span>
<span data-ttu-id="4278e-144">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="4278e-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_educationSynchronizationProfile_start"
}-->
```http
POST https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/start
```

##### <a name="response"></a><span data-ttu-id="4278e-145">Ответ</span><span class="sxs-lookup"><span data-stu-id="4278e-145">Response</span></span>
<span data-ttu-id="4278e-146">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="4278e-146">Here is an example of the response.</span></span> 

><span data-ttu-id="4278e-p107">**Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="4278e-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationFileSynchronizationVerificationMessage",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 2105

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/Collection(microsoft.graph.verificationMessage)",
    "value": [
        {
            "type": "Error",
            "fileName": "section.csv",
            "description": "5 row(s) have missing data for the field - SIS ID"
        },
        {
            "type": "Error",
            "fileName": "section.csv",
            "description": "5 row(s) have an invalid format for the field - SIS ID"
        },
        {
            "type": "Warning",
            "fileName": "student.csv",
            "description": "3 duplicates found in column SIS ID which requires values to be Unique."
        },
        {
            "type": "Warning",
            "fileName": "student.csv",
            "description": "3 duplicates found in column Username which requires values to be Unique."
        },
        {
            "type": "Error",
            "fileName": "studentenrollment.csv",
            "description": "125 row(s) have referenced data not found in source. Field - Section SIS ID"
        },
        {
            "type": "Error",
            "fileName": "studentenrollment.csv",
            "description": "35 row(s) have referenced data not found in source. Field - SIS ID"
        },
        {
            "type": "Warning",
            "fileName": "teacher.csv",
            "description": "3 duplicates found in column SIS ID which requires values to be Unique."
        },
        {
            "type": "Warning",
            "fileName": "teacher.csv",
            "description": "3 duplicates found in column Username which requires values to be Unique."
        },
        {
            "type": "Error",
            "fileName": "teacherroster.csv",
            "description": "10 row(s) have referenced data not found in source. Field - Section SIS ID"
        },
        {
            "type": "Error",
            "fileName": "teacherroster.csv",
            "description": "91 row(s) have referenced data not found in source. Field - SIS ID"
        }
    ]
}
```
<!--
{
  "type": "#page.annotation",
  "suppressions": [
    "Error: /api-reference/beta/api/educationsynchronizationprofile-start.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
