---
title: тип перечисления Ембеддедсимдевицестатевалуе
description: Описывает различные состояния для встроенного кода активации SIM-карты.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: enumPageType
ms.openlocfilehash: 44cc4482677fd353a2bbbcc275e4f927a1b3f80a
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49288371"
---
# <a name="embeddedsimdevicestatevalue-enum-type"></a>тип перечисления Ембеддедсимдевицестатевалуе

Пространство имен: microsoft.graph

> **Важно!** API Microsoft Graph в версии/Beta могут изменяться; рабочее использование не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Описывает различные состояния для встроенного кода активации SIM-карты.

## <a name="members"></a>Элементы
|Элемент|Значение|Описание|
|:---|:---|:---|
|нотевалуатед|нуль|Указывает, что встроенный код активации SIM-карты свободен и доступен для назначения устройству.|
|сбоев|1,1|Указывает, что службе Intune не удалось доставить этот профиль устройству.|
|устанавливать|2|Указывает, что встроенный код активации SIM-карты назначен устройству, и устройство устанавливает маркер.|
|устанавлива|4|Указывает на то, что встроенный код активации SIM-карты успешно установлен на целевом устройстве.|
|удалять|4 |Указывает, что служба Intune пытается удалить профиль с устройства.|
|error|5 |Указывает на наличие ошибки в этом профиле.|
|deleted|6 |Указывает, что профиль будет удален с устройства.|
|ремоведбюсер|7 |Указывает, что профиль удаляется с устройства пользователем|




