---
title: 내부자 위험 관리 계획
description: 조직에서 참가자 위험 관리 정책을 사용 하도록 계획 하는 방법을 알아봅니다.
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
ms.openlocfilehash: e8bf55cf3c27170c471dd45a68fd1ec2fa4a615b
ms.sourcegitcommit: 474bd6a86c3692d11fb2c454591c89029ac5bbd5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/19/2020
ms.locfileid: "49357447"
---
# <a name="plan-for-insider-risk-management"></a>내부자 위험 관리 계획

조직에서 [참가자 위험 관리](insider-risk-management.md) 를 시작 하기 전에 정보 기술 및 준수 관리 팀에서 검토 해야 하는 중요 한 계획 작업 및 고려 사항이 있습니다. 다음 영역에서 배포를 철저히 이해 하 고 계획 하는 것은 사용자의 참가자 위험 관리 기능 구현 및 사용이 원활 하 게 진행 되 고 솔루션에 대 한 모범 사례와 부합 되도록 하는 데 도움이 됩니다.

## <a name="work-with-stakeholders-in-your-organization"></a>조직의 관련자에 대 한 작업

조직에서 참가자 위험 관리 경고 및 사례에 대 한 작업을 수행 하기 위해 공동 작업을 수행할 수 있는 적절 한 관련자를 파악 합니다. 초기 계획에 포함 해야 하는 몇 가지 권장 되는 이해 관계자 및 종단 간 [참가자 위험 관리 워크플로](insider-risk-management.md#workflow) 는 다음과 같은 조직 영역의 사용자입니다.

- 정보 기술
- 규정 준수
- 개인 정보
- 보안
- 인사부
- 법률 정보

## <a name="determine-any-regional-compliance-requirements"></a>지역별 규정 준수 요구 사항 확인

지리적 영역과 조직 영역에 따라 조직의 다른 영역과는 다른 규정 준수 및 개인 정보 요구 사항이 있을 수 있습니다. 이러한 영역의 관련자와 협력 하 여 참가자 위험 관리의 규정 준수 및 개인 정보 제어를 이해 하 고 조직의 다양 한 영역에서 사용 하는 방법을 파악 합니다. 일부 시나리오의 경우 규정 준수 및 개인 정보 보호 요구 사항에 따라 사용자 또는 해당 영역의 정책 요구 사항에 대 한 사례를 기반으로 조사 및 사례 로부터 일부 관련자를 지정 하거나 제한 하는 정책이 필요할 수도 있습니다.

특정 관련자에 게 특정 지역, 역할 또는 부서의 사용자와 관련 된 사례 조사에 대 한 요구 사항이 있는 경우 다른 지역 및 인구를 대상으로 하는 별도의 [참가자 위험 관리 정책](insider-risk-management-policies.md) (동일한 경우에도)을 구현할 수 있습니다. 이 구성을 통해 적절 한 관련자는 해당 역할과 지역과 관련 된 사례를 보다 쉽게 심사 하 고 관리할 수 있습니다. 또한 investigators 및 검토자가 사용자와 같은 언어를 활용 하 여 참가자 위험 관리 경고 및 사례에 대 한 에스컬레이션 프로세스를 간소화 하는 지역에 대 한 프로세스 및 정책을 만드는 것도 고려할 수 있습니다.

## <a name="plan-for-the-review-and-investigation-workflow"></a>검토 및 조사 워크플로 계획

[Microsoft 365 준수 센터](https://compliance.microsoft.com/)에서 일반 흐름에 대 한 경고 및 사례를 모니터링 하 고 검토 하려면 전용 관련자를 선택 합니다. 참가자 위험 관리에서 사용할 수 있는 다른 역할 그룹에 서로 다른 관련자를 할당 하는 방법을 이해 하 고 있어야 합니다.

준수 관리 팀의 구조에 따라 특정 역할 그룹에 사용자를 할당 하 여 다른 유형의 참가자 위험 관리 기능을 관리할 수 있는 옵션이 제공 됩니다. 참가자 위험 관리를 구성할 때 다음 역할 그룹 옵션 중에서 선택 합니다.

| **역할 그룹** | **역할 권한** |
| :---- | :---------------- |
| **참가자 위험 관리** | 이 역할 그룹을 사용 하 여 단일 그룹에서 조직의 참가자 위험 관리를 관리 합니다. 지정 된 관리자, 분석가 및 investigators에 대 한 모든 사용자 계정을 추가 하 여 단일 그룹에서 참가자 위험 관리 권한을 구성할 수 있습니다. 이 역할 그룹에는 모든 참가자 위험 관리 권한 역할이 포함 되어 있습니다. 이 구성은 개별 사용자 그룹에 대해 정의 된 별도의 사용 권한이 필요 하지 않은 조직에 적합 하며, 참가자 위험 관리를 빠르게 시작할 수 있는 가장 쉬운 방법입니다.|
| **참가자 위험 관리 관리자** | 이 역할 그룹을 사용 하 여 처음에 참가자 위험 관리를 구성 하 고 참가자 위험 관리자를 정의 된 그룹으로 세분 합니다.  이 역할 그룹의 사용자는 참가자 위험 관리 정책, 전역 설정 및 역할 그룹 할당을 만들고, 읽고, 업데이트 하 고, 삭제할 수 있습니다. |
| **참가자 위험 관리 분석가** | 이 그룹을 사용 하 여 참가자 위험 사례 분석가 역할을 하는 사용자에 게 사용 권한을 할당 합니다. 이 역할 그룹의 사용자는 모든 참가자 위험 관리 알림, 사례 및 알림 서식 파일에 액세스할 수 있습니다. 사용자는 참가자 위험 콘텐츠 탐색기에 액세스할 수 없습니다. |
| **참가자 위험 관리 Investigators** | 이 그룹을 사용 하 여 사용자의 참가자 위험 데이터 investigators 작동할 수 있는 권한을 할당 합니다. 이 역할 그룹의 사용자는 모든 참가자 위험 관리 알림, 사례, 알림 서식 파일 및 콘텐츠 탐색기에 모든 경우에 액세스할 수 있습니다. |

## <a name="understand-requirements-and-dependencies"></a>요구 사항 및 종속성 이해

참가자 위험 관리 정책을 구현 하는 방법에 따라 적절 한 Microsoft 365 라이선스 구독을 준비 하 고 일부 솔루션 필수 구성 요소를 계획 해야 합니다.

**라이선싱:** Microsoft 365 라이선스 구독을 광범위 하 게 선택한 경우의 참가자 위험 관리를 사용할 수 있습니다. 자세한 내용은 [참가자 위험 관리 시작](insider-risk-management-configure.md#subscriptions-and-licensing) 문서를 참조 하세요.

Microsoft 365 Enterprise E5 요금제가 아직 없는 경우 microsoft 365을 기존 구독에 [추가](https://docs.microsoft.com/office365/admin/try-or-buy-microsoft-365) 하거나 Microsoft 365 Enterprise e 5의 [평가판을 등록할](https://www.microsoft.com/microsoft-365/enterprise) 수 있습니다.

**정책 템플릿 요구 사항:** 선택한 정책 템플릿에 따라 조직에서 참가자 위험 관리를 구성 하기 전에 이해 하 고 계획 해야 하는 요구 사항은 다음과 같습니다.

- Departing users 서식 파일을 사용 하 여 **데이터 절도** 를 사용할 때는 조직의 사용자에 대 한 resignation 및 종료 날짜 정보를 정기적으로 가져오기 위해 MICROSOFT 365 HR 커넥터를 구성 해야 합니다. 조직의 Microsoft 365 HR 커넥터를 구성 하는 방법에 대 한 단계별 지침은 [HR connector 문서를 사용한 가져오기 데이터](import-hr-data.md) 를 참조 하십시오.
- **데이터 누수** 템플릿을 사용 하는 경우에는 하나 이상의 DLP (데이터 손실 방지) 정책을 구성 하 여 조직에서 중요 한 정보를 정의 하 고 심각도가 높은 DLP 정책 알림에 대해 참가자 위험 경고를 수신 해야 합니다. 조직의 DLP 정책을 구성 하는 방법에 대 한 자세한 내용은 [dlp 정책 만들기, 테스트 및 조정](create-test-tune-dlp-policy.md) 의 단계별 지침을 참조 하십시오.
- **보안 정책 위반** 템플릿을 사용 하는 경우 Defender 보안 센터의 참가자 위험 관리 통합에서 보안 위반 알림을 가져오려면 끝점에 대해 Microsoft defender를 사용 하도록 설정 해야 합니다. 참가자 위험 관리와의 끝점 통합을 위해 Defender를 사용 하도록 설정 하는 단계별 지침을 보려면 [Microsoft defender 문서에서 고급 기능 구성을](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-features) 참조 하세요.
- **불만 사용자** 서식 파일을 사용 하는 경우 조직의 사용자에 대 한 성능 또는 강등 상태 정보를 정기적으로 가져오기 위해 MICROSOFT 365 HR 커넥터를 구성 해야 합니다. 조직의 Microsoft 365 HR 커넥터를 구성 하는 방법에 대 한 단계별 지침은 [HR connector 문서를 사용한 가져오기 데이터](import-hr-data.md) 를 참조 하십시오.

## <a name="test-with-a-small-group-of-users-in-a-production-environment"></a>프로덕션 환경에서 소규모 사용자 그룹으로 테스트

프로덕션 환경에서 솔루션을 광범위 하 게 사용 하도록 설정 하기 전에 조직에서 필요한 준수, 개인 정보 보호 및 법적 검토를 수행 하는 동안 소수의 프로덕션 사용자 집합을 사용 하 여 정책을 테스트할 수 있습니다. 테스트 환경에서 참가자 위험 관리를 평가 하려면 시뮬레이트된 사용자 작업 및 처리를 위한 심사 및 사례에 대 한 알림을 만들기 위해 기타 신호를 생성 해야 합니다. 이 방법은 대부분의 조직에서 실용적이 지 않으므로 프로덕션 환경에서 소수의 사용자 그룹을 사용 하 여 참가자 위험 관리를 테스트 하는 것이 좋습니다.

이 테스트를 수행 하는 동안 참가자 위험 관리 콘솔에서 익명화 기능을 사용 하도록 설정 된 않지만 익명화 사용자 표시 이름으로 유지 하 여 도구 내에서 개인 정보를 유지 관리 합니다. 이 설정은 정책이 일치 하는 사용자의 개인 정보를 보호 하 고, 참가자 위험 경고에 대 한 데이터 조사 및 분석 검토에서 objectivity을 승격할 수 있도록 지원 합니다.

참가자 위험 관리 정책을 구성한 후 즉시 경고가 표시 되지 않으면 최소 위험 임계값이 아직 충족 되지 않았음을 의미할 수 있습니다. 정책이 트리거된 후 예상 대로 작동 하는지 확인 하는 좋은 방법은 사용자가 **사용자** 페이지에서 해당 정책에 대 한 범위 내에 있는지 확인 하는 것입니다.

## <a name="resources-for-stakeholders"></a>관련자를 위한 리소스

참가자 위험 관리 설명서를 관리 및 재구성 워크플로에 포함 된 조직의 관련자와 공유 합니다.

- [내부자 위험 정책 만들기 및 관리](insider-risk-management-policies.md)
- [내부자 위험 경고 조사](insider-risk-management-alerts.md)
- [내부자 위험 사례에 대한 작업 수행](insider-risk-management-cases.md)
- [참가자 위험 콘텐츠 탐색기를 사용 하 여 사례 데이터 검토](insider-risk-management-content-explorer.md)
- [내부자 위험 알림 서식 파일 만들기](insider-risk-management-notices.md)

## <a name="ready-to-get-started"></a>시작할 준비가 되셨습니까?

조직에 대 한 참가자 위험 관리를 구성할 준비가 되셨습니까? 다음 문서를 검토 합니다.

- 전역 정책 설정을 구성 하기 위한 [참가자 위험 관리 설정을 시작](insider-risk-management-settings.md) 합니다.
- 구성 요소를 구성 하 고 정책을 만들고 알림을 받기 시작 하기 위해 [참가자 위험 관리를 시작](insider-risk-management-configure.md) 합니다.
