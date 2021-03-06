---
title: Exchange 2007 지원 종료 로드맵
ms.author: dstrome
author: dstrome
manager: laurawi
ms.date: 1/31/2018
audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
ms.assetid: c3024358-326b-404e-9fe6-b618e54d977d
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
description: Exchange Server 2007의 지원 종료 후 옵션에 대해 알아보고 Microsoft 365, Office 365 또는 Exchange 2016으로의 마이그레이션 계획을 시작 합니다.
ms.openlocfilehash: 3f0a5c8ef9765a184358b932548eaa2ae7c59adc
ms.sourcegitcommit: d3ca8021f7da00a474ac14aac5f1358204a848f2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/01/2020
ms.locfileid: "49519848"
---
# <a name="exchange-2007-end-of-support-roadmap"></a>Exchange 2007 지원 종료 로드맵

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

Exchange Server 2007 4 월 2017 지원 종료에 도달 했습니다. Exchange 2007에서 Microsoft 365, Office 365 또는 Exchange 2016로 마이그레이션을 시작한 적이 없는 경우 이제 계획을 시작 하는 데 걸리는 시간입니다.
  
## <a name="what-does-end-of-support-mean"></a>*지원이 끝나는* 것은 무엇을 의미 하나요?

Exchange 서버에는 거의 모든 Microsoft 제품과 마찬가지로 새로운 기능, 버그 수정, 보안 픽스 등을 제공 하는 지원 주기가 있습니다. 이 수명 주기는 일반적으로 제품 초기 릴리스에서 10 년 동안 지속 됩니다. 이 수명 주기의 끝은 제품의 지원 종료 라고 합니다. Exchange 2007는 5 월 11 일, 2017에 대 한 지원 종료에 도달 했으므로 더 이상 다음을 제공 하지 않습니다.
  
- 발생할 수 있는 문제에 대 한 기술 지원
    
- 서버의 안정성 및 유용성에 영향을 줄 수 있는 문제에 대 한 버그 수정
    
- 보안 침해에 취약 한 서버를 만들 수 있는 취약성에 대 한 보안 수정
    
- 표준 시간대 업데이트
    
지원 종료 날짜 이후에는 Exchange 2007 설치가 계속 실행 됩니다. 그러나 새 업데이트나 지원이 없기 때문에 가능한 한 빨리 Exchange 2007에서 마이그레이션하는 것이 좋습니다.
  
지원 종료에 가까운 Office 2007 서버에 대 한 자세한 내용은 [office 2007 서버 및 제품에서 업그레이드 계획](upgrade-from-office-2007-servers-and-products.md)을 참조 하십시오.
  
## <a name="what-are-my-options"></a>내 옵션 이란?

다음을 수행할 수 있습니다.
  
- 가공선, 단계적 또는 하이브리드 마이그레이션을 사용 하 여 Microsoft 365로 마이그레이션
    
- Exchange 2007 서버를 온-프레미스 서버에서 새 버전의 Exchange로 마이그레이션합니다.
    
다음 섹션에서는 각 옵션에 대해 자세히 알아봅니다.
  
### <a name="migrate-to-microsoft-365"></a>Microsoft 365로 마이그레이션

Exchange 2007 배포를 중지 하는 데 도움이 되는 가장 간단 하 고 간단한 옵션은 전자 메일을 Microsoft 365로 마이그레이션하는 것입니다. Microsoft 365로 마이그레이션하는 경우 다음을 비롯 하 여 다음과 같은 10 년 이전 기술과의 최신 기능을 단일 홉으로 만들 수 있습니다.
  
- 보존 정책, In-Place 및 소송 보류, 원본 위치 eDiscovery 등의 규정 준수 기능
    
- Microsoft 365 그룹
    
- 중요 받은 편지함
    
- MyAnalytics
    
- 전자 메일, 일정, 연락처 등에 프로그래밍 방식으로 액세스 하는 데 사용할 수 있는 REST Api
    
Microsoft 365에는 새 기능을 먼저 제공 하므로, 사용자는 일반적으로 바로 사용을 시작할 수 있습니다. 다음에 대해 걱정할 필요가 없습니다.
  
- 하드웨어 구입 및 유지 관리
    
- 서버에 대 한 지불 및 냉각
    
- 보안, 제품 및 시간대 수정 사항에 대해 최신 상태를 유지 합니다.
    
- 준수 요구 사항을 지원 하기 위해 저장소 및 소프트웨어 유지 관리
    
- 새 버전의 Exchange로 업그레이드 하는 경우 Microsoft 365에서는 항상 최신 Exchange 버전을 사용 하 고 있습니다.
    
#### <a name="how-should-i-migrate-to-microsoft-365"></a>Microsoft 365로 마이그레이션하려면 어떻게 해야 하나요?

몇 가지 마이그레이션 옵션을 사용할 수 있습니다. 다음을 비롯 한 몇 가지 사항을 고려해 야 합니다.

- 이동 해야 하는 좌석 또는 사서함의 수입니다.
- 마이그레이션을 마지막으로 수행할 시간입니다.
- 마이그레이션 중에 온-프레미스 설치와 Microsoft 365 간의 원활한 통합이 필요한 지 여부

이 표에서는 마이그레이션 옵션 및 사용할 방법을 결정 하는 가장 중요 한 요소를 보여 줍니다.
  

|**마이그레이션 옵션**|**조직 크기**|**기간**|
|:-----|:-----|:-----|
|단독형 마이그레이션  <br/> |좌석 150 개 미만  <br/> |1 주 이내  <br/> |
|미리 구성된 마이그레이션  <br/> |150 개 이상  <br/> |몇 주 동안  <br/> |
|전체 하이브리드 마이그레이션  <br/> |수백 ~ 수천 개  <br/> |몇 개월 이상  <br/> |
   
다음 섹션에서는 이러한 방법의 개요를 제공 합니다. 자세한 내용은 [마이그레이션 경로 결정](https://support.office.com/article/Decide-on-a-migration-path-0d4f2396-9cef-43b8-9bd6-306d01df1e27)을 참조 하십시오. 
  
#### <a name="cutover-migration"></a>단독형 마이그레이션

마이그레이션에 따라 미리 선택한 날짜 및 시간에 모든 사서함, 메일 그룹, 연락처 등을 Microsoft 365로 마이그레이션합니다. 마이그레이션이 완료 된 후에는 온-프레미스 Exchange 서버를 종료 하 고 Microsoft 365만 사용 하 여 시작 합니다.
  
마이그레이션에 대 한 자세한 내용은 많은 사서함이 없는 소규모 조직에 게 적합 하며, Microsoft 365에 빠르게 액세스 하 고, 다른 방법의 복잡 한 일부를 처리 하지 않으려고 합니다. 그러나 주 단위로 완료 되어야 하며, 사용자가 Outlook 프로필을 다시 구성 해야 합니다. 마이그레이션 중에는 최대 2000 개의 사서함을 처리할 수 있지만,이를 사용 하는 것이 최고 150 사서함을 마이그레이션하는 것이 좋습니다. 더 많은 마이그레이션을 시도 하면 기한 전에 모든 사서함을 전송 하는 데 시간이 오래 걸릴 수 있으며 IT 지원 담당자가 Outlook을 다시 구성 하는 데 도움이 되는 요청을 많이 받을 수 있습니다.
  
마이그레이션에 대 한 자세한 내용은 다음 항목을 고려 하세요.
  
- Microsoft 365에서 Outlook Anywhere (TCP port 443)를 사용 하 여 Exchange 2007 서버에 연결 해야 합니다.
    
- 모든 온-프레미스 사서함이 Microsoft 365로 이동 됩니다.
    
- 사용자의 사서함에 대 한 읽기 권한이 있는 온-프레미스 관리자 계정이 필요 합니다.
    
- Microsoft 365에서 사용 하려는 Exchange 2007 허용 도메인은 서비스에서 확인 된 도메인으로 추가 해야 합니다.
    
- 마이그레이션을 시작 하는 시간과 완료 단계를 시작할 때 사이에 microsoft 365에서는 주기적으로 Microsoft 365 및 온-프레미스 사서함을 동기화 합니다. 이를 통해 온-프레미스 사서함에 남아 있는 전자 메일을 걱정 하지 않고 마이그레이션을 완료할 수 있습니다.
    
- 사용자는 Microsoft 365 계정에 대 한 새로운 임시 암호를 받게 됩니다. 사용자가 처음으로 자신의 사서함에 로그인 할 때 암호를 변경 해야 합니다.
    
- 마이그레이션하려는 각 사용자 사서함에 대해 Exchange Online을 포함 하는 Microsoft 365 라이선스가 필요 합니다.
    
- 사용자가 각 장치에서 새 Outlook 프로필을 설정 하 고 전자 메일을 다시 다운로드 해야 합니다. Outlook에서 다운로드 하는 전자 메일의 양은 다를 수 있습니다. 자세한 내용은 [오프 라인으로 유지할 메일 양 변경을](https://support.office.com/article/Change-how-much-mail-to-keep-offline-f3a1251c-6dd5-4208-aef9-7c8c9522d633?ui=en-US&amp;rs=en-US&amp;ad=US&amp;fromAR=1)참조 하십시오.
    
각 마이그레이션에 대 한 자세한 내용은 다음 항목을 참조 하십시오.
  
- [전자 메일 마이그레이션에 대해 알아야 할 사항](https://support.office.com/article/What-you-need-to-know-about-a-cutover-email-migration-to-Office-365-961978ef-f434-472d-a811-1801733869da)
    
- [전자 메일 마이그레이션 반복 수행](https://support.office.com/article/Perform-a-cutover-migration-of-email-to-Office-365-9496e93c-1e59-41a8-9bb3-6e8df0cd81b4)
    
#### <a name="staged-migration"></a>미리 구성된 마이그레이션

미리 구성 된 마이그레이션의 경우 Microsoft 365로 마이그레이션하려는 사서함이 몇 개 있거나, 마이그레이션을 완료 하기 위해 한 주 이상을 수행 해야 하며, 공유 약속 있음/없음 일정 정보와 같은 고급 하이브리드 마이그레이션 기능을 사용할 필요가 없습니다.
  
미리 구성 된 마이그레이션은 사서함을 Microsoft 365로 마이그레이션하는 데 더 많은 시간을 기울여야 하며 몇 주 내에 마이그레이션을 완료 하도록 계획 하는 조직에 매우 유용 합니다. 사서함을 일괄적으로 마이그레이션할 수 있습니다. 지정 된 시간에 마이그레이션되는 사서함의 수와 사용자를 제어할 수 있습니다. 예를 들어 동일한 부서의 사용자 사서함을 일괄 처리 하 여 모두 동시에 이동할 수 있습니다. 또는 마지막 일괄 처리까지 executive 사서함을 남길 수 있습니다. 기본적으로는 마이그레이션에 대 한 것 처럼 사용자가 Outlook 프로필을 다시 만들어야 합니다.
  
미리 구성 된 마이그레이션을 수행 하는 방법을 고려 하 고 있는 경우 다음 사항을 고려해 야 합니다.
  
- Microsoft 365에서는 Outlook Anywhere (TCP 포트 443)를 사용 하 여 Exchange 2007 서버에 연결 해야 합니다.
    
- 사용자의 사서함에 대 한 읽기 권한이 있는 온-프레미스 관리자 계정이 필요 합니다.
    
- Microsoft 365에서 사용 하려는 Exchange 2007 허용 도메인은 서비스에서 확인 된 도메인으로 추가 해야 합니다.
    
- 일괄적으로 마이그레이션할 각 사서함의 전체 이름과 전자 메일 주소를 사용 하 여 CSV 파일을 만들어야 합니다. 또한 마이그레이션하려는 각 사서함에 대 한 새 암호를 포함 하 고 각 사용자에 게 해당 암호를 전송 해야 합니다. 사용자가 새 Microsoft 365 사서함에 처음 로그인 할 때 암호를 변경 하 라는 메시지가 표시 됩니다.
    
- 마이그레이션 일괄 처리를 시작 하는 시간과 완료 단계를 시작할 때 사이에 Microsoft 365에서는 일괄 처리에 포함 된 Microsoft 365 및 온-프레미스 사서함을 주기적으로 동기화 합니다. 이를 통해 온-프레미스 사서함에 남아 있는 전자 메일을 걱정 하지 않고 마이그레이션을 완료할 수 있습니다.
    
- 마이그레이션하려는 각 사용자 사서함에 대해 Exchange Online을 포함 하는 Microsoft 365 라이선스가 필요 합니다.
    
- 사용자가 각 장치에서 새 Outlook 프로필을 설정 하 고 전자 메일을 다시 다운로드 해야 합니다. Outlook에서 다운로드 하는 전자 메일의 양은 다를 수 있습니다. 자세한 내용은 [오프 라인으로 유지할 메일 양 변경을](https://support.office.com/article/Change-how-much-mail-to-keep-offline-f3a1251c-6dd5-4208-aef9-7c8c9522d633?ui=en-US&amp;rs=en-US&amp;ad=US&amp;fromAR=1)참조 하십시오.
    
미리 구성 된 마이그레이션에 대 한 자세한 내용은 다음 항목을 참조 하십시오.
  
- [미리 구성 된 전자 메일 마이그레이션에 대해 알아야 할 사항](https://support.office.com/article/What-you-need-to-know-about-a-staged-email-migration-to-Office-365-7e2c82be-5f3d-4e36-bc6b-e5b4d411e207)
    
- [미리 구성 된 전자 메일 마이그레이션 수행](https://support.office.com/article/Perform-a-staged-migration-of-email-to-Office-365-83bc0b69-de47-4cc4-a57d-47e478e4894e)
    
#### <a name="full-hybrid"></a>전체 하이브리드

전체 하이브리드 마이그레이션에서는 조직에 수백, 수천 개까지 사서함이 포함 되어 있으며 이러한 항목 중 일부 또는 전체를 Microsoft 365로 이동 하려고 합니다. 이러한 마이그레이션은 일반적으로 더 길기 때문에 하이브리드 마이그레이션을 사용 하면 다음과 같은 작업을 수행할 수 있습니다.
  
- Microsoft 365의 사용자에 대 한 약속 있음/없음 일정 정보를 온-프레미스 사용자에 게 표시 하 고 그 반대의 경우도 마찬가지입니다.
    
- 온-프레미스와 Microsoft 365 둘 다에 받는 사람이 포함 된 통합 전체 주소 목록을 확인 합니다.
    
- 온-프레미스 인지 아니면 Microsoft 365에 있든 관계 없이 모든 사용자에 대 한 전체 Outlook 받는 사람 속성을 볼 수 있습니다.
    
- TLS 및 인증서를 사용 하 여 온-프레미스 Exchange 서버와 Microsoft 365 간의 전자 메일 통신을 보호 합니다.
    
- 온-프레미스 Exchange 서버와 Microsoft 365 간에 전송 되는 메시지를 내부로 취급 하 여 다음과 같은 기능을 사용할 수 있습니다.
    
  - 내부 메시지를 대상으로 하는 전송 및 준수 에이전트로 올바르게 평가 및 처리 해야 합니다.
    
  - 스팸 방지 필터를 무시 합니다.
    
전체 하이브리드 마이그레이션은 여러 달 이상의 하이브리드 구성에 유지 해야 하는 조직에 가장 적합 합니다. 온라인 사서함 이동을 사용 하 여이 섹션의 앞부분에 나열 된 기능을 비롯 하 여 디렉터리 동기화, 보다 나은 통합 준수 기능 및 Microsoft 365에서 사서함을 이동 하는 기능을 확인할 수 있습니다. Microsoft 365은 온-프레미스 조직의 확장이 됩니다.
  
전체 하이브리드 마이그레이션을 수행 하는 방법을 고려 하 고 있다면 다음 사항을 고려해 야 합니다.
  
- 전체 하이브리드 마이그레이션은 모든 유형의 조직에 적합 하지 않습니다. 전체 하이브리드 마이그레이션의 복잡도로 인해 사서함 수가 수백 개 미만인 조직은 일반적으로 작업을 설정 하는 데 필요한 노력과 비용을 정당화 하는 이점을 제공 하지 않습니다. 조직 처럼 생각 되는 경우 대신 직접 또는 미리 구성 된 마이그레이션을 고려 하는 것이 좋습니다.
    
- Exchange 2007 조직에 Exchange 2013 서버를 하나 이상 배포 하 여 "하이브리드 서버"로 작동 해야 합니다. 이 서버는 Exchange 2007 서버를 대신 하 여 Microsoft 365와 통신 합니다.
    
- Microsoft 365에서는 TCP 포트 443을 통해 외부에서 Outlook 사용을 통해 "hybrid server"에 연결 해야 합니다.
    
- 온-프레미스 Active Directory 서버와 Microsoft 365 간에 Azure Active Directory (Azure AD) 연결을 사용 하 여 디렉터리 동기화를 설정 해야 합니다.
    
- 사용자가 로컬 네트워크에 로그인 할 때와 동일한 사용자 이름 및 암호를 사용 하 여 Microsoft 365 사서함에 로그인 할 수 있습니다. 이 기능을 사용 하려면 암호 동기화 및/또는 adfs (Active Directory Federation Services)와 함께 Azure AD Connect가 필요 합니다.
    
- 마이그레이션하려는 각 사용자 사서함에 대해 Exchange Online을 포함 하는 Microsoft 365 라이선스가 필요 합니다.
    
- 사용자가 대부분의 장치에서 새 Outlook 프로필을 설정할 필요는 없지만 일부 구형 Android 휴대폰에는 새 프로필이 필요할 수도 있습니다. 사용자가 자신의 전자 메일을 redownload 필요가 없습니다.
    
전체 하이브리드 마이그레이션이 적합 한 경우 마이그레이션에 도움이 되는 다음 리소스를 참조 하세요.
  
- [Exchange 배포 도우미](https://aka.ms/exdeploy)
    
- [Exchange Server 하이브리드 배포](https://technet.microsoft.com/library/jj200581%28v=exchg.150%29.aspx)
    
- [하이브리드 구성 마법사](https://technet.microsoft.com/library/hh529921%28v=exchg.150%29.aspx)
    
- [하이브리드 구성 마법사 FAQ](https://technet.microsoft.com/library/mt488940%28v=exchg.150%29.aspx)
    
- [하이브리드 배포 필수 구성 요소](https://technet.microsoft.com/library/hh534377%28v=exchg.150%29.aspx)
    
### <a name="migrate-to-a-newer-version-of-exchange-server"></a>새 버전의 Exchange Server로 마이그레이션

Microsoft 365로 마이그레이션하는 것이 최상의 가치와 사용자 환경을 달성할 수 있다는 것을 강력히 확신 합니다. 그러나 일부 조직에서는 전자 메일을 온-프레미스로 유지 해야 한다는 점을 이해 하 고 있습니다. 이는 데이터를 다른 국가에 저장 하지 않을 것 이므로 규정 요구 사항에 의해 발생 하는 것이 원인일 수 있습니다. 전자 메일을 온-프레미스에 유지 하도록 선택 하는 경우 Exchange 2007 환경을 Exchange 2010, Exchange 2013 또는 Exchange 2016로 마이그레이션할 수 있습니다.
  
Microsoft 365로 마이그레이션할 수 없는 경우 Exchange 2016로 마이그레이션하는 것이 좋습니다. Exchange 2016에는 이전 Exchange 버전의 모든 기능이 포함 되어 있습니다. 또한 일부 기능은 Microsoft 365 에서만 사용할 수 있지만 Microsoft 365에서 제공 되는 환경과 가장 유사 합니다. 누락 된 항목을 몇 개만 확인 하세요.
  
|**Exchange 릴리스**|**기능**|
|:-----|:-----|
|Exchange 2010  <br/> | Role-Based 액세스 제어 (Acl 없는 사용 권한)  <br/>  Outlook Web App 사서함 정책  <br/>  약속 있음/없음 공유 및 조직 간 일정 위임 기능  <br/> |
|Exchange 2013  <br/> | *Exchange 2010의 기능 및 ...*  <br/>  서버 역할 수를 3 개 (사서함, 클라이언트 액세스, Edge 전송)로 줄이는 단순화 된 아키텍처  <br/>  중요 한 정보의 누출을 방지 하는 데 도움이 되는 DLP (데이터 손실 방지 정책)  <br/>  향상 된 Outlook Web App 환경  <br/> |
|Exchange 2016  <br/> | *Exchange 2013의 기능 및 ...*  <br/>  사서함 및 Edge 전송에만 해당 하는 보다 간단한 서버 역할  <br/>  SharePoint와의 통합과 함께 DLP 개선  <br/>  향상 된 데이터베이스 복구 기능  <br/>  온라인 문서 공동 작업 |
   
#### <a name="which-version-should-i-migrate-to"></a>어떤 버전을 마이그레이션해야 하나요?

처음에는 Exchange 2016로 마이그레이션될 것으로 가정 하는 것이 좋습니다. 그런 후 다음 정보를 사용 하 여 가정을 확인 하거나 Exchange 2016를 규칙으로 처리 합니다. 몇 가지 이유로 인해 Exchange 2016로 마이그레이션할 수 없는 경우 Exchange 2013와 동일한 프로세스를 수행 합니다.
  
|**고려 사항**|**추가 정보**|
|:-----|:-----|
|지원 날짜 종료  <br/> | Exchange 2007와 마찬가지로 각 Exchange 버전의 지원 종료 날짜는 다음과 같습니다.  <br/> *Exchange 2010* -2020 년 1 월  <br/> *Exchange 2013* -2023 년 4 월  <br/> *Exchange 2016* -2025 년 10 월  <br/>  이전에는 지원 끝에서 다른 마이그레이션을 수행 하는 데 필요한 더 빠른 방법을 설명 합니다.<br/> |
|Exchange 2010 및 2013의 마이그레이션 경로입니다.  <br/> |Exchange 2010 또는 Exchange 2013로 마이그레이션하는 일반적인 단계는 다음과 같습니다.  <br/> -Exchange 2010 또는 2013을 기존 Exchange 2007 조 직에 설치 합니다. <br/>-Exchange 2010 또는 2013로 서비스 및 기타 인프라를 이동 합니다.<br/>-사서함 및 공용 폴더를 Exchange 2010 또는 2013로 이동 합니다.<br/>-남은 Exchange 2007 서버를 해제 합니다. |
|Exchange 2016의 마이그레이션 경로  <br/> |Exchange 2016로 마이그레이션하는 일반적인 단계는 다음과 같습니다.  <br/> -Exchange 2013을 기존 Exchange 2007 조직에 설치 합니다.<br/>-Exchange 2013로 서비스 및 기타 인프라를 이동 합니다.<br/>-사서함과 공용 폴더를 Exchange 2013으로 이동 합니다.<br/>-남은 Exchange 2007 서버를 해제 합니다.<br/>-Exchange 2016을 기존 Exchange 2013 조직에 설치 합니다.<br/>-사서함, 공용 폴더, 서비스 및 기타 인프라를 Exchange 2016으로 이동 합니다 (순서와 관계 없음). 나머지 Exchange 2013 서버를 해제 합니다.<br/><br/> **참고:** Exchange 2013에서 Exchange 2016로 마이그레이션하는 것은 간단 합니다. 두 버전에는 거의 동일한 하드웨어 요구 사항이 적용 되며, 이러한 버전은 매우 호환성이 있습니다. 따라서 Exchange 2013에 대해 구매한 서버를 다시 작성 하 고 Exchange 2016를 설치할 수 있습니다. 온라인 사서함 이동의 경우 대부분의 사용자는 사서함이 서버에서 이동 된 것을 확인 한 후 Exchange 2016를 사용 하 여 다시 작성 한 후에 야 합니다.           |
|버전 동시 사용  <br/> | 로 마이그레이션하는 경우 ...  <br/> **Exchange 2016:** Exchange 2007 서버를 포함 하는 조직에는 exchange 2016을 설치할 수 없습니다. 먼저 Exchange 2010 또는 2013 (Exchange 2013 권장)로 마이그레이션을 수행 하 고 모든 Exchange 2007 server를 제거한 다음 Exchange 2016로 마이그레이션해야 합니다.  <br/> **Exchange 2010 또는 exchange 2013:** Exchange 2010 또는 Exchange 2013를 기존 Exchange 2007 조 직에 설치할 수 있습니다. 이를 통해 하나 이상의 Exchange 2010 또는 2013 서버를 설치 하 고 마이그레이션을 수행할 수 있습니다.  <br/> |
|서버 하드웨어  <br/> | 서버 하드웨어 요구 사항이 Exchange 2007에서 변경 되었습니다. 하드웨어가 호환 되는지 확인 합니다. 자세한 내용은 다음을 참조하세요.  <br/> [Exchange 2016 시스템 요구 사항](https://technet.microsoft.com/library/aa996719%28v=exchg.160%29.aspx) <br/> [Exchange 2013 시스템 요구 사항](https://technet.microsoft.com/library/aa996719%28v=exchg.150%29.aspx) <br/> [Exchange 2010 시스템 요구 사항](https://technet.microsoft.com/library/aa996719%28v=exchg.141%29.aspx) <br/>  Exchange 성능이 크게 개선 되 고 컴퓨팅 파워 및 저장소 공간이 신형 서버에 제공 된다는 것은 동일한 수의 사서함을 지원 하기 위한 서버 수가 더 적기 때문입니다.  <br/> |
|운영 체제 버전  <br/> | 각 버전에 대해 지원 되는 최소 운영 체제 버전은 다음과 같습니다.  <br/> **Exchange 2016** -Windows Server 2012  <br/> **Exchange 2013** -Windows Server 2008 R2 SP1  <br/> **Exchange 2010** -Windows SERVER 2008 SP2  <br/>  [Exchange 지원 가능성 매트릭스](https://technet.microsoft.com/library/ff728623%28v=exchg.150%29.aspx)에서 운영 체제를 지 원하는 방법에 대 한 자세한 정보를 확인 하세요.  <br/> |
|Active Directory 포리스트 기능 수준  <br/> | 각 버전에 대해 지원 되는 최소 Active Directory 포리스트 기능 수준은 다음과 같습니다.  <br/> **Exchange 2016** Windows Server 2008 R2 SP1  <br/> **Exchange 2013** Windows Server 2003  <br/> **Exchange 2010** Windows Server 2003  <br/>  [Exchange 지원 가능성 매트릭스](https://technet.microsoft.com/library/ff728623%28v=exchg.150%29.aspx)에서 포리스트 기능 수준 지원에 대 한 자세한 정보를 확인 하세요.  <br/> |
|Office 클라이언트 버전  <br/> | 각 버전에 대해 지원 되는 최소 Office 클라이언트 버전은 다음과 같습니다.  <br/> **Exchange 2016** -Office 2010 (최신 업데이트 포함)  <br/> **Exchange 2013** -OFFICE 2007 SP3  <br/> **Exchange 2010** -Office 2003  <br/>  Office 클라이언트 지원에 대 한 자세한 내용은 [Exchange 지원 가능성 매트릭스](https://technet.microsoft.com/library/ff728623%28v=exchg.150%29.aspx)를 확인 하세요.  <br/> |
   
#### <a name="how-do-i-migrate"></a>마이그레이션하는 방법

전자 메일을 온-프레미스에 유지 하도록 결정 한 경우 다음 리소스를 사용 하 여 마이그레이션에 도움을 받을 수 있습니다.
  
- [Exchange 배포 도우미](https://aka.ms/exdeploy)
    
- Exchange [2016](https://technet.microsoft.com/library/bb738144%28v=exchg.160%29.aspx), [2013](https://technet.microsoft.com/library/bb738144%28v=exchg.150%29.aspx), [2010](https://www.microsoft.com/download/en/details.aspx?displaylang=en&amp;id=5401) 에 대 한 Active Directory 스키마 변경 사항
    
- Exchange [2016](https://technet.microsoft.com/library/aa996719%28v=exchg.160%29.aspx), [2013](https://technet.microsoft.com/library/aa996719%28v=exchg.150%29.aspx), [2010](https://technet.microsoft.com/library/aa996719%28v=exchg.141%29.aspx) 에 대 한 시스템 요구 사항
    
- Exchange [2016](https://technet.microsoft.com/library/bb691354%28v=exchg.160%29.aspx), [2013](https://technet.microsoft.com/library/bb691354%28v=exchg.150%29.aspx), [2010](https://technet.microsoft.com/library/bb691354%28v=exchg.141%29.aspx) 의 필수 구성 요소
    
## <a name="get-help"></a>도움말 보기

Microsoft 365로 마이그레이션하는 경우 Microsoft FastTrack 서비스를 사용할 수 있는 자격이 있을 수 있습니다. FastTrack은 최상의 방법, 도구 및 리소스를 제공 하 여 Microsoft 365로 마이그레이션을 최대한 원활 하 게 진행 합니다. 무엇 보다도, 지원 엔지니어가 마이그레이션 진행 과정을 통해 마지막 사서함 마이그레이션에 대 한 모든 계획 및 디자인을 안내 합니다. FastTrack에 대 한 자세한 내용은 [Microsoft FastTrack](https://fasttrack.microsoft.com/)를 참조 하십시오.
  
Microsoft 365로 마이그레이션하는 동안 문제가 발생 하 여 FastTrack를 사용 하지 않는 경우 또는 최신 버전의 Exchange Server로 마이그레이션하는 경우에는 다음 작업을 수행 하는 데 도움이 됩니다. 사용할 수 있는 몇 가지 리소스는 다음과 같습니다.
  
- [기술 커뮤니티](https://social.technet.microsoft.com/Forums/office/home?category=exchangeserver)
    
- [고객 지원](https://support.microsoft.com/gp/support-options-for-business)
    
## <a name="related-topics"></a>관련 항목

[Office 2007 서버 및 클라이언트를 업그레이드 하는 데 도움이 되는 리소스](upgrade-from-office-2007-servers-and-products.md)
