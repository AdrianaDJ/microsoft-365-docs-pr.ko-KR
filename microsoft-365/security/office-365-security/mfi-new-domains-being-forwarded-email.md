---
title: 전자 메일 인사이트가 전달되는 새 도메인
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: exchange-online
localization_priority: Normal
ms.assetid: ''
description: 관리자는 보안 & 준수 센터의 메일 흐름 대시보드를 통해 전달 되는 새 도메인을 사용 하 여 사용자가 전달 된 적이 없는 외부 도메인으로 메시지를 전달 하는 경우 조사를 진행 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: a72ffd001ea22972d9dc6c00af8a4dd7881386b7
ms.sourcegitcommit: 474bd6a86c3692d11fb2c454591c89029ac5bbd5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/19/2020
ms.locfileid: "49356958"
---
# <a name="new-domains-being-forwarded-email-insight-in-the-security--compliance-center"></a>보안 & 준수 센터에서 전자 메일을 전달 하는 새 도메인

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


특정 도메인의 외부 받는 사람에 게 전자 메일 메시지를 전달 해야 하는 올바른 비즈니스 이유가 있습니다. 그러나 조직의 사용자가 메시지를 도메인으로 전달 하기 시작 하는 경우, 즉 조직의 아무도 메시지를 전달 하지 않은 경우 (새 도메인) 의심 스러운 일입니다.

이 조건은 사용자 계정이 손상 되었음을 나타낼 수 있습니다. 계정이 손상 된 것으로 의심 되는 경우 [손상 된 전자 메일 계정에 응답](responding-to-a-compromised-email-account.md)을 참조 하세요.

**전달 되는 새 도메인** 이 [보안 & 준수 센터](https://protection.office.com) 에서는 조직의 사용자가 새 도메인으로 메시지를 전달 하는 경우 사용자에 게 알려 줍니다.

이 통찰력은 문제가 검색 된 경우에만 나타나며 [전달 보고서](view-mail-flow-reports.md#forwarding-report) 페이지에 표시 됩니다.

![전자 메일 인사이트가 전달되는 새 도메인](../../media/mfi-new-domains-being-forwarded.png)

위젯을 클릭 하면 전달 된 메시지에 대 한 자세한 내용을 확인할 수 있는 플라이 아웃이 표시 되며 [전달 보고서](view-mail-flow-reports.md#forwarding-report)에 대 한 링크를 포함 합니다.

![전달 되는 새 도메인을 클릭 한 후 표시 되는 세부 정보 플라이 아웃 전자 메일 통찰력](../../media/mfi-new-domains-being-forwarded-details.png)

**보고서** 대시보드 또는 사이트의 **최상위 insights & 추천** 영역에서 **모두 보기** 를 클릭 한 후에는이 세부 정보 페이지로 이동할 수도 있습니다 \> **Dashboard** <https://protection.office.com/insightdashboard> .

외부 도메인에 대 한 자동 메시지 전달을 방지 하려면 일부 또는 모든 외부 도메인에 대해 원격 도메인을 구성 합니다. 자세한 내용은 [Exchange Online에서 원격 도메인 관리](https://docs.microsoft.com/Exchange/mail-flow-best-practices/remote-domains/manage-remote-domains)를 참조 하세요.

## <a name="related-topics"></a>관련 항목

메일 흐름 대시보드의 다른 정보에 대 한 자세한 내용은 [Security & 준수 센터의 메일 흐름 정보](mail-flow-insights-v2.md)를 참조 하십시오.
