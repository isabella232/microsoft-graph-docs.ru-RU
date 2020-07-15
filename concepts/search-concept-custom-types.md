---
title: Использование API службы поиска Microsoft в Microsoft Graph для поиска пользовательских типов
description: С помощью API Microsoft Search можно импортировать внешние данные через ресурс [екстерналитем](/graph/api/resources/externalitem?view=graph-rest-beta) и запускать поисковые запросы для этого внешнего контента.
author: nmoreau
localization_priority: Normal
ms.prod: search
ms.openlocfilehash: 875d6e928f5136ec0b33d013cc111739a3b6067e
ms.sourcegitcommit: 2c8a12389b82ee5101b2bd17eae11b42e65e52c0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "45142311"
---
# <a name="use-the-microsoft-search-api-in-microsoft-graph-to-search-custom-types"></a><span data-ttu-id="a8416-103">Использование API службы поиска Microsoft в Microsoft Graph для поиска пользовательских типов</span><span class="sxs-lookup"><span data-stu-id="a8416-103">Use the Microsoft Search API in Microsoft Graph to search custom types</span></span>

<span data-ttu-id="a8416-104">С помощью API Microsoft Search можно импортировать внешние данные через ресурс [екстерналитем](/graph/api/resources/externalitem?view=graph-rest-beta) и запускать поисковые запросы для этого внешнего контента.</span><span class="sxs-lookup"><span data-stu-id="a8416-104">You can use the Microsoft Search API to import external data via the [externalItem](/graph/api/resources/externalitem?view=graph-rest-beta) resource, and run search queries on this external content.</span></span>

[!INCLUDE [search-api-preview-signup](../includes/search-api-preview-signup.md)]

<span data-ttu-id="a8416-105">Чтобы выполнить поиск пользовательских типов, укажите следующие данные в тексте запроса метода [запроса](/graph/api/search-query?view=graph-rest-beta) :</span><span class="sxs-lookup"><span data-stu-id="a8416-105">To search for custom types, specify the following in the [query](/graph/api/search-query?view=graph-rest-beta) method request body:</span></span>

- <span data-ttu-id="a8416-106">Свойство **контентсаурцес** для включения идентификатора подключения, назначаемого во время установки соединителя</span><span class="sxs-lookup"><span data-stu-id="a8416-106">The **contentSources** property to include the connection ID that is assigned during the connector setup</span></span>

- <span data-ttu-id="a8416-107">Свойство **EntityTypes** в качестве`externalItem`</span><span class="sxs-lookup"><span data-stu-id="a8416-107">The **entityTypes** property as `externalItem`</span></span>

- <span data-ttu-id="a8416-108">Свойство **stored_fields** , включающее поля внешнего элемента, которые требуется получить</span><span class="sxs-lookup"><span data-stu-id="a8416-108">The **stored_fields** property to include the fields in the external item you want to retrieve</span></span>

## <a name="example"></a><span data-ttu-id="a8416-109">Пример</span><span class="sxs-lookup"><span data-stu-id="a8416-109">Example</span></span>

### <a name="request"></a><span data-ttu-id="a8416-110">Запрос</span><span class="sxs-lookup"><span data-stu-id="a8416-110">Request</span></span>

```HTTP
POST https://graph.microsoft.com/beta/search/query
Content-Type: application/json
```

```json
{
  "requests": [
    {
      "entityTypes": [
        "externalItem"
      ],
      "contentSources": [
        "/external/connections/servicenow-connector-contoso"
      ],
      "query": {
        "query_string": {
          "query": "contoso tickets"
        }
      },
      "from": 0,
      "size": 25,
      "stored_fields": [
        "number",
        "shortdescription",
        "syscreatedon",
        "accessurl",
        "previewContent"
      ]
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="a8416-111">Отклик</span><span class="sxs-lookup"><span data-stu-id="a8416-111">Response</span></span>

```json
{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.searchResponse)",
  "value": [
    {
      "hitsContainers": [
        {
          "total": 2,
          "moreResultsAvailable": false,
          "hits": [
            {
              "_id": "AAMkADc0NDNlNTE0",
              "_score": 1,
              "_sortField": "Relevance",
              "_source": {
                "@odata.type": "#microsoft.graph.externalItem",
                "properties": {
                  "number": "KB0010025",
                  "shortdescription": "Contoso maintenance guidelines",
                  "syscreatedon": "2019-10-14T22:45:02Z",
                  "accessurl": "https://contoso.service-now.com/kb_view.do?sys_kb_id=6b5465781ba000104793877ddc4bcb81",
                  "previewContent": "Contoso maintenance guidelines"
                }
              }
            },
            {
              "_id": "MG+1glPAAAAAAl3AAA=",
              "_score": 2,
              "_sortField": "Relevance",
              "_source": {
                "@odata.type": "#microsoft.graph.externalItem",
                "properties": {
                  "number": "KB0054396",
                  "shortdescription": "Contoso : Setting Office for the first time.",
                  "syscreatedon": "2019-08-09T01:53:26Z",
                  "accessurl": "https://contoso.service-now.com/kb_view.do?sys_kb_id=004d8d931b0733004793877ddc4bcb29",
                  "previewContent": "Description:  Setting Office for the first time.  Resolution:    To setup any Office app for the first time, tap any Office app like Word to launch it.    Tap Sign in if you already have a Microsoft Account or a Microsoft 365 work or school account."
                }
              }
            }
          ]
        }
      ]
    }
  ]
}
```

## <a name="known-limitations"></a><span data-ttu-id="a8416-112">Известные ограничения</span><span class="sxs-lookup"><span data-stu-id="a8416-112">Known limitations</span></span>

- <span data-ttu-id="a8416-113">Пользовательские типы не поддерживают поиск в нескольких источниках (указывается в **контентсаурцес**).</span><span class="sxs-lookup"><span data-stu-id="a8416-113">Custom types don’t support searching across multiple sources (specified in **contentSources**).</span></span> <span data-ttu-id="a8416-114">Одновременно можно выполнять поиск только по одному подключению.</span><span class="sxs-lookup"><span data-stu-id="a8416-114">You can search only one connection at a time.</span></span>

- <span data-ttu-id="a8416-115">Необходимо указать свойство **stored_fields** ; в противном случае результаты поиска не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="a8416-115">You must specify the **stored_fields** property; otherwise, search results are not returned.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a8416-116">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="a8416-116">Next steps</span></span>

- [<span data-ttu-id="a8416-117">Использование API Поиска (Майкрософт) для запроса данных</span><span class="sxs-lookup"><span data-stu-id="a8416-117">Use the Microsoft Search API to query data</span></span>](/graph/api/resources/search-api-overview?view=graph-rest-beta)
