---
title: EOP의 메일 흐름 규칙
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9c2cf227-eff7-48ef-87fb-487186e47363
description: 메일 흐름 규칙 (전송 규칙)을 사용 하 여 조직을 통과 하는 메시지를 식별 하 고이에 대 한 조치를 취할 수 있습니다.
ms.openlocfilehash: 11bf2af56c6e85c868e2e0726736f624e196805c
ms.sourcegitcommit: 9546708a5506fdbadbfe2500cbf1bd1aeaec6fcb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/13/2020
ms.locfileid: "49021052"
---
# <a name="mail-flow-rules-transport-rules-in-standalone-eop"></a>독립형 EOP 메일 흐름 규칙(전송 규칙)

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


Exchange Online 사서함이 없는 독립 실행형 EOP (Exchange Online Protection) 조직에서 메일 흐름 규칙 (전송 규칙이 라고도 함)을 사용 하 여 조직에서 진행 되는 메시지를 식별 하 고 작업을 수행할 수 있습니다.

이 항목에서는 메일 흐름 규칙의 구성 요소와 작동 방식을 설명 합니다.

메일 흐름 규칙을 만들고 복사 하 고 관리 하는 방법에 대 한 자세한 내용은 [Exchange Online에서 메일 흐름 규칙 관리](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules)를 참조 하십시오. 각 규칙에 대해 규칙을 적용하거나, 규칙을 테스트하거나, 규칙을 테스트하고 보낸 사람에게 알릴 수 있는 옵션이 제공됩니다. 테스트 옵션에 대 한 자세한 내용은 [Exchange Online에서](https://docs.microsoft.com/exchange/security-and-compliance/data-loss-prevention/policy-tips) [메일 흐름 규칙](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/test-mail-flow-rules) 및 정책 팁 테스트를 참조 하십시오.

메일 흐름 규칙과 일치 하는 메시지에 대 한 요약 및 세부 보고서를 보려면 [메일 보호 보고서를 사용 하 여 맬웨어, 스팸 및 규칙 감지에 대 한 데이터 보기](https://docs.microsoft.com/exchange/monitoring/use-mail-protection-reports)를 참조 하세요.

메일 흐름 규칙을 사용해서 특정 메시징 정책을 실행하려면 다음 항목을 참조하세요.

- [메일 흐름 규칙을 사용 하 여 Exchange Online의 메시지 첨부 파일 검사](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments)

- [Office 365 Enterprise의 암호화 설정](../../compliance/set-up-encryption.md)

- [Exchange Online의 조직 전체 메시지 법적 고 지 사항, 서명, 바닥글 또는 헤더](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/disclaimers-signatures-footers-or-headers)

- [메일 흐름 규칙을 사용하여 메시지의 스팸 신뢰 수준(SCL) 설정](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)

- [EOP에서 수신 거부 목록 만들기](create-block-sender-lists-in-office-365.md)

- [Exchange Online Protection의 첨부 파일 차단을 통해 맬웨어 위협 줄이기](reducing-malware-threats-through-file-attachment-blocking-in-exchange-online-pro.md)

- [Office 365에서 전자 메일 메시지를 암호화 하거나 암호를 해독 하는 규칙 정의](https://docs.microsoft.com/microsoft-365/compliance/define-mail-flow-rules-to-encrypt-email)

다음 비디오에서는 독립 실행형 EOP에서 메일 흐름 규칙을 설정 하는 방법을 보여 줍니다.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/7cdcd2cb-9382-4065-98e1-81257b32a189?autoplay=false]

## <a name="mail-flow-rule-components"></a>메일 흐름 규칙 구성 요소

메일 흐름 규칙은 조건, 예외, 작업 및 속성으로 구성 됩니다.

- **조건** : 작업을 적용할 메시지를 식별 합니다. 일부 조건은 받는 사람, 보낸 사람 또는 참조 필드와 같은 메시지 헤더 필드를 검사 합니다. 다른 조건은 메시지 제목, 본문, 첨부 파일, 메시지 크기 또는 메시지 분류와 같은 message 속성을 검사 합니다. 대부분의 경우 비교 연산자 (예: 같음, 같지 않음, 포함 하지 않음)와 일치 하는 값을 지정 해야 합니다. 조건이 나 예외가 없으면 규칙이 모든 메시지에 적용 됩니다.

독립 실행형 EOP의 메일 흐름 규칙 조건에 대 한 자세한 내용은 [Exchange Online의 메일 흐름 규칙 조건 및 예외 (조건자)](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)를 참조 하십시오.

- **예외** : 선택적으로 작업을 적용할 수 없는 메시지를 식별 합니다. 조건에서 사용할 수 있는 동일한 메시지 식별자를 예외에서도 사용할 수 있습니다. 예외는 조건을 재정의하며, 메시지가 구성된 모든 조건과 일치하더라도 규칙 작업이 메시지에 적용되지 않도록 합니다.

- **작업** : 규칙의 조건과 일치 하 고 예외와는 일치 하지 않는 메시지에 수행할 작업을 지정 합니다. 예외는 조건보다 우선하며, 메시지가 모든 조건과 일치하더라도 작업이 전자 메일 메시지에 적용되지 않도록 합니다.

독립 실행형 EOP에서 사용할 수 있는 메일 흐름 규칙 작업에 대 한 자세한 내용은 [mail flow rule actions In Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)을 참조 하십시오.

- **속성** : 조건, 예외 또는 작업이 아닌 다른 규칙 설정을 지정 합니다. 예를 들어, 규칙이 적용되는 시기, 규칙 적용 또는 테스트 여부, 규칙이 활성화되는 시기를 지정합니다.

  자세한 내용은이 항목의 [메일 흐름 규칙 속성](#mail-flow-rule-properties) 섹션을 참조 하십시오.

### <a name="multiple-conditions-exceptions-and-actions"></a>여러 조건, 예외 및 작업

Use a transport rule so messages can bypass Clutter

****

|구성 요소|추가한|설명|
|---|---|---|
|설명|그리고|메시지는 규칙의 모든 조건과 일치해야 합니다. 하나의 조건 또는 다른 조건과 일치해야 하는 경우 각 조건에 대해 별도의 규칙을 사용합니다. 예를 들어 첨부 파일이 있는 메시지와 특정 텍스트가 포함 된 메시지에 같은 고 지 사항을 추가 하려면 각 조건에 대해 규칙을 하나씩 만듭니다. EAC에서는 규칙을 쉽게 복사할 수 있습니다.|
|메시지는 규칙의 모든 조건과 일치해야 합니다. 하나의 조건 또는 다른 조건과 일치해야 하는 경우 각 조건에 대해 별도의 규칙을 사용합니다. 예를 들어 패턴과 일치하는 콘텐츠가 있는 메시지 및 첨부 파일이 있는 메시지에 동일한 고지 사항을 추가하려면 각 조건에 대해 하나의 규칙을 만듭니다. 규칙은 쉽게 복사할 수 있습니다.|또는|일부 조건에는 둘 이상의 값을 지정할 수 있습니다. 이 메시지는 지정 된 값 중 하 나와 일치 하는 것이 아닌 모든 항목 중 하나 여야 합니다. 예를 들어 전자 메일 메시지에 제목 주식 가격 정보가 있고 **제목에 다음 단어 중** 하나가 Contoso 또는 Stock과 일치 하도록 구성 되어 있으면 주체에 지정 된 값이 하나 이상 포함 되므로 조건이 충족 됩니다.|
|일부 조건에는 둘 이상의 값을 지정할 수 있습니다. 여러 개의 값을 입력할 수 있는 조건의 경우 메시지가 해당 조건에 대해 지정된 값 중 하나에만 일치하면 됩니다. 예를 들어 전자 메일 메시지의 제목이 주가 정보이고 제목에 다음 단어 포함 조건이 Contoso 또는 주가라는 단어와 일치하도록 구성된 경우 조건 값 중 적어도 하나가 제목에 포함되어 있으므로 조건이 충족됩니다.|또는|메시지가 예외 중 하 나와 일치 하는 경우 해당 작업은 메시지에 적용 되지 않습니다. 메시지는 모든 예외와 일치 하지 않아도 됩니다.|
|예외 중 하나라도 메시지와 일치하면 작업은 처리되지 않습니다. 메시지가 모든 예외와 일치할 필요는 없습니다.|그리고|규칙 조건과 일치 하는 메시지는 규칙에 지정 된 모든 작업을 받습니다. 예외는 조건과 정반대의 방식으로 처리됩니다. <p> 규칙 조건에 일치하는 메시지에는 규칙에 지정된 모든 작업이 적용됩니다. 예를 들어, 메시지 제목 앞에 다음 추가 및 숨은 참조란에 받는 사람 추가 작업을 선택한 경우 두 작업 모두 메시지에 적용됩니다. 즉, 지정된 문자열이 메시지 제목 앞에 붙고 지정된 받는 사람이 숨은 참조로 추가됩니다.<p> 규칙이 적용 될 때 후속 규칙이 메시지에 적용 되지 않도록 규칙에 대해 작업을 설정할 수도 있습니다.|
|

### <a name="mail-flow-rule-properties"></a>메일 흐름 규칙 속성

다음 표에는 메일 흐름 규칙에서 사용할 수 있는 규칙 속성에 대 한 설명이 나와 있습니다.

****

|EAC의 속성 이름|PowerShell의 매개 변수 이름|설명|
|---|---|---|
|**우선 순위**|_우선 순위_|규칙이 메시지에 적용 되는 순서를 나타냅니다. 기본 우선 순위는 규칙을 만든 시기 (이전 규칙은 새 규칙 보다 우선 순위가 높고 우선 순위 규칙의 우선 순위가 낮은 규칙 보다 높음)에 따라 달라 집니다. <p> 규칙 목록에서 규칙을 위나 아래로 이동 하 여 EAC에서 규칙 우선 순위를 변경 합니다. PowerShell에서는 우선 순위 번호 (우선 순위가 가장 높은 값)를 설정 합니다. <p> 예를 들어 신용 카드 번호가 포함된 메시지는 거부하는 규칙과 승인을 요구하는 또 다른 규칙이 있을 때 거부 규칙이 먼저 적용되도록 한 다음 다른 규칙이 적용되지 않도록 할 수 있습니다.  |
|**Mode**|_Mode_|규칙에서 즉시 메시지를 처리 하도록 시작할지, 아니면 메시지 배달에 영향을 주지 않고 (즉, 데이터 손실 방지 또는 DLP 정책 팁을 포함 하거나 제외 하 여 규칙을 테스트할 지를 지정할 수 있습니다.) <p> 정책 팁은 Outlook 또는 웹용 Outlook에 메시지를 만드는 사용자에 게 가능한 정책 위반에 대 한 정보를 제공 하는 간략 한 메모를 표시 합니다. 자세한 내용은 **정책 팁** 을 참조하세요. <p> 모드에 대 한 자세한 내용은 **Test a mail flow rule을** 참조 하십시오.|
|**다음 날짜에이 규칙 활성화** <p> **다음 날짜에이 규칙 비활성화**|_ActivationDate_ <p> _ExpiryDate_|규칙이 활성화 되는 날짜 범위를 지정 합니다.|
|**설정** 확인란 선택 또는 선택 되지 않음|새 규칙: **new-transportrule** Cmdlet에서 Enabled 매개 변수를 _사용_ 합니다. <p> 기존 규칙: **new-transportrule** 또는 **Disable-New-transportrule** cmdlet을 사용 합니다. <p> 이 값은 규칙의 **State** 속성에 표시 됩니다.|사용 하지 않도록 설정 된 규칙을 만들고 테스트할 준비가 되 면 사용 하도록 설정할 수 있습니다. 또는 규칙을 삭제 하지 않고 사용 하지 않도록 설정 하 여 설정을 보존할 수 있습니다.|
|**규칙 처리가 완료 되지 않으면 메시지 연기**|_RuleErrorAction_|규칙 처리를 완료할 수 없는 경우 메시지를 처리할 방법을 지정할 수 있습니다. 기본적으로 규칙은 무시 되지만 처리를 위해 메시지를 다시 전송 하도록 선택할 수 있습니다.|
|**메시지의 보낸 사람 주소와 일치**|_SenderAddressLocation_|규칙에서 보낸 사람의 전자 메일 주소를 검사 하는 조건이 나 예외를 사용 하는 경우 메시지 헤더, 메시지 봉투 또는 둘 다에 있는 값을 찾을 수 있습니다.|
|**추가 규칙 처리 중지**|_SenderAddressLocation_|이 작업은 규칙에 대 한 작업이 며 EAC의 속성 처럼 표시 됩니다. 규칙이 메시지를 처리 한 후에는 메시지에 추가 규칙을 적용 하지 않도록 선택할 수 있습니다.|
|**Comments**|_Comments_|규칙에 대 한 설명을 입력할 수 있습니다.|
|

## <a name="how-mail-flow-rules-are-applied-to-messages"></a>메시지에 메일 흐름 규칙을 적용 하는 방법

조직에서 흐르는 모든 메시지는 조직에서 사용 하도록 설정 된 메일 흐름 규칙을 기준으로 평가 됩니다. 규칙은 EAC의 **메일 흐름** 규칙 페이지에 나열 된 순서에 \> **Rules** 따라 처리 되거나 PowerShell의 해당 _Priority_ 매개 변수 값에 기반 합니다.

조직의 모든 메시지가 조직에 대해 사용하도록 설정된 전송 규칙을 기준으로 평가됩니다. 규칙은 EAC의 규칙 페이지에 표시된 순서 또는 exsdkExMSH의 Priority 매개 변수 값에 따라 처리됩니다.  이 설정은 여러 메일 흐름 규칙 (메시지에 적용 하려는 규칙)의 조건과 일치 하는 메시지에 중요 합니다. 모든? 단 1?

### <a name="differences-in-processing-based-on-message-type"></a>메시지 유형에 따른 처리 방식의 차이

조직을 통과하는 메시지 유형에는 몇 가지가 있습니다. 다음 표에는 메일 흐름 규칙에서 처리할 수 있는 메시지 유형이 나와 있습니다.

****

|조직을 통과하는 메시지 유형에는 몇 가지가 있습니다. 다음 표에는 전송 규칙으로 처리될 수 있는 메시지 유형이 나와 있습니다.|메시지 유형|
|---|---|
|**일반 메시지** : 단일 rtf (서식 있는 텍스트), HTML 또는 일반 텍스트 메시지 본문 또는 여러 부분으로 된 메시지 본문이 나 대체 문자 집합을 포함 하는 메시지입니다.|예|
|**Office 365 메시지 암호화** : Office 365 메시지 365 암호화로 암호화 된 메시지 자세한 내용은 [Office 365의 암호화](https://docs.microsoft.com/microsoft-365/compliance/encryption)를 참조하세요.|규칙은 항상 해당 헤더를 검사 하는 조건에 따라 봉투 헤더에 액세스 하 고 메시지를 처리할 수 있습니다. <p> 암호화 된 메시지의 내용을 조사 하거나 수정 하는 규칙의 경우 전송 암호 해독이 사용 하도록 설정 되어 있는지 확인 해야 합니다 (필수 또는 선택 사항, 기본값은 선택 사항). 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 하거나 암호를 해독 하는 규칙 정의](https://docs.microsoft.com/microsoft-365/compliance/define-mail-flow-rules-to-encrypt-email)를 참조 하세요.|
|**S/MIME 암호화 메시지**|규칙은 해당 헤더를 검사 하는 조건에 따라 봉투 머리글만 액세스 하 고 메시지를 처리할 수만 있습니다. <p> 메시지의 콘텐츠를 검사 해야 하는 조건이 포함 된 규칙이 나 메시지의 내용을 수정 하는 작업은 처리할 수 없습니다.|
|**Rms 보호 메시지** : AD Rms (Active Directory Rights management Services) 또는 RMS (Azure 권한 관리) 정책이 적용 된 메시지입니다.|규칙은 항상 해당 헤더를 검사 하는 조건에 따라 봉투 헤더에 액세스 하 고 메시지를 처리할 수 있습니다. <p> RMS 보호 메시지의 내용을 조사 하거나 수정 하는 규칙은 전송 암호 해독이 사용 하도록 설정 되어 있는지 확인 해야 합니다 (필수 또는 선택 사항, 기본값은 선택 사항).|
|**일반 텍스트 서명 메시지** : 서명 되었지만 암호화 되지 않은 메시지입니다.|예|
|**UM 메시지** : 음성 메일, 팩스, 부재 중 전화 알림, Microsoft Outlook voice Access를 사용 하 여 만들었거나 전달 된 메시지 등 통합 메시징 서비스에서 만들거나 처리 한 메시지입니다.|예|
|**익명 메시지** : 익명 보낸 사람이 보낸 메시지입니다.|예|
|**보고서 읽기** : 보낸 사람에의 한 읽음 확인 요청에 따라 생성 되는 보고서입니다. 읽기 보고서에는 또는의 메시지 클래스가 포함 `IPM.Note*.MdnRead` `IPM.Note*.MdnNotRead` 됩니다.|예|
|

## <a name="what-else-should-i-know"></a>더 알아야 할 것은 무엇입니까?

- 규칙에 대 한 **version** 또는 **ruleversion** 속성 값은 Exchange Online Protection에서 중요 하지 않습니다.

- 메일 흐름 규칙을 만들거나 수정한 후 새 규칙이 나 업데이트 된 규칙을 메시지에 적용 하는 데 최대 30 분이 걸릴 수 있습니다.

## <a name="for-more-information"></a>자세한 내용

[메일 흐름 규칙을 사용 하 여 Exchange Online의 메시지 첨부 파일 검사](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments)

[Office 365의 전자 메일 암호화](../../compliance/email-encryption.md)

[저널, 전송 및 받은 편지함 규칙 제한](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#journal-transport-and-inbox-rule-limits)
