---
title: Office 365 메시지 암호화를 사용 하 여 중요 한 정보 유형 정책 만들기
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/28/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- Strat_O365_Enterprise
description: Office 365 메시지 암호화를 사용 하 여 조직에 대 한 중요 한 정보 유형 정책을 만드는 방법을 알아봅니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: bfc77fa88ff798f98d260682dfbdbdd57b17af69
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47545988"
---
# <a name="create-a-sensitive-information-type-policy-for-your-organization-using-message-encryption"></a>메시지 암호화를 사용 하 여 조직에 대 한 중요 한 정보 유형 정책 만들기

Exchange 메일 흐름 규칙 또는 DLP (데이터 손실 방지)를 사용 하 여 Office 365 메시지 암호화로 중요 한 정보 유형 정책을 만들 수 있습니다. Exchange 메일 흐름 규칙을 만들려면 EAC (Exchange 관리 센터) 또는 PowerShell을 사용할 수 있습니다.

## <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a>EAC에서 메일 흐름 규칙을 사용 하 여 정책을 만들려면

EAC (Exchange 관리 센터)에 로그인 하 고 **메일 흐름**  >  **규칙**으로 이동 합니다. 규칙 페이지에서 Office 365 메시지 암호화를 적용 하는 규칙을 만듭니다. 메시지 또는 첨부 파일에 특정 키워드나 중요 한 정보 유형이 있는 경우와 같은 조건을 기준으로 규칙을 만들 수 있습니다.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a>PowerShell에서 메일 흐름 규칙을 사용 하 여 정책을 만들려면

조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하 고, Windows PowerShell 세션을 시작 하 고, Exchange Online에 연결 합니다. 지침을 확인하려면 [Exchange Online PowerShell에 연결](https://aka.ms/exopowershell)을 참조하세요. New-transportrule cmdlet을 사용 하 여 정책을 만듭니다.

## <a name="example-mail-flow-rule-created-with-powershell"></a>PowerShell로 만든 메일 흐름 규칙 예제

PowerShell에서 다음 명령을 실행 하 여 전자 메일 또는 첨부 파일에 다음과 같은 중요 한 정보 유형이 포함 되어 있는 경우 *암호화 전용* 정책을 사용 하 여 조직 외부로 전송 된 전자 메일을 자동으로 암호화 하는 Exchange 메일 흐름 규칙을 만듭니다.

- ABA 라우팅 번호
- 신용 카드 번호
- DEA (약품 집행 기관) 번호
- 미국/영국 passport number
- 미국 은행 계좌 번호
- 미국 ITIN(개인 납세자 번호)
- 미국 SSN(사회 보험 번호)

```powershell
Set-IRMConfiguration -DecryptAttachmentForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

자세한 내용은 [설정-IRMConfiguration](https://docs.microsoft.com/powershell/module/exchange/set-irmconfiguration) 및 [new-transportrule](https://docs.microsoft.com/powershell/module/exchange/new-transportrule)를 참조 하세요.

## <a name="how-recipients-access-attachments"></a>받는 사람이 첨부 파일에 액세스 하는 방법

Microsoft에서 메시지를 암호화 하면 받는 사람은 암호화 된 전자 메일에 액세스 하 여 열 때 첨부 파일에 무제한으로 액세스할 수 있습니다.

## <a name="to-prepare-for-this-change"></a>이 변경 내용을 준비 하려면

해당 하는 최종 사용자 설명서 및 교육 자료를 업데이트 하 여 조직의 사용자가이 변경 내용을 준비할 수 있습니다. 다음 Office 365 메시지 암호화 리소스를 사용자와 적절 하 게 공유 합니다.

- [PC 용 Outlook에서 암호화 된 메시지 보내기, 확인 및 회신](https://support.microsoft.com/en-us/office/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Microsoft 365 Essentials Video: Office 메시지 암호화](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a>감사 로그에서 이러한 변경 내용을 확인 합니다.

Microsoft 365에서이 활동을 감사 하 고 관리자가 사용할 수 있도록 합니다. 이 작업은 ' New-New-transportrule ' 이며 보안 & 준수 센터의 감사 로그 검색에서 사용 하는 예제 감사 항목의 코드 조각이 아래에 있습니다.

```text
*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications"…etc.*
```

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a>중요 한 정보 유형 정책을 사용 하지 않도록 설정 하거나 사용자 지정 하려면

Exchange 메일 흐름 규칙을 만든 후에는 EAC (exchange 관리 센터)의 **메일 흐름**규칙으로 이동 하 여 [규칙을 사용 하지 않도록 설정 하거나 편집](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) 하  >  **Rules** 고 "*아웃 바운드 중요 한 전자 메일 암호화 (box 규칙을 초과*합니다." 규칙을 사용 하지 않도록 설정할 수 있습니다.
