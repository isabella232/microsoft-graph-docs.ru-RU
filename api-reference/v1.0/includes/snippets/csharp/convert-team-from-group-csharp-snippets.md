---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 34c55765e34c83c87bf0b24941c2270f70417186
ms.sourcegitcommit: c4366ac71cf496242c8ff435bc8d8b3816bdc1aa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2020
ms.locfileid: "48315370"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var team = new Team
{
    Channels = (ITeamChannelsCollectionPage)new List<Channel>()
    {
        new Channel
        {
            DisplayName = "Class Announcements 📢",
            IsFavoriteByDefault = true
        },
        new Channel
        {
            DisplayName = "Homework 🏋️",
            IsFavoriteByDefault = true
        }
    },
    MemberSettings = new TeamMemberSettings
    {
        AllowCreateUpdateChannels = false,
        AllowDeleteChannels = false,
        AllowAddRemoveApps = false,
        AllowCreateUpdateRemoveTabs = false,
        AllowCreateUpdateRemoveConnectors = false
    },
    InstalledApps = (ITeamInstalledAppsCollectionPage)new List<TeamsAppInstallation>()
    {
        new TeamsAppInstallation
        {
            AdditionalData = new Dictionary<string, object>()
            {
                {"teamsApp@odata.bind", "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.vsts')"}
            }
        },
        new TeamsAppInstallation
        {
            AdditionalData = new Dictionary<string, object>()
            {
                {"teamsApp@odata.bind", "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('1542629c-01b3-4a6d-8f76-1938b779e48d')"}
            }
        }
    },
    AdditionalData = new Dictionary<string, object>()
    {
        {"template@odata.bind", "https://graph.microsoft.com/beta/teamsTemplates('standard')"},
        {"group@odata.bind", "https://graph.microsoft.com/v1.0/groups('groupId')"}
    }
};

await graphClient.Teams
    .Request()
    .AddAsync(team);

```