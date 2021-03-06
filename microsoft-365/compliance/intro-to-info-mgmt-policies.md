---
title: 정보 관리 정책 소개
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 5/16/2014
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- WSU150
- SPO160
- OSU150
- MET150
ms.assetid: 63a0b501-ba59-44b7-a35c-999f3be057b2
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: 정보 관리 정책을 사용 하 여 콘텐츠가 보존 되는 시간 또는 사용자가 해당 콘텐츠에 대해 수행할 수 있는 작업을 제어 하 고 추적 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: dfb1aeb3dbd3a2b17f18bbd03d5f4d3e198e4c47
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44815515"
---
# <a name="introduction-to-information-management-policies"></a>정보 관리 정책 소개

정보 관리 정책은 콘텐츠 형식에 대한 규칙 집합입니다. 조직에서는 정보 관리 정책을 사용하여 콘텐츠의 보존 기간이나 사용자가 해당 콘텐츠에 대해 수행할 수 있는 작업과 같은 사항을 제어하고 추적할 수 있습니다. 정보 관리 정책은 조직이 법률 또는 정부 규정을 준수하도록 도와주거나 내부 비즈니스 프로세스를 적용할 수 있습니다. 
  
예를 들어 해당 금융 기관에 대 한 "적절 한 제어"를 시연 해야 하는 정부 규정을 따라야 하는 조직에서는 재무 관련 문서에 대 한 작성 및 승인 프로세스의 특정 작업을 감사 하는 하나 이상의 정보 관리 정책을 만들 수 있습니다.
  
방법 정보는 [Create and apply information management 정책도](create-info-mgmt-policies.md)을 참조 하십시오.
  
## <a name="features-of-information-management-policies"></a>정보 관리 정책의 기능
<a name="__top"> </a>

조직에서 콘텐츠 및 프로세스를 관리 하기 위해 개별적으로 또는 조합 하 여 사용할 수 있는 미리 정의 된 정책 기능에는 네 가지 기본 범주가 있습니다. 
  
![콘텐츠 정책 유형](../media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
감사 정책 기능을 사용 하면 조직에서 문서 및 목록 항목에 대해 수행 되는 이벤트 및 작업을 기록 하 여 해당 콘텐츠 관리 시스템을 사용 하는 방법을 분석할 수 있습니다. 감사 정책 기능을 구성 하 여 문서 또는 항목을 편집, 표시, 체크 인, 체크 아웃 또는 삭제 하거나 사용 권한을 변경한 경우와 같은 이벤트를 기록할 수 있습니다. 모든 감사 정보는 서버의 단일 감사 로그에 저장 되며 사이트 관리자가 해당 서버에서 보고서를 실행할 수 있습니다. 
  
만료 정책 기능은 조직이 일정 한 trackable 방식으로 사이트에서 오래 된 콘텐츠를 삭제 하거나 제거 하는 데 도움이 됩니다. 이렇게 하면 오래 된 콘텐츠를 보존 하는 데 드는 비용과 위험을 모두 관리할 수 있습니다. 특정 날짜나 문서를 만들거나 마지막으로 수정한 후 일정 시간 내에 해당 유형의 콘텐츠를 만료 하도록 지정 하는 만료 정책을 구성할 수 있습니다.
  
조직에서 특정 필요에 맞는 사용자 지정 정책 기능을 만들어 배포할 수도 있습니다. 예를 들어 제조 조직에서는 사용자가 보안 되지 않은 프린터로 이러한 문서의 복사본을 인쇄 하지 못하도록 하는 모든 초안 제품 디자인 사양 문서에 대 한 정보 관리 정책을 정의할 수 있습니다. 이러한 유형의 정보 관리 정책을 정의 하기 위해 제품 디자인 사양 콘텐츠 형식에 대 한 관련 정보 관리 정책에 추가할 수 있는 인쇄 제한 정책 기능을 만들고 배포할 수 있습니다.
  
## <a name="locations-to-use-an-information-management-policy"></a>정보 관리 정책을 사용할 위치
<a name="__toc340213528"> </a>

정보 관리 정책을 구현 하려면이를 사이트의 목록, 라이브러리 또는 콘텐츠 형식에 추가 해야 합니다. 정보 관리 정책을 만들거나 추가 하는 위치는 정책이 적용 되는 범위나 사용할 수 있는 크기에 영향을 줍니다. 다음을 수행할 수 있습니다.
  
 **사이트 모음 정책을 만들고이 정책을 콘텐츠 형식, 목록 또는 라이브러리에 추가** 사이트 모음의 최상위 사이트에 있는 정책 목록에서 사이트 모음 정책을 만들 수 있습니다. 사이트 모음 정책을 만든 후에는 다른 사이트 모음의 관리자가 해당 정책 목록으로 가져올 수 있도록 내보낼 수 있습니다. 내보낼 수 있는 사이트 모음 정책을 만들면 조직의 여러 사이트에서 정보 관리 정책을 표준화 하는 데 도움이 됩니다. 
  
사이트 콘텐츠 형식에 사이트 모음 정책을 추가 하 고 해당 사이트 콘텐츠 형식의 인스턴스를 목록 또는 라이브러리에 추가 하는 경우 해당 목록 또는 라이브러리의 소유자가 해당 목록이 나 라이브러리에 대 한 사이트 모음 정책을 수정할 수 없습니다. 사이트 모음 정책을 사이트 콘텐츠 형식에 추가 하는 것이 사이트 계층 구조의 각 수준에서 적용 되도록 하는 좋은 방법입니다.
  
![사이트 설정 페이지의 콘텐츠 형식 정책 서식 파일 링크](../media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
 **최상위 사이트의 사이트 콘텐츠 형식 갤러리에서 사이트 콘텐츠 형식에 대 한 정보 관리 정책을 만든 다음 하나 이상의 목록 또는 라이브러리에 해당 콘텐츠 형식을 추가** 합니다. 사이트 콘텐츠 형식에 대해 직접 정보 관리 정책을 만든 다음 해당 사이트 콘텐츠 형식의 인스턴스를 여러 목록 또는 라이브러리에 연결할 수도 있습니다. 이러한 방식으로 정보 관리 정책을 만드는 경우 해당 콘텐츠 형식의 사이트 모음에 있는 모든 항목 또는 해당 콘텐츠 형식에서 상속 되는 콘텐츠 형식에 정책이 포함 됩니다. 그러나 사이트 콘텐츠 형식에 대해 직접 정보 관리 정책을 만드는 경우에는이 방식으로 만든 정책을 내보낼 수 없으므로 다른 사이트 모음에서이 정보 관리 정책을 다시 사용 하는 것이 더 어렵습니다. 
  
![사이트 설정 페이지의 사이트 콘텐츠 형식 링크](../media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
![사이트 콘텐츠 형식에 대 한 설정 페이지의 정보 관리 정책 링크](../media/15d83a34-6c8f-4b6e-b6ee-e9b0a70cbb4b.png)
  
참고 사이트 모음에서 사용 되는 정책을 제어 하기 위해 사이트 모음 관리자는 콘텐츠 형식에 대해 직접 정책 기능을 설정 하는 기능을 사용 하지 않도록 설정할 수 있습니다. 이 제한이 적용 되 면 콘텐츠 형식을 만드는 사용자가 사이트 모음 정책 목록에서 정책만 선택할 수 있도록 제한 됩니다.
  
 **목록 또는 라이브러리에 대 한 정보 관리 정책 만들기** 조직에서 제한 된 콘텐츠 집합에 특정 정보 관리 정책을 적용 해야 하는 경우 개별 목록 또는 라이브러리에만 적용 되는 정보 관리 정책을 만들 수 있습니다. 정책이 한 위치에만 적용 되 고 다른 위치에서는 내보내거나 다시 사용할 수 없으므로 정보 관리 정책을 만드는 방법은 유연성이 가장 뛰어납니다. 그러나 특정 상황을 해결 하기 위해 제한적으로 적용 되는 고유한 정보 관리 정책을 만들어야 하는 경우가 있습니다. 
  
![문서 라이브러리에 대 한 설정 페이지의 정보 관리 정책 링크](../media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
참고 
  
목록이 나 라이브러리에서 여러 콘텐츠 형식을 지원 하지 않는 경우에만 목록 또는 라이브러리에 대 한 정보 관리 정책을 만들 수 있습니다. 목록 또는 라이브러리에서 여러 콘텐츠 형식을 지 원하는 경우 해당 목록이 나 라이브러리에 연결 된 각 개별 목록 콘텐츠 형식에 대 한 정보 관리 정책을 정의 해야 합니다. 특정 목록 또는 라이브러리에 연결 된 사이트 콘텐츠 형식의 인스턴스를 목록 콘텐츠 형식 이라고 합니다.
  
사이트 모음에서 사용 되는 정책을 제어 하기 위해 사이트 모음 관리자는 목록 또는 라이브러리에서 직접 정책 기능을 설정 하는 기능을 사용 하지 않도록 설정할 수 있습니다. 이 제한이 적용 되 면 목록 또는 라이브러리를 관리 하는 사용자는 사이트 모음 정책 목록에서 정책을 선택 하는 것으로 제한 됩니다.
  
[정보 관리 정책은 콘텐츠 형식에 대 한 규칙 집합입니다. 정보 관리 정책을 사용 하면 조직이 보존 되는 기간 또는 사용자가 해당 콘텐츠에 대해 수행할 수 있는 작업을 제어 하 고 추적 하는 데 도움이 됩니다. 정보 관리 정책은 조직이 법적 또는 정부 규정을 준수 하거나 내부 비즈니스 프로세스를 적용 하는 데 도움이 될 수 있습니다. 예를 들어 해당 금융 기관에 대 한 "적절 한 제어"를 시연 해야 하는 정부 규정을 따라야 하는 조직에서는 재무 관련 문서에 대 한 작성 및 승인 프로세스의 특정 작업을 감사 하는 하나 이상의 정보 관리 정책을 만들 수 있습니다. 방법 정보는 Create and apply information management 정책도을 참조 하십시오.](intro-to-info-mgmt-policies.md#__top)
  

