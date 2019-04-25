---
title: Удаление oAuth2PermissionGrant
description: Удаление oAuth2PermissionGrant.
localization_priority: Normal
ms.openlocfilehash: 5c115ada8e39412fbe64259da02b1eadef3f263b
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32540151"
---
# <a name="delete-oauth2permissiongrant"></a><span data-ttu-id="80f91-103">Удаление oAuth2PermissionGrant</span><span class="sxs-lookup"><span data-stu-id="80f91-103">Delete oAuth2PermissionGrant</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="80f91-104">Удаление oAuth2PermissionGrant.</span><span class="sxs-lookup"><span data-stu-id="80f91-104">Delete an oAuth2PermissionGrant.</span></span>

## <a name="permissions"></a><span data-ttu-id="80f91-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="80f91-105">Permissions</span></span>
<span data-ttu-id="80f91-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="80f91-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="80f91-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="80f91-108">Permission type</span></span>      | <span data-ttu-id="80f91-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="80f91-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="80f91-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="80f91-110">Delegated (work or school account)</span></span> | <span data-ttu-id="80f91-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="80f91-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="80f91-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="80f91-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="80f91-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="80f91-113">Not supported.</span></span>    |
|<span data-ttu-id="80f91-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="80f91-114">Application</span></span> | <span data-ttu-id="80f91-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="80f91-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="80f91-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="80f91-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /oAuth2Permissiongrants/{id}
DELETE /users/{id | userPrincipalName}/oAuth2Permissiongrants/{id}
DELETE /drive/root/createdByUser/oAuth2Permissiongrants/{id}

```
## <a name="request-headers"></a><span data-ttu-id="80f91-117">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="80f91-117">Request headers</span></span>
| <span data-ttu-id="80f91-118">Имя</span><span class="sxs-lookup"><span data-stu-id="80f91-118">Name</span></span>       | <span data-ttu-id="80f91-119">Тип</span><span class="sxs-lookup"><span data-stu-id="80f91-119">Type</span></span> | <span data-ttu-id="80f91-120">Описание</span><span class="sxs-lookup"><span data-stu-id="80f91-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="80f91-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="80f91-121">Authorization</span></span>  | <span data-ttu-id="80f91-122">string</span><span class="sxs-lookup"><span data-stu-id="80f91-122">string</span></span>  | <span data-ttu-id="80f91-p102">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="80f91-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="80f91-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="80f91-125">Request body</span></span>
<span data-ttu-id="80f91-126">Не указывайте текст запроса для этого метода.</span><span class="sxs-lookup"><span data-stu-id="80f91-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="80f91-127">Отклик</span><span class="sxs-lookup"><span data-stu-id="80f91-127">Response</span></span>

<span data-ttu-id="80f91-p103">В случае успешного выполнения этот метод возвращает код отклика `204 No Content`. В тексте отклика не возвращается никаких данных.</span><span class="sxs-lookup"><span data-stu-id="80f91-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="80f91-130">Пример</span><span class="sxs-lookup"><span data-stu-id="80f91-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="80f91-131">Запрос</span><span class="sxs-lookup"><span data-stu-id="80f91-131">Request</span></span>
<span data-ttu-id="80f91-132">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="80f91-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_oAuth2Permissiongrant"
}-->
```http
DELETE https://graph.microsoft.com/beta/oAuth2Permissiongrants/{id}
```
##### <a name="response"></a><span data-ttu-id="80f91-133">Отклик</span><span class="sxs-lookup"><span data-stu-id="80f91-133">Response</span></span>
<span data-ttu-id="80f91-134">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="80f91-134">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Delete oAuth2Permissiongrant",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/api/oauth2permissiongrant-delete.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
