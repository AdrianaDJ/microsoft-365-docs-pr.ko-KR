---
title: 고급 메시지 암호화로 암호화 된 전자 메일 해지
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 06/11/2020
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: 관리자 및 메시지 보낸 사람으로 서 Office 365 고급 메시지 암호화를 사용 하 여 암호화 된 특정 전자 메일을 해지할 수 있습니다.
ms.openlocfilehash: 79ab3ef801d4d19317cbf1416d858de74d9f1393
ms.sourcegitcommit: 22dab0f7604cc057a062698005ff901d40771692
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/25/2020
ms.locfileid: "46868956"
---
# <a name="revoke-email-encrypted-by-advanced-message-encryption"></a>고급 메시지 암호화로 암호화 된 전자 메일 해지

전자 메일 해지가 Office 365 Advanced Message 암호화의 일부로 제공 됩니다. Office 365 Advanced Message Encryption은 [microsoft 365 Enterprise e5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (비영리 스태프 가격), Office 365 Enterprise E5 (비영리 스태프 가격) 및 Office 365 교육용 A5에 포함 되어 있습니다. 조직에서 Office 365 고급 메시지 암호화를 포함 하지 않는 구독을 사용 하는 경우 microsoft 365 E3, microsoft 365 E3 (비영리 직원 가격) 또는 Microsoft 365 (고급 규정 준수) 용 microsoft 365 e3, Microsoft 365 E3 (비영리 스태프 가격) 또는 Office 365 Sku에 대 한 Office 준수 sku 추가 기능을 사용해 서 구매할 수 있습니다.

이 문서는 [Office 365 메시지 암호화](ome.md)에 대 한 보다 광범위 한 문서에 포함 되어 있습니다.

메시지가 Office 365 고급 메시지 암호화를 사용 하 여 암호화 되었지만 Microsoft 365 관리자 이거나 메시지를 보낸 사용자 인 경우 특정 조건에 따라 메시지를 취소할 수 있습니다. 관리자 PowerShell을 사용 하 여 메시지를 해지 합니다. 보낸 사람은 웹에서 Outlook을 통해 직접 보낸 메시지를 해지 합니다. 이 문서에서는 해지가 가능한 상황 및 수행 방법에 대해 설명 합니다.
  
## <a name="encrypted-emails-that-you-can-revoke"></a>해지할 수 있는 암호화 된 전자 메일

받는 사람이 링크 기반 브랜드의 암호화 된 전자 메일을 받은 경우 관리자 및 메시지 보낸 사람은 암호화 된 전자 메일을 해지할 수 있습니다. 받는 사람이 지원 되는 Outlook 클라이언트에서 기본 인라인 환경을 받은 경우 메시지를 해지할 수 없습니다.

받는 사람이 링크 기반 환경이 나 인라인 환경을 수신 하는지 여부는 받는 사람 id 유형에 따라 다릅니다. Office 365 및 Microsoft 계정 받는 사람 (예: outlook.com users)은 지원 되는 Outlook 클라이언트에서 인라인 환경을 가져옵니다. Gmail 및 Yahoo 받는 사람과 같은 다른 모든 받는 사람 유형은 링크 기반 환경을 가져옵니다.

관리자 및 메시지 보낸 사람은 웹용 Outlook에서 직접 암호화를 적용 하 여 암호화 된 메시지를 해지할 수 있습니다. 예를 들어 암호화만 옵션을 사용 하 여 암호화 된 메시지

:::image type="content" source="../media/adhocencryptionrevoke.png" alt-text="웹용 Outlook의 암호화만 옵션을 보여 주는 스크린샷":::

## <a name="recipient-experience-for-revoked-encrypted-emails"></a>해지 된 암호화 전자 메일에 대 한 받는 사람 환경

전자 메일이 해지 되 면 Office 365 메시지 암호화 포털: "보낸 사람이 메시지를 철회 했습니다." 라는 오류가 수신 됩니다.

![암호화 된 전자 메일을 해지 한 것을 보여 주는 스크린샷](../media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-message-that-you-sent"></a>보낸 암호화 된 메시지를 해지 하는 방법

보낸 암호화 된 메시지를 해지 하려면 다음 단계를 완료 합니다.

1. 웹용 Outlook의 **보낸** 편지함 폴더에서 해지할 메시지를 찾습니다.

   메일이 revocable 경우 메시지 맨 위에 "외부 액세스 제거" 링크가 표시 됩니다.

    :::image type="content" source="../media/infoprotect-email-encryption/adhocencryptionrevokesentmsg.png" alt-text="웹용 Outlook에서 해지할 암호화 된 메일을 보여 주는 스크린샷":::

2. **외부 액세스 제거** 를 클릭 하 여 메시지를 해지 합니다.

   메시지에 해당 상태가 해지 된 것으로 표시 됩니다.

   :::image type="content" source="../media/adhocencryptionrevokedmsg.png" alt-text="웹용 Outlook에서 해지 된 암호화 메시지를 보여 주는 스크린샷":::

## <a name="how-to-revoke-an-encrypted-message-as-an-administrator"></a>암호화 된 메시지를 관리자로 해지 하는 방법

Microsoft 365 관리자는 다음과 같은 일반적인 단계를 수행 하 여 적합 한 암호화 된 전자 메일을 해지 합니다.

- 전자 메일의 메시지 ID를 가져옵니다.
- 메시지를 해지할 수 있는지 확인 합니다.
- 메일을 해지 합니다.

### <a name="step-1-obtain-the-message-id-of-the-email"></a>1단계. 전자 메일의 메시지 ID 가져오기

암호화 된 메일을 해지 하려면 먼저 메일의 메시지 ID를 수집 합니다. MessageId는 대개 다음 형식입니다.

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

해지할 전자 메일의 메시지 ID를 확인 하는 방법에는 여러 가지가 있습니다. 이 섹션에서는 몇 가지 옵션에 대해 설명 하지만 ID를 제공 하는 모든 메서드를 사용할 수 있습니다.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a>보안 및 준수 센터에서 메시지 추적을 사용 하 여 해지할 전자 메일의 메시지 ID를 식별 하려면 &amp;

1. [보안 & 준수 센터에서 새 메시지 추적을](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)사용 하 여 보낸 사람이 나 받는 사람에 게 전자 메일을 검색 합니다.

2. 전자 메일을 찾은 후에는이를 선택 하 여 **메시지 추적 세부 정보** 창을 표시 합니다. **자세한 정보** 를 확장 하 여 메시지 ID를 찾습니다.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a>보안 및 준수 센터에서 Office 메시지 암호화 보고서를 사용 하 여 해지할 전자 메일의 메시지 ID를 식별 하려면 &amp;

1. 보안 &amp; 및 준수 센터에서 **메시지 암호화 보고서**로 이동 합니다. 이 보고서에 대 한 자세한 내용은 [보안 및 &amp; 준수 센터의 전자 메일 보안 보고서 보기](../security/office-365-security/view-email-security-reports.md)를 참조 하세요.

2. **정보 보기** 테이블을 선택 하 고 해지할 메시지를 식별 합니다.

3. 메시지를 두 번 클릭 하 여 메시지 ID를 포함 하는 세부 정보를 확인 합니다.

### <a name="step-2-verify-that-the-mail-is-revocable"></a>2단계. 메일이 revocable 확인

메시지를 취소할 수 있는지 여부를 확인 하려면 보안 및 준수 센터의 **Details (정보** ) 테이블에서 암호화 보고서에 해지 상태 필드를 표시할지 여부를 확인 &amp; 합니다.

Windows PowerShell을 사용 하 여 특정 전자 메일 메시지를 해지할 수 있는지 여부를 확인 하려면 다음 단계를 완료 합니다.

1. 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 지침을 확인하려면 [Exchange Online PowerShell에 연결](https://aka.ms/exopowershell)을 참조하세요.

2. 다음과 같이 OMEMessageStatus cmdlet을 실행 합니다.

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   이 명령은 메시지의 제목과 메시지의 revocable 여부를 반환 합니다. 예를 들면 다음과 같습니다.

     ```text
     Subject        IsRevocable
     -------        -----------
     "Test message" True
     ```

### <a name="step-3-revoke-the-mail"></a>3단계. 메일 해지

해지할 전자 메일의 메시지 ID를 알고 있고 메시지가 revocable 확인 되 면 보안 &amp; 준수 센터 또는 Windows PowerShell을 사용 하 여 전자 메일을 해지할 수 있습니다.

보안 및 준수 센터를 사용 하 여 메시지를 해지 하려면 &amp;

1. 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 여 보안 & 준수 센터에 연결 합니다.

2. **암호화 보고서**의 메시지에 대 한 **세부 정보** 테이블에서 **메시지 취소**를 선택 합니다.

Windows PowerShell을 사용 하 여 전자 메일을 해지 하려면 OMEMessageRevocation cmdlet을 사용 합니다.

1. 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 [Exchange Online PowerShell에 연결](https://aka.ms/exopowershell)합니다.

2. 다음과 같이 OMEMessageRevocation cmdlet을 실행 합니다.

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. 전자 메일이 해지 되었는지 확인 하려면 다음과 같이 OMEMessageStatus cmdlet을 실행 합니다.

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    해지가 성공한 경우 cmdlet은 다음 결과를 반환 합니다.  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a>Office 365 고급 메시지 암호화에 대 한 추가 정보

- [Office 365 고급 메시지 암호화](ome-advanced-message-encryption.md)

- [Office 365 고급 메시지 암호화-전자 메일 만료](ome-advanced-expiration.md)

- [메시지 정책 및 규정 준수 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
