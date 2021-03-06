---
title: 사례 연구-Contoso는 Microsoft 팀, Exchange 및 Yammer 통신에 대 한 비속어 (공격적인 언어 정책)를 빠르게 구성 합니다.
description: Contoso에 대 한 사례 연구 및 Microsoft 팀, Exchange Online 및 Yammer 통신에서 악의적인 언어를 모니터링 하도록 통신 준수 정책을 신속 하 게 구성 하는 방법을 설명 합니다.
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- remotework
search.appverid:
- MET150
- MOE150
ms.openlocfilehash: 9c20b322d4da0339d7c8711abcee38f19f556423
ms.sourcegitcommit: abf63669daf12993ad3353e4b578f41c8910b20f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2020
ms.locfileid: "47289391"
---
# <a name="case-study---contoso-quickly-configures-an-offensive-language-policy-for-microsoft-teams-exchange-and-yammer-communications"></a>사례 연구-Contoso는 Microsoft 팀, Exchange 및 Yammer 통신에 대 한 비속어 (공격적인 언어 정책)를 빠르게 구성 합니다.

Microsoft 365의 통신 준수는 조직에서 부적절 한 메시지를 감지, 캡처 및 관리 하 여 통신 위험을 최소화 하는 데 도움이 됩니다. 미리 정의 된 정책 및 사용자 지정 정책을 사용 하면 정책 일치에 대 한 내부 및 외부 통신을 검색 하 여 지정한 검토자가 검사할 수 있습니다. 검토자는 조직에서 스캔 한 전자 메일, Microsoft 팀, Yammer 또는 타사 통신을 조사 하 고 적절 한 교정 작업을 수행 하 여 조직의 메시지 표준을 준수 하도록 할 수 있습니다.

Contoso Corporation은 공격적인 언어를 모니터링 하도록 정책을 빠르게 구성 해야 하는 가상 조직입니다. Microsoft 365은 주로 전자 메일, Microsoft 팀 및 Yammer 지원을 위해 사용 되었지만 작업 공간 harassment에 회사 정책을 적용 하기 위한 새로운 요구 사항이 있습니다. Contoso IT 관리자 및 준수 전문가는 Microsoft 365의 기본 작업에 대 한 기본적인 지식을 이해 하 고 있으며, 통신 준수를 빠르게 시작 하는 방법에 대 한 종단 간 지침을 찾고 있습니다.

이 사례 연구에서는 악의적인 언어에 대 한 통신을 모니터링 하기 위한 통신 준수 정책을 빠르게 구성 하는 기본 사항을 다룹니다. 이 지침에는 다음이 포함 됩니다.

- 1 단계-통신 준수 계획
- 2 단계-Microsoft 365의 통신 준수에 액세스
- 3 단계-필수 구성 요소 구성 및 통신 준수 정책 만들기
- 4 단계-알림 조사 및 업데이트 관리

## <a name="step-1-planning-for-communication-compliance"></a>1 단계: 통신 준수 계획

Contoso IT administrators 및 규정 준수 전문가는 Microsoft 365의 규정 준수 솔루션에 대 한 온라인 웹 세미나 통신 준수 정책을 통해 작업 공간 harassment를 줄이기 위한 업데이트 된 회사 정책 요구 사항을 충족 하도록 했습니다. 공동 작업에서는 Microsoft 팀, 개인 메시지 및 커뮤니티 대화, 그리고 Exchange Online에서 전송 되는 전자 메일 메시지에서 보낸 채팅에 대 한 악의적인 언어를 모니터링 하는 통신 준수 정책을 만들고 사용 하도록 설정 하는 계획을 개발 했습니다. 계획에는 다음이 포함 됩니다.

- 통신 준수 기능에 액세스 해야 하는 IT 관리자
- 통신 정책을 만들고 관리 해야 하는 준수 전문가
- 준수 전문가 및 기타 부서의 기타 부서 (인적 자원, 법률 등)에서 통신 준수 알림을 조사 하 고 수정 해야 하는 기타 동료입니다.
- 통신 준수 공격적인 언어 정책에 대 한 범위 내에 속하는 사용자입니다.

### <a name="licensing"></a>라이선싱

첫 번째 단계는 Contoso의 Microsoft 365 라이선스에 통신 준수 솔루션에 대 한 지원이 포함 되어 있는지 확인 하는 것입니다. 통신 준수를 액세스 하 고 사용 하려면 Contoso IT 관리자는 Contoso에 다음 중 하나가 포함 되어 있는지 확인 해야 합니다.

- Microsoft 365 E5 구독 (유료 또는 평가판 버전)
- Microsoft 365 E3 구독 + Microsoft 365 E5 준수 추가 기능
- Microsoft 365 E3 구독 + Microsoft 365 E5 참가자 위험 관리 추가 기능
- Microsoft 365 A5 구독 (유료 또는 평가판 버전)
- Microsoft 365 A3 구독 + Microsoft 365 A5 규정 준수 추가 기능
- Microsoft 365 A3 구독 + Microsoft 365 A5 참가자 위험 관리 추가 기능
- Microsoft 365 G5 구독 (유료 또는 평가판 버전)
- Microsoft 365 G5 구독 + Microsoft 365 G5 준수 추가 기능
- Microsoft 365 G5 subscription + Microsoft 365 G5 Insider 위기 관리 추가 기능
- Office 365 Enterprise E5 구독 (유료 또는 평가판 버전)
- Office 365 Enterprise E3 구독 + Office 365 고급 준수 추가 기능 (새 구독에 더 이상 사용할 수 없음)

또한 통신 준수 정책에 포함 된 사용자에 게 위의 라이선스 중 하나를 할당 해야 한다는 것을 확인 해야 합니다.

>[!IMPORTANT]
>Office 365 고급 규정 준수는 더 이상 독립 실행형 구독으로 판매 되지 않습니다. 현재 구독이 만료 되 면 고객은 위의 구독 중 하나로 전환 해야 하며, 이러한 기능은 동일 하거나 추가 준수 기능이 포함 되어 있습니다.

Contoso IT 관리자는 다음 단계를 수행 하 여 Contoso에 대 한 라이선스 지원을 확인 합니다.

1. IT 관리자가 **microsoft 365 관리 센터** [ https://admin.microsoft.com) ](https://admin.microsoft.com) 에 로그인 하 고 **microsoft 365 관리 센터**  >  **청구**  >  **라이선스로**이동 합니다.

2. 여기서는 통신 준수에 대 한 지원을 포함 하는 [라이선스 옵션](https://docs.microsoft.com/microsoft-365/compliance/communication-compliance-configure?view=o365-worldwide#before-you-begin) 중 하나가 있는지 확인 합니다.

![통신 준수 라이선스](../media/communication-compliance-case-licenses.png)

### <a name="permissions-for-communication-compliance"></a>통신 준수에 대 한 사용 권한

통신 준수 기능을 관리 하기 위한 권한을 구성 하는 데 사용 되는 역할 그룹에는 다섯 가지가 있습니다. **통신 준수** 를 Microsoft 365 준수 센터에서 메뉴 옵션으로 사용할 수 있도록 하 고 이러한 구성 단계를 계속 하려면 Contoso 관리자에 게 *통신 준수 관리자* 역할이 할당 되어 있어야 합니다.

Contoso *는 통신 준수 역할 그룹* 을 사용 하 여 모든 통신 준수 관리자, 분석가, investigators 및 뷰어를 그룹에 할당 하기로 결정 합니다. 이렇게 하면 Contoso에서 더 쉽게 작업을 수행 하 고 준수 관리 요구 사항에 적합 합니다.

|**역할**|**역할 권한**|
|:-----|:-----|
| **통신 준수** | 이 역할 그룹을 사용 하 여 단일 그룹의 조직에 대 한 통신 준수를 관리 합니다. 지정 된 관리자, 분석가, investigators 및 뷰어에 대 한 모든 사용자 계정을 추가 하 여 단일 그룹에서 통신 준수 권한을 구성할 수 있습니다. 이 역할 그룹에는 모든 통신 준수 권한 역할이 포함 되어 있습니다. 이 구성은 서로 다른 사용자 그룹에 대해 정의 된 별도의 사용 권한이 필요 하지 않은 조직에 적합 하며 통신 준수를 빠르게 시작할 수 있는 가장 쉬운 방법입니다. |
| **통신 준수 관리자** | 이 역할 그룹을 사용 하 여 초기에 통신 준수 관리자를 정의 된 그룹으로 세분 하 고 의사 소통 준수를 구성 합니다. 이 역할 그룹에 할당 된 사용자는 통신 준수 정책, 전역 설정 및 역할 그룹 할당을 만들고, 읽고, 업데이트 하 고, 삭제할 수 있습니다. 이 역할 그룹에 할당 된 사용자는 메시지 알림을 볼 수 없습니다. |
| **통신 준수 분석가** | 이 그룹을 사용 하 여 통신 준수 분석가 역할을 하는 사용자에 게 사용 권한을 할당 합니다. 이 역할 그룹에 할당 된 사용자는 검토자로 할당 되는 정책, 메시지 메타 데이터를 보거나, 추가 검토자에 게 승격 하거나, 사용자에 게 알림을 보낼 수 있습니다. 분석가가 보류 중인 알림을 확인할 수 없습니다. |
| **통신 준수 Investigator** | 이 그룹을 사용 하 여 통신 준수 investigators 역할을 할 사용자에 게 사용 권한을 할당 합니다. 이 역할 그룹에 할당 된 사용자는 메시지 메타 데이터와 콘텐츠를 보고, 추가 검토자에 게 에스컬레이션 하며, 고급 eDiscovery 사례로 에스컬레이션 하 고, 사용자에 게 알림을 보내며, 경고를 해결할 수 있습니다. |
| **통신 준수 뷰어** | 이 그룹을 사용 하 여 통신 보고서를 관리할 사용자에 게 사용 권한을 할당 합니다. 이 역할 그룹에 할당 된 사용자는 통신 준수 홈 페이지의 모든 보고 widget에 액세스 하 고 모든 통신 준수 보고서를 볼 수 있습니다. |

1. Contoso IT 관리자는 **Office 365 보안 & 준수 센터** 사용 권한 페이지 (전역 관리자 계정의 자격 증명을 사용 하 여 [) https://protection.office.com/permissions) ](https://protection.office.com/permissions) 에 로그인 하 고 Microsoft 365에서 역할을 확인 하 고 관리 하는 링크를 선택 합니다.
2. **보안 & 준수 센터**에서 **사용 권한** 으로 이동 하 여 Office 365에서 역할을 보고 관리 하는 링크를 선택 합니다.
3. 관리자가 *통신 준수* 역할 그룹을 선택한 다음 **역할 그룹 편집**을 선택 합니다.
4. 관리자가 왼쪽 탐색 창에서 **구성원 선택을** 선택 하 고 **편집**을 선택 합니다.
5. **추가** 를 선택한 다음 통신 준수, 조사 및 검토를 관리 하는 모든 Contoso 사용자에 대 한 확인란을 선택 합니다.
6. 관리자가 **추가**를 선택한 다음 **완료**를 선택 합니다.
7. 이 경우 **저장** 을 선택 하 여 Contoso 사용자를 역할 그룹에 추가 합니다. **닫기를** 선택 하 여 단계를 완료 합니다.

## <a name="step-2-accessing-communication-compliance-in-microsoft-365"></a>2 단계: Microsoft 365의 통신 준수에 액세스

통신 준수에 대 한 사용 권한을 구성 하 고 나면, Contoso IT administrators 및 준수 전문가가 통신 준수 역할 그룹에 할당 하 여 Microsoft 365의 통신 준수 솔루션에 액세스할 수 있습니다. Contoso IT 관리자 및 준수 전문가는 통신 준수에 액세스 하 고 새 정책 만들기를 시작할 수 있는 몇 가지 방법을 제공 합니다.

- 통신 준수 솔루션에서 직접 시작
- Microsoft 365 준수 센터에서 시작
- Microsoft 365 솔루션 카탈로그에서 시작
- Microsoft 365 관리 센터에서 시작

### <a name="starting-directly-from-the-communication-compliance-solution"></a>통신 준수 솔루션에서 직접 시작

솔루션에 액세스 하는 가장 빠른 방법은 **Communication 준수** () 솔루션에 직접 로그인 하는 것입니다 <https://compliance.microsoft.com/supervisoryreview> . 이 링크를 사용 하 여 Contoso IT 관리자 및 준수 전문가는 알림 상태를 빠르게 검토 하 고 미리 정의 된 템플릿에서 새 정책을 만들 수 있는 통신 준수 개요 대시보드로 향합니다.

![통신 준수 개요](../media/communication-compliance-case-overview.png)

### <a name="starting-from-the-microsoft-365-compliance-center"></a>Microsoft 365 준수 센터에서 시작

Contoso IT 관리자 및 준수 전문가가 통신 준수 솔루션에 액세스 하는 또 다른 쉬운 방법은 **Microsoft 365 준수 센터** [() https://compliance.microsoft.com) ](https://compliance.microsoft.com)에 직접 로그인 하는 것입니다. 로그인 한 후에는 모든 준수 솔루션을 표시 하려면 **모두 표시** 컨트롤을 선택 하 고 시작 하려면 **통신 준수** 솔루션을 선택 하기만 하면 됩니다.

![준수 센터](../media/communication-compliance-case-center.png)

### <a name="starting-from-the-microsoft-365-solution-catalog"></a>Microsoft 365 솔루션 카탈로그에서 시작

Contoso IT 관리자 및 규정 준수 전문가는 Microsoft 365 솔루션 카탈로그를 선택 하 여 통신 준수 솔루션에 액세스할 수도 있습니다. **Microsoft 365 준수 센터**에서 왼쪽 탐색 창의 **솔루션** 섹션에서 **카탈로그** 를 선택 하면 모든 microsoft 365 준수 솔루션을 나열 하는 솔루션 카탈로그를 열 수 있습니다. Contoso IT 관리자는 **참가자 위험 관리** 섹션으로 스크롤한 후 시작 하기 위한 통신 준수를 선택할 수 있습니다. 또한 Contoso IT 관리자는 탐색에 표시 기능을 사용 하 여 통신 준수 솔루션을 왼쪽 탐색 창에 고정 하 여 향후 로그인 할 때 빠르게 액세스할 수 있도록 결정 합니다.

![솔루션 카탈로그](../media/communication-compliance-case-solution.png)

### <a name="starting-from-the-microsoft-365-admin-center"></a>Microsoft 365 관리 센터에서 시작

Microsoft 365 [관리 센터 https://admin.microsoft.com) 에서](https://admin.microsoft.com) 시작할 때의 통신 준수에 액세스 하려면 Contoso IT 관리자 및 준수 전문가가 microsoft 365 관리 센터에 로그인 하 고 **microsoft 365 관리 센터**  >  **규정 준수**로 이동 합니다.

![통신 준수 링크](../media/communication-compliance-case-compliance-link.png)

이 작업을 수행 하면 **Office 365 보안 및 준수 센터가**열리고 페이지 맨 위에 있는 배너에 제공 된 **Microsoft 365 준수 센터** 에 대 한 링크를 선택 해야 합니다.

![Office 365 보안 및 준수 센터](../media/communication-compliance-case-scc.png)

**Microsoft 365 준수 센터**에서 Contoso IT 관리자는 **모두 표시** 를 선택 하 여 준수 솔루션의 전체 목록을 표시 합니다.

![통신 준수 메뉴](../media/communication-compliance-case-show-all.png)

**모두 표시**를 선택한 후에는 Contoso IT 관리자가 통신 준수 솔루션에 액세스할 수 있습니다.

![통신 준수 개요](../media/communication-compliance-case-overview.png)

## <a name="step-3-configuring-prerequisites-and-creating-a-communication-compliance-policy"></a>3 단계: 필수 구성 요소 구성 및 통신 준수 정책 만들기

통신 준수 정책을 시작 하려면 Contoso IT 관리자가 공격적인 언어를 모니터링 하기 위해 새 정책을 설정 하기 전에 구성 해야 하는 몇 가지 필수 구성 요소가 있습니다. 이러한 필수 구성 요소가 완료 되 면 Contoso IT 관리자 및 준수 전문가가 새 정책을 구성 하 고, 규정 준수 전문가는 조사를 시작 하 고 생성 된 모든 경고를 수정 수 있습니다.

### <a name="enabling-auditing-in-microsoft-365"></a>Microsoft 365에서 감사 사용

통신 준수를 위해서는 감사 로그가 알림을 표시 하 고 검토자가 수행한 업데이트 관리 작업을 추적 해야 합니다. 감사 로그는 정의 된 조직 정책과 관련 된 모든 활동을 요약 한 것 이거나, 통신 준수 정책이 변경 된 경우에도 발생 합니다.

Contoso IT 관리자는 감사를 설정 하는 단계별 [지침](https://docs.microsoft.com/microsoft-365/compliance/turn-audit-log-search-on-or-off) 을 검토 하 고 완료 합니다. 감사를 설정한 후에는 감사 로그를 준비 중 이며 준비 완료 후 몇 시간 내에 검색을 실행할 수 있음을 알리는 메시지가 표시 됩니다. Contoso IT 관리자는이 작업을 한 번만 수행 하면 됩니다.

### <a name="configuring-yammer-tenant-for-native-mode"></a>기본 모드에 대 한 Yammer 테 넌 트 구성

통신 규정을 준수 하려면 조직에 대 한 Yammer 테 넌 트를 전용 모드로 사용 하 여 비공개 메시지 및 공용 커뮤니티 대화에서 비속어를 모니터링 해야 합니다.

Contoso IT 관리자는 [microsoft 365 문서의 Yammer 기본 모드 개요](https://docs.microsoft.com/yammer/configure-your-yammer-network/overview-native-mode) 에 나와 있는 정보를 검토 하 고 [Microsoft 365 용 기본 모드에 맞게 yammer 네트워크 구성](https://docs.microsoft.com/yammer/configure-your-yammer-network/native-mode) 문서에서 마이그레이션 도구를 실행 하는 단계를 수행 하는 방법을 확인 하세요.

### <a name="setting-up-a-group-for-in-scope-users"></a>범위 내 사용자에 대 한 그룹 설정

Contoso 준수 전문가는 모든 사용자에 게 공격적인 언어를 모니터링할 통신 정책에 추가 하려고 합니다. 각 사용자 계정을 개별적으로 정책에 추가할지 결정 했지만이 정책에 대 한 사용자의 **모든 사용자** 메일 그룹을 사용 하는 데 필요한 시간을 단축 합니다.

모든 Contoso 사용자를 포함 하도록 새 그룹을 만들어야 하는 경우 다음 단계를 수행 해야 합니다.

1. Contoso it 관리자는 **microsoft 365 관리 센터** [ https://admin.microsoft.com) ](https://admin.microsoft.com) 에 로그인 하 고 **microsoft 365 관리 센터**  >  **그룹**  >  **그룹**으로 이동 합니다.
2. **그룹 추가** 를 선택 하 고 마법사를 완료 하 여 새 *Microsoft 365 그룹* 또는 *메일 그룹*을 만듭니다.

    ![그룹](../media/communication-compliance-case-all-employees.png)

3. 새 그룹을 만든 후에는 모든 Contoso 사용자를 새 그룹에 추가 해야 합니다. **Exchange 관리 센터** [ https://outlook.office365.com/ecp) 를 열고](https://outlook.office365.com/ecp) **exchange 관리 센터**  >  **받는 사람**  >  **그룹**으로 이동 합니다. Contoso IT 관리자는 구성원 영역 및 새로 만든 *모든 직원* 그룹을 선택 하 고 **편집** 컨트롤을 선택 하 여 마법사에서 새 그룹에 모든 Contoso 사용자를 추가 합니다.

    ![Exchange 관리 센터](../media/communication-compliance-case-eac.png)

### <a name="creating-the-policy-to-monitor-for-offensive-language"></a>공격적인 언어에 대해 모니터링할 정책 만들기

모든 필수 구성 요소가 완료 되 면 IT 관리자와 Contoso 규정 준수 전문가가 공격적인 언어를 모니터링 하도록 통신 준수 정책을 구성할 준비가 되었습니다. 새로운 공격적인 언어 정책 템플릿을 사용 하 여이 정책을 구성 하는 것은 간단 하 고 빠른 방법입니다.

1. Contoso IT 관리자 및 준수 전문가가 **Microsoft 365 준수 센터** 에 로그인 하 고 왼쪽 탐색 창에서 **통신 준수** 를 선택 합니다. 이 작업을 수행 하면 통신 준수 정책 서식 파일에 대 한 빠른 링크가 있는 **개요** 대시보드가 열립니다. 서식 파일에 대해 **시작** 을 선택 하 여 **공격적인 언어 서식 파일에 대 한 모니터** 를 선택 합니다.

    ![공격에 적합 한 통신 준수 언어 서식 파일](../media/communication-compliance-case-template.png)

2. 정책 서식 파일 마법사에서 Contoso IT 관리자 및 준수 전문가가 공동 작업을 통해 **정책 이름**, **사용자 또는 그룹 감독할**및 **검토자**의 세 가지 필수 필드를 완성 합니다.
3. 정책 마법사에서 정책 이름을 이미 제안 했으므로 IT 관리자 및 준수 전문가가 제안 된 이름을 유지 하 고 나머지 필드에 포커스를 둡니다. **감독할 사용자 또는 그룹** 에 대 한 *모든 사용자* 그룹을 선택 하 고 **검토자** 필드에 대 한 정책 알림을 조사 및 수정 해야 하는 준수 전문가를 선택 합니다. 정책을 구성 하 고 경고 정보 수집을 시작 하는 마지막 단계는 **정책 만들기**를 선택 하는 것입니다.

    ![원하지 않는 통신 준수 언어 마법사](../media/communication-compliance-case-wizard.png)

## <a name="step-4-investigate-and-remediate-alerts"></a>4 단계: 알림 검사 및 수정

이제 공격적인 언어를 모니터링 하기 위한 통신 준수 정책이 구성 되었으므로 Contoso 준수 전문가의 다음 단계는 정책에 의해 생성 된 경고를 조사 하 고 수정 하는 것입니다. 정책이 모든 통신 원본 채널의 통신을 완벽 하 게 처리 하 고 경고 **대시보드에**경고가 표시 되는 데 최대 24 시간이 소요 됩니다.

경고가 생성 되 면 Contoso 준수 전문가가 [워크플로 지침](https://docs.microsoft.com/microsoft-365/compliance/communication-compliance-investigate-remediate) 에 따라 공격적인 언어 문제를 조사 하 고 수정 합니다.