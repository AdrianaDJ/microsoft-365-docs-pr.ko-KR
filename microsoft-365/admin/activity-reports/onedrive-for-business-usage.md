---
title: 관리 센터의 Microsoft 365 보고서-비즈니스용 OneDrive 사용 현황
ms.author: pebaum
author: pebaum
manager: pamgreen
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- SPO_Content
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
- ODB150
- ODB160
ms.assetid: 0de3b312-c4e8-4e4b-a02d-32b2f726a680
description: '비즈니스용 OneDrive 사용 현황 보고서를 다운로드 하 여 조직 전체에서 사용 되는 총 파일 및 저장소 수를 확인할 수 있습니다. '
ms.openlocfilehash: e08dff4e763479afa197377d37e474384492c012
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47948920"
---
# <a name="microsoft-365-reports-in-the-admin-center---onedrive-for-business-usage"></a>관리 센터의 Microsoft 365 보고서-비즈니스용 OneDrive 사용 현황

Microsoft 365 **보고서** 대시보드에는 조직의 제품 전체에 대 한 활동 개요가 표시 됩니다. 보고서 대시보드를 통해 개별 제품 수준 보고서의 하위 수준을 표시하여 각 제품 내의 활동에 대한 더 세부화된 정보를 확인할 수 있습니다. [보고서 개요 항목](activity-reports.md)을 확인하세요.
  
예를 들어 대시보드의 OneDrive 카드에서는 비즈니스용 OneDrive에서 가져오는 값(예: 총 파일 수 및 조직 전체를 통해 사용되는 저장소)을 대략적으로 볼 수 있습니다. 그런 다음 하위 수준을 표시하여 활성 OneDrive 계정의 추세, 사용자가 상호 작용 중인 파일 수 외에도 사용되는 저장소를 파악할 수 있습니다. 사용자의 OneDrive에 대한 세부 정보도 제공합니다.
  
> [!NOTE]
> 보고서를 보려면 Microsoft 365 또는 Exchange, SharePoint, 팀 서비스, 팀 통신 또는 비즈니스용 Skype 관리자의 전역 관리자, 전역 독자 또는 보고서 독자 여야 합니다.  
 
## <a name="how-do-i-get-to-the-onedrive-usage-report"></a>OneDrive 사용 현황 보고서에 액세스하려면 어떻게 하나요?

1. 관리 센터에서 **보고서** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">사용</a>으로 이동 합니다.

    
2. **보고서 선택** 드롭다운에서 **OneDrive** \> **사용**을 선택 합니다. 
  
## <a name="interpret-the-onedrive-usage-report"></a>OneDrive 사용 현황 보고서 해석

**계정**, **파일** 및 **저장소** 보기를 확인하여 비즈니스용 OneDrive 사용 현황을 볼 수 있습니다. 
  
![OneDrive Usage Report](../../media/49c5b93b-d081-436e-8992-236343a6d46b.png)
  
|항목|설명|
|:-----|:-----|
|1.  <br/> |**OneDrive 사용 현황** 보고서는 지난 7일, 30일, 90일 또는 180일간의 추세를 보여 줍니다. 그러나 보고서에서 특정 날짜를 선택 하는 경우 테이블 (7)은 현재 날짜 로부터 최대 28 일 동안의 데이터를 표시 합니다 (보고서가 생성 된 날짜 아님).  <br/> |
|2.  <br/> |각 보고서의 데이터는 대개 최근 24 ~ 48 시간까지 포함 됩니다. <br/>|
|3.  <br/> |**계정** 보기는 전체 및 활성 OneDrive 계정 수의 추세를 보여 줍니다. '활성 계정'은 사용자가 파일 보기, 수정, 업로드, 다운로드, 공유 또는 동기화 할 수 있는 계정입니다.  <br/> |
|4.  <br/> |**파일** 보기에는 전체 및 활성 파일 수가 표시 됩니다. 파일은 특정 기간에 저장, 동기화, 수정 또는 공유 된 경우에만 활성으로 간주 됩니다.  <br/> 참고: 파일 활동은 단일 파일에 대해 여러 번 발생할 수 있지만 하나의 활성 파일로 계산 됩니다. 예를 들어 지정된 기간 동안 같은 파일을 여러 번 저장하고 동기화할 수 있지만, 데이터에서 하나의 동기화된 파일 및 하나의 활성 파일로 계산됩니다.           |
|5.  <br/> |**저장소** 보기에는 사용 중인 OneDrive 저장소의 크기에 관한 추세가 표시됩니다. 저장 용량 제한을 확인 하려면 사용자에 게 [기본 저장 제한이 있는지 또는 특정 한도를 포함 하는지 확인](https://docs.microsoft.com/onedrive/set-default-storage-space#check-if-a-user-has-the-default-storage-limit-or-a-specific-limit)을 참조 하십시오.  <br/> 참고:이 크기에는 파일과 연결 된 모든 버전 및 메타 데이터가 포함 됩니다.           |
|6.  <br/> | **계정** 차트에서 Y축은 OneDrive 계정의 수입니다.  <br/>  **파일** 차트에서 Y축은 OneDrive에서 저장된 파일 수입니다.  <br/>  **저장소** 차트에서 Y축은 사용된 OneDrive 저장소 크기입니다.  <br/>  모든 차트의 X축은 모두 이 특정 보고서에 선택된 날짜 범위입니다.  <br/> |
|7.  <br/> |범례에서 항목을 선택 하 여 차트에 표시 되는 계열을 필터링 할 수 있습니다. 예를 들어 **파일** 차트에서 **전체 파일** 또는 **활성 파일**을 선택 합니다. **계정** 차트에서 **총 계정** 또는 **활성 계정을**선택 합니다. 또는 **저장소** 차트에서 **사용 되는 저장소**를 선택 합니다. 선택 항목을 변경해도 표에 있는 정보는 변경되지는 않습니다.  <br/> |
|8.  <br/> | 이 표에서는 각 사용자의 OneDrive에 대한 데이터 분석 결과를 보여줍니다. 표에 표시되려면, OneDrive을(를) 포함하는 제품 라이선스가 사용자에게 할당되어야 하며, SharePoint Online을(를) 켜놓아야 합니다. 사용자는 또한 OneDrive 동기화 클라이언트에 로그인하거나 웹 브라우저를 사용하여 OneDrive을(를) 검색해야 합니다.  <br/>  OneDrive에 파일 활동이 있으면 파일 활동이 수행된 최신 날짜가 있습니다. 표의 행이 **마지막 활동 날짜**로 정렬되므로 가장 최근 파일 활동이 있는 OneDrive이 목록의 맨 위에 표시됩니다.  <br/>  표에서 열을 추가하거나 제거할 수 있습니다.  <br/> ![열 옵션](../../media/onedriveusage-columns.png)  <br/> **URL** 은 사용자의 OneDrive에 대 한 웹 주소입니다.  <br/> **삭제됨**은 OneDrive의 삭제 상태입니다. 계정이 삭제됨으로 표시되려면 7일 이상이 소요됩니다.  <br/> **소유자**는OneDrive의 기본 관리자의 사용자 이름입니다.  <br/> **소유자 계정 이름은** OneDrive 소유자의 전자 메일 주소입니다.  <br/> **마지막 활동 날짜(UTC)** 는 OneDrive에서 파일 활동이 수행된 마지막 날짜입니다. OneDrive에 파일 활동이 없으면, 값은 비어 있게 됩니다.  <br/> **파일 수**는 OneDrive의 파일 수입니다.  <br/> **활성 파일 수**는 해당 기간 이내의 활성 파일의 수입니다.<br/> 참고: 보고서에 대해 지정 된 기간 동안 파일이 제거 된 경우 보고서에 표시 되는 활성 파일 수는 OneDrive의 현재 파일 수 보다 클 수 있습니다. 삭제 된 사용자는 180 일 동안 계속 해 서 보고서에 표시 됩니다.<br/>**사용된 저장소(MB)** 는 OneDrive에서 사용하는 저장소의 크기(MB)입니다. <br/>  조직의 정책으로 인해 사용자 정보를 식별할 수 있는 보고서를 볼 수 없는 경우 이러한 모든 보고서의 개인 정보 설정을 변경할 수 있습니다. [Microsoft 365 관리 센터의 활동 보고서](activity-reports.md)에서 **사용자 수준의 세부 정보를 숨기는 방법** 섹션을 확인 하세요.  <br/> |
|9.  <br/> |**열 관리 아이콘** 을 선택 ![ 하 여 ](../../media/13d2e536-de88-4db3-80c7-7a3a57298eb4.png) 보고서에서 열을 추가 하거나 제거 합니다.  <br/> |
|10.  <br/> |**내보내기** 링크를 선택 하 여 Excel .csv 파일에 보고서 데이터를 내보낼 수도 있습니다. 그러면 각 OneDrive의 데이터를 내보내고 향후 분석을 위해 간단하게 정렬 및 필터링을 수행할 수 있습니다. 사용자가 2,000 OneDrive 계정 미만을 가진 경우 보고서 자체의 표에서 정렬 및 필터링할 수 있습니다. 2,000 OneDrive 계정 이상을 가진 경우 필터링 및 정렬하려면 데이터를 내보내야 합니다.  <br/> 참고: 데이터를 Excel 파일로 내보낼 때 콘텐츠 보고서가 생성 된 날짜는 열 **로 데이터** 의 파일에 반영 됩니다.  <br/> |
|||
   
