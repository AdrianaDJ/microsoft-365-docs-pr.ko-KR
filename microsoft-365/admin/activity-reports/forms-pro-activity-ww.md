---
title: 관리 센터의 Microsoft 365 보고서-Dynamics 365 고객 음성 활동
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
ROBOTS: NOINDEX, NOFOLLOW
search.appverid:
- BCS160
- MST160
- MET150
- MOE150
description: Microsoft 365 관리 센터에서 Microsoft 365 보고서 대시보드를 사용 하 여 Microsoft Dynamics 365 고객 음성 활동 보고서를 가져오는 방법을 알아봅니다.
ms.openlocfilehash: 0a854c7a89977a96e11d8ec28fd7789e8418c1cf
ms.sourcegitcommit: 82d8be71c5861a501ac62a774b306a3fc1d4e627
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48988957"
---
# <a name="microsoft-365-reports-in-the-admin-center---dynamics-365-customer-voice-activity"></a>관리 센터의 Microsoft 365 보고서-Dynamics 365 고객 음성 활동

Microsoft 365 **보고서** 대시보드에는 조직의 제품 전체에 대 한 활동 개요가 표시 됩니다. 보고서 대시보드를 통해 개별 제품 수준 보고서의 하위 수준을 표시하여 각 제품 내의 활동에 대한 더 세부화된 정보를 확인할 수 있습니다. [보고서 개요 항목](activity-reports.md)을 확인하세요.
  
예를 들어 Dynamics 365 고객 음성과의 상호 작용을 확인 하 여 Microsoft Dynamics 365 고객 음성을 사용 하도록 허가 된 모든 사용자의 활동을 파악할 수 있습니다. 또한 작성 된 Pro 설문 조사 수와 사용자가 응답 한 Pro 설문 조사를 확인 하 여 진행 중인 공동 작업의 수준을 이해 하는 데 도움이 됩니다. 
  
> [!NOTE]
> 보고서를 보려면 Microsoft 365 또는 Exchange, SharePoint, 팀 서비스, 팀 통신 또는 비즈니스용 Skype 관리자의 전역 관리자, 전역 독자 또는 보고서 독자 여야 합니다.  
 
## <a name="how-to-get-to-the-dynamics-365-customer-voice-activity-report"></a>Dynamics 365 고객 음성 활동 보고서에 액세스 하는 방법

1. 관리 센터에서 **보고서** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">사용 현황</a> 페이지를 참조하세요. 
2. 대시보드 홈 페이지에서 Dynamics 365 고객 음성 카드의 **기타 보기** 단추를 클릭 합니다.
  
## <a name="interpret-the-dynamics-365-customer-voice-activity-report"></a>Dynamics 365 고객 음성 활동 보고서 해석

**작업** 탭을 선택 하 여 Dynamics 365 고객 음성 보고서의 활동을 볼 수 있습니다.<br/>![Microsoft 365 reports-Microsoft Dynamics 365 고객 음성 활동 보고서](../../media/a7e57d18-1ac8-4d4b-bd70-83361505dc3e.png)

**열 선택을** 선택 하 여 보고서에서 열을 추가 하거나 제거 합니다.  <br/> ![Dynamics 365 고객 음성 활동 보고서-열 선택](../../media/5ab66f4b-32eb-4c9b-9683-1157ae9e2c0a.png)

**내보내기** 링크를 선택 하 여 보고서 데이터를 Excel .csv 파일로 내보낼 수도 있습니다. 그러면 모든 사용자의 데이터를 내보내고 향후 분석을 위해 간단하게 정렬 및 필터링을 수행할 수 있습니다. 사용자가 2,000명 미만인 경우 보고서 자체의 표에서 정렬 및 필터링할 수 있습니다. 사용자가 2,000명 이상인 경우 필터링 및 정렬하려면 데이터를 내보내야 합니다. 
  
|항목|설명|
|:-----|:-----|
|**메트릭**|**정의**|
|사용자 이름  <br/> |Microsoft Forms에서 활동을 수행한 사용자의 전자 메일 주소입니다.  <br/> |
|마지막 활동 날짜 (UTC)  <br/> |선택한 날짜 범위에 대해 사용자가 양식 활동을 수행한 마지막 날짜입니다. 특정 날짜에 발생한 활동을 보려면 차트에서 직접 날짜를 선택합니다.<br/>이렇게 하면 특정 날짜에 활동을 수행한 사용자에 대해서만 파일 활동 데이터가 표시 되도록 테이블이 필터링 됩니다.  <br/> |
|작성 된 설문 조사 수  <br/> |사용자가 만든 설문 조사 수입니다.   <br/> |
|설문 조사 응답 수  <br/> |설문 조사가 배포 된 응답자의 응답 수입니다.|
|||