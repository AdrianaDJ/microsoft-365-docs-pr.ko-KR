---
title: 결제 방법 관리
f1.keywords:
- CSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- commerce
ms.custom:
- TopSMBIssues
- okr_SMB
- AdminSurgePortfolio
search.appverid:
- MET150
description: Microsoft 365 관리 센터에서 결제 방법을 관리 하는 방법에 대해 알아봅니다.
ms.date: ''
ms.openlocfilehash: 81c7509fb2f3be982890ec6b68dafb83ff0c1876
ms.sourcegitcommit: 25afc0c34edc7f8a5eb389d8c701175256c58ec8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "47324237"
---
# <a name="manage-payment-methods"></a>결제 방법 관리

::: moniker range="o365-21vianet"
> [!NOTE]
> 관리 센터가 변경되고 있습니다. 사용자의 환경이 여기에 설명된 세부 정보와 맞지 않는 경우에는 [새 Microsoft 365 관리 센터 정보](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet)를 참조하세요.
::: moniker-end

Microsoft에서 비즈니스 제품 또는 서비스를 구매할 때 기존 결제 방법을 사용 하거나 새 지불 방법을 추가할 수 있습니다. 신용 또는 직불 카드 또는 은행 계좌를 사용 하 여 구매 하는 항목에 대 한 요금을 지불할 수 있습니다.

비즈니스 계정에 대금 청구 프로필이 있고 대금 청구 프로필 소유자 또는 대금 청구 프로필 참가자 인 경우 신용 카드 또는 송장 지불로 지원 되는 대금 청구 프로필을 사용 하 여 구매 또는 지불 명세서를 만들 수 있습니다. 청구 송장 관리자는 대금 청구 프로필만 사용 하 여 자재 명세서를 지불할 수 있습니다. 대금 청구 프로필 및 역할에 대 한 자세한 내용은 [청구 프로필 관리](manage-billing-profiles.md)를 참조 하세요.

비즈니스 계정에 대금 청구 프로필이 없는 경우 전역 또는 대금 청구 관리자는 비즈니스 계정에 추가 된 모든 은행 계정을 관리 하 고 사용할 수 있습니다. 그러나 추가한 신용 카드만 관리 하거나 사용할 수 있습니다.

> [!NOTE]
> 일부 국가나 지역에서는 은행 계좌 결제 옵션을 사용할 수 없습니다.
>
> 테 넌 트와 동일한 국가에서 발급 된 결제 방법을 사용 해야 합니다.

## <a name="before-you-begin"></a>시작하기 전에

이 문서의 작업을 수행 하려면 전역 또는 대금 청구 관리자 여야 합니다. 자세한 내용은 [관리자 역할 정보](../../admin/add-users/about-admin-roles.md)를 참조하세요.

## <a name="add-a-payment-method"></a>결제 방법 추가

결제 방법을 추가 해도 구독이 연결 되지 않습니다. 지불 방법에 대해 단일 구독을 할당 하려면 [단일 구독에 대 한 결제 방법 변경을](#change-a-payment-method-for-a-single-subscription)참조 하십시오. 다른 결제 방법을 사용 하는 모든 구독을 새 것으로 바꾸려면 [결제 방법 바꾸기를](#replace-a-payment-method)참조 하세요.

1. 관리 센터에서 **청구**  >  **금액 & 지불**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">지불 방법</a> 페이지로 이동 합니다.
2. **결제 방법 추가**를 선택합니다.
3. **결제 방법** 페이지의 드롭다운 메뉴에서 결제 방법을 선택합니다.
4. 새 카드나 은행 계좌에 대 한 정보를 입력 하 고 **추가**를 선택 합니다.

## <a name="update-payment-method-details"></a>결제 방법 세부 정보 업데이트

기존 결제 방법의 신용 또는 직불 카드, 대금 청구 주소 또는 만료 날짜에 대 한 이름을 변경할 수 있습니다. 그러나 카드나 계정 번호는 변경할 수 없습니다. 계정 번호가 변경 된 경우에는 [해당 번호를 다른 결제 방법으로 바꾼](#replace-a-payment-method)다음 [이전 항목을 삭제](#delete-a-payment-method)합니다.

1. 관리 센터에서 **청구**  >  **금액 & 지불**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">지불 방법</a> 페이지로 이동 합니다.
2. 업데이트할 결제 방법의 행을 선택 합니다. 오른쪽 창에서 **편집**을 선택 합니다.
3. 신용, 직불 카드, 대금 청구 주소, 만료 날짜 등의 결제 방법 정보를 업데이트 한 다음 **저장**을 선택 합니다.

## <a name="replace-a-payment-method"></a>결제 방법 바꾸기

결제 방법을 바꾸면 같은 결제 방법을 사용 하는 모든 구독 및 대금 청구 프로필에 대해 교체 됩니다. 결제 방법을 바꾸면 기존 결제 방법이 삭제 되지 않습니다. 다른 구독 및 대금 청구 프로필에 대해 계속 해 서 선택 하 여 사용할 수 있습니다.

단일 구독에 대 한 결제 방법을 변경 하려면 [단일 구독에 대 한 결제 방법 변경을](#change-a-payment-method-for-a-single-subscription)참조 하십시오.

1. 관리 센터에서 **청구**  >  **금액 & 지불**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">지불 방법</a> 페이지로 이동 합니다.
2. 바꿀 지불 방법의 행을 선택 합니다. 오른쪽 창에는 선택한 결제 방법을 사용 하는 모든 청구 프로필 및 개별 구독이 나열 됩니다.
3. 오른쪽 창에서 **모든 항목에 대 한 결제 방법 바꾸기를**선택 합니다.
4. 기존 결제 방법을 사용 하려면 드롭다운 목록에서 항목을 선택 하 고 **바꾸기를**선택 합니다.
    > [!NOTE]
    > 청구 프로필과 연결 된 구독이 있는 경우 신용 또는 직불 카드만 사용 하 여 요금을 지불할 수 있습니다. **결제 방법** 페이지에 나열 된 은행 계좌는 드롭다운 목록에서 선택할 수 없습니다.
5. 새 결제 방법을 추가 하려면 **지불 방법 추가**를 선택 합니다.
6. **결제 방법 추가** 창에서 계정 정보를 입력 한 다음 **저장**을 선택 합니다. 테 넌 트와 동일한 국가의 결제 방법을 사용 해야 합니다.
7. 드롭다운 목록에서 새 결제 방법이 이미 선택 되어 있습니다. **바꾸기를**선택 합니다.

## <a name="change-a-payment-method-for-a-single-subscription"></a>단일 구독에 대 한 결제 방법 변경

단일 구독에 대해 요금을 지불 하는 데 사용 되는 결제 방법을 변경할 수 있습니다.

1. 관리 센터에서 **Billing**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">제품</a> 청구 페이지로 이동 합니다.
2. **제품** 탭에서 대체 결제 방법으로 결제 하려는 구독을 찾습니다.
3. **기타 작업** (점 3 개)을 선택 하 고 **결제 방법 바꾸기를**선택 합니다.
4. **결제 방법 바꾸기** 창의 드롭다운 목록에서 대체 결제 방법을 선택 하거나 결제 방법 추가를 선택 합니다.
5. 결제 방법을 추가 하는 경우 카드 또는 계정 세부 정보를 입력 한 다음 **저장**을 선택 합니다.
6. 선택한 결제 방법이 올바른지 확인 한 다음 **바꾸기를**선택 합니다.

## <a name="delete-a-payment-method"></a>결제 방법 삭제

구독 또는 대금 청구 프로필에 연결 되지 않은 결제 방법만 삭제할 수 있습니다. 이는 모든 구독 상태에 적용 됩니다.

### <a name="delete-a-payment-method-with-no-subscriptions-or-billing-profiles-attached"></a>구독 또는 대금 청구 프로필을 연결 하지 않은 결제 방법 삭제

결제 방법이 구독 또는 대금 청구 프로필과 연결 되어 있지 않으면 즉시 삭제할 수 있습니다.

1. 관리 센터에서 **청구**  >  **금액 & 지불**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">지불 방법</a> 페이지로 이동 합니다.
2. 삭제할 결제 방법을 찾은 다음 3 개의 점을 선택 하 고 **삭제**를 선택 합니다.
3. 오른쪽 창 맨 아래에서 **삭제**를 선택 합니다.

### <a name="delete-a-payment-method-with-subscriptions-or-billing-profiles-attached"></a>구독 또는 대금 청구 프로필을 연결 하 여 결제 방법 삭제

결제 방법이 구독 또는 대금 청구 프로필에 첨부 된 경우 먼저 기존 결제 방법으로 교체 하거나 새 결제 방법을 추가 합니다.

1. 관리 센터에서 **청구**  >  **금액 & 지불**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">지불 방법</a> 페이지로 이동 합니다.
2. 삭제할 지불 방법의 행을 선택 합니다. 오른쪽 창에는 해당 결제 방법을 사용 하는 기존 구독이 나열 됩니다.
3. 오른쪽 창에서 **삭제**를 선택 합니다.
4. 기존 결제 방법을 사용 하려면 드롭다운 목록에서 **다음**을 선택 하 고 **삭제**를 선택 합니다.
    > [!NOTE]
    > 청구 프로필과 연결 된 구독이 있는 경우 신용 카드로 결제 하는 경우에만 해당 구독을 사용할 수 있습니다. **결제 방법** 페이지에 나열 된 은행 계좌는 드롭다운 목록에서 선택할 수 없습니다.
5. 새 결제 방법을 추가 하려면 **지불 방법 추가**를 선택 합니다.
6. 추가 하려는 결제 방법의 유형을 선택 하 고 계정 정보를 입력 한 다음 **저장**을 선택 합니다.
7. 드롭다운 목록에서 새 결제 방법이 이미 선택 되어 있습니다. **다음**을 선택합니다.
8. **삭제**를 선택합니다.

## <a name="troubleshoot-payment-methods"></a>결제 방법 문제 해결

|**문제**|**문제 해결 단계**|
|:----------|:-----|
|**"브라우저가 현재 쿠키를 차단 하도록 설정 되어 있습니다." 라는 오류 메시지가 표시 됩니다.** |타사 쿠키를 허용하도록 브라우저를 설정하고 다시 시도하세요. |
|**내 신용 카드 또는 직불 카드가 거절 되었습니다.** |신용 카드 또는 직불 카드로 결제 하는 경우 카드가 거절 되 면 Microsoft에서 해당 결제를 처리할 수 없음을 알리는 전자 메일을 받게 됩니다. 카드 정보 &mdash; 카드 번호, 만료 날짜, 카드의 이름, 주소, 구/군/시, 시/도 및 우편 번호를 포함 하는 주소가 &mdash; 카드와 명령문에서 수행 하는 것과 정확히 동일 하 게 나타나는지 확인 합니다. 구독 세부 정보 페이지의 청구 섹션에 있는 **임금** **잔액** 링크를 사용 하 여 카드 정보를 업데이트 하 고 대금을 즉시 제출할 수 있습니다. 자세한 내용은 다음을 참조 하세요. [신용 카드를 거절 했 고 결제 기한이 경과 된 경우](pay-for-your-subscription.md#what-if-my-credit-card-was-declined-and-my-payment-is-past-due)  <br/><br/>  "거부 됨" 메시지가 계속 표시 되 면 해당 은행에 문의 하세요. 사용자의 카드가 활성 상태가 아닐 수 있습니다. 최근 만료 날짜를 사용 하 여 메일에서 카드를 받은 경우 해당 사용자가 활성화 되었는지 확인 합니다. 또한 은행에서 온라인, 국제 또는 되풀이 되는 거래에 대해 카드가 승인 되지 않은 경우를 확인할 수 있습니다. |
|**카드나 은행 계좌 번호를 업데이트 하려고 합니다.** |기존 결제 방법에서는 카드나 계정 번호를 변경할 수 없습니다. 카드나 계정 번호가 변경 된 경우 지불 방법에서 새 구독으로 이동 하는 [다른 결제 방법으로 바꾼](#replace-a-payment-method)다음 [이전 결제 방법을 삭제](#delete-a-payment-method-with-no-subscriptions-or-billing-profiles-attached)합니다. |
|**내 계정에 카드 또는 은행 계정이 하나 뿐 이며 제거 하려고 합니다.** |결제 방법이 하나인 경우에는 삭제 하기 전에 [새 결제 방법으로 교체](#replace-a-payment-method) 해야 합니다. |
|**내 카드 또는 은행 계좌를 추가할 수 없습니다.**  |테 넌 트와 동일한 국가에서 발급 된 결제 방법을 사용 해야 합니다. 카드 또는 은행 계좌 정보를 입력 하는 데 문제가 있는 경우 [지원 서비스에 문의할](../../admin/contact-support-for-business-products.md)수 있습니다. |

## <a name="related-content"></a>관련 콘텐츠

[비즈니스 구독 결제](pay-for-your-subscription.md) (문서) \
[청구 프로필 관리](manage-billing-profiles.md) (문서) \
[청구 주기 변경](change-payment-frequency.md) (문서)