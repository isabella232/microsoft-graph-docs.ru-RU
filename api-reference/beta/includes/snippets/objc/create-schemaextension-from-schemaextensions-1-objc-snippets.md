---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 8642b5a9dc7f25adee5efc2ba6f1f699e48a4c08
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "35488651"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/beta/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/schemaExtensions"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphSchemaExtension *schemaExtension = [[MSGraphSchemaExtension alloc] init];
[schemaExtension setId:@"graphlearn_courses"];
[schemaExtension setDescription:@"Graph Learn training courses extensions"];
NSMutableArray *targetTypesList = [[NSMutableArray alloc] init];
[targetTypesList addObject: @"Group"];
[schemaExtension setTargetTypes:targetTypesList];
NSMutableArray *propertiesList = [[NSMutableArray alloc] init];
MSGraphExtensionSchemaProperty *properties = [[MSGraphExtensionSchemaProperty alloc] init];
[properties setName:@"courseId"];
[properties setType:@"Integer"];
[propertiesList addObject: properties];
MSGraphExtensionSchemaProperty *properties = [[MSGraphExtensionSchemaProperty alloc] init];
[properties setName:@"courseName"];
[properties setType:@"String"];
[propertiesList addObject: properties];
MSGraphExtensionSchemaProperty *properties = [[MSGraphExtensionSchemaProperty alloc] init];
[properties setName:@"courseType"];
[properties setType:@"String"];
[propertiesList addObject: properties];
[schemaExtension setProperties:propertiesList];

NSError *error;
NSData *schemaExtensionData = [schemaExtension getSerializedDataWithError:&error];
[urlRequest setHTTPBody:schemaExtensionData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```