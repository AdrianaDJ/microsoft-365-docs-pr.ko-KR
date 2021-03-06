---
title: SharePoint Online에서 포털 시작 롤아웃 계획 계획
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- SPO_Content
f1.keywords:
- CSH
ms.custom: Adm_O365
search.appverid:
- SPO160
- MET150
description: 이 문서에서는 SharePoint Online에서 포털 시작을 계획 하는 방법과 성공적인 시작을 위해 수행 해야 하는 단계에 대해 설명 합니다.
ms.openlocfilehash: e22fa4d9cbfed79841d844f111e3eb91a708512e
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692871"
---
# <a name="planning-your-portal-launch-roll-out-plan-in-sharepoint-online"></a>SharePoint Online에서 포털 시작 롤아웃 계획 계획

포털은 사이트에서 콘텐츠를 사용하는 다수의 사이트 방문자를 보유하는 인트라넷 상의 SharePoint 사이트입니다. 대규모 조직에서는 이들을 다수 보유할 수도 있습니다. 예를 들어 회사 포털과 HR 포털이 있습니다. 일반적으로 포털에서는 사이트와 해당 콘텐츠를 만들고 저술하는 사용자가 비교적 적습니다. 포털을 사용하는 대부분의 방문자는 콘텐츠를 읽고 사용하기만 합니다.

이 문서에서는 SharePoint Online으로의 배포 및 롤아웃 계획을 계획 하는 방법에 대해 설명 합니다. 또한 SharePoint Online에서는 일반적인 부하 테스트가 허용 되지 않으므로 수행 하는 방법도 제공 합니다. SharePoint Online은 클라우드 서비스 이며 부하 기능, 서비스의 전체 부하 균형은 Microsoft에 의해 관리 됩니다.

성공적인 포털을 만들려면 [정상 포털 만들기, 시작 및 유지 관리](https://go.microsoft.com/fwlink/?linkid=2105838) 에 설명 된 기본 원칙, 모범 사례 및 권장 사항을 따릅니다. 

배포 방법이 아래에 강조 표시 되어 있습니다.

## <a name="overview-of-capacity-planning-in-sharepoint-online"></a>SharePoint Online의 용량 계획 개요
어떤 팜에서 든 효율적으로 용량을 사용 하 고 예기치 않은 성장을 처리 하기 위해 특정 사용 시나리오를 추적 하는 자동화 기능을 제공 합니다. 한 팜의 모든 테 넌 트에 대해 정확한 증가를 예측할 수는 없지만 집계 된 요청의 합계는 시간이 지남에 따라 예측 가능 합니다. SharePoint Online의 성장 추세를 파악 하 여 향후 확장이 계획 될 수 있습니다. [용량 계획 및 부하 테스트 SharePoint Online](capacity-planning-and-load-testing-sharepoint-online.md)에 대 한 자세한 내용을 설명 합니다.

성공적인 시작의 주요 부분은 아래에 설명 된 "웨이브" 또는 "단계별 롤아웃" 접근 방식입니다. 

## <a name="can-i-load-test-sharepoint-online"></a>테스트 SharePoint Online을 로드할 수 있나요?
SharePoint Online은 팜 간에 균형이 조정 되는 공유 된 다중 tenanted 환경으로, 수평으로 조정 됩니다. 부하 테스트 확장 크기가 지속적으로 변경 되는 경우에는이를 제외 하 고 SharePoint Online과 같은 환경에서 예기치 않은 결과가 제공 되지만이는 허용 되지 않습니다. 

자세한 내용은 [용량 계획 및 부하 테스트 SharePoint Online를](capacity-planning-and-load-testing-sharepoint-online.md) 확인 하세요.

## <a name="optimize-pages-by-following-recommended-guidelines"></a>권장 지침에 따라 페이지 최적화
온-프레미스 배포의 페이지는 sharepoint online에 대 한 권장 지침에 따라 검토 하지 않고 SharePoint Online으로 이동 해서는 안 됩니다. 가장 좋은 방법은 조직의 모든 사용자가 사이트의 시작 지점으로 액세스 하 게 되는 사이트 또는 포털에 대해 언제 든 지 모든 홈 페이지를 최적화 하는 것입니다.

다음과 같은 몇 가지 기본 요인을 고려해 야 합니다.
- 온-프레미스 배포는 개체 캐시, 출력 캐시 및 blob 캐시와 같은 전통적인 서버 쪽 캐시를 활용할 수 있습니다. 클라우드의 토폴로지 차이를 통해 이러한 옵션은 대규모 차이로 인해 사용 하기에 적합 하지 않을 수도 있습니다.
- 클라우드 소비에 사용 되는 모든 페이지/기능/사용자 지정은 사용자의 배포 된 위치 뿐만 아니라 더 많은 대기 시간에 최적화 되어 있어 서로 다른 영역이 나 지역의 사용자가 보다 일관성 있는 환경을 유지할 수 있도록 해야 합니다. 클라우드는 최신 SharePoint의 경우를 비롯 하 여 배포 된 사용자 기본을 최적화 하기 위해 CDN (콘텐츠 배달 네트워크)과 같은 최적화 기능을 제공 하며, OOTB (마지막으로 알려진 양호한 (LKG)를 box (기본 제공) 웹 파트에서 활용 합니다.

### <a name="what-to-do"></a>수행할 작업:
 - SharePoint Online의 모든 사이트 페이지에 대해 지침 분석 및 제공을 지 원하는 Chromium 확장인 [페이지 진단 도구](https://aka.ms/perftool)를 사용 합니다. 이 기능은 사이트 소유자, 편집자, 관리자 및 개발자가 분석 및 최적화를 시작 하기 위한 출발점으로 설계 되었으므로 사용할 수 있습니다.
 - 또한 개발자는 최신 페이지의 브라우저에서 f12 브라우저 도구와 같은 개발 도구와 CTRL-F12를 함께 사용 해야 합니다. [Fiddler](https://www.telerik.com/download/fiddler) 은 페이지의 크기 가중치 (메가바이트 단위)와 전체 페이지 로드에 영향을 주는 통화 및 요소의 수를 검토 하는 데에도 사용할 수 있습니다. 

이 섹션은 페이지 최적화에 대 한 간략 한 요약입니다.  자세한 내용은  [정상 포털 만들기, 시작 및 유지 관리](https://go.microsoft.com/fwlink/?linkid=2105838)를 참조 하세요.

## <a name="follow-a-wave--phased-roll-out-approach"></a>물결/단계적 롤아웃 방식 준수
사이트 시작에 대 한 기존의 큰 느낌표 방식을 사용 하면 사용자 지정, 외부 원본, 서비스 또는 프로세스가 올바른 배율로 테스트 되었음을 확인할 수 없습니다. 이는 시작 하는 데 달이 걸리지만, 조직 규모에 따라 며칠 이상에 의존 하는 것이 좋습니다. 따라서 웨이브 롤아웃 계획 후에는 다음 단계로 진행 하기 전에 문제를 일시 중지 및 해결 하는 옵션을 제공 하므로 문제에 영향을 받는 사용자의 수가 줄어듭니다. 서비스는 사용 현황 및 예측 사용량을 기준으로 용량을 확장 하며, 시작을 알릴 필요가 없는 경우에는 지침을 따라 성공을 확인 해야 합니다.
  
다음 이미지에 표시 된 것 처럼, 초대 된 사용자 수가 실제로 사이트를 사용 하는 것 보다 훨씬 더 많은 경우가 많습니다. 이 이미지는 릴리스를 배포 하는 방법에 대 한 전략을 보여 줍니다. 이 방법을 사용 하면 대다수의 사용자에 게 표시 되기 전에 SharePoint 사이트를 개선 하는 방법을 확인할 수 있습니다.
  
![초대받은 사용자 및 활성 사용자를 보여 주는 그래프](../media/0bc14a20-9420-4986-b9b9-fbcd2c6e0fb9.png)
  
파일럿 단계에서는 조직이 신뢰 하 고 알고 있음을 사용자 로부터 피드백을 얻는 것이 좋습니다. 이렇게 하면 시스템을 사용 하는 방법과 수행 하는 방법을 측정할 수 있습니다.
  
각 물결 중에는 각 배포 전파가 진행 되는 동안 성능 뿐 아니라 기능에 대 한 사용자 의견도 수집 합니다. 이렇게 하면 시스템을 천천히 소개 하 고 시스템이 더 많이 사용 됨에 따라 개선 되는 이점이 있습니다. 또한이를 통해 사이트를 더 많은 사용자에 게 롤아웃할 수 있을 뿐만 아니라 페이지 최적화 지침에 따라 사용자에 게 긍정적인 환경을 제공 하는 방법으로 향상 된 부하에 대응할 수도 있습니다.

### <a name="what-to-do"></a>수행할 작업:
- 각 단계의 타이밍을 결정 하 고, 계속 하기 전에 조정 해야 하는 긴급 대책/일시 중지 기회를 확인 합니다.
- 사용 하도록 설정 하려는 첫 번째 사용자 그룹을 계획 하 여 앞으로 이동 하는 데 필요한 피드백을 받을 수 있도록 합니다. 즉, 가능한 경우 적절 한 시기에 피드백을 제공할 수 있는 활성 사용자 그룹을 선택 합니다.
- 각 물결을 계획할 때, 사용자가 5000 명 미만인 소규모 사용자 기지를 시작한 다음 각 물결을 진행 하면서 그룹 크기를 늘립니다. 이 방법을 사용 하면 지그재그형 방법을 만들고 필요한 경우 더 쉽게 일시 중단을 수행할 수 있습니다.
