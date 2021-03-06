---
title: 관리자 (셀프 서비스 구입) 관리
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- commerce
ms.custom: AdminSurgePortfolio
search.appverid:
- MET150
description: 관리자는 조직의 사용자가 만든 셀프 서비스 구매를 관리 하는 방법을 확인할 수 있습니다.
ms.openlocfilehash: ca25bf0c3e3539196e81dcc289592028cc4dfa47
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47546677"
---
# <a name="manage-self-service-purchases-admin"></a>셀프 서비스 구매(관리자) 관리

::: moniker range="o365-21vianet"

> [!NOTE]
> 관리 센터가 변경되고 있습니다. 사용자의 환경이 여기에 설명된 세부 정보와 맞지 않는 경우에는 [새 Microsoft 365 관리 센터 정보](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet)를 참조하세요.

::: moniker-end

관리자는 조직의 사용자가 만든 셀프 서비스 구매를 볼 수 있습니다. 제품 이름, 구매자 이름, 구독 구입, 만료 날짜, 구입 가격 및 각 셀프 서비스 구매에 대 한 사용자 지정이 표시 됩니다. 조직에서 필요한 경우 PowerShell을 통해 제품별로 셀프 서비스 구매를 해제할 수 있습니다. 셀프 서비스 구매 나 중앙을 통해 구매한 제품에 대해 동일한 데이터 관리 및 액세스 정책을 사용 합니다.

조직의 사용자가 셀프 서비스 구매를 수행할 수 있는지 여부를 제어할 수도 있습니다. 자세한 내용은 [Use AllowSelfServicePurchase for The MSCommerce PowerShell module](allowselfservicepurchase-powershell.md)을 참조 하십시오.

## <a name="view-self-service-subscriptions"></a>셀프 서비스 구독 보기

1. 관리 센터에서 **Billing**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">제품</a> 청구 페이지로 이동 합니다.
2. **제품** 탭에서 필터 아이콘을 선택한 다음 **셀프 서비스**를 선택 합니다.
3. 구독에 대 한 세부 정보를 보려면 목록에서 하나를 선택 합니다.

## <a name="view-who-has-licenses-for-a-self-service-purchase-subscription"></a>셀프 서비스 구매 구독 라이선스를 가진 사용자 보기

1. 관리 센터에서 **청구**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">라이선스</a> 페이지로 이동 합니다.
2. 필터 아이콘을 선택한 다음 **셀프 서비스**를 선택 합니다.
3. 사용자에 게 할당 된 라이선스를 볼 제품을 선택 합니다.
    > [!NOTE]
    > 제품에 대 한 구매를 여러 개 사용 하는 경우 해당 제품이 한 번만 나열 되며 **사용 가능한 수량** 열에 해당 제품에 대해 구매한 모든 구독의 합계가 표시 됩니다.
4. **사용자** 목록은 셀프 서비스 구매를 수행한 사용자 이름별로 그룹화 됩니다.
5. 이러한 구독에 대 한 라이선스가 있는 사용자 목록을 내보내려면 내보낼 구독을 선택 하 고 **사용자 내보내기를**선택 합니다.

## <a name="disable-or-enable-self-service-purchases"></a>셀프 서비스 구매 사용 또는 사용 안 함

조직의 사용자에 대해 셀프 서비스 구매를 사용 하지 않도록 설정 하거나 사용 하도록 설정할 수 있습니다. **MSCommerce** PowerShell 모듈에는 조직의 사용자가 셀프 서비스 구매를 수행할 수 있는지 여부 및 해당 제품에 **대 한 정책에 대** 한 **policyid** 매개 변수 값이 포함 되어 있습니다.

**MSCommerce** PowerShell 모듈을 사용 하 여 다음을 수행할 수 있습니다.

- 제품에서 사용 하거나 사용 하지 않도록 설정 되었는지 여부에 관계 없이 **AllowSelfServicePurchase** 매개 변수 값의 기본 상태를 확인 합니다.
- 해당 하는 제품 목록 및 셀프 서비스 구매가 사용 하도록 설정 되었는지 여부 확인
- 특정 제품에 대 한 현재 설정을 보거나 수정 하 여 사용 하거나 사용 하지 않도록 설정

자세한 내용은 [Use AllowSelfServicePurchase for The MSCommerce PowerShell module](allowselfservicepurchase-powershell.md)을 참조 하십시오.

## <a name="centralize-licenses-under-a-single-subscription"></a>단일 구독을 통해 라이선스 중앙 집중화

기존 라이선스를 할당 하거나 셀프 서비스 구매에 할당 된 사용자에 대 한 기존 계약을 통해 추가 구독을 구매할 수 있습니다. 이러한 중앙에서 구매한 라이선스를 할당 한 후에는 purchasers에서 기존 구독을 취소 하도록 요청할 수 있습니다.

1. 관리 센터에서 **결제** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">구매 서비스</a> 페이지로 이동 합니다.
2. 구매할 제품을 찾아 선택한 다음 **구입**을 선택 합니다.
3. 나머지 단계를 완료 하 여 구매를 완료 합니다.
4. 보기의 단계에 따라 [셀프 서비스를 구매한 구독에 대 한 라이선스를 가진](#view-who-has-licenses-for-a-self-service-purchase-subscription) 사용자의 목록을 내보내 다음 단계에서 참조로 사용할 수 있습니다.
5. 다른 구독에 라이선스가 있는 모든 사용자에 게 라이선스를 할당 합니다. 전체 단계는 [사용자에 게 라이선스 할당](../../admin/manage/assign-licenses-to-users.md)을 참조 하세요.
6. 셀프 서비스 구매 구독을 구매한 사용자에 게 문의 하 여 [취소](manage-self-service-purchases-users.md#cancel-a-subscription)하도록 요청 합니다.

## <a name="take-over-a-self-service-purchase-subscription"></a>셀프 서비스 구매 구독 사용

조직의 사용자가 만든 셀프 서비스 구매 구독을 사용할 수 있습니다. 셀프 서비스 구매 구독을 사용 하는 경우 다음 두 가지 옵션을 사용할 수 있습니다.

1. 사용자를 다른 구독으로 이동 하 고 원래 구독을 취소 합니다.
2. 셀프 서비스 구매 구독을 취소 하 고 할당 된 사용자 로부터 라이선스를 제거 합니다.

### <a name="move-users-to-a-different-subscription"></a>다른 구독으로 사용자 이동

사용자를 다른 구독으로 이동 하면 이전 구독이 자동으로 취소 됩니다. 최초 셀프 서비스 구매 구독을 구매한 사용자에 게 구독이 취소 되었음을 알리는 전자 메일을 받습니다.

> [!NOTE]
> 사용자를 이동 하는 구독에서 이동할 각 사용자에 대해 사용 가능한 라이선스가 있어야 합니다.

1. 관리 센터에서 **Billing**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">제품</a> 청구 페이지로 이동 합니다.
2. **제품** 탭에서 필터 아이콘을 선택한 다음 **셀프 서비스**를 선택 합니다.
3. 수행 하려는 구독을 선택 합니다.
4. 구독 정보 페이지의 **구독 및 설정** 섹션에서 **이 구독에 대 한 제어권 적용**을 선택 합니다.
5. 오른쪽 창에서 **사용자 이동을**선택 합니다.
6. 사용자를 이동할 대상 제품을 선택 하 고 **사용자 이동을**선택 합니다.
7. **사용자 이동** 상자에서 **사용자 이동을**선택 합니다. 이동 프로세스는 몇 분 정도 걸릴 수 있습니다. 프로세스를 실행 하는 동안 브라우저를 닫지 마세요.
8. 이동 프로세스가 완료 되 면 **이동 완료 창을**닫습니다.
9. 구독 정보 페이지에는 셀프 서비스를 구매한 구독의 **구독 상태가** **삭제**됨으로 표시 됩니다.

### <a name="cancel-a-self-service-purchase-subscription"></a>셀프 서비스 구매 구독 취소

셀프 서비스 구매 구독을 취소 하도록 선택 하면 라이선스가 있는 사용자가 제품에 액세스할 수 없게 됩니다. 최초 셀프 서비스 구매 구독을 구매한 사용자에 게 구독이 취소 되었음을 알리는 전자 메일을 받습니다.

1. 관리 센터에서 **Billing**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">제품</a> 청구 페이지로 이동 합니다.
2. **제품** 탭에서 필터 아이콘을 선택한 다음 **셀프 서비스**를 선택 합니다.
3. 취소할 구독을 선택 합니다.
4. 구독 정보 페이지의 **구독 및 설정** 섹션에서 **이 구독에 대 한 제어권 적용**을 선택 합니다.
5. 오른쪽 창에서 **구독 취소**를 선택 합니다.
6. 드롭다운 목록에서 취소에 대 한 이유를 선택한 다음 **구독 취소**를 선택 합니다.
7. 취소 하 시겠습니까 **?** 상자에서 **구독 취소**를 선택 합니다.
8. 오른쪽 창을 닫습니다.
9. 구독 정보 페이지에서 **구독 상태가** **삭제**됨으로 표시 됩니다.

## <a name="need-help-contact-us"></a>도움이 필요하신가요? 문의처.

셀프 서비스 구매에 대 한 일반적인 질문은 [셀프 서비스 구매 FAQ](self-service-purchase-faq.md)를 참조 하세요.

궁금한 사항이 있거나 셀프 서비스 구매에 도움이 필요한 경우 [고객 지원에 문의 하세요](../../admin/contact-support-for-business-products.md).