---
title: Отчеты об использовании устройств со Skype для бизнеса
description: Вы можете получить сведения о типах клиентов и устройств, используемых в Организации. Эти данные могут пригодиться при проведении анализа, планировании и принятии других бизнес-решений для организации.
localization_priority: Normal
ms.prod: reports
author: pranoychaudhuri
doc_type: conceptualPageType
ms.openlocfilehash: ef75a4b29a82cdd05b2fb726806b0732dc36c9fd
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47997657"
---
# <a name="skype-for-business-device-usage-reports"></a>Отчеты об использовании устройств со Skype для бизнеса

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Вы можете получить сведения о типах клиентов и устройств, используемых в Организации. Эти данные могут пригодиться при проведении анализа, планировании и принятии других бизнес-решений для организации.

> **Примечание:** Сведения о различных представлениях отчетов и их именах можно найти в [статье Microsoft 365 Reports-клиенты Skype для бизнеса](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).

## <a name="reports"></a>Отчеты

| Функция                                 | Возвращаемый тип CSV | Возвращаемый тип JSON                         | Описание                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Получение сведений о пользователях](../api/reportroot-getskypeforbusinessdeviceusageuserdetail.md) | Stream          | [скипефорбусинессдевицеусажеусердетаил](../resources/skypeforbusinessdeviceusageuserdetail.md) | Получите сведения об использовании устройств со Skype для бизнеса с разбивкой по пользователям. |
| [Получение количества пользователей с разбивкой по устройствам](../api/reportroot-getskypeforbusinessdeviceusagedistributionusercounts.md) | Stream          | [скипефорбусинессдевицеусажедистрибутионусеркаунтс](../resources/skypeforbusinessdeviceusagedistributionusercounts.md) | Узнайте, сколько сотрудников организации используют уникальные устройства. В отчете будет показано количество пользователей устройств с Windows, телефонов с Windows, телефонов с Android, iPhone и iPad. |
| [Получение количества пользователей](../api/reportroot-getskypeforbusinessdeviceusageusercounts.md) | Stream          | [скипефорбусинессдевицеусажеусеркаунтс](../resources/skypeforbusinessdeviceusageusercounts.md) | Отследите динамику использования по количеству пользователей в организации, подключавшихся с помощью приложения Skype для бизнеса. Кроме того, вы получите статистические данные с разбивкой по типу устройства (устройство с Windows, телефон с Windows, телефон с Android, iPhone или iPad), на котором установлено клиентское приложение Skype для бизнеса, используемое в организации. |


