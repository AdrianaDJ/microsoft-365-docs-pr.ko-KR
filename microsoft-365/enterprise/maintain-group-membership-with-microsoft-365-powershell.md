---
title: PowerShell을 사용 하 여 보안 그룹 구성원 유지 관리
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- PowerShell
- Ent_Office_Other
- O365ITProTrain
ms.assetid: 6770c5fa-b886-4512-8c67-ffd53226589e
description: PowerShell을 사용 하 여 Microsoft 365 그룹의 멤버 자격을 유지 하는 방법을 알아봅니다.
ms.openlocfilehash: b47f501c9726e1d4dcb2e9d61108224db0408b8e
ms.sourcegitcommit: fcc1b40732f28f075d95faffc1655473e262dd95
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/14/2020
ms.locfileid: "49073064"
---
# <a name="maintain-security-group-membership-with-powershell"></a>PowerShell을 사용 하 여 보안 그룹 구성원 유지 관리

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

Microsoft 365 관리 센터 대신 microsoft 365 용 PowerShell을 사용 하 여 Microsoft 365의 보안 그룹 구성원을 유지 관리할 수 있습니다. 

>[!Note]
>Microsoft 365 관리 센터를 사용 하 여 [microsoft 365 그룹 구성원을 유지 관리 하는 방법을 알아봅니다](https://docs.microsoft.com/microsoft-365/admin/create-groups/add-or-remove-members-from-groups) . 추가 리소스 목록은 [Manage users and groups](https://docs.microsoft.com/microsoft-365/admin/add-users/)을 참조 하십시오.
>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a>Graph 모듈용 Azure Active Directory PowerShell 사용하기
먼저 [Microsoft 365 테 넌 트에 연결](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)합니다.

### <a name="add-or-remove-user-accounts-as-members-of-a-group"></a>사용자 계정을 그룹의 구성원으로 추가 또는 제거

**Upn을 기준으로 사용자 계정을 추가 하려면** Upn (사용자 계정 이름) (예: belindan@contoso.com) 및 보안 그룹 표시 이름을 입력 하 고 "<" 및 ">" 문자를 제거한 후 powershell 창 또는 powershell ISE (통합 스크립트 환경)에서 이러한 명령을 실행 합니다.

```powershell
$userUPN="<UPN of the user account to add>"
$groupName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

**표시 이름으로 사용자 계정을 추가 하려면** 사용자 계정 표시 이름 (예: Belinda newman)과 그룹 표시 이름을 입력 하 고 powershell 창 또는 powershell ISE에서 다음 명령을 실행 합니다.

```powershell
$userName="<display name of the user account to add>"
$groupName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userName }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

UPN을 사용 하 **여 사용자 계정을 제거 하려면** 사용자 계정 UPN (예: belindan@contoso.com)과 그룹 표시 이름을 입력 하 고 powershell 창 또는 powershell ISE에서이 명령을 실행 합니다.

```powershell
$userUPN="<UPN of the user account to remove>"
$groupName="<display name of the group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

**표시 이름으로 사용자 계정을 제거 하려면** 사용자 계정 표시 이름 (예: Belinda newman)과 그룹 표시 이름을 입력 하 고 powershell 창 또는 powershell ISE에서 다음 명령을 실행 합니다.

```powershell
$userName="<display name of the user account to remove>"
$groupName="<display name of the group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

### <a name="add-or-remove-groups-as-members-of-a-group"></a>그룹 구성원으로 그룹 추가 또는 제거

보안 그룹은 다른 그룹을 구성원으로 포함할 수 있습니다. 그러나 Microsoft 365 그룹은 사용할 수 없습니다. 이 섹션에는 보안 그룹에 대 한 그룹만 추가 하거나 제거 하기 위한 PowerShell 명령이 포함 되어 있습니다.

**표시 이름별로 그룹을 추가 하려면** 추가할 그룹의 표시 이름을 입력 하 고 구성원 그룹을 포함할 그룹의 표시 이름을 채운 다음 powershell 창 또는 powershell ISE에서이 명령을 실행 합니다.

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group that will contain the member group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

**표시 이름으로 그룹을 제거 하려면** 제거할 그룹의 표시 이름과 구성원 그룹을 포함 하는 그룹의 표시 이름을 입력 하 고 powershell 창 또는 powershell ISE에서이 명령을 실행 합니다.

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group that will contain the member group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a>Windows PowerShell용 Microsoft Azure Active Directory 모듈 사용하기

먼저 [Microsoft 365 테 넌 트에 연결](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)합니다.


### <a name="add-or-remove-user-accounts-as-members-of-a-group"></a>사용자 계정을 그룹의 구성원으로 추가 또는 제거

**Upn을 기준으로 사용자 계정을 추가 하려면** Upn (사용자 계정 이름)을 입력 하 고 (예: belindan@contoso.com), 그룹 표시 이름을 "<" 및 ">" 문자를 제거 하 고 powershell 창 또는 powershell ISE에서이 명령을 실행 합니다.

```powershell
$userUPN="<UPN of the user account to add>"
$groupName="<display name of the group>"
Add-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

**표시 이름으로 사용자 계정을 추가 하려면** 사용자 계정 표시 이름 (예: Belinda newman)과 그룹 표시 이름을 입력 하 고 powershell 창 또는 powershell ISE에서 다음 명령을 실행 합니다.

```powershell
$userName="<display name of the user account to add>"
$groupName="<display name of the group>"
Add-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.DisplayName -eq $userName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

UPN을 사용 하 **여 사용자 계정을 제거 하려면** 사용자 계정 UPN (예: belindan@contoso.com)과 그룹 표시 이름을 입력 하 고 powershell 창 또는 powershell ISE에서이 명령을 실행 합니다.

```powershell
$userUPN="<UPN of the user account to remove>"
$groupName="<display name of the group>"
Remove-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

**표시 이름으로 사용자 계정을 제거 하려면** 사용자 계정 표시 이름 (예: Belinda newman)과 그룹 표시 이름을 입력 하 고 powershell 창 또는 powershell ISE에서 다음 명령을 실행 합니다.

```powershell
$userName="<display name of the user account to remove>"
$groupName="<display name of the group>"
Remove-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.DisplayName -eq $userName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

### <a name="add-or-remove-groups-as-members-of-a-group"></a>그룹 구성원으로 그룹 추가 또는 제거

보안 그룹은 다른 그룹을 구성원으로 포함할 수 있습니다. 그러나 Microsoft 365 그룹은 사용할 수 없습니다. 이 섹션에는 보안 그룹에 대 한 그룹만 추가 하거나 제거 하기 위한 PowerShell 명령이 포함 되어 있습니다.

**표시 이름별로 그룹을 추가 하려면** 추가할 그룹의 표시 이름을 입력 하 고 구성원 그룹을 포함할 그룹의 표시 이름을 채운 다음 powershell 창 또는 powershell ISE에서이 명령을 실행 합니다.

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group that will contain the member group>"
Add-MsolGroupMember -GroupMemberObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID -GroupMemberType Group
```

**표시 이름으로 그룹을 제거 하려면** 제거할 그룹의 표시 이름과 구성원 그룹을 포함 하는 그룹의 표시 이름을 입력 하 고 powershell 창 또는 powershell ISE에서이 명령을 실행 합니다.

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group contains the member group>"
Remove-MsolGroupMember -GroupMemberObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID -GroupMemberType Group
```

## <a name="see-also"></a>참고 항목

[PowerShell로 Microsoft 365 사용자 계정, 라이선스 및 그룹 관리](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[PowerShell로 Microsoft 365 관리](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[Microsoft 365 용 PowerShell 시작](getting-started-with-microsoft-365-powershell.md)

