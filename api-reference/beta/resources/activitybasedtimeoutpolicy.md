---
title: Тип ресурса Активитибаседтимеаутполици
description: Представляет политику, которая может управлять временем ожидания простоя веб-сеансов для приложений, поддерживающих функциональность времени ожидания на основе действий.
localization_priority: Normal
author: lujiangfeng666
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: 2f50969aa02b5115e061e7e874e7f9b5667f3570
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48024530"
---
# <a name="activitybasedtimeoutpolicy-resource-type"></a>Тип ресурса Активитибаседтимеаутполици

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет политику, которая может управлять временем ожидания простоя веб-сеансов для приложений, поддерживающих функциональность времени ожидания на основе действий. Приложения принудительно применяют функцию автоматического выхода после периода бездействия. Этот тип политики можно применять только на уровне Организации (путем установки для свойства **исорганизатиондефаулт** значения `true` ).

Наследуется от [стсполици](stsPolicy.md).

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип | Описание |
|:-------------|:------------|:------------|
| [Создание Активитибаседтимеаутполици](../api/activitybasedtimeoutpolicy-post-activitybasedtimeoutpolicies.md) | [активитибаседтимеаутполици](activitybasedtimeoutpolicy.md) | Создание объекта Активитибаседтимеаутполици. |
| [Получение Активитибаседтимеаутполици](../api/activitybasedtimeoutpolicy-get.md) | [активитибаседтимеаутполици](activitybasedtimeoutpolicy.md) | Чтение свойств и связей объекта Активитибаседтимеаутполици. |
| [Список АктивитибаседтимеаутполиЦиес](../api/activitybasedtimeoutpolicy-list.md) | [активитибаседтимеаутполици](activitybasedtimeoutpolicy.md) | Чтение свойств и связей объектов Активитибаседтимеаутполици. |
| [Обновление Активитибаседтимеаутполици](../api/activitybasedtimeoutpolicy-update.md) | Нет | Обновление объекта Активитибаседтимеаутполици. |
| [Удаление Активитибаседтимеаутполици](../api/activitybasedtimeoutpolicy-delete.md) | Нет | Удаление объекта Активитибаседтимеаутполици. |

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|id|String| Уникальный идентификатор для этой политики. Только для чтения.|
|RDLC|Коллекция String| Коллекция String, содержащая строку JSON, определяющую правила и параметры для этой политики. Ниже приведены дополнительные сведения о схеме JSON для этого свойства. Обязательный.|
|description|String| Описание для этой политики.|
|displayName|String| Отображаемое имя для этой политики. Обязательный.|
|исорганизатиондефаулт|Boolean|Если задано значение true, активируется эта политика. Для одного и того же типа политики может быть задано несколько политик, но только одна из них может быть активирована в качестве организации по умолчанию. Необязательное значение по умолчанию — false.|


### <a name="properties-of-an-activity-based-timeout-policy-definition"></a>Свойства определения политики времени ожидания на основе действий
Свойства, приведенные ниже, формируют объект JSON, представляющий политику времени ожидания, основанную на действиях. Этот объект JSON необходимо **преобразовать в строку с escape-символами** , которые будут вставлены в свойство **definition** . Ниже показан пример в формате JSON.

<!-- {
  "blockType": "ignored"
}-->
```json
{
  "definition":["{\"ActivityBasedTimeoutPolicy\":{\"Version\":1,\"ApplicationPolicies\":[{\"ApplicationId\":\"default\",\"WebSessionIdleTimeout\":\"01:00:00\"},{\"ApplicationId\":\"c44b4083-3bb0-49c1-b47d-974e53cbdf3c\",\"WebSessionIdleTimeout\":\"00:15:00\"}]}}"]
}
```

>Note: все временные интервалы в этих свойствах указаны в формате "DD. чч: мм: СС".

>Note: Max Values для свойств, обозначенных в "Days", — 1 секунды, обозначенное как количество дней. Например, максимальное значение в 1 день задается как "23:59:59".

| Свойство     | Тип   |Описание|
|:-------------|:------|:---------|
|Версия|Целое число|Версия политики. Установите значение 1. Обязательный.|
|аппликатионполиЦиес|Объект JSON|Коллекция политики приложений. Политика приложений — это сочетание объекта ApplicationId и объекта Вебсессионидлетимеаут: <br> <ul><li>**ApplicationId**: допустимые значения:<ul><li> по умолчанию: применяет политику ко всем приложениям, поддерживающим функциональность времени ожидания на основе действий, но не зависящее от приложения</li><li> c44b4083-3bb0-49c1-b47d-974e53cbdf3c: применение политики к порталу Azure</li></ul></li><li>**Вебсессионидлетимеаут**: период бездействия пользователя, по истечении которого срок действия веб-сеанса пользователя считается истекшим. Минимальное значение — 5 минут; Максимальное значение — 1 день.</li></ul> |


## <a name="relationships"></a>Отношения

Нет

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.activityBasedTimeoutPolicy",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "definition": ["String"],
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "isOrganizationDefault": true
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "activityBasedTimeoutPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

