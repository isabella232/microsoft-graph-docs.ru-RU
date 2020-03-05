---
title: Тип ресурса fileHash
description: Содержит сведения о состоянии хэшей файлов (криптографии и зависящие от местонахождения).
localization_priority: Normal
doc_type: resourcePageType
ms.prod: ''
author: ''
ms.openlocfilehash: a163a89e1e7ca7cb2a6bdf4c65945a601323d8fd
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42498240"
---
# <a name="filehash-resource-type"></a><span data-ttu-id="0442e-103">Тип ресурса fileHash</span><span class="sxs-lookup"><span data-stu-id="0442e-103">fileHash resource type</span></span>

<span data-ttu-id="0442e-104">Пространство имен: Microsoft. Graph</span><span class="sxs-lookup"><span data-stu-id="0442e-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="0442e-105">Содержит сведения о состоянии хэшей файлов (криптографии и зависящие от местонахождения).</span><span class="sxs-lookup"><span data-stu-id="0442e-105">Contains stateful information about file hashes (cryptographic and location-sensitive).</span></span>

## <a name="properties"></a><span data-ttu-id="0442e-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="0442e-106">Properties</span></span>

| <span data-ttu-id="0442e-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="0442e-107">Property</span></span>     | <span data-ttu-id="0442e-108">Тип</span><span class="sxs-lookup"><span data-stu-id="0442e-108">Type</span></span>        | <span data-ttu-id="0442e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0442e-109">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="0442e-110">хаштипе</span><span class="sxs-lookup"><span data-stu-id="0442e-110">hashType</span></span>|<span data-ttu-id="0442e-111">Перечисление [филехаштипе](filehashtypeenumtype.md)</span><span class="sxs-lookup"><span data-stu-id="0442e-111">[fileHashType](filehashtypeenumtype.md) enum</span></span>|<span data-ttu-id="0442e-112">Тип хэша файла.</span><span class="sxs-lookup"><span data-stu-id="0442e-112">File hash type.</span></span> <span data-ttu-id="0442e-113">Возможные значения: `unknown`, `sha1`, `sha256`, `md5`, `authenticodeHash256`, `lsHash`, `ctph`, `peSha1`, `peSha256`.</span><span class="sxs-lookup"><span data-stu-id="0442e-113">Possible values are: `unknown`, `sha1`, `sha256`, `md5`, `authenticodeHash256`, `lsHash`, `ctph`, `peSha1`, `peSha256`.</span></span>|
|<span data-ttu-id="0442e-114">хашвалуе</span><span class="sxs-lookup"><span data-stu-id="0442e-114">hashValue</span></span>|<span data-ttu-id="0442e-115">String</span><span class="sxs-lookup"><span data-stu-id="0442e-115">String</span></span>|<span data-ttu-id="0442e-116">Значение хэша файла.</span><span class="sxs-lookup"><span data-stu-id="0442e-116">Value of the file hash.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0442e-117">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="0442e-117">JSON representation</span></span>

<span data-ttu-id="0442e-118">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="0442e-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileHash"
}-->

```json
{
  "hashType": "@odata.type: microsoft.graph.fileHashType",
  "hashValue": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileHash resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
