---
title: Тип ресурса iosNotificationSettings
description: Элемент, описывающий параметры уведомлений.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 0e3dc929e96869475d4376c344bf08ff17ae7edd
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48074988"
---
# <a name="iosnotificationsettings-resource-type"></a>Тип ресурса iosNotificationSettings

Пространство имен: microsoft.graph

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Элемент, описывающий параметры уведомлений.

## <a name="properties"></a>Свойства
|Свойство|Тип|Описание|
|:---|:---|:---|
|bundleID|String|Идентификатор пакета для приложения, к которому необходимо применить эти параметры уведомлений.|
|appName|String|Имя приложения, которое нужно связать со свойством bundleID.|
|publisher|String|Издатель, которого нужно связать со свойством bundleID.|
|enabled|Boolean|Указывает, разрешены ли уведомления для этого приложения.|
|showInNotificationCenter|Boolean|Указывает, можно ли отображать уведомления в центре уведомлений.|
|showOnLockScreen|Boolean|Указывает, можно ли отображать уведомления на экране блокировки.|
|alertType|[иоснотификатионалерттипе](../resources/intune-deviceconfig-iosnotificationalerttype.md)|Определяет тип оповещения для уведомлений, связанных с этим приложением. Возможные значения: `deviceDefault`, `banner`, `modal`, `none`.|
|badgesEnabled|Boolean|Указывает, разрешены ли эмблемы для этого приложения.|
|soundsEnabled|Boolean|Указывает, разрешены ли звуковые сигналы для этого приложения.|

## <a name="relationships"></a>Связи
Нет

## <a name="json-representation"></a>Представление JSON
Ниже представлено описание ресурса в формате JSON.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosNotificationSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosNotificationSettings",
  "bundleID": "String",
  "appName": "String",
  "publisher": "String",
  "enabled": true,
  "showInNotificationCenter": true,
  "showOnLockScreen": true,
  "alertType": "String",
  "badgesEnabled": true,
  "soundsEnabled": true
}
```









