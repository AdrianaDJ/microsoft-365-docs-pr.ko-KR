---
title: 간단한 기본 구성
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/14/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
- seo-marvel-apr2020
ms.assetid: 6f916a77-301c-4be2-b407-6cec4d80df76
description: 이 테스트 랩 가이드를 사용 하 여 Microsoft 365 for enterprise의 테스트를 위한 간단한 테스트 환경을 만듭니다.
ms.openlocfilehash: 2b8505e142c3c1b87578db7342ed299b95d8c049
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487391"
---
# <a name="the-lightweight-base-configuration"></a>간단한 기본 구성

*이 테스트 랩 가이드는 enterprise 및 Office 365 Enterprise 테스트 환경용 Microsoft 365에 모두 사용할 수 있습니다.*

이 문서에서는 Microsoft 365 E5 구독 및 Windows 10 Enterprise를 실행 하는 컴퓨터를 사용 하 여 단순화 된 환경을 만드는 방법에 대해 설명 합니다.

![간단한 Microsoft 365 Enterprise 테스트 환경](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

간단한 테스트 환경을 만드는 작업에는 다음 다섯 단계가 포함 됩니다.
- [1 단계: Microsoft 365 E5 구독 만들기](#phase-1-create-your-microsoft-365-e5-subscription)
- [2단계: Office 365 평가판 구독 구성](#phase-2-configure-your-office-365-trial-subscription)
- [3단계: Microsoft 365 E5 평가판 구독 추가.](#phase-3-add-a-microsoft-365-e5-trial-subscription)
- [4단계: Windows 10 Enterprise 컴퓨터 만들기](#phase-4-create-a-windows-10-enterprise-computer)
- [5단계: Azure AD에 Windows 10 컴퓨터 가입](#phase-5-join-your-windows-10-computer-to-azure-ad)

결과 환경을 사용 하 여 [기업에 대 한 Microsoft 365](https://www.microsoft.com/microsoft-365/enterprise)의 기능과 기능을 테스트 합니다.

![Microsoft 클라우드의 테스트 랩 가이드](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> 엔터프라이즈 테스트 랩 가이드 스택의 Microsoft 365에 있는 모든 문서에 대 한 시각적 지도를 보려면 [microsoft 365 for Enterprise Test Lab Guide stack](../downloads/Microsoft365EnterpriseTLGStack.pdf)을 참조 하십시오.

>[!NOTE]
>이 문서를 인쇄하여 30일 동안의 Office 365 평가판 구독 기간 동안 환경에 필요한 특정 정보를 기록할 수 있습니다. 추가 30일 동안 평가판 구독을 쉽게 연장할 수 있습니다. 영구 테스트 환경의 경우 별도의 Azure AD 테넌트와 소수의 라이선스를 사용해서 유료 구독을 새로 만듭니다.

## <a name="phase-1-create-your-microsoft-365-e5-subscription"></a>1 단계: Microsoft 365 E5 구독 만들기

Microsoft 365 E5 평가판 구독으로 시작 하 여 Microsoft 365 E5 구독을 추가 합니다.

>[!NOTE]
>테스트 환경에 현재 유료 구독에서 별도의 Azure AD 테 넌 트가 있도록 하려면 Office 365의 평가판 구독을 만드는 것이 좋습니다. 이러한 분리는 프로덕션 구독에 영향을 주지 않고 테스트 테 넌 트에서 사용자 및 그룹을 추가 하 고 제거할 수 있음을 의미 합니다.

Microsoft 365 E5 평가판 구독을 시작하려면 먼저 가상의 회사 이름 및 새 Microsoft 계정이 필요합니다.
  
1. 회사 이름으로 Microsoft 샘플 콘텐츠에 사용되는 가상의 회사인 Contoso의 변형을 사용하는 것이 좋지만 필수는 아닙니다. 여기에 가상의 회사 이름을 기록하세요. ![선](../media/Common-Images/TableLine.png)
    
2. 새 Microsoft 계정을 등록하려면으로 [https://outlook.com](https://outlook.com)으로 이동한 후 새 전자 메일 계정 및 주소를 사용하여 계정을 만듭니다. 이 계정을 사용하여 Office 365에 등록합니다.
    
    - 여기에 새 계정의 이름과 성을 기록합니다. ![선](../media/Common-Images/TableLine.png)
    
    - 여기서 새 전자 메일 계정 주소를 기록합니다. ![선](../media/Common-Images/TableLine.png)@outlook.com
    
### <a name="sign-up-for-an-office-365-e5-trial-subscription"></a>Office 365 E5 평가판 구독 등록

1. 브라우저에서으로 이동 [https://aka.ms/e5trial](https://aka.ms/e5trial) 합니다.
    
2. **Office 365 E5에 대 한 감사** 페이지의 1 단계에서 새 전자 메일 계정 주소를 입력 합니다.
3. 트레일 구독 프로세스의 2 단계에서 요청 된 정보를 입력 한 다음 확인을 수행 합니다.
4. 3 단계에서 조직 이름을 입력 한 다음 구독에 대 한 전역 관리자가 될 계정 이름입니다.
5. 4단계에서 여기에 로그인 페이지를 기록합니다(선택 후 복사). ![Line](../media/Common-Images/TableLine.png)
6. 여기에 사용자 ID를 기록합니다. ![Line](../media/Common-Images/TableLine.png).onmicrosoft.com  
   입력 한 암호를 안전한 위치에 기록 합니다.
   이 값은 **전역 관리자 이름**으로 사용됩니다.
7. **설정으로 이동을**선택 합니다.
8. Office 365 E5 설치에서 계속을 ** *선택 하*고 전자 메일 및 로그인에 대 한 onmicrosoft.com**를 선택한 다음 **종료를 선택 하 고 나중에 계속**합니다.

Microsoft 365 관리 센터가 나타납니다.
    
## <a name="phase-2-configure-your-office-365-trial-subscription"></a>2단계: Office 365 평가판 구독 구성

이 단계에서는 추가 사용자로 구독을 구성하고 Office 365 E5 라이선스를 할당합니다.
  
컴퓨터에서 Graph 모듈에 대 한 Azure Active Directory PowerShell을 사용 하 여 구독에 연결 하려면 PowerShell을 사용 [하 여 Microsoft 365에 연결](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)의 지침을 사용 합니다.
    
**Windows PowerShell 자격 증명 요청** 대화 상자에서 전역 관리자 이름 (예: *jdoe@contosotoycompany.onmicrosoft.com*) 및 암호를 입력 합니다.
  
조직 이름 (예: *contosotoycompany*), 위치에 대 한 두 문자로 된 국가 코드, 공통 계정 암호를 입력 한 다음 PowerShell 프롬프트에서 다음 명령을 실행 합니다.

```powershell
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$commonPW="<common user account password>"
$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password=$commonPW

$userUPN= "user2@" + $orgName + ".onmicrosoft.com"
New-AzureADUser -DisplayName "User 2" -GivenName User -SurName 2 -UserPrincipalName $userUPN -UsageLocation $loc -AccountEnabled $true -PasswordProfile $PasswordProfile -MailNickName "user2"
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value "ENTERPRISEPREMIUM" -EQ).SkuID
$LicensesToAssign = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$LicensesToAssign.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $LicensesToAssign

$userUPN= "user3@" + $orgName + ".onmicrosoft.com"
New-AzureADUser -DisplayName "User 3" -GivenName User -SurName 3 -UserPrincipalName $userUPN -UsageLocation $loc -AccountEnabled $true -PasswordProfile $PasswordProfile -MailNickName "user3"
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value "ENTERPRISEPREMIUM" -EQ).SkuID
$LicensesToAssign = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$LicensesToAssign.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $LicensesToAssign

$userUPN= "user4@" + $orgName + ".onmicrosoft.com"
New-AzureADUser -DisplayName "User 4" -GivenName User -SurName 4 -UserPrincipalName $userUPN -UsageLocation $loc -AccountEnabled $true -PasswordProfile $PasswordProfile -MailNickName "user4"
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value "ENTERPRISEPREMIUM" -EQ).SkuID
$LicensesToAssign = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$LicensesToAssign.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $LicensesToAssign
```
> [!NOTE]
> 여기서 공통 암호를 사용하는 것은 테스트 환경을 위한 구성을 쉽게 하고 자동화하기 위한 것입니다. 물론 프로덕션 구독에서는 공통 암호를 사용하지 않는 것이 좋습니다. 

### <a name="record-key-information-for-future-reference"></a>나중에 참조할 수 있도록 주요 정보 기록

이러한 값을 아직 기록 하지 않은 경우 지금 기록 합니다.
  
- 전역 관리자 이름: ![Line](../media/Common-Images/TableLine.png).onmicrosoft.com (1단계의 스텝 6)
    
    이 계정의 암호도 안전한 위치에 기록합니다.
    
- 평가판 구독 조직 이름:  ![Line](../media/Common-Images/TableLine.png) (1단계의 스텝 4)
    
- 사용자 2, 사용자 3, 사용자 4, 사용자 5에 대한 계정을 나열하려면 Windows PowerShell 프롬프트에 대한 Microsoft Azure Active Directory 모듈에서 다음 명령을 실행합니다.
    
  ```powershell
  Get-AzureADUser | Sort UserPrincipalName | Select UserPrincipalName
  ```

    여기에 계정 이름을 기록합니다.
    
  - 사용자 2 계정 이름: user2@![Line](../media/Common-Images/TableLine.png).onmicrosoft.com
    
  - 사용자 3 계정 이름: user3@![Line](../media/Common-Images/TableLine.png).onmicrosoft.com
    
  - 사용자 4 계정 이름: user4@![Line](../media/Common-Images/TableLine.png).onmicrosoft.com
    
  - 사용자 5 계정 이름: user5@![Line](../media/Common-Images/TableLine.png).onmicrosoft.com
    
    해당 계정의 공통 암호도 안전한 위치에 적어둡니다.
   
### <a name="using-an-office-365-test-environment"></a>Office 365 테스트 환경 사용

Office 365 테스트 환경만 필요한 경우이 문서의 나머지 부분을 읽을 필요가 없습니다.

Office 365 및 Microsoft 365에 모두 적용 되는 추가 테스트 랩 가이드에 대 한 자세한 내용은 [Microsoft 365 for Enterprise Test Lab 가이드](m365-enterprise-test-lab-guides.md)를 참조 하세요.
  
## <a name="phase-3-add-a-microsoft-365-e5-trial-subscription"></a>3단계: Microsoft 365 E5 평가판 구독 추가.

이 단계에서는 Microsoft 365 E5 평가판 구독을 등록하고 Office 365 E5 평가판 구독과 동일한 조직에 추가합니다.
  
우선, Microsoft 365 E5 평가판 구독을 추가하고 전역 관리자 계정에 새로운 Microsoft 365 라이선스를 할당합니다.
  
1. 인터넷 브라우저 비공개 창에서 전역 관리자 계정 자격 증명을 사용 하 여 Microsoft 365 관리 센터에 로그인 [https://admin.microsoft.com](https://admin.microsoft.com) 합니다.
    
2. **Microsoft 365 관리 센터** 페이지의 왼쪽 탐색 영역에서 **결제 > 구입 서비스**를 선택 합니다.
    
3. **서비스 구매** 페이지에서 **Microsoft 365 E5**를 선택한 다음 **무료 평가판 받기를**선택 합니다.

4. **Microsoft 365 E5 평가판** 페이지에서 문자 메시지 또는 전화 통화를 수신 하 고, 전화 번호를 입력 하 고, **텍스트** 를 선택 하거나 전화를 **걸**것을 결정 합니다. 인증을 수행합니다.

5. **주문 확인** 페이지에서 **지금 사용해 보기**를 선택 합니다.

6. **주문 수신** 페이지에서 **계속**을 선택 합니다.

7. Microsoft 365 관리 센터에서 **사용자 > 활성 사용자**를 선택 합니다.

8. **활성 사용자**에서 관리자 계정을 선택 합니다.

9. **라이선스 및 앱**을 선택 합니다.

10. Office 365 Enterprise E5의 라이센스를 비활성화하고 Microsoft 365 E5의 라이센스를 활성화합니다.

11. **변경 내용 저장**을 선택한 다음 사용자 계정 정보 창을 닫습니다.

다음, 다른 모든 계정 (사용자 2, 사용자 3, 사용자 4 및 사용자 5)에 대해 이전 절차의 8단계에서 11단계를 반복합니다.
  
> [!NOTE]
> Microsoft 365 E5 평가판 구독의 길이는 30 일입니다. 영구 테스트 환경의 경우 소수의 라이선스를 사용해서 이 평가판 구독을 유료 구독으로 전환합니다.
  
이제 테스트 환경에는 다음이 구현됩니다.
  
- Microsoft 365 E5 평가판 구독.
- 모든 해당 사용자 계정(전역 관리자만 또는 5개의 사용자 계정 모두)이 Microsoft 365 E5를 사용하도록 설정됩니다.
    
Microsoft 365 E5를 추가 하는 결과 구성은 다음과 같습니다.
  
![Microsoft 365 Enterprise 테스트 환경 3단계](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase2.png)
  
## <a name="phase-4-create-a-windows-10-enterprise-computer"></a>4단계: Windows 10 Enterprise 컴퓨터 만들기

이 단계에서는 Windows 10 Enterprise를 실행하는 독립 실행형 컴퓨터를 실제 컴퓨터, 가상 머신 또는 Azure Virtual Machine으로 만듭니다.
  
### <a name="physical-computer"></a>실제 컴퓨터

개인 컴퓨터에서 Windows 10 Enterprise를 설치 합니다. [여기](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise)에서 Windows 10 Enterprise 평가판을 다운로드할 수 있습니다.
  
### <a name="virtual-machine"></a>가상 컴퓨터

선택한 하이퍼바이저를 사용 하 여 가상 컴퓨터를 만든 다음 Windows 10 Enterprise를 설치 합니다. [여기](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise)에서 Windows 10 Enterprise 평가판을 다운로드할 수 있습니다.
  
### <a name="virtual-machine-in-azure"></a>Azure의 가상 머신

Microsoft Azure에서 Windows 10 가상 머신을 만들려면 Windows 10 Enterprise에 대한 이미지에 액세스할 수 있는 ***Visual Studio 기반 구독이 있어야 합니다***. 다른 유형의 Azure 구독(예: 평가판 및 유료 구독)으로는 이 이미지에 액세스할 수 없습니다. 최신 정보를 보려면 [개발/테스트 시나리오에 Azure의 Windows 클라이언트 사용](https://docs.microsoft.com/azure/virtual-machines/windows/client-images)을 참조하세요.
  
> [!NOTE]
> 다음 명령 집합은 최신 버전의 Azure PowerShell을 사용합니다. [Azure PowerShell cmdlet으로 시작](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/)을 참조하세요. 다음 명령은 리소스 그룹, 저장소 계정 및 가상 네트워크를 포함 하 여 WIN10 라는 Windows 10 Enterprise 가상 컴퓨터와 모든 필수 인프라를 구축 합니다. Azure 인프라 서비스에 이미 익숙한 경우 현재 배포 된 인프라에 맞게 이러한 지침을 조정 합니다.
  
먼저 Microsoft PowerShell 프롬프트를 시작합니다.
  
이 명령을 사용하여 Azure 계정에 로그인합니다.
  
```powershell
Connect-AzAccount
```

이 명령을 사용 하 여 구독 이름을 가져옵니다.
  
```powershell
Get-AzSubscription | Sort Name | Select Name
```

Azure 구독을 설정합니다. 문자를 포함 하 여 따옴표 안에 있는 모든 것을 \< and > 올바른 이름으로 바꿉니다.
  
```powershell
$subscr="<subscription name>"
Get-AzSubscription -SubscriptionName $subscr | Select-AzSubscription
```

다음으로 새 리소스 그룹을 만듭니다. 고유한 리소스 그룹 이름을 확인하려면 이 명령을 사용하여 기존 리소스 그룹을 나열합니다.
  
```powershell
Get-AzResourceGroup | Sort ResourceGroupName | Select ResourceGroupName
```

이러한 명령을 사용하여 새 리소스 그룹을 만듭니다. 문자를 포함 하 여 따옴표 안에 있는 모든 것을 \< and > 올바른 이름으로 바꿉니다.
  
```powershell
$rgName="<resource group name>"
$locName="<location name, such as West US>"
New-AzResourceGroup -Name $rgName -Location $locName
```

다음으로, 다음 명령을 사용 하 여 새 가상 네트워크 및 WIN10 가상 컴퓨터를 만듭니다. 메시지가 표시 되 면 WIN10에 대 한 로컬 관리자 계정의 이름 및 암호를 입력 하 고이를 안전한 위치에 저장 합니다.
  
```powershell
$corpnetSubnet=New-AzVirtualNetworkSubnetConfig -Name Corpnet -AddressPrefix 10.0.0.0/24
New-AzVirtualNetwork -Name "M365Ent-TestLab" -ResourceGroupName $rgName -Location $locName -AddressPrefix 10.0.0.0/8 -Subnet $corpnetSubnet
$rule1=New-AzNetworkSecurityRuleConfig -Name "RDPTraffic" -Description "Allow RDP to all VMs on the subnet" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
New-AzNetworkSecurityGroup -Name Corpnet -ResourceGroupName $rgName -Location $locName -SecurityRules $rule1
$vnet=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "M365Ent-TestLab"
$nsg=Get-AzNetworkSecurityGroup -Name Corpnet -ResourceGroupName $rgName
Set-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name Corpnet -AddressPrefix "10.0.0.0/24" -NetworkSecurityGroup $nsg
$vnet | Set-AzVirtualNetwork
$pip=New-AzPublicIpAddress -Name WIN10-PIP -ResourceGroupName $rgName -Location $locName -AllocationMethod Dynamic
$nic=New-AzNetworkInterface -Name WIN10-NIC -ResourceGroupName $rgName -Location $locName -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $pip.Id
$vm=New-AzVMConfig -VMName WIN10 -VMSize Standard_A2_V2
$cred=Get-Credential -Message "Type the name and password of the local administrator account for WIN10."
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName WIN10 -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsDesktop -Offer Windows-10 -Skus RS3-Pro -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name WIN10-TestLab-OSDisk -DiskSizeInGB 128 -CreateOption FromImage
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

## <a name="phase-5-join-your-windows-10-computer-to-azure-ad"></a>5단계: Azure AD에 Windows 10 컴퓨터 가입

Windows 10 Enterprise가 있는 실제 또는 가상 머신을 만든 후에 로컬 관리자 계정으로 로그인합니다.
  
> [!NOTE]
> Azure의 가상 컴퓨터에 대해  [다음 지침](https://docs.microsoft.com/azure/virtual-machines/windows/connect-logon) 에 따라 연결 합니다.
  
다음으로, WIN10 컴퓨터를 Microsoft 365 E5 구독의 Azure AD 테넌트에 가입합니다.
  
1. WIN10 컴퓨터의 데스크톱에서 **시작 > 설정 > 계정을 사용 하 여 회사 또는 학교 > 연결 > 액세스**를 선택 합니다.
    
2. **회사 또는 학교 계정 설정** 대화 상자에서 **Azure Active Directory에이 장치 가입**을 선택 합니다.
    
3. **회사 또는 학교 계정**에 Microsoft 365 E5 구독의 전역 관리자 계정 이름을 입력 하 고 **다음**을 선택 합니다.
    
4. **암호 입력**에 전역 관리자 계정의 암호를 입력 하 고 **로그인**을 선택 합니다.
    
5. 조직이 조직 인지 확인 하는 메시지가 표시 되 면 **가입**을 선택한 다음 **완료**를 선택 합니다.
    
6. 설정 창을 닫습니다.
    
다음으로, WIN10 컴퓨터에 Microsoft 365 Apps for enterprise를 설치 합니다.
  
1. Microsoft Edge browser를 열고 전역 관리자 계정 자격 증명을 사용 하 여 [microsoft 365 관리 센터](https://admin.microsoft.com) 에 로그인 합니다.
    
2. **Microsoft Office 홈** 탭에서 **Office 설치**를 선택 합니다.
    
3. 수행할 작업을 묻는 메시지가 표시 되 면 **실행**을 선택한 다음 **사용자 계정 컨트롤**에 대해 **예** 를 선택 합니다.
    
4. Office 설치가 완료 될 때까지 기다립니다. **모든 설정이 완료**되 면 **닫기** 를 두 번 선택 합니다.
    
결과 환경은 다음과 같습니다.

![Microsoft 365 Enterprise 테스트 환경 5단계](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)

여기에는 다음과 같은 WIN10 컴퓨터가 포함됩니다.

- Microsoft 365 E5 구독의 Azure AD 테넌트에 가입했습니다.
- Microsoft Intune(EMS)에서 Azure AD 장치로 등록합니다.
- Microsoft 365 enterprise 용 앱이 설치 되어 있습니다.
  
이제 [엔터프라이즈 용 Microsoft 365](https://www.microsoft.com/microsoft-365/enterprise)의 추가 기능을 시험해 볼 준비가 되었습니다.
  
## <a name="next-steps"></a>다음 단계

다음과 같은 추가 테스트 랩 가이드 집합에 대해 알아봅니다.
  
- [ID](m365-enterprise-test-lab-guides.md#identity)
- [모바일 장치 관리](m365-enterprise-test-lab-guides.md#mobile-device-management)
- [정보 보호](m365-enterprise-test-lab-guides.md#information-protection)
   

## <a name="see-also"></a>참고 항목

[엔터프라이증용 Microsoft 365 테스트 랩 가이드](m365-enterprise-test-lab-guides.md)

[엔터프라이즈용 Microsoft 365 개요](microsoft-365-overview.md)

[엔터프라이즈 설명서에 대 한 Microsoft 365](https://docs.microsoft.com/microsoft-365-enterprise/)
