---
title: Microsoft 365 용 PowerShell을 사용 하 여 비즈니스용 Skype Online 정책 할당
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/16/2020
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
ms.assetid: 36743c86-46c2-46be-b9ed-ad9d4e85d186
description: '요약: Microsoft 365 용 PowerShell을 사용 하 여 비즈니스용 Skype Online 정책에 대 한 사용자 단위 통신 설정을 지정 합니다.'
ms.openlocfilehash: 6ff9fce3e0287313f6725b370b6ba89cb939eb3a
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692533"
---
# <a name="assign-per-user-skype-for-business-online-policies-with-powershell-for-microsoft-365"></a>Microsoft 365 용 PowerShell을 사용 하 여 비즈니스용 Skype Online 정책 할당

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

Microsoft 365 용 PowerShell을 사용 하는 것은 비즈니스용 Skype 온라인 정책을 사용 하 여 사용자별 통신 설정을 효율적으로 할당 하는 효율적인 방법입니다.
  
## <a name="prepare-to-run-the-powershell-commands"></a>PowerShell 명령 실행 준비

다음 절차에 따라 명령을 실행 하도록 설정 합니다 (이미 완료 한 단계 건너뛰기).
  
1. [비즈니스용 Skype Online 커넥터 모듈](https://www.microsoft.com/download/details.aspx?id=39366)을 다운로드 하 고 설치 합니다.
    
2. Windows PowerShell 명령 프롬프트를 열고 다음 명령을 실행합니다. 
    
```powershell
Import-Module LyncOnlineConnector
$userCredential = Get-Credential
$sfbSession = New-CsOnlineSession -Credential $userCredential
Import-PSSession $sfbSession
```

메시지가 나타나면 비즈니스용 Skype Online 관리자 계정 이름 및 암호를 입력 합니다.
    
## <a name="updating-external-communication-settings-for-a-user-account"></a>사용자 계정에 대 한 외부 통신 설정 업데이트

사용자 계정에 대 한 외부 통신 설정을 변경 하려는 경우를 예로 들 수 있습니다. 예를 들어 Alex가 페더레이션 사용자와 통신할 수 있도록 허용 하려는 경우 (EnableFederationAccess이 True 인 경우) Windows Live users (EnablePublicCloudAccess와 False)는 사용 하지 않는 것이 좋습니다. 이렇게 하려면 다음과 같은 두 가지 작업을 수행 해야 합니다.
  
1. 기준을 충족하는 외부 액세스 정책을 찾습니다.
    
2. 해당 외부 액세스 정책을 Alex에게 할당합니다.
    
Alex을 할당할 외부 액세스 정책을 결정 하는 방법은 무엇 인가요? 다음 명령은 EnableFederationAccess가 True로 설정되고 EnablePublicCloudAccess가 False로 설정된 모든 외부 액세스 정책을 반환합니다.
  
```powershell
Get-CsExternalAccessPolicy -Include All| Where-Object {$_.EnableFederationAccess -eq $True -and $_.EnablePublicCloudAccess -eq $False}
```

ExternalAccessPolicy의 사용자 지정 인스턴스를 만든 경우가 아니면 해당 명령은 조건을 충족 하는 정책 하나 (FederationOnly)를 반환 합니다. 예를 들면 다음과 같습니다.
  
```powershell
Identity                          : Tag:FederationOnly
Description                       :
EnableFederationAccess            : True
EnableXmppAccess                  : False
EnablePublicCloudAccess           : False
EnablePublicCloudAudioVideoAccess : False
EnableOutsideAccess               : True
```

이제 Alex에 할당할 정책을 알고 있으므로 [get-csexternalaccesspolicy](https://go.microsoft.com/fwlink/?LinkId=523974) cmdlet을 사용 하 여 해당 정책을 할당할 수 있습니다. 예를 들면 다음과 같습니다.
  
```powershell
Grant-CsExternalAccessPolicy -Identity "Alex Darrow" -PolicyName "FederationOnly"
```

정책을 할당 하는 작업은 매우 간단 하며, 사용자의 Id와 할당할 정책의 이름을 지정 하기만 하면 됩니다. 
  
정책 및 정책 할당에 대 한 작업을 수행 하는 경우에는 한 번에 한 사용자 계정을 사용 하는 것으로 제한 되지 않습니다. 페더레이션 파트너 및 Windows Live 사용자와 통신할 수 있는 모든 사용자의 목록이 필요한 경우를 예로 들어 보겠습니다. 여기서 해당 사용자에게는 외부 사용자 액세스 정책 FederationAndPICDefault가 이미 할당되어 있습니다. 이를 알고 있으므로 간단한 명령을 하나씩 실행 하 여 모든 사용자의 목록을 표시할 수 있습니다. 해당 명령은 다음과 같습니다.
  
```powershell
Get-CsOnlineUser -Filter {ExternalAccessPolicy -eq "FederationAndPICDefault"} | Select-Object DisplayName
```

이처럼 ExternalAccessPolicy 속성이 FederationAndPICDefault로 설정된 모든 사용자가 표시됩니다. 화면에 표시 되는 정보의 양을 제한 하기 위해 Select-Object cmdlet을 사용 하 여 각 사용자의 표시 이름만 표시 합니다. 
  
모든 사용자 계정이 같은 정책을 사용 하도록 구성 하려면 다음 명령을 사용 합니다.
  
```powershell
Get-CsOnlineUser | Grant-CsExternalAccessPolicy "FederationAndPICDefault"
```

이 명령은 Get-csonlineuser를 사용 하 여 Lync에 대해 사용 하도록 설정 된 모든 사용자의 컬렉션을 반환한 다음, 모든 해당 정보를 부여-Get-csexternalaccesspolicy로 보내 컬렉션에 있는 각 사용자에 게 FederationAndPICDefault 정책을 할당 합니다.
  
또 다른 예로, 이전에 FederationAndPICDefault 정책을 할당 했 고, 이제 생각이 변경 되었으며 전역 외부 액세스 정책에 의해 관리 되는 것을 Alex 가정해 보겠습니다. 전역 정책은 모든 사용자에 게 명시적으로 할당할 수 없습니다. 대신 해당 사용자에 게 할당 된 사용자별 정책이 없는 경우 지정 된 사용자에 게 글로벌 정책이 사용 됩니다. 따라서 전역 정책에 따라 Alex를 관리 하려면 이전에 자신에 게 할당 된 사용자별 정책을  *할당*  해제 해야 합니다. 예제 명령은 다음과 같습니다.
  
```powershell
Grant-CsExternalAccessPolicy -Identity "Alex Darrow" -PolicyName $Null
```

이 명령은 Alex에 할당 된 외부 액세스 정책의 이름을 null 값 ($Null)으로 설정 합니다. Null은 "nothing"을 의미 합니다. 즉, Alex에 외부 액세스 정책이 할당 되지 않습니다. 사용자에 게 할당 된 외부 액세스 정책이 없으면 해당 사용자는 전역 정책에 의해 관리 됩니다.
  

## <a name="managing-large-numbers-of-users"></a>다 수의 사용자 관리

많은 수의 사용자 (1000 이상)를 관리 하려면 [Invoke](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/invoke-command?view=powershell-7) cmdlet을 사용 하 여 스크립트 블록을 통해 명령을 일괄 처리 해야 합니다.  이전 예제에서는 cmdlet을 실행할 때마다 통화를 설정 하 고 결과를 기다린 후에 다시 전송 해야 합니다.  스크립트 블록을 사용 하는 경우이를 통해 cmdlet이 원격으로 실행 되 고 완료 된 후에는 데이터를 다시 보낼 수 있습니다. 

```powershell
Import-Module LyncOnlineConnector
$sfbSession = New-CsOnlineSession
$users = Get-CsOnlineUser -Filter { ClientPolicy -eq $null } -ResultSize 500

$batch = 50
$filter = ''
$total = $users.Count
$count = 0
    $users | ForEach-Object {
    $upn = $_.UserPrincipalName
    $filter += "(UserPrincipalName -eq '$upn')"
    $batch--
    $count++
    if (($batch -eq 0) -or ($count -eq $total)) {
        $filterSB=[ScriptBlock]::Create($filter)
        Invoke-Command -Session $s -ScriptBlock {param($f) Get-CsOnlineUser -filter $f | Grant-CsClientPolicy -PolicyName "ClientPolicyNoIMURL" -Passthru | Grant-CsExternalAccessPolicy -PolicyName "FederationAndPICDefault"} -ArgumentList $filterSB

        # Reset
        $batch = 50
        $filter = ''
    } else {
        $filter += " -or "
    }
}
```

이렇게 하면 클라이언트 정책이 없는 경우 500 사용자가 한 번에 검색 됩니다. 여기에는 클라이언트 정책 "ClientPolicyNoIMURL"과 외부 액세스 정책 "FederationAndPicDefault"가 부여 됩니다. 결과가 50 그룹으로 일괄 처리 되 고 각 50의 각 배치가 원격 컴퓨터로 전송 됩니다.
  
## <a name="see-also"></a>참고 항목

[PowerShell을 통해 비즈니스용 Skype Oline 관리](manage-skype-for-business-online-with-microsoft-365-powershell.md)
  
[PowerShell로 Microsoft 365 관리](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[Microsoft 365 용 PowerShell 시작](getting-started-with-microsoft-365-powershell.md)
