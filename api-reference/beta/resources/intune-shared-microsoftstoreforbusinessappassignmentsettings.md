---
title: Тип ресурса microsoftStoreForBusinessAppAssignmentSettings
description: Содержит свойства, используемые при назначении мобильного приложения Microsoft Store для бизнеса группе.
author: davidmu1
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 62dab652d6b4f9b16d8f95d6820f3361835f4711
ms.sourcegitcommit: b38fd4c8c734243f6f82448045a1f6bf63311ec9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "42768928"
---
# <a name="microsoftstoreforbusinessappassignmentsettings-resource-type"></a><span data-ttu-id="74d85-103">Тип ресурса microsoftStoreForBusinessAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="74d85-103">microsoftStoreForBusinessAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="74d85-104">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="74d85-104">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="74d85-105">**Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="74d85-105">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="74d85-106">Содержит свойства, используемые при назначении мобильного приложения Microsoft Store для бизнеса группе.</span><span class="sxs-lookup"><span data-stu-id="74d85-106">Contains properties used to assign an Microsoft Store for Business mobile app to a group.</span></span>


<span data-ttu-id="74d85-107">Наследуется от [mobileAppAssignmentSettings](../resources/intune-shared-mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="74d85-107">Inherits from [mobileAppAssignmentSettings](../resources/intune-shared-mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="74d85-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="74d85-108">Properties</span></span>
|<span data-ttu-id="74d85-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="74d85-109">Property</span></span>|<span data-ttu-id="74d85-110">Тип</span><span class="sxs-lookup"><span data-stu-id="74d85-110">Type</span></span>|<span data-ttu-id="74d85-111">Описание</span><span class="sxs-lookup"><span data-stu-id="74d85-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="74d85-112">useDeviceContext</span><span class="sxs-lookup"><span data-stu-id="74d85-112">useDeviceContext</span></span>|<span data-ttu-id="74d85-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="74d85-113">Boolean</span></span>|<span data-ttu-id="74d85-114">Указывает, следует ли использовать контекст работы устройства для мобильного приложения Microsoft Store для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="74d85-114">Whether or not to use device execution context for Microsoft Store for Business mobile app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="74d85-115">Связи</span><span class="sxs-lookup"><span data-stu-id="74d85-115">Relationships</span></span>
<span data-ttu-id="74d85-116">Нет</span><span class="sxs-lookup"><span data-stu-id="74d85-116">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="74d85-117">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="74d85-117">JSON Representation</span></span>
<span data-ttu-id="74d85-118">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="74d85-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessAppAssignmentSettings",
  "useDeviceContext": true
}
```



