---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 3f04080a5cfac8562f6cbec115de5f8a78a1724e
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "35726611"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/reports/getTeamsDeviceUsageUserCounts(period='D7')?$format=application/json"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *teamsDeviceUsageUserCountsList = [[NSMutableArray alloc] init];
        teamsDeviceUsageUserCountsList = [jsonFinal valueForKey:@"value"];
        MSGraphTeamsDeviceUsageUserCounts *teamsDeviceUsageUserCounts = [[MSGraphTeamsDeviceUsageUserCounts alloc] initWithDictionary:[teamsDeviceUsageUserCountsList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```