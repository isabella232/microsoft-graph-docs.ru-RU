---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a5bf205fe7beb149a175bf8ead06ccd042d01cdd
ms.sourcegitcommit: c650b95ef4d0c3e93e2eb36cd6b52ed31200164f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "44684940"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var quality = new TeleconferenceDeviceQuality
{
    CallChainId = Guid.Parse("0622673d-9f69-49b3-9d4f-5ec64f42ecce"),
    ParticipantId = Guid.Parse("ea078406-b5d4-4d3c-b85e-90103dcec7f6"),
    MediaLegId = Guid.Parse("bd9ee398-4b9d-42c7-8b8d-4e8efad9435f"),
    DeviceName = "TestAgent",
    DeviceDescription = "TestDescription",
    MediaQualityList = new List<TeleconferenceDeviceMediaQuality>()
    {
        new TeleconferenceDeviceAudioQuality
        {
            ChannelIndex = 1,
            MediaDuration = new Duration("PT20M"),
            NetworkLinkSpeedInBytes = 13000,
            LocalIPAddress = "127.0.0.1",
            LocalPort = 6300,
            RemoteIPAddress = "102.1.1.101",
            RemotePort = 6301,
            InboundPackets = 5500,
            OutboundPackets = 5400,
            AverageInboundPacketLossRateInPercentage = 0.01,
            AverageOutboundPacketLossRateInPercentage = 0.02,
            MaximumInboundPacketLossRateInPercentage = 0.05,
            MaximumOutboundPacketLossRateInPercentage = 0.06,
            AverageInboundRoundTripDelay = new Duration("PT0.03S"),
            AverageOutboundRoundTripDelay = new Duration("PT0.04S"),
            MaximumInboundRoundTripDelay = new Duration("PT0.13S"),
            MaximumOutboundRoundTripDelay = new Duration("PT0.14S"),
            AverageInboundJitter = new Duration("PT0.01S"),
            AverageOutboundJitter = new Duration("PT0.015S"),
            MaximumInboundJitter = new Duration("PT0.023S"),
            MaximumOutboundJitter = new Duration("PT0.024S")
        },
        new TeleconferenceDeviceVideoQuality
        {
            ChannelIndex = 1,
            MediaDuration = new Duration("PT20M"),
            NetworkLinkSpeedInBytes = 13000,
            LocalIPAddress = "127.0.0.1",
            LocalPort = 6300,
            RemoteIPAddress = "102.1.1.101",
            RemotePort = 6301,
            InboundPackets = 5500,
            OutboundPackets = 5400,
            AverageInboundPacketLossRateInPercentage = 0.01,
            AverageOutboundPacketLossRateInPercentage = 0.02,
            MaximumInboundPacketLossRateInPercentage = 0.05,
            MaximumOutboundPacketLossRateInPercentage = 0.06,
            AverageInboundRoundTripDelay = new Duration("PT0.03S"),
            AverageOutboundRoundTripDelay = new Duration("PT0.04S"),
            MaximumInboundRoundTripDelay = new Duration("PT0.13S"),
            MaximumOutboundRoundTripDelay = new Duration("PT0.14S"),
            AverageInboundJitter = new Duration("PT0.01S"),
            AverageOutboundJitter = new Duration("PT0.015S"),
            MaximumInboundJitter = new Duration("PT0.023S"),
            MaximumOutboundJitter = new Duration("PT0.024S")
        },
        new TeleconferenceDeviceScreenSharingQuality
        {
            ChannelIndex = 1,
            MediaDuration = new Duration("PT20M"),
            NetworkLinkSpeedInBytes = 13000,
            LocalIPAddress = "127.0.0.1",
            LocalPort = 6300,
            RemoteIPAddress = "102.1.1.101",
            RemotePort = 6301,
            InboundPackets = 5500,
            OutboundPackets = 5400,
            AverageInboundPacketLossRateInPercentage = 0.01,
            AverageOutboundPacketLossRateInPercentage = 0.02,
            MaximumInboundPacketLossRateInPercentage = 0.05,
            MaximumOutboundPacketLossRateInPercentage = 0.06,
            AverageInboundRoundTripDelay = new Duration("PT0.03S"),
            AverageOutboundRoundTripDelay = new Duration("PT0.04S"),
            MaximumInboundRoundTripDelay = new Duration("PT0.13S"),
            MaximumOutboundRoundTripDelay = new Duration("PT0.14S"),
            AverageInboundJitter = new Duration("PT0.01S"),
            AverageOutboundJitter = new Duration("PT0.015S"),
            MaximumInboundJitter = new Duration("PT0.023S"),
            MaximumOutboundJitter = new Duration("PT0.024S")
        }
    }
};

await graphClient.Communications.Calls
    .LogTeleconferenceDeviceQuality(quality)
    .Request()
    .PostAsync();

```