---
title: 보안 강화를 위해 Microsoft 365 테 넌 트 구성
f1.keywords:
- NOCSH
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/11/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid: MET150
ms.assetid: 8d274fe3-db51-4107-ba64-865e7155b355
ms.custom:
- seo-marvel-apr2020
description: 이 항목에서는 Microsoft 365 환경의 보안에 영향을 주는 테 넌 트 수준 설정에 대 한 권장 구성을 안내 합니다.
ms.openlocfilehash: cc1f69663badaa7ae6590bb1d389cb15f13da79d
ms.sourcegitcommit: 474bd6a86c3692d11fb2c454591c89029ac5bbd5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/19/2020
ms.locfileid: "49357542"
---
# <a name="configure-your-microsoft-365-tenant-for-increased-security"></a>보안 강화를 위해 Microsoft 365 테 넌 트 구성

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


이 항목에서는 Microsoft 365 환경의 보안에 영향을 주는 테 넌 트 수준 설정에 대 한 권장 구성을 안내 합니다. 보안 요구 사항에 따라 보안이 더 나 덜 필요할 수 있습니다. 이 권장 사항을 출발점으로 사용 합니다.

## <a name="check-office-365-secure-score"></a>Office 365 보안 점수 확인

Office 365 안전한 점수는 정기 활동 및 보안 설정에 따라 조직의 보안을 분석 하 고 점수를 할당 합니다. 먼저 현재 점수를 기록 합니다. 일부 테 넌 트 수준 설정을 조정 하면 점수가 증가 합니다. 목표는 최대 점수를 얻는 것이 아니라 사용자의 생산성에 부정적인 영향을 주지 않는 환경을 보호 하기 위한 기회를 확보 하기 위한 것입니다. [Microsoft 보안 점수](../mtp/microsoft-secure-score.md)를 참조 하세요.

## <a name="tune-threat-management-policies-in-the-microsoft-365-security-center"></a>Microsoft 365 보안 센터에서 위협 관리 정책 조정

Microsoft 365 보안 센터에는 환경을 보호 하는 기능이 포함 되어 있습니다. 또한 작업을 모니터링 하 고 수행 하는 데 사용할 수 있는 보고서 및 대시보드가 포함 되어 있습니다. 일부 영역에는 기본 정책 구성이 제공 됩니다. 일부 영역에는 기본 정책이 나 규칙이 포함 되지 않습니다. 위협 관리에서 이러한 정책을 방문 하 여 보다 안전한 환경에 대 한 위협 관리 설정을 조정 합니다.

****

|영역|기본 정책 포함|권장 사항|
|---|---|---|
|**피싱 방지**|예|사용자 지정 도메인이 있는 경우 기본 피싱 방지 정책을 구성 하 여 CEO와 같은 가장 귀중 한 사용자의 전자 메일 계정을 보호 하 고 도메인을 보호 합니다. <p> [Office 365에서 피싱 방지](set-up-anti-phishing-policies.md) 정책을 검토 하 고 [EOP에서 피싱 방지 정책 구성을](configure-anti-phishing-policies-eop.md) 참조 하거나 [Microsoft Defender for Office 365에서](configure-atp-anti-phishing-policies.md)피싱 방지 정책을 구성 합니다.|
|**맬웨어 방지 엔진**|예| 기본 정책을 편집 합니다. <ul><li>일반 첨부 파일 유형 필터: 선택</li></ul> <p> 사용자 지정 맬웨어 필터 정책을 만들어 조직의 지정 된 사용자, 그룹 또는 도메인에 적용할 수도 있습니다. <p> 추가 정보: <ul><li>[맬웨어 방지 보호 기능](anti-malware-protection.md)</li><li>[맬웨어 방지 정책 구성](configure-anti-malware-policies.md)</li></ul>|
|**Microsoft Defender for Office 365의 안전한 첨부 파일**|아니요|안전한 첨부 파일의 기본 페이지에서 **전역 설정을** 클릭 하 고이 설정을 켭니다. <ul><li>**SharePoint, OneDrive 및 Microsoft Teams의 ATP 켜기**</li></ul> <p> 다음 설정을 사용 하 여 안전 첨부 파일 정책을 만듭니다. <ul><li> **Block**: 알 수 없는 맬웨어 응답으로 **차단을** 선택 합니다.</li><li>**리디렉션 사용**:이 확인란을 선택 하 고 관리자 또는 격리 계정과 같은 전자 메일 주소를 입력 합니다.</li><li>**첨부 파일에 대 한 맬웨어 검사 시간이 초과 되거나 오류가 발생 하는 경우 위의 선택 사항을 적용** 합니다.</li><li>**_적용 대상_*: **받는 사람 도메인이** \> 도메인을 선택 합니다.</li></ul> <p> 추가 정보: [SharePoint, OneDrive 및 Microsoft 팀의 ATP](atp-for-spo-odb-and-teams.md) 및 [안전한 첨부 파일 정책 설정](set-up-atp-safe-attachments-policies.md)|
|**Microsoft Defender for Office 365의 안전한 링크**|예|안전한 링크의 기본 페이지에서 **전역 설정을** 클릭 합니다. <ul><li>**에서 안전한 링크 사용: Office 365 응용 프로그램**:이 설정이 설정 되어 있는지 확인 합니다.</li><li>**사용자가 안전 링크를 클릭 하는 경우 추적 안 함**:이 설정을 해제 하 여 사용자 클릭을 추적 합니다.</li></ul> <p> 다음 설정을 사용 하 여 안전 링크 정책을 만듭니다. <ul><li>**메시지에서 알 수 없는 잠재적 악성 url에 대 한 작업 선택**:이 설정이 **켜져** 있는지 확인 합니다.</li><li>**Microsoft 팀 내에서 알 수 없거나 잠재적 악성 url에 대 한 작업 선택**:이 **설정이 설정 되어 있는지 확인 합니다.**</li><li>**의심 스러운 링크 및 파일을 가리키는 링크에 대해 실시간 URL 검사 적용**:이 확인란을 선택 합니다.</li><li>**메시지를 배달 하기 전에 URL 검색이 완료 될 때까지 기다렸다가** 이 확인란을 선택 합니다.</li><li>**조직 내에서 전송 된 전자 메일 메시지에 안전한 링크 적용**:이 확인란을 선택 합니다.</li><li>**사용자가 원래 URL까지 클릭할 수 없도록 함**:이 확인란을 선택 합니다.</li><li>**적용 대상**: **받는 사람 도메인이** \> 도메인을 선택 합니다.</li></ul> <p> 추가 정보: [안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)|
|**스팸 방지 (메일 필터링)**|예| 시청할 대상: <ul><li>스팸 너무 많은 경우 — 사용자 지정 설정을 선택 하 고 기본 스팸 필터 정책을 편집 합니다.</li><li>스푸핑 인텔리전스-도메인 스푸핑 중인 보낸 사람을 검토 합니다. 이 보낸 사람을 차단 하거나 허용 합니다.</li></ul> <p> 추가 정보: [Microsoft 365 전자 메일로 스팸 방지 보호](anti-spam-protection.md)기능을 사용 합니다.|
|**_전자 메일 인증_* _|예|전자 메일 인증에서는 DNS (Domain Name System)를 사용 하 여 전자 메일을 보낸 사람에 대 한 전자 메일 메시지에 안정형 정보를 추가 합니다. Microsoft 365은 기본 도메인 (onmicrosoft.com)에 대해 전자 메일 인증을 설정 하지만 Microsoft 365 관리자는 사용자 지정 도메인에 대해 전자 메일 인증을 사용할 수도 있습니다. 다음과 같은 세 가지 인증 방법이 사용 됩니다. <ul><li>또는 SPF (보낸 사람 정책 프레임 워크)</li><ul><li>설치 시 [스푸핑을 방지 하려면 Microsoft 365에서 SPF를 설정](set-up-spf-in-office-365-to-help-prevent-spoofing.md)합니다 .를 참조 하세요.</li></ul> <li>DomainKeys 확인 메일 (DKIM)</li><ul><li>[사용자 지정 도메인에서 전송 되는 아웃 바운드 전자 메일의 유효성 검사를 보려면 DKIM을 사용](use-dkim-to-validate-outbound-email.md)합니다.</li><li>DKIM을 구성한 후에는 보안 센터에서 사용 하도록 설정 합니다.</li></ul><li>도메인 기반 메시지 인증, 보고 및 적합성 (DMARC)</li><ul><li>DMARC 설치의 경우 [DMARC를 사용 하 여 Microsoft 365에서 전자 메일의 유효성을 검사](use-dmarc-to-validate-email.md)합니다.</li></ul></ul>|
|

> [!NOTE]
> SPF, 하이브리드 배포 및 문제 해결을 위한 비표준 배포의 경우 [Microsoft 365에서 SPF (Sender Policy Framework)를 사용 하 여 스푸핑을 방지 하는 방법](how-office-365-uses-spf-to-prevent-spoofing.md)입니다.

## <a name="view-dashboards-and-reports-in-the-security-and-compliance-centers"></a>보안 및 준수 센터에서 대시보드 및 보고서 보기

다음 보고서 및 대시보드를 방문 하 여 환경의 상태에 대해 자세히 알아보세요. 조직에서 Office 365 서비스를 사용 하는 동안 이러한 보고서의 데이터는 더 풍부 하 게 됩니다. 지금은 모니터링 하 고 조치를 취할 수 있는 기능에 대해 익숙해져야 합니다. 자세한 내용은 [Microsoft 365 보안 및 준수 센터의 보고서](../../compliance/reports-in-security-and-compliance.md)를 참조 하세요.

_***

|대시보드|설명|
|---|---|
|[위협 관리 대시보드](security-dashboard.md)|보안 센터의 **threat management** 섹션에서이 대시보드를 사용 하 여 이미 처리 된 위협을 확인 하 고, 비즈니스 보안을 위해 이미 수행 된 위협 조사 및 응답 기능에 대 한 편리한 도구로 비즈니스 의사 결정권자에 게 보고 합니다.|
|[위협 탐색기 (또는 실시간 검출)](threat-explorer.md)|이는 보안 센터의 **위협 관리** 섹션에도 있습니다. 테 넌 트에 대 한 공격을 조사 하거나 발생 하는 경우 Explorer (또는 실시간 검색)를 사용 하 여 위협을 분석 합니다. Explorer 및 실시간 검색 보고서에는 시간에 따른 공격 량이 표시 되며 위협 계열, 침입자 인프라 등을 통해이 데이터를 분석할 수 있습니다. 인시던트 목록에 대해 의심 스러운 전자 메일을 표시할 수도 있습니다.|
|보고서-대시보드|보안 센터의 **Reports (보고서** ) 섹션에서 SharePoint Online 및 Exchange Online 조직에 대 한 감사 보고서를 봅니다. **보고서 보기** 페이지에서 azure Ad (Active Directory) 사용자 로그인 보고서, 사용자 활동 보고서 및 azure ad audit 로그에 액세스할 수도 있습니다.|
|

![보안 센터 대시보드](../../media/870ab776-36d2-49c7-b615-93b2bc42fce5.png)

## <a name="configure-additional-exchange-online-tenant-wide-settings"></a>추가 Exchange Online 테 넌 트 수준 설정 구성

Exchange 관리 센터의 보안 및 보호를 위한 대부분의 컨트롤은 보안 센터에도 포함 되어 있습니다. 두 위치에서 모두 구성 하지 않아도 됩니다. 다음은 권장 되는 몇 가지 추가 설정입니다.

****

|영역|기본 정책 포함|권장 사항|
|---|---|---|
|**메일 흐름** (전송 규칙이 라고도 함)|아니요|매크로가 포함 된 Office 파일 형식이 나 실행 파일 형식을 차단 하 여 랜 섬 웨어를 보호할 수 있는 메일 흐름 규칙을 추가 합니다. 자세한 내용은 [메일 흐름 규칙을 사용 하 여 Exchange Online의 메시지 첨부 파일 검사](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments)를 참조 하세요. <p> 다음 추가 항목을 참조 하세요. <ul><li>[랜섬웨어로부터 보호](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/secure-your-business-data#ransomware)</li><li>[Office 365의 맬웨어 및 랜 섬 웨어 보호](https://docs.microsoft.com/Office365/Enterprise/office-365-malware-and-ransomware-protection)</li><li>[Office 365에서 랜 섬 웨어 공격 으로부터 복구](recover-from-ransomware.md)</li></ul> <p> 메일 흐름 규칙을 만들어 외부 도메인으로 전자 메일을 자동 전달 하지 못하게 합니다. 자세한 내용은 [보안 점수를 사용한 클라이언트 외부 전달 규칙 완화](https://docs.microsoft.com/archive/blogs/office365security/mitigating-client-external-forwarding-rules-with-secure-score)를 참조 하세요. <p> 추가 정보: [Exchange Online의 메일 흐름 규칙 (전송 규칙)](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)|
|**최신 인증 사용**|아니요|최신 인증은 MFA (multi-factor authentication)를 사용 하기 위한 필수 구성 요소입니다. 전자 메일을 비롯 한 클라우드 리소스 액세스를 보호 하려면 MFA를 사용 하는 것이 좋습니다. <p> 다음 항목을 참조 하세요. <ul><li>[Exchange Online에서 최신 인증 사용 여부 설정](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online)</li><li>[비즈니스용 Skype Online: 최신 인증용으로 테 넌 트를 사용 하도록 설정](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx)</li></ul> <p> 최신 인증은 Office 2016 클라이언트, SharePoint Online 및 비즈니스용 OneDrive에 기본적으로 사용 하도록 설정 되어 있습니다. <p> 추가 정보: [office 2013 및 office 2016 클라이언트 앱에 대 한 최신 인증이 작동 하는 방식](https://docs.microsoft.com/microsoft-365/enterprise/modern-auth-for-office-2013-and-2016)|
|

## <a name="configure-tenant-wide-sharing-policies-in-sharepoint-admin-center"></a>SharePoint 관리 센터에서 테 넌 트 수준 공유 정책 구성

보호 수준에 따라 SharePoint 팀 사이트를 구성 하기 위한 Microsoft 권장 사항을 기준 보호로 시작 합니다. 자세한 내용은 [SharePoint Online 사이트 및 파일 보호](https://docs.microsoft.com/microsoft-365-enterprise/secure-sharepoint-online-sites-and-files) 를 참조 하세요.

기본 수준에서 구성 된 SharePoint 팀 사이트는 익명 액세스 링크를 사용 하 여 외부 사용자와 파일을 공유할 수 있습니다. 전자 메일로 파일을 보내는 대신이 방법을 사용 하는 것이 좋습니다.

기준 보호를 위한 목표를 지원 하려면 여기에서 권장 하는 대로 테 넌 트 수준 공유 정책을 구성 합니다. 개별 사이트에 대 한 공유 설정은이 테 넌 트 차원 정책 보다 더 제한적일 수 있지만 허용은 더 제한적입니다.

****

|영역|기본 정책 포함|권장 사항|
|---|---|---|
|**공유** (SharePoint Online 및 비즈니스용 OneDrive)|예|외부 공유는 기본적으로 사용 하도록 설정 됩니다. 다음 설정을 권장 합니다. <ul><li>인증 된 외부 사용자에 대 한 공유를 허용 하 고 익명 액세스 링크를 사용 합니다 (기본 설정).</li><li>익명 액세스 링크는 다음 며칠 후에 만료 됩니다. 원하는 경우 숫자를 입력 합니다 (예: 30 일).</li><li>기본 링크 유형-내부 (조직의 사용자만)를 선택 합니다. 익명 링크를 사용 하 여 공유 하려는 사용자는 공유 메뉴에서이 옵션을 선택 해야 합니다.</li></ul> <p> 추가 정보: [외부 공유 개요](https://docs.microsoft.com/sharepoint/external-sharing-overview)|
|

SharePoint 관리 센터 및 비즈니스용 OneDrive 관리 센터에는 동일한 설정이 포함 됩니다. 두 관리 센터의 설정이 둘 다에 적용 됩니다.

## <a name="configure-settings-in-azure-active-directory"></a>Azure Active Directory의 설정 구성

보다 안전한 환경에 대해 테 넌 트 전체 설치를 완료 하려면 Azure Active Directory에서 이러한 두 영역을 방문 해야 합니다.

### <a name="configure-named-locations-under-conditional-access"></a>명명 된 위치 구성 (조건부 액세스 아래)

조직에 안전한 네트워크 액세스 권한이 있는 사무실이 포함 되어 있는 경우에는 신뢰할 수 있는 IP 주소 범위를 Azure Active Directory에 명명 된 위치로 추가 합니다. 이 기능은 로그인 위험 이벤트에 대해 보고 된 가양성 수를 줄이는 데 도움이 됩니다.

참고: [Azure Active Directory에서 명명 된 위치](https://docs.microsoft.com/azure/active-directory/active-directory-named-locations)

### <a name="block-apps-that-dont-support-modern-authentication"></a>최신 인증을 지원 하지 않는 앱 차단

다단계 인증을 사용 하려면 최신 인증을 지 원하는 앱이 필요 합니다. 최신 인증을 지원 하지 않는 앱은 조건부 액세스 규칙을 사용 하 여 차단할 수 없습니다.

보안 환경에서는 최신 인증을 지원 하지 않는 앱에 대해 인증을 사용 하지 않도록 설정 해야 합니다. 곧 제공 되는 컨트롤을 사용 하 여 Azure Active Directory에서이 작업을 수행할 수 있습니다.

이 경우에는 다음 방법 중 하나를 사용 하 여 SharePoint Online 및 비즈니스용 OneDrive에 대해이 작업을 수행 합니다.

- PowerShell을 사용 하려면 [ADAL (최신 인증을 사용 하지 않는 앱 차단)](https://docs.microsoft.com/mem/intune/protect/app-modern-authentication-block)을 참조 하세요.

- "장치 액세스 ' 페이지 (최신 인증을 사용 하지 않는 앱에서의 액세스 제어)의 SharePoint 관리 센터에서이를 구성 합니다. 차단을 선택 합니다.

## <a name="get-started-with-cloud-app-security-or-office-365-cloud-app-security"></a>Cloud App Security 또는 Office 365 Cloud App Security 시작 하기

Office 365 Cloud App Security를 사용 하 여 위험을 평가 하 고 의심 스러운 활동에 대해 알림을 받아 작업을 자동으로 수행 합니다. Office 365 E5 요금제가 필요 합니다.

또는 Office 365를 포함 하 여 모든 클라우드 응용 프로그램에 대 한 액세스 권한 부여, 포괄적인 제어 및 향상 된 보호 기능을 사용 하는 경우에도 Microsoft Cloud App Security를 사용해 서 심층적으로 확인할 수 있습니다.

이 솔루션은 EMS E5 계획을 권장 하기 때문에 해당 환경의 다른 SaaS 응용 프로그램과 함께 사용할 수 있도록 Cloud App Security부터 시작 하는 것이 좋습니다. 기본 정책 및 설정으로 시작 합니다.

추가 정보:

- [Cloud App Security 배포](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)

- [Microsoft Cloud App Security에 대한 자세한 정보](https://www.microsoft.com/cloud-platform/cloud-app-security)

- [Cloud App Security 란?](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)

![Cloud App Security 대시보드](../../media/1fb2aa65-54b8-4746-9f5e-c187d339e9f5.png)

## <a name="additional-resources"></a>추가 리소스

다음 문서 및 가이드에서는 Microsoft 365 환경을 보호 하기 위한 추가 지침을 제공 합니다.

- [정치적 캠페인, 비영리 및 기타 agile 조직에 대 한 Microsoft 보안 지침](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md) (이 권장 사항은 모든 환경, 특히 클라우드 전용 환경)에서 사용할 수 있습니다.

- [Id 및 장치에 대 한 권장 보안 정책 및 구성](microsoft-365-policies-configurations.md) (이러한 권장 사항에는 AD FS 환경에 대 한 도움말이 포함 됨)
