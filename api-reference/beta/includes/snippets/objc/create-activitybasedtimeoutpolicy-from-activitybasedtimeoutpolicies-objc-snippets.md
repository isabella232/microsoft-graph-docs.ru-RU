---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 837973e6d5a8505ae1288d47064d4ab89f69ebca
ms.sourcegitcommit: c4d6ccd343a6b298a2aa844f1bad66c736487251
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/11/2020
ms.locfileid: "42589968"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/policies/activityBasedTimeoutPolicies"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphActivityBasedTimeoutPolicy *activityBasedTimeoutPolicy = [[MSGraphActivityBasedTimeoutPolicy alloc] init];
NSMutableArray *definitionList = [[NSMutableArray alloc] init];
[definitionList addObject: @"definition-value"];
[activityBasedTimeoutPolicy setDefinition:definitionList];
[activityBasedTimeoutPolicy setDisplayName:@"displayName-value"];
[activityBasedTimeoutPolicy setIsOrganizationDefault: true];

NSError *error;
NSData *activityBasedTimeoutPolicyData = [activityBasedTimeoutPolicy getSerializedDataWithError:&error];
[urlRequest setHTTPBody:activityBasedTimeoutPolicyData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```