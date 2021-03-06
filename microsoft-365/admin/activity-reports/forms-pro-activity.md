---
title: 관리 센터의 Microsoft 365 보고서-Dynamics 365 고객 음성 활동
ms.author: sirkkuw
author: sirkkuw
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
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
description: Microsoft 365 관리 센터에서 Microsoft 365 보고서 대시보드를 사용 하 여 Microsoft Dynamics 365 고객 음성 활동 보고서를 가져오는 방법을 알아봅니다.
ms.openlocfilehash: de03067197c80634f02318b35a79eb84e33c4b86
ms.sourcegitcommit: 82d8be71c5861a501ac62a774b306a3fc1d4e627
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2020
ms.locfileid: "48988555"
---
# <a name="microsoft-365-reports-in-the-admin-center---dynamics-365-customer-voice-activity"></a>관리 센터의 Microsoft 365 보고서-Dynamics 365 고객 음성 활동

Microsoft 365 **보고서** 대시보드에는 조직의 제품 전체에 대 한 활동 개요가 표시 됩니다. 보고서 대시보드를 통해 개별 제품 수준 보고서의 하위 수준을 표시하여 각 제품 내의 활동에 대한 더 세부화된 정보를 확인할 수 있습니다. [보고서 개요 항목](activity-reports.md)을 확인하세요.
  
예를 들어 Dynamics 365 고객 음성과의 상호 작용을 확인 하 여 Microsoft Dynamics 365 고객 음성을 사용 하도록 허가 된 모든 사용자의 활동을 파악할 수 있습니다. 또한 작성 된 Pro 설문 조사 수와 사용자가 응답 한 Pro 설문 조사를 확인 하 여 진행 중인 공동 작업의 수준을 이해 하는 데 도움이 됩니다. 
  
> [!NOTE]
> 보고서를 보려면 Microsoft 365 또는 Exchange, SharePoint, 팀 서비스, 팀 통신 또는 비즈니스용 Skype 관리자의 전역 관리자, 전역 독자 또는 보고서 독자 여야 합니다. 

## <a name="how-to-get-to-the-forms-pro-activity-report"></a>양식 Pro 활동 보고서에 액세스 하는 방법

1. 관리 센터에서 **보고서** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">사용 현황</a> 페이지를 참조하세요.

    
2. **보고서 선택** 드롭다운에서 **Dynamics 365 고객 음성** \> **활동** 을 선택 합니다.

## <a name="interpret-the-dynamics-365-customer-voice-activity-report"></a>Dynamics 365 고객 음성 활동 보고서 해석

**활동** 및 **사용자** 차트를 확인 하 여 사용자의 Dynamics 365 고객 음성 활동을 볼 수 있습니다. 

![양식 활동 보고서](../../media/formsproactivity.png)

|항목|설명|
|:-----|:-----|
|1.  <br/> |**Dynamics 365 고객 음성** 활동 보고서는 지난 7 일, 30 일, 90 일 또는 180 일 동안의 추세를 볼 수 있습니다. 그러나 보고서에서 특정 날짜를 선택 하는 경우 테이블 (7)은 현재 날짜 로부터 최대 28 일 동안의 데이터를 표시 합니다 (보고서가 생성 된 날짜 아님).   <br/> |
|2.  <br/> |각 보고서의 데이터는 대개 최근 48 시간 동안의 최신 항목입니다.  <br/> |
|3.  <br/> |**사용자** 보기를 사용 하면 활성 Dynamics 365 고객 음성 사용자 수의 추세를 파악할 수 있습니다. 특정 기간 내에 작성, 편집, 보기 등의 Pro 설문 조사에 대 한 활동을 실행 한 경우 사용자는 활성으로 간주 됩니다.  <br/> |
|4.  <br/> |**활동** 보기를 사용 하면 활성 사용자 수의 추세를 파악할 수 있습니다. 사용자가 지정된 기간 동안 파일 활동(저장, 동기화, 수정 또는 공유)을 실행하거나 페이지를 방문한 경우 활성으로 간주됩니다.<br/> 참고: 단일 설문 조사에서 활동은 여러 번 발생할 수 있지만 하나의 활성 설문 조사로만 계산 됩니다. 예를 들어 Pro 설문 조사를 만들고 계속 해 서 같은 설문 조사를 지정 된 기간 동안 여러 번 편집 하면 하나의 설문 조사로만 계산 됩니다. <br>|
|5.<br/>|**사용자** 차트에서 Y 축은 고유 사용자 수입니다. X 축은 고유 사용자가 활성 상태인 날짜입니다. 범례는 다음과 같습니다.<br/><br/>**디자이너** 는 사용자가 Dynamics 365 고객 음성 설문 조사를 만들거나 편집한 것을 의미 합니다.<br><br>**활동** 차트에서 Y 축은 설문 조사 당 Dynamics 365 고객 음성 응답 수입니다. X 축은 설문 조사 또는 응답 활동이 발생 한 날짜입니다. 범례는 다음과 같습니다.<br/><br/>**작성 된 설문 조사** 는 사용자가 만든 고유한 Dynamics 365 고객 음성 조사 수입니다.<br>**응답** 은 설문 조사를 받은 사용자가 제출한 익명 또는 익명이 아닌 응답의 수입니다. |
|6.<br/>|범례에서 항목을 선택 하 여 차트에 표시 되는 계열을 필터링 할 수 있습니다. 예를 들어 사용자 차트에서 디자이너, 응답자 또는 총 사용자를 선택 하 여 각 항목에 관련 된 정보만 표시 합니다. 이 선택 항목을 변경 해도 아래 눈금 표에 있는 정보는 변경 되지 않습니다.|
|7.<br/>|이 표에서는 사용자 수준별 활동 분석 결과를 보여 줍니다. 범례는 다음과 같습니다.<br/><br/>**Username** 은 Microsoft Forms에서 활동을 수행한 사용자의 전자 메일 주소입니다.<br/>**마지막 활동 날짜 (UTC)** 는 선택한 날짜 범위에 대해 사용자가 양식 활동을 수행한 마지막 날짜입니다. 특정 날짜에 발생한 활동을 보려면 차트에서 직접 날짜를 선택합니다.<br/>이렇게 하면 특정 날짜에 활동을 수행한 사용자에 대해서만 파일 활동 데이터가 표시 되도록 테이블이 필터링 됩니다.<br/><br/>**작성 된 설문 조사 수** 는 사용자가 만든 설문 조사 수입니다.<br/> **설문 조사 응답 수** 는 설문 조사가 배포 된 응답자 로부터의 응답 수입니다.|
|8.<br/>|**열 관리** 아이콘을 선택 하 여 보고서에서 열을 추가 하거나 제거 합니다.|
|9.<br/>|**내보내기** 링크를 선택 하 여 보고서 데이터를 Excel .csv 파일로 내보낼 수도 있습니다. 이렇게 하면 모든 사용자의 데이터를 내보내고 추가 분석을 위해 단순 집계, 정렬 및 필터링을 수행할 수 있습니다. 사용자가 100 명 미만인 경우 보고서 자체의 테이블 내에서 정렬 및 필터링 할 수 있습니다. 사용자가 100 개를 초과 하는 경우 필터링 및 정렬 하려면 데이터를 내보내야 합니다.|