---
title: тип перечисления Виндовспривацидатаакцесслевел
description: Определите категорию уровня доступа к определенной конфиденциальной информации Windows.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: acd71682d7e682dec53bb87885374aabdd38089d
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49215193"
---
# <a name="windowsprivacydataaccesslevel-enum-type"></a>тип перечисления Виндовспривацидатаакцесслевел

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Определите категорию уровня доступа к определенной конфиденциальной информации Windows.

## <a name="members"></a>Элементы
|Элемент|Значение|Описание|
|:---|:---|:---|
|notConfigured|нуль|Уровень доступа не указан, нет целей. Устройство может вести себя как в Усеринконтрол, так и Форцеаллов. Это может зависеть от данных о конфиденциальности, а также версий Windows и других факторов.|
|форцеаллов|1,1|Приложениям будет разрешен доступ к указанным данным о конфиденциальности.|
|форцедени|2|Приложениям будет отказано в доступе к указанным данным о конфиденциальности.|
|усеринконтрол|4|Пользователи будут получать приглашение при попытке приложения получить доступ к указанным данным о конфиденциальности.|




