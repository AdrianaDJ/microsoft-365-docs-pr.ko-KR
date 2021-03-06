---
title: Advanced eDiscovery의 전자 메일 스레딩
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Advanced eDiscovery 분석을 수행할 때 전자 메일 스레딩은 전자 메일 대화를 구문 분석 하 고 각 메시지를 서로 다른 범주로 구분 합니다.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: b087bfc84175f80daaf1c0d2f1394584a70757ac
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285564"
---
# <a name="email-threading-in-advanced-ediscovery"></a>Advanced eDiscovery의 전자 메일 스레딩

잠시 동안 진행 되 고 있는 전자 메일 대화를 생각해 볼 수 있습니다. 대부분의 경우 스레드의 마지막 전자 메일에는 위의 모든 전자 메일의 내용이 포함 됩니다. 마지막 전자 메일을 검토 하면 해당 스레드에서 발생 한 대화의 전체 컨텍스트를 확인할 수 있습니다. 전자 메일 스레딩에서는 검토자가 컨텍스트 손실 없이 수집 된 문서를 분수로 검토할 수 있도록 이러한 전자 메일이 식별 됩니다.

## <a name="what-does-email-threading-do"></a>전자 메일 스레딩의 기능

전자 메일 스레딩은 각 전자 메일을 분석 하 고 개별 메시지에 deconstructs 합니다. 각 전자 메일은 개별 메시지의 연쇄입니다. 그런 다음 검토 집합의 모든 전자 메일을 분석 하 여 전자 메일이 고유한 콘텐츠를 포함 하는지 또는 체인이 다른 전자 메일에 완전히 포함 되어 있는지를 확인 합니다. 최종 전자 메일은 다음 네 가지 범주로 나뉩니다.

- **포함**: 전자 메일의 마지막 메시지에는 고유한 콘텐츠가 있으며 전자 메일에는 해당 콘텐츠가 완전히이 전자 메일에 포함 된 다른 전자 메일에 포함 된 첨부 파일이 모두 있습니다.

- **포함 빼기**: 전자 메일의 마지막 메시지에는 고유한 콘텐츠가 있지만 전자 메일에는 해당 콘텐츠가 완전히이 전자 메일에 포함 된 다른 전자 메일에 포함 된 첨부 파일이 포함 되지 않습니다.

- **포함 복사본**: 포함/포괄 되는 전자 메일의 정확한 복사본

- **없음**:이 전자 메일의 콘텐츠는 포함/포괄으로 표시 되는 하나 이상의 전자 메일에 완전히 포함 됩니다.

## <a name="how-is-it-different-from-conversations-in-outlook"></a>Outlook의 대화와는 다른 이유는 무엇 인가요?

이는 Outlook의 대화 그룹과 유사 합니다. 그러나 몇 가지 중요 한 차이가 있습니다. 분기을 두 대화로 이동 하는 전자 메일 대화를 생각해 보십시오. 예를 들어 사용자가 대화에서 최신 상태가 아닌 전자 메일에 응답 하 여 대화의 마지막 두 전자 메일이 모두 고유한 콘텐츠를 가지도록 합니다.

Outlook에서는 전자 메일을 단일 대화로 그룹화 하는 것도 가능 합니다. 마지막 전자 메일만 읽으면 고유한 콘텐츠가 포함 된 두 번째-마지막 전자 메일의 컨텍스트가 손실 된다는 뜻입니다. 전자 메일 스레딩에서는 각 전자 메일을 개별 구성 요소로 구문 분석 하 고 비교 하므로 전자 메일 스레딩은 마지막 두 개의 전자 메일을 모두 포함 하 여 포함으로 표시 된 모든 전자 메일을 읽을 때 컨텍스트를 놓치지 않도록 합니다.
