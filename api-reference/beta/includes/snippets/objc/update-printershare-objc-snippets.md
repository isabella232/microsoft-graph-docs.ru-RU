---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 9849fa45dfd66c2aa1b5dfcc9525fc31348ee1d9
ms.sourcegitcommit: 33ffed5b785abf36b1a7786856c9266958830d25
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2020
ms.locfileid: "42947646"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/print/printerShares/{id}"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphPrinterShare *printerShare = [[MSGraphPrinterShare alloc] init];
[printerShare setName:@"ShareName"];

NSError *error;
NSData *printerShareData = [printerShare getSerializedDataWithError:&error];
[urlRequest setHTTPBody:printerShareData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```