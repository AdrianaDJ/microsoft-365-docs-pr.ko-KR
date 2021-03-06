---
title: 데이터 이동 도중 및 이후
ms.author: andyber
author: andybergen
manager: laurawi
ms.date: 12/10/2019
audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.collection: SPO_Content
search.appverid:
- MET150
localization_priority: Normal
ms.assetid: f47e3e09-b1dc-4b80-b6ea-fd6e0933407f
f1.keywords:
- NOCSH
description: 데이터 이동은 테 넌 트에 대 한 서비스 및 연결 된 데이터를 새 데이터 센터 geo로 이동할 때 발생 하는 백 엔드 작업입니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: ca3159aeb951fb0cb3bf3aba953979dabc6ba024
ms.sourcegitcommit: 1db81b85d327fe423695ce675ad325e538417211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49349259"
---
# <a name="during-and-after-your-data-move"></a>데이터 이동 도중 및 이후

데이터 이동은 최종 사용자에게 최소의 영향만 미치는 백 엔드 작업입니다. Microsoft에서 사용자의 테넌트의 각 서비스 및 연결된 데이터를 새 데이터 센터 지역으로 이동하는 동안 필요한 작업은 없습니다. 사용자에게 최소한의 영향만 미치면서, 백그라운드에서 사전에 데이터 전송 및 유효성 검사가 진행됩니다.
  
> [!NOTE]
> 서비스마다 다른 시간에 이동이 발생합니다. 결과적으로 다른 시간에 각 서비스의 기능이 제한된다는 설명이 표시될 수 있습니다. 
  
각 Exchange Online, SharePoint Online 및 팀 채팅 서비스에 대 한 이동이 완료 되 면 Microsoft 365 메시지 센터에서 확인을 시청 하세요. 아래 표에 나와 있는 것 처럼, rest에서 핵심 고객 데이터를 완료 하기 위한 등록 기간이 끝나면 최대 24 개월이 새 데이터 센터 지역으로 이동 될 수 있습니다.   

|**등록 국가가 있는 고객**|**모든 이동 완료 시기**|
|:-----|:-----|
|오스트레일리아, 뉴질랜드, 피지  <br/> |2022 년 7 월 1 일  <br/> |
|일본  <br/> |2022 년 7 월 1 일  <br/> |
|인도  <br/> |2022 년 7 월 1 일  <br/> |
|캐나다  <br/> |2022 년 7 월 1 일  <br/> |
|대한민국  <br/> |2022 년 7 월 1 일  <br/> |
|영국  <br/> |2022 년 7 월 1 일  <br/> |
|프랑스  <br/> |2022 년 7 월 1 일  <br/> |
|아랍에미리트  <br/> |2022 년 7 월 1 일  <br/> |
|남아프리카 공화국  <br/> |2022 년 7 월 1 일  <br/> |
|스위스, 리히텐슈타인  <br/> |2022 년 7 월 1 일  <br/> |
|노르웨이  <br/> |2022 년 11 월 1 일  <br/> |
|독일  <br/> |5 월 1 일, 2023  <br/> |
|브라질  <br/> |2023 년 6 월 1 일  <br/> |

## <a name="exchange-online"></a>Exchange Online

각 사용자를 새 데이터 센터 지역으로 이동하는 데 시간이 걸리므로 일부 사용자는 다른 사용자가 새 데이터 센터 지역으로 이동되는 동안 이전 데이터 센터 지역에 계속 남아 있게 됩니다. 즉, 여러 사서함에 액세스 하는 기능 중 일부는 지난 주까지 이동 프로세스를 진행 하는 동안 제대로 작동 하지 않을 수 있습니다. 이러한 기능은 다음 섹션에 설명되어 있습니다.
  
### <a name="open-shared-folder-in-outlook-web-access"></a>Outlook Web Access에서 "공유 폴더" 열기 

일부 사용자는 "공유 폴더" 기능을 사용 하 여 Outlook Web Access에서 다른 사서함 (사용자가 읽기 또는 쓰기 권한을 가진 공유 메일 폴더)을 엽니다. 다음 표에서는 사서함을 이동 하는 동안 공유 폴더에 대 한 액세스를 작동 하는 방법을 설명 합니다. 공유 사서함에 대한 모든 권한이 있는 사용자는 이동하는 동안 Outlook Web Access를 사용하여 사서함을 열 수 있습니다. 
  
|**구성**|**설명**|
|:-----|:-----|
|사용자에게 다른 사서함에 대한 사서함 폴더 권한이 있음  <br/> |제한될 수 있습니다.  <br/> 사용자 a와 사서함 B가 테 넌 트 이동 중에 같은 지역에 있지 않은 경우 사용자 a는 사서함 B의 특정 폴더에 대 한 사용 권한이 있는 경우 Outlook Web Access에서 사서함 B의 폴더를 열 수 없습니다.  <br/> 공유 폴더를 추가하려면 왼쪽 탐색 패널에서 사용자 이름을 마우스 오른쪽 단추로 클릭하고 **공유 폴더 추가** 를 선택합니다.  <br/> |
|사용자에게 다른 사서함에 대한 모든 사서함 권한이 있음  <br/> |완전히 지원됩니다.  <br/> 사용자 A에 게 사서함 B에 대 한 "모든 권한" 권한이 있으면 사용자 A가 Outlook Web Access의 왼쪽 탐색 패널에서 공유 폴더를 클릭 하 여 사서함 B가 표시 된 창을 열 수 있습니다.  사용자는 부정적인 영향을 주지 않으면 서 이동 하는 동안 Outlook Web Access를 사용 하 여 공유 사서함을 열 수 있습니다. 이러한 제한 사항은 사서함의 폴더 수준 공유에만 적용됩니다.           |
  
## <a name="sharepoint-online"></a>SharePoint Online

SharePoint Online이 이동 될 때 다음 서비스에 대 한 데이터도 이동 됩니다.
  
- 비즈니스용 OneDrive
    
- Microsoft 365 비디오 서비스
    
- 브라우저에서 Office
    
- 엔터프라이즈용 Microsoft 365 앱
    
- Visio Pro for Microsoft 365
    
SharePoint Online 데이터 이동을 완료 한 후에는 다음과 같은 몇 가지 효과를 확인할 수 있습니다.
  
### <a name="microsoft-365-video-services"></a>Microsoft 365 비디오 서비스

- 비디오에서는 SharePoint Online에서 콘텐츠의 나머지 부분에 대 한 이동을 보다 긴 데이터 이동합니다.
    
- SharePoint Online 콘텐츠를 이동한 후에는 비디오를 재생할 수 없을 때 시간 프레임이 나타납니다.
    
- 이전 데이터 센터에서 코드 변환된 복사본을 제거한 후 새로운 데이터 센터에서 다시 코드 변환을 수행하기 때문입니다.
    
### <a name="search"></a>검색

SharePoint Online 데이터를 이동 하는 과정에서 검색 인덱스 및 검색 설정을 새 위치로 마이그레이션합니다. SharePoint Online 데이터를 이동할 때까지 계속 해 서 사용자에 게 원래 위치에 있는 인덱스를 **처리 합니다.** SharePoint Online 데이터 이동이 완료 된 후 새 위치에서 검색을 통해 콘텐츠 크롤링이 자동으로 시작 됩니다. 이 시점부터는 마이그레이션된 인덱스에서 고객의 사용자에게 서비스를 제공합니다. 마이그레이션 후 발생하는 콘텐츠 변경 내용은 크롤링하기 전까지 마이그레이션된 인덱스에 포함되지 않습니다. 대부분의 고객은 SharePoint Online 데이터 이동을 완료 한 후 결과가 최신이 아닌 것을 알 수 없지만, 일부 고객의 경우 처음 24-48 시간 동안 최신 상태를 유지 하는 경우가 있습니다. 
  
영향을 받는 기능은 다음과 같습니다.
  
- 검색 결과 및 검색 웹 파트: 마이그레이션 후 발생한 변경 내용은 크롤링하기 전까지 결과에 포함되지 않습니다. 
    
- Delve: 마이그레이션 후 발생한 변경 내용은 크롤링하기 전까지 Delve에 포함되지 않습니다.
    
- 사이트에 대 한 인기 및 검색 보고서: 새 위치에 있는 Excel 보고서의 수에는 SharePoint Online 데이터 이동이 완료 된 후에 실행 된 사용 현황 보고서의 마이그레이션 수와 카운트만 포함 됩니다. 중간 기간의 모든 수는 손실되며 복구할 수 없습니다. 이 기간은 일반적으로 이틀 정도입니다. 일부 고객은 손실되는 기간이 더 짧거나 길 수도 있습니다.
    
- 비디오 포털: 비디오 포털의 조회수 및 통계는 Excel 보고서 통계에 따라 달라지므로 Excel 보고서의 손실 기간만큼 비디오 포털에 대한 조회수 및 통계가 손실됩니다.
    
- eDiscovery: 마이그레이션하는 동안 변경된 항목은 크롤링하기 전까지 표시되지 않습니다.
    
- DLP(데이터 손실 방지): 항목의 변경 내용을 크롤링하기 전까지는 항목에 정책이 적용되지 않습니다.

## <a name="microsoft-teams"></a>Microsoft Teams

Microsoft는 Exchange Online, SharePoint Online 및 비즈니스용 OneDrive 외에도 팀 채팅 서비스 데이터를 로컬 데이터 센터로 마이그레이션합니다.

- 개인 메시지 및 채널 메시지를 포함 한 팀 대화방 메시지
- 채팅에 사용 되는 팀 이미지

팀 파일은 SharePoint Online 및 팀 채팅 파일에 저장 되며 비즈니스용 OneDrive에 저장 됩니다. 음성 메일, 일정, 채팅 기록 및 연락처는 Exchange Online에 저장 됩니다. 대부분의 경우 Exchange Online, SharePoint Online 및 비즈니스용 OneDrive는 고객이 로컬 데이터 센터 지역에 있는 고객에 게 이미 사용 되 고 있으며 적합 한 고객 국가에 대 한 Microsoft 365 마이그레이션 프로그램의 일부 이기도 합니다.

## <a name="skype-for-business"></a>비즈니스용 Skype

비즈니스용 Skype 이동을 더 이상 사용할 수 없습니다.  [비즈니스용 Skype Online은](https://docs.microsoft.com/lifecycle/announcements/skype-for-business-online-retirement) 2021 년 7 월 31 일에 만료 됩니다. 그 후에는 서비스에 더 이상 액세스할 수 없게 됩니다. 
  
## <a name="related-topics"></a>관련 항목 
 
[데이터 이동을 요청하는 방법](request-your-data-move.md)
    
[데이터 이동 일반 FAQ](data-move-faq.md)
  
[Microsoft Dynamics CRM Online에 대 한 새로운 데이터 센터 지역](https://go.microsoft.com/fwlink/p/?Linkid=615924)
  
[지역별 Azure services](https://azure.microsoft.com/regions/)
