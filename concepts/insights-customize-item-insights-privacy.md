---
title: Настройка элемента конфиденциальности insights в Microsoft Graph
description: ''
author: simonhult
localization_priority: Priority
ms.prod: insights
ms.custom: scenarios:getting-started
ms.openlocfilehash: 7a2e587692f5e1eb54d46887c46b00d0ca5692ce
ms.sourcegitcommit: 60ced1be6ed8dd2d23263090a1cfbc16689bb043
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "48782429"
---
# <a name="customizing-item-insights-privacy-in-microsoft-graph-preview"></a>Настройка элемента конфиденциальности insights в Microsoft Graph (предварительный просмотр)

Параметры конфиденциальности элемента insights позволяют настраивать видимость информации, получаемой из Microsoft Graph, между пользователями и другими элементами (например, документами и сайтами) в Microsoft 365. Вы можете отключить приложение Delve с помощью уже существующих элементов управления, но также использовать в дальнейшем другие полезные возможности, связанные с insights.

## <a name="background"></a>Общие сведения
На момент первого выпуска в 2014 году, Office Graph был внутренней службой для Delve. Был представлен набор элементов управления конфиденциальностью как в Office Graph, так и в пользовательском интерфейсе Delve. С тех пор Office Graph развивался и стал более независимой и мощной частью интерфейса Microsoft 365, а также Microsoft Graph. Чтобы предложить связанную схему Microsoft Graph, компания Майкрософт представила элемент [itemInsights](/graph/api/resources/iteminsights?view=graph-rest-beta&preserve-view=true), который наследует все свойства ранее существовавшего ресурса [officeGraphInsights](/graph/api/resources/officegraphinsights?view=graph-rest-beta&preserve-view=true), и сохранила **officeGraphInsights** для обеспечения обратной совместимости. Введение **itemInsights** также разделяет историю конфиденциальности на две независимые части.  

Хотя существующие приложения могут продолжать использовать **officeGraphInsights** , их следует обновить до **itemInsights** , чтобы обеспечить гибкую настройку элементов в Office Graph и Delve.

## <a name="how-to-customize-item-insights"></a>Как настроить элемент insights?

С помощью параметров аналитики элементов администраторы получают возможность гибко использовать инструменты Azure AD. Администраторы могут отключать аналитику элементов для всей организации или только для участников указанной группы Azure AD. Для настройки аналитики элементов можно использовать пакет SDK PowerShell SDK или API REST Microsoft Graph с соответствующими разрешениями. Помните, что требуется _роль глобального администратора_ . 

В следующем разделе описывается настройка параметров аналитики с помощью командлетов PowerShell. Если вы используете API REST, пропустите следующий раздел и перейдите к разделу [Настройка аналитики элементов с помощью API REST](#configure-item-insights-using-rest-api). Дополнительные сведения см. в описании операций REST [read](/graph/api/iteminsightssettings-get?view=graph-rest-beta&preserve-view=true) или [update](/graph/api/iteminsightssettings-update?view=graph-rest-beta&preserve-view=true).

### <a name="how-to-configure-item-insights-setting-via-powershell"></a>Как настроить параметры аналитики элементов с помощью PowerShell?
Убедитесь, что выполнены следующие дополнительные предварительные требования. После этого используйте [пакет SDK PowerShell Microsoft Graph](/graph/powershell/installation), чтобы настроить аналитику элементов для всей организации или для определенных групп.

#### <a name="additional-prerequisites"></a>Дополнительные предварительные требования
* **Модуль PowerShell** — установите [модуль версии 0.9.1 или более поздней](https://www.powershellgallery.com/packages/Microsoft.Graph).
* **.NET Framework** — установите [.NET Framework 4.7.2](https://dotnet.microsoft.com/download/dotnet-framework) или более поздней версии.

#### <a name="command-examples"></a>Примеры команд
Чтобы получить конфигурацию аналитики элементов для организации, используйте модуль PowerShell Microsoft Graph и следующую команду, заменив в ней `$OrgID` на применимый идентификатор вашей организации:
```powershell
   Get-MgOrganizationSettingItemInsight -OrganizationId $OrgID
```

По умолчанию аналитика элементов включена для всей организации. С помощью модуля PowerShell Microsoft Graph можно изменить это и отключить аналитику элементов для всех пользователей в организации. Используйте следующую команду, заменив `$OrgID` на идентификатор организации и указав `-IsEnabledInOrganization` как `false`:
```powershell
   Update-MgOrganizationSettingItemInsight -OrganizationId $OrgID -IsEnabledInOrganization:$false
```
Также можно изменить поведение по умолчанию и отключить аналитику элементов для определенной группы Azure AD. Используйте следующую команду, заменив `$OrgID` на идентификатор организации, а `$GroupID` — на идентификатор группы Azure AD:
```powershell
   Update-MgOrganizationSettingItemInsight -OrganizationId $OrgID -DisabledForGroup $GroupId
```

#### <a name="using-earlier-versions-of-the-powershell-module"></a>Использование ранних версий модуля PowerShell

Если вы используете модуль Microsoft Graph PowerShell версии 0.9.0 или более ранней, вызовите командлет `Update-MgOrganizationSettingItemInsight` одним из двух способов, как в следующих примерах: 

- Добавьте `-AdditionalProperties @{}` в конец команды:
  ```powershell
  Update-MgOrganizationSettingItemInsight -OrganizationId $OrgID -DisabledForGroup 28f9ceac-39aa-4829-9a67-b8f1db11eaa1 -AdditionalProperties @{}
  ```
- Также можно использовать `-BodyParameter`: 
  ```powershell
  Update-MgOrganizationSettingItemInsight -OrganizationId $OrgID -BodyParameter @{DisabledForGroup = "85f741b4-e924-41a8-abf8-d61a7b950bb5"; IsEnabledInOrganization = $false}
  ```

### <a name="configure-item-insights-using-rest-api"></a>Настройка аналитики элементов с помощью API REST
Как сказано выше, параметры конфиденциальности для аналитики элементов по умолчанию включены для всей организации. Параметры по умолчанию можно изменить двумя способами.

- Отключите аналитику элементов для всех пользователей в организации, установив для свойства **isEnabledInOrganization** ресурса [itemInsightsSettings](/graph/api/resources/iteminsightssettings?view=graph-rest-beta&preserve-view=true) значение `false`. 
- Отключите аналитику элементов для _подмножества_ , назначив этих пользователей в группу Azure AD и установив для свойства **disabledForGroup** идентификатор этой группы. Подробнее о [создании групп и добавлении пользователей в качестве участников](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal). 

Используйте операцию [update](/graph/api/iteminsightssettings-update?view=graph-rest-beta&preserve-view=true) для соответствующей настройки свойств **isEnabledInOrganization** и **disabledForGroup** .

| Как включить элемент insights | isEnabledInOrganization | disabledForGroup |
|:-------------|:------------|:------------|
| Вся организация (по умолчанию) | `true` | пусто |
| Недоступно для подмножества пользователей в организации | `true` | Идентификатор группы Azure AD, содержащей подмножество пользователей |
| Недоступно для всей организации | `false` | пропущено |

При обновлении параметров элемента Insights учитывайте следующее:
- [Параметры аналитики элементов](/graph/api/resources/iteminsightssettings?view=graph-rest-beta&preserve-view=true) доступны только в конечных точках бета-версии.
- Получите идентификатор группы Azure AD на портале Azure и убедитесь в том, что группа существует, так как в ходе обновления не проверяется существование группы. Указание несуществующей группы в **disabledForGroup** _не_ отключает insights для пользователей в организации.
- Обновление параметров в Microsoft 365 может занять до 8 часов.
- Независимо от параметров элемента insights, Delve будет по прежнему использовать [настройки конфиденциальности](/sharepoint/delve-for-office-365-admins#control-access-to-delve-and-related-features?view=graph-rest-beta&preserve-view=true) на уровне клиента Delve и пользователя.


## <a name="behavior-changes-in-ui-and-apis"></a>Изменение поведения в пользовательском интерфейсе и интерфейсах API
Некоторые [тенденции](/graph/api/resources/insights-trending) или[используемые](/graph/api/resources/insights-used) insights, могут быть затронуты так, как описано ниже. Со временем масштаб и типы этих insights будут расширены. 

- В карточке профиля пользователя, который отключил элемент insights, не отображаются **использованные** документы. То же ограничение распространяется на результат профиля поиска Майкрософт в Bing, где панель **Последние Файлы** становится пустой. Кроме того, уменьшается точность расшифровки аббревиатур при поиске.

- В Delve у пользователя, который отключил элемент insights, есть скрытые документы. 

- Любой пользователь, который отключили элемент insights, удаляет свою активность из аналитики всей организации. Как правило, эта аналитика предлагает специальные insights, которые могут быть полезны коллегам пользователя, начиная с Outlook, заканчивая OneDrive и SharePoint. Аналитика всегда анонимна, независимо от настроек, но когда пользователь отключает insights, его активность исключается из процесса улучшения эффективность других пользователей.

- Для пользователя, который отключил элемент insights, запрос [тенденций](/graph/api/resources/insights-trending) и[используемых](/graph/api/resources/insights-used) ресурсов в Microsoft Graph API возвращается`HTTP 403 Forbidden`.

- Если для пользователя, выполняющего поиск в Outlook на мобильном устройстве, включен раздел **Обнаружение** , то при отключении аналитики элементов для этого пользователя документы, находящиеся в разделе **Обнаружение** и популярные у этого пользователя, будут скрыты. В противном случае популярные документы будут рекомендоваться и отображаться на основании других действий пользователя.


## <a name="transition-period"></a>Переходный период
Чтобы настроить параметры элемента Insights, до конца 2020, Microsoft 365 будет использовать и параметры Delve, и параметры элемента insights, и применять более эффективное из них при наличии различий. Это означает, что пользователь считается отказавшимся от использования элемента insights, если он отказался или с помощью элементов управления Delve, или с помощью параметров элемента insights.

По истечении этого переходного периода, настройки Delve применяются только к Delve, а параметры элемента insights влияют только на элемент insights в Microsoft Graph. Убедитесь в том, что вы настроили элемент insights в соответствии с требованиями вашей организации.


> [!NOTE]
> В течение переходного периода, по техническими причинам, стартовая страница SharePoint может предоставлять неактуальные предложения, если в организации отключен элемент insights для всех пользователей. Эта проблема будет устранена в ходе предстоящих изменений на стороне сервера. 

## <a name="see-also"></a>См. также
Подробнее о Delve и об использовании параметров Delve для управления отображением документов в канале **Обнаружение** : 
- [Общение и совместная работа в Office Delve](https://support.microsoft.com/office/connect-and-collaborate-in-office-delve-46f92806-b52c-4187-b60e-b3bf8d25f73e)
- [Защищены ли мои документы в Office Delve?](https://support.microsoft.com/office/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3)
- [Delve для администраторов](/sharepoint/delve-for-office-365-admins)
