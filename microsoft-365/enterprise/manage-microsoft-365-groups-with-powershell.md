---
title: PowerShell을 사용 하 여 Microsoft 365 그룹 관리
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
search.appverid:
- MET150
- MOE150
- MED150
- MBS150
- BSA160
- BCS160
ms.assetid: aeb669aa-1770-4537-9de2-a82ac11b0540
description: 이 문서에서는 PowerShell에서 Microsoft 365 그룹에 대 한 일반적인 관리 작업을 수행 하는 방법을 알아봅니다.
ms.openlocfilehash: 1cad2aa39a6b106cbb4dbfbafa995899b2442ed1
ms.sourcegitcommit: 9d1351ea6d9942550b52132817f9f9693ddef2fd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2020
ms.locfileid: "48830618"
---
# <a name="manage-microsoft-365-groups-with-powershell"></a>PowerShell을 사용 하 여 Microsoft 365 그룹 관리

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

이 문서에서는 Microsoft PowerShell의 그룹에 대 한 일반적인 관리 작업을 수행 하는 단계를 제공 합니다. 또한 그룹에 대 한 PowerShell cmdlet도 나열 합니다. SharePoint 사이트 관리에 대 한 자세한 내용은 [PowerShell을 사용 하 여 Sharepoint Online 사이트 관리](https://docs.microsoft.com/sharepoint/manage-team-and-communication-sites-in-powershell)를 참조 하세요.

## <a name="link-to-your-microsoft-365-groups-usage-guidelines"></a>Microsoft 365 Groups 링크 사용 지침
<a name="BK_LinkToGuideLines"> </a>

사용자가 [Outlook에서 그룹을 만들거나 편집할](https://support.office.com/article/04d0c9cf-6864-423c-a380-4fa858f27102.aspx)때 조직의 사용 지침에 대 한 링크를 표시할 수 있습니다. 예를 들어 그룹 이름에 특정 접두사 또는 접미사를 추가 해야 하는 경우

Azure AD (Active Directory) PowerShell을 사용 하 여 사용자가 Microsoft 365 그룹에 대 한 조직의 사용 지침을 가리키도록 합니다. [그룹 설정 구성을 위한 Azure Active Directory cmdlet](https://go.microsoft.com/fwlink/?LinkID=827484) 을 확인 하 고 **디렉터리 수준에서 만들기 설정** 의 단계에 따라 사용 지침 하이퍼링크를 정의 합니다. AAD cmdlet을 실행 하면 사용자는 Outlook에서 그룹을 만들거나 편집할 때 지침에 대 한 링크를 볼 수 있습니다.

![사용 지침 링크를 사용 하 여 새 그룹 만들기](../media/3f74463f-3448-4f24-a0ec-086d9aa95caa.png)

![그룹 사용 지침을 클릭 하 여 조직 Office 365 그룹 지침을 확인 합니다.](../media/d0d54ace-f0ec-4946-b2de-50ce23f17765.png)

## <a name="allow-users-to-send-as-the-microsoft-365-group"></a>사용자가 Microsoft 365 그룹으로 메일을 보낼 수 있도록 허용
<a name="BK_LinkToGuideLines"> </a>

Microsoft 365 그룹을 "다른 사람 이름으로 보내기"로 설정 하려는 경우 [add-recipientpermission](https://docs.microsoft.com/powershell/module/exchange/add-recipientpermission) 및 [add-recipientpermission](https://docs.microsoft.com/powershell/module/exchange/get-recipientpermission) cmdlet을 사용 하 여이를 구성 합니다. 이 설정을 사용 하도록 설정 하면 Microsoft 365 그룹 사용자가 Outlook 또는 웹용 Outlook을 사용 하 여 Microsoft 365 그룹으로 전자 메일을 보내고 회신할 수 있습니다. 사용자는 그룹으로 이동 하 여 새 전자 메일을 만들고 "다른 사람 이름으로 보내기" 필드를 그룹의 전자 메일 주소로 변경할 수 있습니다.

([Exchange 관리 센터 에서도이 작업을 수행할 수](https://docs.microsoft.com/office365/admin/create-groups/allow-members-to-send-as-or-send-on-behalf-of-group)있습니다.)

*\<GroupAlias\>* 업데이트할 그룹의 별칭으로 바꾸고 *\<UserAlias\>* 사용 권한을 부여할 사용자의 별칭으로 대체 하려면 다음 스크립트를 사용 합니다. [Exchange Online PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) 하 여이 스크립트를 실행 합니다.

```PowerShell
$groupAlias = "<GroupAlias>"
$userAlias = "<UserAlias>"
$groupsRecipientDetails = Get-Recipient -RecipientTypeDetails groupmailbox -Identity $groupAlias

Add-RecipientPermission -Identity $groupsRecipientDetails.Name -Trustee $userAlias -AccessRights SendAs
```

일단 cmdlet이 실행 되 면 사용자는 **보낸** 사람 필드에 그룹 전자 메일 주소를 추가 하 여 해당 그룹으로 보낼 outlook 또는 웹용 outlook으로 이동할 수 있습니다.

## <a name="create-classifications-for-microsoft-365-groups-in-your-organization"></a>조직의 Microsoft 365 그룹에 대 한 분류 만들기

조직의 사용자가 Microsoft 365 그룹을 만들 때 설정할 수 있는 민감도 레이블을 만들 수 있습니다. 그룹을 분류 하려는 경우에는 이전 그룹 분류 기능 대신 민감도 레이블을 사용 하는 것이 좋습니다. 민감도 레이블 사용에 대 한 자세한 내용은 [Microsoft 팀, microsoft 365 그룹 및 SharePoint 사이트의 콘텐츠를 보호 하려면 사용 민감도 레이블을](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites)참조 하세요.

> [!IMPORTANT]
> 현재 분류 레이블을 사용 하는 경우 민감도 레이블이 사용 되도록 설정 되 면 그룹을 만드는 사용자는 더 이상 사용할 수 없게 됩니다.

이전 그룹 분류 기능은 계속 사용할 수 있습니다. 조직의 사용자가 Microsoft 365 그룹을 만들 때 설정할 수 있는 분류를 만들 수 있습니다. 예를 들어 사용자가 자신이 만드는 그룹에 "Standard", "Secret" 및 "Top Secret"를 설정 하도록 허용할 수 있습니다. 그룹 분류는 기본적으로 설정 되지 않으며 사용자가이를 설정 하기 위해 만들어야 합니다. Azure Active Directory PowerShell을 사용 하 여 사용자가 Microsoft 365 그룹에 대 한 조직의 사용 지침을 가리키도록 합니다.

[그룹 설정 구성을 위한 Azure Active Directory cmdlet](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-cmdlets) 을 확인 하 고 **디렉터리 수준에서 만들기 설정** 의 단계에 따라 Microsoft 365 그룹에 대 한 분류를 정의 합니다.

```powershell
$setting["ClassificationList"] = "Low Impact, Medium Impact, High Impact"
```

각 분류에 설명을 연결 하기 위해  *ClassificationDescriptions* settings 특성을 사용 하 여 정의할 수 있습니다.

```powershell
$setting["ClassificationDescriptions"] ="Classification:Description,Classification:Description"
```

여기서 분류는 ClassificationList의 문자열과 일치 합니다.

예제:

```powershell
$setting["ClassificationDescriptions"] = "Low Impact: General communication, Medium Impact: Company internal data , High Impact: Data that has regulatory requirements"
```

위의 Azure Active Directory cmdlet을 실행 하 여 분류를 설정한 후에 특정 그룹에 대 한 분류를 설정 하려면 [remove-unifiedgroup](https://docs.microsoft.com/powershell/module/exchange/Set-UnifiedGroup) cmdlet을 실행 합니다.

```powershell
Set-UnifiedGroup <LowImpactGroup@constoso.com> -Classification <LowImpact>
```

또는 분류가 포함 된 새 그룹을 만듭니다.

```powershell
New-UnifiedGroup <HighImpactGroup@constoso.com> -Classification <HighImpact> -AccessType <Public>
```

Exchange online PowerShell을 사용 하는 방법에 대 한 자세한 내용은 exchange [online에서 powershell을 사용 하 여](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell) 확인 하 고 [exchange Online powershell에 연결](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) 합니다.

이러한 설정을 사용 하도록 설정 하면 그룹 소유자가 웹 및 Outlook의 Outlook에 있는 드롭다운 메뉴에서 분류를 선택 하 고 그룹 **편집** 페이지에서이를 저장할 수 있습니다.

![Microsoft 365 그룹 분류 선택](../media/f8d4219a-6180-491d-b0e1-4313ac83998b.png)

## <a name="hide-microsoft-365-groups-from-the-global-address-list"></a>전체 주소 목록에서 Microsoft 365 그룹을 숨깁니다.
<a name="BKMK_CreateClassification"> </a>

조직의 GAL (전체 주소 목록) 및 기타 목록에 Microsoft 365 그룹을 표시할지 여부를 지정할 수 있습니다. 예를 들어 주소 목록에 표시 하지 않으려는 법무 부서 그룹이 있는 경우 GAL에 해당 그룹이 나타나지 않게 할 수 있습니다. 다음과 같이 Set-Unified Group cmdlet을 실행 하 여 주소 목록에서 그룹을 숨깁니다.

```powershell
Set-UnifiedGroup -Identity "Legal Department" -HiddenFromAddressListsEnabled $true
```

## <a name="allow-only-internal-users-to-send-message-to-microsoft-365-groups"></a>내부 사용자만 Microsoft 365 그룹에 메시지를 보낼 수 있도록 허용
<a name="BKMK_CreateClassification"> </a>

다른 조직의 사용자가 Microsoft 365 그룹에 전자 메일을 보내지 못하도록 하려면 해당 그룹의 설정을 변경 하면 됩니다. 이를 통해 내부 사용자만 그룹에 전자 메일을 보낼 수 있습니다. 외부 사용자가 해당 그룹에 메시지를 보내려고 하면 거부 됩니다.

다음과 같이 Set-UnifiedGroup cmdlet을 실행 하 여이 설정을 업데이트할 수 있습니다.

```powershell
Set-UnifiedGroup -Identity "Internal senders only" -RequireSenderAuthenticationEnabled $true
```

## <a name="add-mailtips-to-microsoft-365-groups"></a>Microsoft 365 그룹에 메일 설명 추가
<a name="BKMK_CreateClassification"> </a>

보낸 사람이 Microsoft 365 그룹에 전자 메일을 보내려고 할 때마다 메일 설명이 표시 될 수 있습니다.

그룹에 메일 설명를 추가 하려면 Set-Unified Group cmdlet을 실행 합니다.

```powershell
Set-UnifiedGroup -Identity "MailTip Group" -MailTip "This group has a MailTip"
```

메일 설명와 함께 메일 설명에 대 한 추가 언어를 지정 하는 MailTipTranslations를 설정할 수도 있습니다. 스페인어 번역을 사용할 수 있다고 가정 하 고 다음 명령을 실행 합니다.

```powershell
Set-UnifiedGroup -Identity "MailaTip Group" -MailTip "This group has a MailTip" -MailTipTranslations "@{Add="ES:Esta caja no se supervisa."
```

## <a name="change-the-display-name-of-the-microsoft-365-group"></a>Microsoft 365 그룹의 표시 이름 변경

표시 이름은 Microsoft 365 그룹의 이름을 지정 합니다. Exchange 관리 센터 또는 Microsoft 365 관리 센터에서이 이름을 볼 수 있습니다. Set-UnifiedGroup 명령을 실행 하 여 그룹의 표시 이름을 편집 하거나 기존 Microsoft 365 그룹에 표시 이름을 할당할 수 있습니다.

```powershell
Set-UnifiedGroup -Identity "mygroup@contoso.com" -DisplayName "My new group"
```

## <a name="change-the-default-setting-of-microsoft-365-groups-for-outlook-to-public-or-private"></a>Outlook에 대 한 Microsoft 365 그룹의 기본 설정을 공용 또는 비공개로 변경
<a name="BKMK_CreateClassification"> </a>

Outlook의 Microsoft 365 그룹은 기본적으로 비공개로 만들어집니다. 조직에서 Microsoft 365 그룹을 기본적으로 공용으로 생성 하려는 경우 다음 PowerShell cmdlet 구문을 사용 합니다.

 `Set-OrganizationConfig -DefaultGroupAccessType Public`

비공개로 설정 하려면 다음을 수행 합니다.

 `Set-OrganizationConfig -DefaultGroupAccessType Private`

설정을 확인 하려면

 `Get-OrganizationConfig | ft DefaultGroupAccessType`

자세한 내용은 [set-organizationconfig](https://docs.microsoft.com/powershell/module/exchange/set-organizationconfig) 및 [Get-set-organizationconfig](https://docs.microsoft.com/powershell/module/exchange/get-organizationconfig)를 참조 하십시오.

## <a name="microsoft-365-groups-cmdlets"></a>Microsoft 365 Groups cmdlet

Microsoft 365 그룹에서는 다음과 같은 cmdlet을 사용할 수 있습니다.

|**cmdlet 이름**|**설명**|
|:-----|:-----|
|[Remove-unifiedgroup](https://go.microsoft.com/fwlink/p/?LinkId=616182) <br/> |이 cmdlet을 사용 하 여 기존 Microsoft 365 그룹을 조회 하 고 group 개체의 속성을 볼 수 있습니다.  <br/> |
|[Remove-unifiedgroup](https://go.microsoft.com/fwlink/p/?LinkId=616189) <br/> |특정 Microsoft 365 그룹의 속성 업데이트  <br/> |
|[Remove-unifiedgroup](https://go.microsoft.com/fwlink/p/?LinkId=616183) <br/> |새 Microsoft 365 그룹을 만듭니다. 이 cmdlet은 최소한의 매개 변수 집합을 제공 합니다. 확장 속성의 값을 설정 하려면 새 그룹을 만든 후에 Set-UnifiedGroup를 사용 합니다.  <br/> |
|[Remove-unifiedgroup을 제거 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=616186) <br/> |기존 Microsoft 365 그룹 삭제  <br/> |
|[Add-unifiedgrouplinks](https://go.microsoft.com/fwlink/p/?LinkId=616194) <br/> |Microsoft 365 그룹에 대 한 멤버 자격 및 소유자 정보 검색  <br/> |
|[Add-unifiedgrouplinks 추가](https://go.microsoft.com/fwlink/p/?LinkId=616191) <br/> |기존 Microsoft 365 그룹에 구성원, 소유자 및 구독자 추가 <br/> |
|[Add-unifiedgrouplinks을 제거 합니다.](https://go.microsoft.com/fwlink/p/?LinkId=616195) <br/> |기존 Microsoft 365 그룹에서 소유자 및 구성원을 제거 합니다.  <br/> |
|[UserPhoto](https://go.microsoft.com/fwlink/p/?LinkId=536510) <br/> |계정에 연결 된 사용자 사진에 대 한 정보를 확인 하는 데 사용 됩니다. Active Directory에 사용자 사진 저장  <br/> |
|[UserPhoto](https://go.microsoft.com/fwlink/p/?LinkId=536511) <br/> |사용자 사진을 계정에 연결 하는 데 사용 됩니다. Active Directory에 사용자 사진 저장  <br/> |
|[UserPhoto](https://go.microsoft.com/fwlink/p/?LinkId=536512) <br/> |Microsoft 365 그룹의 사진 제거  <br/> |

## <a name="related-topics"></a>관련 항목

[Microsoft 365 그룹으로 메일 그룹 업그레이드](https://docs.microsoft.com/office365/admin/manage/upgrade-distribution-lists)

[Microsoft 365 그룹을 만들 수 있는 사용자 관리](https://docs.microsoft.com/office365/admin/create-groups/manage-creation-of-groups)

[Microsoft 365 그룹에 대 한 게스트 액세스 관리](https://support.office.com/article/bfc7a840-868f-4fd6-a390-f347bf51aff6)

[에서 정적 그룹 구성원을 동적으로 변경](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-change-type)
