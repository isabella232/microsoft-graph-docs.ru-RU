---
title: Работа с API отчетов об использовании методов проверки подлинности
description: Отчет об использовании способов проверки подлинности помогает Организации определить, как их конечные пользователи используют функции Azure Active Directory, такие как самостоятельный сброс паролей и многофакторная проверка подлинности (MFA).
localization_priority: Normal
author: khotz
ms.prod: microsoft-identity-platform
doc_type: conceptualPageType
ms.openlocfilehash: 6d626c558dd7728d08682e5eebce138a5197f5b6
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "48402303"
---
# <a name="working-with-the-authentication-methods-usage-report-api"></a>Работа с API отчетов об использовании методов проверки подлинности

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Отчеты об использовании методов проверки подлинности позволяют понять, как пользователи в вашей организации используют функции Azure Active Directory (Azure AD), такие как самостоятельный сброс пароля и многофакторная проверка подлинности (MFA).

В этих отчетах представлены следующие сведения:

- Методы проверки подлинности более успешны для Организации. 
- Сведения об ошибках, с которыми работает конечный пользователь.
- Какую кампанию необходимо выполнить, чтобы помочь конечным пользователям принять использование REST пароля и MFA для самостоятельного пароля.

## <a name="common-requests"></a>Общие запросы

В следующей таблице перечислены некоторые распространенные запросы, которые можно использовать с этим API.

| Операция | Попробовать в песочнице Graph | Описание |
| --------- | --- | ----------- |
| [жеткредентиалусеррегистратионкаунт](/graph/api/resources/credentialuserregistrationcount?view=graph-rest-beta) | [ПОЛУЧЕНИЕ/кредентиалусеррегистратионкаунт](https://developer.microsoft.com/graph/graph-explorer?request=reports/getCredentialUserRegistrationcount()&version=beta) | Получение числа пользователей, зарегистрированных для самостоятельного сброса пароля и MFA. |
| [жеткредентиалусажесуммари](/graph/api/resources/credentialusagesummary?view=graph-rest-beta) | [ПОЛУЧЕНИЕ/кредентиалусажесуммари](https://developer.microsoft.com/graph/graph-explorer?request=reports/getCredentialUsageSummary&version=beta) | Получение числа пользователей, использующих самостоятельный сброс пароля. |
| [кредентиалусеррегистратиондетаилс](/graph/api/resources/credentialuserregistrationdetails?view=graph-rest-beta) | [ПОЛУЧЕНИЕ/кредентиалусеррегистратиондетаилс](https://developer.microsoft.com/graph/graph-explorer?request=reports/credentialUserRegistrationDetails&version=beta) | Получение сведений о пользователях для самостоятельного сброса пароля и действий регистрации MFA. |
| [усеркредентиалусажедетаилс](/graph/api/resources/usercredentialusagedetails?view=graph-rest-beta) | [ПОЛУЧЕНИЕ/усеркредентиалусажедетаилс](https://developer.microsoft.com/graph/graph-explorer?request=reports/userCredentialUsageDetails&version=beta) | Получение сведений о пользователях для всех действий самостоятельного сброса пароля. |

## <a name="licenses"></a>Лицензии

Отчеты об использовании доступны для лицензионных функций, которые используют преимущества самостоятельного сброса пароля и MFA в клиенте.

## <a name="next-steps"></a>Дальнейшие действия

- Сведения о [развертывании средства самообслуживания Azure Active Directory для самостоятельного сброса пароля](/azure/active-directory/authentication/howto-sspr-deployment).
- Узнайте, как развернуть [Azure Active Directory MFA](/azure/active-directory/authentication/howto-mfa-getstarted).
- Узнайте, как включить [регистрацию сведений о безопасности в сочетании](/azure/active-directory/authentication/howto-registration-mfa-sspr-combined).