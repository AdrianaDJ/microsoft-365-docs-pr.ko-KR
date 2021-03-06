---
title: PowerShell을 사용하여 온라인 비즈니스 정책용 Skype 관리
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/17/2020
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- NOCSH
ms.custom: ''
ms.assetid: ff93a341-6f0f-4f06-9690-726052e1be64
description: '요약: PowerShell을 사용 하 여 정책으로 비즈니스용 Skype Online 사용자 계정 속성을 관리 합니다.'
ms.openlocfilehash: 20a75fa1c131f693fcf30d20477af5c9ee7aed35
ms.sourcegitcommit: 22755cebfbfa2c4dc3f8b4f54ccb23636a211ee5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2020
ms.locfileid: "48477044"
---
# <a name="manage-skype-for-business-online-policies-with-powershell"></a>PowerShell을 사용하여 온라인 비즈니스 정책용 Skype 관리

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

비즈니스용 Skype Online에 대 한 사용자 계정의 여러 속성을 관리 하려면 Microsoft 365 용 PowerShell을 사용 하 여 정책 속성으로 지정 해야 합니다.
  
## <a name="before-you-begin"></a>시작하기 전에

다음 절차에 따라 명령을 실행 하도록 설정 합니다 (이미 완료 한 단계 건너뛰기).

  > [!Note]
  > 비즈니스용 Skype Online 커넥터는 현재 최신 팀 PowerShell 모듈에 포함 되어 있습니다. 최신 팀 PowerShell 공용 릴리스를 사용 하는 경우 비즈니스용 Skype Online 커넥터를 설치할 필요가 없습니다.

1. [팀 PowerShell 모듈](https://docs.microsoft.com/microsoftteams/teams-powershell-install)을 설치 합니다.
    
2. Windows PowerShell 명령 프롬프트를 열고 다음 명령을 실행합니다. 

   ```powershell
   Import-Module MicrosoftTeams
   $userCredential = Get-Credential
   $sfbSession = New-CsOnlineSession -Credential $userCredential
   Import-PSSession $sfbSession
   ```

   메시지가 나타나면 비즈니스용 Skype Online 관리자 계정 이름 및 암호를 입력 합니다.
    
## <a name="manage-user-account-policies"></a>사용자 계정 정책 관리

많은 비즈니스용 Skype Online 사용자 계정 속성은 정책을 사용 하 여 구성 됩니다. 정책은 하나 이상의 사용자에 게 적용할 수 있는 설정의 모음 뿐입니다. 정책 구성에 대 한 자세한 내용을 보려면 FederationAndPICDefault 정책에 대해이 명령 예를 실행 하면 됩니다.
  
```powershell
Get-CsExternalAccessPolicy -Identity "FederationAndPICDefault"
```

그러면 다음과 비슷한 결과가 반환 됩니다.
  
```powershell
Identity                          : Tag:FederationAndPICDefault
Description                       :
EnableFederationAccess            : True
EnableXmppAccess                  : False
EnablePublicCloudAccess           : True
EnablePublicCloudAudioVideoAccess : True
EnableOutsideAccess               : True
```

이 예에서이 정책 내의 값은 페더레이션 사용자와의 통신에 사용 될 수 있는 작업을 결정 합니다. 예를 들어 사용자가 조직 외부의 사용자와 통신할 수 있도록 Enableout간 액세스 속성을 True로 설정 해야 합니다. 이 속성은 Microsoft 365 관리 센터에 나타나지 않습니다. 대신 사용자가 선택한 다른 항목에 따라 속성이 자동으로 True 또는 False로 설정 됩니다. 다른 두 가지 주요 속성은 다음과 같습니다.
  
- **EnableFederationAccess** 는 사용자가 페더레이션 도메인의 사용자와 통신할 수 있는지 여부를 나타냅니다.
    
- **Enablepubliccloudaccess** 는 사용자가 Windows Live 사용자와 통신할 수 있는지 여부를 나타냅니다.
    
따라서 사용자 계정 (예: **EnableFederationAccess $True**)에서 페더레이션 관련 속성을 직접 변경 하지 않습니다. 대신 미리 구성 된 원하는 속성 값을 가진 외부 액세스 정책에 계정을 할당 합니다. 사용자가 페더레이션 사용자와 Windows Live 사용자와 통신할 수 있게 하려면 해당 사용자 계정에 이러한 유형의 통신을 허용 하는 정책이 할당 되어야 합니다.
  
누군가가 조직 외부의 사용자와 통신할 수 있는지 여부를 확인 하려면 다음을 수행 해야 합니다.
  
- 해당 사용자에 게 할당 된 외부 액세스 정책을 확인 합니다.
    
- 해당 정책에서 허용 되는 기능을 확인 합니다.
    
예를 들어 다음 명령을 사용 하 여이 작업을 수행할 수 있습니다.
  
```powershell
Get-CsOnlineUser -Identity "Alex Darrow" | ForEach {Get-CsExternalAccessPolicy -Identity $_.ExternalAccessPolicy}
```

이 명령은 사용자에 게 할당 된 정책을 찾은 다음 해당 정책 내에서 사용 하거나 사용 하지 않도록 설정 된 기능을 찾습니다.
  
PowerShell을 사용 하 여 비즈니스용 Skype Online 정책을 관리 하려면 다음에 대 한 cmdlet을 참조 하세요.

- [클라이언트 정책](https://docs.microsoft.com/previous-versions//mt228132(v=technet.10)#client-policy-cmdlets)
- [회의 정책](https://docs.microsoft.com/previous-versions//mt228132(v=technet.10)#conferencing-policy-cmdlets)
- [모바일 정책](https://docs.microsoft.com/previous-versions//mt228132(v=technet.10)#mobile-policy-cmdlets)
- [온라인 음성 메일 정책](https://docs.microsoft.com/previous-versions//mt228132(v=technet.10)#online-voicemail-policy-cmdlets)
- [음성 라우팅 정책](https://docs.microsoft.com/previous-versions//mt228132(v=technet.10)#voice-routing-policy-cmdlets)


> [!NOTE]
> 비즈니스용 Skype Online 다이얼 플랜은 이름을 제외한 모든 관점에서 정책입니다. Office Communications Server 및 Exchange와의 이전 버전과의 호환성을 제공 하기 위해 "전화 걸기 정책" 대신 "다이얼 플랜" 이라는 이름이 선택 되었습니다. 
  
예를 들어 사용 가능한 모든 음성 정책을 확인 하려면 다음 명령을 실행 합니다.
  
```powershell
Get-CsVoicePolicy
```

> [!NOTE]
> 그러면 사용할 수 있는 모든 음성 정책의 목록이 반환 됩니다. 그러나 모든 정책을 모든 사용자에 게 할당할 수 있는 것은 아닙니다. 이는 라이선스 및 지리적 위치를 포함 하는 다양 한 제한으로 인해 발생 합니다. ("[사용 위치](https://msdn.microsoft.com/library/azure/dn194136.aspx)" 라고 부르는 ") 특정 사용자에 게 할당할 수 있는 외부 액세스 정책 및 회의 정책을 확인 하려면 다음과 같은 명령을 사용 합니다. 

```powershell
Get-CsConferencingPolicy -ApplicableTo "Alex Darrow"
Get-CsExternalAccessPolicy -ApplicableTo "Alex Darrow"
```

적용 범위 Ableto 매개 변수는 반환 된 데이터를 지정 된 사용자에 게 할당할 수 있는 정책 (예: Alex Darrow)으로 제한 합니다. 라이선스 및 사용 위치 제한에 따라 사용 가능한 모든 정책의 하위 집합을 나타낼 수 있습니다. 
  
정책 속성이 Microsoft 365에서 사용 되지 않는 경우도 있고, 일부 경우에는 Microsoft 지원 담당자만 관리할 수 있습니다. 
  
비즈니스용 Skype를 사용 하는 경우 사용자는 일종의 정책에 따라 관리 해야 합니다. 유효한 정책 관련 속성이 비어 있는 경우에는 해당 사용자가 사용자 단위 정책을 특별히 할당 하지 않으면 사용자에 게 자동으로 적용 되는 정책 인 전역 정책에 의해 관리 되 고 있음을 의미 합니다. 사용자 계정에 대해 나열 된 클라이언트 정책이 표시 되지 않으므로 글로벌 정책에 의해 관리 됩니다. 다음 명령을 사용 하 여 전역 클라이언트 정책을 결정할 수 있습니다.
  
```powershell
Get-CsClientPolicy -Identity "Global"
```

## <a name="see-also"></a>참고 항목

[PowerShell을 통해 비즈니스용 Skype Oline 관리](manage-skype-for-business-online-with-microsoft-365-powershell.md)
  
[PowerShell로 Microsoft 365 관리](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[Microsoft 365 용 PowerShell 시작](getting-started-with-microsoft-365-powershell.md)

