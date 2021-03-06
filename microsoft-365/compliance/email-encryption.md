---
title: Microsoft 365의 전자 메일 암호화
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/28/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
description: OME(Office 메시지 암호화), S/MIME, IRM(정보 권한 관리)를 비롯한 Microsoft 365 암호화 옵션을 비교하고 TLS(전송 계층 보안)에 대해 자세히 알아보세요.
ms.openlocfilehash: 81ce8ca567c2b696060a1dd41b9af06bfc7b94a7
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769056"
---
# <a name="email-encryption"></a>전자 메일 암호화

이 문서에서는 OME(Office 메시지 암호화), S/MIME, IRM(정보 권한 관리)을 비롯한 Microsoft 365의 암호화 옵션을 비교하고 TLS(전송 계층 보안)을 소개합니다.
  
Microsoft 365 delivers multiple encryption options to help you meet your business needs for email security. This article presents three ways to encrypt email in Office 365. If you want to learn more about all security features in Office 365, visit the [Office 365 Trust Center](https://go.microsoft.com/fwlink/p/?LinkID=282470). This article introduces the three types of encryption available for Microsoft 365 administrators to help secure email in Office 365:
  
- OME(Office 메시지 암호화)

- S/MIME(Secure/Multipurpose Internet Mail Extensions)

- IRM(정보 권한 관리)

## <a name="email-encryption-and-how-microsoft-365-uses-it"></a>전자 메일 암호화 및 Microsoft 365가 이를 사용하는 방법

Encryption is the process by which information is encoded so that only an authorized recipient can decode and consume the information. Microsoft 365 uses encryption in two ways: in the service, and as a customer control. In the service, encryption is used in Microsoft 365 by default; you don't have to configure anything. For example, Microsoft 365 uses Transport Layer Security (TLS) to encrypt the connection, or session, between two servers. 
  
일반적으로 전자 메일 암호화가 작동하는 방식은 다음과 같습니다.
  
- 보내는 사람의 컴퓨터에서 또는 메시지를 전송하는 동안 중앙 서버를 통해 메시지가 암호화되거나 일반 텍스트에서 읽을 수 없는 암호 텍스트로 변환됩니다.

- 메시지를 누군가 가로채는 경우 읽지 못하도록 보호하기 위해 메시지는 전송되는 동안 암호 텍스트로 남아 있습니다.

- 받는 사람이 메시지를 받으면 다음 두 가지 방법 중 하나를 통해 메시지가 읽을 수 있는 일반 텍스트 형식으로 다시 변환됩니다.

  - 받는 사람의 컴퓨터가 메시지의 암호를 해독하는 키를 사용하거나

  - 중앙 서버가 받는 사람의 ID를 확인한 후 받는 사람을 대신하여 메시지의 암호를 해독합니다.

Microsoft 365 내에서 조직 간의 통신, Microsoft 365와 Microsoft 365 외부의 신뢰할 수 있는 비즈니스 파트너 간의 통신 등 Microsoft 365에서 통신 보안을 확보하는 방법에 대한 자세한 내용은 [Office 365의 전자 메일 연결 보안을 위해 Exchange Online에서 TLS를 사용하는 방법](exchange-online-uses-tls-to-secure-email-connections.md)을 참조하세요.
  
[Office 365의 암호화](https://www.youtube.com/watch?v=KmfxCd5ublI)에 대한 소개를 보려면이 비디오를 시청하세요.
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a>Office 365에서 사용할 수 있는 전자 메일 암호화 옵션 비교

||![OME를 설명하는 개념 아트워크](../media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)|![IRM을 설명하는 개념 아트워크](../media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)|![SMIME를 설명하는 개념 아트워크](../media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)|
|:-----|:-----|:-----|:-----|
|OME(Office 365 메시지 암호화)란 무엇입니까?|OME(Office 365 메시지 암호화)는 Azure RMS(권한 관리)를 기반으로 구축된 서비스로, 대상의 전자 메일 주소(Gmail, Yahoo! Mail, Outlook.com 등)에 상관없이 사용자 조직 내부 또는 외부 사람에게 암호화된 전자 메일을 보낼 수 있습니다. <br/> 관리자는 암호화 조건을 정의하는 전송 규칙을 설정할 수 있습니다. 사용자가 규칙에 맞는 메시지를 보내면 암호화가 자동으로 적용됩니다. <br/> To view encrypted messages, recipients can either get a one-time passcode, sign in with a Microsoft account, or sign in with a work or school account associated with Office 365. Recipients can also send encrypted replies. They don't need a Microsoft 365 subscription to view encrypted messages or send encrypted replies.|IRM은 전자 메일 메시지에 사용 제한을 적용하는 암호화 솔루션입니다. 권한이 없는 사용자가 중요한 정보를 인쇄, 전달 또는 복사하는 것을 방지할 수 있습니다. <br/> Microsoft 365의 IRM 기능은 Azure RMS(Azure 권한 관리)를 사용합니다.|S/MIME is a certificate-based encryption solution that allows you to both encrypt and digitally sign a message. The message encryption helps ensure that only the intended recipient can open and read the message. A digital signature helps the recipient validate the identity of the sender. <br/> 디지털 서명과 메시지 암호화 둘 모두는 디지털 서명을 확인하고 메시지를 암호화 또는 암호 해독하는 키가 포함된 고유한 디지털 인증서를 사용하여 가능해졌습니다. <br/> To use S/MIME, you must have public keys on file for each recipient. Recipients have to maintain their own private keys, which must remain secure. If a recipient's private keys are compromised, the recipient needs to get a new private key and redistribute public keys to all potential senders.|
|어떤 작업을 수행하나요?|OME: <br/> 내부 또는 외부 받는 사람에게 보내는 메시지를 암호화합니다. <br/>  사용자가 Outlook.com, Yahoo! Mail, Gmail 등의 전자 메일 주소로 암호화된 메시지를 보낼 수 있습니다. <br/>  관리자가 전자 메일 확인 포털을 사용자 지정하여 조직의 브랜드를 반영할 수 있습니다. <br/> Microsoft가 사용자 대신 키를 안전하게 관리합니다. <br/> 브라우저에서 암호화된 메시지(HTML 첨부 파일로 전송)를 열 수 있는 한 특별한 클라이언트 쪽 소프트웨어가 필요하지 않습니다.|IRM: <br/> 암호화 및 사용 제한을 사용하여 전자 메일 메시지 및 첨부 파일을 온라인/오프라인으로 보호합니다. <br/> 관리자가 전송 규칙 또는 Outlook 보호 규칙을 설정할 수 있도록 함으로써 IRM을 자동으로 적용하여 메시지를 선택할 수 있습니다. <br/> Outlook 또는 웹용 Outlook(이전 Outlook Web App)에서 템플릿을 수동으로 적용할 수 있도록 합니다.|S/MIME는 디지털 서명으로 기밀성 보낸사람 인증을 확인하고 암호화로 메시지 기밀을 확인합니다.|
|어떤 작업을 하지 않나요?|OME doesn't let you apply usage restrictions to messages. For example, you can't use it to stop a recipient from forwarding or printing an encrypted message.|Some applications may not support IRM emails on all devices. For more information about these and other products that support IRM email, see [Client device capabilities](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities).|S/MIME는 암호화된 메시지에 대한 맬웨어, 스팸 또는 정책 검색을 허용하지 않습니다.|
|권장 사항 및 예제 시나리오|We recommend using OME when you want to send sensitive business information to people outside your organization, whether they're consumers or other businesses. For example:  <br/>  은행 직원이 고객에게 신용 카드 청구서를 보내는 경우  <br/>  병원에서 환자에게 의료 기록을 보내는 경우  <br/>  한 변호사가 다른 변호사에게 기밀 법적 정보를 보내는 경우|사용 제한뿐만 아니라 암호화도 적용하려는 경우 IRM을 사용하는 것이 좋습니다. 예를 들면 다음과 같습니다.  <br/>  자신의 팀에 새 제품 관련 기밀 정보를 보내는 관리자가 “전달 금지” 옵션을 적용하는 경우  <br/>  임원이 Office 365를 사용하는 파트너의 첨부 파일이 포함된 입찰 제안서를 다른 회사와 공유해야 하는데 전자 메일과 첨부 파일이 모두 보호되어야 하는 경우|사용자의 조직 또는 받는 사람의 조직이 진정한 피어 투 피어 암호화를 요구하는 경우 S/MIME를 사용하는 것이 좋습니다.  <br/>  S/MIME는 다음과 같은 시나리오에서 가장 많이 사용됩니다.  <br/>  정부 기관이 다른 정부 기관과 통신하는 경우  <br/>  기업이 정부 기관과 통신하는 경우|
||

[Azure Information Protection](https://docs.microsoft.com/microsoft-365/compliance/protect-information) 및 전자 메일 암호화를 모두 사용하여 데이터를 보호하는 경우, 다음을 고려하세요.
- OME 및 IRM 암호화에 민감도 레이블을 사용할 수 있습니다. 자세한 내용은 [민감도 레이블을 사용하여 암호화를 적용하여 콘텐츠에 대한 액세스 제한](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels?view=o365-worldwide#what-happens-to-existing-encryption-when-a-labels-applied)을 참조하세요.
- S/MIME를 사용하여 디지털 서명이 된 전자 메일에 민감도 레이블을 적용할 수 있습니다.
- 종단 간 암호화로 보호되는 메시지는 정책에서 처리되지 않으므로 S/MIME를 사용하여 암호화된 전자 메일에 민감도 레이블을 적용할 수 없습니다.

## <a name="encryption-options-available-for-my-microsoft-365-subscription"></a>내 Microsoft 365 구독에 사용할 수 있는 암호화 옵션

Microsoft 365 구독의 전자 메일 암호화 옵션에 대한 내용은 [Exchange Online 서비스 설명](https://technet.microsoft.com/library/exchange-online-service-description.aspx)을 참조하세요. 여기서 다음 암호화 기능에 대한 정보를 찾을 수 있습니다.

- IRM 기능과 새 OME 기능을 포함하는 Azure RMS

- S/MIME

- TLS

- BitLocker를 통한 보관된 데이터 암호화

Microsoft 365와 함께 PGP(Pretty Good Privacy)와 같은 타사 암호화 도구를 사용할 수도 있습니다. Microsoft 365는 PGP/MIME를 지원하지 않으므로 PGP/Inline만을 사용하여 PGP-암호화된 전자 메일을 보내고 받을 수 있습니다.

## <a name="what-about-encryption-for-data-at-rest"></a>보관된 데이터의 암호화는 어떻게 하나요?

“보관된 데이터”는 활성 전송 중이 아닌 데이터를 나타냅니다. Microsoft 365에서는 BitLocker 드라이브 암호화를 사용하여 보관된 전자 메일 데이터를 암호화합니다. BitLocker는 Microsoft 데이터 센터의 하드 드라이브를 암호화하여 무단 액세스에 대한 보호를 강화합니다. 자세한 내용은 [BitLocker 개요](https://go.microsoft.com/fwlink/p/?LinkId=394737)를 참조하세요.
  
## <a name="more-information-about-email-encryption-options"></a>전자 메일 암호화 옵션에 대한 자세한 정보

이 문서와 TLS에서의 전자 메일 암호화 옵션에 대한 자세한 내용은 다음 문서를 참조하세요.
  
**OME**
  
[OME(Office 365 메시지 암호화)](ome.md)
  
**IRM**
  
[Exchange Online의 정보 권한 관리](https://technet.microsoft.com/library/jj983436%28v=exchg.150%29.aspx)
  
[Azure 권한 관리란?](https://technet.microsoft.com/library/jj585026)
  
**S/MIME**
  
[메시지 서명 및 암호화를 위한 S/MIME](https://technet.microsoft.com/library/dn626158)
  
[S/MIME 이해](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[공개 키 암호화 이해](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
**TLS**
  
[커넥터를 사용하여 사용자 지정 메일 흐름 구성하기](https://technet.microsoft.com/library/jj723138%28v=exchg.150%29.aspx)
