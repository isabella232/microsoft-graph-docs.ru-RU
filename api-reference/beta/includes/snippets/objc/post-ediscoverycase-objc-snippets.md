---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: abad9613422cc319f9bec76f19f640704f03f412
ms.sourcegitcommit: 496410c1e256aa093eabf27f17e820d9ee91a293
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2020
ms.locfileid: "46566959"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/compliance/ediscovery/cases"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphEdiscoveryCase *ediscoveryCase = [[MSGraphEdiscoveryCase alloc] init];
[ediscoveryCase setDisplayName:@"My Case 1"];

NSError *error;
NSData *ediscoveryCaseData = [ediscoveryCase getSerializedDataWithError:&error];
[urlRequest setHTTPBody:ediscoveryCaseData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```