---
title: Обновление объекта deviceAppManagement
description: Обновление свойств объекта deviceAppManagement.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: 27da30374f9f224695945f545b0527dce83f74d6
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "49257508"
---
# <a name="update-deviceappmanagement"></a>Обновление объекта deviceAppManagement

Пространство имен: microsoft.graph

> **Важно!** API в версии/Beta в Microsoft Graph могут быть изменены. Использование этих API в производственных приложениях не поддерживается.

> **Примечание.** API Microsoft Graph для Intune требует наличия [активной лицензии Intune](https://go.microsoft.com/fwlink/?linkid=839381) для клиента.

Обновление свойств объекта [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).
## <a name="prerequisites"></a>Необходимые компоненты
Для вызова этого API требуется одно из следующих разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).  Обратите внимание, что соответствующее разрешение зависит от рабочего процесса.

|Тип разрешения|Разрешения (в порядке убывания привилегий)|
|:---|:---|
| Делегированные (рабочая или учебная учетная запись) | |
| &nbsp;&nbsp; **Приложения**, **книги**, **onboarding** входящая миграция, **Интеграция партнеров** или **набор политик** | DeviceManagementApps.ReadWrite.All |
| &nbsp;&nbsp; **Управление устройствами** | DeviceManagementManagedDevices.ReadWrite.All |
| Делегированные (личная учетная запись Майкрософт) | Не поддерживается. |
| Приложение | |
| &nbsp;&nbsp; **Приложения**, **книги**, **onboarding** входящая миграция, **Интеграция партнеров** или **набор политик** | DeviceManagementApps.ReadWrite.All |
| &nbsp;&nbsp; **Управление устройствами** | DeviceManagementManagedDevices.ReadWrite.All |

## <a name="http-request"></a>HTTP-запрос
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement
```

## <a name="request-headers"></a>Заголовки запроса
|Заголовок|Значение|
|:---|:---|
|Авторизация|Bearer &lt;token&gt;. Обязательный.|
|Accept|application/json|

## <a name="request-body"></a>Текст запроса
В тексте запроса добавьте представление объекта [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) в формате JSON.

В таблице ниже приведены свойства, которые необходимо указывать при создании объекта [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).

|Свойство|Тип|Описание|
|:---|:---|:---|
|id|String|Ключ объекта.|
|**Встроенное подключение**|
|isEnabledForMicrosoftStoreForBusiness|Boolean|Указывает, включена ли для учетной запись синхронизация приложений из Microsoft Store для бизнеса.|
|microsoftStoreForBusinessLanguage|String|Сведения о языковом стандарте, используемом для синхронизации приложений из Microsoft Store для бизнеса. Региональные параметры, относящиеся к стране или региону. Названия этих региональных параметров соответствуют стандарту RFC 4646 (для Windows Vista и более поздних версий). Используется формат <languagecode2>-<страна/код_региона2>, где <languagecode2> — это двухбуквенный код в нижнем регистре, полученный из стандарта ISO 639-1, а <страна/код_регион2> — код из двух прописных букв по стандарту ISO 3166. Например, en-US для английского (США) — это определенный региональный стандарт.|
|microsoftStoreForBusinessLastCompletedApplicationSyncTime|DateTimeOffset|Время последней завершенной синхронизации приложений из Microsoft Store для бизнеса.|
|microsoftStoreForBusinessLastSuccessfulSyncDateTime|DateTimeOffset|Время последней успешной синхронизации приложений из Microsoft Store для бизнеса с учетной записью.|
|микрософтсторефорбусинесспорталселектион|[microsoftStoreForBusinessPortalSelectionOptions](../resources/intune-onboarding-microsoftstoreforbusinessportalselectionoptions.md)|Сведения о портале конечного пользователя используются для синхронизации приложений из Microsoft Store для бизнеса и портала компании Intune. Выбрать можно три варианта: \[ "только корпоративный портал", "Корпоративный портал и частный магазин", "только частный магазин" \] . Возможные значения: `none`, `companyPortal`, `privateStore`.|

Этот метод поддерживает [параметры запросов OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) для настройки ответа.

## <a name="response"></a>Отклик
В случае успешного выполнения этот метод возвращает код отклика `200 OK` и обновленный объект [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) в тексте отклика.

## <a name="example"></a>Пример

### <a name="request"></a>Запрос

Ниже приведен пример запроса.

``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a>Отклик

Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 110

{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
}
```










