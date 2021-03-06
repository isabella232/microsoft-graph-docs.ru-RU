---
title: Начало работы с подключениями к данным в Microsoft Graph
description: 'Прежде чем использовать подключение к данным Microsoft Graph, администратору Microsoft 365 необходимо выполнить два действия, которые включают возможность управления перемещением данных для администраторов через Privileged Access Management (PAM). '
author: ajacks-msft
localization_priority: Priority
ms.prod: data-connect
ms.openlocfilehash: f451da704c0fce255f37b61da7c7446145d8afd1
ms.sourcegitcommit: 7153a13f4e95c7d9fed3f2c10a3d075ff87b368d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "44897283"
---
# <a name="get-started-with-microsoft-graph-data-connect"></a>Начало работы с подключениями к данным в Microsoft Graph

Прежде чем использовать подключение к данным Microsoft Graph, администратору Microsoft 365 необходимо выполнить два действия, которые включают возможность управления перемещением данных для администраторов через Privileged Access Management (PAM). 

1. Дайте согласие на участие в подключении данных Microsoft Graph через портал Microsoft 365 Admin на странице **Службы и надстройки**. Это позволит Microsoft Azure осуществлять запросы на перемещение данных (вы сохраните полный контроль над данными, но разрешите ресурсам Azure доступ к ним). Данные не будут передаваться, пока не будет утвержден определенный конвейер.
2. Настройте группу безопасности, поддерживающую почту, или список рассылки в подписке Microsoft 365. Убедитесь, что утверждающая группа не пустая. Только пользователи в группе могут утверждать запросы на перемещение данных.

## <a name="next-steps"></a>Дальнейшие действия

Поздравляем! Теперь вы готовы к созданию интеллектуальных приложений с помощью инструментария Azure. Чтобы узнать подробные пошаговые инструкции, см. [учебный модуль по подключению данных в Microsoft Graph](https://github.com/microsoftgraph/msgraph-training-dataconnect/blob/master/Lab.md). Дополнительные сведения о возможностях, предоставляемых подключением к данным Microsoft Graph, см. в статьях о [наборах данных, регионах и приемниках](data-connect-datasets.md) и [выборе и фильтрации пользователей](data-connect-filtering.md), поддерживаемых подключением к данным.
