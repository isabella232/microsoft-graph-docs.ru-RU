---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: a1ba073997568524b1ba11bf4da31130e16f771b
ms.sourcegitcommit: 94c8985a3956622ea90f7e641f894d57b0982eb9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2020
ms.locfileid: "44217532"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/teams/{teamId}/schedule/timesOff"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphTimeOff *timeOff = [[MSGraphTimeOff alloc] init];
[timeOff setUserId:@"c5d0c76b-80c4-481c-be50-923cd8d680a1"];
MSGraphTimeOffItem *sharedTimeOff = [[MSGraphTimeOffItem alloc] init];
[sharedTimeOff setTimeOffReasonId:@"TOR_891045ca-b5d2-406b-aa06-a3c8921245d7"];
[sharedTimeOff setStartDateTime: "2019-03-11T07:00:00Z"];
[sharedTimeOff setEndDateTime: "2019-03-12T07:00:00Z"];
[sharedTimeOff setTheme: [MSGraphScheduleEntityTheme white]];
[timeOff setSharedTimeOff:sharedTimeOff];
MSGraphTimeOffItem *draftTimeOff = [[MSGraphTimeOffItem alloc] init];
[draftTimeOff setTimeOffReasonId:@"TOR_891045ca-b5d2-406b-aa06-a3c8921245d7"];
[draftTimeOff setStartDateTime: "2019-03-11T07:00:00Z"];
[draftTimeOff setEndDateTime: "2019-03-12T07:00:00Z"];
[draftTimeOff setTheme: [MSGraphScheduleEntityTheme pink]];
[timeOff setDraftTimeOff:draftTimeOff];

NSError *error;
NSData *timeOffData = [timeOff getSerializedDataWithError:&error];
[urlRequest setHTTPBody:timeOffData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```