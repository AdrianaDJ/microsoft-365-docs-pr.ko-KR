---
title: Office 365 고급 메시지 암호화로 암호화 된 전자 메일의 만료 날짜 설정
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/8/2019
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Office 365 Advanced Message Encryption을 사용 하 여 사용자 지정 브랜드 서식 파일을 통해 전자 메일에 만료 날짜를 설정 하 여 이메일 보안을 확장할 수 있습니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: bbd018e55592e5b17149edf1a4dc0907c0184417
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769168"
---
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a>Office 365 고급 메시지 암호화로 암호화 된 전자 메일의 만료 날짜 설정

Office 365 Advanced Message Encryption은 [microsoft 365 Enterprise e5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (비영리 스태프 가격), Office 365 Enterprise E5 (비영리 스태프 가격) 및 Office 365 교육용 A5에 포함 되어 있습니다. 조직에서 Office 365 고급 메시지 암호화를 포함 하지 않는 구독을 사용 하는 경우 microsoft 365 E3, microsoft 365 E3 (비영리 직원 가격) 또는 Microsoft 365 (고급 규정 준수) 용 microsoft 365 e3, Microsoft 365 E3 (비영리 스태프 가격) 또는 Office 365 Sku에 대 한 Office 준수 sku 추가 기능을 사용해 서 구매할 수 있습니다.

사용자가 OME 포털을 사용 하 여 암호화 된 전자 메일에 액세스 하는 외부의 받는 사람에 게 보내는 전자 메일에 메시지 만료를 사용할 수 있습니다. Windows PowerShell에서 만료 날짜를 지정 하는 사용자 지정 브랜드 서식 파일을 사용 하 여 조직에서 보낸 암호화 된 전자 메일을 보고 회신할 때 받는 사람이 OME 포털을 사용 하도록 강제 합니다.

Office 365 전역 관리자는 회사 브랜드를 적용 하 여 조직의 전자 메일 메시지 모양을 사용자 지정할 때 이러한 전자 메일 메시지에 대 한 만료를 지정할 수도 있습니다. Office 365 고급 메시지 암호화를 사용 하면 조직에서 보낸 암호화 된 전자 메일용 템플릿을 여러 개 만들 수 있습니다. 서식 파일을 사용 하면 받는 사람에 게 사용자가 보낸 메일에 대 한 액세스 권한이 있는 기간을 제어할 수 있습니다.

최종 사용자가 만료 날짜가 설정 된 메일을 받는 경우 사용자는 래퍼 전자 메일에서 만료 날짜를 볼 수 있습니다. 사용자가 만료 된 메일을 열려고 하면 OME 포털에 오류가 표시 됩니다.

전자 메일에 대 한 만료 날짜만 외부 받는 사람으로 설정할 수 있습니다.

Office 365 고급 메시지 암호화를 사용 하 여 사용자 지정 브랜딩을 적용할 때마다 Office 365에서 해당 래퍼를 서식 파일을 적용 하는 메일 흐름 규칙에 맞는 전자 메일에 적용 합니다. 또한 사용자 지정 브랜딩을 사용 하는 경우에만 만료를 사용할 수 있습니다.

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a>PowerShell을 사용 하 여 메일 만료를 적용 하는 사용자 지정 브랜딩 서식 파일 만들기

1. 조직에서 전역 관리자 권한이 있는 계정을 사용 하 여 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) 합니다.

2. New-OMEConfiguration cmdlet을 실행 합니다.

    ```powershell
    New-OMEConfiguration -Identity "Expire in 7 days" -ExternalMailExpiryInDays 7
    ```

여기서,

- `Identity` 은 사용자 지정 서식 파일의 이름입니다.

- `ExternalMailExpiryInDays` 받는 사람이 만료 되기 전에 메일을 보관할 수 있는 기간 (일)을 식별 합니다. 1 – 730 일 사이에 임의의 값을 사용할 수 있습니다.

## <a name="more-information-about-office-365-advanced-message-encryption"></a>Office 365 고급 메시지 암호화에 대 한 추가 정보

- [Office 365 고급 메시지 암호화](ome-advanced-message-encryption.md)

- [Office 365 고급 메시지 암호화로 암호화된 전자 메일 취소](revoke-ome-encrypted-mail.md)

- [메시지 정책 및 규정 준수 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
