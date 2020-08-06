---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: cc607e633c70c47aeee25bc047815ee74d4eccc9
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46567257"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/policies/identitySecurityDefaultsEnforcementPolicy"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphIdentitySecurityDefaultsEnforcementPolicy *identitySecurityDefaultsEnforcementPolicy = [[MSGraphIdentitySecurityDefaultsEnforcementPolicy alloc] init];
[identitySecurityDefaultsEnforcementPolicy setIsEnabled: false];

NSError *error;
NSData *identitySecurityDefaultsEnforcementPolicyData = [identitySecurityDefaultsEnforcementPolicy getSerializedDataWithError:&error];
[urlRequest setHTTPBody:identitySecurityDefaultsEnforcementPolicyData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```