---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 8eae39be66c7045bc9d55e9e2f45ea8f5eec4fa7
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40871426"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/communications/calls/491f0b00-ffff-4bc9-a43e-b226498ec22a/redirect"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

NSMutableDictionary *payloadDictionary = [[NSMutableDictionary alloc] init];

NSMutableArray *targetsList = [[NSMutableArray alloc] init];
MSGraphInvitationParticipantInfo *targets = [[MSGraphInvitationParticipantInfo alloc] init];
MSGraphIdentitySet *identity = [[MSGraphIdentitySet alloc] init];
MSGraphIdentity *application = [[MSGraphIdentity alloc] init];
[application setDisplayName:@"test bot 2"];
[application setId:@"22bfd41f-550e-477d-8789-f6f7bd2a5e8b"];
[identity setApplication:application];
[targets setIdentity:identity];
[targetsList addObject: targets];
payloadDictionary[@"targets"] = targetsList;

NSString *callbackUri = @"https://bot.contoso.com/api/calls/24701998-1a73-4d42-8085-bf46ed0ae039";
payloadDictionary[@"callbackUri"] = callbackUri;

NSData *data = [NSJSONSerialization dataWithJSONObject:payloadDictionary options:kNilOptions error:&error];
[urlRequest setHTTPBody:data];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```