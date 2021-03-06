---
title: 보안 & 준수 센터에서 eDiscovery 권한 할당
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
search.appverid:
- MOE150
- MET150
ms.assetid: 5b9a067b-9d2e-4aa5-bb33-99d8c0d0b5d7
description: 보안 & 준수 센터를 사용 하 여 eDiscovery 관련 작업을 수행 하는 데 필요한 사용 권한을 할당 합니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: f81ac5a87fad99689f7cfa36c044d3de765f4520
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48920312"
---
# <a name="assign-ediscovery-permissions-in-the-security--compliance-center"></a>보안 & 준수 센터에서 eDiscovery 권한 할당

사용자가 Office 365 또는 Microsoft 365 준수 센터의 보안 & 준수 센터에서 [eDiscovery 관련 도구](ediscovery.md) 를 사용 하 게 하려면 적절 한 사용 권한을 할당 해야 합니다. 이 작업을 수행 하는 가장 쉬운 방법은 보안 & 준수 센터의 **사용 권한** 페이지에서 해당 역할 그룹에 해당 하는 사람을 추가 하는 것입니다. 이 항목에서는 보안 & 준수 센터를 사용 하 여 eDiscovery 및 콘텐츠 검색 관련 작업을 수행 하는 데 필요한 사용 권한에 대해 설명 합니다.
  
보안 & 준수 센터의 기본 eDiscovery 관련 역할 그룹을 **EDiscovery 관리자** 라고 합니다. 이 역할 그룹에는 두 개의 하위 그룹이 있습니다.
  
- **ediscovery** 관리자-ediscovery Manager는 보안 & 준수 센터의 콘텐츠 검색 도구를 사용 하 여 조직의 콘텐츠 위치를 검색 하 고 미리 보기 및 검색 결과 내보내기와 같은 다양 한 검색 관련 작업을 수행할 수 있습니다. 또한 구성원은 핵심 eDiscovery 및 고급 eDiscovery에서 사례를 만들고 관리 하 고, 사례에 구성원을 추가 및 제거 하 고, 사례 보류를 만들고, 사례와 연결 된 검색을 실행 하 고, 사례 데이터에 액세스할 수 있습니다. eDiscovery 관리자는 자신이 만드는 사례에 액세스 하 고 관리할 수만 있습니다. 다른 eDiscovery 관리자가 만든 사례에 액세스 하거나 관리할 수 없습니다.
  
- **ediscovery** 관리자-ediscovery 관리자는 ediscovery 관리자 역할 그룹의 구성원이 며, ediscovery 관리자가 수행할 수 있는 동일한 콘텐츠 검색 및 사례 관리 관련 작업을 수행할 수 있습니다. 또한 eDiscovery 관리자(Administrator)는 다음과 같은 작업을 수행할 수 있습니다.
  
  - 보안 & 준수 센터의 **eDiscovery** 및 **고급 eDiscovery** 페이지에 나열 된 모든 경우에 액세스 합니다.

  - 조직의 모든 경우에 대 한 고급 eDiscovery의 사례 데이터 액세스
  
  - 서비스 케이스의 구성원으로 자신을 추가한 후 eDiscovery 사례를 관리 합니다.
  
  조직에서 eDiscovery 관리자가 필요한 이유는 [추가 정보](#more-information) 섹션을 참조 하십시오.

> [!NOTE]
> 고급 eDiscovery를 사용 하 여 사용자 데이터를 분석 하려면 사용자 (데이터 custodian)에 Office 365 E5 또는 Microsoft 365 E5 라이선스를 할당 해야 합니다. 또는 Office 365 E1 또는 Office 365 또는 Microsoft 365 E3 라이선스를 사용 하는 사용자에 게 Microsoft 365 E5 준수 또는 Microsoft 365 eDiscovery 및 감사 추가 기능 라이선스를 할당할 수 있습니다. 관리자, 규정 준수 담당자 또는 구성원으로 사례에 할당 되 고 고급 eDiscovery를 사용 하 여 데이터를 수집, 확인 및 분석 하는 데에는 E5 라이선스가 필요 하지 않습니다. 고급 eDiscovery 라이선스에 대 한 자세한 내용은 [Advanced ediscovery 시작](get-started-with-advanced-ediscovery.md)을 참조 하세요.
  
## <a name="confirm-your-roles"></a>역할 확인

- 보안 & 준수 센터에서 eDiscovery 권한을 할당 하려면 조직 관리 역할 그룹의 구성원 이거나 역할 관리 역할을 할당 받아야 합니다.

- Security & 준수 센터 PowerShell의 [추가-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/Add-RoleGroupMember) cmdlet을 사용 하 여 메일 사용이 가능한 보안 그룹을 ediscovery 관리자 역할 그룹에 있는 ediscovery 관리자의 구성원으로 추가할 수 있습니다. 그러나 메일 사용이 가능한 보안 그룹은 eDiscovery Administrators 그룹에 추가할 수 없습니다. 자세한 [내용은 추가 정보](#more-information) 섹션을 참조 하십시오. 
  
## <a name="assign-ediscovery-permissions-in-the-security--compliance-center"></a>보안 & 준수 센터에서 eDiscovery 권한 할당

1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
  
2. 회사 또는 학교 계정을 사용하여 로그인합니다.
  
3. 보안 및 준수 센터의 왼쪽 창에서 **사용 권한을** 선택한 다음 **eDiscovery Manager** 옆에 있는 확인란을 선택 합니다.
  
4. **Ediscovery 관리자** 플라이 아웃 페이지에서 할당 하려는 eDiscovery 권한에 따라 다음 중 하나를 수행 합니다.
  
    **사용자를 EDiscovery 관리자로 지정 하려면 다음을** 수행 합니다. **EDiscovery 관리자** 옆에 있는 **편집** 을 선택 합니다. **Ediscovery 관리자 선택** 섹션에서 **ediscovery 관리자 선택** 하이퍼링크를 선택 하 고 아이콘 추가 (추가)를 선택 합니다 ![ ](../media/ITPro-EAC-AddIcon.gif) **Add**. EDiscovery 관리자로 추가할 사용자 (또는 사용자)를 선택 하 고 **추가** 를 선택 합니다. 사용자 추가가 완료 되 면 **완료** 를 선택 합니다. 그런 다음 **Ediscovery 관리자** 플라이 아웃 선택 페이지에서 **저장** 을 선택 하 여 ediscovery 관리자 멤버 자격에 대 한 변경 내용을 저장 합니다.
  
    **사용자를 EDiscovery 관리자로 설정 하려면 다음을** 수행 합니다. **EDiscovery 관리자** 옆에 있는 **편집** 을 선택 합니다. **Ediscovery 관리자 선택** 섹션의 **eDiscovery 관리자** 에서 **ediscovery 관리자 선택을** 선택 하 고 **편집** 을 선택한 후에 ![ 아이콘 추가를 선택 ](../media/ITPro-EAC-AddIcon.gif) **Add** 합니다. **EDiscovery 관리자로** 추가 하려는 사용자 (또는 사용자)를 선택한 다음 **추가** 를 선택 합니다. 사용자 추가가 완료 되 면 **완료** 를 선택 합니다. 그런 다음 **Ediscovery 관리자** 플라이 아웃 선택 페이지에서 **저장** 을 선택 하 여 ediscovery 관리자 멤버 자격에 대 한 변경 내용을 저장 합니다.
  
> [!NOTE]
> **EDiscoveryCaseAdmin** cmdlet을 사용 하 여 사용자를 eDiscovery 관리자로 설정할 수도 있습니다. 그러나이 cmdlet을 eDiscovery 관리자로 설정 하려면 사용자에 게 사례 관리 역할을 할당 받아야 합니다. 자세한 내용은 [Add-eDiscoveryCaseAdmin](https://go.microsoft.com/fwlink/p/?LinkID=798217)를 참조 하세요. 
  
보안 & 준수 센터의 **사용 권한** 페이지에서 사용자 eDiscovery 관련 사용 권한을 준수 관리자, 조직 관리 및 검토자 역할 그룹에 추가 하 여 할당할 수도 있습니다. 이러한 각 역할 그룹에 할당 된 eDiscovery 관련 RBAC 역할에 대 한 자세한 내용은 [eDiscovery와 관련 된 rbac 역할](#rbac-roles-related-to-ediscovery) 섹션을 참조 하십시오.

## <a name="rbac-roles-related-to-ediscovery"></a>EDiscovery와 관련 된 RBAC 역할

다음 표에서는 보안 & 준수 센터의 eDiscovery 관련 RBAC 역할을 나열 하 고 각 역할이 기본적으로 할당 되는 기본 제공 역할 그룹을 나타냅니다.
  
|**역할**|**준수 관리자**|**eDiscovery 관리자 & 관리자**|**조직 관리**|**Reviewer**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|사례 관리 <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|통신 <br/> | <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|규격 검색 <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|Custodian <br/> | <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|내보내기 <br/> | <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|Hold <br/>  |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |
|미리 보기 <br/>  | <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> | <br/> |
|검토 <br/>  | <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> | <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |
|RMS 암호 해독 <br/>  ||![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png) <br/> |||
|검색 및 제거 <br/> | <br/> | <br/> |![확인 표시](../media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)           <br/> | <br/> |
||||
  
다음 섹션에서는 위의 표에 나열 된 각 eDiscovery 관련 RBAC 역할에 대해 설명 합니다.

### <a name="case-management"></a>사례 관리

이 역할을 사용 하면 보안 & 준수 센터에서 핵심 eDiscovery 및 고급 eDiscovery 사례에 대 한 액세스를 만들고, 편집 하 고, 삭제 하 고, 제어할 수 있습니다. 앞에서 설명한 것 처럼, 사용자는 **eDiscoveryCaseAdmin** cmdlet을 사용 하 여 eDiscovery 관리자로 설정할 수 있도록 사례 관리 역할을 할당 받아야 합니다.

자세한 내용은 다음을 참조하세요.

- [핵심 eDiscovery 시작](get-started-core-ediscovery.md)

- [Advanced eDiscovery 시작](get-started-with-advanced-ediscovery.md)

### <a name="communication"></a>통신

이 역할을 통해 사용자는 고급 eDiscovery 사례에서 식별 된 custodians와의 모든 통신을 관리할 수 있습니다. 여기에는 보존 알림, 유지 및 관리에 대 한 알림을 만드는 작업이 포함 됩니다. 또한 사용자는 보류 알림의 custodian 확인을 추적 하 고 각 custodian에서 custodian로 식별 된 경우의 통신을 추적 하는 데 사용 되는 custodian 포털에 대 한 액세스를 관리할 수 있습니다.

자세한 내용은 [Advanced eDiscovery에서 통신에](managing-custodian-communications.md)대 한 작업을 참조 하세요.

### <a name="compliance-search"></a>규격 검색

이 역할을 사용 하면 사용자가 보안 & 준수 센터에서 콘텐츠 검색 도구를 실행 하 여 사서함 및 공용 폴더, SharePoint Online 사이트, 비즈니스용 OneDrive 사이트, 비즈니스용 Skype 대화, Microsoft 365 그룹 및 Microsoft 팀, Yammer 그룹을 검색할 수 있습니다. 이 역할을 사용 하면 사용자가 예상 검색 결과를 가져오고 내보내기 보고서를 만들 수 있지만 검색 결과를 미리 보거나 내보내거나 삭제 하는 등의 콘텐츠 검색 작업을 시작 하려면 추가 역할이 필요 합니다.

준수 검색 역할이 할당 되었지만 미리 보기 역할이 없는 사용자는 미리 보기 역할이 할당 된 사용자가 미리 보기 작업을 시작한 검색 결과를 미리 볼 수 있습니다. 미리 보기 역할이 없는 사용자는 초기 미리 보기 작업을 만든 후 최대 2 주 동안 결과를 미리 볼 수 있습니다.

마찬가지로 준수 검색 역할을 할당 했지만 내보내기 역할이 없는 사용자는 내보내기 역할이 할당 된 사용자가 내보내기 작업을 시작한 검색의 결과를 다운로드할 수 있습니다. 내보내기 역할이 없는 사용자는 초기 내보내기 작업을 만든 후 최대 2 주까지 검색 결과를 다운로드할 수 있습니다. 그 후에는 내보내기 역할을 가진 사용자가 내보내기를 다시 시작 하지 않으면 결과를 다운로드할 수 없습니다.

자세한 내용은 [Office 365의 콘텐츠 검색](content-search.md)을 참조 하세요.

### <a name="custodian"></a>Custodian

이 역할을 사용 하면 사용자가 고급 eDiscovery 사례를 위해 custodians을 식별 및 관리 하 고, Azure Active Directory 및 기타 원본의 정보를 통해 custodians와 연결 된 데이터 원본을 찾을 수 있습니다. 사용자는 사서함, SharePoint 사이트 및 팀과 같은 다른 데이터 원본을 사례에 custodians 연결할 수 있습니다. 또한 사용자는 custodians와 연결 된 데이터 원본에 법적 보존을 설정 하 여 콘텐츠를 사례 컨텍스트에서 보존할 수 있습니다.

자세한 내용은 [Advanced eDiscovery에서 custodians 사용](managing-custodians.md)을 참조 하십시오.

### <a name="export"></a>내보내기

사용자는 역할을 사용 하 여 콘텐츠 검색의 결과를 로컬 컴퓨터로 내보낼 수 있습니다. 또한 고급 eDiscovery에서 분석에 대 한 검색 결과를 준비할 수 있습니다.

검색 결과를 내보내는 방법에 대 한 자세한 내용은 [Export search results From Security & 준수 센터](export-search-results.md)를 참조 하세요.

### <a name="hold"></a>Hold

사용자는이 역할을 사용 하 여 사서함, 공용 폴더, 사이트, 비즈니스용 Skype 대화 및 Microsoft 365 그룹에서 콘텐츠를 보류할 수 있습니다. 콘텐츠가 보존 되는 동안에는 콘텐츠 소유자가 원본 콘텐츠를 수정 하거나 삭제할 수는 있지만 보류를 제거 하거나 보존 기간이 만료 될 때까지 콘텐츠가 보존 됩니다.

보류에 대 한 자세한 내용은 다음 항목을 참조 하십시오.

- [핵심 eDiscovery에서 보류 만들기](create-ediscovery-holds.md) 

- [고급 eDiscovery에서 보류 만들기](add-custodians-to-case.md#step-4-place-custodians-on-hold)

### <a name="preview"></a>미리 보기

이 역할을 통해 사용자는 콘텐츠 검색에서 반환 된 항목의 목록을 볼 수 있습니다. 또한 목록에서 각 항목을 열고 해당 콘텐츠를 볼 수 있습니다.

### <a name="review"></a>검토

이 역할을 사용 하면 사용자가 [고급 ediscovery (클래식)](office-365-advanced-ediscovery.md) 에서 대/소문자 데이터를 액세스할 수 있습니다 ( *고급 ediscovery v1* 으로도 인식). 이 역할의 기본 목적은 사용자에 게 고급 eDiscovery (클래식)에 대 한 액세스 권한을 부여 하는 것입니다. 이 역할이 할당 된 사용자는 보안 & 준수 센터의 **eDiscovery** 페이지에 있는 사례 목록을 보고 열 수 있습니다. 사용자가 보안 & 준수 센터의 사례에 액세스 한 후 advanced **ediscovery로 전환을** 선택 하 여 고급 ediscovery (클래식)의 사례 데이터에 액세스 하 고 분석할 수 있습니다. 이 역할을 사용 하면 사용자가 사례와 연결 된 콘텐츠 검색의 결과를 미리 보거나 기타 콘텐츠 검색 또는 사례 관리 작업을 수행할 수 없습니다.

> [!NOTE]
> 현재 검토 역할을 할당 하거나 검토자 역할 그룹의 구성원 인 사용자는 Microsoft 365 ( *고급 ediscovery v 2.0* 이 라고도 함) [의 고급 ediscovery](overview-ediscovery-20.md) 데이터에 액세스할 수 없습니다. 사례 데이터를 검토할 수 있도록 Advanced eDiscovery v 2.0의 사례에 구성원을 추가 하려면 사용자가 eDiscovery 관리자 역할 그룹의 구성원 이어야 합니다.

### <a name="rms-decrypt"></a>RMS 암호 해독

사용자는이 역할을 사용 하 여 검색 결과를 미리 보고 암호 해독 된 권한으로 보호 되는 전자 메일 메시지를 내보낼 때 권한으로 보호 된 전자 메일 메시지 이 역할을 사용 하면 사용자가 eDiscovery 검색 결과에 포함 된 전자 메일 메시지에 암호화 된 파일을 첨부할 때 [Microsoft 암호화 기술로](encryption.md) 암호화 된 파일을 보고 내보낼 수도 있습니다. 또한 사용자는이 역할을 사용 하 여 고급 eDiscovery에서 검토 집합에 추가 된 암호화 된 전자 메일 첨부 파일을 검토 하 고 쿼리할 수 있습니다. EDiscovery의 암호 해독에 대 한 자세한 내용은 [Microsoft 365 eDiscovery 도구에서 암호 해독](ediscovery-decryption.md)를 참조 하세요.

### <a name="search-and-purge"></a>검색 및 제거

이 역할을 사용 하면 사용자가 콘텐츠 검색 조건과 일치 하는 데이터를 일괄적으로 제거할 수 있습니다. 자세한 내용은 [조직에서 전자 메일 메시지 검색 및 삭제](search-for-and-delete-messages-in-your-organization.md)를 참조 하세요.

## <a name="more-information"></a>추가 정보

- **eDiscovery 관리자를 만드는 이유** 앞에서 설명한 것처럼 eDiscovery 관리자는 조직의 모든 eDiscovery 사례를 보고 액세스할 수 있는 eDiscovery 관리자 역할 그룹의 구성원입니다. 모든 eDiscovery 사례에 액세스하는 이 기능에는 다음과 같은 두 가지 중요한 목적이 있습니다.

  - eDiscovery 사례의 유일한 구성원이 조직을 떠나면 조직 관리 역할 그룹의 구성원이나 eDiscovery 관리자 역할 그룹의 다른 구성원을 비롯한 어느 누구도 해당 eDiscovery 사례의 구성원이 아니므로 사례에 액세스할 수 없습니다. 이 상황에서는 해당 사례의 데이터에 액세스할 수 없습니다. 그러나 eDiscovery 관리자가 조직의 모든 eDiscovery 사례에 액세스할 수 있으므로 사례를 확인 하 고 해당 사례를 구성원으로 추가 하거나 다른 eDiscovery 관리자를 추가할 수 있습니다.

  - EDiscovery 관리자는 모든 핵심 eDiscovery 및 고급 eDiscovery 사례를 보고 액세스할 수 있으므로 모든 사례 및 관련 준수 검색을 감사 하 고 감독 할 수 있습니다. 이를 통해 준수 검색 또는 eDiscovery 사례의 오용을 방지할 수 있습니다. 또한 eDiscovery 관리자는 준수 검색 결과에서 잠재적으로 중요 한 정보에 액세스할 수 있으므로 eDiscovery 관리자 인 사용자 수를 제한 해야 합니다.

- **그룹을 eDiscovery 관리자 역할 그룹의 구성원으로 추가할 수 있나요?** 앞에서 설명한 것 처럼, Security & 준수 센터 PowerShell의 **추가 기능 그룹 구성원** cmdlet을 사용 하 여 ediscovery 관리자 역할 그룹에서 메일 사용이 가능한 보안 그룹의 구성원으로이를 추가할 수 있습니다. 예를 들어 다음 명령을 실행 하 여 eDiscovery 관리자 역할 그룹에 메일 사용이 가능한 보안 그룹을 추가할 수 있습니다. 

  ```powershell
  Add-RoleGroupMember "eDiscovery Manager" -Member <name of security group>
  ```

    Exchange 메일 그룹 및 Microsoft 365 그룹은 지원 되지 않습니다. 명령을 사용 하 여 Exchange Online PowerShell에서 만들 수 있는 메일 사용이 가능한 보안 그룹을 사용 해야 합니다 `New-DistributionGroup -Type Security` . 또한 Exchange 관리 센터 또는 Microsoft 365 관리 센터에서 메일 사용이 가능한 보안 그룹을 만들고 구성원을 추가할 수 있습니다. 새 메일 사용이 가능한 보안을 eDiscovery 관리자 역할 그룹에 추가할 수 있도록 만든 후 최대 60 분까지 걸릴 수 있습니다. 

    또한 앞에서 설명한 것 처럼 보안 & 준수 센터 PowerShell에서 **eDiscoveryCaseAdmin** cmdlet을 사용 하 여 메일 사용이 가능한 보안 그룹을 eDiscovery 관리자로 설정할 수 없습니다. 개별 사용자만 eDiscovery 관리자로 추가할 수 있습니다.

    또한 메일 사용이 가능한 보안 그룹을 사례 구성원으로 추가할 수 없습니다.
