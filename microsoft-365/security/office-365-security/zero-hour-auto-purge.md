---
title: 제로 시간 자동 제거 (ZAP)
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: 관리자는 0 시간 자동 삭제 (ZAP)가 Exchange Online 사서함의 배달 된 메시지를 retroactively에서 정크 메일 폴더로 이동 하는 것을 retroactively 수 있는 격리 또는 피싱 인 것으로 확인 하는 방법에 대해 알아볼 수 있습니다.
ms.openlocfilehash: fd5186bc40d2d80097e6292d86ea113a41e0dd52
ms.sourcegitcommit: ce46d1bd67091d4ed0e2b776dfed55e2d88cdbf4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49131152"
---
# <a name="zero-hour-auto-purge-zap-in-exchange-online"></a>Exchange Online에서 제로 시간 자동 제거 (ZAP)

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


## <a name="basic-features-of-zap"></a>ZAP의 기본 기능

Exchange Online의 사서함이 있는 Microsoft 365 조 직에서 제로 시간 자동 삭제 (ZAP)는 retroactively에서 Exchange Online 사서함으로 이미 배달 된 악의적인 피싱, 스팸 또는 맬웨어 메시지를 검색 하 고 neutralizes 하는 전자 메일 보호 기능입니다.

온-프레미스 Exchange 사서함을 보호 하는 독립 실행형 EOP (Exchange Online Protection) 환경에서는 ZAP이 작동 하지 않습니다.

## <a name="how-zap-works"></a>ZAP 작동 방식

스팸 및 맬웨어 서명은 서비스에서 매일 실시간으로 업데이트 됩니다. 그러나 사용자에 게 콘텐츠를 배달 한 후에 weaponized를 포함 하 여 여러 가지 이유로 인해 여전히 악의적인 메시지를 받을 수 있습니다. ZAP은 서비스의 스팸 및 맬웨어 서명에 대 한 업데이트를 지속적으로 모니터링 하 여이 문제를 해결 합니다. ZAP은 이미 사용자의 사서함에 있는 메시지를 찾아 제거할 수 있습니다.

사용자가 ZAP 작업을 원활 하 게 수행할 수 있습니다. 메시지를 검색 하 고 이동한 경우 알림을 받지 않습니다.

[수신 허용-보낸 사람 목록](create-safe-sender-lists-in-office-365.md), 메일 흐름 규칙 (전송 규칙이 라고도 함), 받은 편지함 규칙 또는 추가 필터는 ZAP 보다 우선적으로 적용 됩니다. 메일 흐름에서와 마찬가지로 서비스에서 전달 된 메시지의 ZAP이 결정 되는 경우에도 수신 허용-보낸 사람 구성으로 인해 메시지가 처리 되지 않습니다. 이는 필터링을 우회 하도록 메시지를 구성 하는 경우에 주의 해야 할 또 다른 이유입니다.

### <a name="malware-zap"></a>맬웨어 ZAP

배달 후 맬웨어가 포함 되는 것으로 확인 된 **읽음 또는 읽지 않은 메시지** 에 대해 ZAP 설정별가 맬웨어 첨부 파일을 포함 하는 메시지를 표시 합니다. 관리자만 격리에서 맬웨어 메시지를 보고 관리할 수 있습니다.

맬웨어 ZAP은 맬웨어 방지 정책에서 기본적으로 사용 하도록 설정 됩니다. 자세한 내용은 [EOP에서 맬웨어 방지 정책 구성을](configure-anti-malware-policies.md)참조 하세요.

### <a name="phish-zap"></a>피싱 ZAP

배달 후에 피싱으로 식별 된 **읽음 또는 읽지 않은 메시지** 의 경우 ZAP 결과는 해당 하는 스팸 방지 정책에서 **피싱 전자 메일** 필터링 결과에 대해 구성 된 작업에 따라 달라 집니다. 다음 목록에는 피싱에 대 한 사용 가능한 필터링 결과 작업 및 가능한 ZAP 결과에 대 한 설명이 나와 있습니다.

- **X-헤더 추가**( **제목 줄 앞에 텍스트 포함**): ZAP이 메시지에 대해 작업을 수행 하지 않습니다.

- **정크 메일로 메시지 이동**: ZAP 사서함에서 정크 메일 규칙을 사용 하는 경우 (기본적으로 사용 하도록 설정 되어 있음) 메시지를 정크 메일 폴더로 이동 합니다. 자세한 내용은 [Microsoft 365에서 Exchange Online 사서함의 정크 메일 설정 구성을](configure-junk-email-settings-on-exo-mailboxes.md)참조 하세요.

- **전자 메일 주소로 메시지 리디렉션**, **메시지 삭제**, **격리 메시지**: ZAP 설정별 메시지

기본적으로 스팸 방지 정책에서 피싱 ZAP을 사용 하도록 설정 되어 있으며 **피싱 전자 메일** 필터링 결과의 기본 작업은 **메시지를 격리** 하며,이는 메시지를 기본적으로 피싱 ZAP 설정별 한다는 것을 의미 합니다.

스팸 필터링 verdicts 구성에 대 한 자세한 내용은 [Microsoft 365에서 스팸 방지 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요.

### <a name="spam-zap"></a>스팸 ZAP

배달 후 스팸으로 식별 된 **읽지 않은 메시지** 의 경우 ZAP 결과는 해당 하는 스팸 방지 정책에서 **스팸** 필터링 결과에 대해 구성 된 작업에 따라 달라 집니다. 스팸 및 가능한 ZAP 결과에 대 한 사용 가능한 필터링 결과 작업은 다음 목록에 설명 되어 있습니다.

- **X-헤더 추가**( **제목 줄 앞에 텍스트 포함**): ZAP이 메시지에 대해 작업을 수행 하지 않습니다.

- **정크 메일로 메시지 이동**: ZAP 사서함에서 정크 메일 규칙을 사용 하는 경우 (기본적으로 사용 하도록 설정 되어 있음) 메시지를 정크 메일 폴더로 이동 합니다. 자세한 내용은 [Microsoft 365에서 Exchange Online 사서함의 정크 메일 설정 구성을](configure-junk-email-settings-on-exo-mailboxes.md)참조 하세요.

- **전자 메일 주소로 메시지 리디렉션**, **메시지 삭제**, **격리 메시지**: ZAP 설정별 메시지 최종 사용자는 자신의 스팸 격리 된 메시지를 보고 관리할 수 있습니다.

기본적으로 스팸 방지 정책에서 스팸 ZAP을 사용 하도록 설정 되어 있으며 스팸 필터링 결과의 기본 작업은 **정크 메일 폴더로 메시지를 이동** 하는 것으로 **, 스팸 zap** 은 **읽지 않은** 메시지를 정크 메일 폴더로 이동 합니다.

스팸 필터링 verdicts 구성에 대 한 자세한 내용은 [Microsoft 365에서 스팸 방지 정책 구성을](configure-your-spam-filter-policies.md)참조 하세요.

### <a name="zap-considerations-for-microsoft-defender-for-office-365"></a>Microsoft Defender for Office 365의 ZAP 고려 사항

ZAP은 안전한 첨부 파일 검색에서 [동적 배달](atp-safe-attachments.md#dynamic-delivery-in-safe-attachments-policies) 프로세스에 있는 메시지를 격리 하지 않으며, EOP 맬웨어 필터링이 이미 해당 첨부 파일을 **맬웨어 경고 Text.txt** 파일로 바꾸었습니다. 이러한 유형의 메시지에 대해 피싱 또는 스팸 신호를 수신 하 고 스팸 방지 정책의 필터링 결과 메시지에 대 한 특정 작업을 수행 하도록 설정 된 경우 (정크로 이동, 리디렉션, 삭제 또는 격리), ZAP은 ' 정크로 이동 ' 작업을 기본으로 합니다.

## <a name="how-to-see-if-zap-moved-your-message"></a>메시지가 ZAP에서 이동 된 것을 확인 하는 방법

ZAP이 메시지를 이동 했는지 확인 하려면 [위협 방지 상태 보고서](view-email-security-reports.md#threat-protection-status-report) 또는 [위협 탐색기 (및 실시간 검색)](threat-explorer.md)를 사용할 수 있습니다. 시스템 작업으로, ZAP이 Exchange 사서함 감사 로그에 기록 되지 않습니다.

## <a name="zap-faq"></a>ZAP FAQ

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-email-folder"></a>합법적인 메시지를 정크 메일 폴더로 이동 하면 어떻게 되나요?

[가양성](report-junk-email-messages-to-microsoft.md)에 대 한 일반적인 보고 프로세스를 따라야 합니다. 메시지를 받은 편지함에서 정크 메일 폴더로 이동 하는 유일한 이유는 서비스가 스팸 또는 악성 메시지를 받는 것으로 확인 되었기 때문입니다.

### <a name="what-if-i-use-the-quarantine-folder-instead-of-the-junk-mail-folder"></a>정크 메일 폴더 대신 Quarantine 폴더를 사용 하는 경우에는 어떻게 하나요?

ZAP은이 항목의 앞부분에서 설명한 스팸 방지 정책 구성을 기반으로 하는 메시지에 대해 작업을 수행 합니다.

### <a name="what-if-im-using-safe-senders-mail-flow-rules-or-allowedblocked-sender-lists"></a>수신 허용-보낸 사람, 메일 흐름 규칙 또는 허용/차단 된 보낸 사람 목록을 사용 하는 경우

수신 허용-보낸 사람, 메일 흐름 규칙 또는 차단 및 조직 설정 허용이 우선적으로 적용 됩니다. 서비스에서 구성 된 작업을 수행 하는 중 이므로 이러한 메시지는 ZAP에서 제외 됩니다. 이는 필터링을 우회 하도록 메시지를 구성 하는 경우에 주의 해야 할 또 다른 이유입니다.

### <a name="what-if-a-message-is-moved-to-another-folder-eg-inbox-rules"></a>다른 폴더 (예: 받은 편지함 규칙)로 메시지를 이동 하는 경우

메시지가 삭제 되지 않았거나, 동일 하거나 더 강력 하지만 작업이 아직 적용 되지 않은 경우에도 ZAP이 계속 작동 합니다. 예를 들어 피싱 방지 정책이 격리로 설정 되어 있고 메시지가 이미 정크 메일에 있는 경우에는 ZAP에서 메시지를 격리 하는 작업을 수행 합니다.

### <a name="how-does-zap-affect-mailboxes-on-hold"></a>ZAP이 보류 중인 사서함에 어떤 영향을 줍니까?

ZAP은 보류 중인 사서함에서 메시지를 격리 하지 않습니다. 스팸 방지 정책에서 스팸 또는 피싱 결과에 대해 구성 된 작업을 기반으로 메시지를 정크 메일 폴더로 이동할 수 있습니다.

Exchange Online의 보류에 대 한 자세한 내용은 [Exchange online의 원본 위치 유지 및 소송 보존](https://docs.microsoft.com/Exchange/security-and-compliance/in-place-and-litigation-holds)을 참조 하세요.
