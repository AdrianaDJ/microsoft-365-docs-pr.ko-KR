---
title: 고객 관리 암호화 기능
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
ms.collection: Strat_O365_Enterprise
ms.custom:
- seo-marvel-mar2020
description: 이 문서에서는 Microsoft 365에서 관리 및 구성할 수 있는 암호화 기술에 대해 알아봅니다.
ms.openlocfilehash: a70f737d1af10622b093bddc682cc493396fff45
ms.sourcegitcommit: 1c90bcc5c56f24895f01c3e0423c3f6b73715c13
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/13/2020
ms.locfileid: "44214224"
---
# <a name="customer-managed-encryption-features"></a>고객 관리 암호화 기능

Microsoft는 microsoft 365에서 관리 하는 Microsoft 365의 암호화 기술과 함께 다음과 같이 관리 및 구성할 수 있는 추가 암호화 기술도 함께 작동 합니다.

- [Azure 권한 관리](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms)

- [보안 다용도 인터넷 메일 확장](https://blogs.technet.com/b/exchange/archive/2014/12/15/how-to-configure-s-mime-in-office-365.aspx)

- [Office 365 메시지 암호화](https://products.office.com/en-us/exchange/office-365-message-encryption)

- [파트너 조직과의 보안 메일 흐름](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-for-secure-mail-flow-with-a-partner)

이러한 기술에 대 한 자세한 내용은 [Microsoft 365 서비스 설명을](https://technet.microsoft.com/library/office-365-service-descriptions.aspx)참조 하십시오.

## <a name="azure-rights-management"></a>Azure 권한 관리

Azure RMS ( [Azure 권한 관리](https://docs.microsoft.com/azure/information-protection/what-is-azure-rms) )는 [azure Information protection](https://docs.microsoft.com/information-protection/understand-explore/what-is-information-protection)에서 사용 되는 보호 기술입니다. 암호화, id 및 권한 부여 정책을 사용 하 여 여러 플랫폼과 장치에서 휴대폰, 태블릿 및 Pc로 파일 및 전자 메일을 보호 합니다. 데이터에 대 한 보호가 유지 되므로 조직 내부 및 외부 모두에서 정보를 보호할 수 있습니다. Azure RMS는 모든 파일 형식에 대 한 영구 보호 기능을 제공 하 고 어디서 든 파일을 보호 하며 b2b 공동 작업 및 광범위 한 Windows 및 비 Windows 장치를 지원 합니다. Azure RMS 보호를 통해 [DLP (데이터 손실 방지) 정책을](https://docs.microsoft.com/exchange/security-and-compliance/data-loss-prevention/data-loss-prevention)강화할 수도 있습니다. Azure 권한 관리 서비스를 사용할 수 있는 응용 프로그램 및 서비스에 대 한 자세한 내용은 azure [권한 관리 서비스를 지 원하는](https://docs.microsoft.com/information-protection/understand-explore/applications-support)응용 프로그램을 참조 하십시오.

Azure RMS는 Microsoft 365와 통합 되어 있으며 모든 고객에 게 제공 됩니다. Azure RMS를 사용 하도록 Microsoft 365을 구성 하려면 [SharePoint 관리 센터에서 Azure 권한 관리를 사용 하 고 irm (정보 권한 관리)을 설정 하도록 irm을 구성](https://technet.microsoft.com/library/dn151475(v=exchg.150).aspx)합니다 .를 참조 하세요. 온-프레미스 ad RMS (Active Directory) RMS 서버를 작동 하 [는 경우에는 온-프레미스 adfs 서버를 사용 하도록 IRM을 구성할](https://docs.microsoft.com/office365/SecurityCompliance/configure-irm-to-use-an-on-premises-ad-rms-server)수도 있지만, 다른 조직과의 안전한 공동 작업 같은 새로운 기능을 사용 하려면 [Azure RMS로 마이그레이션하](https://docs.microsoft.com/azure/information-protection/migrate-from-ad-rms-to-azure-rms) 는 것이 좋습니다.

Azure RMS를 사용 하 여 고객 데이터를 보호 하는 경우 Azure RMS는 무결성에 대 한 SHA-256 해시 알고리즘에 2048 비트 RSA 비대칭 키를 사용 하 여 데이터를 암호화 합니다. Office 문서 및 전자 메일의 대칭 키는 AES 128 비트 (CBC 모드에서 PKCS # 7 패딩을 사용 됨)입니다. Azure rms로 보호 되는 각 문서 또는 전자 메일에 대해 Azure RMS는 단일 AES 키 ("콘텐츠 키")를 만들고 해당 키가 문서에 포함 되어 있으므로 해당 문서 버전을 유지 합니다. 콘텐츠 키가 해당 문서에서 정책의 일부로 조직의 RSA 키 ("Azure Information Protection 테 넌 트 키")를 사용 하 여 보호 되 고 문서 작성자가 해당 정책에도 서명 됩니다. 이 테 넌 트 키는 조직에 대해 Azure RMS로 보호 되는 모든 문서 및 전자 메일에 공통적 이며, 조직에서 고객 관리 하는 테 넌 트 키를 사용 하는 경우에만이 키를 Azure Information Protection 관리자만 변경할 수 있습니다. Azure RMS에서 사용 되는 암호화 컨트롤에 대 한 자세한 내용은 [AZURE rms의 작동 방식를 참조 하세요. 를 살펴보십시오](https://docs.microsoft.com/information-protection/understand-explore/how-does-it-work).

기본 Azure RMS 구현에서 Microsoft는 각 테 넌 트에 대해 고유한 루트 키를 생성 하 고 관리 합니다. 고객은 온-프레미스 Hsm (하드웨어 보안 모듈)에서 키를 생성 하 고 Microsoft의 FIPS 140-2 수준 2-유효성이 검사 된 Hsm으로 전송한 후에도이 키를 제어할 수 있는 키 관리 [(BYOK)](https://docs.microsoft.com/azure/information-protection/plan-implement-tenant-key) 를 사용 하 여 azure RMS에서 루트 키의 수명 주기를 관리할 수 있습니다. 키를 보호 된 Hsm에서 내보내거나 추출할 수 없으므로 모든 담당자에 게 루트 키에 대 한 액세스 권한을 부여 하지 않습니다. 또한 언제 든 지 루트 키에 대 한 모든 액세스를 표시 하는 거의 실시간 로그에 액세스할 수 있습니다. 자세한 내용은 [Azure 권한 관리 사용 현황 로깅 및 분석](https://docs.microsoft.com/azure/information-protection/log-analyze-usage)을 참조 하세요.

Azure 권한 관리는 유선 탭핑, 중간자 개입 공격, 데이터 절도, 조직 공유 정책에 대 한 의도 하지 않은 위반 등의 위협을 완화 하는 데 도움이 됩니다. 이와 동시에, 해당 데이터를 따르는 정책에 의해 전달 되는 고객 데이터에 대 한 모든 unwarranted 액세스를 차단 하 고, 잘못 된 사용자가 의도적으로 또는 모르고 데이터 손실 방지 기능을 제공 하는 경우 해당 데이터의 위험을 완화 합니다. Azure Information Protection의 일부로 사용 되는 경우 Azure RMS는 데이터 분류 및 레이블 지정 기능, 콘텐츠 표시, 문서 액세스 추적 및 액세스 해지 기능도 제공 합니다. 이러한 기능에 대 한 자세한 내용은 azure [information protection,](https://docs.microsoft.com/information-protection/understand-explore/what-is-information-protection) [azure information protection 배포 로드맵](https://docs.microsoft.com/information-protection/plan-design/deployment-roadmap)및 [azure information protection의 빠른 시작 자습서](https://docs.microsoft.com/information-protection/get-started/infoprotect-quick-start-tutorial)를 참조 하세요.

## <a name="secure-multipurpose-internet-mail-extension"></a>보안 다용도 인터넷 메일 확장

S/MIME (Secure/Expressioninternet Mail Extensions)는 MIME 데이터의 디지털 서명 및 공개 키 암호화에 대 한 표준입니다. S/MIME은 Rfc 3369, 3370, 3850, 3851 및 기타 항목에 정의 되어 있습니다. 이를 통해 사용자는 전자 메일을 암호화 하 고 전자 메일에 디지털 서명을 할 수 있습니다. S/MIME을 사용 하 여 암호화 된 전자 메일은 해당 받는 사람만 사용할 수 있는 개인 키를 사용 하 여 전자 메일을 받는 사람만 암호를 해독할 수 있습니다. 따라서 전자 메일을 받는 사람이 아닌 다른 사람에 게 서 해당 전자 메일의 암호를 해독할 수 없습니다.

[Microsoft는 S/MIME를 지원](https://blogs.technet.com/b/exchange/archive/2014/12/15/how-to-configure-s-mime-in-office-365.aspx)합니다. 공용 인증서는 고객의 온-프레미스 Active Directory에 배포 되 고 Microsoft 365 테 넌 트로 복제 될 수 있는 특성에 저장 됩니다. 공개 키에 해당 하는 개인 키는 온-프레미스에 유지 되 고 Office 365로 전송 되지 않습니다. 사용자는 Outlook, 웹에서 Outlook, Exchange ActiveSync 클라이언트를 사용 하 여 조직의 두 사용자 간에 전자 메일을 작성, 암호화, 해독, 읽고, 디지털 서명할 수 있습니다. 자세한 내용은 [현재 Office 365에서 S/MIME 암호화](https://blogs.office.com/2014/02/26/smime-encryption-now-in-office-365/)를 참조 하세요.

## <a name="office-365-message-encryption"></a>Office 365 메시지 암호화

Aip ( [Azure Information Protection](https://docs.microsoft.com/information-protection/understand-explore/what-is-information-protection) )를 기반으로 하는 [Office 365 메시지 암호화](https://products.office.com/exchange/office-365-message-encryption) (OME)를 통해 모든 사용자에 게 암호화 및 권한으로 보호 된 메일을 보낼 수 있습니다. OME는 연결 누르기 및 중간자와 같은 위협 및 기타 위협 (예: 적절 한 사용 권한이 없는 권한이 없는 사용자의 unwarranted 데이터 액세스)을 완화 합니다. Microsoft는 Azure Information Protection을 토대로 구축 된 보다 간단 하 고 직관적인 보안 전자 메일 환경을 제공 합니다. Microsoft 365에서 보낸 메시지를 조직 내부 또는 외부의 모든 사람에 게 보호할 수 있습니다. 이러한 메시지는 Azure Active Directory, Microsoft 계정 및 Google Id를 비롯 한 모든 id를 사용 하는 다양 한 메일 클라이언트 집합에서 볼 수 있습니다. 조직에서 암호화 된 메시지를 사용할 수 있는 방법에 대 한 자세한 내용은 [Office 365 메시지 암호화](https://docs.microsoft.com/microsoft-365/compliance/ome)를 참조 하세요.

## <a name="transport-layer-security"></a>전송 계층 보안   

파트너와의 보안 통신을 보장 하려는 경우 인바운드 및 아웃 바운드 커넥터를 사용 하 여 보안 및 메시지 무결성을 제공할 수 있습니다. 인증서를 사용 하 여 각 커넥터에 대해 강제 인바운드 및 아웃 바운드 TLS를 구성할 수 있습니다. 암호화 된 SMTP 채널을 사용 하면 중간자 개입 공격을 통해 데이터가 유출 되지 않도록 할 수 있습니다. 자세한 내용은 [Exchange Online이 TLS를 사용 하 여 전자 메일 연결을 보호 하는 방법을](https://docs.microsoft.com/microsoft-365/compliance/exchange-online-uses-tls-to-secure-email-connections)참조 하세요.

## <a name="domain-keys-identified-mail"></a>도메인 키 식별 메일

EOP (exchange Online Protection) 및 Exchange Online은 DKIM (Domain Keys 식별 메일) 메시지의 인바운드 유효성 검사를 지원 합니다. DKIM은 메시지가 원래 있었던 도메인에서 보낸 것 이며 다른 사용자에 의해 위장 되지 않았음을 검사 하는 방법입니다. 전자 메일 메시지를 발송을 담당 하는 조직에 연결할 수 있으며 전자 메일 암호화에 대 한 보다 큰 패러다임의 일부임을 제공 합니다. 이 패러다임의 세 가지 부분에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [스푸핑을 방지할 수 있도록 SPF 설정](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)

- [DKIM을 사용하여 사용자 지정 도메인에서 전송한 아웃바운드 전자 메일의 유효성 검사](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)

- [DMARC를 사용하여 전자 메일의 유효성 검사](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)
