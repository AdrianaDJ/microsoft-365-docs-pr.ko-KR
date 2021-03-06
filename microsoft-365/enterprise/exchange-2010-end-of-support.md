---
title: Exchange 2010 지원 종료 로드맵
ms.author: dstrome
author: dstrome
manager: laurawi
audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
ms.assetid: e150e7b9-c432-4c8d-a0ae-c11847129a7d
f1.keywords:
- NOCSH
description: Exchange 2010이 지원 종료에 도달 했습니다. 이 계획 로드맵을 사용 하 여 Exchange Online으로 또는 최신 버전의 Exchange Server 온-프레미스로 업그레이드할 준비를 할 수 있습니다.
ms.openlocfilehash: 23384d93c4e65fb25a66ca6f2f0bcbe46b34ee18
ms.sourcegitcommit: d3ca8021f7da00a474ac14aac5f1358204a848f2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/01/2020
ms.locfileid: "49519694"
---
# <a name="exchange-2010-end-of-support-roadmap"></a>Exchange 2010 지원 종료 로드맵

*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*

Exchange Server 2010는 **2020 년 10 월 13 일** 에 지원 종료에 도달 했습니다. 아직 Exchange 2010에서 Microsoft 365, Office 365 또는 Exchange 2016로 마이그레이션을 시작한 적이 없는 경우 이제 계획을 시작 하는 데 걸리는 시간입니다.

## <a name="what-does-end-of-support-mean"></a>*지원이 끝나는* 것은 무엇을 의미 하나요?

대부분의 Microsoft 제품은 새로운 기능, 버그 수정, 보안 픽스 등이 제공 되는 지원 주기를 제공 합니다. 이 수명 주기는 일반적으로 제품 초기 릴리스에서 10 년 동안 지속 됩니다. 이 수명 주기의 끝은 제품의 지원 종료 라고 합니다. Exchange 2010는 2020 년 10 월 13 일에 지원 종료에 도달 하 여 더 이상 다음을 제공 하지 않습니다.

- 발생할 수 있는 문제에 대 한 기술 지원
- 서버의 안정성 및 유용성에 영향을 줄 수 있는 문제에 대 한 버그 수정
- 보안 침해에 취약 한 서버를 만들 수 있는 취약성에 대 한 보안 수정
- 표준 시간대 업데이트

이 날짜 후에도 Exchange 2010 설치가 계속 실행 됩니다. 그러나 위에 나열 된 변경 사항으로 인해 가능한 한 빨리 Exchange 2010에서 마이그레이션하는 것이 좋습니다.

지원 종료에 대 한 자세한 내용은 [Office 2010 서버 및 클라이언트에서 업그레이드 하는 데 도움이](upgrade-from-office-2010-servers-and-products.md)되는 리소스를 참조 하세요.

## <a name="what-are-my-options"></a>내 옵션 이란?

옵션을 살펴보고 마이그레이션 계획을 준비 하는 데는 상당한 시간이 걸립니다. 다음을 수행할 수 있습니다.

- Microsoft 365로 완벽 하 게 마이그레이션합니다. 간단한 통과, 최소 하이브리드 또는 전체 하이브리드 마이그레이션을 사용 하 여 사서함을 마이그레이션합니다. 그런 다음 온-프레미스 Exchange 서버와 Active Directory를 제거 합니다.
- 온-프레미스 서버에서 exchange 2010 서버를 Exchange 2016로 마이그레이션합니다.

> [!IMPORTANT]
> 조직에서 사서함을 Microsoft 365로 마이그레이션하는 경우, 온-프레미스 Active Directory에서 사용자 계정을 계속 관리 하기 위해 DirSync 또는 Azure AD Connect를 유지 하도록 선택 하는 경우에는 하나 이상의 Microsoft Exchange server 온-프레미스를 유지 해야 합니다. 모든 Exchange 서버를 제거 하는 경우에는 온-프레미스 Active Directory에 기관의 원본이 남아 있으므로 exchange Online의 Exchange 받는 사람을 변경할 수 없습니다. 변경 내용을 적용 해야 합니다. 이 시나리오에서는 다음과 같은 옵션을 사용할 수 있습니다.
>
>- *권장 사항:* 사서함을 Microsoft 365로 마이그레이션하고 2020 업그레이드 한 경우 Exchange 2010을 사용 하 여 Microsoft 365에 연결 하 고 사서함을 마이그레이션합니다. 다음으로, exchange 2016를 exchange 2010로 마이그레이션하고 나머지 Exchange 2010 서버는 해제 합니다.
>- 2020 년 10 월 13 일에 사서함 마이그레이션 및 온-프레미스 서버 업그레이드를 완료 하지 않은 경우 온-프레미스 Exchange 2010 서버를 먼저 Exchange 2016로 업그레이드 합니다. 그런 다음 Exchange 2016을 사용 하 여 Microsoft 365에 연결 하 고 사서함을 마이그레이션합니다.

> [!NOTE]
> 다소 복잡 하지만 온-프레미스 Exchange 2010 서버를 Exchange 2016로 마이그레이션하는 동안 사서함을 Microsoft 365로 마이그레이션할 수도 있습니다.

다음은 Exchange Server 2010에 대 한 지원 종료를 방지 하기 위해 수행할 수 있는 세 가지 경로입니다.

![Exchange Server 2010 업그레이드 경로](../media/exchange-2010-end-of-support/exchange-2010-end-of-support-options.png)

다음 섹션에서는 각 옵션에 대해 자세히 알아봅니다.

## <a name="migrate-to-microsoft-365"></a>Microsoft 365로 마이그레이션

Exchange 2010 배포를 중지 하는 데 도움이 되는 가장 간단 하 고 간단한 옵션은 전자 메일을 Microsoft 365로 마이그레이션하는 것입니다. Microsoft 365로 마이그레이션하는 경우 이전 기술과에서 다음과 같은 단일 홉을 현재 기능으로 만들 수 있습니다.

- 보존 정책, In-Place 및 소송 보류, 원본 위치 eDiscovery 등의 규정 준수 기능
- Microsoft Teams.
- Power BI
- 중요 받은 편지함
- MyAnalytics.

Microsoft 365에는 새 기능을 먼저 제공 하므로 조직에서 바로 사용을 시작할 수 있습니다. 또한 다음 사항을 걱정 하지 않아도 됩니다.

- 하드웨어 구입 및 유지 관리
- 서버에 대 한 지불 및 냉각
- 보안, 제품 및 시간대 수정 사항에 대해 최신 상태를 유지 합니다.
- 준수 요구 사항을 지원 하기 위해 저장소 및 소프트웨어 유지 관리
- 새 버전의 Exchange로 업그레이드 하는 경우 Microsoft 365에서 항상 최신 버전의 Exchange를 사용할 수 있습니다.

### <a name="how-should-i-migrate-to-microsoft-365"></a>Microsoft 365로 마이그레이션하려면 어떻게 해야 하나요?

조직에 따라 Microsoft 365에 대 한 몇 가지 옵션을 사용할 수 있습니다. 먼저 다음과 같은 몇 가지 사항을 고려해 야 합니다.
- 이동 해야 하는 좌석 또는 사서함의 수입니다.
- 마이그레이션을 마지막으로 수행할 시간입니다.
- 마이그레이션 중에 온-프레미스 설치와 Microsoft 365 간에 원활한 통합이 필요한 지 여부
 
이 표에서는 마이그레이션 옵션 및 사용할 방법을 결정 하는 가장 중요 한 요소를 보여 줍니다.

|마이그레이션 옵션|조직 크기|기간|
|---|---|---|
|단독형 마이그레이션|좌석 150 개 미만|1 주 이내|
|최소 하이브리드 마이그레이션|좌석 150 개 미만|몇 주 이내 또는 그 밖의 경우|
|전체 하이브리드 마이그레이션|150 개 이상|몇 주 이상|

다음 섹션에서는 이러한 방법의 개요를 제공 합니다. 자세한 내용은 [마이그레이션 경로 결정](https://support.office.com/article/Decide-on-a-migration-path-0d4f2396-9cef-43b8-9bd6-306d01df1e27)을 참조 하세요.

### <a name="cutover-migration"></a>단독형 마이그레이션

마이그레이션 후에는 모든 사서함, 메일 그룹, 연락처 등을 설정 된 날짜 및 시간에 Office 365로 마이그레이션합니다. 작업이 완료 되 면 온-프레미스 Exchange 서버를 종료 하 고 Microsoft 365만 사용을 시작 합니다.

마이그레이션에 대 한 자세한 내용은 많은 사서함이 없는 소규모 조직에 게 적합 하며, Microsoft 365에 빠르게 액세스 하 고, 다른 방법의 복잡성을 처리 하지 않으려고 합니다. 하지만 1 주 이내에 완료 되어야 합니다. 사용자가 자신의 Outlook 프로필을 다시 구성 해야 합니다. 마이그레이션 중에는 150 최대 2000 개의 사서함을 마이그레이션할 수 있지만이를 사용 하는 것이 가장 좋습니다. 더 많은 마이그레이션을 시도 하면 기한 전에 모든 사서함을 전송 하는 데 시간이 오래 걸릴 수 있으며 IT 지원 담당자가 Outlook을 다시 구성 하는 데 도움이 되는 요청을 많이 받을 수 있습니다.

다음은 마이그레이션에 대해 고려해 야 할 사항입니다.

- Microsoft 365에서는 Outlook Anywhere (TCP 포트 443)를 사용 하 여 Exchange 2010 서버에 연결 해야 합니다.
- 모든 온-프레미스 사서함이 Microsoft 365로 이동 됩니다.
- 사용자의 사서함에 대 한 읽기 권한이 있는 온-프레미스 관리자 계정이 필요 합니다.
- Microsoft 365에서 사용 하려는 Exchange 2010 허용 도메인은 서비스에서 확인 된 도메인으로 추가 해야 합니다.
- 마이그레이션을 시작 하 고 완료 단계를 시작할 때 사이에 microsoft 365에서는 주기적으로 Microsoft 365 및 온-프레미스 사서함을 동기화 합니다. 이를 통해 온-프레미스 사서함에 남아 있는 전자 메일을 걱정 하지 않고 마이그레이션을 완료할 수 있습니다.
- 사용자에 게 Microsoft 365 계정에 대 한 새로운 임시 암호가 수신 됩니다. 사용자가 처음으로 자신의 사서함에 로그인 할 때이를 변경 해야 합니다.
- 마이그레이션하려는 각 사용자 사서함에 대해 Exchange Online을 포함 하는 Microsoft 365 라이선스가 필요 합니다.
- 사용자가 각 장치에서 새 Outlook 프로필을 설정 하 고 전자 메일을 다시 다운로드 해야 합니다. Outlook에서 다운로드 하는 전자 메일의 양은 다를 수 있습니다. 자세한 내용은 [Outlook에서 오프 라인으로 작업](https://support.microsoft.com/office/f3a1251c-6dd5-4208-aef9-7c8c9522d633)을 참조 하세요.

각 마이그레이션에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [전자 메일 마이그레이션에 대해 알아야 할 사항](https://docs.microsoft.com/Exchange/mailbox-migration/what-to-know-about-a-cutover-migration)
- [Office 365에 전자 메일을 간편 하 게 마이그레이션 수행](https://docs.microsoft.com/Exchange/mailbox-migration/cutover-migration-to-office-365)

### <a name="minimal-hybrid-migration"></a>최소 하이브리드 마이그레이션

최소 하이브리드 또는 express 마이그레이션에서는 몇 주 내에 수백 개의 사서함을 Microsoft 365으로 이동 합니다. 이 방법은 공유 약속 있음/없음 일정 정보와 같은 고급 하이브리드 마이그레이션 기능을 지원 하지 않습니다.

최소 하이브리드 마이그레이션은 사서함을 Microsoft 365로 마이그레이션하는 데 더 많은 시간을 기울여야 하지만 몇 주 이내에 마이그레이션을 완료 하기 위한 계획을 수립 해야 하는 조직에서 매우 유용 합니다. 복잡 한 경우가 많지 않고 고급 *전체 하이브리드 마이그레이션의* 몇 가지 이점을 얻을 수 있습니다. 지정 된 시간에 마이그레이션할 사서함의 수 및 개수를 제어할 수 있습니다. Microsoft 365 사서함은 온-프레미스 계정의 사용자 이름과 암호를 사용 하 여 만들어집니다. 또한 마이그레이션에 포함 된 것과 달리 사용자는 Outlook 프로필을 다시 만들 필요가 없습니다.

최소한의 하이브리드 마이그레이션에 대해서는 다음 사항을 고려해 야 합니다.

- 온-프레미스 Active Directory 서버와 Microsoft 365 간에 일회성 디렉터리 동기화를 수행 해야 합니다.
- 사용자는 사서함 앞에 있는 것과 동일한 사용자 이름 및 암호를 사용 하 여 Microsoft 365 사서함에 로그인 할 수 있습니다.
- 마이그레이션하려는 각 사용자 사서함에 대해 Exchange Online을 포함 하는 Microsoft 365 라이선스가 필요 합니다.
- 사용자가 대부분의 장치에서 새 Outlook 프로필을 설정할 필요는 없지만 일부 이전 Android 휴대폰에는 새 프로필이 필요할 수도 있습니다. 사용자는 자신의 전자 메일을 redownload 필요가 없습니다.

자세한 내용은 [최소 하이브리드를 사용 하 여 Exchange 사서함을 Office 365로 빠르게 마이그레이션을](https://docs.microsoft.com/Exchange/mailbox-migration/use-minimal-hybrid-to-quickly-migrate)참조 하세요.

### <a name="full-hybrid"></a>전체 하이브리드

전체 하이브리드 마이그레이션에서 수백, 수천 개의 사서함을 보유 하 고 있으며 일부 또는 전체를 Microsoft 365로 이동 하는 경우 이러한 마이그레이션은 일반적으로 더 길기 때문에 하이브리드 마이그레이션을 사용 하면 다음과 같은 작업을 수행할 수 있습니다.

- Microsoft 365의 사용자에 대 한 약속 있음/없음 일정 정보를 온-프레미스 사용자에 게 표시 하 고 그 반대의 경우도 마찬가지입니다.
- 온-프레미스와 Microsoft 365 둘 다에 받는 사람이 포함 된 통합 전체 주소 목록을 확인 합니다.
- 온-프레미스 인지 아니면 Microsoft 365에 있든 관계 없이 모든 사용자에 대 한 전체 Outlook 받는 사람 속성을 볼 수 있습니다.
- TLS 및 인증서를 사용 하 여 온-프레미스 Exchange 서버와 Office 365 간의 전자 메일 통신을 보호 합니다.
- 온-프레미스 Exchange 서버와 Microsoft 365 간에 전송 되는 메시지를 내부로 취급 하 여 다음과 같은 기능을 사용할 수 있습니다.
  - 내부 메시지를 대상으로 하는 전송 및 준수 에이전트로 올바르게 평가 및 처리 해야 합니다.
  - 스팸 방지 필터를 무시 합니다.

전체 하이브리드 마이그레이션은 여러 달 이상의 하이브리드 구성에 유지 해야 하는 조직에 가장 적합 합니다. 이 섹션의 앞부분에 나와 있는 기능과 디렉터리 동기화, 향상 된 통합 준수 기능 및 온라인 사서함 이동을 사용 하 여 Microsoft 365에서 사서함을 이동 하는 기능을 확인할 수 있습니다. Microsoft 365은 온-프레미스 조직의 확장이 됩니다.

전체 하이브리드 마이그레이션에 대해 고려해 야 할 사항:

- 모든 조직에 적합 하지 않습니다. 전체 하이브리드 마이그레이션의 복잡도로 인해 사서함 수가 수백 개 미만인 조직은 일반적으로 작업량 및 비용을 정당화 한 이점을 볼 수 있습니다. 이러한 경우에는 대신 단위 또는 최소 하이브리드 마이그레이션을 수행 하는 것이 좋습니다.
- 온-프레미스 Active Directory 서버와 Microsoft 365 간에 Azure Active Directory (Azure AD) 연결을 사용 하 여 디렉터리 동기화를 설정 해야 합니다.
- 사용자가 로컬 네트워크에 로그인 할 때 사용 하는 것과 동일한 사용자 이름 및 암호를 사용 하 여 Microsoft 365 사서함에 로그인 할 수 있습니다. (이 기능을 사용 하려면 암호 동기화 및/또는 adfs (Active Directory Federation Services)와 함께 Azure AD Connect가 필요 합니다.
- 마이그레이션하려는 각 사용자 사서함에 대해 Exchange Online을 포함 하는 Microsoft 365 라이선스가 필요 합니다.
- 사용자가 대부분의 장치에서 새 Outlook 프로필을 설정할 필요는 없지만 일부 구형 Android 휴대폰에는 새 프로필이 필요할 수도 있습니다. 사용자는 자신의 전자 메일을 redownload 필요가 없습니다.

> [!IMPORTANT]
> 조직에서 사서함을 Microsoft 365로 마이그레이션하는 경우, 온-프레미스 Active Directory에서 사용자 계정을 계속 관리 하기 위해 DirSync 또는 Azure AD Connect를 유지 하도록 선택 하는 경우에는 하나 이상의 Exchange 서버를 온-프레미스로 유지 해야 합니다. 모든 Exchange 서버가 제거 되 면 exchange Online에서 Exchange 받는 사람을 변경할 수 없게 됩니다. 이는 기관 원본이 온-프레미스 Active Directory에 남아 있으며 변경 해야 하기 때문입니다.

전체 하이브리드 마이그레이션이 적절 하 게 재생 되는 경우 다음과 같은 유용한 리소스를 참조 하세요.

- [Exchange 배포 도우미](https://aka.ms/exdeploy)
- [Exchange Server 하이브리드 배포](https://docs.microsoft.com/exchange/exchange-hybrid)
- [하이브리드 구성 마법사](https://docs.microsoft.com/exchange/hybrid-configuration-wizard)
- [하이브리드 구성 마법사 FAQ](https://docs.microsoft.com/exchange/hybrid-configuration-wizard-faqs)
- [하이브리드 배포 필수 구성 요소](https://docs.microsoft.com/exchange/hybrid-deployment-prerequisites)

## <a name="upgrade-to-a-newer-version-of-exchange-server-on-premises"></a>새 버전의 Exchange Server 온-프레미스로 업그레이드

Microsoft 365로 마이그레이션을 완료 하 여 최상의 가치와 사용자 환경을 얻을 것으로 확신 합니다. 그러나 일부 조직에서는 일부 Exchange 서버를 온-프레미스로 유지 해야 합니다. 이는 규정 요구 사항, 즉 클라우드에서 충족할 수 없는 고유한 설정이 나 요구 사항이 있거나, 아직 Active Directory 온-프레미스를 사용 하기 때문에 Exchange에서 클라우드 사서함을 관리 해야 하는 경우에 데이터를 외부 데이터 센터에 저장 하지 않도록 하기 위한 것입니다. 어떤 경우 든 Exchange 온-프레미스를 사용 하는 경우 exchange 2010 환경이 Exchange 2013 또는 Exchange 2016 이상으로 업그레이드 되었는지 확인 해야 합니다.

최상의 환경을 위해 남은 온-프레미스 환경을 Exchange 2016으로 업그레이드 하는 것이 좋습니다. Exchange server 2010에서 Exchange Server 2016로 바로 이동 하려면 Exchange Server 2013을 설치 하지 않아도 됩니다.

Exchange 2016에는 이전 Exchange 버전의 모든 기능이 포함 되어 있습니다. 이러한 기능은 microsoft 365 에서만 사용할 수 있지만 Microsoft 365에서 사용 가능한 환경에 가장 근접 하 게 일치 합니다. 누락 된 항목을 몇 개만 확인 하세요.

|Exchange 릴리스|기능|
|---|---|
|**Exchange 2013**|아키텍처를 단순화 하 여 서버 역할의 수를 3 개 (사서함, 클라이언트 액세스, Edge 전송)로 줄입니다.|
||중요 한 정보의 누출을 방지 하는 데 도움이 되는 DLP (데이터 손실 방지 정책)|
||향상 된 Outlook Web App 환경|
|**Exchange 2016**|*Exchange 2013의 기능 및 ...*|
||사서함 및 Edge 전송에만 해당 하는 보다 간단한 서버 역할|
||SharePoint와의 통합과 함께 DLP 개선|
||향상 된 데이터베이스 복구 기능|
||온라인 문서 공동 작업|

|고려 사항|추가 정보|
|---|---|
|지원 날짜 종료|Exchange 2010와 마찬가지로 각 Exchange 버전의 지원 종료 날짜는 다음과 같습니다.<br/><br/>Exchange 2013-2023 년 4 월<br/>Exchange 2016-2025 년 10 월<br/><br/>이전에는 지원 종료 날짜 보다 더 빨리 다른 마이그레이션을 수행 해야 합니다. 4 월 2023은 생각 보다 훨씬 더 가깝습니다.|
|Exchange 2013 또는 2016의 마이그레이션 경로|Exchange 2013 또는 Exchange 2016을 선택할 때 Exchange 2010에서 새 버전으로의 마이그레이션 경로는 동일 합니다.<br/><br/>기존 Exchange 2010 조직에 Exchange 2013 또는 2016을 설치 합니다.<br/>Exchange 2013 또는 2016로 서비스 및 기타 인프라를 이동 합니다.<br/>사서함 및 공용 폴더를 Exchange 2013 또는 2016 서비스 해제 나머지 Exchange 2010 서버로 이동 합니다.|
|버전 동시 사용|Exchange 2013 또는 Exchange 2016로 마이그레이션할 때 기존 Exchange 2010 조직에 두 버전을 모두 설치할 수 있습니다. 이를 통해 하나 이상의 Exchange 2013 또는 Exchange 2016 서버를 설치 하 고 마이그레이션을 수행할 수 있습니다.|
|서버 하드웨어|서버 하드웨어 요구 사항이 Exchange 2010에서 변경 되었습니다. 하드웨어가 호환 되는지 확인 합니다. 각 버전의 하드웨어 요구 사항에 대 한 자세한 내용은 여기를 참조 하세요.<br/><br/>[Exchange 2016 시스템 요구 사항](https://docs.microsoft.com/Exchange/plan-and-deploy/system-requirements?view=exchserver-2016)<br/>[Exchange 2013 시스템 요구 사항](https://docs.microsoft.com/Exchange/exchange-2013-system-requirements-exchange-2013-help)<br/><br/>Exchange 성능이 크게 개선 되 고 최신 서버에서 컴퓨팅 파워 및 저장 용량이 증가 함에 따라서 동일한 사서함 수를 지원 하기 위한 서버 수가 더 적습니다.|
|운영 체제 버전|각 버전에 대해 지원 되는 최소 운영 체제 버전은 다음과 같습니다.<br/><br/>Exchange 2016-Windows Server 2012<br/>Exchange 2013-Windows Server 2008 R2 SP1<br/><br/>운영 체제 지원에 대 한 자세한 내용은 [Exchange 지원 가능성 매트릭스](https://docs.microsoft.com/exchange/plan-and-deploy/supportability-matrix)를 확인할 수 있습니다.|
|Active Directory 포리스트 기능 수준|각 버전에 대해 지원 되는 최소 Active Directory 포리스트 기능 수준은 다음과 같습니다.<br/><br/>Exchange 2016-Windows Server 2008 R2 SP1<br/>Exchange 2013-Windows Server 2003<br/><br/>[Exchange 지원 가능성 매트릭스](https://docs.microsoft.com/exchange/plan-and-deploy/supportability-matrix)에서 포리스트 기능 수준 지원에 대 한 자세한 정보를 확인할 수 있습니다.|
|Office 클라이언트 버전|각 버전에 대해 지원 되는 최소 Office 클라이언트 버전은 다음과 같습니다.<br/><br/>Exchange 2016-Office 2010 (최신 업데이트 포함)<br/>Exchange 2013-Office 2007 SP3<br/><br/>Office 클라이언트 지원에 대 한 자세한 내용은 [Exchange 지원 가능성 매트릭스](https://docs.microsoft.com/exchange/plan-and-deploy/supportability-matrix)를 확인 하세요.||| 


다음 리소스를 사용 하 여 마이그레이션에 도움을 받을 수 있습니다.

- [Exchange 배포 도우미](https://aka.ms/exdeploy)
- Exchange [2016](https://docs.microsoft.com/exchange/plan-and-deploy/active-directory/ad-schema-changes?view=exchserver-2016), [2013](https://docs.microsoft.com/Exchange/exchange-2013-active-directory-schema-changes-exchange-2013-help) 에 대 한 Active Directory 스키마 변경 사항
- Exchange [2016](https://docs.microsoft.com/exchange/plan-and-deploy/system-requirements?view=exchserver-2016), [2013](https://docs.microsoft.com/Exchange/exchange-2013-system-requirements-exchange-2013-help) 에 대 한 시스템 요구 사항
- Exchange [2016](https://docs.microsoft.com/exchange/plan-and-deploy/prerequisites?view=exchserver-2016), [2013](https://docs.microsoft.com/Exchange/exchange-2013-prerequisites-exchange-2013-help) 의 필수 구성 요소

## <a name="summary-of-options-for-office-2010-client-and-servers-and-windows-7"></a>Office 2010 클라이언트 및 서버 및 Windows 7의 옵션 요약

Office 2010 클라이언트 및 서버와 Windows 7에 대한 업그레이드, 마이그레이션 및 클라우드 옵션으로 이동에 대한 시각적 요약은 [지원 종료 포스터](../downloads/Office2010Windows7EndOfSupport.pdf)를 참조하세요.

[![Office 2010 클라이언트 및 서버 및 Windows 7 포스터에 대 한 지원 종료](../media/microsoft-365-overview/office2010-windows7-end-of-support.png)](../downloads/Office2010Windows7EndOfSupport.pdf)

이 페이지의 포스터는 Office 2010 클라이언트 및 서버 제품 및 Windows 7에서 지원 끝에 도달 하는 데 사용할 수 있는 다양 한 경로를 보여 주고, Microsoft 365 Enterprise의 기본 설정 경로 및 옵션을 지원 합니다.

또한이 포스터를 [다운로드](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/Office2010Windows7EndOfSupport.pdf) 하 여 letter, legal 또는 tabloid (11 x 17) 형식으로 인쇄할 수 있습니다.

## <a name="what-if-i-need-help"></a>도움이 필요한 경우 어떻게 하나요?

Microsoft 365로 마이그레이션하는 경우 Microsoft FastTrack 서비스를 사용할 수 있는 자격이 있을 수 있습니다. FastTrack은 최상의 방법, 도구 및 리소스를 제공 하 여 Microsoft 365로 마이그레이션을 최대한 원활 하 게 진행 합니다. 무엇 보다, 마지막 사서함 마이그레이션에 대 한 지원 엔지니어가 계획 및 디자인을 안내 합니다. FastTrack에 대 한 자세한 내용은 [Microsoft FastTrack](https://fasttrack.microsoft.com/)를 참조 하십시오.

Microsoft 365로 마이그레이션하는 동안 문제가 발생 하 여 FastTrack를 사용 하지 않거나 새 버전의 Exchange Server로 마이그레이션하는 경우 사용할 수 있는 몇 가지 리소스는 다음과 같습니다.

- [기술 커뮤니티](https://social.technet.microsoft.com/Forums/office/home?category=exchangeserver)
- [고객 지원](https://support.microsoft.com/gp/support-options-for-business)

## <a name="related-articles"></a>관련 문서

[Office 2010 서버 및 클라이언트 업그레이드에 도움이 되는 리소스](upgrade-from-office-2010-servers-and-products.md)
