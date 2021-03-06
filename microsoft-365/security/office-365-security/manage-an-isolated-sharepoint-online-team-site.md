---
title: 격리된 SharePoint Online 팀 사이트 관리
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- seo-marvel-apr2020
ms.assetid: 79a61003-4905-4ba8-9e8a-16def7add37c
description: 격리 된 SharePoint Online 팀 사이트를 관리 하 고, 새 사용자 및 그룹을 추가 하 고, 사용자 및 그룹을 제거 하 고, 사용자 지정 권한으로 문서 하위 폴더를 만듭니다.
ms.openlocfilehash: e63cd6d17bf30ce6d236e38673b33cf054940eac
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48200622"
---
# <a name="manage-an-isolated-sharepoint-online-team-site"></a>격리된 SharePoint Online 팀 사이트 관리

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


 **요약:** 이러한 절차를 사용 하 여 격리 된 SharePoint Online 팀 사이트를 관리 합니다.
  
이 문서에서는 격리 된 SharePoint Online 팀 사이트의 일반적인 관리 작업에 대해 설명 합니다.
  
## <a name="add-a-new-user"></a>새 사용자 추가

다른 사용자가 사이트에 참가 하는 경우 사이트 참여 수준을 결정 해야 합니다.
  
- 관리: 새 사용자 계정을 site admins 액세스 그룹에 추가 합니다.
    
- 활성 공동 작업: 사이트 구성원 액세스 그룹에 사용자 계정 추가
    
- 보기: 사이트 뷰어 액세스 그룹에 사용자 계정 추가
    
AD DS (Active Directory 도메인 서비스)를 통해 사용자 계정 및 그룹을 관리 하는 경우 일반 AD DS 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 사용자를 해당 액세스 그룹에 추가 하 고 구독과 동기화를 기다립니다.
  
Microsoft 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 Microsoft 365 관리 센터 또는 Microsoft PowerShell을 사용할 수 있습니다.
  
- Microsoft 365 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 해당 하는 액세스 그룹에 적절 한 사용자를 추가 합니다.
    
- PowerShell의 경우 먼저 [Graph 모듈에 대 한 Azure Active Directory PowerShell을 사용 하 여 연결](https://docs.microsoft.com/microsoft-365/enterprise/connect-to-microsoft-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module)합니다. UPN (사용자 계정 이름)을 사용 하 여 액세스 그룹에 사용자 계정을 추가 하려면 다음 PowerShell 명령 블록을 사용 합니다.
    
```powershell
$userUPN="<UPN of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

표시 이름이 있는 access 그룹에 사용자 계정을 추가 하려면 다음 PowerShell 명령 블록을 사용 합니다.

```powershell
$userDisplayName="<display name of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="add-a-new-group"></a>새 그룹 추가

전체 그룹에 대 한 액세스 권한을 추가 하려면 사이트에서 그룹의 모든 구성원에 대 한 참여 수준을 결정 해야 합니다.
  
- 관리: 사이트 관리자 액세스 그룹에 그룹 추가
    
- 활성 공동 작업: 사이트 구성원 액세스 그룹에 그룹 추가
    
- 보기: 사이트 뷰어 액세스 그룹에 그룹 추가
    
AD DS를 통해 사용자 계정 및 그룹을 관리 하는 경우 일반 AD DS 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 그룹을 적절 한 그룹에 추가 하 고 구독과 동기화를 기다립니다.
  
Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 Microsoft 365 관리 센터 또는 PowerShell을 사용할 수 있습니다.
  
- Microsoft 365 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 적절 한 액세스 그룹에 적절 한 그룹을 추가 합니다.
    
- PowerShell의 경우 먼저 [Graph 모듈에 대 한 Azure Active Directory PowerShell을 사용 하 여 연결](https://docs.microsoft.com/microsoft-365/enterprise/connect-to-microsoft-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module)합니다.
 그런 후 다음 PowerShell 명령을 사용 합니다.
 
```powershell
$newGroupName="<display name of the new group to add>"
$siteGrpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $newGroupName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $siteGrpName }).ObjectID
```

## <a name="remove-a-user"></a>사용자 제거

사이트에서 다른 사용자의 액세스 권한을 제거 해야 하는 경우 해당 사이트의 참가를 기반으로 하는 현재 구성원 인 액세스 그룹에서 해당 항목을 제거 합니다.
  
- 관리: site admins 액세스 그룹에서 사용자 계정 제거
    
- 활성 공동 작업: 사이트 구성원 액세스 그룹에서 사용자 계정을 제거 합니다.
    
- 보기: 사이트 뷰어 액세스 그룹에서 사용자 계정 제거
    
AD DS를 통해 사용자 계정 및 그룹을 관리 하는 경우에는 일반 AD DS 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 액세스 그룹에서 해당 사용자를 제거 하 고 구독과 동기화를 기다립니다.
  
Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 Microsoft 365 관리 센터 또는 PowerShell을 사용할 수 있습니다.
  
- Microsoft 365 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 해당 하는 액세스 그룹에서 해당 사용자를 제거 합니다.
    
- PowerShell의 경우 먼저 [Graph 모듈에 대 한 Azure Active Directory PowerShell을 사용 하 여 연결](https://docs.microsoft.com/microsoft-365/enterprise/connect-to-microsoft-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module)합니다.
UPN을 사용 하 여 액세스 그룹에서 사용자 계정을 제거 하려면 다음 PowerShell 명령 블록을 사용 합니다.
    
```powershell
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

표시 이름이 있는 액세스 그룹에서 사용자 계정을 제거 하려면 다음 PowerShell 명령 블록을 사용 합니다.
    
```powershell
$userDisplayName="<display name of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="remove-a-group"></a>그룹 제거

전체 그룹에 대 한 액세스 권한을 제거 하려면 사이트에서 해당 사용자의 참여에 따라 현재 구성원 인 그룹을 액세스 그룹에서 제거 합니다.
  
- 관리: site admins 액세스 그룹에서 그룹을 제거 합니다.
    
- 활성 공동 작업: 사이트 구성원 액세스 그룹에서 그룹을 제거 합니다.
    
- 보기: 사이트 뷰어 액세스 그룹에서 그룹 제거
    
Windows Server Active Directory를 통해 사용자 계정 및 그룹을 관리 하는 경우 일반 AD DS 사용자 및 그룹 관리 절차를 사용 하 여 적절 한 액세스 그룹에서 해당 그룹을 제거 하 고 구독과 동기화를 기다립니다.
  
Office 365을 통해 사용자 계정 및 그룹을 관리 하는 경우 Microsoft 365 관리 센터 또는 PowerShell을 사용할 수 있습니다.
  
- Microsoft 365 관리 센터의 경우 사용자 계정 관리자 또는 회사 관리자 역할이 할당 된 사용자 계정으로 로그인 하 고 그룹을 사용 하 여 해당 하는 액세스 그룹에서 적절 한 그룹을 제거 합니다.
    
- PowerShell의 경우 먼저 [Graph 모듈에 대 한 Azure Active Directory PowerShell을 사용 하 여 연결](https://docs.microsoft.com/microsoft-365/enterprise/connect-to-microsoft-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module)합니다.    
표시 이름을 사용 하 여 액세스 그룹에서 그룹을 제거 하려면 다음 PowerShell 명령 블록을 사용 합니다.
    
```powershell
$groupMemberName="<display name of the group to remove>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="create-a-documents-subfolder-with-custom-permissions"></a>사용자 지정 권한으로 문서 하위 폴더 만들기

일부 경우에는 격리 된 사이트 내에서 작업 하는 사용자의 하위 집합에 보다 개인적인 공동 작업을 수행 해야 하는 경우가 있습니다. SharePoint Online 사이트의 경우 사이트의 문서 폴더에 하위 폴더를 만들고 사용자 지정 사용 권한을 할당할 수 있습니다. 사용 권한이 없는 권한은 하위 폴더가 표시 되지 않습니다.
  
사용자 지정 사용 권한을 사용 하 여 문서 하위 폴더를 만들려면 다음을 수행 합니다.
  
1. 사이트에 대 한 관리자 액세스 그룹의 구성원 인 계정에 로그인 합니다. 도움을 받으려면 [Microsoft 365에 로그인하는 위치](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4)를 참조하세요.
    
2. 격리 된 팀 사이트로 이동 하 여 **문서**를 클릭 합니다.
    
3. 사용자 지정 사용 권한이 있는 하위 폴더가 포함 될 문서 폴더의 폴더로 이동 하 여 해당 폴더를 만든 다음 엽니다.
    
4. **공유**를 클릭합니다.
    
5. **고급 > 사용 하 여 공유를**클릭 합니다.
    
6. **사용 권한 상속 중지**를 클릭 하 고 **확인**을 클릭 합니다.
    
7. **공유**를 클릭합니다.
    
8. **고급 > 사용 하 여 공유를**클릭 합니다.
    
9. **> Advanced와 공유 > 사용 권한 부여를**클릭 합니다.
    
10. 사용 권한 페이지의 ** \<site name> 목록에서 구성원**을 클릭 합니다.
    
11. ** \<site name> 구성원** 페이지에서 사이트 구성원 액세스 그룹 옆에 있는 확인 표시를 선택 하 고 **작업**을 클릭 한 다음 **그룹에서 사용자 제거**를 클릭 하 고 **확인**을 클릭 합니다.
    
12. 이 하위 폴더에 특정 구성원을 추가 하려면 **새로 만들기 > 사용자 추가**를 클릭 합니다.
    
13. **공유** 대화 상자에서 하위 폴더의 파일에 대해 공동 작업할 수 있는 사용자 계정의 이름을 입력 하 고 **공유**를 클릭 합니다.
    
14. 웹 페이지를 새로 고쳐 새 결과를 확인 합니다.
    
15. 왼쪽 탐색 창의 **그룹** 에서 ** \<site name> 방문자** 그룹을 클릭 하 고 11-14 단계를 사용 하 여 하위 폴더의 파일을 볼 수 있는 사용자 계정 집합 (필요한 경우)을 지정 합니다.
    
16. 왼쪽 탐색 창의 **그룹** 에서 ** \<site name> 소유자** 그룹을 클릭 하 고 11-14 단계를 사용 하 여 하위 폴더의 사용 권한을 관리할 수 있는 사용자 계정 집합 (필요한 경우)을 지정 합니다.
    
17. 브라우저에서 **사용자 및 그룹** 탭을 닫습니다.
    
## <a name="see-also"></a>참고 항목

[격리된 SharePoint Online 팀 사이트](isolated-sharepoint-online-team-sites.md)
  
[격리된 SharePoint Online 팀 사이트 디자인](design-an-isolated-sharepoint-online-team-site.md)

[격리된 SharePoint Online 팀 사이트 배포](deploy-an-isolated-sharepoint-online-team-site.md)



