---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: bf4bdbeab69ff9711d1644ebfabeebde59e091bf
ms.sourcegitcommit: 2050639c9e9a6b2dab9ce53d6a9fc87e98789b50
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2020
ms.locfileid: "45081337"
---
```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/users"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphUser *user = [[MSGraphUser alloc] init];
[user setDisplayName:@"John Smith"];
NSMutableArray *identitiesList = [[NSMutableArray alloc] init];
MSGraphObjectIdentity *identities = [[MSGraphObjectIdentity alloc] init];
[identities setSignInType:@"userName"];
[identities setIssuer:@"contoso.onmicrosoft.com"];
[identities setIssuerAssignedId:@"johnsmith"];
[identitiesList addObject: identities];
MSGraphObjectIdentity *identities = [[MSGraphObjectIdentity alloc] init];
[identities setSignInType:@"emailAddress"];
[identities setIssuer:@"contoso.onmicrosoft.com"];
[identities setIssuerAssignedId:@"jsmith@yahoo.com"];
[identitiesList addObject: identities];
MSGraphObjectIdentity *identities = [[MSGraphObjectIdentity alloc] init];
[identities setSignInType:@"federated"];
[identities setIssuer:@"facebook.com"];
[identities setIssuerAssignedId:@"5eecb0cd"];
[identitiesList addObject: identities];
[user setIdentities:identitiesList];
MSGraphPasswordProfile *passwordProfile = [[MSGraphPasswordProfile alloc] init];
[passwordProfile setPassword:@"password-value"];
[passwordProfile setForceChangePasswordNextSignIn: false];
[user setPasswordProfile:passwordProfile];
[user setPasswordPolicies:@"DisablePasswordExpiration"];

NSError *error;
NSData *userData = [user getSerializedDataWithError:&error];
[urlRequest setHTTPBody:userData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
    completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

        //Request Completed

}];

[meDataTask execute];

```