---
title: 핵심 데이터를 새로운 Microsoft 365 datacenter (지역)로 이동
ms.author: andyber
author: andybergen
manager: laurawi
ms.date: 12/10/2019
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0a35176a-e585-4dec-a90b-36be8314667f
f1.keywords:
- NOCSH
description: 새로운 Office 365 데이터 센터의 지역 및 data 상주 옵션을 사용 하 여 핵심 데이터를 새 지역으로 이동 하도록 요청 하는 방법에 대해 알아봅니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 6c5e63a973ca6fdf6aaaaca884df306ff790c325
ms.sourcegitcommit: 1db81b85d327fe423695ce675ad325e538417211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49349247"
---
# <a name="moving-core-data-to-new-microsoft-365-datacenter-geos"></a>핵심 데이터를 새로운 Microsoft 365 datacenter (지역)로 이동

Microsoft 365 서비스에 대 한 새 데이터 센터 지역가 계속 해 서 열립니다. 이러한 새 데이터 센터 지역는 지속적인 고객 요구 및 사용 증가를 지원 하기 위해 용량을 추가 하 고 리소스를 계산 합니다. 또한 새 데이터 센터 지역는 핵심 고객 데이터에 대 한 상주 데이터를 제공 합니다. 

핵심 고객 데이터는 다음을 포함 하는 고객 데이터의 하위 집합을 지칭 하는 용어입니다. 
- Exchange Online 사서함 콘텐츠 (전자 메일 본문, 일정 항목 및 전자 메일 첨부 파일 콘텐츠)
- SharePoint Online 사이트 콘텐츠 및 해당 사이트 내에 저장 된 파일
- 비즈니스용 OneDrive에 업로드 된 파일
- 채팅에 사용 되는 개인 메시지, 채널 메시지 및 이미지를 비롯 한 팀 채팅 메시지
  
핵심 고객 데이터가 기존 데이터 센터 지역에 이미 저장되어 있는 기존 고객은 새 데이터 센터 지역의 시작에 영향을 받지 않습니다. Microsoft는 새 데이터 센터 지역에 고유한 기능 또는 규정 준수 인증을 도입하지 않습니다. 두 지역 중 어떤 지역의 고객이든 이전과 동일한 서비스 품질, 성능 및 보안 제어를 경험할 수 있습니다. 아래 표에 나열 된 기존 고객은 rest에서 조직의 핵심 고객 데이터를 새 데이터 센터 지역으로 초기 마이그레이션을 요청 하는 옵션을 제공 합니다.
  
|**테 넌 트 등록 국가를 사용 하는 고객**|**이전 데이터 센터 지역**|**새 데이터 센터 지역**|**지역 서비스 재개 시점**|
|:-----|:-----|:-----|:-----|
|**일본**| 아시아/태평양 | 일본 | 2014년 12월 |
|**오스트레일리아, 뉴질랜드, 피지**| 아시아/태평양 | 오스트레일리아 | 2015년 3월 |
|**인도**| 아시아/태평양 | 인도 | 2015년 10월 |
|**캐나다**| 미국 | 캐나다 | 2016년 5월 |
|**영국**| 유럽 연합 | 영국 | 2016년 9월 |
|**대한민국**| 아시아/태평양 | 대한민국 | 2017년 4월 |
|**프랑스**| 유럽 연합 | 프랑스 | 2018년 3월 |
|**아랍에미리트**| 유럽 연합 | 아랍에미리트 | 2019년 6월 |
|**남아프리카 공화국**| 유럽 연합 | 남아프리카 공화국 | 2019년 7월 |
|**스위스, 리히텐슈타인**| 유럽 연합 | 스위스 | 2019년 12월 |
|**독일**| 유럽 연합 | 독일 | 2019년 12월 |
|**노르웨이**| 유럽 연합 | 노르웨이 | 2020년 4월 |
|**브라질**| 아메리카 | 브라질 | 11 월 2020 |

10 월 1 일 (으)로 2020, 테 넌 트에 포함 된 Office 365 교육 구독을 사용 하는 고객은 마이그레이션에 적합 하지 않습니다.

전체 데이터 센터 geos, 데이터 센터 및 나머지 고객 데이터 위치는 [대화형 데이터 센터 맵의](https://office.com/datamaps)일부로 사용할 수 있습니다. 
  
## <a name="data-residency-option"></a>데이터 상주 옵션

Microsoft는 위의 표에 나열 된 데이터 센터의 운영 체제에 포함 된 적격 한 마이크로소프트 365 고객에 게 data 상주 옵션을 제공 합니다. 이 옵션을 사용 하면 데이터 상주 요구 사항이 있는 적격 고객은 나머지 조직의 핵심 고객 데이터를 새로운 데이터 센터 지역으로 마이그레이션할 수 있습니다.  Microsoft는 등록 기간 동안 마이그레이션을 요청 하는 모든 적격 고객에 게 커밋된 마감 기한을 제공 합니다.  데이터 센터 지리적 등록 창에 대 한 자세한 내용을 확인 하 고 프로그램에 등록 하는 단계에 대 한 자세한 내용은 [data move를 요청 하는 방법](request-your-data-move.md) 페이지를 참조 하세요.  데이터 이동은 요청 기간이 완료 되 면 최대 24 개월까지 걸릴 수 있습니다.

Microsoft는 새 데이터 센터 지역에 고유한 기능 또는 규정 준수 인증을 도입하지 않습니다.
    
전체적으로 운영되는 자동화 환경에서 데이터 이동을 수행할 때 수반되는 복잡성, 정밀도 및 규모 때문에 귀하의 테넌트 또는 다른 단일 테넌트에서 데이터 이동이 완료될 것으로 예상되는 시기를 알려드리기가 어렵습니다. 고객은 데이터 이동이 완료되었을 때 메시지 센터에서 관련 서비스별로 1번의 확인을 받게 됩니다. 
    
데이터 이동은 최종 사용자에게 최소의 영향만 미치는 백 엔드 서비스 작업입니다. 영향을 받을 수 있는 기능은 [During and after your data move](during-and-after-your-data-move.md) 페이지에 나와 있습니다. 가용성을 위해 [Microsoft Online SERVICES SLA (서비스 수준 계약)](https://go.microsoft.com/fwlink/p/?LinkId=523897) 를 준수 하 고, 고객이 이동 중에 대비 하거나 모니터링 해야 하는 작업이 없습니다. 서비스 유지 관리에 대한 알림은 필요한 경우에 수행됩니다. 

데이터를 새 데이터 센터 지역으로 이동 하는 것은 고객에 게 추가 비용 없이 완료 됩니다.
    
## <a name="related-topics"></a>관련 항목 
 
[데이터 이동을 요청하는 방법](request-your-data-move.md)
    
[데이터 이동 일반 FAQ](data-move-faq.md)
  
[Microsoft Dynamics CRM Online에 대 한 새로운 데이터 센터 지역](https://go.microsoft.com/fwlink/p/?Linkid=615924)
  
[지역별 Azure services](https://azure.microsoft.com/regions/)
