---
title: Microsoft 365 및 Office 365 서비스용 설정 가이드
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- M365-subscription-management
- SPO_Content
- m365initiative-coredeploy
f1.keywords:
- CSH
ms.custom: Adm_O365_Setup
search.appverid:
- MET150
- MET150
- BCS160
ms.assetid: 165f46e8-3533-4d76-be57-97f81ebd40f2
description: 설치 가이드를 사용 하 여 Microsoft 365 또는 Office 365의 계획 및 구성을 가속화 합니다.
ms.openlocfilehash: 7024494de231e5adcce4bb91414b5f7bb3349f88
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48844095"
---
# <a name="setup-guides-for-microsoft-365-and-office-365-services"></a>Microsoft 365 및 Office 365 서비스용 설정 가이드

Microsoft 365 및 Office 365 설치 가이드에는 테 넌 트, 앱 및 서비스를 계획 하 고 배포 하기 위한 맞춤형 지침 및 리소스가 제공 됩니다. 이러한 가이드는 [microsoft 365 FastTrack](https://www.microsoft.com/fasttrack/microsoft-365) 온 보 딩 전문가가 개별 상호 작용에 공유 하는 것과 동일한 모범 사례를 사용 하 여 작성 되었으며 microsoft 365 관리 센터 내의 모든 관리자가 사용할 수 있습니다. 제품 설정에 대 한 정보를 제공 하 고, 보안 기능을 사용 하며, 공동 작업 도구를 배포 하 고, 고급 배포 속도를 향상 하기 위한 스크립트를 제공

## <a name="how-to-access-setup-guides-in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서 설치 가이드에 액세스 하는 방법

설치 가이드는 Microsoft 365 관리 센터의 [설치 지침](https://aka.ms/setupguidance) 페이지에서 액세스할 수 있습니다. 진행 상황을 추적 하 고 언제 든 지 안내선을 완성할 수 있습니다. **설치 지침** 페이지에 연결 하려면 다음을 수행 합니다.

1. [Microsoft 365 관리 센터](https://admin.microsoft.com/)에서 **홈** 페이지로 이동 합니다.

2. **교육 & 가이드** 카드를 찾습니다. 

   ![Microsoft 365 관리 센터의 가이드 카드 & 교육](../media/setup-guides-for-microsoft-365/adminportal-trainingandguides.png)

3. **사용자 지정 설치 지침** 을 선택 합니다.

   ![Microsoft 365 관리 센터의 설치 지침 페이지 스크린샷](../media/setup-guides-for-microsoft-365/adminportal-setupguidance.png)

>[!NOTE]
>Microsoft 365 관리 센터에 액세스 하려면 테 넌 트 관리자 권한이 필요 합니다.

## <a name="how-do-setup-guides-work-in-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서 설정 가이드는 어떻게 작동 하나요?

각 가이드에서는 구성을 변경 하는 데 사용할 수 있는 스크립트, 리소스, 문서 및 필요에 따라 단계별 지침을 제공 합니다. 이러한 가이드에서는 중소 조직과 대규모 조직의 특정 요구를 반영 하는 선택 항목을 제공 합니다. 또한 지침에는 신규 및 숙련 된 관리자 모두에 대 한 지원이 포함 됩니다.

![설정 가이드의 예](../media/setup-guides-for-microsoft-365/m365-setupguide-example.png)

가이드를 사용 하 여 계획 단계 중, 배포 및 롤아웃 중에 특정 Microsoft 365 및 Office 365 기능에 대해 자세히 알아보고, 설정을 수정 하기 위한 배포를 완료 한 후에 해당 정보를 다시 검토 합니다.

## <a name="guides-for-initial-setup"></a>초기 설정 가이드

### <a name="prepare-your-environment"></a>작업 환경 준비

[환경 준비](https://aka.ms/prepareyourenvironment) 가이드에서는 Microsoft 365 및 Office 365 서비스에 대 한 조직의 환경을 준비 하는 데 도움이 되는 정보를 제공 합니다. 목표에 관계 없이 성공적인 배포를 위해 완료 해야 하는 작업이 있습니다. 환경을 준비 하는 동안 오류가 발생 하지 않도록 하려면 도메인을 연결 하 고, 사용자를 추가 하 고, 라이선스를 할당 하 고, Exchange Online을 사용 하 여 전자 메일을 설정 하 고, Office 앱을 설치 또는 배포 하는 단계별 지침을 제공 합니다. 

### <a name="email-setup-advisor"></a>전자 메일 설정 도우미

[전자 메일 설정 관리자](https://aka.ms/office365setup) 는 조직에 대해 Exchange Online을 구성 하는 데 필요한 단계별 지침을 제공 합니다. 여기에는 새 전자 메일 계정 설정, 전자 메일 마이그레이션, 전자 메일 보호 구성 등이 포함 됩니다. 전자 메일을 설정 하려면이 관리자를 사용 하 여 조직의 현재 메일 시스템, 마이그레이션되는 사서함 수, 사용자 및 해당 액세스를 관리 하는 방법에 따라 권장 되는 마이그레이션 방법을 수신 합니다.

### <a name="gmail-contacts-and-calendar-advisor"></a>Gmail 연락처 및 일정 도우미

Gmail 사용자의 사서함을 Microsoft 365로 마이그레이션하는 경우 전자 메일 메시지가 마이그레이션되고 연락처 및 일정 항목은 마이그레이션되지 않습니다. [Gmail 연락처 및 일정 관리자](https://aka.ms/gmailcontactscalendar) 는 Outlook.com, Outlook 클라이언트 또는 PowerShell과 함께 import 및 export 메서드를 사용 하 여 google 연락처 및 google 일정 항목을 Microsoft 365로 가져오는 단계를 제공 합니다.

### <a name="microsoft-365-deployment-advisor"></a>Microsoft 365 배포 관리자

[Microsoft 365 배포 관리자](https://aka.ms/microsoft365setupguide) 는 생산성 도구, 보안 정책 및 장치 관리 기능을 설정할 때의 지침을 제공 합니다. Microsoft 365 Business Premium 또는 Microsoft 365 for enterprise 구독을 사용 하는 경우이 관리자를 통해 조직의 장치를 설정 하 고 구성할 수 있습니다. 

사용자는 클라우드 서비스를 사용 하도록 설정 하 고, 장치를 지원 되는 최신 버전의 Windows 10으로 업데이트 하 고, 장치를 Azure Active Directory (Azure AD)에 단일 중앙 위치에 가입 하기 위한 지침 및 리소스에 대 한 액세스 권한을 수신 합니다.


### <a name="remote-work-setup-guide"></a>원격 작업 설정 가이드

[원격 작업 설정 가이드](https://aka.ms/remoteworksetup) 에서는 사용자가 원격으로 작업을 수행 하 고, 데이터가 안전 하며, 사용자의 자격 증명을 safeguarded 수 있도록 하는 데 필요한 팁과 리소스가 조직에 제공 됩니다. 

원격 작업자의 장치 트래픽을 해당 클라우드의 Microsoft 365 리소스와 조직의 네트워크 둘 다에 최적화 하 여 원격 액세스 VPN 인프라에 대 한 부담을 줄일 수 있는 지침을 받을 수 있습니다. 

### <a name="windows-virtual-desktop-setup-guide"></a>Windows 가상 데스크톱 설정 가이드

Windows 가상 데스크톱은 클라우드에서 실행 되는 종합적인 데스크톱 및 앱 가상화 서비스입니다. 간소화 된 관리, 다중 세션 Windows 10, Microsoft 365 앱에 대 한 최적화 및 RDS (원격 데스크톱 서비스) 환경에 대 한 지원을 제공 하는 VDI (가상 데스크톱 인프라) 뿐입니다. 시간 (분)에 Windows 데스크톱 및 앱을 배포 및 확장 하 고 기본 제공 되는 보안 및 규정 준수 기능을 알아봅니다. 

[Windows Virtual Desktop 설정 가이드](https://aka.ms/wvdsetupguide) 에서는 관리자에 게 배포, 설치 지침 및 추가 리소스에 대 한 계획 리소스와 필수 구성 요소를 제공 합니다. 

### <a name="microsoft-edge-deployment-advisor"></a>Microsoft Edge 배포 관리자

Microsoft Edge는 세계 최고의 호환성과 성능, 관심 있는 보안 및 개인 정보 보호를 제공 하기 위해 처음부터 새로 재구축 되었으며, 웹을 최대한 활용 하도록 설계 되었습니다.

[Microsoft Edge 배포 관리자](https://aka.ms/edgeadvisor) 는 조직에서 액세스 하는 사이트를 확인 하도록 엔터프라이즈 사이트 검색을 구성 하 고, 중요 한 보안 기능을 검토 및 구성 하며, 조직의 요구 사항을 충족 하기 위해 개인 정보 취급 방침 및 추가 정책을 구성 하 고, 장치에서 웹 액세스를 관리 하는 데 도움을 줄 수 있습니다. Microsoft Edge를 개별 장치에 다운로드 하거나 구성 관리자 또는 Microsoft Intune을 사용 하 여 조직에서 여러 사용자에 게 배포 하는 방법을 확인할 수 있습니다.
Windows 가상 데스크톱은 클라우드에서 실행 되는 종합적인 데스크톱 및 앱 가상화 서비스입니다. 간소화 된 관리, 다중 세션 Windows 10, Microsoft 365 앱에 대 한 최적화 및 RDS (원격 데스크톱 서비스) 환경에 대 한 지원을 제공 하는 VDI (가상 데스크톱 인프라) 뿐입니다. 시간 (분)에 Windows 데스크톱 및 앱을 배포 및 확장 하 고 기본 제공 되는 보안 및 규정 준수 기능을 알아봅니다. 

### <a name="intune-configuration-manager-co-management-setup-guide"></a>Intune 구성 관리자 공동 관리 설정 가이드

기존 Configuration Manager 클라이언트 장치 및 조직에서 Microsoft Intune 및 Configuration Manager 둘 다로 공동 관리 하려는 새로운 인터넷 기반 장치에 대 한 [Intune Configuration manager 공동 관리 설치 가이드](https://aka.ms/comanagementsetup) 를 사용 합니다. 이 공동 관리 배포 가이드를 사용 하 여 Windows 10 장치를 관리 하 고 조직의 장치에 새로운 기능을 추가 하 여 두 솔루션의 이점을 모두 받을 수 있습니다.

## <a name="guides-for-authentication-and-access"></a>인증 및 액세스 가이드

### <a name="azure-ad-setup-guide"></a>Azure AD 설정 가이드

[AZURE AD 설정 가이드](https://aka.ms/aadpguidance) 에서는 조직이 강력한 보안 토대를 갖도록 하기 위한 정보를 제공 합니다. 이 가이드에서는 관리자를 위한 azure AD (역할 기반 액세스 제어), Azure FS (온-프레미스 디렉터리에 연결) 및 Azure AD Connect Health와 같은 초기 기능을 설정 하 여 자동화 된 동기화 중에 하이브리드 id의 상태를 모니터링할 수 있도록 합니다. 

또한 선택적인 고급 id 보호 및 사용자 프로비저닝 자동화를 포함 하 여 셀프 서비스 암호 재설정, 조건부 액세스 및 통합 타사 로그인을 사용 하는 방법에 대 한 필수 정보도 포함 되어 있습니다.

### <a name="sync-users-from-your-orgs-directory"></a>조직의 디렉터리에서 사용자 동기화

[Org 디렉터리 마법사에서 사용자 동기화](https://aka.ms/directorysyncsetup) 는 디렉터리 동기화를 설정 하는 과정을 안내 합니다. 이렇게 하면 간편 하 게 액세스 하 고 간편 하 게 관리할 수 있도록 온-프레미스 및 클라우드 id가 함께 제공 됩니다. Single sign-on, 셀프 서비스 옵션, 자동 계정 프로 비전, 조건부 액세스 제어 및 준수 정책 같은 새로운 기능을 사용할 때의 잠금을 해제 합니다. 이를 통해 사용자는 어디에서 나 필요한 리소스에 액세스할 수 있습니다.

### <a name="plan-your-passwordless-deployment"></a>Passwordless 배포 계획

다음과 같은 passwordless 인증 방법 중 하나를 사용 하 여 사용자가 자신의 장치에 안전 하 게 액세스할 수 있도록 하는 다른 로그인 방식으로 업그레이드 합니다. 

- 비즈니스용 Windows Hello
- Microsoft Authenticator 앱
- 보안 키 

[Passwordless less 배포 마법사](https://aka.ms/passwordlesssetup) 를 사용 하 여 사용할 최선의 passwordless 인증 방법을 검색 하 고 배포 방법에 대 한 지침을 받습니다. 

### <a name="plan-your-self-service-password-reset-sspr-deployment"></a>SSPR (셀프 서비스 암호 재설정) 배포 계획

사용자가 자신의 계정이 잠겨 있는 경우 암호를 개별적으로 변경 하거나 다시 설정할 수 있도록 하 고, 헬프데스크 엔지니어에 게 연락 하지 않고 암호를 잊어버린 경우 

사용자의 환경에 SSPR을 배포 하는 데 도움이 되도록 [셀프 서비스 암호 다시 설정 배포 마법사](https://aka.ms/SSPRSetupGuide) 에서 적절 한 Azure portal 옵션을 구성 하는 관련 문서와 지침을 확인할 수 있습니다.

### <a name="active-directory-federation-services-ad-fs-deployment-advisor"></a>AD FS (Active Directory Federation Services) 배포 관리자

[AD FS 배포 관리자](https://aka.ms/adfsguidance) 는 Microsoft 365 및 Office 365 서비스용 사용자를 인증 하는 온-프레미스 AD FS 인프라를 배포 하는 방법에 대 한 단계별 지침을 제공 합니다. 이 가이드를 사용 하 여 조직에서 AD FS 구성 요소와 요구 사항을 검토 하 고, 배포에 필요한 SSL 인증서를 취득 및 설치 하 고, 필요한 웹 응용 프로그램 프록시 서버를 설치할 수 있습니다. 

## <a name="guides-for-security-and-compliance"></a>보안 및 규정 준수 가이드

### <a name="microsoft-defender-for-endpoint-advisor"></a>끝점 관리자 용 Microsoft Defender

[Microsoft Defender For Endpoint advisor](https://aka.ms/mdatpsetup) 는 엔터프라이즈 네트워크에서 advanced threat를 차단, 감지, 조사 및 대응 하는 데 도움이 되는 지침을 제공 합니다. 조직의 취약성에 대 한 정보를 확인 하 고 가장 적합 한 배포 패키지 및 구성 방법을 결정 합니다. 

>[!NOTE]
>Microsoft 볼륨 라이선스는 Microsoft Defender for Endpoint에 필요 합니다.

### <a name="exchange-online-protection-setup-guide"></a>Exchange Online Protection 설정 가이드

Microsoft EOP (Exchange Online Protection)는 메시징 정책 위반 으로부터 조직을 보호 하는 기능을 사용 하 여 스팸 및 맬웨어에 대 한 보호를 위한 클라우드 기반 전자 메일 필터링 서비스입니다. 

[Exchange Online Protection 설정 가이드](https://aka.ms/EOPguidance) 를 사용 하 여 세 가지 배포 시나리오 온 &mdash; -프레미스 사서함, 하이브리드 (온-프레미스 및 클라우드) 사서함 또는 조직에 적합 한 모든 클라우드 사서함을 선택 하 여 EOP를 설정 합니다 &mdash; . 이 가이드에서는 사용자의 라이선스를 설정 및 검토 하 고, Microsoft 365 관리 센터에서 사용 권한을 할당 하 고, 보안 & 준수 센터에서 조직의 맬웨어 방지 및 스팸 정책을 구성할 수 있는 정보와 리소스를 제공 합니다. 

### <a name="microsoft-defender-for-office-365-advisor"></a>Microsoft Defender for Office 365 advisor

[Microsoft Defender For Office 365 advisor](https://aka.ms/oatpsetup) 는 환경에서 전자 메일 메시지, 링크 및 타사 공동 작업 도구를 통해 발생할 수 있는 악의적인 위협 으로부터 조직을 보호 합니다. 이 가이드에서는 조직의 요구 사항에 맞게 Office 용 Defender 365 계획을 준비 하 고 식별 하는 데 도움이 되는 리소스와 정보를 제공 합니다. 

### <a name="microsoft-information-protection-setup-guide"></a>Microsoft information protection 설정 가이드

중요 한 정보를 보호할 수 있도록 정보 보호 전략에 적용할 수 있는 기능에 대 한 개요를 확인 하세요. 중요 한 정보를 검색, 분류, 보호 및 모니터링 하는 4 단계 수명 주기 방식을 사용 합니다. [Microsoft information protection 설정 가이드](https://aka.ms/mipsetupguide) 에서는 이러한 각 단계를 완료 하기 위한 지침을 제공 합니다.

### <a name="microsoft-information-governance-setup-guide"></a>Microsoft 정보 거 버 넌 스 설정 가이드

[Microsoft Information 거 버 넌 스 설치 가이드](https://aka.ms/migsetupguide) 는 조직의 거 버 넌 스 전략을 설정 및 관리 하는 데 필요한 정보를 제공 하 여 사용자가 설정한 특정 수명 주기 지침에 따라 데이터를 분류 하 고 관리할 수 있도록 합니다. 이 가이드를 사용 하 여 조직에서 다시 사용할 수 있는 콘텐츠 및 준수 레코드에 적용 되는 레이블, 레이블 정책 및 보존 정책을 작성, 자동 적용 또는 게시 하는 방법에 대해 알아봅니다. 또한 대량 시나리오를 위한 파일 요금제로 CSV 파일을 가져오거나 개별 문서에 수동으로 적용 하기 위한 정보도 볼 수 있습니다. 

## <a name="guides-for-collaboration"></a>공동 작업용 가이드

### <a name="microsoft-365-apps-deployment-advisor"></a>Microsoft 365 Apps 배포 관리자

[Microsoft 365 Apps 배포 관리자](https://aka.ms/OPPquickstartguide) 는 Word, Excel, PowerPoint 및 OneNote와 같은 최신 버전의 Office 제품을 실행 하는 사용자의 장치를 제공 하는 데 도움을 줍니다. 관리 도구를 사용 하 여 엔터프라이즈 배포에 간편 하 게 설치할 수 있는 옵션이 포함 된 다양 한 배포 방법에 대 한 지침을 얻을 수 있습니다. 지침은 환경을 평가 하 고, 특정 배포 요구 사항을 파악 하 고, 필요한 지원 도구를 구현 하 여 성공적인 설치를 보장 하는 데 도움이 됩니다. 

### <a name="office-mobile-apps-setup-assistant"></a>Office 모바일 앱 설정 도우미

[Office 모바일 앱 설치 도우미](https://aka.ms/officeappguidance) 는 Windows, IOS 및 Android 모바일 장치에 office 앱을 다운로드 하 고 설치 하기 위한 지침을 제공 합니다. 이 가이드에서는 휴대폰 및 태블릿 장치에 Microsoft 365 및 Office 365 앱을 다운로드 하 고 설치 하는 단계별 정보를 제공 합니다.

### <a name="microsoft-teams-setup-guide"></a>Microsoft 팀 설정 가이드

[Microsoft 팀 설정 가이드](https://aka.ms/teamsguidance) 에서는 조직에서 팀과 개인 통신에 대 한 메시징, 통화, 오디오 또는 비디오 회의를 통해 실시간 대화를 호스트 하는 팀 작업 영역을 설정할 수 있는 지침을 제공 합니다. 팀 관리 센터 내에서 Network Planner 도구 및 팀 관리자를 사용 하 여 조직의 네트워크 요구 사항을 확인 하기 위한 지침을 받을 수 있습니다. 배포가 완료 되 면 팀을 사용 하 여 시작 하기 위한 유용한 리소스가 가이드에 포함 됩니다.

### <a name="sharepoint-setup-guide"></a>SharePoint 설정 가이드

[Sharepoint 설정 가이드](https://aka.ms/spoguidance) 에서는 sharepoint 문서 저장 및 콘텐츠 관리를 설정 하 고, 사이트를 만들고, 외부 공유를 구성 하 고, 데이터를 마이그레이션하고, 고급 설정을 구성 하 고, 조직 내에서 사용자 계약 및 통신을 구동 하는 데 도움이 됩니다. 콘텐츠 공유 권한 정책을 구성 하는 단계를 따르고, 마이그레이션 동기화 도구를 선택 하 고, SharePoint 환경에 대 한 보안 설정을 사용 하도록 설정 합니다. 

### <a name="onedrive-setup-guide"></a>OneDrive 설정 가이드

Onedrive [설정 가이드](https://aka.ms/ODfBquickstartguide) 를 사용 하 여 onedrive 파일 저장, 공유, 공동 작업 및 동기화 기능을 시작 합니다. OneDrive에서는 사용자가 Microsoft 365 앱 파일을 동기화 하 고, 외부 공유를 구성 하 고, 사용자 데이터를 마이그레이션하고, 고급 보안 및 장치 액세스 설정을 구성할 수 있는 중앙 위치를 제공 합니다. Onedrive 설정 가이드는 OneDrive 구독 또는 독립 실행형 OneDrive 계획을 사용 하 여 배포할 수 있습니다. 

### <a name="yammer-deployment-advisor"></a>Yammer 배포 관리자

Yammer를 사용 하 여 조직 전체에 연결 하 고 참여 합니다. [Yammer 배포 관리자](https://aka.ms/yammerdeploymentguide) 는 도메인을 추가 하 고 관리자를 정의 하 고 yammer 네트워크를 결합 하 여 yammer 네트워크를 준비 합니다. Yammer를 배포 하 고, 디자인을 사용자 지정 하 고, 보안 및 규정 준수를 구성 하 고, 설정을 구체화 하기 위한 지침을 볼 수 있습니다.

## <a name="advanced-wizards"></a>고급 마법사

### <a name="in-place-upgrade-with-configuration-manager"></a>구성 관리자를 사용한 전체 업그레이드

Windows 7 및 Windows 8.1 장치를 최신 버전의 Windows 10으로 업그레이드 하는 경우 [Configuration Manager를 사용 하 여 전체 업그레이드 가이드](https://aka.ms/win10upgradedemo) 를 사용 합니다. 제공 된 스크립트를 사용 하 여 필수 구성 요소를 확인 하 고 전체 업그레이드를 자동으로 구성 합니다.

### <a name="deploy-office-to-your-users"></a>사용자에 게 Office 배포

Office 배포 도구를 사용 하 여 설치를 사용자 지정 하는 기능을 사용 하 여 클라우드에서 Office 앱을 배포 합니다. [사용자에 게 Office 배포 가이드](https://aka.ms/proplusodt) 에서는 고급 설정을 사용 하 여 사용자 지정 된 Office 구성을 만들거나 미리 작성 된 권장 구성을 사용할 수 있습니다. 사용자가 자동 설치를 수행 하 고 있거나 사용자에 게 개별적으로 또는 대량으로 배포 하 고 있는지 여부에 관계 없이이 고급 마법사는 사용자에 게 조직에 맞게 구성 된 Office 설치를 제공 하는 단계별 지침을 제공 합니다.

### <a name="deploy-office-to-remote-users"></a>원격 사용자에 게 Office 배포

원격으로 작업 하는 것은 정상 이기 때문에 사용자가 내부 네트워크에 연결 되어 있지 않거나 자체 장치를 사용할 때 조직의 Office 설정을 받아야 합니다. 

[Office to 원격 사용자 가이드](https://aka.ms/officeremoteinstall) 를 사용 하 여 사용자 지정 된 office 설치를 만든 다음 사용자에 게 구성 하 여 office를 원활 하 게 설치 하는 데 사용할 수 있는 생성 된 PowerShell 스크립트를 보냅니다.

### <a name="deploy-and-update-microsoft-365-apps-with-configuration-manager"></a>Configuration Manager를 사용 하 여 Microsoft 365 앱 배포 및 업데이트

Configuration Manager를 사용 하는 조직의 경우 configure [and Update microsoft 365 Apps With Configuration manager advisor](https://aka.ms/oppinstall) 를 사용 하 여 fasttrack 엔지니어가 권장 하는 모범 사례를 사용 하 여 Microsoft 365 앱 배포를 자동으로 구성 하는 스크립트를 생성할 수 있습니다. 이 가이드를 사용 하 여 배포 그룹을 작성 하 고, Office 앱 및 기능을 사용자 지정 하 고, 동적 또는 간결한 설치를 구성한 다음 스크립트를 실행 하 여 배포를 대상으로 하는 데 필요한 응용 프로그램, 자동 배포 규칙 및 장치 모음을 만들 수 있습니다. 
