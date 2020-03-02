---
title: Microsoft 365 사용 현황 분석을 사용하도록 설정
f1.keywords:
- CSH
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
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 9db96e9f-a622-4d5d-b134-09dcace55b6a
description: Power BI의 Microsoft 365 사용 현황 분석 서식 파일 앱을 사용 하 여 테 넌 트에 대 한 데이터 수집을 시작 하는 방법을 알아봅니다.
ms.openlocfilehash: 651a820916f65a1695b7300772b1d2ce8aee92bb
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42247294"
---
# <a name="enable-microsoft-365-usage-analytics"></a>Microsoft 365 사용 현황 분석을 사용하도록 설정

Microsoft 365 사용 현황 분석은 Microsoft 365 US 정부 커뮤니티 에서도 사용할 수 있습니다.
  
## <a name="steps-to-enable-microsoft-365-usage-analytics"></a>Microsoft 365 사용 현황 분석을 사용 하도록 설정 하는 단계

Microsoft 365 사용 현황 분석을 시작 하려면 먼저 Microsoft 365 관리 센터에서 데이터를 사용할 수 있도록 설정한 다음 Power BI에서 서식 파일 앱을 시작 해야 합니다.
  
### <a name="get-power-bi"></a>Power BI 가져오기

Power BI가 아직 없는 경우 [POWER Bi Pro에 등록할](https://go.microsoft.com/fwlink/p/?linkid=845347)수 있습니다. **무료 사용** 을 선택 하 여 평가판에 등록 하거나, **지금 구입** 하 여 Power BI Pro를 다운로드 하세요.
  
  
**제품**을 확장하여 Power BI 버전을 구매할 수도 있습니다. 

> [!NOTE]
> 서식 파일 앱을 설치, 사용자 지정 및 배포 하려면 Power BI Pro 라이선스가 필요 합니다. 자세한 내용은 [필수 구성 요소](https://docs.microsoft.com/power-bi/service-template-apps-install-distribute?source=docs#prerequisites)를 참조 하세요.

콘텐츠를 공유 하려면 Power BI Pro 라이선스가 필요 하 고,이를 공유 하는 사용자만이 작업을 수행할 수 있도록 하거나, 콘텐츠가 [프리미엄 용량](https://docs.microsoft.com/power-bi/service-premium-what-is)에 포함 되어 있어야 합니다. 
  
### <a name="enable-the-template-app"></a>서식 파일 앱 사용

서식 파일 앱을 사용 하도록 설정 하려면 **전역 관리자**, **보고서 읽기 권한자**, **Exchange 관리자**, **비즈니스용 Skype 관리자**또는 **SharePoint 관리자**중 하나 여야 합니다. 
  
자세한 내용은 [관리자 역할 정보](../add-users/about-admin-roles.md) 를 참조 하세요. 
  
1. 관리 센터에서 **보고서** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">사용 현황</a> 페이지를 참조하세요. 
    
2. **사용 현황** 페이지에서 **Microsoft 365 사용 현황 분석** 카드를 찾고 **시작**을 선택 합니다.
    
3. 열리는 보고서 패널에서 **데이터를 Power BI에 대 한 Microsoft 365 사용 현황 분석** **에서** \> **저장할**수 있도록 설정 합니다. 
  
이는 데이터 수집 프로세스를 시작 하 여 테 넌 트의 크기에 따라 2 ~ 48 시간 이내에 완료 됩니다. 데이터 수집이 완료 되 면 **POWER BI로 이동** 단추를 사용할 수 있게 됩니다 (더 이상 회색 없음). 
    
### <a name="initiate-the-template-app"></a>서식 파일 앱 시작

서식 파일 앱을 시작 하려면 **전역 관리자**, **보고서 읽기 권한자**, **Exchange 관리자**, **비즈니스용 Skype 관리자**또는 **SharePoint 관리자**중 하나 여야 합니다. 
  
1. 테 넌 트 Id를 복사 하 고 **POWER BI로 이동을**선택 합니다.
    
2.  Power BI로 이동하면 로그인합니다. 앱-탐색 메뉴에서 앱 가져오기 >선택 합니다.    
  
3. **앱** 탭의 검색 상자에 microsoft 365을 입력 한 다음 **microsoft 365 사용 현황 분석** \> 을 선택 하 여 **지금 다운로드**합니다.

    [![지금 받기 선택](../media/78102250-9874-4a32-8365-436f13560b52.png)](https://app.powerbi.com/groups/me/getapps/services/cia_microsoft365.microsoft-365-usage-analytics)
    
4.  앱이 설치 되 면 타일을 클릭 하 여 엽니다.

5.  샘플 데이터를 사용 하 여 앱을 보려면 **앱 탐색** 을 클릭 합니다. **연결** 을 클릭 하 여 조직의 데이터에 앱을 연결 합니다.

6.  **연결**을 클릭 한 후 **Microsoft 365 usage analytics에 연결** 화면에서 \> **다음**단계에서 복사한 테 넌 트 Id를 입력 합니다 (1).
    
7. 다음 화면에서 **인증 방법** \> **로그인**으로 **oAuth2** 을 선택 합니다. 다른 인증 방법을 선택 하는 경우에는 서식 파일 앱에 대 한 연결이 실패 하 게 됩니다.
    
    ![Choose oAuth2 as authentication method](../media/ac85a360-c278-4c60-8aa3-68f4828f1d96.png)
  
8. 서식 파일 앱이 인스턴스화되면 Microsoft 365 사용 현황 분석 대시보드를 웹의 Power BI에서 사용할 수 있습니다. 대시보드의 초기 로드는 2 ~ 30 분 정도 소요 됩니다.
  
모든 보고서에서 테 넌 트 수준 집계를 사용할 수 있습니다. **사용자 수준 세부 정보는 다음 달 또는 15 일 후에 옵트인 하면 사용할 수 있습니다**. 이렇게 하면 사용자 작업의 모든 보고서에 영향을 줍니다 (이 보고서를 보고 사용 하는 방법에 대 한 팁은 [Microsoft 365 사용 현황 분석에서 보고서 탐색 및 활용](navigate-and-utilize-reports.md) 참조).
    
## <a name="make-the-collected-data-anonymous"></a>수집된 데이터를 익명으로 설정

모든 보고서에 대해 수집되는 데이터를 익명으로 만들려면 글로벌 관리자여야 합니다. 이렇게 하면 보고서의 사용자, 그룹 및 사이트 이름과 같은 식별 가능한 정보와 서식 파일 앱이 숨겨집니다.
  
1. 관리 센터에서 **설정** \> **설정**으로 이동 하 여 **서비스** 탭에서 **보고서**를 선택 합니다.
    
2. **보고서**를 선택 하 고 **익명 식별자를 표시**하도록 선택 합니다. 이 설정은 사용 현황 보고서와 서식 파일 앱에 모두 적용 됩니다.
  
3. **변경 내용 저장**을 선택 합니다.