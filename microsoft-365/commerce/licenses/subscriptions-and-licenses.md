---
title: 비즈니스용 Office 365의 구독 및 라이선스 이해
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- commerce
search.appverid:
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 7ac93507-0e38-4398-8bfe-9c1d123cb387
description: '비즈니스용 Office 365의 구독 및 라이선스에 대해 알아보고 라이선스를 할당할 수 있는 사람 및 사용자에 게 라이선스를 할당할 때 수행 되는 작업을 파악 합니다. '
ms.custom: okr_SMB
ms.openlocfilehash: 1a90e4b80322ad075f2149801aebd02ac07a2aef
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42246349"
---
# <a name="understand-subscriptions-and-licenses-in-office-365-for-business"></a>비즈니스용 Office 365의 구독 및 라이선스 이해

이 문서에서는 구독 및 라이선스 간의 관계에 대해 설명 하 고, 라이선스를 [할당할 수 있는 사람](#find-out-who-can-assign-licenses), 사용자 [에 게 라이선스를 할당할 때 수행 되는 작업](#understand-what-happens-when-you-assign-a-license-to-someone)및 [사용자가 Office를 설치할 수 있는 장치 개수](#how-many-devices-can-people-install-office-on)에 대 한 추가 정보를 제공 합니다. 또한 [비 사용자 사서함의 라이선스 이해](#understand-licenses-for-non-user-mailboxes)에 대 한 링크와 [라이선스 관리에 대 한 문서](#articles-about-managing-licenses)도 포함 되어 있습니다.
  
비즈니스용 Office 365에 대 한 구독을 구입할 때 매월 또는 연간 기준으로 지불 하는 응용 프로그램 및 서비스 집합에 등록 합니다. 구독의 일부로 수신 하는 응용 프로그램 및 서비스는 구입한 제품 (예: Office 365 Business 또는 Office 365 Business Premium)에 따라 달라 집니다. [Office 구입 365 페이지](https://products.office.com/compare-all-microsoft-office-products?&activetab=tab:primaryr1)에서 각 제품과 함께 제공 되는 내용을 검토할 수 있습니다. 

구독을 구입할 때 조직의 사용자 수를 기준으로 필요한 라이선스 수를 지정합니다. 구입을 완료한 후 사용자 계정을 만들고 각 사용자에게 라이선스를 할당합니다. 조직의 요구 사항이 변경 되 면 새 사용자를 수용할 수 있는 라이선스를 추가로 구입 하거나 다른 사용자에 게 라이선스를 다시 할당 합니다. 

구독이 두 개 이상 있는 경우 각 구독에 대해 다른 사용자에게 라이선스를 할당할 수 있습니다. 예를 들어 모든 사용자가 Office 365 Business Premium 구독의 일부로 모든 Office 365 응용 프로그램 및 서비스에 할당 될 수 있지만, 사용자의 하위 집합은 별도의 Visio 구독을 통해 Visio Online에 할당 될 수도 있습니다. 

  
## <a name="find-out-who-can-assign-licenses"></a>라이선스를 할당할 수 있는 사용자 찾기

여러 유형의 관리자가 해당 역할에 따라 서로 다른 방법으로 라이선스를 사용할 수 있습니다. 다음 표에는 가장 일반적인 옵션이 나열되어 있습니다. 관리자 역할 및 권한의 전체 목록은 [관리자 역할 정보](../../admin/add-users/about-admin-roles.md)를 참조하세요.
  
|**관리자 역할**|**라이선스 할당**|**라이선스 제거**|**추가 라이선스 구입**|**계정 삭제**|
|:-----|:-----|:-----|:-----|:-----|
|전역 관리자  <br/> |예  <br/> |예  <br/> |예  <br/> |예  <br/> |
|대금 청구 관리자  <br/> |아니요  <br/> |아니요  <br/> |예  <br/> |아니요  <br/> |
|사용자 관리 관리자  <br/> |예  <br/> |예  <br/> |아니요  <br/> |예  <br/> |
|서비스 관리자  <br/> |아니요  <br/> |아니요  <br/> |아니요  <br/> |아니요  <br/> |
|암호 관리자  <br/> |아니요  <br/> |아니요  <br/> |아니요  <br/> |아니요  <br/> |
   
## <a name="understand-what-happens-when-you-assign-a-license-to-someone"></a>사용자에게 라이선스를 할당할 때 발생하는 사항 이해

다음 표에는 사용자에게 라이선스를 할당할 때 자동으로 발생하는 일이 나와 있습니다.
  
|**구독에 이 서비스가 있는 경우**|**자동으로 일어나는 일**|
|:-----|:-----|
|Exchange Online  <br/> |해당 사용자의 사서함이 만들어집니다.  <br/> |
|SharePoint Online  <br/> |기본 SharePoint Online 팀 사이트에 대한 편집 권한이 해당 사용자에게 할당됩니다.  <br/> |
|비즈니스용 Skype Online  <br/> |사용자가 라이선스 관련 기능에 액세스할 수 있습니다.  <br/> |
|Office 365 ProPlus  <br/> |사용자는 조직의 최대 5대의 Mac 또는 PC, 최대 5대의 태블릿, 최대 5대의 스마트폰에 Microsoft Office를 다운로드할 수 있습니다.  <br/> |
   
## <a name="how-many-devices-can-people-install-office-on"></a>사용자가 Office를 설치할 수 있는 장치는 몇 개인가요?

구독에 다음 제품이 포함되는 경우 각 사용자는 최대 5대의 PC 또는 Mac, 최대 5대의 태블릿, 최대 5대의 전화기에 Office를 설치할 수 있습니다.
  
- Office 365 Business
    
- Office 365 Business Premium
    
- Office 365 ProPlus
    
- Office 365 Enterprise E3
    
- Office 365 Enterprise E5
    
## <a name="understand-licenses-for-non-user-mailboxes"></a>비사용자 사서함의 라이선스 이해

리소스 사서함, 대화방 사서함, 공유 사서함이 50GB(기가바이트)의 저장소 할당량을 초과할 경우를 제외하고, 해당 사서함에 라이선스를 할당할 필요가 없습니다. 비사용자 사서함에 대해서는 다음 문서를 참조하세요.
  
- [공유 사서함 만들기](../../admin/email/create-a-shared-mailbox.md)
    
- [Exchange Online의 공유 사서함](https://go.microsoft.com/fwlink/p/?linkid=847433)(다른 모든 Office 365 요금제용) 
    
- [대화방 사서함 만들기 및 관리](https://go.microsoft.com/fwlink/p/?linkid=847434)
    
- [장비 사서함 관리](https://go.microsoft.com/fwlink/p/?linkid=847435)
    
## <a name="articles-about-managing-licenses"></a>라이선스 관리에 대 한 문서

- [사용자에게 라이선스 할당](../../admin/manage/assign-licenses-to-users.md)
    
- [사용자의 라이선스 제거](../../admin/manage/remove-licenses-from-users.md)
    
- [구독용 라이선스 구매](buy-licenses.md)
    
- [다른 구독 구입](../buy-another-subscription.md)
    
- [추가 기능 구입 또는 편집](../buy-or-edit-an-add-on.md)
    
- [구독에서 라이선스 제거](remove-licenses-from-subscription.md)
    
- [라이선스 충돌 해결](../../admin/manage/resolve-license-conflicts.md)
    
- [Yammer 사용자 라이선스 관리](https://docs.microsoft.com/yammer/manage-yammer-users/manage-yammer-licenses-in-office-365)