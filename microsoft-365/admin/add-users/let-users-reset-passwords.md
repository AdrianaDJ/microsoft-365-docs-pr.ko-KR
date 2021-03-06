---
title: 사용자가 암호를 직접 재설정할 수 있도록 허용
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- TRN_M365B
- OKR_SMB_Videos
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 5bc3f460-13cc-48c0-abd6-b80bae72d04a
description: 셀프 서비스 암호 재설정 도구를 사용 하 여 암호를 다시 설정 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: bbde517858186d844412aca21f231620ed76496a
ms.sourcegitcommit: 38d828ae8d4350ae774a939c8decf30cb36c3bea
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49551923"
---
# <a name="let-users-reset-their-own-passwords"></a>사용자가 암호를 직접 재설정할 수 있도록 허용

Microsoft 365 관리자는 사용자가 [셀프 서비스 암호 다시 설정 도구](https://go.microsoft.com/fwlink/p/?LinkId=522677) 를 사용 하 여 암호를 다시 설정할 필요가 없도록 할 수 있습니다. 관리자의 업무를 덜 수 있습니다!
  
## <a name="before-you-begin"></a>시작하기 전에
  
- Microsoft 365 비즈니스, 교육 또는 비영리 유료 요금제를 사용 하 여 클라우드 사용자에 대 한 셀프 서비스 암호 재설정을 **사용할** 수 있습니다. Microsoft 365 평가판에서는 작동 하지 않습니다.

- Azure를 사용합니다. 이러한 단계를 수행할 때 자동으로 Azure의 이 기능을 **무료** 로 이용할 수 있습니다. 다른 Azure 기능을 사용하지 않으면 셀프 서비스 암호 재설정을 사용하는 비용이 부과되지 않습니다.

- **온-프레미스 Active Directory를 사용** 하는 경우 위의 두 지점이 적용 되지 않습니다. 대신이를 설정할 수는 있지만 **AZURE AD Premium에 대 한 유료 구독을 사용 해야** 합니다.

회사, 학교 또는 비영리용 암호 만료 정책을 설정하는 사용자를 위한 문서입니다. 이 단계를 완료하려면 Microsoft 365 관리자 계정으로 로그인해야 합니다. [관리자 계정 이란?](../admin-overview/admin-overview.md)

이 단계를 수행 하려면 [전역 관리자 또는 암호 관리자](about-admin-roles.md) 여야 합니다.

## <a name="watch-let-users-reset-their-own-passwords"></a>시청: 사용자가 자신의 암호를 다시 설정할 수 있도록 허용

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3AY8S]

이 비디오가 도움이 된 경우에는 [소규모 비즈니스와 Microsoft 365를 처음 사용하는 사용자를 위한 완전한 교육 시리즈](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)를 참조하세요.

## <a name="steps-let-people-reset-their-own-passwords"></a>단계: 사용자가 자신의 암호를 다시 설정할 수도 있습니다.

다음 단계에서는 비즈니스의 모든 사용자에 대해 셀프 서비스 암호 재설정을 켭니다.
  
::: moniker range="o365-worldwide"

1. <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">관리 센터</a>에서 조직 설정 **설정** > **Org settings** 페이지로 이동 합니다.

::: moniker-end

::: moniker range="o365-germany"

1. <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">관리 센터</a>에서 **설정** \> **보안 &amp; 개인 정보** 페이지로 이동 합니다.

::: moniker-end

::: moniker range="o365-21vianet"

1. <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">관리 센터</a>에서 **설정** \> **설정** \> **보안 &amp; 개인 정보** 페이지로 이동 합니다.

::: moniker-end

2. **조직 설정** 페이지 맨 위에서 **보안 & 개인 정보 보호** 탭을 선택 합니다.
  
3. **셀프 서비스 암호 재설정** 을 선택 합니다.

4. **셀프 서비스 암호 재설정** 에서 **Azure portal로 이동을 선택 하 여 셀프 서비스 암호 재설정을 켭니다**.

5. 왼쪽 탐색 창에서 **사용자** 를 선택 하 고 **사용자 | 모든 사용자** 페이지에서 **암호 재설정** 을 선택 합니다.
  
6. **속성** 페이지에서 **모두** 를 선택 하 여 회사의 모든 사용자에 대해 사용 하도록 설정 하 고 **저장** 을 선택 합니다.
  
7. 사용자가 로그인 하면 나중에 암호를 다시 설정 하는 데 도움이 되는 추가 연락처 정보를 입력 하 라는 메시지가 표시 됩니다.

## <a name="related-content"></a>관련 콘텐츠

[조직의 암호 만료 정책 설정](../manage/set-password-expiration-policy.md)

[개별 사용자 암호가 만료되지 않도록 설정](set-password-to-never-expire.md)

[Microsoft 365 Business 교육 비디오](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)
