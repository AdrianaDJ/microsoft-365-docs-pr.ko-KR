---
title: 기본 DLP 정책을 사용하여 시작
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 8/10/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: 보고서를 사용 하 여 조직의 기본 DLP (데이터 손실 방지) 정책을 구체화 하는 방법을 알아봅니다.
ms.openlocfilehash: 7c8f0460f9cd02ee3d26197965f5ea74737ac833
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44817617"
---
# <a name="get-started-with-the-default-dlp-policy"></a>기본 DLP 정책을 사용하여 시작

첫 번째 DLP (데이터 손실 방지) 정책을 만들기 전에 DLP는 기본 정책을 사용 하 여 중요 한 정보를 보호 하는 것을 지원 합니다. 이 기본 정책 및 권장 사항 (아래에 표시)은 신용 카드 번호를 포함 하는 전자 메일 또는 문서가 조직 외부의 사용자와 공유 될 때 사용자에 게 알리기 때문에 중요 한 콘텐츠를 안전 하 게 유지할 수 있습니다. 보안 및 준수 센터의 **홈** 페이지에이 권장 사항이 표시 됩니다 &amp; . 
  
이 위젯을 사용 하 여 공유 된 중요 한 정보를 신속 하 게 확인 한 다음 한 번만을 클릭 하 여 기본 DLP 정책을 구체화할 수 있습니다. 또한 기본 DLP 정책은 완전히 사용자 지정 가능 하므로 언제 든 지 편집할 수 있습니다. 처음에는 권장 사항이 표시 되지 않으면 **권장** 섹션의 아래쪽에서 **+ 자세히** 를 클릭 해 보세요. 
  
![공유 콘텐츠 추가 보호 라는 위젯](../media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a>보고서 보기 및 기본 DLP 정책 구체화

사용자가 조직 외부의 사용자와 중요 한 정보를 공유 함을 나타내는 위젯에 있으면 아래쪽에서 **DLP 정책 구체화** 를 선택 합니다. 
  
자세한 보고서에는 신용 카드 번호를 포함 하는 콘텐츠가 최근 30 일 동안 공유 된 시기 및 양이 표시 됩니다. 규칙 일치는 위젯에 표시 되는 데 최대 48 시간이 걸릴 수 있습니다.
  
중요 한 정보를 보호 하기 위해 기본 DLP 정책:
  
- 하나 이상의 신용 카드 번호를 포함 하는 Exchange, SharePoint 및 OneDrive의 콘텐츠가 조직 외부의 사용자와 공유 되는 경우를 감지 합니다.
    
- 정책 팁을 표시 하 고이 중요 한 정보를 조직 외부의 사용자와 공유 하려고 할 때 사용자에 게 전자 메일 알림을 보냅니다. 이러한 옵션에 대 한 자세한 내용은 [DLP 정책에 대 한 전자 메일 알림 보내기 및 정책 팁 보기](use-notifications-and-policy-tips.md)를 참조 하세요.
    
- 조직 외부의 사용자와 콘텐츠를 공유한 사용자를 추적할 수 있도록 자세한 활동 보고서를 생성 합니다. [Dlp 보고서](view-the-dlp-reports.md) 및 [감사 로그 데이터](search-the-audit-log-in-security-and-compliance.md) (여기서 **활동**  =  **DLP**)를 사용 하 여이 정보를 볼 수 있습니다.
    
기본 DLP 정책을 신속 하 게 구체화 하기 위해 다음을 선택할 수 있습니다.
  
- 사용자가 조직 외부의 사용자와이 중요 한 정보를 공유 하는 경우 문제 보고서 전자 메일을 보냅니다.
    
- 다른 사용자를 전자 메일 문제 보고서에 추가 합니다.
    
- 중요 한 정보가 포함 된 콘텐츠에 대 한 액세스를 차단 하지만 필요에 따라 사용자가 재정의 하 고 공유 하거나 보낼 수 있도록 허용 합니다.
    
문제 보고서 또는 액세스 제한에 대 한 자세한 내용은 [데이터 손실 방지 정책 개요](data-loss-prevention-policies.md)를 참조 하세요.
  
나중에 이러한 옵션을 변경 하려면 언제 든 지 기본 DLP 정책을 편집할 수 있습니다-다음 섹션을 참고 하세요.
  
![공유 콘텐츠 더 보호 라는 위젯에 대 한 설정](../media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a>기본 DLP 정책 편집

이 정책은 **기본 DLP 정책이** 며 보안 및 준수 센터의 **정책** 페이지에서 **데이터 손실 방지** 아래에 표시 됩니다 &amp; . 
  
이 정책은 처음부터 직접 만든 DLP 정책과 동일한 방법으로 완전히 사용자 지정할 수 있습니다. 또한 정책을 해제 하거나 삭제 하 여 사용자가 더 이상 정책 팁 이나 전자 메일 알림을 받지 않도록 설정할 수 있습니다.
  
![기본 DLP 정책 이라는 DLP 정책](../media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>위젯이 수행 되 고 표시 되지 않는 경우

**공유 콘텐츠 보호** 라는 위젯은 보안 및 준수 센터 **홈페이지의 홈** 페이지에서 **권장 되** 는 섹션에 표시 됩니다 &amp; . 
  
이 위젯은 다음과 같은 경우에만 표시 됩니다.
  
- 보안 &amp; 및 준수 센터 또는 Exchange 관리 센터에 데이터 손실 방지 정책이 없습니다. 이 위젯은 dlp를 시작 하는 데 도움이 되도록 하기 위한 것으로, 이미 DLP 정책이 있는 경우에는 나타나지 않습니다.
    
- 1 개 이상의 신용 카드를 포함 하는 콘텐츠가 최근 30 일 동안 조직 외부의 사용자와 공유 되었습니다.
    
규칙 일치는 위젯에 사용할 수 있는 시간까지 최대 48 시간이 걸릴 수 있으므로 외부적으로 공유 되는 중요 한 정보를 검색 한 후에는 추천을 표시 하는 데 최대 2 일이 걸릴 수 있습니다.
  
마지막으로, 위젯을 사용 하 여 기본 DLP 정책을 구체화 한 후에는 **홈** 페이지에서 위젯이 사라집니다. 
  

