---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d91e452d387b970128b28e4a545e7b0ac83f4551
ms.sourcegitcommit: 1585d55d3e7030b5fd1f7cfd5de8f9fb8202cd56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2019
ms.locfileid: "37429180"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/onenote/pages/{id}/content"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

NSMutableArray *streamList = [[NSMutableArray alloc] init];
MSGraphStream *stream = [[MSGraphStream alloc] init];
[stream setTarget:@"#para-id"];
[stream setAction:@"insert"];
[stream setPosition:@"before"];
[stream setContent:@"<img src=\"image-url-or-part-name\" alt=\"image-alt-text\" />"];
[streamList addObject: stream];
MSGraphStream *stream = [[MSGraphStream alloc] init];
[stream setTarget:@"#list-id"];
[stream setAction:@"append"];
[stream setContent:@"<li>new-page-content</li>"];
[streamList addObject: stream];

NSError *error;
NSData *streamData = [stream getSerializedDataWithError:&error];
[urlRequest setHTTPBody:streamData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```