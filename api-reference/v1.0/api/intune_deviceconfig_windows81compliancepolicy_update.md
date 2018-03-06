# <a name="update-windows81compliancepolicy"></a><span data-ttu-id="5f86f-101">Update windows81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="5f86f-101">Update windows81CompliancePolicy</span></span>

> <span data-ttu-id="5f86f-102">**Примечание.** Для настройки элементов управления и политик Intune с помощью API Microsoft Graph по-прежнему требуется, чтобы клиент [лицензировал](https://go.microsoft.com/fwlink/?linkid=839381) Intune надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="5f86f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5f86f-103">Обновление свойств объекта [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5f86f-103">Update the properties of a [calendar](../resources/intune_deviceconfig_windows81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5f86f-104">Необходимые разрешения</span><span class="sxs-lookup"><span data-stu-id="5f86f-104">Prerequisites</span></span>
<span data-ttu-id="5f86f-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, в том числе о выборе разрешений, см. в статье [Разрешения](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5f86f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5f86f-107">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="5f86f-107">Permission type</span></span>|<span data-ttu-id="5f86f-108">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="5f86f-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5f86f-109">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5f86f-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5f86f-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f86f-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5f86f-111">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="5f86f-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5f86f-112">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5f86f-112">Not supported.</span></span>|
|<span data-ttu-id="5f86f-113">Для приложений</span><span class="sxs-lookup"><span data-stu-id="5f86f-113">Application</span></span>|<span data-ttu-id="5f86f-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5f86f-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5f86f-115">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="5f86f-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="5f86f-116">Заголовки запроса</span><span class="sxs-lookup"><span data-stu-id="5f86f-116">Request headers</span></span>
|<span data-ttu-id="5f86f-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5f86f-117">Header</span></span>|<span data-ttu-id="5f86f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5f86f-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5f86f-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f86f-119">Authorization</span></span>|<span data-ttu-id="5f86f-120">Bearer &lt;token&gt;. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5f86f-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="5f86f-121">Accept</span><span class="sxs-lookup"><span data-stu-id="5f86f-121">Accept</span></span>|<span data-ttu-id="5f86f-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5f86f-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5f86f-123">Тело запроса</span><span class="sxs-lookup"><span data-stu-id="5f86f-123">Request body</span></span>
<span data-ttu-id="5f86f-124">В теле запроса добавьте представление объекта [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="5f86f-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_windows81compliancepolicy.md) object.</span></span>

<span data-ttu-id="5f86f-125">Ниже показаны свойства, которые необходимо указывать при создании объекта [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5f86f-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="5f86f-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="5f86f-126">Property</span></span>|<span data-ttu-id="5f86f-127">Тип</span><span class="sxs-lookup"><span data-stu-id="5f86f-127">Type</span></span>|<span data-ttu-id="5f86f-128">Описание</span><span class="sxs-lookup"><span data-stu-id="5f86f-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5f86f-129">id</span><span class="sxs-lookup"><span data-stu-id="5f86f-129">id</span></span>|<span data-ttu-id="5f86f-130">String</span><span class="sxs-lookup"><span data-stu-id="5f86f-130">String</span></span>|<span data-ttu-id="5f86f-131">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="5f86f-131">Key of the setting.</span></span> <span data-ttu-id="5f86f-132">Наследуется от объекта [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5f86f-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5f86f-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5f86f-133">createdDateTime</span></span>|<span data-ttu-id="5f86f-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f86f-134">DateTimeOffset</span></span>|<span data-ttu-id="5f86f-135">Дата и время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="5f86f-135">DateTime the object was created.</span></span> <span data-ttu-id="5f86f-136">Наследуется от объекта [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5f86f-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5f86f-137">description</span><span class="sxs-lookup"><span data-stu-id="5f86f-137">description</span></span>|<span data-ttu-id="5f86f-138">String</span><span class="sxs-lookup"><span data-stu-id="5f86f-138">String</span></span>|<span data-ttu-id="5f86f-139">Указанное администратором описание конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="5f86f-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="5f86f-140">Наследуется от объекта [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5f86f-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5f86f-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5f86f-141">lastModifiedDateTime</span></span>|<span data-ttu-id="5f86f-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f86f-142">DateTimeOffset</span></span>|<span data-ttu-id="5f86f-143">Дата и время последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="5f86f-143">DateTime the object was last modified.</span></span> <span data-ttu-id="5f86f-144">Наследуется от объекта [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5f86f-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5f86f-145">displayName</span><span class="sxs-lookup"><span data-stu-id="5f86f-145">displayName</span></span>|<span data-ttu-id="5f86f-146">String</span><span class="sxs-lookup"><span data-stu-id="5f86f-146">String</span></span>|<span data-ttu-id="5f86f-147">Указанное администратором имя конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="5f86f-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="5f86f-148">Наследуется от объекта [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5f86f-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5f86f-149">version</span><span class="sxs-lookup"><span data-stu-id="5f86f-149">version</span></span>|<span data-ttu-id="5f86f-150">Int32</span><span class="sxs-lookup"><span data-stu-id="5f86f-150">Int32</span></span>|<span data-ttu-id="5f86f-151">Версия конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="5f86f-151">Version of the device configuration.</span></span> <span data-ttu-id="5f86f-152">Наследуется от объекта [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5f86f-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5f86f-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="5f86f-153">passwordRequired</span></span>|<span data-ttu-id="5f86f-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="5f86f-154">Boolean</span></span>|<span data-ttu-id="5f86f-155">Указывает на то, что для разблокировки устройства с Windows требуется пароль.</span><span class="sxs-lookup"><span data-stu-id="5f86f-155">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="5f86f-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="5f86f-156">passwordBlockSimple</span></span>|<span data-ttu-id="5f86f-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="5f86f-157">Boolean</span></span>|<span data-ttu-id="5f86f-158">Указывает, требуется ли блокировать простой пароль.</span><span class="sxs-lookup"><span data-stu-id="5f86f-158">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="5f86f-159">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="5f86f-159">passwordExpirationDays</span></span>|<span data-ttu-id="5f86f-160">Int32</span><span class="sxs-lookup"><span data-stu-id="5f86f-160">Int32</span></span>|<span data-ttu-id="5f86f-161">Срок действия пароля (в днях).</span><span class="sxs-lookup"><span data-stu-id="5f86f-161">Password expiration in days.</span></span>|
|<span data-ttu-id="5f86f-162">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="5f86f-162">passwordMinimumLength</span></span>|<span data-ttu-id="5f86f-163">Int32</span><span class="sxs-lookup"><span data-stu-id="5f86f-163">Int32</span></span>|<span data-ttu-id="5f86f-164">Минимальная длина пароля.</span><span class="sxs-lookup"><span data-stu-id="5f86f-164">The minimum password length.</span></span>|
|<span data-ttu-id="5f86f-165">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="5f86f-165">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="5f86f-166">Int32</span><span class="sxs-lookup"><span data-stu-id="5f86f-166">Int32</span></span>|<span data-ttu-id="5f86f-167">Период бездействия (в минутах), по истечении которого будет запрашиваться ввод пароля.</span><span class="sxs-lookup"><span data-stu-id="5f86f-167">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="5f86f-168">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="5f86f-168">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="5f86f-169">Int32</span><span class="sxs-lookup"><span data-stu-id="5f86f-169">Int32</span></span>|<span data-ttu-id="5f86f-170">Количество наборов символов, которые требуются для пароля.</span><span class="sxs-lookup"><span data-stu-id="5f86f-170">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="5f86f-171">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="5f86f-171">passwordRequiredType</span></span>|<span data-ttu-id="5f86f-172">String</span><span class="sxs-lookup"><span data-stu-id="5f86f-172">String</span></span>|<span data-ttu-id="5f86f-173">Требуемый тип пароля.</span><span class="sxs-lookup"><span data-stu-id="5f86f-173">The required password type.</span></span> <span data-ttu-id="5f86f-174">Возможные значения: `deviceDefault`, `alphanumeric`, `numeric`.</span><span class="sxs-lookup"><span data-stu-id="5f86f-174">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="5f86f-175">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="5f86f-175">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="5f86f-176">Int32</span><span class="sxs-lookup"><span data-stu-id="5f86f-176">Int32</span></span>|<span data-ttu-id="5f86f-177">Количество предыдущих паролей, повторное использование которых необходимо запретить.</span><span class="sxs-lookup"><span data-stu-id="5f86f-177">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="5f86f-178">Допустимые значения: от 0 до 24.</span><span class="sxs-lookup"><span data-stu-id="5f86f-178">Valid values 0 to 24</span></span>|
|<span data-ttu-id="5f86f-179">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="5f86f-179">osMinimumVersion</span></span>|<span data-ttu-id="5f86f-180">String</span><span class="sxs-lookup"><span data-stu-id="5f86f-180">String</span></span>|<span data-ttu-id="5f86f-181">Минимальная версия Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="5f86f-181">Minimum Windows 8.1 version.</span></span>|
|<span data-ttu-id="5f86f-182">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="5f86f-182">osMaximumVersion</span></span>|<span data-ttu-id="5f86f-183">String</span><span class="sxs-lookup"><span data-stu-id="5f86f-183">String</span></span>|<span data-ttu-id="5f86f-184">Максимальная версия Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="5f86f-184">Maximum Windows 8.1 version.</span></span>|
|<span data-ttu-id="5f86f-185">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="5f86f-185">storageRequireEncryption</span></span>|<span data-ttu-id="5f86f-186">Boolean</span><span class="sxs-lookup"><span data-stu-id="5f86f-186">Boolean</span></span>|<span data-ttu-id="5f86f-187">Указывает, обязательно ли шифрование данных на устройстве с Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="5f86f-187">Indicates whether or not to require encryption on a windows 8.1 device.</span></span>|



## <a name="response"></a><span data-ttu-id="5f86f-188">Ответ</span><span class="sxs-lookup"><span data-stu-id="5f86f-188">Response</span></span>
<span data-ttu-id="5f86f-189">В случае успешного выполнения этот метод возвращает код ответа `200 OK` и обновленный объект [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md) в теле ответа.</span><span class="sxs-lookup"><span data-stu-id="5f86f-189">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_windows81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5f86f-190">Пример</span><span class="sxs-lookup"><span data-stu-id="5f86f-190">Example</span></span>
### <a name="request"></a><span data-ttu-id="5f86f-191">Запрос</span><span class="sxs-lookup"><span data-stu-id="5f86f-191">Request</span></span>
<span data-ttu-id="5f86f-192">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="5f86f-192">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 602

{
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="5f86f-193">Ответ</span><span class="sxs-lookup"><span data-stu-id="5f86f-193">Response</span></span>
<span data-ttu-id="5f86f-p110">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. Все свойства будут возвращены при фактическом вызове.</span><span class="sxs-lookup"><span data-stu-id="5f86f-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 774

{
  "@odata.type": "#microsoft.graph.windows81CompliancePolicy",
  "id": "6bb4b7e0-b7e0-6bb4-e0b7-b46be0b7b46b",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```



