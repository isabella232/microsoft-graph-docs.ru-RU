---
title: Update androidCompliancePolicy
description: Обновление свойств объекта androidCompliancePolicy.
ms.openlocfilehash: b5349395c3818df98f9451ee7aba18c58a369fdc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27026906"
---
# <a name="update-androidcompliancepolicy"></a><span data-ttu-id="effa2-103">Update androidCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="effa2-103">Update androidCompliancePolicy</span></span>

> <span data-ttu-id="effa2-104">**Примечание.** Для настройки элементов управления и политик Intune с помощью API Microsoft Graph по-прежнему требуется, чтобы клиент [лицензировал](https://go.microsoft.com/fwlink/?linkid=839381) Intune надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="effa2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="effa2-105">Обновление свойств объекта [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="effa2-105">Update the properties of a [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="effa2-106">Необходимые разрешения</span><span class="sxs-lookup"><span data-stu-id="effa2-106">Prerequisites</span></span>
<span data-ttu-id="effa2-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="effa2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="effa2-109">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="effa2-109">Permission type</span></span>|<span data-ttu-id="effa2-110">Разрешения (в порядке убывания привилегий)</span><span class="sxs-lookup"><span data-stu-id="effa2-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="effa2-111">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="effa2-111">Delegated (work or school account)</span></span>|<span data-ttu-id="effa2-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="effa2-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="effa2-113">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="effa2-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="effa2-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="effa2-114">Not supported.</span></span>|
|<span data-ttu-id="effa2-115">Для приложений</span><span class="sxs-lookup"><span data-stu-id="effa2-115">Application</span></span>|<span data-ttu-id="effa2-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="effa2-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="effa2-117">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="effa2-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="effa2-118">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="effa2-118">Request headers</span></span>
|<span data-ttu-id="effa2-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="effa2-119">Header</span></span>|<span data-ttu-id="effa2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="effa2-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="effa2-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="effa2-121">Authorization</span></span>|<span data-ttu-id="effa2-122">Требуется Bearer &lt;маркер&gt;
</span><span class="sxs-lookup"><span data-stu-id="effa2-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="effa2-123">Accept</span><span class="sxs-lookup"><span data-stu-id="effa2-123">Accept</span></span>|<span data-ttu-id="effa2-124">application/json</span><span class="sxs-lookup"><span data-stu-id="effa2-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="effa2-125">Текст запроса</span><span class="sxs-lookup"><span data-stu-id="effa2-125">Request body</span></span>
<span data-ttu-id="effa2-126">В тексте запроса добавьте представление объекта [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="effa2-126">In the request body, supply a JSON representation for the [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object.</span></span>

<span data-ttu-id="effa2-127">В приведенной ниже таблице показаны свойства, которые необходимо указывать при создании объекта [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="effa2-127">The following table shows the properties that are required when you create the [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).</span></span>

|<span data-ttu-id="effa2-128">Свойство</span><span class="sxs-lookup"><span data-stu-id="effa2-128">Property</span></span>|<span data-ttu-id="effa2-129">Тип</span><span class="sxs-lookup"><span data-stu-id="effa2-129">Type</span></span>|<span data-ttu-id="effa2-130">Описание</span><span class="sxs-lookup"><span data-stu-id="effa2-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="effa2-131">id</span><span class="sxs-lookup"><span data-stu-id="effa2-131">id</span></span>|<span data-ttu-id="effa2-132">String</span><span class="sxs-lookup"><span data-stu-id="effa2-132">String</span></span>|<span data-ttu-id="effa2-133">Ключ объекта.</span><span class="sxs-lookup"><span data-stu-id="effa2-133">Key of the entity.</span></span> <span data-ttu-id="effa2-134">Наследуется от объекта [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="effa2-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="effa2-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="effa2-135">createdDateTime</span></span>|<span data-ttu-id="effa2-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="effa2-136">DateTimeOffset</span></span>|<span data-ttu-id="effa2-137">Дата и время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="effa2-137">DateTime the object was created.</span></span> <span data-ttu-id="effa2-138">Наследуется от объекта [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="effa2-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="effa2-139">описание</span><span class="sxs-lookup"><span data-stu-id="effa2-139">description</span></span>|<span data-ttu-id="effa2-140">String</span><span class="sxs-lookup"><span data-stu-id="effa2-140">String</span></span>|<span data-ttu-id="effa2-141">Указанное администратором описание конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="effa2-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="effa2-142">Наследуется от объекта [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="effa2-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="effa2-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="effa2-143">lastModifiedDateTime</span></span>|<span data-ttu-id="effa2-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="effa2-144">DateTimeOffset</span></span>|<span data-ttu-id="effa2-145">Дата и время последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="effa2-145">DateTime the object was last modified.</span></span> <span data-ttu-id="effa2-146">Наследуется от объекта [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="effa2-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="effa2-147">displayName</span><span class="sxs-lookup"><span data-stu-id="effa2-147">displayName</span></span>|<span data-ttu-id="effa2-148">String</span><span class="sxs-lookup"><span data-stu-id="effa2-148">String</span></span>|<span data-ttu-id="effa2-149">Указанное администратором имя конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="effa2-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="effa2-150">Наследуется от объекта [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="effa2-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="effa2-151">version</span><span class="sxs-lookup"><span data-stu-id="effa2-151">version</span></span>|<span data-ttu-id="effa2-152">Int32</span><span class="sxs-lookup"><span data-stu-id="effa2-152">Int32</span></span>|<span data-ttu-id="effa2-153">Версия конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="effa2-153">Version of the device configuration.</span></span> <span data-ttu-id="effa2-154">Наследуется от объекта [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="effa2-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="effa2-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="effa2-155">passwordRequired</span></span>|<span data-ttu-id="effa2-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-156">Boolean</span></span>|<span data-ttu-id="effa2-157">Указывает, что для разблокировки устройства требуется указывать пароль.</span><span class="sxs-lookup"><span data-stu-id="effa2-157">Require a password to unlock device.</span></span>|
|<span data-ttu-id="effa2-158">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="effa2-158">passwordMinimumLength</span></span>|<span data-ttu-id="effa2-159">Int32</span><span class="sxs-lookup"><span data-stu-id="effa2-159">Int32</span></span>|<span data-ttu-id="effa2-160">Минимальная длина пароля.</span><span class="sxs-lookup"><span data-stu-id="effa2-160">Minimum password length.</span></span> <span data-ttu-id="effa2-161">Допустимые значения: от 4 до 16.</span><span class="sxs-lookup"><span data-stu-id="effa2-161">Valid values 4 to 16</span></span>|
|<span data-ttu-id="effa2-162">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="effa2-162">passwordRequiredType</span></span>|[<span data-ttu-id="effa2-163">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="effa2-163">androidRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|<span data-ttu-id="effa2-164">Тип символов в поле пароль.</span><span class="sxs-lookup"><span data-stu-id="effa2-164">Type of characters in password.</span></span> <span data-ttu-id="effa2-165">Возможные значения: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span><span class="sxs-lookup"><span data-stu-id="effa2-165">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="effa2-166">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="effa2-166">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="effa2-167">Int32</span><span class="sxs-lookup"><span data-stu-id="effa2-167">Int32</span></span>|<span data-ttu-id="effa2-168">Период бездействия (в минутах), по истечении которого будет запрашиваться ввод пароля.</span><span class="sxs-lookup"><span data-stu-id="effa2-168">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="effa2-169">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="effa2-169">passwordExpirationDays</span></span>|<span data-ttu-id="effa2-170">Int32</span><span class="sxs-lookup"><span data-stu-id="effa2-170">Int32</span></span>|<span data-ttu-id="effa2-171">Количество дней до окончания срока действия пароля.</span><span class="sxs-lookup"><span data-stu-id="effa2-171">Number of days before the password expires.</span></span> <span data-ttu-id="effa2-172">Допустимые значения: от 1 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="effa2-172">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="effa2-173">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="effa2-173">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="effa2-174">Int32</span><span class="sxs-lookup"><span data-stu-id="effa2-174">Int32</span></span>|<span data-ttu-id="effa2-175">Количество предыдущих паролей, которые требуется блокировать.</span><span class="sxs-lookup"><span data-stu-id="effa2-175">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="effa2-176">securityPreventInstallAppsFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="effa2-176">securityPreventInstallAppsFromUnknownSources</span></span>|<span data-ttu-id="effa2-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-177">Boolean</span></span>|<span data-ttu-id="effa2-178">Указывает, что для устройств требуется запретить установку приложений из неизвестных источников.</span><span class="sxs-lookup"><span data-stu-id="effa2-178">Require that devices disallow installation of apps from unknown sources.</span></span>|
|<span data-ttu-id="effa2-179">securityDisableUsbDebugging</span><span class="sxs-lookup"><span data-stu-id="effa2-179">securityDisableUsbDebugging</span></span>|<span data-ttu-id="effa2-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-180">Boolean</span></span>|<span data-ttu-id="effa2-181">Запрещает USB-отладку на устройствах с Android.</span><span class="sxs-lookup"><span data-stu-id="effa2-181">Disable USB debugging on Android devices.</span></span>|
|<span data-ttu-id="effa2-182">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="effa2-182">securityRequireVerifyApps</span></span>|<span data-ttu-id="effa2-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-183">Boolean</span></span>|<span data-ttu-id="effa2-184">Указывает, что требуется включить функцию проверки приложений для Android.</span><span class="sxs-lookup"><span data-stu-id="effa2-184">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="effa2-185">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="effa2-185">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="effa2-186">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-186">Boolean</span></span>|<span data-ttu-id="effa2-187">Указывает, что защита от угроз для устройств должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="effa2-187">Require that devices have enabled device threat protection.</span></span>|
|<span data-ttu-id="effa2-188">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="effa2-188">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="effa2-189">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="effa2-189">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="effa2-190">Указывает, что на уровне минимального риска, определенного в Mobile Threat Protection, нужно сообщать о несоответствии требованиям.</span><span class="sxs-lookup"><span data-stu-id="effa2-190">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="effa2-191">Возможные значения: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span><span class="sxs-lookup"><span data-stu-id="effa2-191">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="effa2-192">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="effa2-192">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="effa2-193">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-193">Boolean</span></span>|<span data-ttu-id="effa2-194">Устройства запрещено взламывать и рутовать.</span><span class="sxs-lookup"><span data-stu-id="effa2-194">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="effa2-195">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="effa2-195">osMinimumVersion</span></span>|<span data-ttu-id="effa2-196">String</span><span class="sxs-lookup"><span data-stu-id="effa2-196">String</span></span>|<span data-ttu-id="effa2-197">Минимальная версия Android.</span><span class="sxs-lookup"><span data-stu-id="effa2-197">Minimum Android version.</span></span>|
|<span data-ttu-id="effa2-198">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="effa2-198">osMaximumVersion</span></span>|<span data-ttu-id="effa2-199">String</span><span class="sxs-lookup"><span data-stu-id="effa2-199">String</span></span>|<span data-ttu-id="effa2-200">Максимальная версия Android.</span><span class="sxs-lookup"><span data-stu-id="effa2-200">Maximum Android version.</span></span>|
|<span data-ttu-id="effa2-201">minAndroidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="effa2-201">minAndroidSecurityPatchLevel</span></span>|<span data-ttu-id="effa2-202">String</span><span class="sxs-lookup"><span data-stu-id="effa2-202">String</span></span>|<span data-ttu-id="effa2-203">Минимальный уровень обновления для системы безопасности Android.</span><span class="sxs-lookup"><span data-stu-id="effa2-203">Minimum Android security patch level.</span></span>|
|<span data-ttu-id="effa2-204">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="effa2-204">storageRequireEncryption</span></span>|<span data-ttu-id="effa2-205">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-205">Boolean</span></span>|<span data-ttu-id="effa2-206">Указывает, что шифрование на устройствах с Android должно быть обязательным.</span><span class="sxs-lookup"><span data-stu-id="effa2-206">Require encryption on Android devices.</span></span>|
|<span data-ttu-id="effa2-207">securityRequireSafetyNetAttestationBasicIntegrity</span><span class="sxs-lookup"><span data-stu-id="effa2-207">securityRequireSafetyNetAttestationBasicIntegrity</span></span>|<span data-ttu-id="effa2-208">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-208">Boolean</span></span>|<span data-ttu-id="effa2-209">Указывает, что устройству требуется пройти базовую проверку целостности SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="effa2-209">Require the device to pass the SafetyNet basic integrity check.</span></span>|
|<span data-ttu-id="effa2-210">securityRequireSafetyNetAttestationCertifiedDevice</span><span class="sxs-lookup"><span data-stu-id="effa2-210">securityRequireSafetyNetAttestationCertifiedDevice</span></span>|<span data-ttu-id="effa2-211">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-211">Boolean</span></span>|<span data-ttu-id="effa2-212">Указывает, что устройству требуется пройти проверку сертификата SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="effa2-212">Require the device to pass the SafetyNet certified device check.</span></span>|
|<span data-ttu-id="effa2-213">securityRequireGooglePlayServices</span><span class="sxs-lookup"><span data-stu-id="effa2-213">securityRequireGooglePlayServices</span></span>|<span data-ttu-id="effa2-214">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-214">Boolean</span></span>|<span data-ttu-id="effa2-215">Указывает, что на устройстве требуется установить и включить Сервисы Google Play.</span><span class="sxs-lookup"><span data-stu-id="effa2-215">Require Google Play Services to be installed and enabled on the device.</span></span>|
|<span data-ttu-id="effa2-216">securityRequireUpToDateSecurityProviders</span><span class="sxs-lookup"><span data-stu-id="effa2-216">securityRequireUpToDateSecurityProviders</span></span>|<span data-ttu-id="effa2-217">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-217">Boolean</span></span>|<span data-ttu-id="effa2-218">Указывает, что на устройстве требуется использовать обновленных поставщиков безопасности.</span><span class="sxs-lookup"><span data-stu-id="effa2-218">Require the device to have up to date security providers.</span></span> <span data-ttu-id="effa2-219">Указывает, что устройству требуется включить и обновлять Сервисы Google Play.</span><span class="sxs-lookup"><span data-stu-id="effa2-219">The device will require Google Play Services to be enabled and up to date.</span></span>|
|<span data-ttu-id="effa2-220">securityRequireCompanyPortalAppIntegrity</span><span class="sxs-lookup"><span data-stu-id="effa2-220">securityRequireCompanyPortalAppIntegrity</span></span>|<span data-ttu-id="effa2-221">Boolean</span><span class="sxs-lookup"><span data-stu-id="effa2-221">Boolean</span></span>|<span data-ttu-id="effa2-222">Указывает, обязательна ли проверка целостности среды выполнения в клиентском приложении "Корпоративный портал".</span><span class="sxs-lookup"><span data-stu-id="effa2-222">Require the device to pass the Company Portal client app runtime integrity check.</span></span>|



## <a name="response"></a><span data-ttu-id="effa2-223">Ответ</span><span class="sxs-lookup"><span data-stu-id="effa2-223">Response</span></span>
<span data-ttu-id="effa2-224">В случае успешного выполнения этот метод возвращает код ответа `200 OK` и обновленный объект [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) в тексте ответа.</span><span class="sxs-lookup"><span data-stu-id="effa2-224">If successful, this method returns a `200 OK` response code and an updated [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="effa2-225">Пример</span><span class="sxs-lookup"><span data-stu-id="effa2-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="effa2-226">Запрос</span><span class="sxs-lookup"><span data-stu-id="effa2-226">Request</span></span>
<span data-ttu-id="effa2-227">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="effa2-227">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 1159

{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordMinimumLength": 5,
  "passwordRequiredType": "alphabetic",
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordPreviousPasswordBlockCount": 2,
  "securityPreventInstallAppsFromUnknownSources": true,
  "securityDisableUsbDebugging": true,
  "securityRequireVerifyApps": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "securityBlockJailbrokenDevices": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "minAndroidSecurityPatchLevel": "Min Android Security Patch Level value",
  "storageRequireEncryption": true,
  "securityRequireSafetyNetAttestationBasicIntegrity": true,
  "securityRequireSafetyNetAttestationCertifiedDevice": true,
  "securityRequireGooglePlayServices": true,
  "securityRequireUpToDateSecurityProviders": true,
  "securityRequireCompanyPortalAppIntegrity": true
}
```

### <a name="response"></a><span data-ttu-id="effa2-228">Ответ</span><span class="sxs-lookup"><span data-stu-id="effa2-228">Response</span></span>
<span data-ttu-id="effa2-p113">Ниже приведен пример ответа. Примечание. Объект ответа, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.
</span><span class="sxs-lookup"><span data-stu-id="effa2-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1331

{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
  "id": "752c820f-820f-752c-0f82-2c750f822c75",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordMinimumLength": 5,
  "passwordRequiredType": "alphabetic",
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordPreviousPasswordBlockCount": 2,
  "securityPreventInstallAppsFromUnknownSources": true,
  "securityDisableUsbDebugging": true,
  "securityRequireVerifyApps": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "securityBlockJailbrokenDevices": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "minAndroidSecurityPatchLevel": "Min Android Security Patch Level value",
  "storageRequireEncryption": true,
  "securityRequireSafetyNetAttestationBasicIntegrity": true,
  "securityRequireSafetyNetAttestationCertifiedDevice": true,
  "securityRequireGooglePlayServices": true,
  "securityRequireUpToDateSecurityProviders": true,
  "securityRequireCompanyPortalAppIntegrity": true
}
```



