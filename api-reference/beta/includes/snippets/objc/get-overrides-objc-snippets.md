---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a5a8974a7f86e06ba9af473e7a4d9081b873c5b5
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35489257"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/inferenceClassification/overrides"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *inferenceClassificationOverrideList = [[NSMutableArray alloc] init];
        inferenceClassificationOverrideList = [jsonFinal valueForKey:@"value"];
        MSGraphInferenceClassificationOverride *inferenceClassificationOverride = [[MSGraphInferenceClassificationOverride alloc] initWithDictionary:[inferenceClassificationOverrideList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```