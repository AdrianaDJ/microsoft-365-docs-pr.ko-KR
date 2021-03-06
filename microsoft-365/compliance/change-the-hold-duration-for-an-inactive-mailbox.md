---
title: 비활성 사서함의 보존 기간 변경
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
ms.custom:
- seo-marvel-apr2020
description: Office 365 사서함이 비활성 상태가 되 면 비활성 사서함에 할당 된 보류 또는 Office 365 보존 정책의 기간을 변경 합니다.
ms.openlocfilehash: 675e6eb36f762a50c3caafce07d09fda9ba9d98e
ms.sourcegitcommit: e8b9a4f18330bc09f665aa941f1286436057eb28
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/14/2020
ms.locfileid: "45126379"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox"></a>비활성 사서함의 보존 기간 변경

비활성 사서함은 조직에서 이전 직원의 전자 메일을 유지 하는 데 사용 됩니다. 소송 보존, 원본 위치 유지, Microsoft 365 보존 정책 또는 eDiscovery 사례와 관련 된 보류가 사서함에 배치 되 고 해당 사용자 계정이 삭제 되 면 사서함이 비활성화 됩니다. 비활성 사서함의 콘텐츠는 비활성 상태로 설정 되기 전에 사서함에 적용 된 보류 기간 동안 보존 됩니다. 보류 기간은 복구 가능한 항목 폴더에서 항목이 보관 되는 기간을 정의 합니다. 복구 가능한 항목 폴더의 항목에 대 한 보존 기간이 만료 되 면 해당 항목이 비활성 사서함에서 영구적으로 삭제 (제거) 됩니다. 사서함을 비활성화 한 후에는 비활성 사서함에 할당 된 보류 또는 Microsoft 365 보존 정책의 기간을 변경할 수 있습니다.
  
> [!IMPORTANT]
> 계속 해 서 사서함 콘텐츠를 보존 하는 다양 한 방법을 사용할 때 Exchange 관리 센터에서 원본 위치 유지의 만료를 알리는 것입니다. 즉, 소송 보유 및 Microsoft 365 보존 정책을 사용 하 여 비활성 사서함을 만들어야 합니다. 2020 년 4 월 1 일부 터 Exchange Online에 새로운 현재 위치 유지를 만들 수 없습니다. 그러나 비활성 사서함에 저장 된 원본 위치 유지의 보존 기간은 여전히 변경할 수 있습니다. 그러나 2020 년 7 월 1 일부 터 시작 하는 경우에는 보류 시간을 변경할 수 없습니다. 원본 위치 유지를 제거 해야만 비활성 사서함을 삭제할 수 있습니다. 원본 위치 유지 상태인 기존 비활성 사서함은 보존을 제거할 때까지 계속 유지 됩니다. 원본 위치 유지의 만료에 대 한 자세한 내용은 [레거시 eDiscovery 도구의 만료](legacy-ediscovery-retirement.md)를 참조 하세요.
  
## <a name="connect-to-powershell"></a>PowerShell에 연결

- 비활성 사서함의 소송 보존에 대 한 보존 기간을 변경 하려면 Exchange Online PowerShell을 사용 해야 합니다. EAC(Exchange 관리 센터)는 사용할 수 없습니다. 그러나 Exchange Online PowerShell 또는 EAC를 사용 하 여 원본 위치 유지에 대 한 보존 기간을 변경할 수 있습니다. 보안 및 준수 센터 또는 Security & 준수 센터 PowerShell을 사용 하 여 Microsoft 365 보존 정책에 대 한 유지 기간을 변경할 수 있습니다.
    
- Exchange Online PowerShell 또는 보안 & 준수 센터 PowerShell에 연결 하려면 다음 항목 중 하나를 참조 하세요.
    
  - [Exchange Online PowerShell에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [보안 및 준수 센터 PowerShell에 연결하기](https://go.microsoft.com/fwlink/?linkid=799771)
    
- EDiscovery 사례와 관련 된 보류는 무제한 보존으로, 변경할 수 있는 보존 기간이 없음을 의미 합니다. 항목이 영구적으로 또는 보류를 제거 하 고 비활성 사서함이 삭제 될 때까지 유지 됩니다.
    
- 비활성 사서함에 대 한 자세한 내용은 [Microsoft 365의 비활성 사서함](inactive-mailboxes-in-office-365.md)을 참조 하십시오.
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>1 단계: 비활성 사서함의 보류 확인

비활성 사서함에는 여러 가지 유형의 보류 또는 하나 이상의 Microsoft 365 보존 정책이 적용 될 수 있으므로 첫 번째 단계는 비활성 사서함에 대 한 보류를 확인 하는 것입니다.
  
Exchange Online PowerShell에서 다음 명령을 실행 하 여 조직의 모든 비활성 사서함에 대 한 보류 정보를 표시 합니다.
  
```powershell
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```

**LitigationHoldEnabled** 속성의 **True** 값은 비활성 사서함이 소송 보존 상태를 나타냅니다. 원본 위치 유지, eDiscovery 보류 또는 Microsoft 365 보존 정책이 비활성 사서함에 배치 되 면 보류 또는 보존 정책에 대 한 GUID가 **InPlaceHolds** 속성의 값으로 표시 됩니다. 예를 들어 다음은 5 개의 비활성 사서함에 대 한 결과를 보여 줍니다. 
  
```text
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
LitigationHoldDuration: 365.00:00:00
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491}
...
DisplayName           : Mario Necaise
Name                  : marion
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {}
...
DisplayName           : Carol Olson
Name                  : carolo
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {mbxcdbbb86ce60342489bff371876e7f224}
...
DisplayName           : Abraham McMahon
Name                  : abrahamm
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {UniH7d895d48-7e23-4a8d-8346-533c3beac15d}
```

다음 표에는 각 사서함을 비활성화 하는 데 사용 되는 5 가지 서로 다른 보존 유형이 나와 있습니다.
  
|**비활성 사서함**|**보류 유형**|**비활성 사서함에서 보류를 확인 하는 방법**|
|:-----|:-----|:-----|
|Ann Beebe  <br/> |소송 대기  <br/> |*LitigationHoldEnabled* 속성은로 설정 됩니다 `True` .  <br/> |
|Pilar Pinilla  <br/> |원본 위치 유지  <br/> |*InPlaceHolds* 속성은 비활성 사서함에 배치 된 원본 위치 유지의 GUID를 포함 합니다. ID가 접두사로 시작 되지 않으므로 현재 위치 유지로 설정할 수 있습니다.  <br/> `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL`Exchange Online PowerShell의 명령을 사용 하 여 비활성 사서함의 원본 위치 유지에 대 한 정보를 가져올 수 있습니다.  <br/> |
|고 대 Necaise  <br/> |보안 & 준수 센터의 조직 전체 Microsoft 365 보존 정책  <br/> |*InPlaceHolds* 속성은 비어 있습니다. 이는 하나 이상의 조직 전체 또는 (Exchange 전체) Microsoft 365 보존 정책이 비활성 사서함에 적용 됨을 나타냅니다. 이 경우 `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` Exchange Online PowerShell에서 명령을 실행 하 여 조직 전체의 Microsoft 365 보존 정책에 대 한 guid 목록을 가져올 수 있습니다. Exchange 사서함에 적용 되는 조직 전체 보존 정책의 GUID는 접두사로 시작 합니다 `mbx` (예:) `mbxa3056bb15562480fadb46ce523ff7b02` .  <br/> <br/>비활성 사서함에 적용 되는 Microsoft 365 보존 정책을 식별 하려면 Security & 준수 센터 PowerShell에서 다음 명령을 실행 합니다.  <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>
|에이 옛 아들  <br/> |특정 사서함에 적용 되는 보안 & 준수 센터의 Microsoft 365 보존 정책  <br/> |*InPlaceHolds* 속성은 비활성 사서함에 적용 되는 Microsoft 365 보존 정책의 GUID를 포함 합니다. GUID는 접두사로 시작 되므로 특정 사서함에 적용 되는 보존 정책 임을 확인할 수 있습니다 `mbx` . 비활성 사서함에 적용 된 보존 정책의 GUID가 `skp` 접두사로 시작 되 면 보존 정책이 비즈니스용 Skype 대화에 적용 됨을 나타냅니다.  <br/><br/> 비활성 사서함에 적용 되는 Microsoft 365 보존 정책을 식별 하려면 Security & 준수 센터 PowerShell에서 다음 명령을 실행 합니다.<br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name` <br/><br/>`mbx` `skp` 이 명령을 실행할 때 or 접두사를 제거 해야 합니다.  <br/> |
|Abraham McMahon  <br/> |보안 & 준수 센터의 eDiscovery 사례 보류  <br/> |*InPlaceHolds* 속성은 비활성 사서함에 저장 된 eDiscovery 사례 보류의 GUID를 포함 합니다. GUID는 접두사로 시작 되므로 eDiscovery 사례 보류 임을 확인할 수 있습니다 `UniH` .  <br/> `Get-CaseHoldPolicy`보안 & 준수 센터 PowerShell에서 cmdlet을 사용 하 여 비활성 사서함의 보류가 연결 된 eDiscovery 사례에 대 한 정보를 확인할 수 있습니다. 예를 들어 명령을 실행 `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` 하 여 비활성 사서함에 대 한 사례 보류의 이름을 표시할 수 있습니다. `UniH`이 명령을 실행할 때 접두사를 제거 해야 합니다.  <br/><br/> 비활성 사서함의 보류가 연결 된 eDiscovery 사례를 식별 하려면 다음 명령을 실행 합니다.  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/> `Get-ComplianceCase $CaseHold.CaseId | FL Name`<br/><br/><br/> **참고:** 비활성 사서함에 대해서는 eDiscovery 보류를 사용 하지 않는 것이 좋습니다. That's because eDiscovery cases are intended for specific, time-bound cases related to a legal issue. 특정 시점에 법적 사례가 종료 되 고 사례와 관련 된 보류가 제거 되 고 eDiscovery 사례가 닫히거나 삭제 됩니다. 실제로 비활성 사서함에 있는 보류가 eDiscovery 사례와 연결 되 고 보류가 해제 되거나 eDiscovery 사례가 종료 되거나 삭제 되 면 비활성 사서함이 영구적으로 삭제 됩니다. 

Microsoft 365 보존 정책에 대 한 자세한 내용은 [보존 정책 및 보존 레이블에 대 한](retention.md)자세한 정보를 참조 하십시오.
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a>2 단계: 비활성 사서함에 대 한 보존 기간 변경

비활성 사서함에 적용 되는 보존 유형 및 여러 보류가 있는지 확인 한 후에는 보존 기간을 변경 합니다. 
  
### <a name="change-the-duration-for-a-litigation-hold"></a>소송 보존 기간 변경

Exchange Online PowerShell을 사용 하 여 비활성 사서함에 있는 소송 보존의 보존 기간을 변경 하는 방법은 다음과 같습니다. EAC는 사용할 수 없습니다. 다음 명령을 실행 하 여 보존 기간을 변경 합니다. 이 예에서는 보존 기간이 무제한으로 변경 됩니다.
  
```powershell
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

따라서 비활성 사서함의 항목은 무기한 보존 되거나 보존 기간이 다른 값으로 변경 될 때까지 유지 됩니다.
  
> [!TIP]
> 비활성 사서함을 식별 하는 가장 좋은 방법은 해당 **고유 이름이** 나 **Exchange GUID** 값을 사용 하는 것입니다. 이러한 값 중 하나를 사용 하면 실수로 잘못 된 사서함을 지정 하는 것을 방지할 수 있습니다. 
  
### <a name="change-the-duration-for-an-in-place-hold"></a>원본 위치 유지 기간 변경

 EAC 또는 Exchange Online PowerShell을 사용 하 여 원본 위치 유지에 대 한 보존 기간을 변경할 수 있습니다. 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a>EAC를 사용 하 여 보존 기간 변경

1. 변경할 원본 위치 유지의 이름을 알고 있는 경우 다음 단계로 이동 합니다. 그렇지 않으면 다음 명령을 실행 하 여 비활성 사서함에 배치 된 원본 위치 유지의 이름을 가져옵니다. [1 단계](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 구한 원본 위치 유지 GUID를 사용 합니다.

    ```powershell
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. EAC에서 **규정 준수 관리** 원본 \> **위치 eDiscovery &amp; 유지**로 이동 합니다.
    
3. 변경 하려는 원본 위치 유지를 선택 하 고 편집 아이콘 편집을 선택 **Edit** ![ ](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) 합니다.
    
4. 원본 **위치 eDiscovery &amp; 보류** 속성 페이지에서 원본 **위치 유지**를 선택 합니다. 
    
5. 현재 보존 기간에 따라 다음 중 하나를 수행 합니다.
    
    1. 무제한 **보존** 을 선택 하 여 일정 기간 동안 항목을 보존 합니다. 
    
    2. 특정 기간에 대 한 항목을 포함 하도록 **받은 날짜를 기준으로 항목을 보관할 일 수를 지정** 합니다 .를 선택 합니다. 항목을 보유할 일 수를 입력 합니다. 
    
    ![원본 위치 유지 기간을 변경하는 작업의 스크린샷입니다.](../media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. **저장**을 선택합니다.
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a>Exchange Online PowerShell을 사용 하 여 보존 기간 변경

1. 변경할 원본 위치 유지의 이름을 알고 있는 경우 다음 단계로 이동 합니다. 그렇지 않으면 다음 명령을 실행 하 여 비활성 사서함에 배치 된 원본 위치 유지의 이름을 가져옵니다. [1 단계](#step-1-identify-the-holds-on-an-inactive-mailbox)에서 구한 원본 위치 유지 GUID를 사용 합니다.

    ```powershell
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. 다음 명령을 실행 하 여 보존 기간을 변경 합니다. 이 예에서는 보존 기간이 2555 일 (약 7 년)으로 변경 됩니다. 
    
    ```powershell
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     보류 시간을 무제한으로 변경 하려면 _-ItemHoldPeriod 무제한적_을 사용 합니다.
  
## <a name="more-information"></a>추가 정보

- **비활성 사서함의 항목에 대해 보존 기간을 계산 하는 방법** 기간은 사서함 항목을 받거나 만든 원래 날짜부터 계산 됩니다. 
    
- **보존 기간이 만료 되 면 어떻게 됩니까?** 복구 가능한 항목 폴더의 사서함 항목에 대해 보존 기간이 만료 되 면 해당 항목이 비활성 사서함에서 영구적으로 삭제 (제거) 됩니다. 비활성 사서함에 대 한 보존 기간을 지정 하지 않은 경우에는 복구 가능한 항목 폴더의 항목은 제거 되지 않습니다 (비활성 사서함의 보존 기간이 변경 되지 않은 경우). 
    
- **비활성 사서함에서 Exchange 보존 정책이 여전히 처리 되 고 있습니까?** 사용 하지 않을 경우 Exchange 보존 정책 (메시징 레코드 관리 또는 MRM, Exchange Online 기능)이 사서함에 적용 된 경우 **삭제** 보존 작업을 사용 하 여 구성 된 보존 태그는 비활성 사서함에서 계속 처리 됩니다. 즉, 삭제 정책을 사용 하 여 태그가 지정 된 항목은 보존 기간이 만료 될 때 복구 가능한 항목 폴더로 이동 됩니다. 그런 다음 항목의 보존 기간이 만료 되 면 해당 항목이 비활성 사서함에서 제거 됩니다. 
    
    이와 반대로 비활성 사서함에 할당 된 보존 정책에 포함 된 모든 보관 정책 (인, **보관 폴더로 이동** 보존 작업을 사용 하 여 구성 하는 보존 태그)은 무시 됩니다. 즉, 보존 기간이 만료 되 면 보관 정책으로 태그가 지정 된 비활성 사서함의 항목이 기본 사서함에 남아 있습니다. 보관 사서함으로 또는 보관 사서함의 복구 가능한 항목 폴더를 이동 하지는 합니다. 사용자가 비활성 사서함에 로그인 할 수 없기 때문에 보관 정책을 처리 하기 위해 데이터 센터 리소스를 사용 해야 하는 이유는 없습니다. 
    
- **새로 보존 기간을 확인 하려면 다음 명령 중 하나를 실행 합니다.** 첫 번째 명령은 소송 보존에 대 한 것입니다. 두 번째는 원본 위치 유지를 위한 것입니다. 

    ```powershell
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```powershell
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- **일반 사서함 처럼 MFA (관리 되는 폴더 도우미)도 비활성 사서함을 처리 합니다.** Exchange Online에서 MFA는 사서함을 약 7 일 마다 처리 합니다. 비활성 사서함에 대 한 보존 기간을 변경한 후에는 **시작 ManagedFolderAssistant** cmdlet을 사용 하 여 비활성 사서함에 대 한 새 보존 기간을 즉시 처리 하도록 시작할 수 있습니다. 다음 명령을 실행합니다. 

    ```powershell
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- **비활성 사서함에 많은 보류를 적용 하는 경우에는 보류 Guid 중 일부가 표시 되지 않습니다.** 다음 명령을 실행 하 여 비활성 사서함에 저장 된 모든 보류 (소송 보존 제외)의 Guid를 표시할 수 있습니다. 
    
    ```powershell
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
