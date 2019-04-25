---
title: Тип ресурса automaticRepliesSetting
description: 'Параметры конфигурации для автоматического уведомления отправителя о входящих сообщениях электронной почты с сообщением из '
localization_priority: Normal
ms.openlocfilehash: 5ff16aa93042e0d66063cb62de7a8dcdf870c892
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32543865"
---
# <a name="automaticrepliessetting-resource-type"></a><span data-ttu-id="2bdeb-103">Тип ресурса automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="2bdeb-103">automaticRepliesSetting resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="2bdeb-p101">Параметры для настройки автоматического уведомления отправителя письма с помощью сообщения от пользователя, выполнившего вход. Например, для отправки автоматического ответа с уведомлением о том, что пользователь, выполнивший вход, не может отвечать на электронные сообщения.</span><span class="sxs-lookup"><span data-stu-id="2bdeb-p101">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user. For example, an automatic reply to notify that the signed-in user is unavailable to respond to emails.</span></span> 


## <a name="properties"></a><span data-ttu-id="2bdeb-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="2bdeb-106">Properties</span></span>
| <span data-ttu-id="2bdeb-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="2bdeb-107">Property</span></span>     | <span data-ttu-id="2bdeb-108">Тип</span><span class="sxs-lookup"><span data-stu-id="2bdeb-108">Type</span></span>   |<span data-ttu-id="2bdeb-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2bdeb-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2bdeb-110">Екстерналаудиенце</span><span class="sxs-lookup"><span data-stu-id="2bdeb-110">externalAudience</span></span>|<span data-ttu-id="2bdeb-111">String</span><span class="sxs-lookup"><span data-stu-id="2bdeb-111">String</span></span>| <span data-ttu-id="2bdeb-p102">Внешняя аудитория по отношению к организации пользователя, выполнившего вход, которая получит сообщение **ExternalReplyMessage**, если для параметра **Status** задано значение `AlwaysEnabled` или `Scheduled`. Возможные значения: `none`, `contactsOnly`, `all`.</span><span class="sxs-lookup"><span data-stu-id="2bdeb-p102">The set of audience external to the signed-in user's organization who will receive the **ExternalReplyMessage**, if **Status** is `AlwaysEnabled` or `Scheduled`. Possible values are: `none`, `contactsOnly`, `all`.</span></span>|
|<span data-ttu-id="2bdeb-114">Екстерналреплимессаже</span><span class="sxs-lookup"><span data-stu-id="2bdeb-114">externalReplyMessage</span></span>|<span data-ttu-id="2bdeb-115">string</span><span class="sxs-lookup"><span data-stu-id="2bdeb-115">string</span></span>|<span data-ttu-id="2bdeb-116">Автоматический ответ, который нужно отправить указанной внешней аудитории, если для параметра **Status** задано значение `AlwaysEnabled` или `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2bdeb-116">The automatic reply to send to the specified external audience, if **Status** is `AlwaysEnabled` or `Scheduled`.</span></span>|
|<span data-ttu-id="2bdeb-117">Интерналреплимессаже</span><span class="sxs-lookup"><span data-stu-id="2bdeb-117">internalReplyMessage</span></span>|<span data-ttu-id="2bdeb-118">string</span><span class="sxs-lookup"><span data-stu-id="2bdeb-118">string</span></span>|<span data-ttu-id="2bdeb-119">Автоматический ответ, который нужно отправить сотрудникам организации пользователя, выполнившего вход, если для параметра **Status** задано значение `AlwaysEnabled` или `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2bdeb-119">The automatic reply to send to the audience internal to the signed-in user's organization, if **Status** is `AlwaysEnabled` or `Scheduled`.</span></span> |
|<span data-ttu-id="2bdeb-120">scheduledEndDateTime</span><span class="sxs-lookup"><span data-stu-id="2bdeb-120">scheduledEndDateTime</span></span>|[<span data-ttu-id="2bdeb-121">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="2bdeb-121">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="2bdeb-122">Дата и время завершения отправки автоматических ответов, если для параметра **Status** установлено значение `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2bdeb-122">The date and time that automatic replies are set to end, if **Status** is set to `Scheduled`.</span></span> |
|<span data-ttu-id="2bdeb-123">scheduledStartDateTime</span><span class="sxs-lookup"><span data-stu-id="2bdeb-123">scheduledStartDateTime</span></span>|[<span data-ttu-id="2bdeb-124">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="2bdeb-124">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="2bdeb-125">Дата и время начала отправки автоматических ответов, если для параметра **Status** установлено значение `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2bdeb-125">The date and time that automatic replies are set to begin, if **Status** is set to `Scheduled`.</span></span>|
|<span data-ttu-id="2bdeb-126">status</span><span class="sxs-lookup"><span data-stu-id="2bdeb-126">status</span></span>|<span data-ttu-id="2bdeb-127">String</span><span class="sxs-lookup"><span data-stu-id="2bdeb-127">String</span></span>|<span data-ttu-id="2bdeb-p103">Состояние настройки автоматических ответов. Возможные значения: `disabled`, `alwaysEnabled`, `scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2bdeb-p103">Configurations status for automatic replies. Possible values are: `disabled`, `alwaysEnabled`, `scheduled`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2bdeb-130">Представление в формате JSON</span><span class="sxs-lookup"><span data-stu-id="2bdeb-130">JSON representation</span></span>

<span data-ttu-id="2bdeb-131">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="2bdeb-131">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.automaticRepliesSetting"
}-->

```json
{
  "externalAudience": "String",
  "externalReplyMessage": "string",
  "internalReplyMessage": "string",
  "scheduledEndDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "scheduledStartDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "status": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "automaticRepliesSetting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/automaticrepliessetting.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
