---
title: Обновление параметров
description: 'Обновление свойств объекта settings. '
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: a01f04663173267474fa3e6e30f7431fd53041e6
ms.sourcegitcommit: 1cdb3bcddf34e7445e65477b9bf661d4d10c7311
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2019
ms.locfileid: "39844152"
---
# <a name="update-settings"></a><span data-ttu-id="aa3d1-103">Обновление параметров</span><span class="sxs-lookup"><span data-stu-id="aa3d1-103">Update settings</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="aa3d1-104">Обновление свойств объекта [усерсеттингс](../resources/usersettings.md) .</span><span class="sxs-lookup"><span data-stu-id="aa3d1-104">Update the properties of the [userSettings](../resources/usersettings.md) object.</span></span> <span data-ttu-id="aa3d1-105">Пользователи в одной организации могут иметь различные параметры в зависимости от их предпочтения или политики Организации.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-105">Users in the same organization can have different settings based on their preference or on the organization policies.</span></span> <span data-ttu-id="aa3d1-106">Чтобы получить текущие параметры пользователя, просмотрите [параметры текущей учетной записи пользователя](usersettings-get.md).</span><span class="sxs-lookup"><span data-stu-id="aa3d1-106">To get the user current settings, see [current user settings](usersettings-get.md).</span></span> 


### <a name="batch-request"></a><span data-ttu-id="aa3d1-107">Пакетный запрос</span><span class="sxs-lookup"><span data-stu-id="aa3d1-107">Batch request</span></span>

<span data-ttu-id="aa3d1-108">Кроме того, можно отказаться от использования нескольких пользователей из delve и отказаться от их вклада в релевантность содержимого для всей Организации с помощью пакетного запроса.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-108">It's also possible to opt-out multiple users from Delve and disable their contribution on content relevancy for the whole organization through a batch request.</span></span>
<span data-ttu-id="aa3d1-109">Для получения дополнительных сведений см [Пакетная обработка JSON](/graph/json-batching).</span><span class="sxs-lookup"><span data-stu-id="aa3d1-109">To learn more, see [JSON batching](/graph/json-batching).</span></span>

><span data-ttu-id="aa3d1-110">**Важно!** только члены группы ролей " [Управление организацией](https://support.office.com/article/permissions-in-the-office-365-security-compliance-center-d10608af-7934-490a-818e-e68f17d0e9c1?ui=en-US&rs=en-US&ad=US) " могут обновлять нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-110">**Important**: Only members of the [organization management](https://support.office.com/article/permissions-in-the-office-365-security-compliance-center-d10608af-7934-490a-818e-e68f17d0e9c1?ui=en-US&rs=en-US&ad=US) role group can update multiple users.</span></span> 



## <a name="permissions"></a><span data-ttu-id="aa3d1-111">Разрешения</span><span class="sxs-lookup"><span data-stu-id="aa3d1-111">Permissions</span></span>

<span data-ttu-id="aa3d1-p103">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aa3d1-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aa3d1-114">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="aa3d1-114">Permission type</span></span>      | <span data-ttu-id="aa3d1-115">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="aa3d1-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="aa3d1-116">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="aa3d1-116">Delegated (work or school account)</span></span> | <span data-ttu-id="aa3d1-117">User. ReadWrite, User. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="aa3d1-117">User.ReadWrite, User.ReadWrite.All</span></span>   |
|<span data-ttu-id="aa3d1-118">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="aa3d1-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="aa3d1-119">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-119">Not supported.</span></span>    |
|<span data-ttu-id="aa3d1-120">Для приложений</span><span class="sxs-lookup"><span data-stu-id="aa3d1-120">Application</span></span> | <span data-ttu-id="aa3d1-121">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aa3d1-121">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="aa3d1-122">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="aa3d1-122">HTTP request</span></span>

```http
PATCH /me/settings
```

<span data-ttu-id="aa3d1-123">Запрос с параметрами user id или userPrincipalName доступен только пользователю или пользователю с разрешениями User.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-123">Request with a 'user id' or 'userPrincipalName' is only accessible by the user or by a user with the User.ReadWrite.All permissions.</span></span> <span data-ttu-id="aa3d1-124">Дополнительные сведения см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aa3d1-124">To learn more, see [Permissions](/graph/permissions-reference).</span></span> 

```http
PATCH /users/{id | userPrincipalName}/settings/
```

## <a name="request-headers"></a><span data-ttu-id="aa3d1-125">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="aa3d1-125">Request headers</span></span>

| <span data-ttu-id="aa3d1-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aa3d1-126">Header</span></span>       | <span data-ttu-id="aa3d1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="aa3d1-127">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="aa3d1-128">Авторизация</span><span class="sxs-lookup"><span data-stu-id="aa3d1-128">Authorization</span></span>  | <span data-ttu-id="aa3d1-p105">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="aa3d1-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="aa3d1-131">Content-Type</span></span>  | <span data-ttu-id="aa3d1-132">application/json</span><span class="sxs-lookup"><span data-stu-id="aa3d1-132">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="aa3d1-133">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="aa3d1-133">Request body</span></span>

<span data-ttu-id="aa3d1-p106">В тексте запроса укажите значения для соответствующих полей, которые необходимо обновить. Предыдущие значения существующих свойств, не включенных в текст запроса, останутся прежними или будут повторно вычислены с учетом измененных значений других свойств. Для достижения оптимальной производительности не следует включать существующие значения, которые не изменились.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-p106">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="aa3d1-137">Свойство</span><span class="sxs-lookup"><span data-stu-id="aa3d1-137">Property</span></span>     | <span data-ttu-id="aa3d1-138">Тип</span><span class="sxs-lookup"><span data-stu-id="aa3d1-138">Type</span></span>   |<span data-ttu-id="aa3d1-139">Описание</span><span class="sxs-lookup"><span data-stu-id="aa3d1-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="aa3d1-140">contributionToContentDiscoveryDisabled</span><span class="sxs-lookup"><span data-stu-id="aa3d1-140">contributionToContentDiscoveryDisabled</span></span>|<span data-ttu-id="aa3d1-141">Логический</span><span class="sxs-lookup"><span data-stu-id="aa3d1-141">Boolean</span></span>|<span data-ttu-id="aa3d1-142">Установите значение true, чтобы запретить представителю доступ к API [тенденций](../resources/insights-trending.md) и отключить доступ к документам в Office delve для пользователя.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-142">Set to true do disable delegate access to the [Trending](../resources/insights-trending.md) API and to disable access to documents in Office Delve for the user.</span></span> <span data-ttu-id="aa3d1-143">Значение true также влияет на релевантность контента, отображаемого в Office 365, например, Рекомендуемые сайты в SharePoint Home и представление обнаружение в OneDrive для бизнеса содержат менее релевантные результаты.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-143">Setting to true also affects the relevance of the content displayed in Office 365 - for example, Suggested sites in SharePoint Home and the Discover view in OneDrive for Business show less relevant results.</span></span> <span data-ttu-id="aa3d1-144">Этот параметр отражает состояние элемента управления в [Office delve](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout).</span><span class="sxs-lookup"><span data-stu-id="aa3d1-144">This setting reflects the control state in [Office Delve](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout).</span></span>|

## <a name="example"></a><span data-ttu-id="aa3d1-145">Пример</span><span class="sxs-lookup"><span data-stu-id="aa3d1-145">Example</span></span> 

##### <a name="request"></a><span data-ttu-id="aa3d1-146">Запрос</span><span class="sxs-lookup"><span data-stu-id="aa3d1-146">Request</span></span>

<span data-ttu-id="aa3d1-147">Ниже приведен пример запроса на отказаться от участия пользователя в delve и отказаться от его участия в релевантности контента для всей Организации.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-147">Here is an example request on how to opt-out a user from Delve and disable his contribution on content relevancy for the whole organization.</span></span>

```http
PATCH https://graph.microsoft.com/beta/me/settings
Content-type: application/json
Content-length: 37

{
  "contributionToContentDiscoveryDisabled": true
}
```

##### <a name="response"></a><span data-ttu-id="aa3d1-148">Отклик</span><span class="sxs-lookup"><span data-stu-id="aa3d1-148">Response</span></span>

<span data-ttu-id="aa3d1-p108">Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.</span><span class="sxs-lookup"><span data-stu-id="aa3d1-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": true
}
```
