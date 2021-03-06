---
title: DKIM으로 서명된 메시지의 유효성 검사 지원
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
ms.collection:
- M365-security-compliance
description: Exchange Online Protection 및 Exchange Online에서 DKIM 서명 된 메시지의 유효성 검사에 대해 자세히 알아보기
ms.openlocfilehash: e2e91fe426348487fa4dfa8ef929d2d8129ffddc
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48202140"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>DKIM으로 서명된 메시지의 유효성 검사 지원

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


EOP (exchange Online Protection) 및 Exchange Online은[Dkim](https://www.rfc-editor.org/rfc/rfc6376.txt)(Domain Keys 식별 메일) 메시지의 인바운드 유효성 검사를 지원 합니다. DKIM은 메시지가 원래 있었던 도메인에서 보낸 것 이며 다른 사용자에 의해 위장 되지 않았음을 검사 하는 방법입니다. 전자 메일 메시지를 발송을 담당 하는 조직에 전달 합니다. DKIM 확인은 IPv6 통신을 통해 전송 되는 모든 메시지에 자동으로 사용 됩니다. 또한 Microsoft 365에서는 이제 IPv4를 통해 메일을 보내는 경우 DKIM을 지원 합니다. IPv6 지원에 대 한 자세한 내용은 IPv6을 [통한 익명 인바운드 전자 메일 메시지 지원](support-for-anonymous-inbound-email-messages-over-ipv6.md)를 참조 하세요.

DKIM은 메시지 헤더의 DKIM 서명 헤더에 표시되는 디지털 서명된 메시지의 유효성을 검사합니다. DKIM 서명 유효성 검사의 결과는 RFC 7001([메시지 인증 상태를 나타내는 메시지 헤더 필드](https://www.rfc-editor.org/rfc/rfc7001.txt))을 준수하는 Authentication-Results 헤더에 스탬프 처리됩니다. 메시지 헤더 텍스트는 다음과 같이 표시됩니다. 여기서는 contoso.com이 보낸 사람입니다.

 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`

관리자는 DKIM 유효성 검사의 결과에 Exchange [메일 흐름 규칙](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (전송 규칙이 라고도 함)을 만들어 필요에 따라 메시지를 필터링 하거나 라우팅할 수 있습니다.
