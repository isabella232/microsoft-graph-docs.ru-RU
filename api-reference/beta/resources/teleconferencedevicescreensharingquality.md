---
title: Тип ресурса Телеконференцедевицескриншарингкуалити
description: Представляет данные о качестве устройства для демонстрации видеоконференций с видеоконференциями.
localization_priority: Normal
author: dongkyun
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: 4441d249ced2ad0fc81ec4c7f70bc6e762566bac
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48046242"
---
# <a name="teleconferencedevicescreensharingquality-resource-type"></a>Тип ресурса Телеконференцедевицескриншарингкуалити

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет данные о качестве устройства для демонстрации видеоконференций с видеоконференциями.

## <a name="properties"></a>Свойства

**Телеконференцедевицескриншарингкуалити** наследует все свойства из [телеконференцедевицевидеокуалити](teleconferencedevicevideoquality.md).

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.teleconferenceDeviceScreenSharingQuality",
  "baseType": "microsoft.graph.teleconferenceDeviceVideoQuality"
}-->

```json
{
  "averageInboundBitRate": 1024,
  "averageInboundFrameRate": 1024,
  "averageInboundJitter": "String (ISO 8601 duration)",
  "averageInboundPacketLossRateInPercentage": 10,
  "averageInboundRoundTripDelay": "String (ISO 8601 duration)",
  "averageOutboundBitRate": 1024,
  "averageOutboundFrameRate": 1024,
  "averageOutboundJitter": "String (ISO 8601 duration)",
  "averageOutboundPacketLossRateInPercentage": 10,
  "averageOutboundRoundTripDelay": "String (ISO 8601 duration)",
  "channelIndex": 1,
  "inboundPackets": 1024,
  "localIPAddress": "String",
  "localPort": 2000,
  "maximumInboundJitter": "String (ISO 8601 duration)",
  "maximumInboundPacketLossRateInPercentage": 12,
  "maximumInboundRoundTripDelay": "String (ISO 8601 duration)",
  "maximumOutboundJitter": "String (ISO 8601 duration)",
  "maximumOutboundPacketLossRateInPercentage": 12,
  "maximumOutboundRoundTripDelay": "String (ISO 8601 duration)",
  "mediaDuration": "String (ISO 8601 duration)",
  "networkLinkSpeedInBytes": 1000000,
  "outboundPackets": 1024,
  "remoteIPAddress": "String",
  "remotePort": 3000
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teleconferenceDeviceScreenSharingQuality resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


