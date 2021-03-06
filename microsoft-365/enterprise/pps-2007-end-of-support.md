---
title: PerformancePoint Server 2007 지원 종료 로드맵
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: conceptual
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
search.appverid:
- PSV120
- PDD140
- MET150
ms.assetid: 89d9feee-2285-419c-8c14-0f7f583536e0
f1.keywords:
- NOCSH
description: PerformancePoint Server 2007, ProClarity 및 SharePoint Server 2007가 지원 종료에 도달 했습니다. 이 문서를 읽으면 BI 솔루션 업그레이드를 계획 하는 데 도움이 됩니다.
ms.openlocfilehash: 4a13e6f8a40de78c0d98b03369b52a78899fc7a9
ms.sourcegitcommit: d3ca8021f7da00a474ac14aac5f1358204a848f2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/01/2020
ms.locfileid: "49519600"
---
# <a name="performancepoint-server-2007-end-of-support-roadmap"></a>PerformancePoint Server 2007 지원 종료 로드맵

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

Office 2007 서버와 응용 프로그램은 BI (비즈니스 인텔리전스) 솔루션의 일부로 사용할 수 있는 서버 및 응용 프로그램을 포함 하 여 지원 종료에 도달 했습니다. 다음 표에는 영향을 받는 BI 응용 프로그램이 나와 있습니다.
  
|**Microsoft BI 응용 프로그램**|**지원 종료 날짜**|
|:-----|:-----|
|ProClarity Analytics Server 6.3 서비스 팩 3  <br/> ProClarity 데스크톱 전문가 6.3  <br/> ProClarity SharePoint Viewer 6.3  <br/> |2017년 7월 11일  <br/> |
|SharePoint Server 2007 서비스 팩 3  <br/> |2017년 10월 10일  <br/> |
|PerformancePoint Server 2007 서비스 팩 3  <br/> |2018년 1월 9일  <br/> |
   
자세한 내용은 [Office 2007 서버 및 클라이언트에서 업그레이드 하는 데 도움이](upgrade-from-office-2007-servers-and-products.md)되는 리소스를 참조 하세요.
  
## <a name="what-does-end-of-support-mean"></a>*지원이 끝나는* 것은 무엇을 의미 하나요?

대부분의 Microsoft 제품, PerformancePoint Server 2007 SP3, ProClarity software 및 SharePoint Server 2007 s p 3에는 Microsoft가 새로운 기능, 버그 수정 및 보안 업데이트를 제공 하는 지원 수명 주기가 있습니다. 제품의 수명 주기는 일반적으로 제품 초기 릴리스에서 10 년 동안 지속 됩니다. 해당 수명 주기의 끝을 제품의 지원 종료 라고 합니다. ProClarity, PerformancePoint Server 및 SharePoint Server 2007이 지원 종료에 도달 했을 때 Microsoft는 더 이상 다음을 제공 하지 않습니다.
  
- 발생할 수 있는 문제에 대 한 기술 지원
    
- 검색 된 문제와 서버의 안정성 및 유용성에 영향을 줄 수 있는 문제에 대 한 버그 수정
    
- 검색 되 고 서버 또는 응용 프로그램이 보안 위반에 취약 해질 수 있는 취약성에 대 한 보안 수정 사항
    
- 표준 시간대 업데이트
    
지원이 종료 된 경우에도 ProClarity, SharePoint Server 2007 SP3 및 PerformancePoint Server 2007 s p 3의 설치는 계속 실행 됩니다. 그러나 가능한 한 빨리 이러한 응용 프로그램을 마이그레이션하는 것이 좋습니다.
  
## <a name="what-are-my-options"></a>내 옵션 이란?

다음 표에 요약 되어 있는 것 처럼 Microsoft BI 응용 2007 프로그램에 대 한 변경 내용이 많이 있으며, 다음과 같은 몇 가지 옵션을 고려해 야 합니다.
  
|**이 방법을 사용 하는 경우 ...**|**다음 옵션을 탐색 합니다.**|**이를 염두에 두어야 합니다.**|
|:-----|:-----|:-----|
| PerformancePoint Server 2007 &amp; 에서는 다음을 비롯 한 모니터링 분석 기능을 제공 합니다.<br/>-PerformancePoint 모니터링 서버 <br/>-PerformancePoint 대시보드 디자이너<br/>-SharePoint Services 용 대시보드 뷰어 (PerformancePoint 대시보드, 성과 기록표 및 보고서를 렌더링 하는 데 사용 됨)<br/> |Excel **에서 excel을 사용 하** 는 경우 (클라우드 또는 온-프레미스) 개요를 보려면 [Excel 및 Microsoft 365의 BI 기능](https://support.office.com/article/26c0548e-124c-4fd3-aab3-5f64568cb743.aspx)을 참조 하세요.<br/><br/> **POWER BI** (클라우드 또는 온-프레미스) 개요는 [POWER BI 란?](https://go.microsoft.com/fwlink/?linkid=841341) 를 참조 하세요. <br/><br/> **SQL Server Reporting Services** (온-프레미스) 개요에 대 한 자세한 내용은 [SQL Server Reporting Services (SSRS): 모바일 및 페이지를 매긴 보고서 만들기, 배포 및 관리](https://go.microsoft.com/fwlink/?linkid=841342)를 참조 하세요. <br/><br/> **PerformancePoint Services** (온-프레미스) 개요는 [What 's new For PerformancePoint Services (SharePoint Server 2010)](https://go.microsoft.com/fwlink/?linkid=841343)를 참조 하십시오. <br/> |Excel을 온라인 (클라우드 기반) 또는 온-프레미스 솔루션으로 사용할 수 있습니다. Excel에서 다양 한 보고 및 대시보드 요구 사항을 충족할 수 있습니다.  <br/><br/> Power BI는 온라인 또는 온-프레미스 솔루션으로 사용할 수 있습니다. Power BI는 Microsoft 365에 포함 되어 있지 않습니다. 하지만 Power BI 사용을 무료로 시작할 수 있습니다. 나중에 데이터 사용량 및 비즈니스 요구 사항에 따라 Power BI Pro를 Microsoft 365 E5로 업그레이드할 수 있습니다.<br/> <br/> Reporting Services 및 PerformancePoint Services는 모두 온-프레미스 솔루션입니다. <br/><br/> PerformancePoint Services는 SharePoint Server 2010, SharePoint Server 2013 및 SharePoint Server 2016에서 사용할 수 있습니다. <br/> <br/> PerformancePoint Server 2007에서 사용할 수 있는 일부 기능 및 보고서 형식은 Excel, Power BI, Reporting Services 또는 PerformancePoint Services에서 사용할 수 없습니다. 사용 가능한 기능을 검토 하 여 비즈니스 요구에 가장 적합 한 솔루션을 결정 합니다. <br/> |
| 다음을 포함 한 ProClarity 소프트웨어<br/>-ProClarity 데스크톱 전문가<br/> -ProClarity Analytics Server<br/>-ProClarity SharePoint Viewer<br/> |**Microsoft 파트너와 협력** 하 여 사용자의 요구에 가장 적합 한 솔루션을 식별 합니다. [Microsoft 파트너 센터](https://go.microsoft.com/fwlink/?linkid=841249)를 방문 합니다. <br/><br/> 브라우저, Power BI, SQL Server Reporting Services 또는 PerformancePoint Services에서 excel과 excel을 함께 사용 하는 것을 고려할 수도 있습니다.  <br/> |일부 경우에는 Excel, Power BI, Reporting Services 및 PerformancePoint Services를 비롯 한 다른 Microsoft 제품에서 ProClarity 소프트웨어의 모든 기능을 사용할 수 없습니다.  <br/> |
|SharePoint Server 2007 Kpi (MOSS Kpi 라고도 함)  <br/> |Excel **Services를 사용 하는 Excel 서비스** 개요에 대 한 자세한 내용은 [excel 및 Excel Services의 비즈니스 인텔리전스 (SharePoint Server 2013)](https://support.office.com/article/2740f10c-579d-4b40-a1d9-7beb5d38547c.aspx)를 참조 하십시오. <br/> |Sharepoint Server 2007를 사용 하 여 만든 MOSS Kpi는 SharePoint Server 2010, SharePoint Server 2013 및 SharePoint Server 2016에서 사용할 수 있습니다. 그러나 새 MOSS Kpi를 만들 수는 없습니다.  <br/> |
|Excel 2007  <br/> |**Excel** (클라우드 또는 온-프레미스) 개요를 보려면 [Excel 및 Office 365의 BI 기능](https://support.office.com/article/26c0548e-124c-4fd3-aab3-5f64568cb743.aspx)을 참조 하세요. <br/><br/> **POWER BI** (클라우드 또는 온-프레미스) 개요는 [POWER BI 란?](https://go.microsoft.com/fwlink/?linkid=841341) 를 참조 하세요. <br/> |Excel 및 Power BI는 다양 한 데이터 원본을 지원 하 여 조직 클라우드 기반 및 온-프레미스 솔루션을 제공 합니다.  <br/> |
   
### <a name="help-selecting-a-solution"></a>솔루션 선택 지원

여러 BI를 사용할 수 있으므로 가장 적합 한 옵션을 결정 하는 데 너무 많이 걸릴 수 있습니다. 도움이 되는 온라인 가이드가 제공 됩니다. [분석 및 보고를 위해 MICROSOFT BI (비즈니스 인텔리전스) 도구 선택을](https://go.microsoft.com/fwlink/?linkid=839877)참조 하세요.
  
### <a name="what-if-i-dont-upgrade-now"></a>지금 업그레이드 하지 않을 경우 어떻게 하나요?

즉시 업그레이드 하지 않도록 선택할 수 있습니다. 기존 서버와 응용 프로그램은 계속 실행 됩니다. 그러나 지원이 종료 된 후에는 보안 업데이트를 포함 하 여 추가 업데이트를 받을 수 없습니다. 그리고 서버 응용 프로그램에서 문제가 발생 하면 Microsoft 기술 지원 서비스에서 도움을 받을 수 없습니다.
  
## <a name="how-do-i-plan-my-upgrade"></a>업그레이드를 계획 하려면 어떻게 해야 하나요?

업그레이드 옵션을 살펴본 후에는 업그레이드 계획을 준비 해야 합니다. 다음 섹션에는 도움이 되는 정보 및 추가 리소스가 포함 되어 있습니다. 클라우드 또는 온-프레미스에서 둘 다 작동 하며 온-프레미스 전용인 두 가지 기본 옵션은 다음과 같습니다.
  
|**옵션**|**클라우드 또는 온-프레미스에서**|
|:-----|:-----|
|[SharePoint Server가 포함 된 Excel (온-프레미스)](#excel-with-sharepoint-server-on-premises) <br/> |모두  <br/> |
|[Power BI](#use-power-bi-in-the-cloud-or-on-premises)<br/> |모두  <br/> |
|[보고 서비스](#use-reporting-services-on-premises) <br/> |온-프레미스 전용  <br/> |
|[PerformancePoint Services](#use-performancepoint-services-on-premises) <br/> |온-프레미스 전용  <br/> |
   
### <a name="use-excel-in-the-cloud-or-on-premises"></a>Excel 사용 (클라우드 또는 온-프레미스)

SharePoint Server에서 excel *서비스가* 라고도 하는 excel에서는 excel이 컴퓨터에 설치 되어 있지 않아도 브라우저 창에서 통합 문서를 보고 사용할 수 있습니다. Excel을 사용 하 여 보고서, 성과 기록표 및 대시보드를 만들 수 있습니다. 그런 다음 Microsoft 365 또는 SharePoint Server 온-프레미스에서 SharePoint Online을 사용 하 고 있는지 여부에 관계 없이 브라우저에서 Excel을 사용할 수 있는 다른 사람과 통합 문서를 공유 합니다. 온-프레미스 또는 클라우드에서 저장 된 데이터를 사용 하 여 다양 한 데이터 원본을 사용할 수 있습니다.
  
다음 표에서는 excel을 Microsoft 365와 함께 사용 하 여 SharePoint Server에서 Excel을 사용 하는 경우의 주요 이점을 비교 합니다. 자세한 내용은 다음과 같습니다.
  
|**Microsoft 365 (클라우드에서)가 있는 Excel**|**SharePoint Server가 포함 된 Excel (온-프레미스)**|
|:-----|:-----|
|**가장 큰 최신 버전의 Excel** 이 제공 됩니다. Microsoft 365에는 강력한 새 차트 종류, 차트 및 테이블을 쉽고 빠르게 만들 수 있는 기능, 더 많은 데이터 원본을 지 원하는 최신 버전의 Excel이 제공 됩니다. <br/> <br/> **설치 과정은 훨씬 간단해 집니다**. Excel이 Microsoft 365 for business에 포함 되어 있으므로 사용자의 작업이 더 이상 수행 되지 않습니다. 등록 및 로그인 하 고 온-프레미스 서버를 업그레이드 하는 경우 보다 더 빠르고 더 효율적으로 작업을 진행 합니다. <br/> <br/> **모든 사용자에 게 통합 문서에 대 한 모든 권한이 있습니다**. 사용자는 자신의 컴퓨터, 스마트폰, 태블릿을 사용 하 여 모든 위치에서 통합 문서를 안전 하 게 볼 수 있습니다. <br/> <br/> **거기 더 있어!** [Excel 및 Office 365의 BI 기능을](https://support.office.com/article/26c0548e-124c-4fd3-aab3-5f64568cb743.aspx)참조 하세요. <br/> |**전역 설정을 관리** 합니다. SharePoint 관리자는 보안, 부하 분산, 세션 관리, 통합 문서 캐싱, 외부 데이터 연결 등의 전역 설정을 지정할 수 있습니다. <br/> <br/> **PerformancePoint services에서 Excel Services를 사용할 수** 있습니다. SharePoint Server 설치의 일부로 Excel Services 및 PerformancePoint Services를 구성 하 고 PerformancePoint 대시보드에 Excel Services 보고서를 포함할 수 있습니다. <br/> <br/> **거기 더 있어!** [Excel 및 Excel Services의 비즈니스 인텔리전스 (SharePoint Server 2013)를](https://support.office.com/article/2740f10c-579d-4b40-a1d9-7beb5d38547c.aspx)참조 하세요. <br/> |
   
#### <a name="excel-with-microsoft-365-in-the-cloud"></a>Microsoft 365 (클라우드에서)가 있는 Excel

Microsoft 365로 이동 하면 Excel 2016를 포함 하 여 최신 서비스와 응용 프로그램을 사용할 수 있습니다. Microsoft 365에서는 PerformancePoint Services를 사용할 수 없으므로 PerformancePoint 대시보드 콘텐츠를 Excel 통합 문서 또는 다른 보고서로 대체할 수 있습니다. 좋은 소식은 Excel 2016에 새로운 차트 유형이 많고 Excel에서 인상적인 대시보드를 만드는 것이 더 쉽다는 것입니다. 그리고 주기적으로 새로운 기능이 추가 됩니다. 자세한 내용은 [What 'S New In Excel 2016 In Windows](https://support.office.com/article/5fdb9208-ff33-45b6-9e08-1f5cdb3a6c73.aspx)를 참조 하세요.
  
또한 Microsoft 365 중 일부를 50 구매한 경우 Microsoft FastTrack 팀에서 설정 하는 데 도움을 받을 수 있습니다. 자세한 내용을 보려면 [Fasttrack](https://www.microsoft.com/fasttrack/microsoft-365)를 방문 하세요.
  
#### <a name="excel-with-sharepoint-server-on-premises"></a>SharePoint Server가 포함 된 Excel (온-프레미스)

최신 버전의 SharePoint로 업그레이드 하는 경우 다음과 같이 excel Services 또는 브라우저에서 Excel을 사용할 수 있습니다.
  
- SharePoint Server 2010의 Excel Services
    
- SharePoint Server 2013의 Excel Services
    
- Office Online Server의 일부인 Excel이 SharePoint Server 2016와 별도로 설치 됨
    
새 버전의 SharePoint Server 에서도 PerformancePoint Services를 구성 하 고 Excel과 함께 사용할 수 있습니다.
  
SharePoint 업그레이드 옵션에 대 한 자세한 내용은 [Sharepoint Server 2007 end Support 로드맵](sharepoint-2007-end-of-support.md)를 참조 하십시오.
  
Excel 서비스에 대 한 자세한 내용은 [Excel services overview (SharePoint Server 2010)](https://go.microsoft.com/fwlink/?linkid=841362)를 참조 하십시오.
  
### <a name="use-power-bi-in-the-cloud-or-on-premises"></a>Power BI 사용 (클라우드 또는 온-프레미스)

Power BI는 데이터를 분석 하 고 정보를 공유 하는 비즈니스 분석 도구 모음입니다. Power BI에서는 온-프레미스 또는 온라인 데이터 원본을 사용 하 여 대화형 보고서와 대시보드를 만들 수 있습니다. 사용자는 자신의 컴퓨터나 모바일 장치에서 보고서 및 대시보드를 보고 사용할 수 있습니다.
  
Power BI는 Microsoft 365 또는 SharePoint Server의 일부가 아닙니다. Power BI 데스크톱, Power BI 게이트웨이 및 Power BI 서비스를 포함 하는 별도의 제공입니다. Power BI도 SharePoint Online과 통합 됩니다. Power BI를 무료로 시작할 수 있습니다. 데이터 사용량 및 비즈니스 요구 사항에 따라 나중에 Microsoft 365 E5를 사용 하 여 Power BI Pro로 업그레이드할 수 있습니다. 자세한 내용은 [POWER BI 란?](https://go.microsoft.com/fwlink/?linkid=841341) 를 참조 하세요.
  
### <a name="use-reporting-services-on-premises"></a>Reporting Services 사용 (온-프레미스)

SQL Server Reporting Services는 강력한 보고 솔루션을 제공 합니다. 기본 모드 또는 SharePoint 통합 모드에서 Reporting Services를 구성할 수 있습니다. 보고서 디자이너, 보고서 작성기, Power View 등 다양 한 도구를 사용 하 여 보고서를 작성할 수 있습니다. SQL Server의 최신 버전에서는 SQL Server Mobile Report Publisher를 사용 하 여 모든 화면 크기로 확장 되는 보고서를 배달할 수도 있습니다. 이렇게 하면 보는 사람이 모바일 장치에서 보고서를 사용할 수 있습니다. 자세한 내용은 [SQL Server Reporting Services (SSRS): 모바일 및 페이지를 매긴 보고서 만들기, 배포 및 관리](https://go.microsoft.com/fwlink/?linkid=841342)를 참조 하세요.
  
### <a name="use-performancepoint-services-on-premises"></a>온-프레미스에 PerformancePoint Services 사용

PerformancePoint Server 2007는 SharePoint Server 2007와 별도로 판매 되었습니다. SharePoint Server 2010부터 PerformancePoint Services는 SharePoint Server의 서비스 응용 프로그램입니다. 따라서 PerformancePoint Services를 사용 하기 위해 별도의 서버 라이선스 또는 하드웨어를 구입할 필요가 없습니다.
  
PerformancePoint Server 2007에서 PerformancePoint Services로 이동 하려면 최신 버전의 SharePoint Server으로 이동 하 고 PerformancePoint Services를 구성 합니다. 이동 하는 SharePoint Server 버전에 따라 PerformancePoint Server 2007의 기존 대시보드 콘텐츠를 PerformancePoint Services로 가져올 수 있는지 여부가 결정 됩니다.
  
- SharePoint Server 2010로 업그레이드 하는 경우 performancepoint Server 2007에서 SharePoint Server 2010의 performancepoint Services로 PerformancePoint 대시보드 콘텐츠를 가져올 수 있습니다. 자세한 내용은 [가져오기 마법사: PerformancePoint server 2007 content To SharePoint Server 2010를](https://go.microsoft.com/fwlink/?linkid=838873)참조 하세요.
    
- SharePoint Server 2013 또는 SharePoint Server 2016로 이동 하는 경우에는 새 대시보드 콘텐츠 (데이터 원본, 보고서, 성과 기록표 및 대시보드 페이지)를 만들어야 하는 경우가 많습니다.
    
PerformancePoint Services 업그레이드 계획을 시작 하려면 다음 리소스를 참조 하세요.
  
- [SharePoint Server 2007 지원 로드맵 종료](sharepoint-2007-end-of-support.md)
    
- 이동 하려는 SharePoint 버전을 알고 있는 경우 PerformancePoint Services에 대 한 해당 문서를 참조 하세요.
    
  - [PerformancePoint Services 계획(SharePoint Server 2010)](https://go.microsoft.com/fwlink/?linkid=841363)
    
  - [SharePoint Server 2013의 PerformancePoint Services 개요](https://go.microsoft.com/fwlink/?linkid=841551)
    
  - [SharePoint Server 2016의 PerformancePoint Services 개요](https://go.microsoft.com/fwlink/?linkid=874704)
    
PerformancePoint Services로 업그레이드할 때는 몇 가지 새로운 기능과 향상 된 기능을 사용할 수 있습니다. PerformancePoint Services에서는 향상 된 성과 기록표를 제공 합니다. 새 시각화 (예: 분해 트리 및 KPI 세부 정보 보고서) 차트 종류 더 보기 보다 효율적인 시간 인텔리전스 필터링 기능 향상 된 내게 필요한 옵션 준수 자세한 내용은 [What 's new For PerformancePoint Services (SharePoint Server 2010)](https://go.microsoft.com/fwlink/?linkid=841343)을 참조 하십시오.
  
## <a name="where-can-i-get-help-with-my-upgrade"></a>업그레이드에 대 한 도움말은 어디에서 얻을 수 있나요?

온-프레미스를 업그레이드 하 든 Microsoft 365로 이동 하 든 관계 없이 Microsoft 파트너와 함께 작업 하는 것이 좋습니다. 정규 파트너는 비즈니스 요구 사항을 가장 잘 충족 하는 솔루션을 식별 하 고 배포에 도움을 주는 데 도움이 됩니다. [Microsoft 파트너 센터](https://go.microsoft.com/fwlink/?linkid=841249)를 방문 하 고 검색 필터를 사용 하 여 솔루션 공급자를 찾습니다.
  
## <a name="related-topics"></a>관련 항목

[Office 2007 서버 및 클라이언트에서 업그레이드 하는 데 도움이 되는 리소스](upgrade-from-office-2007-servers-and-products.md)