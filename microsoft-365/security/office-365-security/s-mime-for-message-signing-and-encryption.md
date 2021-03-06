---
title: Exchange Online의 암호화를 위한 S/MIME-Office 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 887c710b-0ec6-4ff0-8065-5f05f74afef3
description: 관리자는 Exchange Online의 S/MIME (Secure/다목적 Internet Mail Extensions)를 사용 하 여 전자 메일을 암호화 하 고 디지털 서명을 하는 방법에 대해 알아볼 수 있습니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 8dce3e3fa3d24e1773f51f96e19a58d8a3b2efce
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48200610"
---
# <a name="smime-for-message-signing-and-encryption-in-exchange-online"></a>Exchange Online의 메시지 서명 및 암호화를 위한 S/MIME

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


S/MIME (Secure/Expressioninternet Mail Extensions)는 디지털 서명 및 암호화 된 메시지를 보내기 위한 광범위 하 게 사용할 수 있는 방법 (보다 정확한 프로토콜)입니다. S/MIME을 사용 하면 전자 메일을 암호화 하 고 디지털 서명을 할 수 있습니다. 전자 메일 메시지와 함께 S/MIME을 사용 하는 경우 해당 메시지를 받는 사용자에 게 받은 편지함에 표시 되는 내용이 보낸 사람과 정확히 일치 하는 메시지 인지 확인 하는 데 도움이 됩니다. 또한 메시지를 수신 하는 사용자가 보낸 사람을 가장 하는 사람이 아닌 특정 보낸 사람 으로부터 온 것을 확인할 수 있습니다. 이를 위해 S/MIME는 인증, 메시지 무결성 및 원본 비 부인 (디지털 서명 사용)와 같은 암호화 보안 서비스를 제공 합니다. 또한 전자 메시징에 대 한 개인 정보 보호 및 데이터 보안 (암호화 사용)을 향상 시킬 수 있습니다. 전자 메일 컨텍스트에서 S/MIME의 기록 및 아키텍처에 대 한 자세한 내용은 [s/Mime 이해](https://docs.microsoft.com/previous-versions/tn-archive/aa995740(v=exchg.65))(영문)를 참조 하십시오.

Exchange Online 관리자로 서 조직의 사서함에 대해 S/MIME 기반 보안을 사용 하도록 설정할 수 있습니다. 여기에 연결 된 항목의 지침을 Exchange Online PowerShell과 함께 사용 하 여 S/MIME을 설정 합니다. 지원 되는 전자 메일 클라이언트에서 S/MIME을 사용 하려면 조직의 사용자에 게 서명 및 암호화를 위해 발급 된 인증서와 온-프레미스 AD DS (Active Directory 도메인 서비스)에 게시 되는 데이터를 포함 해야 합니다. AD DS는 인터넷의 클라우드 서비스 또는 원격 시설이 아닌 관리자가 제어할 수 있는 물리적 위치의 컴퓨터에 있어야 합니다. AD DS에 대 한 자세한 내용은 [Active Directory 도메인 서비스 개요](https://docs.microsoft.com/windows-server/identity/ad-ds/get-started/virtual-dc/active-directory-domain-services-overview)를 참조 하세요.

## <a name="supported-scenarios-and-technical-considerations"></a>지원되는 시나리오 및 기술 고려 사항

다음과 같은 끝점에서 작동 하도록 S/MIME을 설정할 수 있습니다.

- Outlook 2010 이상
- 웹용 Outlook(이전 Outlook Web App)
- EAS(Exchange ActiveSync)

이러한 각 끝점에 대해 S/MIME을 설정 하기 위해 수행 하는 단계는 약간 다릅니다. 일반적으로는 다음 단계를 수행 해야 합니다.

1. Windows 기반 CA (인증 기관)를 설치 하 고 S/MIME 인증서를 발급 하도록 공개 키 인프라를 설정 합니다. 타사 인증서 공급자가 발급한 인증서도 지원됩니다. 자세한 내용은 [Active Directory 인증서 서비스 개요](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/hh831740(v=ws.11))를 참조하세요.

   **참고:**

   - 타사 CA가 발급 한 인증서는 모든 클라이언트 및 장치에서 자동으로 신뢰 하는 이점이 있습니다. 내부 전용 CA에서 발급 하는 인증서는 클라이언트 및 장치에서 자동으로 신뢰 되지 않으며 모든 장치 (예: 전화)를 개인 인증서를 신뢰 하도록 구성할 수는 없습니다.

   - 사용자에 게 인증서를 발급 하기 위해 루트 인증서 대신 중간 인증서를 사용 하는 것이 좋습니다. 이러한 방식으로 인증서를 해지 하 고 다시 발급 해야 하는 경우에도 루트 인증서는 그대로 유지 됩니다.

2. **UserSMIMECertificate** 및/또는 **UserCertificate** 특성의 온-프레미스 AD DS 계정에 사용자 인증서를 게시 합니다.

3. Exchange Online 조직의 경우 적절 한 Azure AD Connect 버전을 사용 하 여 AD DS의 사용자 인증서를 Azure Active Directory에 동기화 합니다. 그러면 이러한 인증서가 Azure Active Directory에서 Exchange Online 디렉터리로 동기화되며 받는 사람에 대한 메시지를 암호화할 때 사용됩니다.

4. S/MIME의 유효성을 검사하기 위해 가상 인증서 모음을 설정합니다. 이 정보는 전자 메일의 서명 유효성을 검사 하 고 신뢰할 수 있는 인증서로 서명 되었는지 확인할 때 웹에서 Outlook에서 사용 합니다.

5. S/MIME을 사용하도록 Outlook 또는 EAS 끝점을 설정합니다.

> [!NOTE]
> Mac, iOS, Android 또는 기타 비 Windows 장치에서는 Outlook에서 S/MIME 컨트롤을 설치할 수 없습니다. 자세한 내용은 [웹용 Outlook에서 S/MIME을 사용 하 여 메시지 암호화](https://support.microsoft.com/office/878c79fc-7088-4b39-966f-14512658f480)를 참조 하세요.

## <a name="setup-smime-with-outlook-on-the-web"></a>웹에서 Outlook을 사용 하 여 S/MIME 설정

Exchange Online에 대해 S/MIME을 설정 하려면 다음과 같은 주요 단계를 수행 해야 합니다.

1. [웹용 Outlook용 S/MIME 설정 구성](configure-s-mime-settings-for-outlook-web-app.md)
2. [S/MIME 유효성 검사를 위한 가상 인증서 컬렉션 설정](set-up-virtual-certificate-collection-to-validate-s-mime.md)
3. [S/MIME용으로 Office 365에 사용자 인증서 동기화](sync-user-certificates-to-office-365-for-s-mime.md)

## <a name="related-message-encryption-technologies"></a>관련 메시지 암호화 기술

메시지 보안이 더 중요 해지면 관리자는 보안 메시징의 원리와 개념을 이해 해야 합니다. 이러한 이해는 사용 가능한 다양 한 보호 관련 기술 (S/MIME 포함)이 증가 하기 때문에 특히 중요 합니다. S/MIME 및 전자 메일과 관련하여 S/MIME이 작동하는 방식에 대해 자세히 알아보려면 [S/MIME 이해](https://docs.microsoft.com/previous-versions/tn-archive/aa995740(v=exchg.65))를 참조하세요. 다양한 암호화 기술이 연동되어 저장된 메시지 및 전송 중인 메시지를 보호합니다. S/MIME은 다음 기술과 동시에 사용할 수 있지만 이러한 기술에 종속되는 것은 아닙니다.

- **TLS(전송 계층 보안)** 는 스누핑 및 도청을 방지하기 위해 전자 메일 서버 간의 터널/경로를 암호화합니다.

- **SSL (Secure Sockets layer)** 은 전자 메일 클라이언트와 Microsoft 365 서버 간의 연결을 암호화 합니다.

- **BitLocker**는 데이터 센터의 하드 드라이브에 저장된 데이터를 암호화하여 무단으로 액세스하는 사용자가 해당 데이터를 읽을 수 없도록 합니다.

### <a name="smime-compared-with-office-365-message-encryption"></a>Office 365 메시지 암호화와 S/MIME 비교

S/MIME에는 b2b 및 b2b 환경에서 자주 사용 되는 인증서 및 게시 인프라가 필요 합니다. 사용자가 S/MIME의 암호화 키를 제어 하 고, 보내는 각 메시지에 대해 암호를 사용할지 여부를 선택할 수 있습니다. Outlook과 같은 전자 메일 프로그램에서는 신뢰할 수 있는 루트 인증 기관 위치를 검색 하 여 디지털 서명 및 서명 확인을 수행 합니다. Office 365 메시지 암호화는 조직 내부 또는 외부에 있는 사람에 게 보낸 메일을 암호화 하기 위해 개별 사용자가 아닌 관리자가 구성할 수 있는 정책 기반 암호화 서비스입니다. 이 서비스는 RMS (Azure 권한 관리)를 기반으로 구축 되 고 공용 키 인프라를 사용 하지 않습니다. Office 365 메시지 암호화도 조직의 브랜드를 사용 하 여 메일을 사용자 지정 하는 기능과 같은 추가 기능을 제공 합니다. Office 365 메시지 암호화에 대 한 자세한 내용은 [Encryption In office 365](https://docs.microsoft.com/microsoft-365/compliance/encryption)을 참조 하십시오.

## <a name="more-information"></a>추가 정보

[웹용 Outlook](https://docs.microsoft.com/exchange/exchange-admin-center)

[보안 메일(2000)](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-2000-server/cc962043(v=technet.10))
