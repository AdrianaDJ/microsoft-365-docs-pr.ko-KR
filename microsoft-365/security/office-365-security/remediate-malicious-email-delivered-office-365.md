---
title: Office 365에서 제공 된 악성 전자 메일 재구성
author: msfttracyp
ms.author: tracyp
manager: dansimp
ms.topic: article
ms.service: O365-seccomp
audience: admin
f1.keywords:
- NOCSH
localization_priority: Normal
MS.collection: ''
search.appverid: MET150
description: 위협 수정
appliesto:
- Microsoft 365 Defender
ms.openlocfilehash: 4adabe3e85b2bff26167bfad92a9a7fcbf24e58e
ms.sourcegitcommit: 4debeb8f0fce67f361676340fc390f1b283a3069
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49561294"
---
# <a name="remediate-malicious-email-delivered-in-office-365"></a>Office 365에서 제공 되는 악성 전자 메일 재구성

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


업데이트 관리는 위협에 대해 규정 된 조치를 취하는 것을 의미 합니다. 조직으로 전송 되는 악성 전자 메일은 시스템에서 지울 수 있으며, 자동 제거 (ZAP)를 통해 또는 보안 팀에서 *받은 편지 함으로 이동*, *정크로 이동*, *삭제 된 항목*, *일시 삭제* 또는 *하드 삭제* 로 이동 하는 것과 같은 수정 작업을 통해 정리할 수도 있습니다. Microsoft Defender for Office 365 P2/E5에서는 보안 팀이 수동 및 자동 조사를 통해 전자 메일 및 공동 작업 기능의 위협을 수정할 수 있도록 지원 합니다.

> [!NOTE]
> 보안 팀은 악성 전자 메일을 재구성 하기 위해 *검색 및 삭제* 역할이 할당 되어야 합니다. 역할 할당은 보안 및 준수 센터에서 사용 권한을 통해 수행 됩니다.

## <a name="what-you-need-to-know-before-you-begin"></a>시작 하기 전에 알아야 할 사항

관리자는 전자 메일에 필요한 작업을 수행할 수 있지만, 승인 된 작업을 받으려면 **보안 & 준수 센터** 권한을 통해 해당 사용자에 게 할당 된 *검색 및 제거* 역할이 있어야 합니다 \> **Permissions**. "검색 및 제거" 역할이 역할 그룹 중 하나에 추가 되지 않은 경우에는 작업을 실행할 수 없습니다.

## <a name="manual-and-automated-remediation"></a>수동 및 자동 수정

*수동* 찾기는 보안 팀이 위협 탐색기의 검색 및 필터링 기능을 사용 하 여 위협을 수동으로 식별할 때 발생 합니다. 수정 해야 하는 전자 메일 집합을 식별 한 후 모든 전자 메일 보기 (*맬웨어*, *피싱* 또는 *모든 전자 메일*)를 통해 수동 전자 메일 수정을 트리거할 수 있습니다.

> [!div class="mx-imgBorder"]
> [![Office 365 Threat Explorer의 수동 구하기 날짜별입니다. ](../../media/tp-RemediationArticle1.png)](../../media/tp-RemediationArticle1.png#lightbox)

보안 팀은 위협 탐색기를 사용 하 여 다음과 같은 여러 가지 방법으로 전자 메일을 선택할 수 있습니다.

- 직접 전자 메일 선택: 다양 한 보기에서 필터를 사용 합니다. 수정할 전자 메일을 최대 100 개까지 선택 합니다.

- 쿼리 선택: 위쪽 **선택** 단추를 사용 하 여 전체 쿼리를 선택 합니다. 또한 동일한 쿼리가 action center 메일 전송 세부 정보에도 표시 됩니다.

- 제외를 사용 하는 쿼리 선택: 보안 운영 팀에서 전체 쿼리를 선택 하 고 쿼리에서 특정 전자 메일을 수동으로 제외 하 여 전자 메일을 수정 하려는 경우가 있습니다. 이렇게 하려면 관리자가 **모두 선택** 확인란을 사용 하 고 아래로 스크롤하여 전자 메일을 수동으로 제외할 수 있습니다. 이 쿼리는 최대 1000 개의 전자 메일을 보유할 수 있습니다. 최대 제외 항목 수는 100입니다.

위협 탐색기를 통해 전자 메일을 선택한 후에는 직접 작업을 수행 하거나 전자 메일을 큐에 대기 시켜 작업을 수행할 수 있습니다.

- 직접 승인: *받은 편지 함으로 이동*, *정크로 이동*, 삭제 된 *항목* 으로 이동, *일시 삭제* 또는 *하드 삭제* 는 적절 한 사용 권한을 가진 보안 담당자가 선택 하 고, 재구성 프로세스에서 선택한 작업을 실행 하기 시작 합니다. 임시 플라이 아웃이 진행 중인 수정을 표시 합니다.

- 2 단계 승인: 적절 한 사용 권한이 없거나 작업 실행을 위해 기다려야 하는 관리자가 "수정에 추가" 작업을 수행할 수 있습니다. 이 경우 대상으로 지정 된 전자 메일이 업데이트 관리 컨테이너에 추가 됩니다. 수정이 실행 되기 전에 승인이 필요 합니다.

**자동화 된 조사 및 응답** 동작은 알림 또는 위협 탐색기의 보안 작업 팀에서 트리거됩니다. 여기에는 보안 운영 팀이 승인 해야 하는 권장 수정 작업이 포함 되어 있을 수 있습니다. 이러한 작업은 자동화 조사의 **작업** 탭에 포함 됩니다.

> [!div class="mx-imgBorder"]
> [![Zap 실행 시간을 보여 주는 "Zapped" 페이지의 맬웨어가 포함 된 메일입니다. ](../../media/tp-RemediationArticle3.png)](../../media/tp-RemediationArticle3.png#lightbox)

위협 탐색기에서 생성 되 고 자동 조사에서 제공 되는 승인 된 작업은 알림 센터에 표시 되는 모든 remediations (직접 승인 또는 2 단계 승인) 이 작업은 **검토**  >  **관리 센터** 의 왼쪽 탐색 패널을 통해 액세스 합니다.

> [!div class="mx-imgBorder"]
> [![날짜 및 심각도 별 위협 목록이 포함 된 작업 센터입니다. ](../../media/tp-RemediationArticle4.png)](../../media/tp-RemediationArticle4.png#lightbox)

알림 센터에서 최근 30 일 동안의 모든 수정 작업을 표시 합니다. 위협 탐색기를 통해 수행 되는 작업은 수정 내용이 만들어질 때 보안 작업 팀이 제공한 이름에 따라 나열 됩니다. 자동화 된 조사를 통해 수행 되는 작업은 조사를 트리거한 관련 경고 (예: "Zap email cluster ...")로 시작 하는 제목이 있습니다.

이름, 만든 날짜, 설명, 위협 심각도 및 상태를 포함 하 여 해당 항목에 대 한 세부 정보를 볼 수 있는 수정 내용을 확인 합니다. 또한 다음과 같은 두 개의 탭이 표시 됩니다.

- **메일 전송** 탭: 위협 탐색기나 자동화 된 조사를 통해 전송 되는 전자 메일 수를 표시 합니다. 이러한 전자 메일은 실행 가능 또는 조치 될 수 있습니다.

  > [!div class="mx-imgBorder"]
  > [![작동 가능한 위협 ](../../media/tp-RemediationArticle5.png) 및 조치를 취할 수 있는 작업 센터](../../media/tp-RemediationArticle5.png#lightbox)

  - **실행 가능**: 다음 클라우드 사서함 위치의 전자 메일을 처리 및 이동할 수 있습니다.
    - 받은 편지함
    - 차단할
    - 폴더 삭제됨
    - 일시 삭제 된 폴더

      > [!NOTE]
      > 현재 사서함에 대 한 액세스 권한이 있는 사용자만 일시 삭제 된 폴더의 항목을 복구할 수 있습니다.

  - 실행 **불가능**: 다음 위치에 있는 전자 메일은 재구성 작업에서 수행 하거나 이동할 수 없습니다.
    - 격리
    - 하드 삭제 된 폴더
    - 온-프레미스/외부
    - 실패/삭제 됨

  의심 스러운 메시지는 remediable 또는 nonremediable로 분류 됩니다. 대부분의 경우 remediable 및 nonremediable 메시지는 전송 된 총 메시지와 동일 하 게 결합 됩니다. 그러나 드문 경우 지는 그렇지 않을 수 있습니다. 시스템 지연, 시간 초과 또는 만료 된 메시지 때문에 이러한 상황이 발생할 수 있습니다. 메시지는 조직의 위협 탐색기 보존 기간을 기준으로 만료 됩니다.

  조직의 위협 탐색기 보존 기간 후 이전 메시지를 수정 수 없는 경우, 숫자 불일치가 표시 되는 경우 수정 항목을 다시 시도 하는 것이 좋습니다. 시스템 지연을 위해 일반적으로 몇 시간 내에 업데이트를 새로 고칩니다.

  조직에서 위협 탐색기에 있는 전자 메일의 보존 기간을 30 일이 수정 전자 메일이 29-30 일 이내에 전송 되는 경우에는 메일 제출 수가 항상 추가 되는 것은 아닙니다. 전자 메일이 이미 보존 기간 밖으로 이동 하기 시작 했을 수 있습니다.

  Remediations이 "진행 중" 상태에 있는 경우 시스템 지연 때문일 수 있습니다. 수정 하는 데 몇 시간이 걸릴 수 있습니다. 시스템 지연으로 인해 재구성을 시작할 때 일부 전자 메일에 쿼리를 포함 하지 않을 수 있으므로 메일 전송 횟수의 변형이 표시 될 수 있습니다. 이러한 경우에는 수정을 다시 시도 하는 것이 좋습니다.

  > [!NOTE]
  > 최상의 결과를 위해 업데이트 관리는 5만 개 이하의 범위로 수행 해야 합니다.

  Remediable 전자 메일만 업데이트 관리 중에 처리 됩니다. Nonremediable 전자 메일이 클라우드 사서함에 저장 되지 않으므로 Office 365 전자 메일 시스템에서이를 수정할 수 없습니다.

  관리자는 필요한 경우 전자 메일에 대해 격리 된 작업을 수행할 수 있지만, 이러한 전자 메일은 수동으로 제거 되지 않는 한 격리에서 만료 됩니다. 사용자가 악의적인 콘텐츠를 액세스할 수 없기 때문에 격리 된 전자 메일은 보안 담당자가 격리에서 위협을 제거 하기 위해 조치를 취할 필요가 없습니다. 전자 메일이 온-프레미스 또는 외부에 있는 경우 사용자에 게 연락 하 여 의심 스러운 전자 메일을 처리할 수 있습니다. 또는 관리자가 별도의 전자 메일 서버/보안 도구를 사용 하 여 제거할 수 있습니다. 이러한 전자 메일은 Threat Explorer에서 *배달 위치 = 온-프레미스* 외부 필터를 적용 하 여 확인할 수 있습니다. 실패 하거나 삭제 된 전자 메일 또는 사용자가 액세스할 수 없는 전자 메일의 경우 이러한 메일이 사서함에 도달 하지 않으므로 완화할 전자 메일이 없을 수 있습니다.

  다음 이미지에서는 제출 서류가 알림 센터에 표시 되는 방식을 보여 줍니다. 업데이트 관리에는 여러 제출이 포함 될 수 있습니다. 한 가지 자동화 된 조사를 통해 여러 작업을 승인 하면 각 전자 메일 또는 전자 메일 클러스터 작업이 다른 제출 서류와 동일한 재구성에 표시 됩니다.

  > [!div class="mx-imgBorder"]
  > [![ZAP 전자 메일 클러스터 플라이 아웃 패널 ](../../media/tp-RemediationArticle6.png)](../../media/tp-RemediationArticle6.png#lightbox)

  메일 전송 항목을 선택 하 여 쿼리 (쿼리 선택 시 자동화 된 조사 또는 위협 탐색기를 통해 업데이트 관리를 트리거한 경우)와 재구성 시작 및 종료 시간을 표시 합니다. 또한 수정을 위해 제출 된 메시지 목록도 표시 됩니다. 메시지가 위협 탐색기 보존 기간 밖으로 이동 되 면이 목록에서 메시지가 사라집니다. 이 목록에는 remediable 개별 메시지도 표시 됩니다.

- **작업 로그**:이 탭에는 승인 날짜, 작업을 승인한 관리자, 작업, 상태 및 개수를 포함 하 여 재구성 한 메시지가 표시 됩니다.

  상태는 다음이 될 수 있습니다.

  - **시작 됨**: 재구성이 트리거됩니다.
  - **대기** 중: 전자 메일을 완화할 수 있도록 재구성을 큐에 넣었습니다.
  - **진행** 중: 완화가 진행 중입니다.
  - **완료** 됨: 모든 remediable 전자 메일에 대 한 완화가 완료 되었거나 몇 가지 오류가 발생 했습니다.
  - **실패**: remediations이 완료 되지 않았습니다.

  Remediable 전자 메일만 처리 될 수 있으므로 각 전자 메일의 정리는 성공 또는 실패로 표시 됩니다. 총 remediable 전자 메일에서 성공 및 실패 한 완화 보고가 보고 됩니다.

  - **성공**: remediable 전자 메일에 대 한 적절 한 작업을 수행 했습니다. 예를 들어 관리자가 사서함에서 전자 메일을 제거 하려는 경우 관리자는 전자 메일을 일시 삭제 하는 작업을 수행 합니다. 작업을 수행한 후 원래 폴더에서 remediable 전자 메일이 발견 되지 않으면 상태가 성공한 것으로 표시 됩니다.

  - **실패**: remediable 전자 메일에 대해 필요한 작업을 수행 하지 못했습니다. 예를 들어 관리자가 사서함에서 전자 메일을 제거 하려는 경우 관리자는 전자 메일을 일시 삭제 하는 작업을 수행 합니다. 작업을 수행한 후에도 사서함에서 remediable 전자 메일이 계속 발견 되 면 상태가 실패로 표시 됩니다.

  작업 로그에서 항목을 선택 하 여 재구성 세부 정보를 표시 합니다. 세부 정보에 "성공" 또는 "사서함에서 찾을 수 없음" 이라고 표시 되 면 해당 항목은 이미 사서함에서 제거 된 것입니다. 업데이트 관리 중에도 오류가 발생 하는 경우가 있습니다. 이러한 경우에는 재구성을 다시 시도 하는 것이 좋습니다.
  
  일괄 처리를 수정 경우 메일 전송을 통해 메시지를 전송 하 고 작업 로그를 통해 재구성 한 메시지를 내보낼 수도 있습니다. 내보내기 제한이 10만 레코드로 늘어납니다.

  관리 기능은 위협을 완화 하 고 의심 스러운 전자 메일을 처리할 수 있는 강력한 도구입니다. 조직의 보안을 유지 하는 데 도움이 됩니다.
