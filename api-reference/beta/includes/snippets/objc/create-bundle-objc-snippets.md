---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: bb771961327dfc3c130898a1f62c444761313a4f
ms.sourcegitcommit: bd40e302ce04b686e86989246ab7c4cc9ad3f320
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/03/2020
ms.locfileid: "43127207"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/drive/bundles"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphDriveItem *driveItem = [[MSGraphDriveItem alloc] init];
[driveItem setName:@"Just some files"];
[driveItem set@microsoft.graph.conflictBehavior:@"rename"];
MSGraphBundle *bundle = [[MSGraphBundle alloc] init];
[driveItem setBundle:bundle];
NSMutableArray *childrenList = [[NSMutableArray alloc] init];
MSGraphDriveItem *children = [[MSGraphDriveItem alloc] init];
[children setId:@"1234asdf"];
[childrenList addObject: children];
MSGraphDriveItem *children = [[MSGraphDriveItem alloc] init];
[children setId:@"1234qwerty"];
[childrenList addObject: children];
[driveItem setChildren:childrenList];

NSError *error;
NSData *driveItemData = [driveItem getSerializedDataWithError:&error];
[urlRequest setHTTPBody:driveItemData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```