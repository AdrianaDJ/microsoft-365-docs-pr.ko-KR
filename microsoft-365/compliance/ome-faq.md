---
title: 메시지 암호화 FAQ
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 05/22/2020
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0432dce9-d9b6-4e73-8a13-4a932eb0081e
description: 새 메시지 보호 기능의 작동 방식에 대 한 질문이 있나요? 여기에서 대답을 확인 하세요.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: efccbdf2be33fb771e7e68ba5a0b3dafa82d9ce8
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47546062"
---
# <a name="message-encryption-faq"></a>메시지 암호화 FAQ

새 메시지 보호 기능의 작동 방식에 대 한 질문이 있나요? 여기에서 대답을 확인 하세요. 또한 azure information Protection에서 데이터 보호 서비스, Azure 권한 관리에 대 한 질문에 대 한 답변을 얻을 수 있도록 [Azure Information protection의 데이터 보호에 대 한](https://docs.microsoft.com/information-protection/get-started/faqs-rms) 질문과 대답을 확인 하세요.

## <a name="what-is-office-365-message-encryption-ome"></a>Office 365 메시지 암호화 란 무엇입니까 (OME)?

OME는 전자 메일 암호화 및 권한 관리 기능을 결합 합니다. 권한 관리 기능은 Azure Information Protection에 의해 구동 됩니다.

## <a name="who-can-use-ome"></a>누가 OME를 사용할 수 있나요?

다음 조건에서 OME의 새 기능을 사용할 수 있습니다.
  
- Office 365에서 Exchange Online에 대 한 OME 또는 IRM을 설정 하지 않은 경우

- OME 및 IRM을 설정한 경우 azure Information Protection에서 Azure 권한 관리 서비스를 사용 하는 경우 다음 단계를 사용할 수 있습니다.

- AD RMS (Active Directory Rights Management services)와 함께 Exchange Online을 사용 하는 경우에는 이러한 새로운 기능을 즉시 사용 하도록 설정할 수 없습니다. 대신 [AD RMS를 Azure Information Protection로 마이그레이션](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) 해야 합니다. 마이그레이션이 완료 되 면 OME를 성공적으로 설정할 수 있습니다.

  Azure Information Protection으로 마이그레이션하지 않고 Exchange Online에서 온-프레미스 AD RMS를 계속 사용 하도록 선택 하는 경우 이러한 새로운 기능을 사용할 수 없게 됩니다.

## <a name="what-subscriptions-do-i-need-to-use-the-new-ome-capabilities"></a>새 OME 기능을 사용 하는 데 필요한 구독은 무엇입니까?

새 OME 기능을 사용 하려면 다음 계획 중 하나가 필요 합니다.
  
- Office 365 메시지 암호화는 Office 365 Enterprise E3 및 E5, microsoft Enterprise E3 및 E5, Microsoft 365 Business Premium, Office 365 A1, A3, A5 및 Office 365 정부 G3 및 G5의 일부로 제공 됩니다. 고객은 Azure Information Protection에서 제공 하는 새로운 보호 기능을 수신 하기 위해 추가 라이선스가 필요 하지 않습니다.

- 또한 다음 계획에 Azure Information Protection 계획 1을 추가 하 여 Exchange Online 계획 1, Exchange Online 계획 2, Office 365 F1, 365 Microsoft 365 Business Standard 또는 Office 365 Enterprise E1과 같은 새로운 Office 365 메시지 암호화 기능을 받을 수 있습니다.

- Office 365 메시지 암호화에서 각 사용자 benefiting 기능을 사용 하도록 허가 받아야 합니다.

- 전체 목록은 Office 365 메시지 암호화에 대 한 [Exchange Online 서비스 설명을](https://technet.microsoft.com/library/exchange-online-service-description.aspx) 참조 하세요.

## <a name="can-i-use-exchange-online-with-bring-your-own-key-byok-in-azure-information-protection"></a>Exchange Online을 사용 하 여 Azure Information Protection에서 직접 키 (BYOK)를 가져올 수 있나요?

예로! OME을 설정 하기 전에 시작 하기 전에 확인을 설정 하는 단계를 완료 하는 것이 좋습니다.
  
BYOK에 대 한 자세한 내용은 [Azure Information Protection 테 넌 트 키 계획 및 구현](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key)를 참조 하세요.
  
## <a name="do-ome-and-byok-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>Azure Information Protection을 사용 하 여 OME 및 BYOK를 수행 하 고, subpoenas와 같은 타사 데이터 요청에 대 한 Microsoft의 접근 방식을 변경 합니다.

아니요. OME 및 Azure Information Protection에서 BYOK 라는 자체 암호화 키를 제공 하 고 제어 하는 옵션은 사법 기관에 대응 하도록 설계 되지 않았습니다. Azure Information Protection에 대 한 BYOK를 사용 하는 OME는 준수 중심 고객을 위해 설계 되었습니다. Microsoft는 고객 데이터에 대 한 타사 요청을 매우 심각 하 게 수행 합니다. 클라우드 서비스 공급자는 항상 고객 데이터에 대 한 개인 정보를 제공 합니다. 소환장이 발생 하는 경우에는 항상 제 3 자가 고객에 게 리디렉션되어 정보를 얻도록 시도 합니다. (정부 Smith의 블로그에서 [고객 데이터 보호 스누핑](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/))를 읽어 보십시오. 받은 요청의 세부 정보를 주기적으로 게시 합니다. 타사 데이터 요청에 대 한 자세한 내용은 Microsoft 보안 센터에서 [고객 데이터에 액세스 하기 위해 정부 및 법 집행 요청에 응답](https://www.microsoft.com/trustcenter/privacy/govt-requests-for-data) 을 참조 하세요. 또한 [OST (온라인 서비스 약관)](https://www.microsoft.com/Licensing/product-licensing/products.aspx)에서 "고객 데이터 공개"를 참조 하세요.
  
## <a name="how-is-this-feature-related-to-legacy-office-365-message-encryption-ome-and-information-rights-management-irm-features"></a>이 기능은 어떻게 레거시 Office 365 메시지 암호화 (OME) 및 IRM (정보 권한 관리) 기능과 관련 되어 있습니까?

Office 365 메시지 암호화에 대 한 새로운 기능은 기존 IRM 및 레거시 OME 솔루션의 발전 사항입니다. 다음 표에서는 자세한 정보를 제공 합니다.
  
**레거시 OME, IRM 및 새로운 OME 기능 비교**

|**기능**|**이전 버전의 OME**|**IRM**|**새로운 OME 기능**|
|:-----|:-----|:-----|:-----|
|**암호화 된 전자 메일 보내기**|Exchange 메일 흐름 규칙만을 통해서만|최종 사용자가 Windows 용 Outlook, Mac 용 Outlook 또는 웹용 Outlook에서 시작 되었습니다. 또는 Exchange 메일 흐름 규칙을 통해|최종 사용자가 Windows 용 Outlook, Mac 용 Outlook 또는 웹용 Outlook에서 시작 되었습니다. 또는 메일 흐름 규칙을 통해|
|**권한 관리**|-|전달 금지 옵션 및 사용자 지정 서식 파일|전달 금지 옵션, 암호화 전용 옵션, 기본 및 사용자 지정 템플릿|
|**지원 되는 받는 사람 유형**|외부 받는 사람만|내부 받는 사람만|내부 및 외부 받는 사람|
|**받는 사람에 대 한 경험**|외부 받는 사람이 브라우저 또는 다운로드 된 모바일 앱에서 다운로드 하 여 연 HTML 메시지를 수신 했습니다.|내부 받는 사람도 Windows 용 outlook, Mac 용 Outlook 및 웹용 Outlook에서 암호화 된 전자 메일만 수신 합니다.|내부 및 외부 받는 사람이 Windows 용 outlook, outlook for Mac, 웹용 outlook, Android 용 outlook, 웹에서 outlook, 타사 또는 다른 조직에 있는지 여부에 관계 없이 web portal을 받습니다. OME 포털에는 별도의 다운로드를 수행 하지 않아도 됩니다.|
|**고유한 키를 제공 합니다.**|사용할 수 없음|사용할 수 없음| BYOK 지원 됨|

## <a name="how-do-i-enable-the-new-ome-capabilities-for-my-organization"></a>조직에 대해 새 OME 기능을 사용 하도록 설정 하려면 어떻게 해야 하나요?

[새 Office 365 메시지 암호화 기능 설정을](set-up-new-message-encryption-capabilities.md)참조 하세요.
  
## <a name="will-the-previous-version-of-ome-be-deprecated"></a>이전 버전의 OME는 더 이상 사용 되지 않을 예정 입니까?

이전 버전의 OME를 사용할 수는 있지만 현재는 더 이상 사용 되지 않습니다. 그러나 조직은 신규 및 향상 된 OME 솔루션을 사용 하는 것이 매우 권장 됩니다. 아직 OME을 배포 하지 않은 고객은 이전 버전의 OME를 새로 배포 하는 것을 설정할 수 없습니다.
  
## <a name="my-organization-uses-active-directory-rights-management-can-i-use-this-functionality"></a>조직에서 Active Directory Rights Management를 사용 하 여이 기능을 사용할 수 있나요?

아니요. AD RMS (Active Directory Rights Management services)와 함께 Exchange Online을 사용 하는 경우에는 이러한 새로운 기능을 즉시 사용 하도록 설정할 수 없습니다. 대신 [AD RMS를 Azure Information Protection로 마이그레이션](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) 해야 합니다.
  
## <a name="my-organization-has-an-exchange-hybrid-deployment-can-i-use-this-feature"></a>조직에 Exchange 하이브리드 배포를 포함 하는 경우 이 기능을 사용할 수 있나요?

온-프레미스 사용자는 Exchange Online 메일 흐름 규칙을 사용 하 여 암호화 된 메일을 보낼 수 있습니다. 이렇게 하려면 Exchange Online을 통해 전자 메일을 라우트 해야 합니다. 자세한 내용은 [2 부: 전자 메일 서버에서 Microsoft 365으로 이동 하도록 메일 구성](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365)를 참조 하세요.
  
## <a name="what-email-client-do-i-need-to-use-in-order-to-create-an-ome-encrypted-message-what-applications-are-supported-for-sending-protected-messages"></a>OME 암호화 메시지를 만들기 위해 어떤 전자 메일 클라이언트를 사용 해야 하나요? 보호 된 메시지를 보내는 데 지원 되는 응용 프로그램은 무엇입니까?

Outlook 2016, outlook 2013, Windows 및 Mac 및 웹용 Outlook에서 보호 된 메시지를 만들 수 있습니다.
  
## <a name="what-email-clients-are-supported-to-read-and-reply-to-protected-emails"></a>보호 된 전자 메일을 읽고 회신할 수 있도록 지원 되는 전자 메일 클라이언트는 무엇입니까?

Microsoft 365 사용자는 Windows 및 Mac 용 Outlook (2013 및 2016), 웹용 Outlook 및 Outlook mobile (Android 및 iOS)을 읽고 응답할 수 있습니다. 조직에서 허용 하는 경우 iOS 기본 메일 클라이언트도 사용할 수 있습니다. Microsoft 365 사용자가 아닌 경우 웹 브라우저를 통해 웹에서 암호화 된 메시지를 읽고 회신할 수 있습니다.
  
## <a name="is-there-a-size-limit-for-messages-you-can-send-with-ome"></a>OME을 사용 하 여 보낼 수 있는 메시지의 크기 제한이 있나요?

예. 첨부 파일을 포함 하 여 OME에서 보낼 수 있는 최대 메시지 크기는 30mb입니다.

## <a name="what-file-types-are-supported-as-attachments-in-protected-emails-do-attachments-inherit-the-protection-policies-associated-with-protected-emails"></a>보호 된 전자 메일에서 첨부 파일로 지원 되는 파일 형식은 무엇입니까? 첨부 파일에서 보호 된 전자 메일과 연결 된 보호 정책을 상속 하나요?

모든 파일 형식을 보호 된 메일에 첨부할 수 있습니다. 한 가지 예외를 제외 하 고는 보호 정책이 [Azure Information protection 클라이언트에서 지 원하는 파일 형식](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types)에 언급 된 파일 형식에만 적용 됩니다. OME에서는 Word (.doc), Excel (.xls) 및 PowerPoint (.ppt)의 97-2003 버전의 Office 프로그램을 지원 하지 않습니다.

Word, Excel 또는 PowerPoint 파일과 같은 파일 형식이 지원 되는 경우 받는 사람이 첨부 파일을 다운로드 한 후에도 파일이 항상 보호 됩니다. 예를 들어 첨부 파일이 전달 금지로 보호 되어 있다고 가정해 보겠습니다. 원래 받는 사람은 파일을 다운로드 하 고, 새 받는 사람에 게 메시지를 작성 하 고, 파일을 첨부 합니다. 새 받는 사람이 파일을 받으면 받는 사람은 보호 된 파일을 열 수 없게 됩니다.
  
## <a name="are-pdf-file-attachments-supported"></a>PDF 파일이 첨부 파일을 지원 하나요?

여기서는 간단한 대답이 예입니다. PDF 암호화를 사용 하면 보안 통신 또는 안전한 공동 작업을 통해 중요 한 PDF 문서를 보호할 수 있습니다. 전자 메일을 보낼 때 Office 365 서비스는 Outlook 클라이언트가 아닌 PDF 첨부 파일을 암호화 합니다.

웹용 Outlook, iOS 용 Outlook 및 Android 용 Outlook의 경우 추가 단계를 수행 하지 않고 보낸 Pdf를 암호화할 수 있습니다. 이러한 클라이언트는 기본적으로 PDF 암호화를 지원 합니다.

Outlook 데스크톱은 PDF 파일 첨부 파일의 암호화를 기본적으로 지원 하지 않습니다. 대신, 먼저 PDF 첨부 파일에 암호화를 적용 하도록 Exchange 메일 흐름 규칙이 나 DLP를 설정 해야 합니다. PDF 첨부 파일이 있는 Outlook 데스크톱에서 메일을 보내는 경우 클라이언트는 첨부 파일이 포함 된 메시지를 먼저 서비스에 보냅니다. 서비스가 파일을 받으면 Exchange Online에서 DLP (데이터 손실 방지) 정책 또는 메일 흐름 규칙의 OME 보호를 적용 합니다. 다음으로, Exchange Online은 보호 된 PDF 파일 첨부 파일이 포함 된 메시지를 보냅니다.

PDF 첨부 파일에 대 한 암호화를 사용 하도록 설정 하려면 [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell)에서 다음 명령을 실행 합니다.

```powershell
Set-IRMConfiguration -EnablePdfEncryption $true
```

PDF 암호화를 사용 하면 보안 통신 또는 안전한 공동 작업을 통해 중요 한 PDF 문서를 보호할 수 있습니다. 모든 Outlook 클라이언트의 경우 메시지 및 보호 되지 않는 PDF 첨부 파일은 Exchange Online의 DLP (데이터 손실 방지) 정책 또는 메일 흐름 규칙에 대 한 OME 보호를 상속 합니다. 또한 Outlook 사용자가 보호 되지 않은 PDF 문서를 첨부 하 고 메시지에 보호를 적용 하는 경우 해당 메시지는 메시지 보호를 상속 받습니다. 사용자는 보호 된 Pdf를 지 원하는 응용 프로그램 (예: OME 포털 및 Azure Information Protection 뷰어)에서 암호화 된 첨부 파일을 열 수만 있습니다.

> [!IMPORTANT]
> Outlook 데스크톱 클라이언트에서는 PDF 암호화를 지원 하지 않습니다.

## <a name="are-onedrive-for-business-attachments-supported"></a>비즈니스용 OneDrive 첨부 파일이 지원 됩니까?

Not yet. 비즈니스용 OneDrive 첨부 파일이 지원 되지 않으며 최종 사용자가 비즈니스용 OneDrive 첨부 파일을 포함 하는 메일을 암호화할 수 없습니다.
  
## <a name="what-email-clients-support-preview-of-encrypted-attachments-in-protected-emails"></a>보호 된 전자 메일에서 암호화 된 첨부 파일의 미리 보기를 지 원하는 전자 메일 클라이언트는 무엇입니까?

보호 된 메일로 첨부 파일을 보호 하는 경우 Outlook 클라이언트는 문서를 직접 미리 볼 수 있는 tha 기능을 제공 합니다. Outlook에서는 Office 문서 (.docx, .xlsx, .pptx, doc, xls, ppt)의 미리 보기가 지원 됩니다. 웹용 Outlook은 Office 문서 (.docx, .xlsx, .pptx) 및 PDF의 미리 보기를 지원 합니다.  

## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies"></a>정책을 설정 하 여 메시지를 자동으로 암호화할 수 있습니까?

예. Exchange Online의 메일 흐름 규칙을 사용 하 여 특정 조건에 따라 메시지를 자동으로 암호화 합니다. 예를 들어 받는 사람 ID, 받는 사람 도메인을 기반으로 하거나 메시지의 본문 또는 제목에 있는 콘텐츠를 사용 하 여 정책을 만들 수 있습니다. [Office 365에서 전자 메일 메시지를 암호화 하기 위한 메일 흐름 규칙 정의를](define-mail-flow-rules-to-encrypt-email.md)참조 하세요.
  
## <a name="can-i-automatically-remove-encryption-on-incoming-and-outgoing-mail"></a>들어오고 나가는 메일에서 암호화를 자동으로 제거할 수 있나요?

관리자는 메일 흐름 규칙을 설정 하 여 보내는 메일에 대 한 암호화를 제거할 수 있습니다. 받는 메일에 대 한 암호화를 제거 하는 규칙을 설정할 수는 없습니다.

## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies-in-data-loss-prevention-dlp-through-the-security-amp-compliance-center"></a>보안 및 준수 센터를 통해 DLP (데이터 손실 방지)에서 정책을 설정 하 여 메시지를 자동으로 암호화할 수 &amp; 있습니까?

예로! 메일 흐름 규칙은 Exchange Online에서 설정 하거나, 보안 및 준수 센터에서 DLP를 사용 하 여 설정할 수 있습니다 &amp; .
  
## <a name="can-i-customize-encrypted-messages-with-my-company-branding"></a>회사 브랜딩을 사용 하 여 암호화 된 메시지를 사용자 지정할 수 있습니까?

예로! 전자 메일 메시지 및 OME 포털을 사용자 지정 하는 방법에 대 한 자세한 내용은 암호화 된 메시지에 조직의 브랜드 추가를 참조 하세요. [암호화 된 메시지에 조직의 브랜드 추가를](add-your-organization-brand-to-encrypted-messages.md)참조 하세요.
  
## <a name="are-there-any-reporting-capabilities-or-insights-for-encrypted-emails"></a>암호화 된 전자 메일에 대 한 보고 기능 또는 정보가 있습니까?

보안 및 준수 센터에 암호화 보고서가 있습니다. [보안 & 준수 센터의 전자 메일 보안 보고서 보기를](../security/office-365-security/view-email-security-reports.md)참조 하세요.
  
## <a name="can-i-use-message-encryption-with-compliance-features-such-as-ediscovery"></a>EDiscovery와 같은 규정 준수 기능을 사용 하 여 메시지 암호화를 사용할 수 있나요?

예. 모든 암호화 된 전자 메일 메시지는 Microsoft 365 규정 준수 기능을 통해 검색할 수 있습니다.

## <a name="can-i-remove-encryption-from-email"></a>전자 메일에서 암호화를 제거할 수 있나요?

관리자는 메일 흐름 규칙을 설정 하 여 보내는 메일에서 암호화를 제거할 수 있습니다. 들어오는 메시지의 메일 흐름 규칙을 사용 하 여 암호화를 제거할 수는 없습니다.

## <a name="is-delegated-access-supported"></a>위임 된 액세스를 지원 하나요?

현재로 서는 안 됩니다.

## <a name="can-i-open-encrypted-messages-sent-to-a-shared-mailbox"></a>공유 사서함으로 보낸 암호화 된 메시지를 열 수 있습니까?

예로! 암호화 된 메시지는 공유 사서함에 대해 지원 됩니다.

- 사용자는 공유 사서함이 보호 된 메일을 메일 그룹의 일부로 받은 공유 사서함에서 제한 된 전자 메일을 열 수 있습니다.

- 사용자는 Outlook for Windows, Mac 용 Outlook 및 웹용 Outlook을 사용할 때 전자 메일에서 보호를 상속 하는 첨부 파일을 볼 수 있습니다.

다음 표에는 공유 사서함에 대해 지원 되는 클라이언트가 나와 있습니다.

| 플랫폼 | 메일 읽기 | 전자 메일 첨부 파일 보기 |
|----------|-----------|------------------------|
| 웹용 Outlook | 예 | 예                |
|  Windows용 Outlook| 예 | 예                |
| Outlook for Mac    | 예 | 예                |
| Android용 Outlook| 예 | 아니요                 |
| iOS용 Outlook    | 예 | 아니요                 |
|

현재 알려진 두 가지 제한이 있습니다.

- Outlook mobile을 사용 하 여 모바일 장치에서 받은 전자 메일에 대해서는 첨부 파일을 열 수 없습니다.

- 전자 메일 사용이 가능한 보안 그룹을 통한 할당은 지원 되지 않습니다. 사용자가 공유 사서함에 직접 할당 하 여 제공 되는 액세스를 지원 하며, Exchange Online에 대해 automapping을 사용 하도록 설정 되어 있습니다. Automapping은 Exchange Online에 대해 기본적으로 사용 하도록 설정 됩니다.

**공유 사서함에 사용자를 할당 하려면**

1. [원격 PowerShell을 사용 하 여 Exchange Online에 연결](https://technet.microsoft.com/library/jj984289?v=exchg.150%29.aspx)합니다.

2. Automapping 매개 변수를 사용 하 여 Add-mailboxpermission cmdlet을 실행 합니다. 이 예에서는 지원 사서함에 대 한 Ayla 모든 액세스 권한을 부여 합니다.

   ```powershell
   Add-MailboxPermission -Identity support@contoso.onmicrosoft.com -User ayla@contoso.com -AccessRights FullAccess -AutoMapping $true
   ```

## <a name="what-do-i-do-if-i-dont-receive-the-one-time-pass-code-after-i-requested-it"></a>요청 후 일회용 가공 패스 코드가 수신 되지 않는 경우 어떻게 해야 하나요?

먼저 전자 메일 클라이언트에서 정크 또는 스팸 폴더를 확인 합니다. 조직에 대 한 DKIM 및 DMARC 설정으로 인해 이러한 전자 메일이 스팸으로 필터링 될 수 있습니다.

다음으로, 보안 & 준수 센터에서 격리를 확인 합니다. 대개 1 회 통과 코드를 포함 하는 메시지 (특히 조직에서 수신 하는 첫 번째)는 격리로 끝납니다.
