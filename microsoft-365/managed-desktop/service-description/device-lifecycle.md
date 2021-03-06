---
title: Microsoft Managed Desktop 제품 수명 주기
description: 이 항목에는 Microsoft Managed Desktop에서 사용 되는 장치 사양이 나와 있습니다.
keywords: Microsoft Managed Desktop, Microsoft 365, 서비스, 문서
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 89dbf0e67c112743a557842bb32555d3a079743b
ms.sourcegitcommit: abf63669daf12993ad3353e4b578f41c8910b20f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2020
ms.locfileid: "47289796"
---
# <a name="microsoft-managed-desktop-product-lifecycle"></a>Microsoft Managed Desktop 제품 수명 주기

Microsoft Managed Desktop 이점은 사용자가 항상 최상의 성능, 안정성, 디자인 및 보안 기능을 제공 하는 장치 (예: Windows Hello와 같은 기능 지원)를 사용 하는 것을 보장 합니다. 이 작업을 수행 하기 위해 Microsoft Managed Desktop은 [승인 된 장치](device-list.md)를 지속적으로 업데이트 하는 짧은 카탈로그를 유지 관리 합니다. 
 
이 항목에서는 승인 된 카탈로그에서 장치가 추가 되거나 제거 될 때의 장치 수명 주기에 대해 자세히 설명 합니다. 

> [!NOTE]
> 이 항목에서는 "장치"와 "제품"을 구별 합니다. "장치"에서는 개별 컴퓨터를 하나씩만 의미 합니다. 예를 들어 "일련 번호 1234", "청구서의 랩톱", "공유 VM XYZ"는 특정 장치를 참조 합니다. 그러나 "제품" 이란 모음 또는 장치 패밀리를 나타냅니다. 예를 들어 "Fabrikam 랩탑", "Adatum ZX450 랩탑을" 등을 들 있습니다. 제품은 [승인 된 목록](device-list.md)또는 카탈로그에 추가 되 고 장치는 Microsoft Managed Desktop에 등록 되기 때문에 중요 한 역할을 합니다.

## <a name="product-lifecycle"></a>제품 수명 주기

 일반적으로 제품은 다음 수명 주기 단계로 이동 합니다.

- [제품 릴리스 및 평가](#product-release-and-evaluation)
- [제품 기본 가용성 기간](#product-primary-availability-period)
- [제품 유예 기간](#product-grace-period)
- [제품 폐기](#product-retirement)


다음 그림에서는 전체 시퀀스를 보여 줍니다.

![수명 주기 시간 표시 막대: 제품 일반 가용성부터 시작 하 여 "기본 가용성"은 2 년 동안 지속 됩니다. 이 시간 동안에는 인증 윈도우가 종료 되 고 특정 지점에서 장치가 등록 됩니다. 기본 가용성이 끝나면 제품이 보관 되 고 "유예 기간"이 3 년 후에 시작 됩니다. 시작 중에는 장치가 등록 때부터 관리에서 제거 될 때까지 3 년 동안 사용할 수 있습니다. 유예 기간이 끝나면 카탈로그에서 제품을 제거 합니다.](../../media/non-dark1-edits.PNG)

제품은 최대 24 개월 동안 카탈로그에 유지 되지만 <em>장치</em> 는 개별 등록 날짜에 따라 3 년 동안 관리 됩니다. 실제로 각 제품에는 세 가지 중요 한 날짜가 있지만 각 장치에는 하나만 있습니다. 제품의 경우 이러한 날짜 중 세 가지는 <em>승인 날짜</em>를 기준으로 계산 되므로 언제 든 지 승인 시에 해당 날짜를 게시 하 여 제품의 전체 수명 주기에 적절 하 게 사용할 수 있도록 합니다.

이 표에서는 이론적인 제품의 예제 날짜를 보여 줍니다.


|제품  |승인 날짜  |기본 가용성 종료  |자격의 끝  |
|---------|---------|---------|---------|
|Fabrikam 랩톱    | 1/1/2017 | 6/1/2019 | 6/1/2022 |
|Adatum 랩톱   | 1/1/2018 | 6/1/2020 | 6/1/2023  |

다음 표에는 이론적인 *장치*에 대 한 예제 날짜가 나와 있습니다.


|장치 ID  |등록 날짜  |퇴직 날짜  |
|---------|---------|---------|
|랩탑 #123412     |  2/3/2018       |  2/3/2021       |
|데스크톱 #321513     | 6/2/2018        |  6/2/2021       |


## <a name="product-release-and-evaluation"></a>제품 릴리스 및 평가

제품 수명 주기는 제조업체에서 제품을 공개적으로 출시할 때 시작 됩니다.

![릴리스 및 평가 기간을 보여 주는 수명 주기 시간 표시줄](../../media/non-dark3-edits.PNG)

이 단계에서 Microsoft Managed Desktop 공학적 팀은 제품의 평가 및 인증을 수행 합니다. 이 팀은 기타 다양 한 작업 중에 Windows와의 안정성 및 성능 (하드웨어 기준선, 시장 sentiment 및 재고 및 채널 준비 상태)과 같은 사항을 평가 합니다. 이 프로세스는 보통 6 주 정도 소요 됩니다.
  
Microsoft Managed Desktop은 처음 6 개월 이내에 인증 장치를 평가 합니다. 이렇게 하면 항상 최신 하드웨어 세대에 초점을 맞추어 작업을 진행 하 게 됩니다.
 
이 단계를 완료 하면 Microsoft Managed Desktop이 제품을 [승인 된 목록](device-list.md)에 추가 하 여 고객 enrollments 제품을 효과적으로 출시 합니다. 장치가 인증 된 날짜에 관계 없이 해당 **승인 된 날짜** 는 제품의 일반 사용 가능 날짜에 따라 다시 날짜가 지정 됩니다. 


## <a name="product-primary-availability-period"></a>제품 기본 가용성 기간

이 기간은 제품 가용성의 핵심입니다.

![기본 가용성을 보여 주는 수명 주기 시간 표시줄](../../media/non-dark4-edits.PNG)

이 기간 중에 등록 된 모든 장치에는 Microsoft Managed Desktop (파란색 시간 표시 막대)에서 지원 되는 3 년간의 모든 지원이 제공 됩니다. 이 기간은 일반 사용 가능 날짜 로부터 24 개월 후로 설정 될 때까지 지속 됩니다.

이 기간을 "열기 등록"으로 간주할 수 있으므로 Microsoft Managed Desktop의 값을 최대화 하려면 조달 모델을 대상으로 하 고 선택한 제품을이 기간 내에 포함 하도록 지정 해야 합니다. 예를 들어 고객은 기본 가용성의 마지막 달에 해당 하는 제품을 사용 하 여 2 년간의 settling을 방지 해야 하며, 이러한 장치 대부분은 Microsoft Managed 데스크톱 관리의 최대 3 년간 수신 되지 않습니다 (자세한 내용은 [유예 기간](#product-grace-period) 참조).  

## <a name="product-grace-period"></a>제품 유예 기간

제품 유예 기간은 기본 가용성을 따라 3 년 동안 진행 됩니다. 이 단계를 통해 지원 되는 제품군의 장치를 등록할 수 있지만 아직까지 Microsoft Managed Desktop을 보유 하 고 있는 하드웨어 및 장치 성능에 대 한 준비가 진행 됩니다. 이 단계는 Microsoft Managed Desktop에 대 한 정보를 파악 하기 전에 조달 의사 결정을 내리는 고객에 게 이상적입니다. 

Microsoft Managed Desktop에 등록 하기 전에 최근 많은 수의 승인 된 장치를 구매한 경우에도 등록할 수는 있지만, 3 년간의 관리 작업을 받을 수도 없습니다. 대신, 등록 시기에 관계 없이 만료 날짜가 준수 되지 않습니다. Microsoft Managed Desktop은 내부적으로 이러한 장치를 기본 가용성의 마지막 날에 등록 한 것 처럼 취급 합니다. 이 그림에서 이러한 시나리오는 다음과 같이 파란색 및 녹색 장치가 모두 같은 날에 종료 된다는 것을 볼 수 있습니다.


![유예 기간을 보여 주는 수명 주기 시간 표시줄](../../media/non-dark2-edits.PNG)

위 표에서 Fabrikam 랩톱 예제에는 다음과 같은 상황이 나와 있습니다. 

|제품  |승인 날짜  |기본 가용성 종료  |자격의 끝  |
|---------|---------|---------|---------|
|Fabrikam 랩톱    | 6/1/2017 | 6/1/2019 | 6/1/2022 |

고객은 6/1/2022까지 모든 방식으로 Fabrikam 랩톱을 등록할 수 있지만,이를 6/1/2019에 등록 한 것 처럼 취급 됩니다. Fabrikam 랩톱을 6/1/2021에 등록 하는 경우 1 년의 관리 작업만 받을 수 있습니다. 이 정책을 사용 하면 이전에 지원 했던 제품에서 부분 생명주을 추출할 수 있으며, 이러한 기능은 새로운 장치를 조기에 조달 하지 않아도 됩니다. 

마지막으로이 단계에서는 장치가 [장치 목록](device-list.md) 에서 제거 되 고 [보관 된 장치 목록](archived-device-list.md)으로 이동 됩니다.


## <a name="product-retirement"></a>제품 폐기

제품 폐기는 주기의 마지막 단계입니다. 이 단계에서는 해당 제품 유형의 새 장치를 Microsoft Managed Desktop에 등록할 수 없으며, 정의에 따라 모든 기존 장치가 허용 되는 3 년의 범위를 벗어납니다. 이 기간 동안 Microsoft Managed Desktop은 공용 목록에서 장치를 완전히 제거 합니다. 또한이 단계에서 아직 교체를 확보 하지 않은 경우에는 Microsoft Managed Desktop이 준수 하지 않는 장치에서 아래로 진입 하기 시작 하면 저하 된 서비스가 표시 되기 시작 합니다. 

## <a name="devices-that-are-out-of-compliance"></a>규정을 준수 하지 않는 장치

Microsoft Managed Desktop management에 허용 된 창이 경과 하면 장치가 준수 되지 않습니다. 장치가 3 년 동안 관리 되거나 해당 제품 유형이 장치 카탈로그에서 제거 될 때 발생 합니다. 현재 장치에 대 한 준수를 중단 하기 전에 새 장치를 배포 하는 것과 같은 조달 주기를 항상 대상으로 지정 해야 합니다.

Microsoft Managed Desktop 팀은 조달 주기가 길고 장기간 실행 되는 예산을 중심으로 계획 되는 것을 알 수 있습니다. 장치 채우기의 상태를 항상 확인 하려면 관리 되는 모든 장치, 해당 보존 기간 및 준수를 나타내는 상태를 나열 하는 [웹 사이트](https://aka.ms/mmdportal) 를 제공 합니다. 즉, 항상 장치 보존 기간에 대 한 최신 정보가 있으며, 모든 조달 계획 주기에서이 보고서를 사용할 수 있습니다. 







