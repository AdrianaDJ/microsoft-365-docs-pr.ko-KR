---
title: 암호화 위험 및 보호
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom:
- seo-marvel-mar2020
description: 이 문서에서는 Office 365에 대 한 위험 및 보호에 사용할 수 있는 암호화 기술에 대해 알아봅니다.
ms.openlocfilehash: a9abf3dcc6cbd1bdb237c6ccecbbbaa4d42fda2b
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769188"
---
# <a name="encryption-risks-and-protections"></a>암호화 위험 및 보호

Microsoft는 Microsoft 365 서비스 및 고객 데이터에 대 한 위험을 중점적으로 설명 하는 제어 및 규정 준수 프레임 워크를 따릅니다. Microsoft는 이러한 위험을 완화 하기 위해 다양 한 기술과 프로세스 기반 방법 (컨트롤로 지칭 함)을 구현 합니다. 컨트롤을 통한 위험 식별, 평가 및 완화는 지속적인 프로세스입니다. 

기능, 네트워크, 서버, 응용 프로그램, 사용자 (예: Microsoft 관리자) 및 데이터와 같은 클라우드 서비스의 다양 한 계층 내에서 제어를 구현 하는 것은 심층 방어 전략을 형성 하는 것입니다. 이 전략의 핵심은 서로 다른 여러 컨트롤이 서로 다른 계층에서 구현 되어 동일 하거나 유사한 위험 시나리오를 방지 하는 것입니다. 이 여러 계층 방식에서는 특정 이유로 인해 컨트롤이 실패 하는 경우 유사시 대기 보호를 제공 합니다.

몇 가지 위험 시나리오와이를 완화 하는 현재 사용 가능한 암호화 기술은 다음과 같습니다. 이러한 시나리오는 Office 365에서 구현 된 다른 컨트롤을 통해 완화 되는 경우가 많은 경우에도 해당 됩니다.

| 암호화 기술 | 서비스 | 키 관리 | 위험 시나리오 | 값 |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitLocker | Exchange Online, SharePoint Online 및 비즈니스용 Skype | Microsoft | 디스크 또는 서버가 도난당 하거나 잘못 재생 되었습니다. | BitLocker는 도난당 하거나 잘못 재생 된 하드웨어 (서버/디스크)로 인 한 데이터 손실을 방지 하기 위한 유사시 대기 방식을 제공 합니다. |
| 서비스 암호화 | SharePoint Online, 비즈니스용 Skype 및 비즈니스용 OneDrive; Exchange Online (로드맵) | Microsoft | 내부 또는 외부 해커는 개별 파일/데이터에 blob로 액세스 하려고 합니다. | 키에 액세스 하지 않고 암호화 된 데이터의 암호를 해독할 수 없습니다. 해커의 데이터 액세스 위험을 완화 하는 데 도움이 됩니다. |
| 고객 키 | SharePoint Online, 비즈니스용 OneDrive, Exchange Online 및 비즈니스용 Skype | 고객 | N/A (이 기능은 준수 기능으로 디자인 되었으며, 위험에 대 한 완화로 설계 되지 않음) | 고객이 내부 규정 및 준수 의무를 충족 하 고 서비스를 종료 하 고 데이터에 대 한 Microsoft의 액세스를 해지할 수 있도록 지원 |
| Microsoft 365와 클라이언트 간의 TLS | Exchange Online, SharePoint Online, 비즈니스용 OneDrive, 비즈니스용 Skype, 팀 및 Yammer | Microsoft, 고객 | 인터넷을 통해 Microsoft 365와 클라이언트 컴퓨터 간의 데이터 흐름을 누르기 위한 중간자 또는 기타 공격입니다. | 이 구현에서는 microsoft와 고객 모두에 게 가치를 제공 하 고 Microsoft 365와 클라이언트 사이에 전송 되는 데이터 무결성을 보장 합니다. |
| Microsoft 데이터 센터 간의 TLS | Exchange Online, SharePoint Online, 비즈니스용 OneDrive 및 비즈니스용 Skype | Microsoft | 다른 Microsoft 데이터 센터에 있는 Microsoft 365 서버 간의 고객 데이터 흐름을 누르기 위한 사용자 중간 또는 기타 공격입니다. | 이 구현 방법은 Microsoft 데이터 센터 간의 공격 으로부터 데이터가 보호 되는 또 다른 방법입니다. |
| Azure 권한 관리 (Microsoft 365 또는 Azure Information Protection에 포함 됨) | Exchange Online, SharePoint Online 및 비즈니스용 OneDrive | 고객 | 데이터가 데이터에 대 한 액세스 권한이 없는 사용자에 게 전달 됩니다. | Azure Information Protection은 여러 장치에서 파일 및 전자 메일을 보호 하는 데 도움이 되는 암호화, id 및 권한 부여 정책을 통해 고객에 게 가치를 제공 하는 Azure RMS를 사용 합니다. Azure RMS는 특정 조건과 일치 하는 Microsoft 365에서 시작 되는 모든 전자 메일 (즉, 특정 주소에 전자 메일을 보낼 수 있음)이 다른 받는 사람에 게 전송 되기 전에 자동으로 암호화 되는 고객에 게 값을 제공 합니다. |
| S/MIME | Exchange Online | 고객 | 전자 메일이 의도 한 받는 사람이 아닌 사람의 손에 포함 됩니다. | S/MIME은 전자 메일을 직접 받는 사람이 보낸 전자 메일의 암호를 해독 하는 것을 허용 하 여 고객에 게 가치를 제공 합니다. |
| Office 365 메시지 암호화 | Exchange Online, SharePoint Online | 고객 | 보호 된 첨부 파일을 포함 하는 전자 메일은 Microsoft 365 내부 또는 외부에 있는 사람의 전자 메일 받는 사람이 아닌 사람에 게 전달 됩니다. | OME는 특정 조건과 일치 하는 Microsoft 365에서 시작 하는 모든 전자 메일 (즉, 특정 주소에 보내는 전자 메일)이 다른 내부 또는 외부 받는 사람에 게 전송 되기 전에 자동으로 암호화 되는 고객에 게이에 대 한 가치를 제공 합니다. |
| 파트너 조직과의 SMTP TLS | Exchange Online | 고객 | 전자 메일은 Microsoft 365 테 넌 트를 다른 파트너 조직으로 전송 하는 동안 중간자 또는 기타 공격을 통해 가로채도 됩니다. | 이 시나리오에서는 고객에 게 사용자가 암호화 된 SMTP 채널 내에서 Microsoft 365 테 넌 트와 해당 파트너의 전자 메일 조직 간의 모든 메일을 주고 받을 수 있는 가치를 제공 합니다. |

## <a name="encryption-technologies-available-in-multi-tenant-environments"></a>다중 테 넌 트 환경에서 사용할 수 있는 암호화 기술

| 암호화 기술 | 구현 방법 | 주요 교환 알고리즘 및 강도 | 키 관리 * | FIPS 140-2 유효성 검사 |
|----------------------------------------------------------------------------------|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| BitLocker | Exchange Online | AES 256 비트 | AES 외부 키는 안전한 보안 및 Exchange 서버의 레지스트리에 저장 됩니다. 안전한 보안 저장소는 높은 수준의 권한 상승 및 승인을 필요로 하 여 액세스 해야 합니다. Lockbox 라는 내부 도구를 사용 해야만 액세스를 요청 하 고 승인할 수 있습니다. AES 외부 키도 서버의 신뢰할 수 있는 플랫폼 모듈에 저장 됩니다. 48 자리 숫자 암호는 Active Directory에 저장 되 고 Lockbox로 보호 됩니다. | 예, AES 256 비트를 사용 하는 서버에 대해 |
|  | SharePoint Online | AES 256 비트 | AES 외부 키가 안전한 암호로 저장 됩니다. 안전한 보안 저장소는 높은 수준의 권한 상승 및 승인을 필요로 하 여 액세스 해야 합니다. Lockbox 라는 내부 도구를 사용 해야만 액세스를 요청 하 고 승인할 수 있습니다. AES 외부 키도 서버의 신뢰할 수 있는 플랫폼 모듈에 저장 됩니다. 48 자리 숫자 암호는 Active Directory에 저장 되 고 Lockbox로 보호 됩니다. | 예 |
|  | 비즈니스용 Skype | AES 256 비트 | AES 외부 키가 안전한 암호로 저장 됩니다. 안전한 보안 저장소는 높은 수준의 권한 상승 및 승인을 필요로 하 여 액세스 해야 합니다. Lockbox 라는 내부 도구를 사용 해야만 액세스를 요청 하 고 승인할 수 있습니다. AES 외부 키도 서버의 신뢰할 수 있는 플랫폼 모듈에 저장 됩니다. 48 자리 숫자 암호는 Active Directory에 저장 되 고 Lockbox로 보호 됩니다. | 예 |
| 서비스 암호화 | SharePoint Online | AES 256 비트 | Blob를 암호화 하는 데 사용 되는 키는 SharePoint Online 콘텐츠 데이터베이스에 저장 됩니다. SharePoint Online 콘텐츠 데이터베이스는 rest에서 데이터베이스 액세스 제어 및 암호화로 보호 됩니다. Azure SQL Database에서 TDE를 사용 하 여 암호화를 수행 합니다. 이러한 비밀은 테 넌 트 수준이 아니라 SharePoint Online의 서비스 수준에 있습니다. 이러한 비밀 (마스터 키 라고도 함)은 키 저장소 라는 별도의 보안 리포지토리에 저장 됩니다. TDE는 활성 데이터베이스와 데이터베이스 백업 및 트랜잭션 로그 모두에 대해 rest 보안을 제공 합니다. 고객이 선택적 키를 입력 하면 해당 고객 키가 Azure Key Vault에 저장 되 고, 서비스는이 키를 사용 하 여 사이트 키를 암호화 하는 데 사용 되는 테 넌 트 키를 암호화 한 다음 파일 수준 키를 암호화 하는 데 사용 됩니다. 기본적으로 고객은 키를 제공할 때 새 키 계층 구조가 도입 됩니다. | 예 |
|  | 비즈니스용 Skype | AES 256 비트 | 임의로 생성 된 서로 다른 256 비트 키를 사용 하 여 데이터의 각 부분을 암호화 합니다. 암호화 키는 각 회의 마스터 키로도 암호화 되는 해당 메타 데이터 XML 파일에 저장 됩니다. 또한 마스터 키는 전화 회의 당 한 번만 생성 됩니다. | 예 |
|  | Exchange Online | AES 256 비트 | 각 사서함은 Microsoft (로드맵) 또는 고객이 (고객 키를 사용 하는 경우)에서 제어 하는 암호화 키를 사용 하는 데이터 암호화 정책을 사용 하 여 암호화 됩니다. | 예 |
| Microsoft 365와 클라이언트/파트너 간의 TLS | Exchange Online | [여러 암호 그룹을 지 원하는 oplocks](https://technet.microsoft.com/library/mt163898.aspx) | Exchange Online에 대 한 TLS 인증서 (outlook.office.com)는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> Exchange Online에 대 한 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA1RSA 인증서입니다. | 예, 256 비트 암호화 강도의 TLS 1.2을 사용 하는 경우 |
|  | SharePoint Online | EAP-TLS 1.2 (AES 256) <br> <br> [비즈니스용 OneDrive 및 SharePoint Online에서의 데이터 암호화](https://technet.microsoft.com/library/dn905447.aspx) | SharePoint Online에 대 한 TLS 인증서 (* sharepoint.com)는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> SharePoint Online에 대 한 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA1RSA 인증서입니다. | 예 |
|  | 비즈니스용 Skype | [SIP 통신 및 PSOM 데이터 공유 세션에 대 한 TLS](https://support.office.com/article/Set-up-your-network-for-Skype-for-Business-Online-d21f89b0-3afc-432e-b735-036b2432fdbf) | 비즈니스용 Skype (* lync.com)에 대 한 TLS 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> 비즈니스용 Skype의 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. | 예 |
|  | Microsoft Teams | EAP-TLS 1.2 (AES 256) <br> <br> [Microsoft 팀에 대 한 질문과 대답-관리자 도움말](https://docs.microsoft.com/MicrosoftTeams/teams-overview) | Microsoft 팀에 대 한 TLS 인증서 (teams.microsoft.com, edge.skype.com)는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> Microsoft 팀의 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. | 예 |
| Microsoft 데이터 센터 간의 TLS | 모든 Microsoft 365 서비스 | EAP-TLS 1.2 (AES 256) <br> <br> 보안 실시간 전송 프로토콜 (SRTP) | Microsoft는 Microsoft 데이터 센터 간의 서버 간 통신을 위해 내부적으로 관리 되 고 배포 된 인증 기관을 사용 합니다. | 예 |
| Azure 권한 관리 (Microsoft 365 또는 Azure Information Protection에 포함 됨) | Exchange Online | 업데이트 및 향상 된 RMS 암호화 구현인 [암호화 모드 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10))를 지원 합니다. 서명 및 암호화를 위해 RSA 2048을 지원 하 고 시그니처의 해시로 사용 하는 경우에는 s h a-256입니다. | [Microsoft에서 관리](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)합니다. | 예 |
|  | SharePoint Online | 업데이트 및 향상 된 RMS 암호화 구현인 [암호화 모드 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10))를 지원 합니다. 서명 및 암호화를 위해 RSA 2048을 지원 하 고 서명을 위해 SHA-256을 사용 합니다. | [Microsoft에서 관리](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)(기본 설정) 사용자나 <br> <br> 사용자가 관리 하는 Microsoft 관리 키 대신 사용할 수 있습니다. IT 관리 Azure 구독이 있는 조직은 확인을 사용 하 여 추가 비용 없이 로그 사용을 기록할 수 있습니다. 자세한 내용은 [고유한 키 가져오기 구현](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)을 참조 하십시오. 이 구성에서는 nCipher Hsm을 사용 하 여 키를 보호 합니다. 자세한 내용은 [NCipher hsm And AZURE RMS](https://www.thales-esecurity.com/msrms/cloud)를 참조 하십시오. | 예 |
| S/MIME | Exchange Online | 암호화 메시지 구문 Standard 1.5 (PKCS #7) | 배포 된 고객 관리 공개 키 인프라에 따라 달라 집니다. 키 관리는 고객에 의해 수행 되며, Microsoft는 서명 및 암호 해독에 사용 되는 개인 키에 액세스할 수 없습니다. | 예, 3DES 또는 AES256를 사용 하 여 보내는 메시지를 암호화 하도록 구성 된 경우 |
| Office 365 메시지 암호화 | Exchange Online | Azure RMS와 동일 ([암호화 모드 2](https://technet.microsoft.com/library/dn569290.aspx) -서명 및 암호화를 위한 RSA 2048 및 서명에 대 한 SHA-256) | 은 암호화 인프라로 Azure Information Protection을 사용 합니다. 사용되는 암호화 방식은 메시지 암호화 및 암호 해독에 사용되는 RMS 키를 얻은 위치에 따라 다릅니다. | 예 |
| 파트너 조직과의 SMTP TLS | Exchange Online | EAP-TLS 1.2 (AES 256) | Exchange Online에 대 한 TLS 인증서 (outlook.office.com)는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> Exchange Online에 대 한 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA1RSA 인증서입니다. | 예, 256 비트 암호화 강도의 TLS 1.2을 사용 하는 경우 |

**이 표에서 참조 하는 TLS 인증서는 US 데이터 센터에 대 한 것입니다. 미국 외 데이터 센터는 2048 비트 SHA256RSA 인증서도 사용 합니다.*

***Exchange Online 다중 테 넌 트 환경에 있는 대부분의 서버는 BitLocker에 대해 AES 256 비트 암호화를 사용 하 여 배포 되었습니다. AES 128 비트를 사용 하는 서버는 단계적으로 처리 됩니다.*

## <a name="encryption-technologies-available-in-government-cloud-community-environments"></a>정부 클라우드 커뮤니티 환경에서 사용할 수 있는 암호화 기술

| 암호화 기술 | 구현 방법 | 주요 교환 알고리즘 및 강도 | 키 관리 * | FIPS 140-2 유효성 검사 |
|---------------------------------------------|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| BitLocker | Exchange Online | AES 256 비트 | AES 외부 키는 안전한 보안 및 Exchange 서버의 레지스트리에 저장 됩니다. 안전한 보안 저장소는 높은 수준의 권한 상승 및 승인을 필요로 하 여 액세스 해야 합니다. Lockbox 라는 내부 도구를 사용 해야만 액세스를 요청 하 고 승인할 수 있습니다. AES 외부 키도 서버의 신뢰할 수 있는 플랫폼 모듈에 저장 됩니다. 48 자리 숫자 암호는 Active Directory에 저장 되 고 Lockbox로 보호 됩니다. | 예 |
|  | SharePoint Online | AES 256 비트 | AES 외부 키가 안전한 암호로 저장 됩니다. 안전한 보안 저장소는 높은 수준의 권한 상승 및 승인을 필요로 하 여 액세스 해야 합니다. Lockbox 라는 내부 도구를 사용 해야만 액세스를 요청 하 고 승인할 수 있습니다. AES 외부 키도 서버의 신뢰할 수 있는 플랫폼 모듈에 저장 됩니다. 48 자리 숫자 암호는 Active Directory에 저장 되 고 Lockbox로 보호 됩니다. | 예 |
|  | 비즈니스용 Skype | AES 256 비트 | AES 외부 키가 안전한 암호로 저장 됩니다. 안전한 보안 저장소는 높은 수준의 권한 상승 및 승인을 필요로 하 여 액세스 해야 합니다. Lockbox 라는 내부 도구를 사용 해야만 액세스를 요청 하 고 승인할 수 있습니다. AES 외부 키도 서버의 신뢰할 수 있는 플랫폼 모듈에 저장 됩니다. 48 자리 숫자 암호는 Active Directory에 저장 되 고 Lockbox로 보호 됩니다. | 예 |
| 서비스 암호화 | SharePoint Online | AES 256 비트 | Blob를 암호화 하는 데 사용 되는 키는 SharePoint Online 콘텐츠 데이터베이스에 저장 됩니다. SharePoint Online 콘텐츠 데이터베이스는 rest에서 데이터베이스 액세스 제어 및 암호화로 보호 됩니다. Azure SQL Database에서 TDE를 사용 하 여 암호화를 수행 합니다. 이러한 비밀은 테 넌 트 수준이 아니라 SharePoint Online의 서비스 수준에 있습니다. 이러한 비밀 (마스터 키 라고도 함)은 키 저장소 라는 별도의 보안 리포지토리에 저장 됩니다. TDE는 활성 데이터베이스와 데이터베이스 백업 및 트랜잭션 로그 모두에 대해 rest 보안을 제공 합니다. 고객이 선택적 키를 입력 하면 해당 고객 키가 Azure Key Vault에 저장 되 고, 서비스는이 키를 사용 하 여 사이트 키를 암호화 하는 데 사용 되는 테 넌 트 키를 암호화 한 다음 파일 수준 키를 암호화 하는 데 사용 됩니다. 기본적으로 고객은 키를 제공할 때 새 키 계층 구조가 도입 됩니다. | 예 |
|  | 비즈니스용 Skype | AES 256 비트 | 임의로 생성 된 서로 다른 256 비트 키를 사용 하 여 데이터의 각 부분을 암호화 합니다. 암호화 키는 각 회의 마스터 키로도 암호화 되는 해당 메타 데이터 XML 파일에 저장 됩니다. 또한 마스터 키는 전화 회의 당 한 번만 생성 됩니다. | 예 |
|  | Exchange Online | AES 256 비트 | 각 사서함은 Microsoft 또는 고객이 제어 하는 암호화 키 (고객 키가 사용 되는 경우)를 사용 하는 데이터 암호화 정책을 사용 하 여 암호화 됩니다. | 예 |
| Microsoft 365와 클라이언트/파트너 간의 TLS | Exchange Online | [여러 암호 그룹을 지 원하는 oplocks](https://technet.microsoft.com/library/mt163898.aspx) | Exchange Online에 대 한 TLS 인증서 (outlook.office.com)는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> Exchange Online에 대 한 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA1RSA 인증서입니다. | 예, 256 비트 암호화 강도의 TLS 1.2을 사용 하는 경우 |
|  | SharePoint Online | EAP-TLS 1.2 (AES 256) | SharePoint Online에 대 한 TLS 인증서 (* sharepoint.com)는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> SharePoint Online에 대 한 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA1RSA 인증서입니다. | 예 |
|  | 비즈니스용 Skype | SIP 통신 및 PSOM 데이터 공유 세션에 대 한 TLS | 비즈니스용 Skype (* lync.com)에 대 한 TLS 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> 비즈니스용 Skype의 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. | 예 |
|  | Microsoft Teams | [Microsoft 팀에 대 한 질문과 대답-관리자 도움말](https://docs.microsoft.com/MicrosoftTeams/teams-overview) | Microsoft 팀에 대 한 TLS 인증서 (teams.microsoft.com; edge.skype.com)는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> Microsoft 팀의 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. | 예 |
| Microsoft 데이터 센터 간의 TLS | Exchange Online, SharePoint Online, 비즈니스용 Skype | EAP-TLS 1.2 (AES 256) | Microsoft는 Microsoft 데이터 센터 간의 서버 간 통신을 위해 내부적으로 관리 되 고 배포 된 인증 기관을 사용 합니다. | 예 |
|  |  | 보안 실시간 전송 프로토콜 (SRTP) |  |  |
| Azure 권한 관리 서비스 | Exchange Online | 업데이트 및 향상 된 RMS 암호화 구현인 [암호화 모드 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10))를 지원 합니다. 서명 및 암호화를 위해 RSA 2048을 지원 하 고 시그니처의 해시로 사용 하는 경우에는 s h a-256입니다. | [Microsoft에서 관리](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)합니다. | 예 |
|  | SharePoint Online | 업데이트 및 향상 된 RMS 암호화 구현인 [암호화 모드 2](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/hh867439(v=ws.10))를 지원 합니다. 서명 및 암호화를 위해 RSA 2048을 지원 하 고 시그니처의 해시로 사용 하는 경우에는 s h a-256입니다. | [Microsoft에서 관리](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)(기본 설정) 사용자나 <br> <br> 고객 관리 (BYOK 라고도 함)-Microsoft 관리 키 대신 사용할 수 있습니다. IT 관리 Azure 구독이 있는 조직은 확인을 사용 하 여 추가 비용 없이 로그 사용을 기록할 수 있습니다. 자세한 내용은 [고유한 키 가져오기 구현](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key)을 참조 하십시오. <br> <br> BYOK 시나리오에서는 nCipher Hsm을 사용 하 여 키를 보호 합니다. 자세한 내용은 [NCipher hsm And AZURE RMS](https://www.thales-esecurity.com/msrms/cloud)를 참조 하십시오. | 예 |
| S/MIME | Exchange Online | 암호화 메시지 구문 Standard 1.5 (PKCS #7) | 배포 된 공개 키 인프라에 따라 달라 집니다. | 예, 3DES 또는 AES-256을 사용 하 여 보내는 메시지를 암호화 하도록 구성 된 경우 |
| Office 365 메시지 암호화 | Exchange Online | Azure RMS와 동일 ([암호화 모드 2](https://technet.microsoft.com/library/dn569290.aspx) -서명 및 암호화를 위한 RSA 2048, 시그니처의 해시에 대 한 SHA-256) | 은 Azure RMS를 암호화 인프라로 사용 합니다. 사용되는 암호화 방식은 메시지 암호화 및 암호 해독에 사용되는 RMS 키를 얻은 위치에 따라 다릅니다. <br> <br> Microsoft Azure RMS를 사용 하 여 키를 가져오는 경우 암호화 모드 2가 사용 됩니다. AD (Active Directory) RMS를 사용 하 여 키를 가져오는 경우 암호화 모드 1 또는 암호화 모드 2가 사용 됩니다. 사용 되는 방법은 온-프레미스 AD RMS 배포에 따라 다릅니다. 암호화 모드 1은 원본 AD RMS 암호화 구현입니다. 서명 및 암호화를 위해 RSA 1024를 지원 하 고 서명에 대해 s h a-1을 지원 합니다. 이 모드는 Hsm을 사용 하는 BYOK 구성을 제외 하 고 모든 현재 버전의 RMS에서 계속 지원 됩니다. | 예 |
| 파트너 조직과의 SMTP TLS | Exchange Online | EAP-TLS 1.2 (AES 256) | Exchange Online에 대 한 TLS 인증서 (outlook.office.com)는 Baltimore CyberTrust Root에서 발급 한 2048 비트 SHA256RSA 인증서입니다. <br> <br> Exchange Online에 대 한 TLS 루트 인증서는 Baltimore CyberTrust Root에서 발급 한 2048 비트 sha1RSA 인증서입니다. <br> <br> 보안상의 이유로 인증서는 시간에 따라 변경 됩니다. | 예 |

**이 표에서 참조 하는 TLS 인증서는 US 데이터 센터에 대 한 것입니다. 미국 외 데이터 센터는 2048 비트 SHA256RSA 인증서도 사용 합니다.*
