---
title: Тип ресурса yammerGroupsActivityDetail
description: Ниже указано представление ресурса в формате JSON.
ms.openlocfilehash: 9a4bb00aecb2ae1d14b68a5388e0dedc7c41b1cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27075778"
---
# <a name="yammergroupsactivitydetail-resource-type"></a>Тип ресурса yammerGroupsActivityDetail

## <a name="properties"></a>Свойства

| Свойство           | Тип    |
| :----------------- | :------ |
| reportRefreshDate  | Date    |
| groupDisplayName   | String  |
| isDeleted          | Логический |
| ownerPrincipalName | String  |
| lastActivityDate   | Date    |
| groupType          | String  |
| office365Connected | Логический |
| memberCount        | Int64   |
| postedCount        | Int64   |
| readCount          | Int64   |
| likedCount         | Int64   |
| reportPeriod       | String  |

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerGroupsActivityDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "groupDisplayName": "String", 
  "isDeleted": true, 
  "ownerPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "groupType": "String", 
  "office365Connected": true, 
  "memberCount": 1024, 
  "postedCount": 1024, 
  "readCount": 1024, 
  "likedCount": 1024, 
  "reportPeriod": "String"
}
```
