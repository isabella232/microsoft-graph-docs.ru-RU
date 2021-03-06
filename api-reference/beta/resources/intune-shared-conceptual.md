---
title: Общие ресурсы в Microsoft Intune — API Microsoft Graph
description: Перечисляет API Microsoft Graph для конечных точек Intune (REST), поддерживающих несколько рабочих процессов для организации клиента.
localization_priority: Normal
author: dougeby
ms.prod: intune
ms.openlocfilehash: 80528f0ad7ab587e6945543e03225d112d958604
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49271935"
---
# <a name="shared-resources-in-microsoft-intune"></a>Общие ресурсы в Microsoft Intune

Пространство имен: microsoft.graph

> **Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены. Использование этих API в производственных приложениях не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Эти конечные точки используются в нескольких интерфейсах API Microsoft Graph для рабочих процессов Intune.  Цель, цель и разрешения, необходимые для использования указанного ресурса, меняются в зависимости от конкретного рабочего процесса и контекста базового вызова.  Кроме того, некоторые методы, свойства и действия поддерживаются только для определенных рабочих процессов.

Рабочие процессы Intune совместно работают со следующими ресурсами Graph:

- [Состояние действия](intune-shared-actionstate.md)
- [Объект назначения всех устройств](intune-shared-alldevicesassignmenttarget.md)
- [Объект назначения всех лицензированных пользователей](intune-shared-alllicensedusersassignmenttarget.md)
- [Защита управляемых приложений для Android](intune-shared-androidmanagedappprotection.md)
- [Параметры назначения приложений с управляемым хранилищем Android](intune-shared-androidmanagedstoreappassignmentsettings.md)
- [Целевое хранилище сертификатов](intune-shared-certificatedestinationstore.md)
- [Хранилище сертификатов](intune-shared-certificatestore.md)
- [Шкала срока действия сертификата](intune-shared-certificatevalidityperiodscale.md)
- [Действие портала компании](intune-shared-companyportalaction.md)
- [Действие блокирования портала компании](intune-shared-companyportalblockedaction.md)
- [Состояние соответствия](intune-shared-compliancestatus.md)
- [Тип фильтра назначения управления устройствами и приложениями](intune-shared-deviceandappmanagementassignmentfiltertype.md)
- [Источник назначения для управления устройствами и приложениями](intune-shared-deviceandappmanagementassignmentsource.md)
- [Объект назначения для управления устройствами и приложениями](intune-shared-deviceandappmanagementassignmenttarget.md)
- [Управление приложениями для устройств](intune-shared-deviceappmanagement.md)
- [Категория устройств](intune-shared-devicecategory.md)
- [Политика соответствия устройств требованиям](intune-shared-devicecompliancepolicy.md)
- [Конфигурация устройств](intune-shared-deviceconfiguration.md)
- [Настройка регистрации устройств](intune-shared-deviceenrollmentconfiguration.md)
- [Тип регистрации устройства](intune-shared-deviceenrollmenttype.md)
- [Управление устройствами](intune-shared-devicemanagement.md)
- [Параметры производных учетных данных управления устройствами](intune-shared-devicemanagementderivedcredentialsettings.md)
- [Отчеты службы управления устройствами](intune-shared-devicemanagementreports.md)
- [Сценарий управления устройствами](intune-shared-devicemanagementscript.md)
- [Тип платформы устройства](intune-shared-deviceplatformtype.md)
- [Тип устройства](intune-shared-devicetype.md)
- [Включение](intune-shared-enablement.md)
- [Параметры доступности регистрации](intune-shared-enrollmentavailabilityoptions.md)
- [Состояние регистрации](intune-shared-enrollmentstate.md)
- [Объект назначения группы исключения](intune-shared-exclusiongroupassignmenttarget.md)
- [Расширенное использование ключа](intune-shared-extendedkeyusage.md)
- [Объект назначения группы](intune-shared-groupassignmenttarget.md)
- [Хэш-алгоритмы](intune-shared-hashalgorithms.md)
- [Намерение установки](intune-shared-installintent.md)
- [Настройки назначения бизнес-приложения iOS](intune-shared-ioslobappassignmentsettings.md)
- [Конфигурация подготовки бизнес-приложений iOS](intune-shared-ioslobappprovisioningconfiguration.md)
- [Защита управляемых приложений для iOS](intune-shared-iosmanagedappprotection.md)
- [Настройки назначения приложения из магазина iOS](intune-shared-iosstoreappassignmentsettings.md)
- [Настройки назначения приложения iOS, приобретенного по программе VPP](intune-shared-iosvppappassignmentsettings.md)
- [Диапазон IP-адресов](intune-shared-iprange.md)
- [Диапазон IPv4-адресов](intune-shared-ipv4range.md)
- [Диапазон IPv6-адресов](intune-shared-ipv6range.md)
- [Размер ключа](intune-shared-keysize.md)
- [Параметр поставщика хранилища ключей](intune-shared-keystorageprovideroption.md)
- [Использование ключей](intune-shared-keyusages.md)
- [Пара "ключ-значение"](intune-shared-keyvaluepair.md)
- [Настройки назначения приложения macOS, приобретенного по программе VPP](intune-shared-macosvppappassignmentsettings.md)
- [Тип владельца управляемого устройства](intune-shared-manageddeviceownertype.md)
- [Тип агента управления](intune-shared-managementagenttype.md)
- [Политика Windows Information Protection для MDM](intune-shared-mdmwindowsinformationprotectionpolicy.md)
- [Настройки назначения приложения из Microsoft Store для бизнеса](intune-shared-microsoftstoreforbusinessappassignmentsettings.md)
- [Содержимое MIME](intune-shared-mimecontent.md)
- [Мобильное приложение](intune-shared-mobileapp.md)
- [Настройки назначения мобильного приложения](intune-shared-mobileappassignmentsettings.md)
- [Параметры времени установки мобильного приложения](intune-shared-mobileappinstalltimesettings.md)
- [Устранение неполадок с мобильным приложением: событие](intune-shared-mobileapptroubleshootingevent.md)
- [Тип владельца](intune-shared-ownertype.md)
- [Тип платформы политики](intune-shared-policyplatformtype.md)
- [Проксируемый домен](intune-shared-proxieddomain.md)
- [Report](intune-shared-report.md)
- [Корневая папка отчета](intune-shared-reportroot.md)
- [Итоговое состояние приложения](intune-shared-resultantappstate.md)
- [Цвет RGB](intune-shared-rgbcolor.md)
- [Тип учетной записи, от имени которой запускается приложение](intune-shared-runasaccounttype.md)
- [Состояние выполнения](intune-shared-runstate.md)
- [Сохраненные параметры создания состояния пользовательского интерфейса](intune-shared-saveduistategenerationoptions.md)
- [Настройка типа источника](intune-shared-settingsourcetype.md)
- [Тип альтернативного имени субъекта](intune-shared-subjectalternativenametype.md)
- [Целевая конфигурация управляемых приложений](intune-shared-targetedmanagedappconfiguration.md)
- [URI](intune-shared-uri.md)
- [Пользователь](intune-shared-user.md)
- [Тип учетной записи токена VPP](intune-shared-vpptokenaccounttype.md)
- [Причина сбоя действия с токеном VPP](intune-shared-vpptokenactionfailurereason.md)
- [Настройки назначения бизнес-приложения Win32](intune-shared-win32lobappassignmentsettings.md)
- [Приоритет оптимизации доставки бизнес-приложений Win32](intune-shared-win32lobappdeliveryoptimizationpriority.md)
- [Уведомление бизнес-приложения Win32](intune-shared-win32lobappnotification.md)
- [Параметры перезапуска приложения Win32 LOB](intune-shared-win32lobapprestartsettings.md)
- [Настройки назначения приложения Windows AppX](intune-shared-windowsappxappassignmentsettings.md)
- [Профиль Windows AutoPilot Deployment](intune-shared-windowsautopilotdeploymentprofile.md)
- [Конфигурация присоединения к домену Windows](intune-shared-windowsdomainjoinconfiguration.md)
- [Настройки назначения универсального приложения Windows AppX](intune-shared-windowsuniversalappxappassignmentsettings.md)
- [Состояние центра обновления Windows](intune-shared-windowsupdatestate.md)