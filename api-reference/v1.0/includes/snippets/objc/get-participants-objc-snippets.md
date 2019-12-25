---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: d1c5a1a62c05185aada03191a83bcd68d3a1305d
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40871437"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/communications/calls/7531d31f-d10d-44de-802f-c569dbca451c/participants"]]];
[urlRequest setHTTPMethod:@"GET"];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        NSError *jsonError = nil;
        NSDictionary *jsonFinal = [NSJSONSerialization JSONObjectWithData:data options:0 error:&jsonError];
        NSMutableArray *participantList = [[NSMutableArray alloc] init];
        participantList = [jsonFinal valueForKey:@"value"];
        MSGraphParticipant *participant = [[MSGraphParticipant alloc] initWithDictionary:[participantList objectAtIndex: 0] error:&nserror];

}];

[meDataTask execute];

```