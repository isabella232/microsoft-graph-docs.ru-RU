---
author: daspek
ms.author: dspektor
ms.date: 09/12/2018
title: Акцессактион
localization_priority: Normal
ms.openlocfilehash: bef6444fd42080c6f5b7cdabb69dbe9a50bab8d6
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32535829"
---
# <a name="accessaction-resource-type"></a><span data-ttu-id="043cd-102">Тип ресурса Акцессактион</span><span class="sxs-lookup"><span data-stu-id="043cd-102">accessAction resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="043cd-103">Присутствие ресурса **акцессактион** в [**itemActivity**] [ activity] указывает на то, что действие получило доступ к элементу.</span><span class="sxs-lookup"><span data-stu-id="043cd-103">The presence of the **accessAction** resource on an [**itemActivity**][activity] indicates that the activity accessed an item.</span></span>

><span data-ttu-id="043cd-104">**Примечание:** Записи действий Access доступны только в SharePoint и OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="043cd-104">**Note:** Access activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

[activity]: itemactivity.md

## <a name="properties"></a><span data-ttu-id="043cd-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="043cd-105">Properties</span></span>

<span data-ttu-id="043cd-106">У этого типа ресурса нет свойств.</span><span class="sxs-lookup"><span data-stu-id="043cd-106">This resource type has no properties.</span></span>

## <a name="json-representation"></a><span data-ttu-id="043cd-107">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="043cd-107">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.accessAction"
}-->

```json
{
}
```


<!--
{
  "type": "#page.annotation",
  "description": "The AccessAction object provides information about accesses of an item.",
  "keywords": "activities,activity,action,access",
  "section": "documentation",
  "tocPath": "Resources/AccessAction",
  "suppressions": [
    "Error: /api-reference/beta/resources/accessaction.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
