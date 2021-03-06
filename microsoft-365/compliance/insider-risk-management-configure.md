---
title: 내부자 위험 관리 시작
description: 조직에서 참가자 위험 관리를 구성 합니다.
keywords: Microsoft 365, 참가자 위험 관리, 위험 관리, 규정 준수
localization_priority: Normal
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- m365-security-compliance
- m365solution-insiderrisk
- m365initiative-compliance
ms.openlocfilehash: 793f51146dc85dc1c6750e82301d0e1206187ad9
ms.sourcegitcommit: c1dd5be42fe0c5dcc7c05817c941edd9076febf8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49558202"
---
# <a name="get-started-with-insider-risk-management"></a>내부자 위험 관리 시작

참가자 위험 관리 정책을 사용 하 여 조직의 위험 경고에 대해 작동 하는 위험한 활동 및 관리 도구를 식별 합니다. 필수 구성 요소를 설정 하 고 참가자 위험 관리 정책을 구성 하려면 다음 단계를 완료 합니다.

>[!IMPORTANT]
>Microsoft 365의 참가자 위험 관리 솔루션은 사용자 수준에서 내부 거 버 넌 스를 사용 하는 데 도움이 되는 거주자 수준 옵션을 제공 합니다. 테 넌 트 수준 관리자는 조직의 구성원에 대해이 솔루션에 대 한 액세스 권한을 제공 하 고 Microsoft 365 준수 센터에서 데이터 커넥터를 설정 하 여 잠재적으로 위험한 활동의 사용자 수준 식별을 지원 하기 위해 해당 정보를 설정할 수 있습니다. 고객은 개별 사용자의 행동, 문자 또는 materially와 관련 된 성능 정보와 관련 된 정보를 관리자가 계산 하 고 조직의 다른 사용자가 사용할 수 있게 할 수 있습니다. 또한 고객은 개인에 게 관련 된 개별 사용자의 행동, 문자 또는 성능 materially 관련 하 여 전체 조사를 수행 해야 하며, 참가자 위험 관리 서비스의 통찰력을 사용 하는 것이 아니라는 것을 승인 합니다. 고객은 개별 사용자 id 및 수정 작업과 관련 된 법률을 비롯 하 여 Microsoft 365 참가자 위험 관리 서비스와 모든 관련 기능 또는 서비스를 사용 하 여 해당 하는 모든 법률을 준수 해야 합니다.

사용자의 참가자 위험 정책을 통해 조직의 위험을 관리 하는 방법에 대 한 자세한 내용은 [Microsoft 365의 참가자 위험 관리](insider-risk-management.md)를 참조 하세요.

## <a name="subscriptions-and-licensing"></a>구독 및 라이선스

참가자 위험 관리를 시작 하기 전에 [Microsoft 365 구독](https://www.microsoft.com/microsoft-365/compare-all-microsoft-365-plans) 및 모든 추가 기능을 확인 해야 합니다. 참가자 위험 관리에 액세스 하 고 사용 하려면 조직에 다음 구독 또는 추가 기능 중 하나가 있어야 합니다.

- Microsoft 365 E5 구독 (유료 또는 평가판 버전)
- Microsoft 365 E3 구독 + Microsoft 365 E5 준수 추가 기능
- Microsoft 365 E3 구독 + Microsoft 365 E5 참가자 위험 관리 추가 기능
- Microsoft 365 A5 구독 (유료 또는 평가판 버전)
- Microsoft 365 A3 구독 + Microsoft 365 A5 규정 준수 추가 기능
- Microsoft 365 A3 구독 + Microsoft 365 A5 참가자 위험 관리 추가 기능

참가자 위험 관리 정책에 포함 된 사용자는 위의 라이선스 중 하나를 할당 받아야 합니다.

Microsoft 365 Enterprise E5 요금제가 아직 없는 경우 microsoft 365을 기존 구독에 [추가](https://docs.microsoft.com/office365/admin/try-or-buy-microsoft-365) 하거나 Microsoft 365 Enterprise e 5의 [평가판을 등록할](https://www.microsoft.com/microsoft-365/enterprise) 수 있습니다.

## <a name="step-1-enable-permissions-for-insider-risk-management"></a>1 단계: 참가자 위험 관리에 대 한 사용 권한 설정

>[!Important]
>역할 그룹을 구성 하 고 나면 역할 그룹 권한을 조직 전체의 할당 된 사용자에 게 적용 하는 데 최대 30 분이 소요 될 수 있습니다.

참가자 위험 관리 기능을 관리 하기 위한 권한을 구성 하는 데 사용 되는 네 가지 역할 그룹이 있습니다. 이러한 구성 단계를 계속 하려면 먼저 테 넌 트 관리자가 사용자에 게 **참가자 위험 관리** 또는 **참가자 위험 관리 관리자** 역할 그룹을 할당 해야 합니다. 초기 구성 후에 참가자 위험 관리 기능에 액세스 하 고 관리 하려면 사용자가 적어도 하나의 참가자 위험 관리 역할 그룹의 구성원 이어야 합니다.

준수 관리 팀의 구조에 따라 특정 역할 그룹에 사용자를 할당 하 여 다른 유형의 참가자 위험 관리 기능을 관리할 수 있는 옵션이 제공 됩니다. 참가자 위험 관리를 구성할 때 다음 역할 그룹 옵션 중에서 선택 합니다.

| **역할 그룹** | **역할 권한** |
| :---- | :---------------- |
| **참가자 위험 관리** | 이 역할 그룹을 사용 하 여 단일 그룹에서 조직의 참가자 위험 관리를 관리 합니다. 지정 된 관리자, 분석가 및 investigators에 대 한 모든 사용자 계정을 추가 하 여 단일 그룹에서 참가자 위험 관리 권한을 구성할 수 있습니다. 이 역할 그룹에는 모든 참가자 위험 관리 권한 역할이 포함 되어 있습니다. 이 구성은 개별 사용자 그룹에 대해 정의 된 별도의 사용 권한이 필요 하지 않은 조직에 적합 하며, 참가자 위험 관리를 빠르게 시작할 수 있는 가장 쉬운 방법입니다.|
| **참가자 위험 관리 관리자** | 이 역할 그룹을 사용 하 여 처음에 참가자 위험 관리를 구성 하 고 참가자 위험 관리자를 정의 된 그룹으로 세분 합니다.  이 역할 그룹의 사용자는 참가자 위험 관리 정책, 전역 설정 및 역할 그룹 할당을 만들고, 읽고, 업데이트 하 고, 삭제할 수 있습니다. |
| **참가자 위험 관리 분석가** | 이 그룹을 사용 하 여 참가자 위험 사례 분석가 역할을 하는 사용자에 게 사용 권한을 할당 합니다. 이 역할 그룹의 사용자는 모든 참가자 위험 관리 알림, 사례 및 알림 서식 파일에 액세스할 수 있습니다. 사용자는 참가자 위험 콘텐츠 탐색기에 액세스할 수 없습니다. |
| **참가자 위험 관리 Investigators** | 이 그룹을 사용 하 여 사용자의 참가자 위험 데이터 investigators 작동할 수 있는 권한을 할당 합니다. 이 역할 그룹의 사용자는 모든 참가자 위험 관리 알림, 사례, 알림 서식 파일 및 콘텐츠 탐색기에 액세스할 수 있습니다. |

> [!NOTE]
> 이러한 역할 그룹은 현재 PIM (권한 Id 관리)에서 지원 되지 않습니다. PIM에 대 한 자세한 내용은 [권한 있는 Id 관리에서 AZURE AD 역할 할당](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-add-role-to-user)을 참조 하세요.

### <a name="add-users-to-an-insider-risk-management-role-group"></a>사용자를 참가자 위험 관리 역할 그룹에 추가

사용자를 참가자 위험 관리 역할 그룹에 추가 하려면 다음 단계를 완료 합니다.

1. [https://protection.office.com/permissions](https://protection.office.com/permissions)Microsoft 365 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.

2. 보안 &amp; 및 준수 센터에서 **사용 권한** 으로 이동 합니다. Office 365에서 역할을 보고 관리 하는 링크를 선택 합니다.

3. 사용자를 추가할 참가자 위험 관리 역할 그룹을 선택한 다음 **역할 그룹 편집** 을 선택 합니다.

4. 왼쪽 탐색 창에서 **구성원 선택을** 선택 하 고 **편집** 을 선택 합니다.

5. **추가** 를 선택한 다음 역할 그룹에 추가 하려는 모든 사용자의 확인란을 선택 합니다.

6. **추가** 를 선택한 다음 **완료** 를 선택 합니다.

7. **저장** 을 선택 하 여 역할 그룹에 사용자를 추가 합니다. **닫기를** 선택 하 여 단계를 완료 합니다.

## <a name="step-2-enable-the-audit-log"></a>2 단계: 감사 로그 사용

참가자 위험 관리는 정책에 구성 된 사용자 insights 및 작업에 대 한 감사 로그를 사용 합니다. 감사 로그는 참가자 위험 관리 정책에 연결 된 모든 작업 또는 정책이 변경 될 때마다 요약 됩니다.

감사를 설정 하는 단계별 지침은 [turn 감사 로그 검색 켜기 또는 끄기를](turn-audit-log-search-on-or-off.md)참조 하십시오. 감사를 설정한 후에는 감사 로그를 준비 중 이며 준비 완료 후 몇 시간 내에 검색을 실행할 수 있음을 알리는 메시지가 표시 됩니다. 이 작업은 한 번만 수행 하면 됩니다. 감사 로그를 사용 하는 방법에 대 한 자세한 내용은 [Search the audit log](search-the-audit-log-in-security-and-compliance.md)을 참조 하십시오.

## <a name="step-3-configure-prerequisites-for-templates"></a>3 단계: 서식 파일의 필수 조건 구성

대부분의 참가자 위험 관리 템플릿에는 관련 작업 알림을 생성 하도록 정책 표시기에 대해 구성 해야 하는 필수 구성 요소가 있습니다. 조직에 대해 구성할 정책에 따라 적절 한 필수 구성 요소를 구성 합니다.

### <a name="configure-microsoft-365-hr-connector"></a>Microsoft 365 HR 커넥터 구성

참가자 위험 관리는 타사 위험 관리 및 인적 자원 플랫폼에서 가져온 사용자 및 로그 데이터를 가져오는 것을 지원 합니다. Microsoft 365 인적 자원 (HR) 데이터 커넥터를 사용 하면 사용자 종료 날짜, 마지막 고용 날짜, 성능 개선 계획 알림, 성과 검토 작업 및 작업 수준 변경 상태를 비롯 한 CSV 파일에서 인적 자원 데이터를 가져올 수 있습니다. 이 데이터는 참가자 위험 관리 정책에 대 한 경고 표시를 지원 하 고 조직에서 전체 위험 관리 범위를 구성 하는 데 중요 한 역할을 합니다. 조직에 대해 두 개 이상의 HR 커넥터를 구성 하는 경우, 참가자 위험 관리는 모든 HR 커넥터에서 자동으로 지표를 가져옵니다.

다음 정책 템플릿을 사용 하는 경우 Microsoft 365 HR 커넥터가 필요 합니다.

- Departing 사용자 데이터 절도
- Departing 사용자의 보안 정책 위반
- 불만 사용자에의 한 보안 정책 위반
- 불만 사용자에의 한 데이터 유출

조직에 대해 Microsoft 365 HR 커넥터를 구성 하려면 단계별 지침에 대 한 [HR 데이터를 가져올 커넥터 설정](import-hr-data.md) 문서를 참조 하세요. HR 커넥터를 구성한 후에는 다음 구성 단계로 돌아가십시오.

### <a name="configure-data-loss-prevention-dlp-policies"></a>DLP (데이터 손실 방지) 정책 구성

참가자 위험 관리는 DLP 정책을 사용 하 여 높은 심각도 수준 DLP 경고에 대 한 중요 한 정보를 원치 않는 사용자에 게 제공 하는 고의적인 또는 우발적 노출을 식별할 수 있도록 지원 합니다. **데이터 누수** 템플릿을 사용 하 여 참가자 위험 관리 정책을 구성 하는 경우 정책에 특정 DLP 정책을 할당 해야 합니다.

DLP 정책은 중요 한 정보에 대 한 높은 심각도 DLP에 대 한 참가자 위험 관리의 위험 점수를 사용자에 게 확인 하는 데 도움을 제공 하 고 조직의 전체 위험 관리 범위를 구성 하는 데 중요 합니다. 참가자 위험 관리 및 DLP 정책 통합 및 계획 고려 사항에 대 한 자세한 내용은 [참가자 위험 관리 정책을](insider-risk-management-policies.md#general-data-leaks)참조 하세요.

>[!IMPORTANT]
>다음을 완료 했는지 확인 합니다.
>
>- DLP 및 참가자 위험 관리 정책 둘 다에서 범위 내 사용자를 이해 하 고 적절히 구성 하 여 예상 되는 정책 범위를 생성 합니다.
>- 이러한 서식 파일에 사용 되는 참가자 위험 관리의 DLP 정책에서 **문제 보고서** 설정이 *높은* 심각도 수준 알림에 대해 구성 되어 있는지 확인 합니다. *낮음* 또는 *보통* 으로 **인시던트 보고서** 필드가 설정 된 DLP 정책에서 참가자 위험 관리 알림이 생성 되지 않습니다.

다음 정책 템플릿을 사용 하는 경우 DLP 정책이 필요 합니다.

- 일반 데이터 누수
- 우선 순위 사용자 별 데이터 유출

조직의 DLP 정책을 구성 하는 방법에 대 한 자세한 내용은 [dlp 정책 만들기, 테스트 및 조정](create-test-tune-dlp-policy.md) 의 단계별 지침을 참조 하십시오. DLP 정책을 구성한 후에는 다음 구성 단계로 돌아가십시오.

### <a name="configure-priority-user-groups"></a>우선 순위 사용자 그룹 구성

참가자 위험 관리에는 우선 순위 사용자 그룹을 정책에 할당 하 여 중요 한 위치, 높은 수준의 데이터 및 네트워크 액세스, 또는 위험 동작의 이전 기록이 있는 사용자에 대 한 고유한 위험 활동을 식별 하는 데 도움이 됩니다. 우선 순위 사용자 그룹을 만들고 그룹에 사용자를 할당 하 여 이러한 사용자가 제공 하는 고유한 환경에 대 한 정책 범위를 지정 합니다.

다음 정책 템플릿을 사용 하는 경우 우선 순위 사용자 그룹이 필요 합니다.

- 우선 순위 사용자 별 보안 정책 위반
- 우선 순위 사용자 별 데이터 유출

우선 순위 사용자 그룹을 만들려면 단계별 지침에 대 한 [참가자 위험 관리 설정 시작](insider-risk-management-settings.md#priority-user-groups-preview) 문서를 참조 하세요. 우선 순위 사용자 그룹을 구성한 후에는 다음 구성 단계로 돌아가십시오.

### <a name="configure-physical-badging-connector-optional"></a>실제 배지 획득 커넥터 구성 (선택 사항)

참가자 위험 관리는 실제 제어 및 액세스 플랫폼에서 가져온 사용자 및 로그 데이터를 가져오는 것을 지원 합니다. 실제 배지 획득 커넥터를 사용 하면 사용자 Id, 액세스 포인트 Id, 액세스 시간 및 날짜, 액세스 상태 등의 JSON 파일에서 access 데이터를 가져올 수 있습니다. 이 데이터는 참가자 위험 관리 정책에 대 한 경고 표시를 지원 하 고 조직에서 전체 위험 관리 범위를 구성 하는 데 중요 한 역할을 합니다. 조직에 대해 둘 이상의 실제 배지 획득 커넥터를 구성 하는 경우, 참가자 위험 관리는 모든 실제 배지 획득 커넥터에서 자동으로 지표를 가져옵니다. 실제 배지 획득 커넥터의 정보는 모든 참가자 위험 정책 템플릿을 사용할 때 다른 참가자 위험 신호를 보완 합니다.

>[!IMPORTANT]
>참가자 위험 관리 정책에 대해 departing 및 종료 된 사용자와 관련 한 신호 데이터를 사용 하 고 실제 제어 및 액세스 플랫폼과의 이벤트 데이터와 상호 연결 하려면 Microsoft 365 HR 커넥터도 구성 해야 합니다. Microsoft 365 HR 커넥터를 사용 하지 않고 실제 배지 획득 커넥터를 사용 하도록 설정 하는 경우, 참가자 위험 관리 정책은 조직의 사용자에 대해 권한이 부여 된 실제 액세스에 대 한 이벤트만 처리 합니다.

조직의 실제 배지 획득 커넥터를 구성 하려면 단계별 지침에 대 한 [배지 획득 데이터를 가져올 커넥터 설정](import-physical-badging-data.md) 문서를 참조 하세요. 커넥터를 구성한 후에는 다음 구성 단계로 돌아가십시오.

## <a name="step-4-configure-insider-risk-settings"></a>4 단계: insider 위기 설정 구성

[참가자 위험 설정은](insider-risk-management-settings.md) 정책을 만들 때 선택한 서식 파일에 관계 없이 모든 참가자 위험 관리 정책에 적용 됩니다. 설정은 모든 참가자 위험 관리 탭의 맨 위에 있는 **참가자 위험 설정** 제어를 사용 하 여 구성 됩니다. 이러한 설정은 개인 정보, 지표, 모니터링 windows 및 지능형 검색을 제어 합니다.

정책을 구성 하기 전에 다음의 참가자 위험 설정을 정의 합니다.

1. [Microsoft 365 준수 센터](https://compliance.microsoft.com)에서 **참가자 위험 관리** 로 이동 하 여 페이지의 오른쪽 위 모서리에서 **참가자 위험 설정을** 선택 합니다.
2. **개인 정보** 페이지에서 정책 알림에 대해 사용자 이름을 표시 하기 위한 개인 정보 설정을 선택 합니다.
3. **지표** 페이지에서 모든 참가자 위험 정책에 적용할 경고 표시기를 선택 합니다.

    >[!IMPORTANT]
    >정책에 정의 된 위험한 활동에 대 한 경고를 수신 하려면 하나 이상의 지표를 선택 해야 합니다.

4. **정책 기한** 페이지에서 사용자가 참가자 위험 정책에 대해 일치 하는 항목을 트리거할 때 적용 되는 [정책](insider-risk-management-settings.md#policy-timeframes) 서를 선택 합니다.
5. **지능형** 검색 페이지에서 참가자 위험 정책에 대해 다음 설정을 구성 합니다.
    - [변칙 감지](insider-risk-management-settings.md#anomaly-detections)
    - [공격적인 언어 감지](insider-risk-management-settings.md#offensive-language-detections)
    - [경고 볼륨 수준](insider-risk-management-settings.md#alert-volume)
    - [끝점 경고 상태에 대 한 Microsoft Defender](insider-risk-management-settings.md#microsoft-defender-for-endpoint-preview)
    - [도메인 설정](insider-risk-management-settings.md#domains-preview)
6. 필요한 경우 **알림 내보내기** 페이지에서 Office 365 관리 api를 사용 하 여 참가자 위험 알림 정보를 내보낼 수 있도록 설정 합니다.
7. **우선 순위 사용자 그룹** 페이지에서 우선 순위 사용자 그룹을 만들고 **3 단계** 에서 만들지 않은 경우 사용자를 추가 합니다.
8. **전원 자동화 흐름** 페이지에서 참가자 위험 흐름 서식 파일의 흐름을 구성 하거나 새 흐름을 만듭니다. 단계별 지침을 보려면 [참가자 위험 관리 설정 시작](insider-risk-management-settings.md#power-automate-flows-preview) 문서를 참조 하세요.
9. **우선 순위 자산 페이지** 에서 실제 컨트롤의 데이터와 실제 배지 획득 커넥터로 가져온 액세스 플랫폼을 사용 하도록 우선 순위 자산을 구성 합니다. 단계별 지침을 보려면 [참가자 위험 관리 설정 시작](insider-risk-management-settings.md#priority-physical-assets-preview) 문서를 참조 하세요.
10. **Microsoft** 팀 페이지에서 microsoft 팀이 참가자 위험 관리와의 통합을 사용 하 여 사례 또는 사용자 공동 작업을 위한 팀을 자동으로 만듭니다. 단계별 지침을 보려면 [참가자 위험 관리 설정 시작](insider-risk-management-settings.md#microsoft-teams-preview) 문서를 참조 하세요.
11. **저장** 을 선택 하 여 사용자의 참가자 위험 정책에 대해 이러한 설정을 사용 하도록 설정 합니다.

## <a name="step-5-create-an-insider-risk-management-policy"></a>5 단계: 참가자 위험 관리 정책 만들기

참가자 위험 관리 정책에는 할당 된 사용자 및 경고에 대해 구성 된 위험 표시기 유형이 정의 되어 있습니다. 활동이 알림을 트리거하도록 하려면 정책을 구성 해야 합니다.

1. [Microsoft 365 준수 센터](https://compliance.microsoft.com)에서 **참가자 위험 관리** 로 이동 하 여 **정책** 탭을 선택 합니다.
2. **정책 만들기** 를 선택 하 여 정책 마법사를 엽니다.
3. **새 참가자 위험 정책** 페이지에서 다음 필드를 작성 합니다.
    - **이름 (필수)**: 정책의 이름을 입력 합니다.
    - **설명 (선택 사항)**: 정책에 대 한 설명을 입력 합니다.
    - **정책 템플릿 선택 (필수)**: 정책 [템플릿](insider-risk-management-policies.md#policy-templates) 중 하나를 선택 하 여 위험 지표 유형을 정의 합니다.

    >[!IMPORTANT]
    >대부분의 정책 템플릿은 관련 알림을 생성 하기 위해 정책에 대해 구성 해야 하는 필수 구성 요소를 포함 합니다. 해당 하는 정책 필수 구성 요소를 구성 하지 않은 경우 위의 **3 단계** 를 참조 하세요.

    >[!CAUTION]
    >2020 년 10 월 16 일부터 더 이상 전자 메일 템플릿에서 공격적인 언어를 사용 하 여 정책을 만들 수 없습니다. 이 서식 파일을 사용 하는 모든 활성 정책은 1 월 2021 일에 영구적으로 제거 될 때까지 작동 합니다.

4. 계속 하려면 **다음** 을 선택 합니다.
5. **사용자** 페이지에서 **사용자 또는 그룹 추가** 를 선택 하거나 **우선 순위 사용자 그룹** 을 선택 하 여 선택한 정책 템플릿에 따라 정책에 포함 되는 사용자 또는 우선 순위 사용자 그룹을 정의 합니다. 해당 **하는 경우 모든 사용자 및 메일 사용 가능 그룹** 확인란을 선택 합니다 (우선 순위 사용자 기반 서식 파일을 선택 하지 않은 경우). 계속 하려면 **다음** 을 선택 합니다.
6. **우선 순위를 지정할 콘텐츠 지정 (선택 사항)** 페이지에서 향상 된 위험 점수에 대해 우선 순위를 지정할 원본을 할당할 수 있습니다. 그러나 관련 콘텐츠가이 페이지에서 기본 제공 또는 사용자 지정 중요 한 정보 유형을 포함 하거나 우선 순위로 지정 되지 않은 경우에는 일부 작업에서 경고가 생성 되지 않습니다.
    - **Sharepoint 사이트**: **sharepoint 사이트 추가** 를 선택 하 고 우선 순위를 지정할 SharePoint 조직을 선택 합니다. 예를 들면 *"group1@contoso.sharepoint.com/sites/group1"* 입니다.
    - **중요 한 정보 유형**: **중요 한 정보 유형 추가** 를 선택 하 고 우선 순위를 지정할 민감도 유형을 선택 합니다. 예를 들어 *"미국 은행 계좌 번호"* 및 *"신용 카드 번호"* 를 들 수 있습니다.
    - **민감도 레이블**: **민감도 레이블 추가** 를 선택 하 고 우선 순위를 지정할 레이블을 선택 합니다. 예를 들어 *"기밀"* 및 *"비밀"* 가 있습니다.
7. 계속 하려면 **다음** 을 선택 합니다.
8. **정책 지표 선택** 페이지에는 **참가자 위험 설정** 지표 페이지에서 사용할 수 있는 것으로 정의 된 [표시기](insider-risk-management-settings.md#indicators) 가 표시 됩니다  >  **Indicators** . 마법사를 시작할 때 *데이터 누수* 템플릿을 선택한 경우에는 **dlp 정책** 드롭다운 목록에서 dlp 정책을 선택 하 여 정책에 대 한 지표를 트리거합니다. 정책에 적용할 지표를 선택 합니다. 이러한 지표에 대 한 기본 정책 임계값 설정을 사용 하지 않으려면 **Microsoft에서 권장 하는 기본 임계값 사용** 을 사용 하지 않도록 설정 하 고 선택한 각 표시기에 대해 임계값을 입력 합니다. 하나 이상의 *Office* 또는 *장치* 지표를 선택한 경우 **위험 성과** 를 적절 하 게 boosters 선택 합니다. 위험 점수 boosters는 선택한 지표에만 적용 됩니다.

    >[!IMPORTANT]
    >이 페이지의 표시기를 선택할 수 없는 경우에는 **참가자 위험 관리**  >  **설정**  >  **정책 지표** 페이지에서 모든 정책에 대해 사용 하도록 설정할 지표를 선택 해야 합니다.

9. 계속 하려면 **다음** 을 선택 합니다.
10. **정책 기한** 페이지에는 **참가자 위험 설정** 정책 기간 페이지의 정책에 대 한 [정품 인증 기간 조건이](insider-risk-management-settings.md#policy-timeframes) 표시 됩니다  >  **Policy timeframes** .
11. 계속 하려면 **다음** 을 선택 합니다.
12. **검토** 페이지에서 정책에 대해 선택한 설정을 검토 합니다. **편집** 을 선택 하 여 정책 값을 변경 하거나 **제출을** 선택 하 여 정책을 만들고 활성화 합니다.

## <a name="next-steps"></a>다음 단계

첫 번째 참가자 위험 관리 정책을 만들기 위해 이러한 단계를 완료 한 후에는 약 24 시간 후에 활동 표시기에서 경고를 수신 하기 시작 합니다. 이 문서 4 단계의 지침을 사용 하 여 필요에 따라 추가 정책을 구성 하거나 [새 참가자 위험 정책 만들기](insider-risk-management-policies.md#create-a-new-policy)의 단계를 수행 합니다.

참가자 위험 경고 및 **알림 대시보드** 를 조사 하는 방법에 대 한 자세한 내용은 [참가자 위험 관리 경고](insider-risk-management-alerts.md)를 참조 하세요.
