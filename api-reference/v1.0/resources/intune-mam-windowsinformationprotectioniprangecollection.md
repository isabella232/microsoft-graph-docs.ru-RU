---
title: Тип ресурса windowsInformationProtectionIPRangeCollection
description: Коллекция диапазонов IP-адресов Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: a6a2f52613eae9d8e06751672c95230dfc3b00c4
ms.sourcegitcommit: 873b99d9001d1b2af21836e47f15360b08e10a40
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30253899"
---
# <a name="windowsinformationprotectioniprangecollection-resource-type"></a><span data-ttu-id="b1937-103">Тип ресурса windowsInformationProtectionIPRangeCollection</span><span class="sxs-lookup"><span data-stu-id="b1937-103">windowsInformationProtectionIPRangeCollection resource type</span></span>

> <span data-ttu-id="b1937-104">**Примечание:** Для API Microsoft Graph для Intune требуется [Активная лицензия Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="b1937-104">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="b1937-105">Коллекция диапазонов IP-адресов Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="b1937-105">Windows Information Protection IP Range Collection</span></span>

## <a name="properties"></a><span data-ttu-id="b1937-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="b1937-106">Properties</span></span>
|<span data-ttu-id="b1937-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="b1937-107">Property</span></span>|<span data-ttu-id="b1937-108">Тип</span><span class="sxs-lookup"><span data-stu-id="b1937-108">Type</span></span>|<span data-ttu-id="b1937-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b1937-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b1937-110">displayName</span><span class="sxs-lookup"><span data-stu-id="b1937-110">displayName</span></span>|<span data-ttu-id="b1937-111">Строка</span><span class="sxs-lookup"><span data-stu-id="b1937-111">String</span></span>|<span data-ttu-id="b1937-112">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b1937-112">Display name</span></span>|
|<span data-ttu-id="b1937-113">ranges</span><span class="sxs-lookup"><span data-stu-id="b1937-113">ranges</span></span>|<span data-ttu-id="b1937-114">Коллекция объектов [ipRange](../resources/intune-mam-iprange.md)</span><span class="sxs-lookup"><span data-stu-id="b1937-114">[ipRange](../resources/intune-mam-iprange.md) collection</span></span>|<span data-ttu-id="b1937-115">Коллекция диапазонов адресов протокола Интернета</span><span class="sxs-lookup"><span data-stu-id="b1937-115">Collection of Internet protocol address ranges</span></span>|

## <a name="relationships"></a><span data-ttu-id="b1937-116">Отношения</span><span class="sxs-lookup"><span data-stu-id="b1937-116">Relationships</span></span>
<span data-ttu-id="b1937-117">Нет</span><span class="sxs-lookup"><span data-stu-id="b1937-117">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="b1937-118">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="b1937-118">JSON Representation</span></span>
<span data-ttu-id="b1937-119">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b1937-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionIPRangeCollection",
  "displayName": "String",
  "ranges": [
    {
      "@odata.type": "microsoft.graph.ipRange",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ]
}
```



