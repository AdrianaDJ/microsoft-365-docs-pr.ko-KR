---
title: 메일 흐름 대시보드의 상위 도메인 메일 흐름 상태 이해
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: 관리자는 MX 레코드와 관련 된 메일 흐름 문제를 해결 하기 위해 보안 & 준수 센터의 메일 흐름 대시보드에서 최상위 도메인 메일 흐름 상태 정보를 사용 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: 0d750ab4dbe5875796118086fae1d9119dc486f0
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48920587"
---
# <a name="top-domain-mail-flow-status-insight-in-the-security--compliance-center"></a>보안 & 준수 센터의 상위 도메인 메일 흐름 상태 이해

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


[보안 & 준수 센터](https://protection.office.com) 의 [메일 흐름 대시보드의](mail-flow-insights-v2.md) **최상위 도메인 메일 흐름 상태** 에 대 한 정보는 조직의 현재 메일 흐름 상태를 제공 합니다.

이러한 통찰력은 * *_메일 흐름_* _ 문제가 발생 하는 도메인을 식별 하 고 문제를 해결 하는 데 도움이 됩니다. 예를 들어 도메인이 만료 되었거나 도메인에 잘못 된 MX 레코드가 있기 때문에 도메인에서 외부 전자 메일을 받을 수 없습니다.

![보안 & 준수 센터의 메일 흐름 대시보드의 상위 도메인 흐름 상태 위젯](../../media/mfi-top-domain-mail-flow-status-widget.png)

위젯에 *자세히 보기* *를 클릭 하면 각 도메인의 상태에 대 한 세부 정보를 보여 주는 **도메인 상태** 플라이 아웃이 나타납니다.

- **도메인**
- **이전 MX 레코드**
- **현재 MX 레코드**
- **전자 메일 수신 상태**
- **도메인 상태** : 녹색 확인 표시는 현재 MX 레코드 (위젯을 클릭 한 시점)가 record에 대해 수행한 값과 일치 하 고, 지난 2 시간 동안 도메인에서 전자 메일을 받은 것을 나타냅니다.

  빨간색 X는 MX 레코드가 변경 되었으며 도메인에서 지난 6 시간 동안 전자 메일을 받은 것을 나타냅니다. 이는 사용자의 도메인이 만료 되었거나 MX 레코드가 잘못 업데이트 되었음을 나타내는 것일 수 있습니다. 도메인 등록 기관 또는 DNS 호스팅 서비스에 문의 하 여 도메인의 사용 기간이 만료 되었는지 여부 또는 도메인의 MX 레코드가 올바르지 않은 지 확인 합니다.

더 많은 도메인에 대 한 동일한 정보를 보려면 **자세히 보기** 를 클릭 하면 됩니다.

![상위 도메인 메일 흐름 상태 이해의 세부 정보 플라이 아웃](../../media/mfi-top-domain-mail-flow-status-view-details.png)

## <a name="see-also"></a>참고 항목

메일 흐름 대시보드의 다른 정보에 대 한 자세한 내용은 [Security & 준수 센터의 메일 흐름 정보](mail-flow-insights-v2.md)를 참조 하십시오.
