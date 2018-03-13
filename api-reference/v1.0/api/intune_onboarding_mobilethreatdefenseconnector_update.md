# <a name="update-mobilethreatdefenseconnector"></a><span data-ttu-id="7a2e9-101">Обновление mobileThreatDefenseConnector</span><span class="sxs-lookup"><span data-stu-id="7a2e9-101">Update mobileThreatDefenseConnector</span></span>

> <span data-ttu-id="7a2e9-102">**Примечание.** Для настройки элементов управления и политик Intune с помощью API Microsoft Graph по-прежнему требуется, чтобы клиент [лицензировал](https://go.microsoft.com/fwlink/?linkid=839381) Intune надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="7a2e9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a2e9-103">Обновление свойств объекта [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="7a2e9-103">Update the properties of a [calendar](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7a2e9-104">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="7a2e9-104">Prerequisites</span></span>
<span data-ttu-id="7a2e9-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7a2e9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7a2e9-107">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="7a2e9-107">Permission type</span></span>|<span data-ttu-id="7a2e9-108">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="7a2e9-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7a2e9-109">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7a2e9-109">Delegated (work or school account)</span></span>|<span data-ttu-id="7a2e9-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7a2e9-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="7a2e9-111">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="7a2e9-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7a2e9-112">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7a2e9-112">Not supported.</span></span>|
|<span data-ttu-id="7a2e9-113">Для приложений</span><span class="sxs-lookup"><span data-stu-id="7a2e9-113">Application</span></span>|<span data-ttu-id="7a2e9-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7a2e9-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7a2e9-115">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="7a2e9-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="7a2e9-116">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="7a2e9-116">Request headers</span></span>
|<span data-ttu-id="7a2e9-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7a2e9-117">Header</span></span>|<span data-ttu-id="7a2e9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7a2e9-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7a2e9-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="7a2e9-119">Authorization</span></span>|<span data-ttu-id="7a2e9-120">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7a2e9-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="7a2e9-121">Accept</span><span class="sxs-lookup"><span data-stu-id="7a2e9-121">Accept</span></span>|<span data-ttu-id="7a2e9-122">application/json</span><span class="sxs-lookup"><span data-stu-id="7a2e9-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7a2e9-123">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="7a2e9-123">Request body</span></span>
<span data-ttu-id="7a2e9-124">В теле запроса добавьте представление объекта [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="7a2e9-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object.</span></span>

<span data-ttu-id="7a2e9-125">В приведенной ниже таблице показаны свойства, которые необходимо указывать при создании объекта [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="7a2e9-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="7a2e9-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="7a2e9-126">Property</span></span>|<span data-ttu-id="7a2e9-127">Тип</span><span class="sxs-lookup"><span data-stu-id="7a2e9-127">Type</span></span>|<span data-ttu-id="7a2e9-128">Описание</span><span class="sxs-lookup"><span data-stu-id="7a2e9-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a2e9-129">id</span><span class="sxs-lookup"><span data-stu-id="7a2e9-129">id</span></span>|<span data-ttu-id="7a2e9-130">String</span><span class="sxs-lookup"><span data-stu-id="7a2e9-130">String</span></span>|<span data-ttu-id="7a2e9-131">Пока не задокументировано</span><span class="sxs-lookup"><span data-stu-id="7a2e9-131">Not yet documented</span></span>|
|<span data-ttu-id="7a2e9-132">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="7a2e9-132">lastHeartbeatDateTime</span></span>|<span data-ttu-id="7a2e9-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7a2e9-133">DateTimeOffset</span></span>|<span data-ttu-id="7a2e9-134">Метка времени последнего полученного пакета пульса после того, как администратор включил параметр "Подключиться к MTP"</span><span class="sxs-lookup"><span data-stu-id="7a2e9-134">Timestamp of last heartbeat after admin enabled option Connect to MTP</span></span>|
|<span data-ttu-id="7a2e9-135">partnerState</span><span class="sxs-lookup"><span data-stu-id="7a2e9-135">partnerState</span></span>|<span data-ttu-id="7a2e9-136">String</span><span class="sxs-lookup"><span data-stu-id="7a2e9-136">String</span></span>|<span data-ttu-id="7a2e9-137">Состояние партнера этого клиента. Возможные значения: `unavailable`, `available`, `enabled`, `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="7a2e9-137">Partner state of this tenant Possible values are: `unavailable`, `available`, `enabled`, `unresponsive`.</span></span>|
|<span data-ttu-id="7a2e9-138">androidEnabled</span><span class="sxs-lookup"><span data-stu-id="7a2e9-138">androidEnabled</span></span>|<span data-ttu-id="7a2e9-139">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a2e9-139">Boolean</span></span>|<span data-ttu-id="7a2e9-140">Включение или отключение Android</span><span class="sxs-lookup"><span data-stu-id="7a2e9-140">Android Toggle On or Off</span></span>|
|<span data-ttu-id="7a2e9-141">androidDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="7a2e9-141">androidDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="7a2e9-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a2e9-142">Boolean</span></span>|<span data-ttu-id="7a2e9-143">Для Android. Позволяет администратору настроить получение обязательных данных от партнера по синхронизации перед подтверждением соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="7a2e9-143">For Android, Allows admin to config must receive data from the data sync partner prior to being considered compliant</span></span>|
|<span data-ttu-id="7a2e9-144">iosDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="7a2e9-144">iosDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="7a2e9-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a2e9-145">Boolean</span></span>|<span data-ttu-id="7a2e9-146">Для IOS. Позволяет администратору настроить получение обязательных данных от партнера по синхронизации перед подтверждением соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="7a2e9-146">For IOS, Allows admin to config must receive data from the data sync partner prior to being considered compliant</span></span>|
|<span data-ttu-id="7a2e9-147">partnerUnsupportedOsVersionBlocked</span><span class="sxs-lookup"><span data-stu-id="7a2e9-147">partnerUnsupportedOsVersionBlocked</span></span>|<span data-ttu-id="7a2e9-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a2e9-148">Boolean</span></span>|<span data-ttu-id="7a2e9-149">Позволяет администратору блокировать на включенных платформах устройства, несоответствующие минимальным требованиям для версии</span><span class="sxs-lookup"><span data-stu-id="7a2e9-149">Allows admin to block devices on the enabled platforms that do not meet minimum version requirements</span></span>|
|<span data-ttu-id="7a2e9-150">iosEnabled</span><span class="sxs-lookup"><span data-stu-id="7a2e9-150">iosEnabled</span></span>|<span data-ttu-id="7a2e9-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a2e9-151">Boolean</span></span>|<span data-ttu-id="7a2e9-152">Включение и отключение IOS</span><span class="sxs-lookup"><span data-stu-id="7a2e9-152">IOS Toggle On or Off</span></span>|
|<span data-ttu-id="7a2e9-153">partnerUnresponsivenessThresholdInDays</span><span class="sxs-lookup"><span data-stu-id="7a2e9-153">partnerUnresponsivenessThresholdInDays</span></span>|<span data-ttu-id="7a2e9-154">Int32</span><span class="sxs-lookup"><span data-stu-id="7a2e9-154">Int32</span></span>|<span data-ttu-id="7a2e9-155">Получает или задает количество дней устойчивости к отсутствию отклика для клиента в случае интеграции партнера</span><span class="sxs-lookup"><span data-stu-id="7a2e9-155">Get or Set days the per tenant tolerance to unresponsiveness for this partner integration</span></span>|



## <a name="response"></a><span data-ttu-id="7a2e9-156">Отклик</span><span class="sxs-lookup"><span data-stu-id="7a2e9-156">Response</span></span>
<span data-ttu-id="7a2e9-157">В случае успешного выполнения этот метод возвращает код отклика `200 OK` и обновленный объект [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) в теле отклика.</span><span class="sxs-lookup"><span data-stu-id="7a2e9-157">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7a2e9-158">Пример</span><span class="sxs-lookup"><span data-stu-id="7a2e9-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="7a2e9-159">Запрос</span><span class="sxs-lookup"><span data-stu-id="7a2e9-159">Request</span></span>
<span data-ttu-id="7a2e9-160">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="7a2e9-160">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
Content-type: application/json
Content-length: 347

{
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "iosEnabled": true,
  "partnerUnresponsivenessThresholdInDays": 6
}
```

### <a name="response"></a><span data-ttu-id="7a2e9-161">Ответ</span><span class="sxs-lookup"><span data-stu-id="7a2e9-161">Response</span></span>
<span data-ttu-id="7a2e9-p102">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="7a2e9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 463

{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "id": "e4bede14-de14-e4be-14de-bee414debee4",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "iosEnabled": true,
  "partnerUnresponsivenessThresholdInDays": 6
}
```



