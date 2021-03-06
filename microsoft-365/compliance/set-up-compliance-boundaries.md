---
title: EDiscovery 조사에 대 한 준수 경계 설정
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
ms.assetid: 1b45c82f-26c8-44fb-9f3b-b45436fe2271
description: 준수 경계를 사용 하 여 eDiscovery 관리자가 Microsoft 365에서 검색할 수 있는 사용자 콘텐츠 위치를 제어 하는 논리적 경계를 만드는 방법을 알아봅니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: afc01ea88e9a2de6550741dcaac105ef764a752f
ms.sourcegitcommit: ce46d1bd67091d4ed0e2b776dfed55e2d88cdbf4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49131133"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations"></a>EDiscovery 조사에 대 한 준수 경계 설정

이 문서의 지침은 중요 eDiscovery 또는 고급 eDiscovery를 사용 하 여 조사를 관리할 때 적용할 수 있습니다.

준수 경계는 eDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치 (예: 사서함, OneDrive 계정 및 SharePoint 사이트)를 제어 하는 조직 내에서 논리적 경계를 만듭니다. 또한 규정 준수 경계는 법률, 인적 자원 또는 조직 내 다른 조사를 관리 하는 데 사용 되는 eDiscovery 사례에 액세스할 수 있는 사용자를 제어 합니다. 지리적 boarders 및 규정을 준수 해야 하는 국내 기업에는 종종 다양 한 기관으로 분류 되는 정부에 대 한 적합성 경계가 필요 합니다. Microsoft 365에서는 준수 경계를 통해 콘텐츠 검색을 수행 하 고 eDiscovery 사례를 통해 조사를 관리할 때 이러한 요구 사항을 충족할 수 있습니다.
  
다음 그림의 예제를 사용 하 여 규정 준수 경계의 작동 방식을 알아봅니다.
  
![준수 경계는 eDiscovery 사례에 대 한 액세스를 제어 하는 기관 및 관리 역할 그룹에 대 한 액세스를 제어 하는 검색 권한 필터로 구성 됩니다.](../media/M365_ComplianceBoundary_OrgChart_v2.png)
  
이 예에서 Contoso b 2는 두 개의 자회사, 커피 및 Coho Winery으로 구성 되는 조직입니다. 비즈니스에서는 eDiscovery mangers 및 investigators가 해당 에이전시에서 Exchange 사서함, OneDrive 계정 및 SharePoint 사이트만 검색할 수 있어야 합니다. 또한 eDiscovery 관리자 및 investigators는 해당 에이전시의 eDiscovery 사례만 볼 수 있을 뿐 이며 구성원 인 경우에만 액세스할 수 있습니다. 준수 경계가 이러한 요구 사항을 충족 하는 방식은 다음과 같습니다.
  
- 콘텐츠 검색의 검색 권한 필터링 기능은 eDiscovery 관리자 및 investigators에서 검색할 수 있는 콘텐츠 위치를 제어 합니다. 즉, eDiscovery 관리자 및 네 번째 커피 기관에 있는 investigators는 네 번째 커피 자회사의 콘텐츠 위치만 검색할 수 있음을 의미 합니다. Coho Winery 자회사에도 동일한 제한이 적용 됩니다.

    역할 그룹은 보안 & 준수 센터에서 eDiscovery 사례를 볼 수 있는 사용자를 제어 합니다. 즉, eDiscovery 관리자 및 investigators는 해당 에이전시에서 eDiscovery 사례만 볼 수 있습니다.

- 또한 역할 그룹은 구성원을 eDiscovery 사례에 할당할 수 있는 사용자를 제어 합니다. 즉, eDiscovery 관리자 및 investigators는 자신이 자신을 구성원 인 사례에만 구성원을 할당할 수 있음을 의미 합니다.

준수 경계를 설정 하는 프로세스는 다음과 같습니다.
  
[1 단계: 사용자 특성을 식별 하 여 에이전시를 정의 합니다.](#step-1-identify-a-user-attribute-to-define-your-agencies)

[2 단계: Microsoft Support가 사용자 특성을 OneDrive 계정에 동기화 하는 요청을 파일에 포함](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[3 단계: 각 에이전시에 대 한 역할 그룹 만들기](#step-3-create-a-role-group-for-each-agency)

[4 단계: 검색 권한 필터를 만들어 준수 경계를 적용 합니다.](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[5 단계: 에이전시 내 조사에 대 한 eDiscovery 사례 만들기](#step-5-create-an-ediscovery-case-for-intra-agency-investigations)

## <a name="before-you-set-up-compliance-boundaries"></a>준수 경계를 설정 하기 전에

1 단계에서 id를 확인 하는 Azure Active Directory (Azure AD) 특성을 사용자의 OneDrive 계정 (2 단계)에 성공적으로 동기화 하려면 먼저 다음 필수 구성 요소를 충족 해야 합니다.

- 사용자에 게 Exchange Online 라이선스와 SharePoint Online 라이선스를 할당 해야 합니다.

- 사용자 사서함의 크기는 10mb 이상 이어야 합니다. 사용자의 사서함이 10mb 미만이 면 사용자의 OneDrive 계정에 대 한 기관 정의에 사용 되는 특성이 동기화 되지 않습니다.

- 준수 경계 및 검색 사용 권한 필터를 만드는 데 사용 되는 특성에는 Azure Active Directory (Azure AD) 특성이 사용자 사서함과 동기화 되어 있어야 합니다. 사용 하려는 특성이 동기화 되었는지 확인 하려면 Exchange Online PowerShell에서 [-User](https://docs.microsoft.com/powershell/module/exchange/get-user) cmdlet을 실행 합니다. 이 cmdlet의 출력은 Exchange Online과 동기화 되는 Azure AD 특성을 표시 합니다.

## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a>1 단계: 사용자 특성을 식별 하 여 에이전시를 정의 합니다.

첫 번째 단계는 기관을 정의 하는 데 사용할 Azure AD 특성을 선택 하는 것입니다. 이 특성은 eDiscovery 관리자가이 특성에 대 한 특정 값이 할당 된 사용자의 콘텐츠 위치만 검색 하도록 제한 하는 검색 권한 필터를 만드는 데 사용 됩니다. 예를 들어 Contoso에서 **부서** 특성을 사용 하기로 결정 한다고 가정해 보겠습니다. Coho Winery 자회사의 사용자에 대 한이 특성의 값은 다음과 같습니다  `FourthCoffee` `CohoWinery` . 4 단계에서이 쌍을 사용 하 여  `attribute:value`  eDiscovery 관리자가 검색할 수 있는 사용자 콘텐츠 위치를 제한 합니다 (예 *: FourthCoffee*). 
  
다음은 준수 경계에 사용할 수 있는 Azure AD 사용자 특성의 목록입니다.
  
- Company

- CustomAttribute1-CustomAttribute15

- 부서

- 사무실

- C (2 자리 국가 코드) <sup>*</sup>

  > [!NOTE]
  > <sup>*</sup> 이 특성은 Exchange Online PowerShell에서 **User** cmdlet을 실행 하 여 반환 되는 CountryOrRegion 속성에 매핑됩니다. 이 cmdlet은 지역화 된 국가 이름을 반환 하며,이 이름은 두 문자로 된 국가 코드에서 변환 됩니다. 자세한 내용은 [설정-사용자](https://docs.microsoft.com/powershell/module/exchange/set-user) cmdlet 참조 문서에서 CountryOrRegion 매개 변수 설명을 참조 하십시오.

더 많은 사용자 특성을 사용할 수 있지만 (특히 Exchange 사서함의 경우) 위에 나열 된 특성도 현재 OneDrive에서 지원 됩니다.
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a>2 단계: Microsoft Support가 사용자 특성을 OneDrive 계정에 동기화 하는 요청을 파일에 포함

다음 단계에서는 1 단계에서 선택한 Azure AD 특성을 조직의 모든 OneDrive 계정으로 동기화 하는 Microsoft 지원 서비스에 대 한 요청을 파일 합니다. 이 동기화가 수행 되 면 1 단계에서 선택한 특성 및 값이 라는 숨겨진 관리 속성에 매핑됩니다 `ComplianceAttribute` . 이 특성을 사용 하 여 4 단계에서 OneDrive에 대 한 검색 권한 필터를 만들 수 있습니다.
  
Microsoft 지원 서비스에 요청을 제출할 때 다음 정보를 포함 합니다.
  
- 조직의 기본 도메인 이름

- Azure AD 특성의 이름 (1 단계)

- 지원 요청의 목적에 대 한 다음 제목 또는 설명: "준수 보안 필터에 대해 Azure AD를 사용 하 여 비즈니스용 OneDrive 동기화 사용"을 수행 합니다. 이를 통해 요청을 구현 하는 eDiscovery 엔지니어링 팀에 요청을 라우팅할 수 있습니다.

엔지니어링이 변경 되 고 특성이 OneDrive에 동기화 되 면 Microsoft Support에서 변경 된 빌드 번호와 예상 배포 날짜가 전송 됩니다. 배포 프로세스는 일반적으로 지원 요청을 제출한 후 4-6 주 정도 걸립니다.
  
> [!IMPORTANT]
> 이 특성 변경 내용이 배포 될 때까지 3 단계부터 5 단계까지 완료할 수 있습니다. 그러나 콘텐츠 검색을 실행 해도 특성 동기화가 배포 될 때까지 검색 권한 필터에 지정 된 OneDrive 계정의 문서가 반환 되지 않습니다.
  
## <a name="step-3-create-a-role-group-for-each-agency"></a>3 단계: 각 에이전시에 대 한 역할 그룹 만들기

다음 단계에서는 보안 & 준수 센터에서 조직과 부합 하는 역할 그룹을 만듭니다. 기본 제공 eDiscovery 관리자 그룹을 복사 하 고, 적절 한 구성원을 추가 하 고, 필요에 따라 적용 되지 않을 수 있는 역할을 제거 하 여 역할 그룹을 만드는 것이 좋습니다. EDiscovery 관련 역할에 대 한 자세한 내용은 [Office 365 보안 & 준수 센터에서 ediscovery 사용 권한 할당](assign-ediscovery-permissions.md)을 참조 하십시오.
  
역할 그룹을 만들려면 보안 & 준수 센터의 **사용 권한** 페이지로 이동한 후 준수 경계 및 eDiscovery 사례를 사용 하 여 조사를 관리할 각 에이전시의 각 팀에 대해 역할 그룹을 만듭니다. 
  
Contoso 준수 경계 시나리오를 사용 하 여 네 개의 역할 그룹을 만들고 해당 구성원을 각각에 추가 해야 합니다.
  
- 커피 eDiscovery 관리자 4 대

- 네 번째 커피 Investigators

- Coho Winery eDiscovery 관리자

- Coho Winery Investigators
  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a>4 단계: 검색 권한 필터를 만들어 준수 경계를 적용 합니다.

각 에이전시에 대해 역할 그룹을 만든 후에는 각 역할 그룹을 특정 에이전시에 연결 하는 검색 권한 필터를 만들고 준수 경계 자체를 정의 합니다. 각 에이전시에 대해 하나의 검색 권한 필터를 만들어야 합니다. 보안 권한 필터를 만드는 방법에 대 한 자세한 내용은 [콘텐츠 검색에 대 한 사용 권한 필터링 구성을](permissions-filtering-for-content-search.md)참조 하십시오.
  
준수 경계에 사용 되는 검색 권한 필터를 만드는 데 사용 되는 구문은 다음과 같습니다.

```powershell
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<ComplianceAttribute>  -eq '<AttributeVale> '", "Site_<ComplianceAttribute>  -eq '<AttributeValue>' -or Site_Path -like '<SharePointURL>*'" -Action <Action >
```

다음은 명령의 각 매개 변수에 대 한 설명입니다.
  
- `FilterName`: 필터의 이름을 지정 합니다. 필터를 사용 하는 에이전시를 설명 하거나 식별 하는 이름을 사용 합니다.

- `Users`: 수행 하는 콘텐츠 검색 작업에이 필터를 적용할 사용자 또는 그룹을 지정 합니다. 준수 경계의 경우이 매개 변수는 필터를 만드는 데 사용할 에이전시에서 3 단계에서 만든 역할 그룹을 지정 합니다. 참고 이것은 다중 값 매개 변수 이므로 쉼표로 구분 하 여 하나 이상의 역할 그룹을 포함할 수 있습니다.

- `Filters`: 필터에 대 한 검색 조건을 지정 합니다. 준수 경계에 대해 다음 필터를 정의 합니다. 각 항목은 콘텐츠 위치에 적용 됩니다. 

    - `Mailbox`: 매개 변수에 정의 된 역할 그룹이 검색할 수 있는 사서함을 지정 합니다  `Users` . 준수 경계의 경우  *ComplianceAttribute*  는 1 단계에서 식별 한 특성 및  *AttributeValue*  에서 해당 에이전시를 지정 합니다. 이 필터는 역할 그룹의 구성원이 특정 에이전시의 사서함만 검색할 수 있도록 허용 합니다. 예를 들면 `"Mailbox_Department -eq 'FourthCoffee'"` 입니다. 

    - `Site`: 매개 변수에 정의 된 역할 그룹이 검색할 수 있는 OneDrive 계정을 지정 합니다 `Users` . OneDrive 필터의 경우 실제 문자열을 사용  `ComplianceAttribute` 합니다. 이는 1 단계에서 확인 하 고 2 단계에서 제출한 지원 요청의 결과로 OneDrive 계정에 동기화 되는 것과 동일한 특성에 매핑됩니다. *AttributeValue*  는 에이전시를 지정 합니다. 이 필터는 역할 그룹의 구성원이 특정 에이전시에서 OneDrive 계정만 검색할 수 있도록 허용 합니다. 예를 들면  `"Site_ComplianceAttribute -eq 'FourthCoffee'"` 입니다.

    - `Site_Path`: 매개 변수에 정의 된 역할 그룹이 검색할 수 있는 SharePoint 사이트를 지정 합니다  `Users` . *SharePointURL* 은 역할 그룹의 구성원이 검색할 수 있는 에이전시의 사이트를 지정 합니다. 예:  `"Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`. `Site`및 필터는 `Site_Path` **or** 연산자로 연결 됩니다.

     > [!NOTE]
     > 매개 변수에 대 한 구문에 `Filters` *필터 목록이* 포함 되어 있습니다. 필터 목록은 사서함 필터와 쉼표로 구분 된 사이트 필터를 포함 하는 필터입니다. 위의 예제에서는 쉼표로 **Mailbox_ComplianceAttribute** 구분 하 고 **Site_ComplianceAttribute** `-Filters "Mailbox_<ComplianceAttribute>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq '<AttributeValue>' -or Site_Path -like '<SharePointURL>*'"` 합니다. 콘텐츠 검색을 실행 하는 동안이 필터를 처리 하면 필터 목록 (하나의 사서함 필터 및 사이트 필터)에서 두 개의 검색 권한 필터가 만들어집니다. 필터 목록을 사용 하는 대신 각 에이전시에 대해 두 개의 검색 권한 필터, 즉 사서함 특성에 대 한 검색 권한 필터와 사이트 특성에 대 한 하나의 필터를 만들 수 있습니다. 두 경우 모두 결과는 동일 하 게 됩니다. 필터 목록을 사용 하거나 별도의 검색 권한 만들기 필터를 만드는 것은 기본 설정의 중요 한 사항입니다.

- `Action`: 필터가 적용 되는 준수 검색 작업의 유형을 지정 합니다. 예를 들어  `-Action Search` 매개 변수에 정의 된 역할 그룹의 구성원이 `Users` 콘텐츠 검색을 실행 하는 경우에만 필터를 적용 합니다. 이 경우 검색 결과를 내보낼 때 필터가 적용 되지 않습니다. 준수 경계의 경우 필터를  `-Action All` 모든 검색 작업에 적용 하도록 사용 합니다. 

    콘텐츠 검색 작업 목록은 [콘텐츠 검색에 대 한 권한 필터링 구성](permissions-filtering-for-content-search.md#new-compliancesecurityfilter)의 "new-compliancesecurityfilter" 섹션을 참조 하십시오.

다음은 Contoso 준수 경계 시나리오를 지원 하기 위해 만드는 두 가지 검색 권한 필터의 예입니다. 이 두 예에는 모두 쉼표로 구분 된 필터 목록이 있으며,이 목록에는 사서함과 사이트 필터가 같은 검색 권한 필터에 포함 되 고 쉼표로 구분 됩니다.
  
### <a name="fourth-coffee"></a>커피 4

```powershell
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```

### <a name="coho-winery"></a>Coho Winery

```powershell
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-intra-agency-investigations"></a>5 단계: 내 에이전시 조사에 대 한 eDiscovery 사례 만들기

마지막 단계는 보안 & 준수 센터에서 eDiscovery 사례를 만든 다음 3 단계에서 만든 역할 그룹을 사례 구성원으로 추가 하는 것입니다. 이로 인해 준수 경계를 사용 하는 경우의 두 가지 중요 한 특징이 있습니다.
  
- 사례에 추가 된 역할 그룹의 구성원만이 보안 & 준수 센터에서 사례를 보고 액세스할 수 있습니다. 예를 들어, 네 번째 커피 Investigators 역할 그룹이 사례 유일한 구성원 인 경우에는 네 번째 커피 eDiscovery 관리자 역할 그룹의 구성원 또는 다른 역할 그룹의 구성원도 해당 사례를 보거나 액세스할 수 없습니다.

- 사례에 할당 된 역할 그룹의 구성원이 사례와 연결 된 검색을 실행 하는 경우, 해당 사용자는 해당 에이전시 (4 단계에서 만든 검색 권한 필터에 의해 정의 됨) 내의 콘텐츠 위치만 검색할 수 있습니다.

사례를 만들고 구성원을 할당 하려면 다음을 수행 합니다.

1. 보안 & 준수 센터에서 **ediscovery** 또는 **Advanced eDiscovery** 페이지로 이동한 후 사례를 만듭니다.

2. EDiscovery 사례 목록에서 만든 사례 이름을 클릭 합니다.

3. **이 사례** 플라이 아웃 관리 페이지의 **역할 그룹 관리** 에서 ![ 아이콘 추가를 클릭 ](../media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **Add** 합니다.

    ![EDiscovery 사례의 구성원으로 역할 그룹 추가](../media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. 역할 그룹 목록에서 3 단계에서 만든 역할 그룹 중 하나를 선택 하 고 **추가** 를 클릭 합니다.

5. **이 사례** 플라이 아웃 관리에서 **저장** 을 클릭 하 여 변경 내용을 저장 합니다.

## <a name="searching-and-exporting-content-in-multi-geo-environments"></a>다중 지역 환경에서 콘텐츠 검색 및 내보내기

또한 검색 권한 필터를 사용 하 여 [SharePoint 다중 위치 환경](https://go.microsoft.com/fwlink/?linkid=860840)에서 콘텐츠를 검색 하는 데 사용할 수 있는 콘텐츠와 검색 되는 데이터 센터의 위치를 제어할 수 있습니다.
  
- **검색 결과 내보내기:** 특정 데이터 센터에서 Exchange 사서함, SharePoint 사이트 및 OneDrive 계정 으로부터 검색 결과를 내보낼 수 있습니다. 즉, 검색 결과를 내보낼 데이터 센터 위치를 지정할 수 있습니다.

    **New-compliancesecurityfilter** 또는 **New-compliancesecurityfilter** cmdlet에 **Region** 매개 변수를 사용 하 여 내보내기가 라우팅되는 데이터 센터를 만들거나 변경 합니다.
  
    |**매개 변수 값**|**데이터 센터 위치**|
    |:-----|:-----|
    |NAM  <br/> |북미 (데이터 센터는 미국)  <br/> |
    |EUR  <br/> |유럽  <br/> |
    |APC  <br/> |아시아 태평양  <br/> |
    |CAN <br/> |캐나다|
    |||

- **콘텐츠 검색 경로:** SharePoint 사이트 및 OneDrive 계정의 콘텐츠 검색을 위성 데이터 센터에 라우팅할 수 있습니다. 즉, 검색을 실행할 데이터 센터 위치를 지정할 수 있습니다.

    **Region** 매개 변수에 다음 값 중 하나를 사용 하 여 SharePoint 사이트 및 OneDrive 계정을 검색할 때 검색을 실행할 데이터 센터 위치를 제어 합니다. 
  
    |**매개 변수 값**|**SharePoint의 데이터 센터 라우팅 위치**|
    |:-----|:-----|
    |NAM  <br/> |US  <br/> |
    |EUR  <br/> |유럽  <br/> |
    |APC  <br/> |아시아 태평양  <br/> |
    |CAN  <br/> |US  <br/> |
    |AUS  <br/> |아시아 태평양  <br/> |
    |KOR  <br/> |조직의 기본 데이터 센터  <br/> |
    |GBR  <br/> |유럽  <br/> |
    |JPN  <br/> |아시아 태평양  <br/> |
    |IND  <br/> |아시아 태평양  <br/> |
    |LAM  <br/> |US  <br/> |
    |폴더도  <br/> |유럽 |
    |BRA  <br/> |북미 데이터 센터 |
    |||

   검색 권한 필터에 **Region** 매개 변수를 지정 하지 않으면 조직의 기본 SharePoint 지역이 검색 됩니다. 검색 결과는 가장 가까운 데이터 센터로 내보내집니다.

   이 개념을 단순화 하기 위해 **Region** 매개 변수는 SharePoint 및 OneDrive에서 콘텐츠를 검색 하는 데 사용 되는 데이터 센터를 제어 합니다. Exchange 콘텐츠 검색은 데이터 센터의 지리적 위치에 바인딩되지 않으므로 Exchange에서 콘텐츠를 검색 하는 데는 적용 되지 않습니다. 또한 동일한 **지역** 매개 변수 값은 내보내기가 라우팅되는 데이터 센터도 지시할 수 있습니다. 이는 종종 지리적 boarders에서 데이터 이동을 제어 하는 데 필요 합니다.

> [!NOTE]
> 고급 eDiscovery를 사용 하는 경우 **region** 매개 변수는 데이터를 내보내는 지역을 제어 하지 않습니다. 조직의 기본 데이터 센터에서 데이터를 내보냅니다. 또한 SharePoint 및 OneDrive의 콘텐츠 검색은 데이터 센터의 지리적 위치에 연결 되지 않습니다. 모든 데이터 센터가 검색 됩니다. 고급 eDiscovery에 대 한 자세한 내용은 [Microsoft 365의 고급 ediscovery 솔루션 개요](overview-ediscovery-20.md)를 참조 하세요.

다음은 준수 경계에 대 한 검색 권한 필터를 만들 때 **Region** 매개 변수를 사용 하는 예입니다. 이 경우에는 네 번째 커피 자회사를 북미에 있고 Coho Winery가 유럽에 있는 것으로 가정 합니다. 
  
```powershell
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```powershell
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```

다중 지리적 환경에서 콘텐츠를 검색 하 고 내보낼 때는 다음 사항을 염두에 두어야 합니다.
  
- **지역** 매개 변수가 Exchange 사서함의 검색을 제어하지 않습니다. 사서함을 검색 하면 모든 데이터 센터가 검색 됩니다. Exchange 사서함이 검색 되는 범위를 제한 하려면 검색 권한 필터를 만들거나 변경할 때 **Filters** 매개 변수를 사용 합니다. 

- EDiscovery 관리자가 여러 SharePoint 지역에서 검색 해야 하는 경우에는 해당 eDiscovery 관리자에 대해 검색 권한 필터에 사용할 다른 사용자 계정을 만들어 SharePoint 사이트 또는 OneDrive 계정이 있는 지역을 지정 해야 합니다. 이를 설정 하는 방법에 대 한 자세한 내용은 [콘텐츠 검색](content-search.md#searching-for-content-in-a-sharepoint-multi-geo-environment)에서 "SharePoint 다중 지리적 환경에서 콘텐츠 검색" 섹션을 참조 하십시오.

- SharePoint 및 OneDrive에서 콘텐츠를 검색할 때 **Region** 매개 변수는 ediscovery 관리자가 ediscovery 조사를 수행 하는 기본 또는 위성 위치를 검색 하도록 지시 합니다. EDiscovery 관리자가 SharePoint 및 OneDrive 사이트 검색 사용 권한 필터에 지정 된 지역 외부를 검색 하는 경우 검색 결과가 반환 되지 않습니다.

- 검색 결과를 내보낼 때 모든 콘텐츠 위치의 콘텐츠, 즉 Exchange, 비즈니스용 Skype, SharePoint, OneDrive, 콘텐츠 검색 도구를 사용 하 여 검색할 수 있는 기타 서비스 등의 콘텐츠가 **Region** 매개 변수로 지정 된 데이터 센터의 Azure 저장 위치에 업로드 됩니다. 이렇게 하면 조직이 제어 테두리에 걸쳐 콘텐츠를 내보낼 수 없도록 하 여 규정 준수를 유지 하는 데 도움이 됩니다. 검색 권한 필터에 지역이 지정 되어 있지 않으면 콘텐츠가 조직의 기본 데이터 센터에 업로드 됩니다.

- 다음 명령을 실행 하 여 기존 검색 권한 필터를 편집 하 여 지역을 추가 하거나 변경할 수 있습니다.

    ```powershell
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```

## <a name="using-compliance-boundaries-for-sharepoint-hub-sites"></a>SharePoint 허브 사이트에 준수 경계 사용

[SharePoint 허브 사이트](https://docs.microsoft.com/sharepoint/dev/features/hub-site/hub-site-overview) 는 eDiscovery 준수 경계 다음에 오는 지리적 또는 에이전시 경계와 종종 일치 합니다. 즉, 허브 사이트의 사이트 ID 속성을 사용 하 여 준수 경계를 만들 수 있습니다. 이 작업을 수행 하려면 SharePoint Online PowerShell의 [SPOHubSite](https://docs.microsoft.com/powershell/module/sharepoint-online/get-spohubsite#examples) cmdlet을 사용 하 여 허브 사이트에 대 한 SiteId를 가져온 다음 부서 ID 속성에이 값을 사용 하 여 검색 권한 필터를 만듭니다.

SharePoint 허브 사이트에 대 한 검색 권한 필터를 만들려면 다음 구문을 사용 합니다.

```powershell
New-ComplianceSecurityFilter -FilterName <Filter Name> -Users <User or Group> -Filters "Site_Departmentid -eq '{SiteId of hub site}'" -Action ALL
```

다음은 Coho Winery 에이전시에 대해 허브 사이트에 대 한 검색 권한 필터를 만드는 예입니다.

```powershell
New-ComplianceSecurityFilter -FilterName "Coho Winery Hub Site Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Site_Departmentid -eq '44252d09-62c4-4913-9eb0-a2a8b8d7f863'" -Action ALL
```

## <a name="compliance-boundary-limitations"></a>준수 경계 제한

EDiscovery 사례를 관리 하 고 준수 경계를 사용 하는 조사를 관리할 때는 다음과 같은 제한 사항을 염두에 두어야 합니다.
  
- 검색을 만들고 실행 하는 경우에는 에이전시 외부에 있는 콘텐츠 위치를 선택할 수 있습니다. 그러나 검색 권한 필터 때문에 해당 위치의 콘텐츠가 검색 결과에 포함 되지 않습니다.

- 준수 경계는 eDiscovery 사례의 보류에 적용 되지 않습니다. 즉, 한 에이전시의 eDiscovery 관리자가 사용자를 보류 중인 다른 에이전시에 배치할 수 있습니다. 그러나 eDiscovery 관리자가 보류 되었던 사용자의 콘텐츠 위치를 검색 하는 경우 준수 경계가 적용 됩니다. 즉, eDiscovery 관리자는 사용자를 보류 상태로 설정할 수 있더라도 사용자의 콘텐츠 위치를 검색할 수 없습니다.

    또한 보유 통계는 에이전시의 콘텐츠 위치에만 적용 됩니다.

- 검색 사용 권한 필터는 Exchange 공용 폴더에 적용 되지 않습니다.

## <a name="more-information"></a>추가 정보

- 사서함을 사용 하지 않거나 일시 삭제 한 경우 Azure AD 특성이 더 이상 사서함과 동기화 되지 않습니다. 사서함을 삭제 했을 때 우편함이 보존 되는 경우 사서함을 삭제 하기 전에 마지막으로 Azure AD 특성을 동기화 한 시간을 기준으로 하 여 해당 편지함에 유지 되는 콘텐츠가 여전히 준수 경계 또는 검색 권한 필터에 적용 됩니다. 

    또한 사서함이 사용이 허가 되지 않았거나 일시 삭제 된 경우 사용자 사서함과 OneDrive 계정 간의 동기화가 중단 됩니다. OneDrive 계정에 대 한 준수 특성의 마지막 스탬프 값은 계속 적용 됩니다.

- 준수 특성은 사용자의 Exchange 사서함에서 7 일 마다 OneDrive 계정으로 동기화 됩니다. 앞에서 설명한 것 처럼이 동기화는 사용자에 게 Exchange Online 및 SharePoint Online 라이선스가 모두 할당 되 고 사용자의 사서함이 10mb 이상인 경우에만 발생 합니다.

- 사용자의 사서함과 OneDrive 계정에 대해 준수 경계 및 검색 권한 필터가 구현 된 경우에는 해당 사용자의 사서함을 삭제 하지 않는 것이 좋습니다. 즉, 사용자의 사서함을 삭제 하는 경우 사용자의 OneDrive 계정도 제거 해야 합니다.

- 사용자가 두 개 이상의 OneDrive 계정을 가질 수 있는 상황 (예: 직원을 반환 하는 경우)이 있습니다. 이러한 경우 Azure AD의 사용자와 연결 된 기본 OneDrive 계정만 동기화 됩니다.

- 준수 경계 및 검색 권한 필터는이 스탬프 처리 된 콘텐츠에 대 한 후속 인덱싱, Exchange, OneDrive 및 SharePoint의 콘텐츠에 스탬프 처리 되는 특성에 따라 달라 집니다. 

- `-not()`콘텐츠 기반 규정 준수 범위에 대해 검색 권한 필터에 사용 하는 것과 같은 제외 필터는 사용 하지 않는 것이 좋습니다. 최근에 업데이트 된 특성이 있는 콘텐츠가 인덱싱되지 않은 경우 제외 필터를 사용 하면 예기치 않은 결과가 발생 합니다. 

## <a name="frequently-asked-questions"></a>자주 묻는 질문

**New-ComplianceSecurityFilter 및 Set-ComplianceSecurityFilter cmdlet을 사용 하 여 검색 권한 필터를 만들고 관리할 수 있는 사람**
  
검색 권한 필터를 만들고 보고 수정 하려면 보안 & 준수 센터에서 조직 관리 역할 그룹의 구성원 이어야 합니다.
  
**여러 기관에 걸쳐 있는 둘 이상의 역할 그룹에 eDiscovery 관리자를 할당 하는 경우, 한 에이전시에서 콘텐츠를 검색 하려면 어떻게 해야 합니까?**
  
EDiscovery 관리자는 검색 쿼리에 특정 에이전시로 제한 되는 매개 변수를 추가할 수 있습니다. 예를 들어 조직에서 **CustomAttribute10** 속성을 지정 하 여 기관을 차별화 하는 경우 다음을 검색 쿼리에 추가 하 여 특정 에이전시에서 사서함 및 OneDrive 계정을 검색할 수 있습니다  `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>` .
  
**검색 권한 필터에서 준수 특성으로 사용 되는 특성의 값이 변경 된 경우 어떻게 되나요?**
  
필터에 사용 된 특성의 값이 변경 되는 경우 검색 권한 필터에 대해 최대 3 일이 소요 됩니다. 예를 들어 Contoso 시나리오에서, 네 번째 커피 에이전시의 사용자가 Coho Winery 에이전시로 전송 된다는 것을 가정해 보겠습니다. 따라서 사용자 개체의 **부서** 특성 값은 *FourthCoffee* 에서 *CohoWinery* 로 변경 됩니다. 이 상황에서 네 번째 커피 eDiscovery 및 투자자는 해당 사용자에 대 한 검색 결과를 3 일 동안 (특성이 변경 된 후)으로 가져옵니다. 마찬가지로, Coho Winery eDiscovery 관리자 및 investigators에서 사용자에 대 한 검색 결과를 가져올 때까지 3 일 정도 걸립니다.
  
**EDiscovery 관리자가 두 개의 별도 준수 경계의 콘텐츠를 볼 수 있습니까?**
  
예, 두 기관에 모두 표시 되는 역할 그룹에 eDiscovery 관리자를 추가 하 여 Exchange 사서함을 검색할 때이 작업을 수행할 수 있습니다. 그러나 SharePoint 사이트 및 OneDrive 계정을 검색할 때 eDiscovery 관리자는 해당 기관이 동일한 지역 또는 지리적 위치에 있는 경우에만 서로 다른 준수 경계에서 콘텐츠를 검색할 수 있습니다. **참고:** SharePoint 및 OneDrive에서 콘텐츠를 검색할 때 지리적 위치로 제한이 없기 때문에 사이트에 대 한이 제한은 고급 eDiscovery에서 적용 되지 않습니다.
  
**검색 사용 권한 필터는 eDiscovery 사례 보류, Microsoft 365 보존 정책 또는 DLP에 대해 작동 하나요?**
  
아니요, 현재는 아닙니다.
  
**콘텐츠를 내보내는 위치를 제어 하는 영역을 지정 했지만 해당 지역에 SharePoint 조직이 없는 경우에도 SharePoint를 검색할 수 있나요?**
  
검색 권한 필터에 지정 된 지역이 조직에 없는 경우에는 기본 지역이 검색 됩니다.
  
**조직에서 만들 수 있는 검색 권한 필터의 최대 수는 얼마나 됩니까?**
  
조직에서 만들 수 있는 검색 권한 필터의 수에는 제한이 없습니다. 그러나 검색 권한 필터가 100 개 보다 많으면 검색 성능이 영향을 받습니다. 조직의 검색 권한 필터 수를 가능한 한 작게 유지 하려면 가능 하면 Exchange, SharePoint 및 OneDrive에 대 한 규칙을 단일 검색 권한 필터에 결합 하는 필터를 만듭니다.
