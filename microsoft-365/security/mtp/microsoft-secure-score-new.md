---
title: Microsoft 보안 점수 신규
description: Microsoft 365 보안 센터의 Microsoft 보안 점수, 세부 정보를 계산 하는 방법 및 보안 관리자가이를 사용 하는 것으로 예상할 수 있는 사항에 대해 설명 합니다.
keywords: 보안, 맬웨어, Microsoft 365, M365, 보안 점수, 보안 센터, 개선 작업
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: article
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: 965b4cf872129dc7bc9b439c1c15025acceb44c6
ms.sourcegitcommit: 614666afb104fc97acb4a2ee5577ef63c0de153a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/09/2020
ms.locfileid: "44173554"
---
# <a name="microsoft-secure-score-new"></a><span data-ttu-id="ec221-104">Microsoft 보안 점수 (신규)</span><span class="sxs-lookup"><span data-stu-id="ec221-104">Microsoft Secure Score (new)</span></span>

>[!IMPORTANT]
><span data-ttu-id="ec221-105">Microsoft 보안 점수의이 새로운 반복은 이전 반복을 다음 몇 달 동안 새로운 디자인 요소 및 기능으로 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-105">This new iteration of Microsoft Secure Score is replacing the previous iteration with new design elements and features over the next few months</span></span>
>
><span data-ttu-id="ec221-106">기록 옆에 **메트릭 & 추세** 탭이 표시 되지 않으면 이전 반복에서 진행 되 고 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-106">If you DO NOT see a **Metrics & trends** tab next to History, you are in the previous iteration.</span></span> [<span data-ttu-id="ec221-107">Microsoft 보안 성과로 이동 (이전 반복)</span><span class="sxs-lookup"><span data-stu-id="ec221-107">Go to Microsoft Secure Score (previous iteration)</span></span>](microsoft-secure-score.md)

<span data-ttu-id="ec221-108">Microsoft 보안 점수는 조직의 보안 상태를 측정 한 값으로, 더 많은 향상 작업이 수행 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-108">Microsoft Secure Score is a measurement of an organization's security posture, with a higher number indicating more improvement actions taken.</span></span> <span data-ttu-id="ec221-109">이 도구는 https://security.microsoft.com/securescore [Microsoft 365 보안 센터](overview-security-center.md)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-109">It can be found at https://security.microsoft.com/securescore in the [Microsoft 365 security center](overview-security-center.md).</span></span>

<span data-ttu-id="ec221-110">보안 점수 권장 사항을 따르면 위협 으로부터 조직을 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-110">Following the Security Score recommendations can protect your organization from threats.</span></span> <span data-ttu-id="ec221-111">Microsoft 365 보안 센터의 중앙 집중식 대시보드를 통해 조직은 Microsoft 365 id, 데이터, 앱, 장치 및 인프라의 보안을 모니터링 하 고 작업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-111">From a centralized dashboard in the Microsoft 365 security center, organizations can monitor and work on the security of their Microsoft 365 identities, data, apps, devices, and infrastructure.</span></span>

<span data-ttu-id="ec221-112">보안 점수가 조직에 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-112">Secure Score helps organizations:</span></span>  

* <span data-ttu-id="ec221-113">조직의 보안 환경의 현재 상태를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-113">Report on the current state of the organization's security posture.</span></span>
* <span data-ttu-id="ec221-114">검색, 표시 유형, 지침 및 제어 기능을 제공 하 여 보안 환경을 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-114">Improve their security posture by providing discoverability, visibility, guidance, and control.</span></span>  
* <span data-ttu-id="ec221-115">벤치 마크와 비교 하 여 Kpi (핵심 성과 지표)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-115">Compare with benchmarks and establish key performance indicators (KPIs).</span></span>

<span data-ttu-id="ec221-116">조직은 메트릭 및 추세의 견고한 시각화, 다른 Microsoft 제품과의 통합, 비슷한 조직과의 점수 비교에 대 한 액세스 권한을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-116">Organizations gain access to robust visualizations of metrics and trends, integration with other Microsoft products, score comparison with similar organizations, and much more.</span></span> <span data-ttu-id="ec221-117">이 점수는 타사 솔루션에서 권장 작업을 해결 한 경우에도 반영 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-117">The score can also reflect when third-party solutions have addressed recommended actions.</span></span>

<span data-ttu-id="ec221-118">또한 [Microsoft GRAPH API](https://www.microsoft.com/security/partnerships/graph-security-api)를 통해 권장 사항 및 점수에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-118">Additionally, you can access your recommendations and score through the [Microsoft Graph API](https://www.microsoft.com/security/partnerships/graph-security-api).</span></span> <span data-ttu-id="ec221-119">[보안 점수 리소스 종류](https://go.microsoft.com/fwlink/?linkid=2092996)에 대해 자세히 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-119">Learn about the [Secure Score resource type](https://go.microsoft.com/fwlink/?linkid=2092996).</span></span>

## <a name="how-it-works"></a><span data-ttu-id="ec221-120">작동 방식</span><span class="sxs-lookup"><span data-stu-id="ec221-120">How it works</span></span>

<span data-ttu-id="ec221-121">권장 되는 보안 기능을 구성 하 고, 보안 관련 작업을 수행 하거나, 타사 응용 프로그램 또는 소프트웨어를 사용 하 여 개선 작업을 처리 하거나, 대체 문제를 해결 하기 위한 사항이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-121">You are given points for configuring recommended security features, performing security-related tasks, or addressing the improvement action with a third-party application or software, or an alternate mitigation.</span></span> <span data-ttu-id="ec221-122">일부 향상 작업은 완전히 완료 된 경우에만 점수를 제공 하며 일부 장치 또는 사용자에 대해 완료 되 면 일부를 부분 포인트로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-122">Some improvement actions only give points when fully completed, and some give partial points if they are completed for some devices or users.</span></span> <span data-ttu-id="ec221-123">개선 작업 중 하나를 규정 하지 않으려는 경우 위험 또는 남은 위험을 수락 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-123">If you cannot or do not want to enact one of the improvement actions, you can choose to accept the risk or the remaining risk.</span></span>

<span data-ttu-id="ec221-124">라이선스에 관계 없이 향상 된 가능한 전체 기능을 제공 하 여 보안 모범 사례를 이해 하 고 점수를 높일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-124">We show you the full set of possible improvements, regardless of license, so you can understand security best practices and improve your score.</span></span> <span data-ttu-id="ec221-125">절대 보안 상태는 조직이 소유한 제품 라이선스에 관계 없이 동일 하 게 유지 되는 보안 점수를 통해 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-125">Your absolute security posture is represented by Secure Score, which stays the same no matter what product licenses your organization owns.</span></span> <span data-ttu-id="ec221-126">보안은 유용성과 균형을 유지 해야 하며 모든 권장 사항이 환경에 적합 한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-126">Keep in mind that security should be balanced with usability, and not every recommendation can work for your environment.</span></span>

<span data-ttu-id="ec221-127">점수가 실시간으로 업데이트 되어 시각화 및 향상 작업 페이지에 제공 된 정보를 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-127">Your score is updated in real time to reflect the information presented in the visualizations and improvement action pages.</span></span> <span data-ttu-id="ec221-128">또한 보안 점수가 매일 동기화 되어 각 작업에 대 한 시스템 데이터를 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-128">Secure Score also syncs daily to receive system data about your achieved points for each action.</span></span>

### <a name="how-improvement-actions-are-scored"></a><span data-ttu-id="ec221-129">개선 작업의 점수를 획득 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ec221-129">How improvement actions are scored</span></span>

<span data-ttu-id="ec221-130">각 향상 작업은 10 점 이내에 가치가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-130">Each improvement action is worth 10 points or less.</span></span> <span data-ttu-id="ec221-131">대부분은 이진 방식으로 점수가 지정 되며, 새 정책 만들기 또는 특정 설정을 사용 하는 것과 같은 개선 작업을 구현 하는 경우에는 점수가 100% 인 점수를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-131">Most are scored in a binary fashion — if you implement the improvement action, like create a new policy or turn on a specific setting, you get 100% of the points.</span></span> <span data-ttu-id="ec221-132">다른 향상 작업의 경우 점수는 전체 구성에 대 한 비율로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-132">For other improvement actions, points are given as a percentage of the total configuration.</span></span> <span data-ttu-id="ec221-133">예를 들어, 향상 된 작업에 다단계 인증을 사용 하 여 모든 사용자를 보호 하 여 30 점을 제공 하 고 총 사용자 수가 5 100 인 경우, 2 포인트 (5 개의 보호/100 총 \* 30 최대 포인트 = 2 포인트)의 부분적인 점수가 부여 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-133">For example, if the improvement action states you get 30 points by protecting all your users with multi-factor authentication and you only have 5 of 100 total users protected, you would be given a partial score of around 2 points (5 protected / 100 total \* 30 max pts = 2 pts partial score).</span></span>

### <a name="products-included-in-secure-score"></a><span data-ttu-id="ec221-134">안전한 점수에 포함 된 제품</span><span class="sxs-lookup"><span data-stu-id="ec221-134">Products included in Secure Score</span></span>

<span data-ttu-id="ec221-135">현재 Microsoft 365 (Exchange Online 포함), Azure AD, Microsoft Defender ATP, Azure ATP 및 Cloud App Security에 대 한 권장 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-135">Currently there are recommendations for Microsoft 365 (including Exchange Online), Azure AD, Microsoft Defender ATP, Azure ATP, and Cloud App Security.</span></span> <span data-ttu-id="ec221-136">다른 보안 제품에 대 한 권장 사항은 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-136">Recommendations for other security products are coming soon.</span></span> <span data-ttu-id="ec221-137">권장 사항은 각 제품과 연결 된 모든 공격 표면을 다루지는 않지만 좋은 기준이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-137">The recommendations will not cover all the attack surfaces associated with each product, but they are a good baseline.</span></span> <span data-ttu-id="ec221-138">또한 제 3 자 또는 다른 완화 조치로 인 한 향상 작업을 표시할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-138">You can also mark the improvement actions as covered by a third party or alternate mitigation.</span></span>

## <a name="required-permissions"></a><span data-ttu-id="ec221-139">필요한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="ec221-139">Required permissions</span></span>

<span data-ttu-id="ec221-140">Microsoft 보안 점수에 액세스할 수 있는 권한을 부여 하려면 Azure Active Directory에서 다음 역할 중 하나를 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-140">To have permission to access Microsoft Secure Score, you must be assigned one of the following roles in Azure Active Directory.</span></span>

### <a name="read-and-write-roles"></a><span data-ttu-id="ec221-141">읽기 및 쓰기 역할</span><span class="sxs-lookup"><span data-stu-id="ec221-141">Read and write roles</span></span>

<span data-ttu-id="ec221-142">읽기 및 쓰기 액세스를 사용 하 여 변경을 수행 하 고 보안 점수와 직접 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-142">With read and write access, you can make changes and directly interact with Secure Score.</span></span> <span data-ttu-id="ec221-143">또한 다른 사용자에 게 읽기 전용 액세스 권한을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-143">You can also assign read-only access to other users.</span></span>

* <span data-ttu-id="ec221-144">전역 관리자</span><span class="sxs-lookup"><span data-stu-id="ec221-144">Global administrator</span></span>
* <span data-ttu-id="ec221-145">보안 관리자</span><span class="sxs-lookup"><span data-stu-id="ec221-145">Security administrator</span></span>
* <span data-ttu-id="ec221-146">Exchange 관리자</span><span class="sxs-lookup"><span data-stu-id="ec221-146">Exchange administrator</span></span>
* <span data-ttu-id="ec221-147">SharePoint 관리자</span><span class="sxs-lookup"><span data-stu-id="ec221-147">SharePoint administrator</span></span>
* <span data-ttu-id="ec221-148">계정 관리자</span><span class="sxs-lookup"><span data-stu-id="ec221-148">Account administrator</span></span>

### <a name="read-only-roles"></a><span data-ttu-id="ec221-149">읽기 전용 역할</span><span class="sxs-lookup"><span data-stu-id="ec221-149">Read-only roles</span></span>

<span data-ttu-id="ec221-150">읽기 전용 액세스 권한을 사용 하면 향상 작업에 대 한 상태나 메모를 편집 하거나, 점수 영역을 편집 하거나, 사용자 지정 비교를 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-150">With read-only access, you are not able to edit status or notes for an improvement action, edit score zones, or edit custom comparisons.</span></span>

* <span data-ttu-id="ec221-151">헬프데스크 관리자</span><span class="sxs-lookup"><span data-stu-id="ec221-151">Helpdesk administrator</span></span>
* <span data-ttu-id="ec221-152">사용자 관리자</span><span class="sxs-lookup"><span data-stu-id="ec221-152">User administrator</span></span>
* <span data-ttu-id="ec221-153">서비스 관리자</span><span class="sxs-lookup"><span data-stu-id="ec221-153">Service administrator</span></span>
* <span data-ttu-id="ec221-154">보안 읽기 권한자</span><span class="sxs-lookup"><span data-stu-id="ec221-154">Security reader</span></span>
* <span data-ttu-id="ec221-155">보안 운영자</span><span class="sxs-lookup"><span data-stu-id="ec221-155">Security operator</span></span>
* <span data-ttu-id="ec221-156">전역 읽기 권한자</span><span class="sxs-lookup"><span data-stu-id="ec221-156">Global reader</span></span>

### <a name="graph-api"></a><span data-ttu-id="ec221-157">Graph API</span><span class="sxs-lookup"><span data-stu-id="ec221-157">Graph API</span></span>

<span data-ttu-id="ec221-158">그래프 API에 액세스 하려면 역할 외에 다음 범위 중 하나를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-158">To access the Graph API, you need to have one of the following scopes in addition to a role:</span></span>

* <span data-ttu-id="ec221-159">SecurityEvents. All (읽기 전용 역할의 경우)</span><span class="sxs-lookup"><span data-stu-id="ec221-159">SecurityEvents.Read.All (for read-only roles)</span></span>
* <span data-ttu-id="ec221-160">SecurityEvents. All (읽기 및 쓰기 역할 용)</span><span class="sxs-lookup"><span data-stu-id="ec221-160">SecurityEvents.ReadWrite.All (for read and write roles)</span></span>

## <a name="gain-visibility-into-your-security-posture"></a><span data-ttu-id="ec221-161">보안 환경을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-161">Gain visibility into your security posture</span></span>

<span data-ttu-id="ec221-162">필요한 정보를 보다 신속 하 게 지원 하기 위해 Microsoft 개선 작업을 그룹으로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-162">To help you the information you need more quickly, Microsoft improvement actions are organized into groups:</span></span>

* <span data-ttu-id="ec221-163">Id (Azure AD 계정 & 역할)</span><span class="sxs-lookup"><span data-stu-id="ec221-163">Identity (Azure AD accounts & roles)</span></span>
* <span data-ttu-id="ec221-164">데이터 (Microsoft Information Protection)</span><span class="sxs-lookup"><span data-stu-id="ec221-164">Data  (Microsoft Information Protection)</span></span>
* <span data-ttu-id="ec221-165">장치 (Microsoft Defender ATP)</span><span class="sxs-lookup"><span data-stu-id="ec221-165">Device (Microsoft Defender ATP)</span></span>
* <span data-ttu-id="ec221-166">앱 (Office 365 및 Microsoft Cloud App Security)을 포함 하는 전자 메일 및 클라우드 앱</span><span class="sxs-lookup"><span data-stu-id="ec221-166">App (email and cloud apps, including Office 365 and Microsoft Cloud App Security)</span></span>
* <span data-ttu-id="ec221-167">인프라 (지금은 향상 작업 없음)</span><span class="sxs-lookup"><span data-stu-id="ec221-167">Infrastructure (no improvement actions for now)</span></span>

<span data-ttu-id="ec221-168">Microsoft 보안 점수 개요 페이지에서 이러한 그룹 간의 점수가 분할 되는 방식과 사용할 수 있는 지점을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-168">In the Microsoft Secure Score overview page, you can see how points are split between these groups and what points are available.</span></span> <span data-ttu-id="ec221-169">개요 페이지는 또한 전체 점수에 대 한 모든 보기, 벤치 마크 비교를 사용한 보안 점수의 역사적 추세 및 점수를 높이기 위해 수행할 수 있는 향상 작업의 우선 순위를 지정 하는 위치를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-169">The overview page is also the place to get an all-up view of the total score, historical trend of your secure score with benchmark comparisons, and prioritized improvement actions that can be taken to improve your score.</span></span>

![보안 점수 홈페이지](../../media/secure-score/secure-score-homepage-new.png)


## <a name="take-action-to-improve-your-score"></a><span data-ttu-id="ec221-171">점수를 개선 하기 위한 조치 수행</span><span class="sxs-lookup"><span data-stu-id="ec221-171">Take action to improve your score</span></span>

<span data-ttu-id="ec221-172">**향상 작업** 탭에는 가능한 공격 지를 확인 하는 보안 권장 사항과 함께 해당 상태 (주소, 계획 된 위험, 허용 됨, 제 3 자가 해결 됨, 대안 완화 및 완료 됨)가 함께 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-172">The **Improvement actions** tab lists the security recommendations that address possible attack surfaces, along with their status (to address, planned, risk accepted, resolved through third party, resolved through alternate mitigation, and completed).</span></span> <span data-ttu-id="ec221-173">모든 개선 작업을 검색, 필터링 및 그룹화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-173">You can search, filter, and group all the improvement actions.</span></span>  

### <a name="ranking"></a><span data-ttu-id="ec221-174">순서</span><span class="sxs-lookup"><span data-stu-id="ec221-174">Ranking</span></span>

<span data-ttu-id="ec221-175">순위는 달성할 수 있는 남은 점수, 구현 난이도, 사용자 영향 및 복잡도를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-175">Ranking is based on the number of remaining points left to achieve, implementation difficulty, user impact, and complexity.</span></span> <span data-ttu-id="ec221-176">가장 높은 순위의 향상 작업에는 낮은 난이도, 사용자 영향 및 복잡도의 점수가 많이 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-176">The highest ranked improvement actions have a large number of points remaining with low difficulty, user impact, and complexity.</span></span>

### <a name="view-improvement-action-details"></a><span data-ttu-id="ec221-177">향상 작업 세부 정보 보기</span><span class="sxs-lookup"><span data-stu-id="ec221-177">View improvement action details</span></span>

<span data-ttu-id="ec221-178">특정 향상 작업을 선택 하면 전체 페이지 플라이 아웃이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-178">When you select a specific improvement action, a full page flyout appears.</span></span>  

<span data-ttu-id="ec221-179">![향상 작업 플라이 아웃](../../media/secure-score/secure-score-improvement-action-details.png)
예*그림 2: 개선 작업 플라이 아웃 예제*</span><span class="sxs-lookup"><span data-stu-id="ec221-179">![Improvement action flyout example](../../media/secure-score/secure-score-improvement-action-details.png)
*Figure 2: Improvement action flyout example*</span></span>

<span data-ttu-id="ec221-180">이 작업을 완료 하려면 몇 가지 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-180">To complete the action, you have a few options:</span></span>

* <span data-ttu-id="ec221-181">**관리** 를 선택 하 여 구성 화면으로 이동 하 고 변경을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-181">Select **Manage** to go the configuration screen and make the change.</span></span> <span data-ttu-id="ec221-182">그런 다음 동작이 가치 있는 점수를 얻게 되며 플라이 아웃 됩니다. 점수는 일반적으로 업데이트 하는 데 약 24 시간이 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-182">You will then gain the points that the action is worth, visible in the fly out. Points generally take about 24 hours to update.</span></span>

* <span data-ttu-id="ec221-183">**공유** 를 선택 하 여 개선 작업에 대 한 직접 링크를 복사 하거나, 전자 메일, microsoft 팀, Microsoft Planner 또는 ServiceNow와 같은 링크를 공유할 플랫폼을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-183">Select **Share** to copy the direct link to the improvement action, or choose the platform to share the link such as email, Microsoft Teams, Microsoft Planner, or ServiceNow.</span></span> <span data-ttu-id="ec221-184">ServiceNow를 선택 하면 ServiceNow 및 Microsoft 365 보안 센터 홈에 표시 되는 변경 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-184">Selecting ServiceNow will let you create a change ticket which will be visible in ServiceNow and the Microsoft 365 security center home.</span></span> <span data-ttu-id="ec221-185">자세한 내용은 [Microsoft 365 보안 센터 및 ServiceNow 통합](tickets.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ec221-185">To learn more, see [Microsoft 365 Security Center and ServiceNow integration](tickets.md).</span></span>

### <a name="choose-an-improvement-action-status"></a><span data-ttu-id="ec221-186">향상 작업 상태 선택</span><span class="sxs-lookup"><span data-stu-id="ec221-186">Choose an improvement action status</span></span>

<span data-ttu-id="ec221-187">상태를 선택 하 고 향상 작업과 관련 된 메모를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-187">Choose any statuses and record notes specific to the improvement action.</span></span> <span data-ttu-id="ec221-188">선택할 수 있는 동상은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-188">The statues you can select are the following:</span></span>

* <span data-ttu-id="ec221-189">**해결 방법** : 개선 작업이 필요한 지를 인식 하 고 미래에 특정 시점에 해결할 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-189">**To address** — You recognize that the improvement action is necessary and plan to address it at some point in the future.</span></span> <span data-ttu-id="ec221-190">이 상태는 부분적으로 검색 되었지만 완전히 완료 되지 않은 작업에도 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-190">This state also applies to actions which are detected as partially, but not fully completed.</span></span>
* <span data-ttu-id="ec221-191">**계획** 됨-개선 작업을 완료 하기 위한 구체적인 계획이 마련 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-191">**Planned** — There are concrete plans in place to complete the improvement action.</span></span>
* <span data-ttu-id="ec221-192">**위험 수락** -보안이 항상 유용성과 균형을 유지 해야 하며, 환경에 대 한 모든 권장 사항이 적합 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-192">**Risk accepted** — Security should always be balanced with usability, and not every recommendation will work for your environment.</span></span> <span data-ttu-id="ec221-193">이 경우 위험 또는 남은 위험을 수락 하 고 개선 작업을 적용 하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-193">When that is the case, you can choose to accept the risk, or the remaining risk, and not enact the improvement action.</span></span> <span data-ttu-id="ec221-194">모든 점수를 제공 하는 것은 아니지만 해당 작업은 개선 작업 목록에 더 이상 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-194">You will not be given any points, but the action will no longer be visible in the list of improvement actions.</span></span> <span data-ttu-id="ec221-195">언제 든 지 기록에서이 작업을 보거나 실행 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-195">You can view this action in history or undo it at any time.</span></span>
* <span data-ttu-id="ec221-196">타사 응용 프로그램 또는 소프트웨어 또는 내부 도구로 이미 향상 된 기능을 사용 하 여 타사에서 **확인** 하 고 **다른 완화 작업을 통해 해결** 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-196">**Resolved through third party** and **Resolved through alternate mitigation** — The improvement action has already been addressed by a third-party application or software, or an internal tool.</span></span> <span data-ttu-id="ec221-197">작업을 수행 하는 점수를 얻게 되므로 점수가 향상 되어 전반적인 보안 환경을 보다 효율적으로 반영할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-197">You will gain the points that the action is worth, so your score better reflects your overall security posture.</span></span> <span data-ttu-id="ec221-198">타사 또는 내부 도구가 더 이상 해당 컨트롤을 커버 하지 않으면 다른 상태를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-198">If a third party or internal tool no longer covers the control, you can choose another status.</span></span> <span data-ttu-id="ec221-199">향상 작업이 이러한 상태 중 하나로 표시 되는 경우 Microsoft는 구현의 완성도를 명확 하 게 파악할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-199">Please keep in mind, Microsoft will have no visibility into the completeness of implementation if the improvement action is marked as either of these statuses.</span></span>

#### <a name="threat--vulnerability-management-improvement-actions"></a><span data-ttu-id="ec221-200">위협 & 취약성 관리 개선 작업</span><span class="sxs-lookup"><span data-stu-id="ec221-200">Threat & Vulnerability Management improvement actions</span></span>

<span data-ttu-id="ec221-201">"장치" 범주의 향상 작업을 수행 하는 경우 상태를 선택할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-201">For improvement actions in the "Device" category, you will not be able to choose statuses.</span></span> <span data-ttu-id="ec221-202">대신 [Microsoft Defender 보안 센터](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/use) 의 [tvm (& 취약성 관리) 보안 권장 사항을](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/tvm-security-recommendation) 연결 하 여 조치를 취할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-202">Instead, you will be directed to the associated [Threat & Vulnerability Management (TVM) security recommendation](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/tvm-security-recommendation) in the [Microsoft Defender Security Center](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/use) to take action.</span></span> <span data-ttu-id="ec221-203">선택한 예외 및 작성 한 사유는 해당 포털에만 적용 되며 Microsoft 보안 점수 포털에는 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-203">The exception you choose and justification you write will specific to that portal, and will not be present in the Microsoft Secure Score portal.</span></span>

#### <a name="completed-improvement-actions"></a><span data-ttu-id="ec221-204">완료 된 개선 작업</span><span class="sxs-lookup"><span data-stu-id="ec221-204">Completed improvement actions</span></span>

<span data-ttu-id="ec221-205">향상 작업에 대 한 가능한 모든 점수를 얻은 후에는 개선 조치에 "완료 됨" 상태가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-205">Improvement actions have a "completed" status once all possible points for the improvement action have been achieved.</span></span> <span data-ttu-id="ec221-206">완료 된 개선 작업은 Microsoft 데이터를 통해 확인 되며 상태를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-206">Completed improvement actions are confirmed though Microsoft data, and you will not be able to change the status.</span></span>

### <a name="assess-information-and-review-user-impact"></a><span data-ttu-id="ec221-207">정보 평가 및 사용자 영향 검토</span><span class="sxs-lookup"><span data-stu-id="ec221-207">Assess information and review user impact</span></span>

<span data-ttu-id="ec221-208">**살펴보기** 섹션에는 범주, 제품에 대해 보호할 수 있는 공격 및 제품이 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-208">The **At a glance** section will tell you the category, attacks it can protect against, and the product.</span></span>

<span data-ttu-id="ec221-209">**사용자 영향** 에 따라 개선 작업이 실행 되는 경우 사용자에 게 발생할 항목이 표시 되 고, **영향을 받는 사용자** 에 게는이를 표시할 사람이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-209">The **User impact** shows what the users will experience if the improvement action is enacted, and **Users affected** shows who will experience it.</span></span>

### <a name="implement-the-improvement-action"></a><span data-ttu-id="ec221-210">개선 작업 구현</span><span class="sxs-lookup"><span data-stu-id="ec221-210">Implement the improvement action</span></span>

<span data-ttu-id="ec221-211">**구현** 섹션에서는 다음 단계에 따라 개선 작업을 완료 하기 위한 단계, 개선 작업의 현재 구현 상태 및 자세한 링크를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-211">The **Implementation** section shows any prerequisites, step by step next steps to complete the improvement action, the current implementation status of the improvement action, and any learn more links.</span></span>

<span data-ttu-id="ec221-212">필수 구성 요소는 개선 작업을 처리 하기 전에 완료 해야 하는 작업 또는 획득 해야 하는 모든 라이선스가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-212">Prerequisites will be any licenses that need to be obtained or actions that need to be completed before the improvement action is addressed.</span></span> <span data-ttu-id="ec221-213">라이선스에 개선 작업을 완료 하 고 해당 라이선스가 필요한 사용자에 게 적용 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-213">Make sure you have enough seats in your license to complete the improvement action and that those licenses are applied to the necessary users.</span></span>  

## <a name="track-your-score-history-and-meet-goals"></a><span data-ttu-id="ec221-214">점수 내역 추적 및 목표 달성</span><span class="sxs-lookup"><span data-stu-id="ec221-214">Track your score history and meet goals</span></span>

<span data-ttu-id="ec221-215">**기록** 탭에서 시간에 따른 조직의 점수 그래프를 볼 수 있습니다. 그래프 아래에 선택한 시간 범위에 적용 된 모든 작업 및 결과 점과 범주와 같은 해당 특성의 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-215">You can view a graph of your organization's score over time in the **History** tab. Below the graph is a list of all the actions taken in the selected time range and their attributes, such as resulting points and category.</span></span> <span data-ttu-id="ec221-216">날짜 범위를 사용자 지정 하 고 범주별로 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-216">You can customize a date range and filter by category.</span></span>

<span data-ttu-id="ec221-217">**메트릭 & 추세** 탭에는 다양 한 그래프와 차트를 통해 추세를 보다 명확 하 게 표시 하 고 목표를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-217">In the **Metrics & trends** tab, there are several graphs and charts to give you more visibility into trends and set goals.</span></span> <span data-ttu-id="ec221-218">시각화의 전체 페이지에 대 한 날짜 범위를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-218">You can set the date range for the whole page of visualizations.</span></span> <span data-ttu-id="ec221-219">시각화에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-219">The visualizations include:</span></span>

* <span data-ttu-id="ec221-220">**보안 점수 영역** — 조직의 목표 및 양호한 점수, 양호 및 불량 점수의 범위에 따라 사용자 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-220">**Your Secure Score zone** — Customized based on your organization's goals and definitions of good, okay, and bad score ranges.</span></span>
* <span data-ttu-id="ec221-221">**회귀 추세** -구성, 사용자 또는 장치 변경으로 인해 회귀 된 지점에 대 한 시간 표시 막대입니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-221">**Regression trend** — A timeline of points that have regressed due to configuration, user, or device changes.</span></span>  
* <span data-ttu-id="ec221-222">**비교 추세** — 조직의 보안 점수가 다른 사람들과 비교 하는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-222">**Comparison trend** — How your organization's Secure Score compares to others' over time.</span></span> <span data-ttu-id="ec221-223">이 보기에는 비슷한 사용자 수를 갖는 조직의 점수 평균을 나타내는 줄과 설정할 수 있는 custom 비교 보기가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-223">This view can include lines representing the score average of organizations with similar seat count and a custom comparison view that you can set.</span></span>
* <span data-ttu-id="ec221-224">**위험 수락 추세** — "위험 수용 됨"으로 표시 된 개선 작업의 시간 표시 막대입니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-224">**Risk acceptance trend** — Timeline of improvement actions marked as "risk accepted."</span></span>
* <span data-ttu-id="ec221-225">**점수 변경** -지정 된 날짜 범위에서 이후의 점수 변경과 함께 회귀 됨을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-225">**Score changes** — The number of points achieved, points regressed, along with the subsequent score change, in the specified date range.</span></span>

## <a name="risk-awareness"></a><span data-ttu-id="ec221-226">위험 인식</span><span class="sxs-lookup"><span data-stu-id="ec221-226">Risk awareness</span></span>

<span data-ttu-id="ec221-227">Microsoft 보안 점수는 시스템 구성, 사용자 동작 및 기타 보안 관련 측정값을 기반으로 한 보안 환경을 나타내는 수치 요약입니다. 시스템 또는 데이터를 얼마나 많이 침해 해야 하는지 절대 측정 한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-227">Microsoft Secure Score is a numerical summary of your security posture based on system configurations, user behavior and other security related measurements; it is not an absolute measurement of how likely your system or data will be breached.</span></span> <span data-ttu-id="ec221-228">대신 Microsoft 환경에서 보안 제어를 채택 하는 범위를 나타내므로 위반 위험을 상쇄 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-228">Rather, it represents the extent to which you have adopted security controls in your Microsoft environment which can help offset the risk of being breached.</span></span> <span data-ttu-id="ec221-229">보안 침해에의 한 온라인 서비스에는 전혀 문제가 되지 않으며 보안 점수가 보안상 침해에 대 한 보장으로 해석 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-229">No online service is completely immune from security breaches, and secure score should not be interpreted as a guarantee against security breach in any manner.</span></span>

## <a name="whats-new"></a><span data-ttu-id="ec221-230">어떠한 새로운 기능이 있나요?</span><span class="sxs-lookup"><span data-stu-id="ec221-230">What's new?</span></span> 

<span data-ttu-id="ec221-231">Microsoft 보안 점수가 보안 상태를 보다 효율적으로 대표 하도록 하기 위해 몇 가지 사항을 변경 했습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-231">To make Microsoft Secure Score a better representative of your security posture, we have made some changes.</span></span> <span data-ttu-id="ec221-232">계획 된 변경 사항에 대 한 자세한 내용은 [Microsoft 보안 점수에서](microsoft-secure-score-whats-coming.md)제공 되는 기능을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ec221-232">To learn about planned changes, see [What's coming in Microsoft Secure Score?](microsoft-secure-score-whats-coming.md).</span></span>

- <span data-ttu-id="ec221-233">Azure Active Directory 개선 작업 추가 됨</span><span class="sxs-lookup"><span data-stu-id="ec221-233">Added Azure Active Directory improvement actions</span></span>
- <span data-ttu-id="ec221-234">Azure Advanced Threat Protection 개선 작업 추가</span><span class="sxs-lookup"><span data-stu-id="ec221-234">Added Azure Advanced Threat Protection improvement actions</span></span>
- <span data-ttu-id="ec221-235">Microsoft Defender ATP [위협 & 취약성 관리](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) 보안 권장 사항에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="ec221-235">Support for Microsoft Defender ATP [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) security recommendations</span></span>
    - <span data-ttu-id="ec221-236">이제 TVM에서 제공 하는 모든 릴리스된 보안 권장 사항을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-236">All released security recommendations supplied by TVM are now available</span></span>

### <a name="updated-interface-and-functionality"></a><span data-ttu-id="ec221-237">업데이트 된 인터페이스 및 기능</span><span class="sxs-lookup"><span data-stu-id="ec221-237">Updated interface and functionality</span></span>

* <span data-ttu-id="ec221-238">CISO 팀장 수준 토론을 위한 모든 새 메트릭 및 추세 보기</span><span class="sxs-lookup"><span data-stu-id="ec221-238">All new metrics and trends views for CISO and lead level discussions</span></span>
* <span data-ttu-id="ec221-239">점수를 추적 하 고 벤치 마크 위한 새로운 방법</span><span class="sxs-lookup"><span data-stu-id="ec221-239">New ways to track and benchmark your score</span></span>
* <span data-ttu-id="ec221-240">점수 재발에 대 한 추적 및 이해 향상</span><span class="sxs-lookup"><span data-stu-id="ec221-240">Better tracking and understanding for score regressions</span></span>
* <span data-ttu-id="ec221-241">개선 작업 필터링, 태그, 검색 및 그룹화</span><span class="sxs-lookup"><span data-stu-id="ec221-241">Filter, tag, search, and group your improvement actions</span></span>
* <span data-ttu-id="ec221-242">점수 예측 및 계획 된 작업을 사용 하 여 향후 목표를 향해 관리</span><span class="sxs-lookup"><span data-stu-id="ec221-242">Manage towards your future goals using score projections and planned actions</span></span>
* <span data-ttu-id="ec221-243">더 많은 내용을 확인해 보세요.</span><span class="sxs-lookup"><span data-stu-id="ec221-243">And more!</span></span>

## <a name="we-want-to-hear-from-you"></a><span data-ttu-id="ec221-244">사용자의 의견을 듣고 싶습니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-244">We want to hear from you</span></span>

<span data-ttu-id="ec221-245">문제가 있는 경우 [보안, 개인 정보 & 준수](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) 커뮤니티에서 게시할 때 알려주십시오.</span><span class="sxs-lookup"><span data-stu-id="ec221-245">If you have any issues, please let us know by posting in the [Security, Privacy & Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) community.</span></span> <span data-ttu-id="ec221-246">당사는 커뮤니티를 모니터링 하 고 도움이 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ec221-246">We're monitoring the community and will provide help.</span></span>