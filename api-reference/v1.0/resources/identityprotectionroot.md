---
title: API защиты удостоверений
description: Тип ресурса Идентитипротектионрут
author: cloudhandler
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: ab01fb11d7973adf056685f6ab0d6ef02e2ecb4d
ms.sourcegitcommit: 577bfd3bb8a2e2679ef1c5942a4a496c2aa3a277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2020
ms.locfileid: "48581304"
---
# <a name="identityprotectionroot-resource-type"></a>Тип ресурса Идентитипротектионрут

Пространство имен: microsoft.graph

Защита удостоверений — это средство, которое позволяет организациям находить, анализировать и устранять риски на основе удостоверений в своей среде. С помощью следующих API Microsoft Graph можно запрашивать риски, обнаруженные в целях защиты идентификации. 

* [рискдетектион](riskdetection.md) — запросить Microsoft Graph, чтобы получить список обнаруженных рисков и связанных с входом рисков, а также связанные сведения об обнаружении. Обнаружение рисков в службе идентификации Azure AD включает все определенные подозрительные действия, связанные с учетными записями пользователей в каталоге.

* [riskyUsers](riskyuser.md) — запрос Microsoft Graph для получения сведений о пользователях, которые были признаны опасными для защиты удостоверений. Риск для пользователей представляет вероятность, с которой заданный идентификатор или учетная запись скомпрометирована. Эти риски рассчитываются в автономном режиме с помощью внутренних и внешних источников системы анализа угроз Майкрософт, в том числе исследователей, специалистов по обеспечению безопасности, ИТ-специалистов, Teams корпорации Майкрософт и других надежных источников.

* [Signing](signin.md) — запрос Microsoft Graph для получения сведений о входах Azure AD с определенными свойствами, связанными с состоянием риска, подробным описанием и уровнем. Риск входа представляет вероятность того, что владелец удостоверения не уполномочен на данный запрос проверки подлинности. Эти риски можно рассчитать в режиме реального времени или в автономном режиме с помощью внутренних и внешних источников интеллектуального анализа данных Майкрософт, в том числе исследователей, специалистов по обеспечению безопасности, ИТ-специалистов, Teams корпорации Майкрософт и других надежных источников.

## <a name="what-can-i-do-with-identity-protection-apis-in-microsoft-graph"></a>Что можно делать с API защиты удостоверений в Microsoft Graph?

Ниже приведены популярные запросы для работы с данными журнала аудита.

Operation | URL-адрес
:----------|:----
ПОЛУЧЕНИЕ рискованных пользователей | [GET https://graph.microsoft.com/v1.0/identityProtection/riskyUsers](https://developer.microsoft.com/graph/graph-explorer?request=identityProtection/riskyUsers&version=v1.0)
ПОЛУЧЕНИЕ обнаруженных рисков | [GET https://graph.microsoft.com/v1.0/identityProtection/riskDetections](https://developer.microsoft.com/graph/graph-explorer?request=identityProtection/riskDetections&version=v1.0)
ПОЛУЧЕНИЕ журнала рисков пользователя | [GET https://graph.microsoft.com/v1.0/identityProtection/riskyUsers/{riskyUserId}/history](https://developer.microsoft.com/graph/graph-explorer?request=identityProtection/riskyUsers/{riskyUserId}/history&version=v1.0)
ПОДТВЕРЖДЕНИЕ того, что пользователь скомпрометирован | [Поместить https://graph.microsoft.com/v1.0/identityProtection/riskyUsers/confirmCompromised](https://developer.microsoft.com/graph/graph-explorer?request=/identityProtection/riskyUsers/confirmCompromised&version=v1.0)
ОТКЛОНЕНие опасного пользователя | [Поместить https://graph.microsoft.com/v1.0/identityProtection/riskyUsers/dismiss](https://developer.microsoft.com/graph/graph-explorer?request=/identityProtection/riskyUsers/dismiss&version=v1.0)

## <a name="what-licenses-do-i-need"></a>Какие лицензии нужны?

Защита удостоверений Azure AD — это функция Premium. Для доступа к API Рискдетектион требуется лицензия Azure AD Premium P1 или P2 (Примечание: Лицензия P1 получает сведения об ограниченных рисках). API riskyUsers доступен только для лицензий Azure AD Premium P2.

## <a name="see-also"></a>См. также

* [Сведения о защите удостоверений Azure Active Directory](/azure/active-directory/identity-protection/overview-identity-protection)
* [Начало работы с защитой удостоверений Azure Active Directory и Microsoft Graph](/azure/active-directory/identity-protection/howto-identity-protection-graph-api)