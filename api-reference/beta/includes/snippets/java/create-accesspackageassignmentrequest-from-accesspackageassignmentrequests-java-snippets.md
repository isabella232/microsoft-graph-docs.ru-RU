---
description: Автоматически созданный файл. НЕ ИЗМЕНЯТЬ
ms.openlocfilehash: 83303f8c80e75b73b61a5b16bb9e7e180cae1104
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48952060"
---
```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

AccessPackageAssignmentRequest accessPackageAssignmentRequest = new AccessPackageAssignmentRequest();
accessPackageAssignmentRequest.requestType = "AdminAdd";
AccessPackageAssignment accessPackageAssignment = new AccessPackageAssignment();
accessPackageAssignment.targetId = "46184453-e63b-4f20-86c2-c557ed5d5df9";
accessPackageAssignment.assignmentPolicyId = "2264bf65-76ba-417b-a27d-54d291f0cbc8";
accessPackageAssignment.accessPackageId = "a914b616-e04e-476b-aa37-91038f0b165b";
accessPackageAssignmentRequest.accessPackageAssignment = accessPackageAssignment;

graphClient.identityGovernance().entitlementManagement().accessPackageAssignmentRequests()
    .buildRequest()
    .post(accessPackageAssignmentRequest);

```