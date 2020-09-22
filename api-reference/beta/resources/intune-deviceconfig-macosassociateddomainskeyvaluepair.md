---
title: Тип ресурса МакосассоЦиатеддомаинскэйвалуепаир
description: Комбинация "ключ — значение" для связанных доменов
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: bc73af5746dce61961563b84871e35bab1982c09
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48055444"
---
# <a name="macosassociateddomainskeyvaluepair-resource-type"></a><span data-ttu-id="aed72-103">Тип ресурса МакосассоЦиатеддомаинскэйвалуепаир</span><span class="sxs-lookup"><span data-stu-id="aed72-103">macOSAssociatedDomainsKeyValuePair resource type</span></span>

<span data-ttu-id="aed72-104">Пространство имен: microsoft.graph</span><span class="sxs-lookup"><span data-stu-id="aed72-104">Namespace: microsoft.graph</span></span>

> <span data-ttu-id="aed72-105">**Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aed72-105">**Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.</span></span>

> <span data-ttu-id="aed72-106">**Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.</span><span class="sxs-lookup"><span data-stu-id="aed72-106">**Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.</span></span>

<span data-ttu-id="aed72-107">Комбинация "ключ — значение" для связанных доменов</span><span class="sxs-lookup"><span data-stu-id="aed72-107">Key value pair for associated domains</span></span>


<span data-ttu-id="aed72-108">Наследуется от [KeyValuePair](../resources/intune-shared-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="aed72-108">Inherits from [keyValuePair](../resources/intune-shared-keyvaluepair.md)</span></span>

## <a name="properties"></a><span data-ttu-id="aed72-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="aed72-109">Properties</span></span>
|<span data-ttu-id="aed72-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="aed72-110">Property</span></span>|<span data-ttu-id="aed72-111">Тип</span><span class="sxs-lookup"><span data-stu-id="aed72-111">Type</span></span>|<span data-ttu-id="aed72-112">Описание</span><span class="sxs-lookup"><span data-stu-id="aed72-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aed72-113">name</span><span class="sxs-lookup"><span data-stu-id="aed72-113">name</span></span>|<span data-ttu-id="aed72-114">String</span><span class="sxs-lookup"><span data-stu-id="aed72-114">String</span></span>|<span data-ttu-id="aed72-115">Имя для этой ключевой [РазkeyValuePairа](../resources/intune-shared-keyvaluepair.md) , унаследованной от</span><span class="sxs-lookup"><span data-stu-id="aed72-115">Name for this key-value pair Inherited from [keyValuePair](../resources/intune-shared-keyvaluepair.md)</span></span>|
|<span data-ttu-id="aed72-116">value</span><span class="sxs-lookup"><span data-stu-id="aed72-116">value</span></span>|<span data-ttu-id="aed72-117">String</span><span class="sxs-lookup"><span data-stu-id="aed72-117">String</span></span>|<span data-ttu-id="aed72-118">Значение для этой заданной для этой основе ключа, унаследованной от [KeyValuePair](../resources/intune-shared-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="aed72-118">Value for this key-value pair Inherited from [keyValuePair](../resources/intune-shared-keyvaluepair.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="aed72-119">Связи</span><span class="sxs-lookup"><span data-stu-id="aed72-119">Relationships</span></span>
<span data-ttu-id="aed72-120">Нет</span><span class="sxs-lookup"><span data-stu-id="aed72-120">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="aed72-121">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="aed72-121">JSON Representation</span></span>
<span data-ttu-id="aed72-122">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="aed72-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSAssociatedDomainsKeyValuePair"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSAssociatedDomainsKeyValuePair",
  "name": "String",
  "value": "String"
}
```






