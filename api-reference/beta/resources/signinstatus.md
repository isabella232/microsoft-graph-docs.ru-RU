---
title: Тип ресурса Сигнинстатус
description: Предоставляет состояние входа (успешный или неУдачный) входа
localization_priority: Normal
ms.openlocfilehash: 96bcee62bac24701254f56bee41422ca91501d9e
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32583573"
---
# <a name="signinstatus-resource-type"></a><span data-ttu-id="7bb31-103">Тип ресурса Сигнинстатус</span><span class="sxs-lookup"><span data-stu-id="7bb31-103">signInStatus resource type</span></span>
<span data-ttu-id="7bb31-104">Предоставляет состояние входа (успешный или неУдачный) входа</span><span class="sxs-lookup"><span data-stu-id="7bb31-104">Provides the sign-in status (Success or Failure) of the sign-in</span></span>



## <a name="properties"></a><span data-ttu-id="7bb31-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="7bb31-105">Properties</span></span>
| <span data-ttu-id="7bb31-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="7bb31-106">Property</span></span>     | <span data-ttu-id="7bb31-107">Тип</span><span class="sxs-lookup"><span data-stu-id="7bb31-107">Type</span></span>   |<span data-ttu-id="7bb31-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7bb31-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7bb31-109">additionalDetails</span><span class="sxs-lookup"><span data-stu-id="7bb31-109">additionalDetails</span></span>|<span data-ttu-id="7bb31-110">String</span><span class="sxs-lookup"><span data-stu-id="7bb31-110">String</span></span>|<span data-ttu-id="7bb31-111">Предоставляет дополнительные сведения об активности входа</span><span class="sxs-lookup"><span data-stu-id="7bb31-111">Provides additional details on the sign-in activity</span></span>|
|<span data-ttu-id="7bb31-112">errorCode</span><span class="sxs-lookup"><span data-stu-id="7bb31-112">errorCode</span></span>|<span data-ttu-id="7bb31-113">Int32</span><span class="sxs-lookup"><span data-stu-id="7bb31-113">Int32</span></span>|<span data-ttu-id="7bb31-114">Предоставляет код ошибки 5 6digit, который создается при сбое входа.</span><span class="sxs-lookup"><span data-stu-id="7bb31-114">Provides the 5-6digit error code that's generated during a sign-in failure.</span></span> <span data-ttu-id="7bb31-115">Ознакомьтесь со [списком кодов и сообщений об ошибках](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).</span><span class="sxs-lookup"><span data-stu-id="7bb31-115">Check out the [list of error codes and messages](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).</span></span>|
|<span data-ttu-id="7bb31-116">failureReason</span><span class="sxs-lookup"><span data-stu-id="7bb31-116">failureReason</span></span>|<span data-ttu-id="7bb31-117">String</span><span class="sxs-lookup"><span data-stu-id="7bb31-117">String</span></span>|<span data-ttu-id="7bb31-118">Содержит сообщение об ошибке или причину сбоя для соответствующего действия при входе.</span><span class="sxs-lookup"><span data-stu-id="7bb31-118">Provides the error message or the reason for failure for the corresponding sign-in activity.</span></span> <span data-ttu-id="7bb31-119">Ознакомьтесь со [списком кодов и сообщений об ошибках](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).</span><span class="sxs-lookup"><span data-stu-id="7bb31-119">Check out the [list of error codes and messages](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7bb31-120">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="7bb31-120">JSON representation</span></span>

<span data-ttu-id="7bb31-121">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="7bb31-121">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.signInStatus"
}-->

```json
{
  "additionalDetails": "String",
  "errorCode": 1024,
  "failureReason": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "signInStatus resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
