---
title: Exchange, SharePoint, 비즈니스용 Skype 및 Lync에 대한 아키텍처 모델
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/16/2018
audience: ITPro
ms.topic: conceptual
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- SPO_Content
f1.keywords:
- CSH
ms.custom:
- Ent_Architecture
ms.assetid: 5b49fa68-f8f2-4705-af96-5f5475e8539a
search.appverid:
- MET150
description: SharePoint, Exchange, 비즈니스용 Skype 및 Lync에 대 한 아키텍처 모델, 배포 및 플랫폼 옵션을 설명 하는 IT 포스터를 제공 합니다.
ms.openlocfilehash: 6d5cda89fb67f5c41dcf161abe7258c4600ee8ce
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48919823"
---
# <a name="architectural-models-for-sharepoint-exchange-skype-for-business-and-lync"></a>Exchange, SharePoint, 비즈니스용 Skype 및 Lync에 대한 아키텍처 모델

이 문서의 IT 포스터에서는 SharePoint, Exchange, 비즈니스용 Skype 및 Lync에 대 한 아키텍처 모델 및 배포 옵션에 대해 설명 합니다. 또한 Microsoft Azure에서 SharePoint를 배포 하기 위한 디자인 정보를 제공 합니다.
  
Microsoft 365을 사용 하 여 클라우드를 통해 익숙한 공동 작업 및 통신 서비스를 제공할 수 있습니다. 몇 가지 예외를 제외 하면 온-프레미스 배포를 유지 관리 하거나 Microsoft 365을 사용 하 든 상관 없이 사용자 환경이 동일 하 게 유지 됩니다. 

이 통합 사용자 환경에서는 각 작업을 배치할 위치를 결정 하는 것이 복잡해 집니다. 또한 다음과 같은 질문이 발생 합니다.
  
- 개별 작업의 플랫폼을 선택 하려면 어떻게 해야 합니까?
    
- 모든 서비스를 온-프레미스에 두는 것이 적절할까요?
    
- 하이브리드 배포에 적합 한 시나리오는 무엇 인가요?
    
- Azure는 어떻게 그림에 적합 합니까?
    
- Azure에서 지 원하는 Office server 작업의 구성은 무엇입니까?
    
> [!TIP]
> 이 문서에 나오는 대부분의 포스터는 여러 언어로 제공 됩니다. 사용할 수 있는 언어에는 중국어, 영어, 프랑스어, 독일어, 이탈리아어, 일본어, 한국어, 포르투갈어, 러시아어 및 스페인어가 포함 되어 있습니다. 이러한 언어 중 하나에서 포스터를 다운로드 하려면 포스터 축소판 그림 이미지에서 **더 많은 언어** 를 선택 합니다.
  
의견을 전달해주세요! [cloudadopt@microsoft.com](mailto:cloudadopt@microsoft.com)로 메일을 보내주세요. 
  
다음 링크를 사용 하 여 필요한 포스터를 가져올 수 있습니다.
  
- **아키텍처 모델** : 이러한 리소스를 사용 하 여 SharePoint 2016 및 비즈니스용 Skype 2015에 이상적인 플랫폼과 구성을 확인할 수 있습니다.
    
  - [Microsoft SharePoint 2016 아키텍처 모델](architectural-models-for-sharepoint-exchange-skype-for-business-and-lync.md#SP2016_ArchModel)
    
  - [SharePoint Server 2016 데이터베이스](architectural-models-for-sharepoint-exchange-skype-for-business-and-lync.md#SP2016_Databases)
    
  - [Microsoft 비즈니스용 Skype 2015 아키텍처 모델](architectural-models-for-sharepoint-exchange-skype-for-business-and-lync.md#SfB2015_ArchModel)
    
- **Platform** : 이러한 리소스를 사용 하 여 SharePoint 2013, Exchange 2013 및 Lync 2013에 이상적인 플랫폼과 구성을 확인할 수 있습니다.
    
  - [SharePoint 2013 플랫폼 옵션](architectural-models-for-sharepoint-exchange-skype-for-business-and-lync.md#SP2013_Options)
    
  - [Exchange 2013 플랫폼 옵션](architectural-models-for-sharepoint-exchange-skype-for-business-and-lync.md#Exch2013_options)
    
  - [Lync 2013 플랫폼 옵션](architectural-models-for-sharepoint-exchange-skype-for-business-and-lync.md#Lync2013_Options)
    
- **Azure의 Sharepoint server 2013** : 이러한 IT 포스터를 사용 하 여 azure 인프라 서비스에서 sharepoint server 2013 작업을 디자인 하 고 구성 합니다.
    
  - [SharePoint Server 2013을 사용 하는 Azure의 인터넷 사이트](architectural-models-for-sharepoint-exchange-skype-for-business-and-lync.md#Azure_sharepoint2013)
    
  - [디자인 샘플: SharePoint 용 Azure의 인터넷 사이트 2013](architectural-models-for-sharepoint-exchange-skype-for-business-and-lync.md#DesignSampleInternetSites)
    
  - [Azure로의 SharePoint 재해 복구](architectural-models-for-sharepoint-exchange-skype-for-business-and-lync.md#sharepoint_recovery_Azure)
    
## <a name="architectural-models-posters"></a>아키텍처 모델 포스터

SharePoint 2016 및 비즈니스용 Skype 2015의 IT 포스터는 인쇄 하기 쉬운 형식으로 배포 방법을 비교 하는 방법을 제공 합니다. 포스터에는 모든 구성 또는 플랫폼 옵션이 나열 되어 있습니다. 각 옵션에 대해 다음 정보를 제공 합니다.
  
- **개요** : 개념적 다이어그램을 포함 하 여 플랫폼에 대 한 간략 한 요약을 소개 합니다.
    
- **최상** : 플랫폼에 가장 적합 한 일반적인 시나리오입니다.
    
- **라이선스 요구 사항** : 배포에 필요한 라이선스
    
- **아키텍처 작업** : 설계자로 수행 해야 하는 결정 사항입니다.
    
- **It 전문가 작업 또는 책임** : it 직원이 계획 해야 하는 일일 책임입니다.
    
<a name="SP2016_ArchModel"> </a>
### <a name="microsoft-sharepoint-server-2016-architectural-models"></a>Microsoft SharePoint Server 2016 아키텍처 모델

|항목|설명|
|---|---|
|[![SharePoint Server 2016 아키텍처 모델 포스터의 축소판 그림입니다.](../media/7d3e590c-1f3b-42cf-920d-9edac8fa3e04.png)          ](https://www.microsoft.com/download/details.aspx?id=52650) <br/> [PDF](https://download.microsoft.com/download/4/F/A/4FA0F94B-EE2F-41DB-A047-D9864FEF41E9/SharePoint2016ArchitecturalModels.pdf)  \| [Visio](https://download.microsoft.com/download/4/F/A/4FA0F94B-EE2F-41DB-A047-D9864FEF41E9/SharePoint2016ArchitecturalModels.vsdx)  \| [추가 언어](https://www.microsoft.com/download/details.aspx?id=52650)|이 IT 포스터는 비즈니스 의사 결정권자 및 솔루션 설계자가 알고 있어야 하는 SharePoint Online, Azure 및 SharePoint 온-프레미스 구성에 대해 설명 합니다. <br/><br/> - **Sharepoint Online (saas)** : saas (software as a service) 구독 모델을 통해 SharePoint를 사용 합니다. <br/> - **Sharepoint 하이브리드** : 사용자가 직접 sharepoint 사이트 및 앱을 클라우드로 이동 합니다. <br/> - **Azure의 SharePoint (IaaS)** : 온-프레미스 환경을 Azure로 확장 하 고 여기에 sharepoint 2016 서버를 배포 합니다. (이 모델은 고가용성 또는 재해 복구 환경 및 개발/테스트 환경에 권장 됩니다.) <br/> - **Sharepoint 온-프레미스** : 유지 관리 하는 데이터 센터에서 sharepoint 환경을 계획, 배포, 유지 관리 및 사용자 지정 합니다.|
   
<a name="SP2016_Databases"> </a>
### <a name="sharepoint-server-2016-databases"></a>SharePoint Server 2016 데이터베이스

|항목|설명|
|---|---|
|[![SharePoint Server 2016 데이터베이스 포스터의 축소판 그림입니다.](../media/c53e9de7-3bf8-446d-8766-e6700c8dd8e1.png)](https://www.microsoft.com/download/details.aspx?id=55041) <br/> [PDF](https://download.microsoft.com/download/D/5/D/D5DC1121-8BC5-4953-834F-1B5BB03EB691/DBrefguideSPS2016_tabloid.pdf)  \| [Visio](https://download.microsoft.com/download/D/5/D/D5DC1121-8BC5-4953-834F-1B5BB03EB691/DBrefguideSPS2016_tabloid.vsdx)  \| [추가 언어](https://www.microsoft.com/download/details.aspx?id=55041)|이 IT 포스터는 SharePoint Server 2016 데이터베이스에 대 한 빠른 참조입니다. 각 데이터베이스에 대 한 세부 정보를 볼 수 있습니다. <br/><br/> - 크기 <br/> - 크기 조정 지침 <br/> - I/O 패턴 <br/> - 요구 사항 <br/><br/>  첫 번째 페이지에는 SharePoint 시스템 데이터베이스 및 여러 데이터베이스를 포함 하는 서비스 응용 프로그램이 표시 됩니다. 두 번째 페이지에는 단일 데이터베이스가 있는 모든 서비스 응용 프로그램이 표시됩니다. <br/><br/>  자세한 내용은 [SharePoint Server 2016의 데이터베이스 형식 및 설명을](https://docs.microsoft.com/SharePoint/technical-reference/database-types-and-descriptions)참조 하세요.|
   
<a name="SfB2015_ArchModel"> </a>
### <a name="microsoft-skype-for-business-2015-architectural-models"></a>Microsoft 비즈니스용 Skype 2015 아키텍처 모델

|항목|설명|
|---|---|
|[![비즈니스용 Skype 아키텍처 모델 포스터의 축소판 그림입니다.](../media/132288c0-6ae4-4394-88ab-b57dae367714.png)](https://www.microsoft.com/download/details.aspx?id=55022) <br/> [PDF](https://download.microsoft.com/download/7/7/4/7741262C-A60D-41F7-863B-99BF5964FBFE/Skype%20for%20Business%20Architectural%20Models.pdf)  \| [Visio](https://download.microsoft.com/download/7/7/4/7741262C-A60D-41F7-863B-99BF5964FBFE/Skype%20for%20Business%20Architectural%20Models.vsd)  \| [추가 언어](https://www.microsoft.com/download/details.aspx?id=55022)|이 포스터는 비즈니스용 Skype Online, 온-프레미스, 하이브리드 및 클라우드 PBX (private branch exchange)에 대해 설명 합니다. 또한 비즈니스 의사 결정권자 및 솔루션 설계자가 알고 있어야 하는 Exchange 및 SharePoint 구성과의 통합에 대해 설명 합니다. <br/><br/> 이 포스터는 IT 전문가가 비즈니스용 Skype 온라인 및 비즈니스용 Skype 온-프레미스를 사용할 수 있는 기본 아키텍처 모델의 인식을 높이기 위한 것입니다. <br/><br/>조직의 요구 사항 및 계획에 가장 적합 한 구성을 사용 하 여 시작 합니다. 필요에 따라 다른 구성을 고려 하 고 사용 합니다. 예를 들어 Exchange 및 SharePoint와의 통합을 고려 하거나 Microsoft 클라우드 PBX 제공을 활용 하는 솔루션을 고려해 볼 수 있습니다.|
   
## <a name="platform-options-posters"></a>플랫폼 옵션 포스터

SharePoint 2013, Exchange 2013 및 Lync 2013 용 IT 포스터는 배포 방법을 한눈에 비교할 수 있는 방법을 제공 합니다. 각 포스터에는 모든 구성 또는 플랫폼 옵션이 나열 되어 있습니다. 각 옵션에 대해 다음 정보를 제공 합니다.
  
- **개요** : 개념적 다이어그램을 포함 하 여 플랫폼에 대 한 간략 한 요약을 소개 합니다.
    
- **최상** : 플랫폼에 가장 적합 한 일반적인 시나리오입니다.
    
- **라이선스 요구 사항** : 배포에 필요한 라이선스
    
- **아키텍처 작업** : 설계자로 수행 해야 하는 결정 사항입니다.
    
- **It 전문가 작업 또는 책임** : it 직원이 계획 해야 하는 일일 책임입니다.
    
<a name="SP2013_Options"> </a>
## <a name="sharepoint-2013-platform-options"></a>SharePoint 2013 플랫폼 옵션

|항목|설명|
|---|---|
|[![SharePoint 2013 플랫폼 옵션 포스터의 축소판 그림 이미지입니다.](../media/SP-PlatformOptions.jpg)](https://www.microsoft.com/download/details.aspx?id=40332) <br/> [PDF](https://go.microsoft.com/fwlink/p/?LinkId=324594)  \| [Visio](https://go.microsoft.com/fwlink/p/?LinkId=324593)  \| [추가 언어](https://www.microsoft.com/download/details.aspx?id=40332)|비즈니스 의사 결정권자 및 설계자의 경우이 포스터는 SharePoint 2013, SharePoint의 Microsoft 365, 온-프레미스 하이브리드, Microsoft 365, Azure 및 온-프레미스 전용 배포의 플랫폼 옵션을 보여 줍니다. 여기에는 각 아키텍처, 추천, 라이선스 요구 사항에 대 한 개요와 각 플랫폼에 대 한 IT 전문가 및 IT pro 작업 목록이 포함 되어 있습니다. 포스터는 Azure에서 여러 SharePoint 솔루션을 강조 표시 합니다.|
   
<a name="Exch2013_options"> </a>
## <a name="exchange-2013-platform-options"></a>Exchange 2013 플랫폼 옵션

|항목|설명|
|---|---|
|[![Exchange 플랫폼 옵션 포스터의 축소판 그림 이미지입니다.](../media/ITPro-Other-Exchange2013PlatformOptions.jpg)          ](https://www.microsoft.com/download/details.aspx?id=42676) <br/> [PDF](https://go.microsoft.com/fwlink/p/?LinkID=398740)  \| [Visio](https://go.microsoft.com/fwlink/p/?LinkID=398742)  \| [추가 언어](https://www.microsoft.com/download/details.aspx?id=42676)|비즈니스 의사 결정권자 및 설계자는이 포스터에 Exchange 2013의 플랫폼 옵션에 대 한 설명이 나와 있습니다. 고객은 Microsoft 365, 하이브리드 Exchange, Exchange Server 온-프레미스 및 호스팅된 Exchange를 사용 하 여 Exchange Online에서 선택할 수 있습니다. 포스터는 각 아키텍처 옵션에 대 한 세부 정보 (각, 라이선스 요구 사항 및 IT 전문가 책임)를 포함 합니다.|
   
<a name="Lync2013_Options"> </a>
## <a name="lync-2013-platform-options"></a>Lync 2013 플랫폼 옵션

|항목|설명|
|---|---|
|[![Lync 2013 플랫폼 옵션 포스터의 축소판 그림 이미지입니다.](../media/Lync-PlatformOptions.jpg)          ](https://www.microsoft.com/download/details.aspx?id=41677) <br/> [PDF](https://go.microsoft.com/fwlink/p/?LinkID=391837)  \| [Visio](https://go.microsoft.com/fwlink/p/?LinkID=391839)  \| [추가 언어](https://www.microsoft.com/download/details.aspx?id=41677)|이 포스터는 비즈니스 의사 결정권자와 설계자를 위해 Lync 2013의 플랫폼 옵션에 대해 설명 합니다. 고객은 Microsoft 365, hybrid Lync, Lync Server 온-프레미스 및 호스팅된 Lync를 사용 하 여 Lync Online에서 선택할 수 있습니다. IT 포스터는 각 아키텍처 옵션, 라이선스 요구 사항 및 IT 전문가 책임에 대 한 이상적인 시나리오를 포함 하 여 설명 합니다.|
   
<a name="Lync2013_Options"> </a>
## <a name="sharepoint-in-azure-solutions-posters"></a>Azure의 SharePoint 솔루션 포스터

Azure의 SharePoint 용 IT 포스터는 SharePoint Server 2013를 사용 하는 Azure 기반 솔루션을 보여 줍니다.
  
<a name="Azure_sharepoint2013"> </a>
### <a name="internet-sites-in-microsoft-azure-using-sharepoint-server-2013"></a>SharePoint Server 2013을 사용 하는 Microsoft Azure의 인터넷 사이트

|항목|설명|
|---|---|
|[![SharePoint Server 2013 포스터를 사용 하는 Azure의 인터넷 사이트 이미지입니다.](../media/MS-AZ-SPInternetSites.jpg)          ](https://www.microsoft.com/download/details.aspx?id=41992) <br/> [PDF](https://go.microsoft.com/fwlink/p/?LinkId=392552)  \| [Visio](https://go.microsoft.com/fwlink/p/?LinkId=392551)  \| [추가 언어](https://www.microsoft.com/download/details.aspx?id=41992)|이 포스터는 Azure의 인터넷 연결 사이트용 주요 디자인 활동 및 권장 아키텍처에 대해 간략하게 설명 합니다.  <br/><br/> 자세한 내용은 다음 문서를 참조하세요.  <br/><br/> - [SharePoint Server 2013을 사용 하는 Azure의 인터넷 사이트](internet-sites-in-microsoft-azure-using-sharepoint-server-2013.md) <br/> - [SharePoint 용 Azure 아키텍처 2013](microsoft-azure-architectures-for-sharepoint-2013.md)|
   
<a name="DesignSampleInternetSites"> </a>
### <a name="internet-sites-in-azure-for-sharepoint-2013"></a>SharePoint 용 Azure 2013의 인터넷 사이트

|항목|설명|
|---|---|
|[![SharePoint Server 2013 포스터에 대 한 Microsoft Azure의 인터넷 사이트 이미지입니다.](../media/MS-AZ-InternetSitesDesignSample.jpg)          ](https://www.microsoft.com/download/details.aspx?id=41991) <br/> [PDF](https://go.microsoft.com/fwlink/p/?LinkId=392549)  \| [Visio](https://go.microsoft.com/fwlink/p/?LinkId=392548)  \| [추가 언어](https://www.microsoft.com/download/details.aspx?id=41991)|이 디자인 예제를 SharePoint Server 2013을 사용 하 여 Azure에서 인터넷 연결 사이트의 고유한 아키텍처를 소개 하는 출발점으로 사용 합니다. <br/><br/> 자세한 내용은 다음 문서를 참조하세요.  <br/><br/> - [SharePoint Server 2013을 사용 하는 Azure의 인터넷 사이트](internet-sites-in-microsoft-azure-using-sharepoint-server-2013.md) <br/> - [SharePoint 용 Azure 아키텍처 2013](microsoft-azure-architectures-for-sharepoint-2013.md)|
   
<a name="sharepoint_recovery_Azure"> </a>
### <a name="sharepoint-disaster-recovery-to-microsoft-azure"></a>Microsoft Azure로의 SharePoint 재해 복구

|항목|설명|
|---|---|
|[![Azure에 대 한 SharePoint 재해 복구 프로세스의 포스터 이미지입니다.](../media/SP-DR-Azure.png)          ](https://www.microsoft.com/download/details.aspx?id=41993) <br/> [PDF](https://go.microsoft.com/fwlink/p/?LinkId=392555)  \| [Visio](https://go.microsoft.com/fwlink/p/?LinkId=392554)  \| [추가 언어](https://www.microsoft.com/download/details.aspx?id=41993)|이 IT 포스터는 Azure의 재해 복구 환경에 대한 아키텍처 원리를 표시합니다. <br/><br/> 자세한 내용은 다음 문서를 참조하십시오.  <br/><br/> - [Azure의 SharePoint Server 2013 재해 복구](sharepoint-server-2013-disaster-recovery-in-microsoft-azure.md) <br/> - [SharePoint 용 Azure 아키텍처 2013](microsoft-azure-architectures-for-sharepoint-2013.md)|
   
## <a name="see-also"></a>참고 항목

- [Microsoft 365 솔루션 및 아키텍처 센터](../solutions/solution-architecture-center.md)
  
- [Microsoft 클라우드 아키텍처 모델](../solutions/cloud-architecture-models.md)
  
- [Microsoft 365 테스트 랩 가이드](m365-enterprise-test-lab-guides.md)
  
- [하이브리드 솔루션](hybrid-solutions.md)

