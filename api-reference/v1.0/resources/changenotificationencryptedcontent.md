---
title: Тип ресурса Чанженотификатионенкриптедконтент
description: Объект Чанженотификатионенкриптедконтент представляет зашифрованные данные, вложенные в уведомление об изменении.
localization_priority: Normal
author: baywet
doc_type: resourcePageType
ms.prod: ''
ms.openlocfilehash: f86dc032e3f9e14790358a03e8026f1932ae9431
ms.sourcegitcommit: b70ee16cdf24daaec923acc477b86dbf76f2422b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "48193636"
---
# <a name="changenotificationencryptedcontent-resource-type"></a>Тип ресурса Чанженотификатионенкриптедконтент

Пространство имен: microsoft.graph

Представляет зашифрованные данные, вложенные в уведомление об изменении.

Дополнительные сведения см. в статье [Настройка уведомлений об изменениях, включающих данные ресурсов (Предварительная версия)](/graph/webhooks-with-resource-data.md).

## <a name="properties"></a>Свойства

| Свойство | Тип | Описание |
|:---------|:-----|:------------|
| data | string | Зашифрованные данные в кодировке Base64, которые создают полный респресентед ресурсов как JSON. Данные зашифрованы с `dataKey` помощью `AES/CBC/PKCS5PADDING` комплекта шифров. |
| Подпись | string | Хэш-код HMAC-SHA256 данных для целей проверки в кодировке Base64. |
| датакэй | string | Симметричный ключ в кодировке Base64, созданный Microsoft Graph для шифрования значения данных и создания подписи данных. Этот ключ шифруется с помощью открытого ключа сертификата, предоставленного во время подписки. Его необходимо расшифровать с помощью закрытого ключа сертификата, прежде чем его можно будет использовать для расшифровки данных или проверки подписи. Этот ключ зашифрован с помощью следующего комплекта шифра: `RSA/ECB/OAEPWithSHA1AndMGF1Padding` . |
| енкриптионцертификатеид | string | Идентификатор сертификата, используемого для шифрования `dataKey` . |
| енкриптионцертификатесумбпринт | string | Шестнадцатеричное представление отпечатка сертификата, используемого для шифрования `dataKey` . |

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.changeNotificationEncryptedContent"
}-->

```json
{
  "data": "{encrypted data that produces a full resource}",
  "dataSignature": "<HMAC-SHA256 hash>",
  "dataKey": "{encrypted symmetric key from Microsoft Graph}",
  "encryptionCertificateId": "MySelfSignedCert/DDC9651A-D7BC-4D74-86BC-A8923584B0AB",
  "encryptionCertificateThumbprint": "07293748CC064953A3052FB978C735FB89E61C3D"
}
```

<!-- uuid: 6bb14c3d-16ef-4ea3-8dc7-c88b9190081c
2020-08-05 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "changeNotificationEncryptedConent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
