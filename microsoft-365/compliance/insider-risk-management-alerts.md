---
title: 참가자 위험 관리 알림
description: Microsoft 365의 참가자 위험 관리 경고에 대해 자세히 알아보기
keywords: Microsoft 365, 참가자 위험, 위험 관리, 규정 준수
localization_priority: Normal
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection: m365-security-compliance
ms.openlocfilehash: 602571e5cbd3132209382ca2e2a3d8941ea8ab2e
ms.sourcegitcommit: e5ac81132cc5fd248350627a3cc7b3c640f53b6e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48208829"
---
# <a name="insider-risk-management-alerts"></a>참가자 위험 관리 알림

참가자 위험 관리 알림은 참가자 위험 관리 정책에 정의 된 위험 지표에 의해 자동으로 생성 됩니다. 이러한 경고는 준수 분석가를 제공 하 고 현재 위험 상태의 모든 보기를 investigators 조직에서 검색 된 위험에 대 한 조치를 취할 수 있도록 허용 합니다. 기본적으로 정책은 낮음, 중간 및 높은 심각도 경고를 생성 하지만 필요에 따라 [경고 볼륨을 높이 거 나 낮출](insider-risk-management-settings.md#alert-volume) 수 있습니다. 또한 정책 마법사를 사용 하 여 새 정책을 만들 때 [정책 지표에 대 한 경고 임계값](insider-risk-management-settings.md#indicator-level-settings-preview) 을 구성할 수 있습니다.

## <a name="alert-dashboard"></a>알림 대시보드

참가자 위험 **경고 대시보드** 를 사용 하면 참가자 위험 정책에 의해 생성 된 경고를 보고 작업할 수 있습니다. 각 보고서 위젯은 지난 30 일 동안의 정보를 표시 합니다.

- **검토할 경고**: 검토 및 심사가 필요한 총 경고 수는 경고 심각도 별 분석을 포함 하 여 나열 됩니다.
- **지난 30 일간 경고 열기**: 지난 30 일 동안 정책에서 생성 된 총 경고 수는 높음, 중간 및 낮은 경고 심각도 수준에 따라 정렬 됩니다.
- **평균 경고 해결 시간**: 유용한 경고 통계에 대 한 요약:
    - 시간, 일 또는 월 단위로 나열 되는 심각도가 높은 경고를 확인 하는 데 소요 되는 평균 시간입니다.
    - 시간, 일 또는 월 단위로 나열 되는 중간 심각도 경고를 해결 하는 데 소요 되는 평균 시간입니다.
    - 시간, 일 또는 월 단위로 나열 되는 낮은 심각도 경고를 확인 하는 데 소요 되는 평균 시간입니다.

![참가자 위험 관리 경고 대시보드](../media/insider-risk-alerts-dashboard.png)

>[!NOTE]
>참가자 위험 관리는 위험 조사 및 검토 환경을 보호 하 고 최적화 하는 데 도움이 되는 기본 제공 알림 제한을 사용 합니다. 이러한 제한은 잘못 구성 된 데이터 커넥터 또는 DLP 정책과 같은 정책 경고의 오버 로드를 초래할 수 있는 문제 로부터 보호 합니다. 따라서 사용자에 대 한 새 알림을 표시 하는 데 지연이 있을 수 있습니다.

## <a name="alert-status-and-severity"></a>경고 상태 및 심각도

경고를 다음 상태 중 하나로 분류할 수 있습니다.

- **확인**됨: 경고가 확인 되 고 신규 또는 기존 사례에 할당 되었습니다.
- 해제 **됨: 심사**프로세스에서 경고가 심각 하 게 해제 되었습니다.
- **검토 필요**: 심사 작업이 아직 수행 되지 않은 새 경고입니다.
- **해결 됨**: 마감 및 해결 된 사례의 일부인 경고입니다.

경고 위험 점수가 몇 가지 위험 활동 표시기에서 자동으로 계산 됩니다. 이러한 지표에는 위험 활동의 유형, 작업 발생 빈도, 사용자 위험 활동의 기록 및 활동의 seriousness을 향상 시킬 수 있는 활동 위험의 추가 등이 포함 됩니다. 경고 위험 점수는 각 경고에 대 한 위험 심각도 수준에 대 한 프로그래밍 방식 할당을 구동 하며 사용자 지정할 수 없습니다. 경고가 심사 되지 않고 위험 활동이 계속 해 서 경고로 계산 되는 경우 위험 심각도 수준이 증가할 수 있습니다. 위험 분석가 및 investigators는 경고 위험 심각도를 사용 하 여 조직의 위험 정책 및 표준에 따라 알림을 쉽게 심사할 수 있습니다.

경고 위험 심각도 수준은 다음과 같습니다.

- **높은 심각도**: 경고에 대 한 활동 및 지표로 인해 심각한 위험이 발생 합니다. 연관 된 위험 활동은 심각 하 고 반복적인 corelate 다른 중요 한 위험 요인에 비해 강력 합니다.
- **중간 심각도**: 경고에 대 한 활동 및 표시기가 중간 위험에 노출 됩니다. 연관 된 위험 활동은 중간에 자주 발생 하며 다른 위험 요인에 대 한 일부 상관 관계가 있습니다.
- **낮은 심각도**: 경고에 대 한 활동 및 표시기가 사소한 위험을 야기 합니다. 연관 된 위험 활동은 사소 하지만 더 드물게 발생 하며 다른 중요 한 위험 요인에 corelate 않습니다.

## <a name="filter-alerts-on-the-alert-dashboard"></a>경고 대시보드에서 경고 필터링

조직의 활성 참가자 위험 관리 정책의 수와 유형에 따라 대규모 경고를 검토 하는 것은 어려울 수 있습니다. 알림 필터를 사용 하면 분석가와 investigators에서 여러 특성으로 알림을 정렬할 수 있습니다. **알림 대시보드에서**알림을 필터링 하려면 **필터** 컨트롤을 선택 합니다. 하나 이상의 특성을 기준으로 알림을 필터링 할 수 있습니다.

- **상태**: 경고 목록을 필터링 할 상태 값을 하나 이상 선택 합니다. 이러한 옵션은 *확인*, *해제*, *검토*및 *해결*된 것입니다.
- **심각도**: 경고 목록을 필터링 할 경고 위험 수준을 하나 이상 선택 합니다. *높음*, *중간*및 *낮음*의 옵션을 사용할 수 있습니다.
- **검색 된 시간**: 알림을 만들 때의 시작 및 종료 날짜를 선택 합니다.
- **정책**: 선택한 정책에 의해 생성 된 경고를 필터링 할 하나 이상의 정책을 선택 합니다.

## <a name="search-alerts-on-the-alert-dashboard"></a>경고 대시보드의 검색 알림

특정 단어에 대 한 경고 이름을 검색 하려면 **검색** 컨트롤을 선택 하 고 검색할 단어를 입력 합니다. 검색 결과에는 검색에 정의 된 단어가 포함 된 정책 경고가 표시 됩니다.

## <a name="triage-alerts"></a>문제 분류 알림

참가자 위험 알림을 심사 하려면 다음 단계를 완료 합니다.

1. [Microsoft 365 준수 센터](https://compliance.microsoft.com)에서 **참가자 위험 관리** 로 이동 하 여 **알림** 탭을 선택 합니다.
2. **알림 대시보드에서**심사 하려는 알림을 선택 합니다.
3. **경고 정보 창**에서 다음 탭을 검토 하 고 경고를 심사할 수 있습니다.
    - **요약**:이 탭에는 경고에 대 한 일반적인 정보가 포함 되어 있으며, 알림을 확인 하 고 새 사례를 만들거나 알림을 해제할 수 있습니다. 여기에는 경고의 현재 상태와 경고 위험 심각도 수준 ( *높음*, *보통*, *낮음으로*나열)이 포함 됩니다. 경고가 심사 되지 않은 경우 심각도 수준은 시간이 지남에 따라 증가 하거나 감소할 수 있습니다.
        - **발생**한 작업: 활동에 연결 된 위반 유형을 비롯 하 여 활동 평가 기간 동안 상위 세 가지 위험 활동 및 정책 일치를 표시 합니다.
        - **사용자 세부 정보**: 경고에 할당 된 사용자에 대 한 일반 정보를 표시 합니다. 익명화가 사용 하도록 설정 된 경우 사용자 이름, 전자 메일 주소, 별칭 및 조직 필드는 익명입니다.
        - **알림 세부 정보**: 경고가 생성 된 이후의 시간을 포함 하 고, 경고를 생성 한 정책이 나열 되며, 경고에서 생성 된 사례가 나열 됩니다. 새 알림의 **경우 사례** 필드에 아무 것도 표시 되지 않습니다.
        - **검색 된 콘텐츠**: 경고에 대 한 위험 활동과 관련 된 콘텐츠를 포함 하 고 주요 영역별로 활동 이벤트를 요약 합니다. 활동 링크를 선택 하면 활동 탐색기가 열리고 활동에 대 한 추가 정보가 표시 됩니다.
    - **사용자 활동**:이 탭에는 경고와 연결 된 사용자에 대 한 활동 기록이 표시 됩니다. 이 기록에는이 경고에 대 한 정책에 할당 된 서식 파일에 정의 된 위험 표시기와 관련 된 기타 경고 및 활동이 포함 됩니다. 이 기록을 사용 하면 위험 분석가와 investigators가 심사 프로세스의 일환으로 직원의 이전 위험에 대 한 동작을 구분할 수 있습니다.
    - **작업**: 각 경고에 대해 다음 작업을 사용할 수 있습니다.
        - **확장 된 보기 열기**: **활동 탐색기** 대시보드를 엽니다.
        - **사례 확인 및 만들기**:이 작업을 사용 하 여 사용자와 연결 된 모든 알림에 대 한 새 사례를 확인 하 고 만듭니다. 이 작업을 수행 하면 자동으로 경고 상태가 *확인*됨으로 변경 됩니다.
        - **알림 해제**:이 작업을 사용 하 여 알림을 해제할 수 있습니다. 이 작업을 수행 하면 경고 상태가 *해결 됨으로*변경 됩니다.

## <a name="activity-explorer-preview"></a>활동 탐색기 (미리 보기)

>[!NOTE]
>조직에서이 기능을 사용할 수 있게 되 면 이벤트를 트리거하는 사용자에 대 한 알림 관리 영역에서 활동 탐색기를 사용할 수 있습니다.

활동 탐색기는 위험 investigators 및 분석가에 게 경고에 대 한 자세한 정보를 제공 하는 포괄적인 분석 도구를 제공 합니다. 활동 탐색기를 사용 하 여 검토자가 검색 된 위험한 활동의 시간 표시 막대를 빠르게 검토 하 고 경고와 관련 한 모든 위험 활동을 식별 하 고 필터링 할 수 있습니다. 활동 탐색기에서 알림을 필터링 하려면 필터 컨트롤을 선택 합니다. 경고에 대 한 세부 정보 창에 나열 된 하나 이상의 특성을 기준으로 알림을 필터링 할 수 있습니다. 또한 활동 탐색기는 사용자 지정 가능한 열을 지원 하 여 investigators 및 분석가가 대시보드에 가장 중요 한 정보를 집중할 수 있도록 합니다.

![참가자 위험 관리 활동 탐색기 개요](../media/insider-risk-management-activity-explorer.png)

**활동 탐색기**를 사용 하려면 다음 단계를 완료 합니다.

1. Microsoft 365 준수 센터에서 **참가자 위험 관리** 로 이동 하 여 **알림** 탭을 선택 합니다.
2. **알림 대시보드에서**심사 하려는 알림을 선택 합니다.
3. **경고 정보 창**에서 **확장 된 보기 열기**를 선택 합니다.
4. 선택한 경고에 대 한 페이지에서 **활동 탐색기** 탭을 선택 합니다.

활동 탐색기에서 활동을 검토 하는 경우 investigators 및 분석가는 특정 활동을 선택 하 고 활동 세부 정보 창을 열 수 있습니다. 이 창에는 investigators 및 분석가가 경고 심사 프로세스 중에 사용할 수 있는 작업에 대 한 자세한 정보가 표시 됩니다. 자세한 정보는 경고에 대 한 컨텍스트를 제공 하 고 경고를 트리거한 위험 작업의 전체 범위를 식별 하는 데 도움이 될 수 있습니다.

![참가자 위험 관리 활동 탐색기 세부 정보](../media/insider-risk-management-activity-explorer-details.png)

## <a name="create-a-case-for-an-alert"></a>알림의 사례 만들기

경고를 검토 하 고 심사 함에 따라 위험 활동을 상세히 조사 하기 위한 새로운 사례를 만들 수 있습니다. 알림의 대/소문자를 만들려면 다음 단계를 수행 합니다.

1. [Microsoft 365 준수 센터](https://compliance.microsoft.com)에서 **참가자 위험 관리** 로 이동 하 여 **알림** 탭을 선택 합니다.
2. **알림 대시보드에서**확인 하려는 알림을 선택 하 고 새 사례를 만듭니다.
3. **경고 세부 정보 창**에서 **작업**  >  **확인 & 메시지 만들기**를 선택 합니다.
4. **경고 확인 및 참가자 위험 사례 만들기** 대화 상자에서 대/소문자 이름을 입력 하 고, 참가자로 추가할 사용자를 선택 하 고, 해당 되는 경우 설명을 추가 합니다. 설명은 사례 메모에 자동으로 추가 됩니다.
5. 새 사례를 만들려면 **대/소문자 만들기** 를 선택 하 고, 사례를 만들지 않고 대화 상자를 닫으려면 **취소** 를 선택 합니다.

사례를 만든 후에는 investigators 및 분석가가 사례를 관리 하 고 작동할 수 있습니다. 자세한 내용은 [참가자 위험 관리 사례](insider-risk-management-cases.md) 문서를 참조 하세요.
