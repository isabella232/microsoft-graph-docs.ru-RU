---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f405bde0c5404f2b21db59a909083d15bd3c2cd0
ms.sourcegitcommit: 0e1101d499f35b08aa2309e273871438b1774979
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "35335109"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/privilegedRoles/{id}/assignments"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *privilegedRoleAssignmentList = [[NSMutableArray alloc] init];
        privilegedRoleAssignmentList = [jsonFinal valueForKey:@"value"];
        MSGraphPrivilegedRoleAssignment *privilegedRoleAssignment = [[MSGraphPrivilegedRoleAssignment alloc] initWithDictionary:[privilegedRoleAssignmentList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```