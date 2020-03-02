---
title: Office 365 그룹을 만들 수 있는 사용자 관리
f1.keywords:
- NOCSH
ms.author: mikeplum
ms.reviewer: arvaradh
author: MikePlumleyMSFT
manager: pamgreen
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MSP160
- MST160
- MET150
- MOE150
ms.assetid: 4c46c8cb-17d0-44b5-9776-005fced8e618
description: Office 365 그룹을 만들 수 있는 사용자를 제어 하는 방법을 알아봅니다.
ms.openlocfilehash: a211cb3b69348a4d4a401a3c318fe019d8fd257f
ms.sourcegitcommit: 109b44aa71bb8453d0a602663df0fcf7ed7dfdbe
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/25/2020
ms.locfileid: "42277195"
---
# <a name="manage-who-can-create-office-365-groups"></a>Office 365 그룹을 만들 수 있는 사용자 관리

  
사용자가 Office 365 그룹을 매우 쉽게 만들 수 있으므로 다른 사람을 대신하여 이러한 그룹을 만들어 달라는 요청을 많이 받게 되지는 않습니다. 그러나 비즈니스에 따라 그룹을 만들 수 있는 사용자를 제어하고자 할 수 있습니다.
  
이 문서에서는 **그룹을 사용하는 모든 Office 365 서비스에서** 그룹을 만드는 기능을 사용하지 않도록 설정하는 방법을 설명합니다. 
  
- Outlook
    
- SharePoint
    
- Yammer
    
- Microsoft Teams

- Microsoft Stream
    
- StaffHub
    
- Planner
    
- PowerBI

- 로드맵
    
특정 보안 그룹의 구성원으로 Office 365 그룹 만들기를 제한할 수 있습니다. 이를 구성 하기 위해 Windows PowerShell을 사용 합니다. 이 문서에서는 필요한 단계를 안내 합니다.
  
이 문서에서 설명 하는 단계에서는 특정 역할의 구성원이 그룹을 만들 수 없습니다. Office 365 전역 관리자는 Microsoft 365 관리 센터, Planner, 팀, Exchange, SharePoint Online 등의 모든 수단을 통해 그룹을 만들 수 있습니다. 다른 역할은 제한 된 방법 (아래 참조)을 통해 그룹을 만들 수 있습니다.
        
  - Exchange 관리자: Exchange 관리 센터, Azure AD
    
  - 파트너 계층 1 지원: Microsoft 365 관리 센터, Exchange 관리 센터, Azure AD
    
  - 파트너 계층 2 지원: Microsoft 365 관리 센터, Exchange 관리 센터, Azure AD
    
  - 디렉터리 작성자: Azure AD

  - SharePoint 관리자: SharePoint 관리 센터, Azure AD
  
  - 팀 서비스 관리자: 팀 관리 센터, Azure AD
  
  - 사용자 관리 관리자: Microsoft 365 관리 센터, Yammer, Azure AD
     
이러한 역할 중 하나의 구성원인 경우 제한된 사용자에 대해 Office 365 그룹을 만든 다음 사용자를 그룹 소유자로 할당할 수 있습니다. 이 역할이 있는 사용자는 생성을 방해할 수 있는 PowerShell 설정에 관계 없이 Yammer에서 연결 된 그룹을 만들 수 있습니다.

## <a name="licensing-requirements"></a>라이선스 요구 사항

그룹을 만드는 사용자를 관리 하기 위해 다음 사용자에 게 할당 된 Azure AD Premium 라이선스 또는 Azure AD Basic .EDU 라이선스가 필요 합니다.

- 이러한 그룹 만들기 설정을 구성 하는 관리자
- 그룹을 만들 수 있는 보안 그룹의 구성원

다음 사용자는 Azure AD Premium 또는 Azure AD Basic .EDU 라이선스를 할당할 필요가 없습니다.

- Office 365 그룹의 구성원이 고 다른 그룹을 만들 수 없는 사용자입니다.

## <a name="step-1-create-a-security-group-for-users-who-need-to-create-office-365-groups"></a>1단계: Office 365 그룹을 만들어야 하는 사용자에 대한 보안 그룹 만들기

조직의 보안 그룹을 하나만 사용 하 여 그룹을 만들 수 있는 사용자를 제어할 수 있습니다. 그러나 다른 보안 그룹을 이 그룹의 구성원으로 중첩할 수 있습니다. 예를 들어 그룹 만들기 허용이라는 그룹이 지정된 보안 그룹이고, Microsoft 플래너 사용자 및 Exchange Online 사용자라는 그룹이 해당 그룹의 구성원입니다.

위에 나열 된 역할의 관리자는 그룹을 만들 수 있는 기능을 유지 하므로이 그룹의 구성원 일 필요는 없습니다.

> [!IMPORTANT]
> **보안 그룹** 을 사용 하 여 그룹을 만들 수 있는 사용자를 제한 해야 합니다. Office 365 그룹을 사용하려고 하면 SharePoint에서 보안 그룹을 확인하므로 구성원이 SharePoint에서 그룹을 만들 수 없습니다. 
    
1. 관리 센터에서 **그룹** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">그룹</a> 페이지로 이동 합니다.

2. **그룹 추가**를 클릭 합니다.

3. 그룹 유형으로 **보안** 을 선택 합니다. 그룹의 이름을 기억하세요! 나중에 필요합니다.
  
4. 조직에서 그룹을 만들 수 있도록 하려는 사용자 또는 다른 보안 그룹을 추가 하 여 보안 그룹 설정을 완료 합니다.
    
자세한 내용은 [Microsoft 365 관리 센터에서 보안 그룹 만들기, 편집 또는 삭제](../email/create-edit-or-delete-a-security-group.md)를 참조 하세요.
  
## <a name="step-2-install-the-preview-version-of-the-azure-active-directory-powershell-for-graph"></a>2 단계: Graph 용 Azure Active Directory PowerShell의 preview 버전 설치

이러한 절차를 수행 하려면 Graph 용 Azure Active Directory PowerShell의 preview 버전이 필요 합니다. GA 버전은 작동 하지 않습니다.


> [!IMPORTANT]
> 같은 컴퓨터에 preview와 GA 버전을 동시에 모두 설치할 수는 없습니다. Windows 10, Windows Server 2016에 모듈을 설치할 수 있습니다.

  
*항상*  최신 상태로 유지하는 것이 좋습니다. 이전 AzureADPreview 또는 old AzureAD 버전을 제거하고 최신 버전을 설치하세요. 
  
1. 검색 창에 Windows PowerShell을 입력합니다.
    
2. Right-click on **Windows PowerShell** and select **Run as Administrator**.
    
    !["관리자 권한으로 실행"으로 PowerShell을 여세요.](../media/52517af8-c7b0-4c8f-b2f3-0f82f9d5ace1.png)
    
3. [ExecutionPolicy](https://docs.microsoft.com/powershell/module/microsoft.powershell.security/set-executionpolicy)을 사용 하 여 RemoteSigned에 정책을 설정 합니다.
    
    ```
    Set-ExecutionPolicy RemoteSigned
    ```
  
4. 설치된 모듈 확인:
    
    ```
    Get-InstalledModule -Name "AzureAD*"
    ```

5. 이전 버전의 AzureADPreview 또는 AzureAD를 제거하려면 다음 명령을 실행합니다.
  
    ```
    Uninstall-Module AzureADPreview
    ```

    또는
  
    ```
    Uninstall-Module AzureAD
    ```

6. To install the latest version of AzureADPreview, run this command:
  
    ```
    Install-Module AzureADPreview
    ```

    At the message about an untrusted repository, type **Y**. It will take a minute or so for the new module to install. 

아래의 3 단계에 대해 PowerShell 창을 열어 두세요.
  
## <a name="step-3-run-powershell-commands"></a>3 단계: PowerShell 명령 실행

아래 스크립트를 메모장과 같은 텍스트 편집기 또는 [Windows POWERSHELL ISE](https://docs.microsoft.com/powershell/scripting/components/ise/introducing-the-windows-powershell-ise)에 복사 합니다.

* \<SecurityGroupName\> * 을 만든 보안 그룹의 이름으로 바꿉니다. 예:

`$GroupName = "Group Creators"`

파일을 GroupCreators 저장 합니다. p s. 

PowerShell 창에서 파일을 저장 한 위치로 이동 합니다 ("CD <FileLocation>" 형식).

다음 명령을 입력 하 여 스크립트를 실행 합니다.

`.\GroupCreators.ps1`

메시지가 표시 되 면 [관리자 계정으로 로그인](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#step-2-connect-to-azure-ad-for-your-office-365-subscription) 합니다.

```PowerShell
$GroupName = "<SecurityGroupName>"
$AllowGroupCreation = "False"

Connect-AzureAD

$settingsObjectID = (Get-AzureADDirectorySetting | Where-object -Property Displayname -Value "Group.Unified" -EQ).id
if(!$settingsObjectID)
{
      $template = Get-AzureADDirectorySettingTemplate | Where-object {$_.displayname -eq "group.unified"}
    $settingsCopy = $template.CreateDirectorySetting()
    New-AzureADDirectorySetting -DirectorySetting $settingsCopy
    $settingsObjectID = (Get-AzureADDirectorySetting | Where-object -Property Displayname -Value "Group.Unified" -EQ).id
}

$settingsCopy = Get-AzureADDirectorySetting -Id $settingsObjectID
$settingsCopy["EnableGroupCreation"] = $AllowGroupCreation

if($GroupName)
{
    $settingsCopy["GroupCreationAllowedGroupId"] = (Get-AzureADGroup -SearchString $GroupName).objectid
}
 else {
$settingsCopy["GroupCreationAllowedGroupId"] = $GroupName
}
Set-AzureADDirectorySetting -Id $settingsObjectID -DirectorySetting $settingsCopy

(Get-AzureADDirectorySetting -Id $settingsObjectID).Values
```

스크립트의 마지막 줄에 업데이트 된 설정이 표시 됩니다.

![This is what your settings will look like when you're done.](../media/952cd982-5139-4080-9add-24bafca0830c.png)

나중에 사용 되는 보안 그룹을 변경 하려는 경우 새 보안 그룹의 이름으로 스크립트를 다시 실행할 수 있습니다.

그룹 만들기 제한을 해제 하 고 모든 사용자가 그룹을 만들 수 있도록 하려면 $GroupName를 ""로 설정 하 고 $AllowGroupCreation "True"로 설정한 후 스크립트를 다시 실행 합니다.
    
## <a name="step-4-verify-that-it-works"></a>4 단계: 작동 하는지 확인

1. 그룹을 만드는 기능이 없어야 하는 사람의 사용자 계정으로 Office 365에 로그인합니다. 즉, 사용자가 만들었거나 관리자가 만든 보안 그룹의 구성원이 아닙니다.
    
2. **Planner** 타일을 선택 합니다. 
    
3. Planner의 왼쪽 탐색 창에서 **새 계획** 을 선택 하 여 계획을 만듭니다. 
  
4. 계획 및 그룹 만들기가 사용 하지 않도록 설정 된다는 메시지가 표시 됩니다.

보안 그룹의 구성원을 사용 하 여 동일한 절차를 다시 시도 합니다.

> [!NOTE]
> 보안 그룹의 구성원이 그룹을 만들 수 없는 경우 해당 구성원은 해당 [OWA 사서함 정책을](https://go.microsoft.com/fwlink/?linkid=852135)통해 차단 되지 않아야 합니다.
    
## <a name="related-articles"></a>관련 문서

[Office 365 PowerShell 시작](https://go.microsoft.com/fwlink/p/?LinkId=808033)

[Azure Active Directory에서 셀프 서비스 그룹 관리 설정](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-self-service-management)

[Set-ExecutionPolicy](https://docs.microsoft.com/powershell/module/microsoft.powershell.security/set-executionpolicy)

[그룹 설정 구성을 위한 Azure Active Directory cmdlet](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-cmdlets)