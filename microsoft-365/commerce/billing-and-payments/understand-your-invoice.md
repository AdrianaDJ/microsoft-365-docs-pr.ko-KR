---
title: 청구서 또는 송장 이해하기
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
f1_keywords:
- MACBillingBillsPaymentsInvoices
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- commerce
ms.custom: AdminSurgePortfolio
search.appverid:
- MET150
description: Microsoft 비즈니스 제품에 대 한 청구서 또는 송장을 읽고 이해 하는 방법에 대해 알아보세요.
keywords: 청구 계정, 조직 정보, 송장
ms.openlocfilehash: 80b7e4f14390e2f695dc753358f9e5bebe055bd0
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48638414"
---
# <a name="understand-your-bill-or-invoice"></a>청구서 또는 송장 이해하기

::: moniker range="o365-21vianet"

> [!NOTE]
> 관리 센터가 변경되고 있습니다. 사용자의 환경이 여기에 설명된 세부 정보와 맞지 않는 경우에는 [새 Microsoft 365 관리 센터 정보](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet)를 참조하세요.

::: moniker-end

송장에서는 결제에 대 한 요금 및 지침을 요약해 서 제공 합니다. Microsoft 365 관리 센터에서 [온라인 송장을 볼](#view-your-online-invoice) 수 있습니다. 또한이 파일을 휴대용 문서 형식 (.pdf)으로 다운로드 하 여 전자 메일을 통해 보낼 수 있습니다.

Microsoft 365 구독만 있는 경우 [microsoft 365 for business의 청구서 또는 송장 이해](understand-your-invoice2.md)를 참조 하세요.

## <a name="understand-the-invoice-header"></a>송장 헤더 이해

첫 페이지의 맨 위에는 결제를 담당 하는 사람, 청구서가 전송 되는 위치 및 청구 비용이 요약 되어 있습니다.

| 용어 | 설명 |
| --- | --- |
| 판매 대상 |지불을 담당 하는 법률 엔터티의 이름과 주소를 식별 하는 청구 계정입니다. 이 정보는 계정 계약을 찾고 역할 및 사용 권한을 관리할 수 있는 <a href="https://go.microsoft.com/fwlink/p/?linkid=2084771" target="_blank">청구 계정</a> 페이지에서 관리할 수 있습니다. |
| 청구지 |송장을 받는 사람을 식별 합니다. 이 정보는 <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">청구 프로필</a> 페이지에서 관리할 수 있습니다. 대금 청구 프로필은 **송장 요약** 섹션의 온라인 송장 페이지에도 표시 됩니다. 청구 프로필에 대 한 자세한 내용과이를 사용 하 여 조직에 대 한 보다 유연한 대금 청구 옵션을 만드는 방법에 대 한 자세한 내용은 [청구 프로필 관리](manage-billing-profiles.md)를 참조 하세요. |
| 청구 프로필 |**청구지**, **PO 번호**및 지불 조건 같은 송장 속성을 정의 하는 데 사용 되는 대금 청구 프로필의 이름입니다. 이 정보는 <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">청구 프로필</a> 페이지에서 관리할 수 있습니다. 청구 프로필에 대 한 자세한 내용과이를 사용 하 여 조직에 보다 유연한 대금 청구 옵션을 만드는 방법에 대 한 자세한 내용은 [청구 프로필 관리](manage-billing-profiles.md)를 참조 하세요. |
| 송장 번호 |추적 목적으로 사용 되는 Microsoft에서 생성 한 고유 송장 번호입니다. |
| 송장 날짜 |송장이 생성 된 날짜 (일반적으로 대금 청구 주기 종료 후 5 ~ 12 일)입니다. 청구 프로필 세부 정보 페이지에서 청구서 날짜를 확인할 수 있습니다. 청구 기간 및 송장 날짜의 끝 시간 사이에 발생 하는 요금은 다음 결제 기간에 해당 하는 경우 다음 달에 대 한 송장에 포함 됩니다. 각 송장에 대 한 청구 기간 시작 및 종료 날짜는 **대금 청구 요약**위의 송장 PDF에 나열 되어 있습니다.|
| 지불 조건 |Microsoft 청구서 지불 방법 *Net 30 일* 이란 송장에 대 한 지침에 따라 청구서 날짜 로부터 30 일 이내에 지불 하는 것을 의미 합니다. |

## <a name="understand-the-billing-summary"></a>대금 청구 요약 이해

**대금 청구 요약** 에는 이전 대금 청구 기간 이후의 금액, 적용 된 제작진, 세금 및 총 금액에 대 한 요약이 표시 됩니다.

| 용어 | 설명 |
| --- | --- |
| 요금|이 대금 청구 기간에 대해 구매한 총 제품 수 및 관련 요금 및 세금입니다. 구매는 자재 명세서를 간결 하 게 볼 수 있도록 집계 됩니다. |
| 크레딧 |반환 받은 제작진 |
| Azure 제작진 적용 |Azure 크레딧이 각 대금 청구 기간에 자동으로 적용 됩니다. Azure 크레딧이 없는 경우이 필드는 숨겨집니다. Azure 크레딧에 대 한 자세한 내용은 [Microsoft 고객 계약 Azure 크레딧 잔액 추적](https://docs.microsoft.com/azure/billing/billing-mca-check-azure-credits-balance)을 참조 하십시오. |
| 부분합과 |기한 전 금액 |
| 세금 |대금 청구 프로필의 국가에 따라 지불 하는 세금의 유형 및 수량입니다. 세금을 지불할 필요가 없으면 송장에 세금을 표시 하지 않습니다. |

### <a name="understand-your-charges"></a>비용 이해

비용 페이지에는 제품별로 세분화 된 비용이 표시 됩니다. Azure 고객의 경우 청구서 섹션에 따라 비용이 청구 될 수 있습니다. Azure 제품에서 송장 섹션을 사용 하는 방법에 대 한 자세한 내용은 [Microsoft 고객 계약 청구 계정 시작](https://docs.microsoft.com/azure/billing/billing-mca-overview)의 [송장 섹션](https://docs.microsoft.com/azure/billing/billing-mca-overview#invoice-sections) 을 참조 하세요. 각 제품 주문 내에서 비용은 서비스 제품군으로 구분 됩니다.

| 용어 |설명 |
| --- | --- |
| 단가 | 요금 청구를 계산 하는 데 사용 되는 서비스의 실제 단가 (가격 산정 금액)입니다. 이 가격은 제품, 서비스 제품군, 측정기 및 혜택에 고유 합니다. |
| 수량 | 대금 청구 기간 중 구입 또는 소비 수량 |
| 요금/제작진 | 제작진/refunds가 적용 된 후의 네트워크 금액입니다. |
| Azure 크레딧 | 청구 금액/제작진에 적용 된 Azure 제작진 |
| 세금 비율 | 국가에 따른 세금 비율입니다. |
| 세금 금액 | 세금 급여에 따라 구매에 적용 된 세금의 양 |
| 합계 | 구매로 인 한 총 금액 |

라인 항목 세부 정보는 요금이 부과 되는 제품 유형에 따라 달라 집니다. 예를 들어 Azure 제품의 경우 적용 된 Azure 크레딧 양이 표시 됩니다. 좌석 기반 제품은 단가와 수량을 표시 합니다. 송장 세부 정보에는 구매한 제품, 할인 또는 제작진, 세금 급여 및 금액, 품목 합계가 표시 됩니다.

> Total = 청구 금액-Azure Credit + 세금

각 서비스 제품군의 총 금액은 크레딧/요금에서 Azure 제작진을 빼서 세금을 추가 하 여 계산 됩니다.

> Total = 청구/제작진-Azure Credit + 세금

송장에 자세한 정보를 보려는 Azure 요금이 있는 경우 [Microsoft 고객 계약 송장 검토](https://docs.microsoft.com/azure/cost-management-billing/understand/review-customer-agreement-bill)를 참조 하세요.

## <a name="understand-the-last-invoice-page"></a>마지막 송장 페이지 이해

### <a name="payment-instructions"></a>결제 지침

송장 맨 아래에 청구서 지불 방법에 대 한 지침이 나와 있습니다. 유선, 확인 또는 온라인으로 결제를 수행할 수 있습니다.

### <a name="publisher-information"></a>게시자 정보

청구서에 타사 서비스가 있는 경우 각 출판사의 이름과 주소가 송장 아래쪽에 나열 됩니다.

## <a name="view-your-online-invoice"></a>온라인 송장 보기

송장을 온라인으로 사용할 수 있습니다. 온라인 송장에 대 한 링크는 PDF 송장과 전자 메일 알림에서 제공 됩니다. 온라인 송장을 확장 하 여 송장에 대 한 청구 금액을 확인 하 고 각 항목에 대 한 세부 정보를 볼 수 있습니다. 온라인 송장에는 다음이 포함 됩니다.

- **가격 책정 세부 정보** &mdash; 할인 및 제품 가격에 대 한 세부 정보를 포함 한 추가 정보

- **온라인 결제** &mdash; 송장에서 지불을 온라인으로 설정 하도록 선택할 수 있습니다.

- **Azure 비용 관리** &mdash; Azure 고객의 경우 온라인 송장에는 Azure 비용 관리에 대 한 링크가 포함 됩니다.

### <a name="to-view-your-online-invoice"></a>온라인 송장을 보려면

1. 관리 센터에서 **청구** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">청구서 및 결제</a> 페이지로 이동하십시오.

2. 해당 송장의 .pdf 버전을 다운로드 하려면 보려는 송장에 대 한 행에서 **송장 Pdf 다운로드** 를 선택 합니다.

3. 온라인 송장을 보려면 목록에서 송장을 선택 합니다. 송장 세부 정보 페이지 에서도 .pdf를 다운로드할 수 있습니다.

## <a name="invoice-faq"></a>송장 FAQ

### <a name="when-is-my-invoice-available"></a>사용 가능한 송장은 언제 입니까?

일부 송장은 구매한 후 24 시간 내에 생성 됩니다. 다른 송장은 대금 청구 기간 종료 시 생성 되며 해당 기간의 모든 항목을 포함 합니다.

### <a name="how-do-i-pay-the-amount-due-on-my-invoice"></a>송장에 따른 금액을 어떻게 지불 하나요?

결제 방법은 결제 방법에 따라 달라 지 며 송장 PDF의 아래쪽에 제공 됩니다. 결제 방법이 신용 카드 이면 송장 날짜 10 일 이내에 자동으로 청구 됩니다. 결제 방법이 확인 또는 연결 전송 인 경우 PDF의 **결제 지침** 에 있는 정보를 참조 하세요.

### <a name="whats-the-difference-between-sold-to-and-bill-to-addresses"></a>"판매 대상" 및 "청구지" 주소 간의 차이점은 무엇 인가요?

- **판매 대상:** 송장에서 지불 및 확인을 담당 하는 법률 엔터티입니다. 여기에 제공 된 주소는 구입 중에 대체 배송 주소를 제공 하지 않을 경우 세금을 결정 하는 데 사용 됩니다. 자세한 내용은 [세금 정보](tax-information.md)를 참조 하세요.
- **청구지:** 해당 하는 경우 실제 송장을 보내는 주소입니다. 합법적인 엔터티와의 청구서에는 여러 **자재 명세서** 가 있을 수 있지만 대금 청구 프로필 당 하나의 **자재 명세서** 만 있습니다.

### <a name="what-are-billed-amount-and-amount-due"></a>"대금 청구 금액" 및 "금액 기한"

- **청구 금액:** 구매한 총 구매 금액입니다.
- **만료 금액:** 금액이 확실에 대 한 남은 잔액입니다.

### <a name="what-is-the-difference-between-service-period-and-billing-period"></a>"서비스 기간"과 "대금 청구 기간"의 차이점은 무엇 인가요?

- **서비스 기간:** 서비스를 사용 하는 데 비용이 청구 되는 기간입니다.
- **청구 기간:** 마지막 송장 날짜 이후의 기간입니다.

### <a name="how-do-i-view-and-print-my-bill"></a>내 청구서를 보고 인쇄 하려면 어떻게 하나요?

1. **청구**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">금액 & 지불</a> 페이지에서 송장 날짜 범위를 선택 합니다.
2. 청구서의 PDF 복사본을 인쇄 하거나 저장 하려면 **송장 Pdf 다운로드**를 선택 하 고 pdf를 인쇄 합니다.

자세한 내용은 [청구서 또는 송장 보기](view-your-bill-or-invoice.md)를 참조 하세요.

### <a name="why-dont-i-see-azure-prepayment-as-a-payment-method"></a>Azure prepayment이 결제 방법으로 표시 되지 않는 이유는 무엇 인가요?

Azure prepayment는 적합 한 Azure 제품 및 서비스에 대 한 결제 방법 으로만 사용할 수 있습니다.

## <a name="need-help-contact-support"></a>도움이 필요하신가요? 고객 지원에 문의하세요.

Azure 제작진 관련 질문이 있거나 도움이 필요한 경우 <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">azure 지원 서비스를 통해 지원 요청을 만듭니다</a>.

Microsoft 365 관리 센터의 청구서에 대 한 질문이 있거나 도움이 필요한 경우 [비즈니스 제품 지원 서비스에 문의 하세요](../../admin/contact-support-for-business-products.md).