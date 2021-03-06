---
title: Advanced eDiscovery에서 관련성 분석 테스트
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
ms.date: 09/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: Advanced eDiscovery의 일괄 계산 후 테스트 탭을 사용 하 여 전체 처리 품질을 테스트 및 비교 하 고 유효성을 검사 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: c5a885b3483b9ce319fffefa55037c0c2c8f3c85
ms.sourcegitcommit: c43ebb915fa0eb7eb720b21b62c0d1e58e7cde3d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/30/2020
ms.locfileid: "44936211"
---
# <a name="test-relevance-analysis-in-advanced-ediscovery-classic"></a>Advanced eDiscovery에서 관련성 분석 테스트 (클래식)

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
고급 eDiscovery의 테스트 탭에서는 전체 처리 품질을 테스트 및 비교 하 고 유효성을 검사할 수 있습니다. 이러한 테스트는 일괄 계산 후에 수행 됩니다. 전문가는 컬렉션의 파일에 태그를 지정 하 여 태그 있는 각 파일이 실제로 대/소문자와 관련성이 있는지 여부를 최종 판단 합니다. 
  
단일 및 다중 문제 시나리오에서는 일반적으로 각 문제와 관련 된 테스트를 수행 합니다. 각 테스트 후에 결과를 볼 수 있으며, 지정 된 샘플 테스트 파일을 사용 하 여 테스트 결과를 다시 수정할 수 있습니다.
  
## <a name="testing-the-rest"></a>나머지 테스트

"Rest 테스트" 테스트를 통해 최종 고급 eDiscovery 결과를 기준으로 특정 관련성 구분 점수 위에 있는 파일만 검토 하는 등의 culling 의사 결정을 확인할 수 있습니다. 전문가는 선택한 구분 점수 아래의 파일 샘플을 검토 하 여 해당 집합 내의 관련 파일 수를 평가 합니다.
  
이 테스트에서는 검토 집합 간 통계 및 비교를 제공 하 고 나머지 채우기를 테스트 합니다. 검토 집합의 결과는 교육 중에 관련성에 따라 계산 됩니다. 결과에는 다음과 같은 설정 및 입력 매개 변수에 따른 계산이 포함 됩니다.
  
- 샘플 및 식별 된 관련 파일의 파일 수에 대 한 샘플 통계를 테스트 합니다. 
    
- 테이블 형식 및 검토 집합의 인구 매개 변수와 나머지 부분 (예: 파일 수, 예상 되는 관련 파일의 수, 예상 되는 다양성, 추가 관련 파일을 찾는 데 걸리는 평균 비용)을 비교 합니다. Cost 매개 변수 설정은 관리자가 설정할 수 있습니다.
    
1. **관련성 \> 테스트** 탭을 엽니다. 
    
2. **테스트** 탭에서 **새 테스트**를 클릭 합니다. 다음 예와 같이 **테스트 만들기** 대화 상자가 표시 됩니다. 
    
    ![나머지 결과 테스트 하는 관련성](../media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. **테스트 이름**및 **설명**에 이름과 설명을 입력 합니다.
    
4. **테스트 유형** 목록에서 **나머지 테스트를 선택 합니다** .
    
5. **문제/범주** 목록에서 문제점 이름을 선택 합니다. 
    
6. **로드** 목록에서 부하를 선택 합니다. 
    
7. **읽기%** 에서 기본값을 수락 하거나 구분 기준 점수 매기기 값을 선택 합니다. 
    
8. **설정**하거나 기본값을 그대로 사용 합니다. 복원 아이콘은 기본값을 복원 합니다.
    
9. **태그 지정 시작**을 클릭 합니다. 테스트 샘플이 생성 됩니다.
    
10. **관련성 \> 태그** 탭에서 각 파일을 검토 하 고 태그를 만들었으면 완료 되 면 **계산**을 클릭 합니다.
    
11. 테스트 탭에서 **결과 보기** 를 클릭 하 여 테스트 결과를 볼 수 있습니다. 다음 그림에 예가 나와 있습니다. 
    
    ![나머지 결과 테스트 합니다.](../media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
위 그림에서 표의 **샘플 매개 변수** 섹션에는 전문가가 태그를 지정 하는 샘플의 파일 수와 해당 예제에 나와 있는 관련 파일의 수에 대 한 자세한 정보가 포함 되어 있습니다. 
  
테이블의 **인구 매개 변수** 섹션에는 선택한 구분 아래에 점수가 있는 파일의 검토 집합 및 선택한 구분 위에 점수가 있는 파일의 "나머지"를 포함 하는 테스트 결과가 포함 됩니다. 각 모집단에 대해 다음 결과가 표시 됩니다. 
  
- % 규정 된 읽기 전용 구분이 있는 파일 포함
    
- 총 파일 수 
    
- 예상 되는 관련 파일의 수 
    
- 예측 된 다양성 
    
- 다른 관련 파일을 찾기 위한 평균 검토 비용
    
## <a name="testing-the-slice"></a>조각 테스트

"조각 테스트" 테스트는 "Rest 테스트" 테스트와 비슷한 테스트를 수행 하지만 관련성 읽기%로 지정 된 파일 집합의 세그먼트에 해당 합니다.
  
1. **관련성 \> 테스트** 탭을 엽니다. 
    
2. **테스트** 탭에서 **새 테스트**를 클릭 합니다. **테스트 만들기** 대화 상자가 표시 됩니다. 
    
3. **테스트 이름** 및 **설명**에 정보를 입력 합니다.
    
4. **테스트 유형** 목록에서 **조각 테스트**를 선택 합니다.
    
5. **문제점** 목록에서 문제점 이름을 선택 합니다. 
    
6. **로드** 목록에서 부하를 선택 합니다. 
    
7. 다음 **사이에 읽기%** 에서 기본 하한값 및 high 범위 값을 적용 하거나 값 구분 점수를 선택 합니다. 
    
8. **크기 설정**에서 값을 선택 하거나 기본값을 그대로 사용 합니다.
    
    복원 아이콘은 기본값을 복원 합니다.
    
9. **태그 지정 시작**을 클릭 합니다. 테스트 샘플이 생성 됩니다.
    
10. **관련성 \> 태그** 탭에서 각 파일을 검토 하 고 태그를 만들었으면 완료 되 면 **계산**을 클릭 합니다. 
    
11. 테스트 탭에서 **결과 보기** 를 클릭 하 여 테스트 결과를 볼 수 있습니다. 
    
## <a name="see-also"></a>참고 항목

[고급 eDiscovery (클래식)](office-365-advanced-ediscovery.md)
  
[관련성 평가 이해](assessment-in-relevance-in-advanced-ediscovery.md)
  
[태그 지정 및 평가](tagging-and-assessment-in-advanced-ediscovery.md)
  
[태그 지정 및 관련성 교육](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[관련성 분석 추적](track-relevance-analysis-in-advanced-ediscovery.md)
  
[결과를 기준으로 결정](decision-based-on-the-results-in-advanced-ediscovery.md)

