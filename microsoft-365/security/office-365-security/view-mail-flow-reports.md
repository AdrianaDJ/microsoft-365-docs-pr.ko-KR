---
title: 보안 & 준수 센터에서 메일 흐름 보고서 보기
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: 조직에 대 한 메일 흐름 보안 보고서를 찾아서 사용 하는 방법에 대해 알아봅니다. 메일 흐름 보고서는 보안 & 준수 센터에서 사용할 수 있습니다.
ms.custom: ''
ms.openlocfilehash: 70c96bb4f43edb80f98fdc98aa173fed9e54e7d7
ms.sourcegitcommit: c43ebb915fa0eb7eb720b21b62c0d1e58e7cde3d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/30/2020
ms.locfileid: "44937260"
---
# <a name="view-mail-flow-reports-in-the-security--compliance-center"></a><span data-ttu-id="816c3-104">보안 & 준수 센터에서 메일 흐름 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-104">View mail flow reports in the Security & Compliance Center</span></span>

<span data-ttu-id="816c3-105">보안 & 준수 센터에서 사용할 수 있는 [메일 흐름 정보](mail-flow-insights-v2.md) 이외에, Microsoft 365 조직을 모니터링 하는 데 도움이 되는 다양 한 메일 흐름 보고서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-105">In addition to the [Mail flow insights](mail-flow-insights-v2.md) that are available in the Security & Compliance Center, a variety of mail flow reports are also available to help you monitor your Microsoft 365 organization.</span></span> <span data-ttu-id="816c3-106">[필요한 권한이](#what-permissions-are-needed-to-view-these-reports)있는 경우 <https://office.protection.com> **보고서** 대시보드로 이동 하 여 보안 & 준수 센터에서 이러한 보고서를 볼 수 있습니다 \> **Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="816c3-106">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Security & Compliance Center at <https://office.protection.com> by going to **Reports** \> **Dashboard**.</span></span> <span data-ttu-id="816c3-107">보고서 대시보드로 직접 이동 하려면를 엽니다 <https://office.protection.office.com/insightdashboard> .</span><span class="sxs-lookup"><span data-stu-id="816c3-107">To go directly to the reports dashboard, open <https://office.protection.office.com/insightdashboard>.</span></span>

![보안 & 준수 센터의 보고서 대시보드](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

## <a name="connector-report"></a><span data-ttu-id="816c3-109">커넥터 보고서</span><span class="sxs-lookup"><span data-stu-id="816c3-109">Connector report</span></span>

<span data-ttu-id="816c3-110">**커넥터 보고서** 에는 조직에 대해 구성 된 [인바운드 및 아웃 바운드 커넥터](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) 에 대 한 메일 흐름 활동이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-110">The **Connector report** shows mail flow activity on the [inbound and outbound connectors](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) that are configured for your organization.</span></span>

<span data-ttu-id="816c3-111">보고서를 보려면 [보안 & 준수 센터](https://protection.office.com)를 열고 **보고서** \> **대시보드로** 이동한 후 **커넥터 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-111">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Connector report**.</span></span> <span data-ttu-id="816c3-112">보고서로 직접 이동 하려면를 엽니다 <https://protection.office.com/reportv2?id=ConnectorReport> .</span><span class="sxs-lookup"><span data-stu-id="816c3-112">To go directly to the report, open <https://protection.office.com/reportv2?id=ConnectorReport>.</span></span>

![보고서 대시보드의 커넥터 보고서 위젯](../../media/connector-report-widget.png)

### <a name="report-view-for-the-connector-report"></a><span data-ttu-id="816c3-114">커넥터 보고서에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-114">Report view for the Connector report</span></span>

<span data-ttu-id="816c3-115">보고서 보기에서는 다음과 같은 차트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-115">The following charts are available in report view:</span></span>

- <span data-ttu-id="816c3-116">**데이터 보기 기준: 메일 흐름**:이 차트에서는 다음을 기준으로 구성한 인바운드 및 아웃 바운드 메시지의 수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-116">**View data by: Mail flow**: This chart shows the number of inbound and outbound messages organized by:</span></span>

  - <span data-ttu-id="816c3-117">**합계**</span><span class="sxs-lookup"><span data-stu-id="816c3-117">**Total**</span></span>
  - <span data-ttu-id="816c3-118">**커넥터 없이 인터넷에서**</span><span class="sxs-lookup"><span data-stu-id="816c3-118">**From the internet without a connector**</span></span>
  - <span data-ttu-id="816c3-119">**커넥터 없이 인터넷에 연결**</span><span class="sxs-lookup"><span data-stu-id="816c3-119">**To the internet without a connector**</span></span>
  - <span data-ttu-id="816c3-120">구성한 특정 커넥터</span><span class="sxs-lookup"><span data-stu-id="816c3-120">A specific connector that you've configured.</span></span>
  
  <span data-ttu-id="816c3-121">차트에서 데이터를 격리 하려면 다음 **에 대 한 데이터 표시** 컨트롤을 사용 하 여 이러한 옵션 중 하나 또는 **모든 메일 흐름**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-121">To isolate the data in the chart, use the **Show data for** control to select one of these options or **All mail flow**.</span></span>

  ![커넥터 보고서에서 메일 흐름을 기준으로 데이터 보기](../../media/connector-report-view-data-by-mail-flow.png)

- <span data-ttu-id="816c3-123">**데이터 보기 기준: tls 사용량**:이 차트에서는 메일 흐름에 대 한 Tls (전송 계층 보안) 버전 사용 비율을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-123">**View data by: TLS usage**: This chart shows the percentage of Transport Layer Security (TLS) version usage for mail flow.</span></span>

  <span data-ttu-id="816c3-124">차트에서 데이터를 격리 하려면 다음 **에 대 한 데이터 표시** 컨트롤을 사용 하 여 다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-124">To isolate the data in the chart, use the **Show data for** control to select one of the following options:</span></span>

  - <span data-ttu-id="816c3-125">**모든 메일 흐름**</span><span class="sxs-lookup"><span data-stu-id="816c3-125">**All mail flow**</span></span>
  - <span data-ttu-id="816c3-126">**커넥터 없이 인터넷에서**</span><span class="sxs-lookup"><span data-stu-id="816c3-126">**From the internet without a connector**</span></span>
  - <span data-ttu-id="816c3-127">**커넥터 없이 인터넷에 연결**</span><span class="sxs-lookup"><span data-stu-id="816c3-127">**To the internet without a connector**</span></span>
  - <span data-ttu-id="816c3-128">구성한 특정 커넥터</span><span class="sxs-lookup"><span data-stu-id="816c3-128">A specific connector that you've configured.</span></span>

  ![커넥터 보고서에서 TLS 사용을 기준으로 데이터 보기](../../media/connector-report-view-data-by-tls-usage.png)

<span data-ttu-id="816c3-130">보고서 보기에서 **필터** 를 클릭 하면 **시작 날짜** 및 **종료 날짜**와 함께 날짜 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-130">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-connector-report"></a><span data-ttu-id="816c3-131">커넥터 보고서에 대 한 세부 정보 테이블 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-131">Details table view for the Connector report</span></span>

<span data-ttu-id="816c3-132">보고서 보기에서 **세부 정보 테이블 보기** 를 클릭 하면 다음과 같은 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-132">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="816c3-133">**날짜**</span><span class="sxs-lookup"><span data-stu-id="816c3-133">**Date**</span></span>
- <span data-ttu-id="816c3-134">**커넥터 방향 및 이름**</span><span class="sxs-lookup"><span data-stu-id="816c3-134">**Connector direction and name**</span></span>
- <span data-ttu-id="816c3-135">**커넥터 유형**</span><span class="sxs-lookup"><span data-stu-id="816c3-135">**Connector type**</span></span>
- <span data-ttu-id="816c3-136">**강제 TLS?**: **True** 또는 **False**값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-136">**Forced TLS?**: The value **True** or **False**.</span></span>
- <span data-ttu-id="816c3-137">**TLS 없음** (백분율)</span><span class="sxs-lookup"><span data-stu-id="816c3-137">**No TLS** (percentage)</span></span>
- <span data-ttu-id="816c3-138">**TLS 1.0** (백분율)</span><span class="sxs-lookup"><span data-stu-id="816c3-138">**TLS 1.0** (percentage)</span></span>
- <span data-ttu-id="816c3-139">**TLS 1.1** (백분율)</span><span class="sxs-lookup"><span data-stu-id="816c3-139">**TLS 1.1** (percentage)</span></span>
- <span data-ttu-id="816c3-140">**TLS 1.2** (백분율)</span><span class="sxs-lookup"><span data-stu-id="816c3-140">**TLS 1.2** (percentage)</span></span>
- <span data-ttu-id="816c3-141">**볼륨**: 메시지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-141">**Volume**: The number of messages.</span></span>

<span data-ttu-id="816c3-142">세부 정보 표 보기에서 **필터** 를 클릭 하면 **시작 날짜** 및 **종료 날짜**와 함께 날짜 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-142">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="816c3-143">보고서 보기로 돌아가려면 **보고서 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-143">To go back to the report view, click **View report**.</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="816c3-144">Exchange 전송 규칙 보고서</span><span class="sxs-lookup"><span data-stu-id="816c3-144">Exchange transport rule report</span></span>

<span data-ttu-id="816c3-145">**Exchange 전송 규칙 보고서** 는 조직에서 들어오고 나가는 메시지에 대 한 메일 흐름 규칙 (전송 규칙이 라고도 함)의 영향을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-145">The **Exchange transport rule report** shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="816c3-146">보고서를 보려면 [보안 & 준수 센터](https://protection.office.com)를 열고 **보고서** \> **대시보드로** 이동한 다음 **Exchange 전송 규칙**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-146">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Exchange Transport rule**.</span></span> <span data-ttu-id="816c3-147">보고서로 직접 이동 하려면를 엽니다 <https://protection.office.com/reportv2?id=ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="816c3-147">To go directly to the report, open <https://protection.office.com/reportv2?id=ETRRuleReport>.</span></span>

![보고서 대시보드의 Exchange 전송 규칙 위젯](../../media/transport-rule-report-widget.png)

### <a name="report-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="816c3-149">Exchange 전송 규칙 보고서에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-149">Report view for the Exchange transport rule report</span></span>

<span data-ttu-id="816c3-150">보고서 보기에서는 다음과 같은 차트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-150">The following charts are available in report view:</span></span>

- <span data-ttu-id="816c3-151">**데이터 보기 기준: Exchange 전송 규칙** \> **아래로 나누기: 방향**:이 차트에서는 전송 규칙의 영향을 받는 **인바운드** 및 **아웃 바운드** 메시지의 수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-151">**View data by: Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by transport rules.</span></span>

- <span data-ttu-id="816c3-152">**데이터 보기 기준: Exchange 전송 규칙** \> **아래로 나누기: 심각도**:이 차트에는 **높은 심각도** 및 **보통 심각도**및 **심각도가 낮은** 메시지 수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-152">**View data by: Exchange transport rules** \> **Break down by: Severity**: This chart shows the number of **High severity** and **Medium severity**, and **Low severity** messages.</span></span> <span data-ttu-id="816c3-153">심각도 수준을 규칙의 작업으로 설정 합니다 (심각도 수준이 나 _Setauditseverity_**으로이 규칙 감사** ).</span><span class="sxs-lookup"><span data-stu-id="816c3-153">You set the severity level as an action in the rule (**Audit this rule with severity level** or _SetAuditSeverity_).</span></span> <span data-ttu-id="816c3-154">자세한 내용은 [Mail flow rule actions In Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="816c3-154">For more information, see [Mail flow rule actions in Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="816c3-155">**데이터 보기 기준: DLP Exchange 전송 규칙** \> **아래로 나누기: 방향**:이 차트에서는 DLP (데이터 손실 방지) 전송 규칙의 영향을 받는 **인바운드** 및 **아웃 바운드** 메시지의 수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-155">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) transport rules.</span></span> <span data-ttu-id="816c3-156">다음 옵션을 선택 하 여 차트를 보다 구체화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-156">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="816c3-157">**데이터 표시: 모든 DLP 전송 규칙**</span><span class="sxs-lookup"><span data-stu-id="816c3-157">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="816c3-158">**데이터 표시: 손상 된 사용자**</span><span class="sxs-lookup"><span data-stu-id="816c3-158">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="816c3-159">**데이터 표시: 검색 된 콘텐츠가 부족 함 미국 Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="816c3-159">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

- <span data-ttu-id="816c3-160">**데이터 보기 기준: DLP Exchange 전송 규칙** \> **아래로 나누기: 방향**:이 보기에는 DLP 전송 규칙의 영향을 받은 **높은 심각도** 및 **중간**심각도 메시지와 **낮은 심각도** 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-160">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This view shows the number of **High severity** and **Medium severity**, and **Low severity** messages that were affected by DLP transport rules.</span></span> <span data-ttu-id="816c3-161">다음 옵션을 선택 하 여 차트를 보다 구체화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-161">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="816c3-162">**데이터 표시: 모든 DLP 전송 규칙**</span><span class="sxs-lookup"><span data-stu-id="816c3-162">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="816c3-163">**데이터 표시: 손상 된 사용자**</span><span class="sxs-lookup"><span data-stu-id="816c3-163">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="816c3-164">**데이터 표시: 검색 된 콘텐츠가 부족 함 미국 Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="816c3-164">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

<span data-ttu-id="816c3-165">보고서 보기에서 **필터** 를 클릭 하면 다음 필터를 사용 하 여 결과를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-165">If you click **Filters** in a report view, you can modify the results with the following filters::</span></span>

- <span data-ttu-id="816c3-166">**시작 날짜** 및 **끝 날짜**</span><span class="sxs-lookup"><span data-stu-id="816c3-166">**Start date** and **End date**</span></span>
- <span data-ttu-id="816c3-167">방향 값</span><span class="sxs-lookup"><span data-stu-id="816c3-167">Direction values</span></span>
- <span data-ttu-id="816c3-168">심각도 값</span><span class="sxs-lookup"><span data-stu-id="816c3-168">Severity values</span></span>

![Exchange 전송 규칙 보고서의 보고서 보기](../../media/transport-rule-report-report-view.png)

### <a name="details-table-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="816c3-170">Exchange 전송 규칙 보고서에 대 한 세부 정보 테이블 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-170">Details table view for the Exchange transport rule report</span></span>

<span data-ttu-id="816c3-171">**세부 정보 표 보기**를 클릭 하면 표시 되는 정보는 보고 있는 차트에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-171">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="816c3-172">**데이터 보기 기준: Exchange 전송 규칙**:</span><span class="sxs-lookup"><span data-stu-id="816c3-172">**View data by: Exchange Transport rules**:</span></span>

  - <span data-ttu-id="816c3-173">**날짜**</span><span class="sxs-lookup"><span data-stu-id="816c3-173">**Date**</span></span>
  - <span data-ttu-id="816c3-174">**전송 규칙**</span><span class="sxs-lookup"><span data-stu-id="816c3-174">**Transport rule**</span></span>
  - <span data-ttu-id="816c3-175">**제목**</span><span class="sxs-lookup"><span data-stu-id="816c3-175">**Subject**</span></span>
  - <span data-ttu-id="816c3-176">**보낸 사람 주소**</span><span class="sxs-lookup"><span data-stu-id="816c3-176">**Sender address**</span></span>
  - <span data-ttu-id="816c3-177">**받는 사람 주소**</span><span class="sxs-lookup"><span data-stu-id="816c3-177">**Recipient address**</span></span>
  - <span data-ttu-id="816c3-178">**심각도**</span><span class="sxs-lookup"><span data-stu-id="816c3-178">**Severity**</span></span>
  - <span data-ttu-id="816c3-179">**방향**</span><span class="sxs-lookup"><span data-stu-id="816c3-179">**Direction**</span></span>

- <span data-ttu-id="816c3-180">**데이터 보기 기준: DLP Exchange 전송 규칙**:</span><span class="sxs-lookup"><span data-stu-id="816c3-180">**View data by: DLP Exchange transport rules**:</span></span>

  - <span data-ttu-id="816c3-181">**날짜**</span><span class="sxs-lookup"><span data-stu-id="816c3-181">**Date**</span></span>
  - <span data-ttu-id="816c3-182">**DLP 정책**</span><span class="sxs-lookup"><span data-stu-id="816c3-182">**DLP policy**</span></span>
  - <span data-ttu-id="816c3-183">**전송 규칙**</span><span class="sxs-lookup"><span data-stu-id="816c3-183">**Transport rule**</span></span>
  - <span data-ttu-id="816c3-184">**제목**</span><span class="sxs-lookup"><span data-stu-id="816c3-184">**Subject**</span></span>
  - <span data-ttu-id="816c3-185">**보낸 사람 주소**</span><span class="sxs-lookup"><span data-stu-id="816c3-185">**Sender address**</span></span>
  - <span data-ttu-id="816c3-186">**받는 사람 주소**</span><span class="sxs-lookup"><span data-stu-id="816c3-186">**Recipient address**</span></span>
  - <span data-ttu-id="816c3-187">**심각도**</span><span class="sxs-lookup"><span data-stu-id="816c3-187">**Severity**</span></span>
  - <span data-ttu-id="816c3-188">**방향**</span><span class="sxs-lookup"><span data-stu-id="816c3-188">**Direction**</span></span>

<span data-ttu-id="816c3-189">세부 정보 표 보기에서 **필터** 를 클릭 하면 다음 필터를 사용 하 여 결과를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-189">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="816c3-190">**시작 날짜** 및 **끝 날짜**</span><span class="sxs-lookup"><span data-stu-id="816c3-190">**Start date** and **End date**</span></span>
- <span data-ttu-id="816c3-191">방향 값</span><span class="sxs-lookup"><span data-stu-id="816c3-191">Direction values</span></span>
- <span data-ttu-id="816c3-192">심각도 값</span><span class="sxs-lookup"><span data-stu-id="816c3-192">Severity values</span></span>

<span data-ttu-id="816c3-193">보고서 보기로 돌아가려면 **보고서 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-193">To go back to the report view, click **View report**.</span></span>

## <a name="forwarding-report"></a><span data-ttu-id="816c3-194">전달 보고서</span><span class="sxs-lookup"><span data-stu-id="816c3-194">Forwarding report</span></span>

<span data-ttu-id="816c3-195">**전달 보고서** 에는 조직의 자동으로 전달 되는 메시지가 Exchange Online 사서함의 외부 도메인으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-195">The **Forwarding report** shows your organization's automatically forwarded messages to external domains from Exchange Online mailboxes.</span></span> <span data-ttu-id="816c3-196">전달 된 메시지는 보안 또는 준수 위험을 초래할 수 있으며 계정이 손상 된 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-196">Forwarded messages can pose a security or compliance risk, and might indicate a compromised account.</span></span>

<span data-ttu-id="816c3-197">보고서를 보려면 [보안 & 준수 센터](https://protection.office.com)를 열고 **보고서** \> **대시보드로** 이동한 후 **전달 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-197">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Forwarding report**.</span></span> <span data-ttu-id="816c3-198">보고서로 직접 이동 하려면를 엽니다 <https://protection.office.com/reportv2?id=MailFlowForwarding> .</span><span class="sxs-lookup"><span data-stu-id="816c3-198">To go directly to the report, open <https://protection.office.com/reportv2?id=MailFlowForwarding>.</span></span>

![보고서 대시보드에서 보고서 위젯 전달](../../media/forwarding-report-widget.png)

### <a name="report-view-for-the-forwarding-report"></a><span data-ttu-id="816c3-200">전달 보고서에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-200">Report view for the Forwarding report</span></span>

<span data-ttu-id="816c3-201">보고서 보기에서는 다음과 같은 차트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-201">The following charts are available in the report view:</span></span>

- <span data-ttu-id="816c3-202">**데이터 표시: 전달 메서드**: 다음과 같은 메서드가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-202">**Show data for: Forwarding methods**: The following methods are shown:</span></span>

  - <span data-ttu-id="816c3-203">**전송 규칙**: [메일 흐름 규칙이](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-203">**Transport rule**: Also known as [mail flow rules](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span></span>
  - <span data-ttu-id="816c3-204">**사서함 규칙**: [받은 편지함 규칙이](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59)라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-204">**Mailbox rule**: Also known as [Inbox rules](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span></span>

  ![전달 보고서의 전달 메서드 보기](../../media/forwarding-report-forwarding-methods.png)

- <span data-ttu-id="816c3-206">**다음에 대 한 데이터 표시: 전달 도메인**:이 보기에는 전달 대상이 되는 받는 사람 도메인이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-206">**Show data for: Forwarding domains**: This view shows the recipient domains that are the destinations for forwarding.</span></span>

  ![전달 보고서의 전달 도메인 보기](../../media/forwarding-report-forwarding-domains.png)

- <span data-ttu-id="816c3-208">**데이터 표시: 전달자**: 다음 전달자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-208">**Show data for: Forwarders**: The following forwarders are shown:</span></span>

  - <span data-ttu-id="816c3-209">**전송 규칙**</span><span class="sxs-lookup"><span data-stu-id="816c3-209">**Transport rule**</span></span>
  - <span data-ttu-id="816c3-210">전달 받은 편지함 규칙을 포함 하는 사서함입니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-210">The mailbox that contains the forwarding Inbox rule.</span></span>

  ![전달 보고서의 전달자 보기](../../media/forwarding-report-forwarders.png)

<span data-ttu-id="816c3-212">보고서 보기에서 **필터** 를 클릭 하면 **시작 날짜** 및 **종료 날짜**와 함께 날짜 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-212">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-forwarding-report"></a><span data-ttu-id="816c3-213">전달 보고서에 대 한 세부 정보 테이블 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-213">Details table view for the Forwarding report</span></span>

<span data-ttu-id="816c3-214">보고서 보기에서 **세부 정보 테이블 보기** 를 클릭 하면 다음과 같은 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-214">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="816c3-215">**전달자**: 값 **전송 규칙** 또는 전달 받은 편지함 규칙을 포함 하는 사서함입니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-215">**Forwarders**: The value **Transport rule** or the mailbox that contains the forwarding Inbox rule.</span></span>
- <span data-ttu-id="816c3-216">**전달 유형**: 값 **사서함 규칙** 또는 **전송 규칙**</span><span class="sxs-lookup"><span data-stu-id="816c3-216">**Forwarding type**: The value **Mailbox rule** or **Transport rule**.</span></span>
- <span data-ttu-id="816c3-217">**받는 사람 이름**</span><span class="sxs-lookup"><span data-stu-id="816c3-217">**Recipient name**</span></span>
- <span data-ttu-id="816c3-218">**받는 사람 도메인**</span><span class="sxs-lookup"><span data-stu-id="816c3-218">**Recipient domain**</span></span>
- <span data-ttu-id="816c3-219">**Details**: 메일 흐름 규칙의 GUID 값 또는 받은 편지함 규칙의 RuleIdentity 값입니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-219">**Details**: This is the GUID value of the mail flow rule, or the RuleIdentity value of the Inbox rule.</span></span>
- <span data-ttu-id="816c3-220">**개수**</span><span class="sxs-lookup"><span data-stu-id="816c3-220">**Count**</span></span>
- <span data-ttu-id="816c3-221">**첫 번째 전달 날짜**</span><span class="sxs-lookup"><span data-stu-id="816c3-221">**First forward date**</span></span>

<span data-ttu-id="816c3-222">세부 정보 표 보기에서 **필터** 를 클릭 하면 **시작 날짜** 및 **종료 날짜**와 함께 날짜 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-222">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="816c3-223">보고서 보기로 돌아가려면 **보고서 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-223">To go back to the reports view, click **View report**.</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="816c3-224">메일 흐름 상태 보고서</span><span class="sxs-lookup"><span data-stu-id="816c3-224">Mailflow status report</span></span>

<span data-ttu-id="816c3-225">**메일 흐름 status 보고서** 는 edge에서 허용 되거나 차단 되는 전자 메일에 대 한 추가 정보가 포함 된 [보낸 날짜 및 받은 전자 메일 보고서](#sent-and-received-email-report)와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-225">The **Mailflow status report** is similar to the [Sent and received email report](#sent-and-received-email-report), with additional information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="816c3-226">이 보고서는 edge 보호 정보를 포함 하며, EOP (Exchange Online Protection)에서 평가를 위해 서비스에 허용 되기 전에 차단 되는 전자 메일의 양을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-226">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span>

<span data-ttu-id="816c3-227">보고서를 보려면 [보안 & 준수 센터](https://protection.office.com)를 열고 **보고서** \> **대시보드로** 이동한 다음 **메일 흐름 status report**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-227">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Mailflow status report**.</span></span> <span data-ttu-id="816c3-228">**메일 흐름 상태 보고서**로 바로 이동 하려면을 엽니다 <https://protection.office.com/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="816c3-228">To go directly to the **Mail flow status report**, open <https://protection.office.com/mailflowStatusReport>.</span></span>

![보고서 대시보드의 메일 흐름 상태 보고서 위젯](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="816c3-230">메일 흐름 상황 보고서의 형식 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-230">Type view for the Mailflow status report</span></span>

<span data-ttu-id="816c3-231">보고서를 열 때 **형식** 탭이 기본적으로 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-231">When you open the report, the **Type** tab is selected by default.</span></span> <span data-ttu-id="816c3-232">기본적으로이 보기에는 다음 필터를 사용 하 여 구성 된 차트 및 데이터 테이블이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-232">By default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="816c3-233">**날짜**: 지난 7 일</span><span class="sxs-lookup"><span data-stu-id="816c3-233">**Date**: The last 7 days.</span></span>
- <span data-ttu-id="816c3-234">**방향**:</span><span class="sxs-lookup"><span data-stu-id="816c3-234">**Direction**:</span></span>

  - <span data-ttu-id="816c3-235">**인바운드**</span><span class="sxs-lookup"><span data-stu-id="816c3-235">**Inbound**</span></span>
  - <span data-ttu-id="816c3-236">**아웃 바운드**</span><span class="sxs-lookup"><span data-stu-id="816c3-236">**Outbound**</span></span>
  - <span data-ttu-id="816c3-237">**조직 내** ( **인바운드** 및 **아웃 바운드**와 별도로 계산 됨)</span><span class="sxs-lookup"><span data-stu-id="816c3-237">**Intra-org** (counted separately from **Inbound** and **Outbound**)</span></span>

- <span data-ttu-id="816c3-238">다음을 **입력**합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-238">**Type**:</span></span>

  - <span data-ttu-id="816c3-239">**좋은 메일**</span><span class="sxs-lookup"><span data-stu-id="816c3-239">**Good mail**</span></span>
  - <span data-ttu-id="816c3-240">**맬웨어**</span><span class="sxs-lookup"><span data-stu-id="816c3-240">**Malware**</span></span>
  - <span data-ttu-id="816c3-241">**스팸**</span><span class="sxs-lookup"><span data-stu-id="816c3-241">**Spam**</span></span>
  - <span data-ttu-id="816c3-242">**에 지 보호**</span><span class="sxs-lookup"><span data-stu-id="816c3-242">**Edge protection**</span></span>
  - <span data-ttu-id="816c3-243">**규칙 메시지**</span><span class="sxs-lookup"><span data-stu-id="816c3-243">**Rule messages**</span></span>
  - <span data-ttu-id="816c3-244">**피싱 전자 메일**</span><span class="sxs-lookup"><span data-stu-id="816c3-244">**Phishing email**</span></span>

<span data-ttu-id="816c3-245">차트는 **형식** 값으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-245">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="816c3-246">**필터** 를 클릭 하거나 차트 범례에서 값을 클릭 하 여 이러한 필터를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-246">You can changes these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span>

<span data-ttu-id="816c3-247">데이터 테이블에는 다음과 같은 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-247">The data table contains the following information:</span></span>

- <span data-ttu-id="816c3-248">**방향**</span><span class="sxs-lookup"><span data-stu-id="816c3-248">**Direction**</span></span>
- <span data-ttu-id="816c3-249">**유형**</span><span class="sxs-lookup"><span data-stu-id="816c3-249">**Type**</span></span>
- <span data-ttu-id="816c3-250">**24시간**</span><span class="sxs-lookup"><span data-stu-id="816c3-250">**24 hours**</span></span>
- <span data-ttu-id="816c3-251">**3 일**</span><span class="sxs-lookup"><span data-stu-id="816c3-251">**3 days**</span></span>
- <span data-ttu-id="816c3-252">**7일**</span><span class="sxs-lookup"><span data-stu-id="816c3-252">**7 days**</span></span>
- <span data-ttu-id="816c3-253">**15일**</span><span class="sxs-lookup"><span data-stu-id="816c3-253">**15 days**</span></span>
- <span data-ttu-id="816c3-254">**30일**</span><span class="sxs-lookup"><span data-stu-id="816c3-254">**30 days**</span></span>

<span data-ttu-id="816c3-255">**자세한 내용을 보려면 범주 선택을**클릭 하면 다음 값 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-255">If you click **Choose a category for more details**, you can select from the following values:</span></span>

- <span data-ttu-id="816c3-256">**피싱 전자 메일**:이 옵션을 선택 하면 [위협 방지 상태 보고서](view-email-security-reports.md#threat-protection-status-report)로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-256">**Phishing email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="816c3-257">**전자 메일의 맬웨어**:이 옵션을 선택 하면 [위협 방지 상태 보고서](view-email-security-reports.md#threat-protection-status-report)로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-257">**Malware in email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="816c3-258">**스팸 감지**:이 옵션을 선택 하면 [스팸 감지 보고서](view-email-security-reports.md#spam-detections-report)가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-258">**Spam detections**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="816c3-259">**Edge 차단 된 스팸**:이 옵션을 선택 하면 [스팸 감지 보고서](view-email-security-reports.md#spam-detections-report)가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-259">**Edge blocked spam**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="816c3-260">**내보내기**:</span><span class="sxs-lookup"><span data-stu-id="816c3-260">**Export**:</span></span>

<span data-ttu-id="816c3-261">자세히 보기에 대해서는 1 일 동안 데이터만 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-261">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="816c3-262">따라서 데이터를 7 일간 내보내려는 경우에는 7 개의 서로 다른 내보내기 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-262">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="816c3-263">내보낸 각 .csv 파일은 15만 행으로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-263">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="816c3-264">해당 날짜의 데이터에 15만 개 이상의 행이 포함 되어 있는 경우 여러 .csv 파일이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-264">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="816c3-265">메일 흐름 상황 보고서의 형식 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-265">Type view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-type-view.png)

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="816c3-266">메일 흐름 상태 보고서에 대 한 방향 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-266">Direction view for the Mailflow status report</span></span>

<span data-ttu-id="816c3-267">**방향** 탭을 클릭 하면 **유형** 보기에서 같은 기본 필터가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-267">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="816c3-268">차트는 **방향** 값으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-268">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="816c3-269">**필터** 를 클릭 하거나 차트 범례에서 값을 클릭 하 여 이러한 필터를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-269">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span> <span data-ttu-id="816c3-270">**Type** 보기에서 동일한 필터가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-270">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="816c3-271">데이터 테이블에 **유형** 보기와 동일한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-271">The data table contains same information from the **Type** view.</span></span>

<span data-ttu-id="816c3-272">**자세한 내용에 대 한 자세한 내용은** **종류** 보기와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-272">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

<span data-ttu-id="816c3-273">**내보내기**:</span><span class="sxs-lookup"><span data-stu-id="816c3-273">**Export**:</span></span>

<span data-ttu-id="816c3-274">자세히 보기에 대해서는 1 일 동안 데이터만 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-274">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="816c3-275">따라서 데이터를 7 일간 내보내려는 경우에는 7 개의 서로 다른 내보내기 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-275">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="816c3-276">내보낸 각 .csv 파일은 15만 행으로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-276">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="816c3-277">해당 날짜의 데이터에 15만 개 이상의 행이 포함 되어 있는 경우 여러 .csv 파일이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-277">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="816c3-278">메일 흐름 상황 보고서의 방향 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-278">Direction view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-direction-view.png)

## <a name="sent-and-received-email-report"></a><span data-ttu-id="816c3-279">보내고 받은 전자 메일 보고서</span><span class="sxs-lookup"><span data-stu-id="816c3-279">Sent and received email report</span></span>

<span data-ttu-id="816c3-280">**Sent and received email** 보고서는 스팸 감지, 맬웨어 및 "양호"로 식별 된 전자 메일을 포함 하 여 수신 및 발신 전자 메일에 대 한 정보를 표시 하는 스마트 보고서입니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-280">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> <span data-ttu-id="816c3-281">이 보고서와 [메일 흐름 status 보고서](#mailflow-status-report) 의 차이점은 다음과 같습니다 .이 보고서에는 edge 보호에 의해 차단 된 메시지에 대 한 데이터가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-281">The difference between this report and the [Mailflow status report](#mailflow-status-report) is: this report doesn't include data about messages blocked by edge protection.</span></span>

<span data-ttu-id="816c3-282">보고서의 집계 보기 및 자세히 보기를 사용 하면 90 일의 필터링을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-282">The aggregate view and the detail view of the report allow for 90 days of filtering.</span></span>

<span data-ttu-id="816c3-283">보고서를 보려면 [보안 & 준수 센터](https://protection.office.com)를 열고 **보고서** \> **대시보드로** 이동한 다음 **보내고 받은 전자 메일**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-283">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Sent and received email**.</span></span> <span data-ttu-id="816c3-284">보고서로 직접 이동 하려면를 엽니다 <https://protection.office.com/reportv2?id=SentAndReceivedMailATP> .</span><span class="sxs-lookup"><span data-stu-id="816c3-284">To go directly to the report, open <https://protection.office.com/reportv2?id=SentAndReceivedMailATP>.</span></span>

![보고서 대시보드의 보낸 날짜 및 받은 전자 메일 위젯](../../media/sent-and-received-email-report-widget.png)

### <a name="report-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="816c3-286">보내고 받은 전자 메일 보고서에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-286">Report view for the Sent and received email report</span></span>

<span data-ttu-id="816c3-287">보고서 보기에서는 다음과 같은 차트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-287">The following charts are available in the report view:</span></span>

- <span data-ttu-id="816c3-288">**아래로 나누기: Type**: 다음은 사용 가능한 모든 종류를 표시 하는 차트입니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-288">**Break down by: Type**: The chart shows all available categories:</span></span>

  - <span data-ttu-id="816c3-289">**합계**</span><span class="sxs-lookup"><span data-stu-id="816c3-289">**Total**</span></span>
  - <span data-ttu-id="816c3-290">**좋은 메일**</span><span class="sxs-lookup"><span data-stu-id="816c3-290">**Good mail**</span></span>
  - <span data-ttu-id="816c3-291">**맬웨어 (맬웨어 방지)** (EOP)</span><span class="sxs-lookup"><span data-stu-id="816c3-291">**Malware (anti-malware)** (EOP)</span></span>
  - <span data-ttu-id="816c3-292">**스팸 감지**</span><span class="sxs-lookup"><span data-stu-id="816c3-292">**Spam detections**</span></span>
  - <span data-ttu-id="816c3-293">**규칙 메시지**</span><span class="sxs-lookup"><span data-stu-id="816c3-293">**Rule messages**</span></span>
  - <span data-ttu-id="816c3-294">**고급 맬웨어** (OFFICE 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="816c3-294">**Advanced malware** (Office 365 ATP)</span></span>

  <span data-ttu-id="816c3-295">차트에서 날짜 (데이터 요소)를 가리키면 해당 날짜에 대 한 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-295">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![보낸 편지함 및 받은 전자 메일 보고서에 보기 입력](../../media/sent-and-received-email-report-type-view.png)

- <span data-ttu-id="816c3-297">**나누기: 방향**: **합계**, **인바운드**및 **아웃 바운드** 데이터를 표시 하는 차트입니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-297">**Break down by: Direction**: The chart shows **Total**, **Inbound**, and **Outbound** data.</span></span> <span data-ttu-id="816c3-298">차트에서 날짜 (데이터 요소)를 가리키면 해당 날짜에 대 한 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-298">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![보내고 받은 전자 메일 보고서의 방향 보기](../../media/sent-and-received-email-report-direction-view.png)

- <span data-ttu-id="816c3-300">**드릴 다운 기준** \> **맬웨어 (맬웨어 방지)**:이 옵션을 선택 하면 [전자 메일 보고서의 맬웨어 감지](view-email-security-reports.md#malware-detection-in-email-report)로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-300">**Drill down by** \> **Malware (anti-malware)**: This selection takes you to the [Malware detection in email report](view-email-security-reports.md#malware-detection-in-email-report).</span></span>

- <span data-ttu-id="816c3-301">**드릴 다운 기준** \> **스팸 검색)**:이 옵션을 선택 하면 [스팸 감지 보고서](view-email-security-reports.md#spam-detections-report)가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-301">**Drill down by** \> **Spam detections)**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="816c3-302">보고서 보기에서 **필터** 를 클릭 하면 다음 필터를 사용 하 여 결과를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-302">If you click **Filters** in a report view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="816c3-303">**시작 날짜** 및 **끝 날짜**</span><span class="sxs-lookup"><span data-stu-id="816c3-303">**Start date** and **End date**</span></span>
- <span data-ttu-id="816c3-304">방향 값</span><span class="sxs-lookup"><span data-stu-id="816c3-304">Direction values</span></span>
- <span data-ttu-id="816c3-305">형식 값</span><span class="sxs-lookup"><span data-stu-id="816c3-305">Type values</span></span>

<span data-ttu-id="816c3-306">보고서 보기로 돌아가려면 **보고서 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-306">To go back to the report view, click **View report**.</span></span>

### <a name="details-table-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="816c3-307">보내고 받은 전자 메일 보고서에 대 한 세부 정보 테이블 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-307">Details table view for the Sent and received email report</span></span>

<span data-ttu-id="816c3-308">**아래로 나누기: 방향** 보기 또는 **아래로 나누기 기준: 방향** 보기로 **자세히 표 보기** 를 클릭 하면 다음과 같은 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-308">If you click **View details table** in the **Break down by: Direction** or **Break down by: Direction** view, the following information is shown:</span></span>

- <span data-ttu-id="816c3-309">**날짜 (UTC)**</span><span class="sxs-lookup"><span data-stu-id="816c3-309">**Date (UTC)**</span></span>
- <span data-ttu-id="816c3-310">**유형**</span><span class="sxs-lookup"><span data-stu-id="816c3-310">**Type**</span></span>
- <span data-ttu-id="816c3-311">**방향**</span><span class="sxs-lookup"><span data-stu-id="816c3-311">**Direction**</span></span>
- <span data-ttu-id="816c3-312">**메시지 수**</span><span class="sxs-lookup"><span data-stu-id="816c3-312">**Message count**</span></span>

<span data-ttu-id="816c3-313">세부 정보 표 보기에서 **필터** 를 클릭 하면 다음 필터를 사용 하 여 결과를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-313">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="816c3-314">**시작 날짜** 및 **끝 날짜**</span><span class="sxs-lookup"><span data-stu-id="816c3-314">**Start date** and **End date**</span></span>
- <span data-ttu-id="816c3-315">방향 값</span><span class="sxs-lookup"><span data-stu-id="816c3-315">Direction values</span></span>
- <span data-ttu-id="816c3-316">형식 값</span><span class="sxs-lookup"><span data-stu-id="816c3-316">Type values</span></span>

<span data-ttu-id="816c3-317">보고서 보기로 돌아가려면 **보고서 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-317">To go back to the report view, click **View report**.</span></span>

## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="816c3-318">상위 보낸 사람 및 받는 사람 보고서</span><span class="sxs-lookup"><span data-stu-id="816c3-318">Top senders and recipients report</span></span>

<span data-ttu-id="816c3-319">**상위 보낸 사람 및 받는 사람** 보고서는 상위 전자 메일 보낸 사람 및 받는 사람을 표시 하는 원형 차트입니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-319">The **Top senders and recipients** report is a pie chart showing your top email senders and recipients.</span></span>

<span data-ttu-id="816c3-320">보고서를 보려면 [보안 & 준수 센터](https://protection.office.com)를 열고 **보고서** \> **대시보드로** 이동한 다음 **상위 보낸 사람 및 받는 사람**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-320">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Top senders and recipients**.</span></span> <span data-ttu-id="816c3-321">보고서로 직접 이동 하려면를 엽니다 <https://protection.office.com/reportv2?id=TopSenderRecipientsATP> .</span><span class="sxs-lookup"><span data-stu-id="816c3-321">To go directly to the report, open <https://protection.office.com/reportv2?id=TopSenderRecipientsATP>.</span></span>

![보고서 대시보드의 상위 보낸 사람 및 받는 사람 위젯](../../media/top-senders-and-recipients-widget.png)

### <a name="report-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="816c3-323">상위 보낸 사람 및 받는 사람 보고서에 대 한 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-323">Report view for the Top senders and recipient report</span></span>

<span data-ttu-id="816c3-324">보고서 보기에서는 다음과 같은 차트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-324">The following charts are available in the report view:</span></span>

- <span data-ttu-id="816c3-325">**상위 메일 보낸 사람에 대 한 데이터 표시 \>**</span><span class="sxs-lookup"><span data-stu-id="816c3-325">**Show data for \> Top mail senders**</span></span>
- <span data-ttu-id="816c3-326">**상위 메일 받는 사람에 대 한 데이터 표시 \>**</span><span class="sxs-lookup"><span data-stu-id="816c3-326">**Show data for \> Top mail recipients**</span></span>
- <span data-ttu-id="816c3-327">**주요 스팸 받는 사람에 대 한 데이터 표시 \>**</span><span class="sxs-lookup"><span data-stu-id="816c3-327">**Show data for \> Top spam recipients**</span></span>
- <span data-ttu-id="816c3-328">**데이터 \> 표시 상위 맬웨어 받는 사람** (EOP)</span><span class="sxs-lookup"><span data-stu-id="816c3-328">**Show data for \> Top malware recipients** (EOP)</span></span>
- <span data-ttu-id="816c3-329">**데이터 \> 표시 최상위 맬웨어 받는 사람 (ATP)** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="816c3-329">**Show data for \> Top malware recipients (ATP)** (Office 365 ATP)</span></span>

<span data-ttu-id="816c3-330">원형 차트의 컴포지션은 이러한 선택에 따라 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-330">The composition of the pie chart changes based on these selections.</span></span>

<span data-ttu-id="816c3-331">원형 차트의 쐐기형 위에 마우스를 올리면 보내거나 받은 메시지 수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-331">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>

<span data-ttu-id="816c3-332">보고서 보기에서 **필터** 를 클릭 하면 **시작 날짜** 및 **종료 날짜**와 함께 날짜 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-332">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

![상위 보낸 사람 및 받는 사람 보고서의 보고서 보기에 있는 원형 차트](../../media/top-senders-and-recipients-report-view.png)

### <a name="details-table-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="816c3-334">상위 보낸 사람 및 받는 사람 보고서에 대 한 세부 정보 테이블 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-334">Details table view for the Top senders and recipient report</span></span>

<span data-ttu-id="816c3-335">**세부 정보 표 보기**를 클릭 하면 표시 되는 정보는 보고 있는 차트에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-335">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="816c3-336">**상위 메일 보낸 사람에 대 한 데이터 표시 \>**</span><span class="sxs-lookup"><span data-stu-id="816c3-336">**Show data for \> Top mail senders**</span></span>

  - <span data-ttu-id="816c3-337">**상위 메일 보낸 사람**</span><span class="sxs-lookup"><span data-stu-id="816c3-337">**Top mail senders**</span></span>
  - <span data-ttu-id="816c3-338">**개수**</span><span class="sxs-lookup"><span data-stu-id="816c3-338">**Count**</span></span>

- <span data-ttu-id="816c3-339">**상위 메일 받는 사람에 대 한 데이터 표시 \>**</span><span class="sxs-lookup"><span data-stu-id="816c3-339">**Show data for \> Top mail recipients**</span></span>

  - <span data-ttu-id="816c3-340">**주요 메일 받는 사람**</span><span class="sxs-lookup"><span data-stu-id="816c3-340">**Top mail recipients**</span></span>
  - <span data-ttu-id="816c3-341">**개수**</span><span class="sxs-lookup"><span data-stu-id="816c3-341">**Count**</span></span>

- <span data-ttu-id="816c3-342">**주요 스팸 받는 사람에 대 한 데이터 표시 \>**</span><span class="sxs-lookup"><span data-stu-id="816c3-342">**Show data for \> Top spam recipients**</span></span>

  - <span data-ttu-id="816c3-343">**주요 스팸 받는 사람**</span><span class="sxs-lookup"><span data-stu-id="816c3-343">**Top spam recipients**</span></span>
  - <span data-ttu-id="816c3-344">**개수**</span><span class="sxs-lookup"><span data-stu-id="816c3-344">**Count**</span></span>

- <span data-ttu-id="816c3-345">**데이터 \> 표시 상위 맬웨어 받는 사람** (EOP)</span><span class="sxs-lookup"><span data-stu-id="816c3-345">**Show data for \> Top malware recipients** (EOP)</span></span>

  - <span data-ttu-id="816c3-346">**주요 맬웨어 받는 사람**</span><span class="sxs-lookup"><span data-stu-id="816c3-346">**Top malware recipients**</span></span>
  - <span data-ttu-id="816c3-347">**개수**</span><span class="sxs-lookup"><span data-stu-id="816c3-347">**Count**</span></span>

- <span data-ttu-id="816c3-348">**데이터 \> 표시 최상위 맬웨어 받는 사람 (ATP)** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="816c3-348">**Show data for \> Top malware recipients (ATP)** (Office 365 ATP)</span></span>

  - <span data-ttu-id="816c3-349">**주요 ATP (맬웨어 수신자)**</span><span class="sxs-lookup"><span data-stu-id="816c3-349">**Top malware recipients (ATP)**</span></span>
  - <span data-ttu-id="816c3-350">**개수**</span><span class="sxs-lookup"><span data-stu-id="816c3-350">**Count**</span></span>

<span data-ttu-id="816c3-351">세부 정보 표 보기에서 **필터** 를 클릭 하면 **시작 날짜** 및 **종료 날짜**와 함께 날짜 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-351">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="816c3-352">보고서 보기로 돌아가려면 **보고서 보기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-352">To go back to the report view, click **View report**.</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="816c3-353">이러한 보고서를 표시 하는 데 필요한 사용 권한은 무엇입니까?</span><span class="sxs-lookup"><span data-stu-id="816c3-353">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="816c3-354">보고서를 보고 사용 하려면 보안 & 준수 센터 **및** Exchange Online에서 지정 된 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-354">To view and use the reports, you need to be a member of the specified role group in the Security & Compliance Center **and** in Exchange Online.</span></span>

- <span data-ttu-id="816c3-355">보안 & 준수 센터에서 다음 역할 그룹 중 하나의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-355">In the Security & Compliance Center, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="816c3-356">-조직 관리</span><span class="sxs-lookup"><span data-stu-id="816c3-356">-Organization Management</span></span>

  <span data-ttu-id="816c3-357">-보안 관리자 ( [Azure Active Directory 관리 센터](https://aad.portal.azure.com) 에서이 작업을 수행할 수도 있음)-보안 독자</span><span class="sxs-lookup"><span data-stu-id="816c3-357">-Security Administrator (you can also do this in the [Azure Active Directory admin center](https://aad.portal.azure.com) -Security Reader</span></span>

  <span data-ttu-id="816c3-358">자세한 내용은 [보안 및 준수 센터의 사용 권한](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="816c3-358">For more information, see [Permissions in the Security & Compliance Center](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span></span>

- <span data-ttu-id="816c3-359">Exchange Online에서 다음 역할 그룹 중 하나의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="816c3-359">In Exchange Online, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="816c3-360">-조직 관리</span><span class="sxs-lookup"><span data-stu-id="816c3-360">-Organization Management</span></span>

  <span data-ttu-id="816c3-361">-보기 전용 조직 관리</span><span class="sxs-lookup"><span data-stu-id="816c3-361">-View-only Organization Management</span></span>

  <span data-ttu-id="816c3-362">-보기 전용 받는 사람</span><span class="sxs-lookup"><span data-stu-id="816c3-362">-View-Only Recipients</span></span>

  <span data-ttu-id="816c3-363">-준수 관리</span><span class="sxs-lookup"><span data-stu-id="816c3-363">-Compliance Management</span></span>

<span data-ttu-id="816c3-364">자세한 내용은 exchange online의 [사용 권한](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) 및 [exchange online에서 역할 그룹 관리](https://docs.microsoft.com/Exchange/permissions-exo/role-groups)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="816c3-364">For more information, see [Permissions in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) and [Manage role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span></span>

## <a name="related-topics"></a><span data-ttu-id="816c3-365">관련 항목</span><span class="sxs-lookup"><span data-stu-id="816c3-365">Related topics</span></span>

[<span data-ttu-id="816c3-366">보안 및 준수 센터의 똑똑한 보고서 및 분석</span><span class="sxs-lookup"><span data-stu-id="816c3-366">Smart reports and insights in the Security & Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="816c3-367">보안 및 준수 센터의 전자 메일 보안 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="816c3-367">View email security reports in the Security & Compliance Center</span></span>](view-email-security-reports.md)