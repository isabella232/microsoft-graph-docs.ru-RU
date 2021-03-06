---
title: Тип ресурса teamsApp
description: Приложение в каталоге приложений Microsoft Teams.
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: bf9c152de12acc31ecf13100c6dcba753d1d476b
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48036942"
---
# <a name="teamsapp-resource-type"></a>Тип ресурса teamsApp

Пространство имен: microsoft.graph

Представляет приложение в каталоге приложений [Microsoft Teams](teams-api-overview.md).

Пользователи могут видеть эти приложения в магазине Microsoft Teams, а эти приложения можно устанавливать в [командах](team.md), используя метод [добавления приложения в команду](../api/teamsappinstallation-add.md).

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип  |Описание|
|:---------------|:--------|:----------|
|[Список опубликованных приложений](../api/teamsapp-list.md) | Коллекция [teamsApp](teamsapp.md) | Список опубликованных приложений из каталога приложений Microsoft Teams.|
|[Публикация приложения](../api/teamsapp-publish.md) | [teamsApp](teamsapp.md) | Публикация приложения в каталоге приложений организации.|
|[Обновление опубликованного приложения](../api/teamsapp-update.md) | [teamsApp](teamsapp.md) | Обновление опубликованного приложения в каталоге приложений организации.|
|[Удаление опубликованного приложения](../api/teamsapp-delete.md) | Нет | Удаление опубликованного приложения из каталога приложений организации.|

## <a name="properties"></a>Свойства

| Свойство            | Тип     | Описание |
|:------------------- |:-------- |:----------- |
| id                  | string   | Сгенерированный идентификатор приложения из каталога приложений (отличающийся от предоставленного разработчиком идентификатора в [ZIP-пакете приложения Microsoft Teams](/microsoftteams/platform/concepts/apps/apps-package). |
| externalId          | строка   | Идентификатор каталога, предоставленный разработчиком приложения в [ZIP-пакете приложения Microsoft Teams](/microsoftteams/platform/concepts/apps/apps-package). |
| displayName                | string   | Название приложения каталога, предоставленное разработчиком приложения в [ZIP-пакете приложения Microsoft Teams](/microsoftteams/platform/concepts/apps/apps-package). |
| distributionMethod  | teamsAppDistributionMethod     | Метод распространения приложения. Только для чтения.|

### <a name="teamsappdistributionmethod-values"></a>Значения teamsAppDistributionMethod

|Элемент|Значение|Описание|
|:---|:---|:---|
|store|0| Приложение доступно всем клиентам через магазин приложений Microsoft Teams.|
|organization|1|Приложение доступно только в этом клиенте|
|sideloaded|2|Приложение доступно только тому пользователю или той команде, где оно установлено.|

## <a name="relationships"></a>Отношения

| Связь | Тип   | Описание |
|:---------------|:--------|:----------|
|appDefinitions|Коллекция [teamsAppDefinition](teamsappdefinition.md)| Сведения о каждой версии приложения. |

## <a name="json-representation"></a>Представление в формате JSON

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsApp",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string",
  "externalId": "string",
  "displayName": "string",
  "distributionMethod": "string"
}
```

## <a name="see-also"></a>См. также

- [teamsAppInstallation](teamsappinstallation.md)
- [teamsAppDefinition](teamsappdefinition.md)
- [teamsTab](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


