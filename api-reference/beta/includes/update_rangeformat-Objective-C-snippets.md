---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 810a7e3b8f243ec631a497445841ec2d492afc53
ms.sourcegitcommit: 0e1101d499f35b08aa2309e273871438b1774979
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "35335715"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/drive/items/{id}/workbook/worksheets/Sheet1/range(address='$A$1')/format"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphWorkbookRangeFormat *workbookRangeFormat = [[MSGraphWorkbookRangeFormat alloc] init];
[workbookRangeFormat setColumnWidth: 135];
[workbookRangeFormat setVerticalAlignment:@"Top"];
[workbookRangeFormat setRowHeight: 49];
[workbookRangeFormat setWrapText: false];

NSError *error;
NSData *workbookRangeFormatData = [workbookRangeFormat getSerializedDataWithError:&error];
[urlRequest setHTTPBody:workbookRangeFormatData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```