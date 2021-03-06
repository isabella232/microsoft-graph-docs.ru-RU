---
title: Тип ресурса Нетворкинфо
description: Тип Нетворкинфо
localization_priority: Normal
author: williamlooney
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: c3f2d7cb9c3792ea74691367cf2fa7299c0c8c79
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48601484"
---
# <a name="networkinfo-resource-type"></a>Тип ресурса Нетворкинфо

Пространство имен: microsoft.graph.callRecords

Представляет сведения о сети, используемой в вызове.

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|бандвидсловевентратио|Двойное с плавающей точкой|Доля звонка, когда конечная точка мультимедиа обнаружила доступную пропускную способность или политику пропускной способности, достаточно низкой, чтобы снизить качество передачи звука.|
|басиксервицесетидентифиер|String|Идентификатор набора служб беспроводной локальной сети для конечной точки носителя, используемой для подключения к сети.|
|connectionType|Microsoft. Graph. Каллрекордс. Нетворкконнектионтипе|Тип сети, используемой конечной точкой носителя. Возможные значения: `unknown`, `wired`, `wifi`, `mobile`, `tunnel`, `unknownFutureValue`.|
|делайевентратио|Двойное с плавающей точкой|Доля звонка, когда конечная точка мультимедиа обнаружила, что задержка в сети была достаточно большой, чтобы повлиять на возможность двусторонней связи в реальном времени.|
|днссуффикс|String|DNS-суффикс, связанный с сетевым адаптером конечной точки носителя.|
|ipAddress|String|IP-адрес конечной точки носителя.|
|линкспид|Int64|Скорость канала в битах в секунду, сообщаемая сетевым адаптером, используемым конечной точкой носителя.|
|macAddress|String|MAC-адрес сетевого устройства конечной точки носителя.|
|порта|Int32|Номер сетевого порта, используемый конечной точкой носителя.|
|рецеиведкуалитевентратио|Двойное с плавающей точкой|Доля звонка, когда конечная точка мультимедиа обнаружила, что сеть привела к низкому качеству полученного звука.|
|рефлексивеипаддресс|String|IP-адрес конечной точки носителя, отображаемый сервером ретрансляции мультимедиа. Обычно это общедоступный IP-адрес в Интернете, связанный с конечной точкой.|
|релайипаддресс|String|IP-адрес сервера ретрансляции мультимедиа, выделенный конечной точкой носителя.|
|релайпорт|Int32|Номер сетевого порта, выделенный на сервере ретрансляции мультимедиа конечной точкой мультимедиа.|
|сенткуалитевентратио|Двойное с плавающей точкой|Доля звонка, когда конечная точка мультимедиа обнаружила, что сеть привела к низкому качеству отправленного звука.|
|подсети|String|Подсеть, используемая конечной точкой мультимедиа для потока мультимедиа.|
|вифибанд|Microsoft. Graph. Каллрекордс. Вифибанд|Полоса Wi-Fi, используемая конечной точкой носителя. Возможные значения: `unknown`, `frequency24GHz`, `frequency50GHz`, `frequency60GHz`, `unknownFutureValue`.|
|вифибаттеричарже|Int32|Оценка оставшегося заряда батареи в процентах от конечной точки носителя.|
|вифичаннел|Int32|Канал Wi-Fi, используемый конечной точкой носителя.|
|вифимикрософтдривер|String|Имя драйвера Microsoft WiFi, используемого конечной точкой носителя. Значение может быть локализовано на основе языка, используемого конечной точкой.|
|вифимикрософтдриверверсион|String|Версия драйвера Wi-Fi (Майкрософт), используемая конечной точкой носителя.|
|вифирадиотипе|Microsoft. Graph. Каллрекордс. Вифирадиотипе|Тип радиосвязи Wi-Fi, используемый конечной точкой носителя. Возможные значения: `unknown`, `wifi80211a`, `wifi80211b`, `wifi80211g`, `wifi80211n`, `wifi80211ac`, `wifi80211ax`, `unknownFutureValue`.|
|вифисигналстренгс|Int32|Сила сигнала Wi-Fi в процентном отношении, сообщаемая конечной точкой носителя.|
|вифивендордривер|String|Имя драйвера Wi-Fi, используемого конечной точкой носителя. Значение может быть локализовано на основе языка, используемого конечной точкой.|
|вифивендордриверверсион|String|Версия драйвера Wi-Fi, используемая конечной точкой носителя.|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.callRecords.networkInfo",
  "baseType": null
}-->

```json
{
  "bandwidthLowEventRatio": "Double",
  "basicServiceSetIdentifier": "String",
  "connectionType": "String",
  "delayEventRatio": "Double",
  "dnsSuffix": "String",
  "ipAddress": "String",
  "linkSpeed": 1024,
  "macAddress": "String",
  "port": 1024,
  "receivedQualityEventRatio": "Double",
  "reflexiveIPAddress": "String",
  "relayIPAddress": "String",
  "relayPort": 1024,
  "sentQualityEventRatio": "Double",
  "subnet": "String",
  "wifiBand": "String",
  "wifiBatteryCharge": 1024,
  "wifiChannel": 1024,
  "wifiMicrosoftDriver": "String",
  "wifiMicrosoftDriverVersion": "String",
  "wifiRadioType": "String",
  "wifiSignalStrength": 1024,
  "wifiVendorDriver": "String",
  "wifiVendorDriverVersion": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "networkInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
