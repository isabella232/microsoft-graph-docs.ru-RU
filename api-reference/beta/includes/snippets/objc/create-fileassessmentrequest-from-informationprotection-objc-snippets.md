---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: f7ec831d305eec8912fe316cde5dabb6460e58ed
ms.sourcegitcommit: f27e81daeff242e623d1a3627405667310395734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/25/2019
ms.locfileid: "40871920"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/informationProtection/threatAssessmentRequests"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphThreatAssessmentRequest *threatAssessmentRequest = [[MSGraphThreatAssessmentRequest alloc] init];
[threatAssessmentRequest setExpectedAssessment: [MSGraphThreatExpectedAssessment block]];
[threatAssessmentRequest setCategory: [MSGraphThreatCategory malware]];
[threatAssessmentRequest setFileName:@"test.txt"];
[threatAssessmentRequest setContentData:@"VGhpcyBpcyBhIHRlc3QgZmlsZQ=="];

NSError *error;
NSData *threatAssessmentRequestData = [threatAssessmentRequest getSerializedDataWithError:&error];
[urlRequest setHTTPBody:threatAssessmentRequestData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```