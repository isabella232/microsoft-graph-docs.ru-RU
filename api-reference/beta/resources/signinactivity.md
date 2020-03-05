---
title: Тип ресурса Сигнинактивити
description: Предоставляет дату последнего входа для определенного пользователя.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 8144a681f93df45827c8b304d507eea820adcca2
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42520599"
---
# <a name="signinactivity-resource-type"></a><span data-ttu-id="dce4c-103">Тип ресурса Сигнинактивити</span><span class="sxs-lookup"><span data-stu-id="dce4c-103">signInActivity resource type</span></span>

<span data-ttu-id="dce4c-104">Пространство имен: Microsoft. Graph</span><span class="sxs-lookup"><span data-stu-id="dce4c-104">Namespace: microsoft.graph</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="dce4c-105">Предоставляет дату последнего входа для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="dce4c-105">Provides the last signed-in date for a specific user.</span></span>

## <a name="properties"></a><span data-ttu-id="dce4c-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="dce4c-106">Properties</span></span>

| <span data-ttu-id="dce4c-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="dce4c-107">Property</span></span>     | <span data-ttu-id="dce4c-108">Тип</span><span class="sxs-lookup"><span data-stu-id="dce4c-108">Type</span></span>        | <span data-ttu-id="dce4c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dce4c-109">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="dce4c-110">ластсигниндатетиме</span><span class="sxs-lookup"><span data-stu-id="dce4c-110">lastSignInDateTime</span></span>|<span data-ttu-id="dce4c-111">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dce4c-111">DateTimeOffset</span></span>|<span data-ttu-id="dce4c-112">Дата последнего входа для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="dce4c-112">The last sign-in date for a specific user.</span></span> <span data-ttu-id="dce4c-113">С помощью этого поля можно вычислить время последнего входа пользователя в каталог.</span><span class="sxs-lookup"><span data-stu-id="dce4c-113">You can use this field to calculate the last time a user signed in to the directory.</span></span> <span data-ttu-id="dce4c-114">Это поле можно использовать для создания отчетов, например неактивных пользователей.</span><span class="sxs-lookup"><span data-stu-id="dce4c-114">This field can be used to build reports, such as inactive users.</span></span> <span data-ttu-id="dce4c-115">Метка времени представляет сведения о времени и дате с использованием формата ISO 8601 (всегда используется формат UTC).</span><span class="sxs-lookup"><span data-stu-id="dce4c-115">The timestamp represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="dce4c-116">Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="dce4c-116">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="dce4c-117">ластсигнинрекуестид</span><span class="sxs-lookup"><span data-stu-id="dce4c-117">lastSignInRequestId</span></span>|<span data-ttu-id="dce4c-118">String</span><span class="sxs-lookup"><span data-stu-id="dce4c-118">String</span></span>|<span data-ttu-id="dce4c-119">Идентификатор запроса последнего входа, выполненного этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="dce4c-119">Request ID of the last sign-in performed by this user.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="dce4c-120">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="dce4c-120">JSON representation</span></span>

<span data-ttu-id="dce4c-121">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="dce4c-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.signInActivity",
  "baseType": null
}-->

```json
{
  "lastSignInDateTime": "String (timestamp)",
  "lastSignInRequestId": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "signInActivity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->