---
title: Отчеты об активных пользователях Microsoft 365
description: Вы можете использовать отчет по активным пользователям Microsoft 365, чтобы узнать, сколько лицензий используется отдельными пользователями в вашей организации, и детализировать информацию о том, какие пользователи используют продукты. Этот отчет поможет администраторам выяснить, какие продукты используются редко, или определить пользователей, которым могут понадобиться дополнительное обучение и сведения.
localization_priority: Normal
ms.prod: reports
author: pranoychaudhuri
doc_type: conceptualPageType
ms.openlocfilehash: 3d795c3308b7c1494bbff2a24545ba4ca8053583
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48021254"
---
# <a name="microsoft-365-active-users-reports"></a>Отчеты об активных пользователях Microsoft 365

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Вы можете использовать отчет по активным пользователям Microsoft 365, чтобы узнать, сколько лицензий используется отдельными пользователями в вашей организации, и детализировать информацию о том, какие пользователи используют продукты. Этот отчет поможет администраторам выяснить, какие продукты используются редко, или определить пользователей, которым могут понадобиться дополнительное обучение и сведения.

> **Примечание:** Подробные сведения о различных представлениях и именах отчетов можно найти в [статье Microsoft 365 отчеты об активных пользователях](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).

## <a name="reports"></a>Отчеты
| Функция                                 | Возвращаемый тип CSV | Возвращаемый тип JSON                         | Описание                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Получение сведений о пользователях](../api/reportroot-getoffice365activeuserdetail.md) | Stream          | [office365ActiveUserDetail](../resources/office365activeuserdetail.md) | Получение сведений о активных пользователях Microsoft 365. |
| [Получение количества пользователей](../api/reportroot-getoffice365activeusercounts.md) | Stream          | [office365ActiveUserCounts](../resources/office365activeusercounts.md) | Узнайте, сколько активных пользователей в день было у каждого продукта в отчетный период. |
| [Получение количества пользователей по службам](../api/reportroot-getoffice365servicesusercounts.md) | Поток          | [office365ServicesUserCounts](../resources/office365servicesusercounts.md) | Узнайте, сколько пользователей были активны и неактивны в каждой службе. |


