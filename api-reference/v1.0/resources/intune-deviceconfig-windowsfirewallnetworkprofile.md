---
title: Тип ресурса windowsFirewallNetworkProfile
description: Политики профилей брандмауэра Windows.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: f95258e83603f29990af120624ae91b6a389df74
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48091539"
---
# <a name="windowsfirewallnetworkprofile-resource-type"></a>Тип ресурса windowsFirewallNetworkProfile

Пространство имен: microsoft.graph

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Политики профилей брандмауэра Windows.

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|firewallEnabled|[статеманажементсеттинг](../resources/intune-deviceconfig-statemanagementsetting.md)|Настраивает ведущее устройство на разрешение или блокировку брандмауэра и дополнительной безопасности для профиля сети. Возможные значения: `notConfigured`, `blocked`, `allowed`.|
|stealthModeBlocked|Boolean|Предотвращение работы сервера в скрытом режиме. Если для Стеалсмодерекуиред и Стеалсмодеблоккед задано значение true, Стеалсмодеблоккед имеет приоритет.|
|incomingTrafficBlocked|Boolean|Настраивает брандмауэр на блокировку всего входящего трафика независимо от других параметров политики. Если для Инкомингтраффикрекуиред и Инкомингтраффикблоккед задано значение true, Инкомингтраффикблоккед имеет приоритет.|
|unicastResponsesToMulticastBroadcastsBlocked|Boolean|Настраивает брандмауэр для блокировки одноадресных ответов на многоадресный широковещательный трафик. Если для Уникастреспонсестомултикастброадкастсрекуиред и Уникастреспонсестомултикастброадкастсблоккед задано значение true, UnicastResponsesToMulticastBroadcastsBlocked имеет приоритет.|
|inboundNotificationsBlocked|Boolean|Запрещает брандмауэру отображать уведомления, если приложение заблокировано для прослушивания порта. Если для Инбаунднотификатионсрекуиред и Инбаунднотификатионсблоккед задано значение true, Инбаунднотификатионсблоккед имеет приоритет.|
|authorizedApplicationRulesFromGroupPolicyMerged|Boolean|Настраивает брандмауэр для объединения авторизованных правил приложений из групповой политики с элементами из локального хранилища, а не без учета правил локального хранилища. Если для Аусоризедаппликатионрулесфромграупполицинотмержед и Аусоризедаппликатионрулесфромграупполицимержед задано значение true, AuthorizedApplicationRulesFromGroupPolicyMerged имеет приоритет.|
|globalPortRulesFromGroupPolicyMerged|Boolean|Настраивает брандмауэр для объединения глобальных правил портов из групповой политики с политиками из локального хранилища, а не без учета правил локального хранилища. Если для Глобалпортрулесфромграупполицинотмержед и Глобалпортрулесфромграупполицимержед задано значение true, GlobalPortRulesFromGroupPolicyMerged имеет приоритет.|
|connectionSecurityRulesFromGroupPolicyMerged|Boolean|Настраивает брандмауэр для объединения правил безопасности подключений из групповой политики с политиками из локального хранилища, а не без учета правил локального хранилища. Если для Коннектионсекуритирулесфромграупполицинотмержед и Коннектионсекуритирулесфромграупполицимержед задано значение true, ConnectionSecurityRulesFromGroupPolicyMerged имеет приоритет.|
|outboundConnectionsBlocked|Boolean|Настраивает брандмауэр на блокировку всех исходящих подключений по умолчанию. Если для Аутбаундконнектионсрекуиред и Аутбаундконнектионсблоккед задано значение true, Аутбаундконнектионсблоккед имеет приоритет. Этот параметр будет применяться к выпускам Windows версии 1809 и более поздних версий.|
|inboundConnectionsBlocked|Boolean|Настраивает брандмауэр на блокировку всех входящих подключений по умолчанию. Если для Инбаундконнектионсрекуиред и Инбаундконнектионсблоккед задано значение true, Инбаундконнектионсблоккед имеет приоритет.|
|securedPacketExemptionAllowed|Boolean|Настраивает брандмауэр, чтобы разрешить ведущему компьютеру отвечать на нежелательный сетевой трафик этого трафика, защищенный IPSec, даже если для Стеалсмодеблоккед задано значение true. Если для Секуредпаккетексемптионблоккед и Секуредпаккетексемптионалловед задано значение true, Секуредпаккетексемптионалловед имеет приоритет.|
|policyRulesFromGroupPolicyMerged|Boolean|Настраивает брандмауэр для объединения политик правил брандмауэра из групповой политики с политиками из локального хранилища, а не без учета правил локального хранилища. Если для Полицирулесфромграупполицинотмержед и Полицирулесфромграупполицимержед задано значение true, Полицирулесфромграупполицимержед имеет приоритет.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsFirewallNetworkProfile",
  "firewallEnabled": "String",
  "stealthModeBlocked": true,
  "incomingTrafficBlocked": true,
  "unicastResponsesToMulticastBroadcastsBlocked": true,
  "inboundNotificationsBlocked": true,
  "authorizedApplicationRulesFromGroupPolicyMerged": true,
  "globalPortRulesFromGroupPolicyMerged": true,
  "connectionSecurityRulesFromGroupPolicyMerged": true,
  "outboundConnectionsBlocked": true,
  "inboundConnectionsBlocked": true,
  "securedPacketExemptionAllowed": true,
  "policyRulesFromGroupPolicyMerged": true
}
```









