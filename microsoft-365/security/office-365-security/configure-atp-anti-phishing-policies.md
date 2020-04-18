---
title: ATP 피싱 방지 정책 구성
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: ''
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: 관리자는 Office 365 ATP (Advanced Threat Protection)가 있는 조직에서 사용할 수 있는 고급 피싱 방지 정책을 만들고, 수정 하 고, 삭제 하는 방법에 대해 알아볼 수 있습니다.
ms.openlocfilehash: b0316133c90837bedc657bde355f31d50ffe76ea
ms.sourcegitcommit: db8702cf578b02c6fd6a2670c177b456efae4748
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "43537464"
---
# <a name="configure-atp-anti-phishing-policies-in-office-365"></a><span data-ttu-id="adcbc-103">Office 365에서 ATP 피싱 방지 정책 구성</span><span class="sxs-lookup"><span data-stu-id="adcbc-103">Configure ATP anti-phishing policies in Office 365</span></span>

<span data-ttu-id="adcbc-104">ATP 피싱 방지 정책은 [Office 365 Advanced Threat Protection](office-365-atp.md)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-104">ATP anti-phishing policies are part of [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="adcbc-105">ATP 피싱 방지 정책은 악의 있는 가장 기반 피싱 공격과 기타 유형의 피싱 공격 으로부터 조직을 보호 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-105">ATP anti-phishing policies can help protect your organization from malicious impersonation-based phishing attacks and other types of phishing attacks.</span></span> <span data-ttu-id="adcbc-106">EOP (Exchange Online Protection)의 피싱 방지 정책, ATP 피싱 방지 정책 간의 차이점에 대 한 자세한 내용은 [Office 365의 피싱 방지 보호](anti-phishing-protection.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="adcbc-106">For more information about the differences between anti-phishing policies in Exchange Online Protection (EOP) and ATP anti-phishing policies, see [Anti-phishing protection in Office 365](anti-phishing-protection.md).</span></span>

<span data-ttu-id="adcbc-107">관리자는 기본 ATP 피싱 방지 정책을 보고, 편집 하 고, 구성 하 고, 삭제할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-107">Admins can view, edit, and configure (but not delete) the default ATP anti-phishing policy.</span></span> <span data-ttu-id="adcbc-108">세분성을 높이기 위해 조직의 특정 사용자, 그룹 또는 도메인에 적용 되는 사용자 지정 ATP 피싱 방지 정책을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-108">For greater granularity, you can also create custom ATP anti-phishing policies that apply to specific users, groups, or domains in your organization.</span></span> <span data-ttu-id="adcbc-109">사용자 지정 정책은 항상 기본 정책보다 우선하지만, 사용자 지정 정책의 우선순위(실행 순서)를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-109">Custom policies always take precedence over the default policy, but you can change the priority (running order) of your custom policies.</span></span>

<span data-ttu-id="adcbc-110">Office 365 보안 & 준수 센터 또는 Exchange Online PowerShell에서 ATP 피싱 방지 정책을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-110">You can configure ATP anti-phishing policies in the Office 365 Security & Compliance Center or in Exchange Online PowerShell.</span></span>

<span data-ttu-id="adcbc-111">Exchange Online Protection 조직 (즉, ATP가 없는 Office 365 조직)에서 사용할 수 있는 제한 된 기본 제공 피싱 방지 정책을 구성 하는 방법에 대 한 자세한 내용은 [EOP에서 기본 피싱 방지 정책 구성을](configure-anti-phishing-policies-eop.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-111">For information about configuring the more limited built-in anti-phishing policy that's available in Exchange Online Protection organizations (that is, Office 365 organizations without ATP), see [Configure the default anti-phishing policy in EOP](configure-anti-phishing-policies-eop.md).</span></span>

## <a name="atp-anti-phishing-policies-in-the-office-365-security--compliance-center-vs-exchange-online-powershell"></a><span data-ttu-id="adcbc-112">Office 365 보안 & 준수 센터 vs Exchange Online PowerShell의 ATP 피싱 방지 정책</span><span class="sxs-lookup"><span data-stu-id="adcbc-112">ATP anti-phishing policies in the Office 365 Security & Compliance Center vs Exchange Online PowerShell</span></span>

<span data-ttu-id="adcbc-113">ATP 피싱 방지 정책의 기본 요소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-113">The basic elements of an ATP anti-phishing policy are:</span></span>

- <span data-ttu-id="adcbc-114">**피싱 정책**: 사용 하거나 사용 하지 않도록 설정할 피싱 보호를 지정 하 고 옵션을 적용 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-114">**The anti-phish policy**: Specifies the phishing protections to enable or disable, and the actions to apply options.</span></span>

- <span data-ttu-id="adcbc-115">**피싱 규칙**: 피싱 정책에 대해 정책이 적용 되는 우선 순위 및 받는 사람 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-115">**The anti-phish rule**: Specifies the priority and recipient filters (who the policy applies to) for an anti-phish policy.</span></span>

<span data-ttu-id="adcbc-116">보안 & 준수 센터에서 ATP 피싱 방지 정책을 관리할 때는 이러한 두 가지 요소 간의 차이가 명확 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-116">The difference between these two elements isn't obvious when you manage ATP anti-phishing policies in the Security & Compliance Center:</span></span>

- <span data-ttu-id="adcbc-117">보안 & 준수 센터에서 ATP 피싱 방지 정책을 만드는 경우 실제로는 피싱 규칙과 연결 된 피싱 정책을 모두 같은 이름을 사용 하 여 동시에 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-117">When you create an ATP anti-phishing policy in the Security & Compliance Center, you're actually creating an anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

- <span data-ttu-id="adcbc-118">보안 & 준수 센터에서 ATP 피싱 방지 정책을 수정 하면 이름, 우선 순위, 사용/사용 안 함 및 받는 사람 필터와 관련 된 설정이 피싱 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-118">When you modify an ATP anti-phishing policy in the Security & Compliance Center, settings related to the name, priority, enabled or disabled, and recipient filters modify the anti-phish rule.</span></span> <span data-ttu-id="adcbc-119">다른 모든 설정은 연결 된 피싱 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-119">All other settings modify the associated anti-phish policy.</span></span>

- <span data-ttu-id="adcbc-120">보안 & 준수 센터에서 ATP 피싱 방지 정책을 제거 하면 피싱 규칙과 연결 된 피싱 정책이 모두 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-120">When you remove an ATP anti-phishing policy from the Security & Compliance Center, the anti-phish rule and the associated anti-phish policy are removed.</span></span>

<span data-ttu-id="adcbc-121">Exchange Online PowerShell에서 피싱 정책 및 피싱 규칙 간의 차이가 명백 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-121">In Exchange Online PowerShell, the difference between anti-phish policies and anti-phish rules is apparent.</span></span> <span data-ttu-id="adcbc-122">-AntiPhishPolicy cmdlet을 사용 하 여 피싱 정책을 관리 하 고 \*\* \*-AntiPhishRule\*\* cmdlet을 사용 하 여 피싱 규칙을 관리 합니다. \*\* \*\*\*</span><span class="sxs-lookup"><span data-stu-id="adcbc-122">You manage anti-phish policies by using the **\*-AntiPhishPolicy** cmdlets, and you manage anti-phish rules by using the **\*-AntiPhishRule** cmdlets.</span></span>

- <span data-ttu-id="adcbc-123">PowerShell에서는 먼저 피싱 정책을 만든 다음 규칙이 적용 되는 정책을 식별 하는 피싱 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-123">In PowerShell, you create the anti-phish policy first, then you create the anti-phish rule that identifies the policy that the rule applies to.</span></span>

- <span data-ttu-id="adcbc-124">PowerShell에서는 피싱 정책의 설정과 피싱 규칙을 각각 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-124">In PowerShell, you modify the settings in the anti-phish policy and the anti-phish rule separately.</span></span>

- <span data-ttu-id="adcbc-125">PowerShell에서 피싱 정책을 제거 하면 해당 하는 피싱 규칙이 자동으로 제거 되지 않고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-125">When you remove an anti-phish policy from PowerShell, the corresponding anti-phish rule isn't automatically removed, and vice versa.</span></span>

### <a name="default-atp-anti-phishing-policy"></a><span data-ttu-id="adcbc-126">기본 ATP 피싱 방지 정책</span><span class="sxs-lookup"><span data-stu-id="adcbc-126">Default ATP anti-phishing policy</span></span>

<span data-ttu-id="adcbc-127">모든 ATP 조직에는 다음 속성이 포함 된 Office365 AntiPhish Default 라는 기본 제공 되는 ATP 피싱 방지 정책이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-127">Every ATP organization has a built-in ATP anti-phishing policy named Office365 AntiPhish Default that has these properties:</span></span>

- <span data-ttu-id="adcbc-128">정책에 연결 된 피싱 규칙 (받는 사람 필터)이 없더라도 Office365 AntiPhish Default 라는 피싱 정책이 조직의 모든 받는 사람에 게 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-128">The anti-phish policy named Office365 AntiPhish Default is applied to all recipients in the organization, even though there's no anti-phish rule (recipient filters) associated with the policy.</span></span>

- <span data-ttu-id="adcbc-129">Office365 AntiPhish Default 정책에는 수정할 수 없는 사용자 지정 우선 순위 값이 **가장 낮습니다** (정책이 항상 마지막으로 적용 됨)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-129">The policy named Office365 AntiPhish Default has the custom priority value **Lowest** that you can't modify (the policy is always applied last).</span></span> <span data-ttu-id="adcbc-130">만드는 모든 사용자 지정 정책에는 항상 Office365 AntiPhish Default 라는 정책 보다 높은 우선 순위가 부여 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-130">Any custom policies that you create always have a higher priority than the policy named Office365 AntiPhish Default.</span></span>

- <span data-ttu-id="adcbc-131">Office365 AntiPhish Default 라는 정책이 기본 정책 ( **IsDefault** 속성에 값 `True`이 있음) 이며 기본 정책을 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-131">The policy named Office365 AntiPhish Default is the default policy (the **IsDefault** property has the value `True`), and you can't delete the default policy.</span></span>

<span data-ttu-id="adcbc-132">피싱 방지 보호 기능의 효율성을 높이려면 특정 사용자 또는 사용자 그룹에 적용 되는 보다 엄격한 설정을 사용 하 여 사용자 지정 ATP 피싱 방지 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-132">To increase the effectiveness of anti-phishing protection, you can create custom ATP anti-phishing policies with stricter settings that are applied to specific users or groups of users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="adcbc-133">시작하기 전에 알아야 할 내용은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="adcbc-133">What do you need to know before you begin?</span></span>

- <span data-ttu-id="adcbc-134"><https://protection.office.com/>에서 보안 및 준수 센터를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-134">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="adcbc-135">**ATP 피싱 방지** 페이지로 바로 이동 하려면을 사용 <https://protection.office.com/antiphishing>합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-135">To go directly to the **ATP anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="adcbc-136">Exchange Online PowerShell에 연결하려면 [Exchange Online PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="adcbc-136">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="adcbc-137">이 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-137">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="adcbc-138">피싱 방지 정책을 추가, 수정 및 삭제 하려면 **조직 관리** 또는 **보안 관리자** 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-138">To add, modify, and delete anti-phishing policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="adcbc-139">피싱 방지 정책에 대 한 읽기 전용 액세스를 위해서는 **보안 독자** 역할 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-139">For read-only access to anti-phishing policies, you need to be a member of the **Security Reader** role group.</span></span> <span data-ttu-id="adcbc-140">보안 및 규정 준수 센터의 역할 그룹에 대한 자세한 내용은 [Office 365 보안 및 규정 준수 센터의 사용 권한](permissions-in-the-security-and-compliance-center.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="adcbc-140">For more information about role groups in the Security & Compliance Center, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="adcbc-141">ATP 피싱 사기 정책에 대 한 권장 설정은 [OFFICE ATP 피싱 방지 정책 설정을](recommended-settings-for-eop-and-office365-atp.md#office-atp-anti-phishing-policy-settings)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-141">For our recommended settings for ATP anti-phishing policies, see [Office ATP anti-phishing policy settings](recommended-settings-for-eop-and-office365-atp.md#office-atp-anti-phishing-policy-settings).</span></span>

- <span data-ttu-id="adcbc-142">새 정책이 나 업데이트 된 정책을 적용할 최대 30 분을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-142">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="adcbc-143">필터링 파이프라인에서 피싱 방지 정책이 적용 되는 위치에 대 한 자세한 내용은 [Office 365의 전자 메일 보호의 주문 및 우선 순위](how-policies-and-protections-are-combined.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="adcbc-143">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection in Office 365](how-policies-and-protections-are-combined.md).</span></span>

## <a name="use-the-security--compliance-center-to-create-atp-anti-phishing-policies"></a><span data-ttu-id="adcbc-144">보안 & 준수 센터를 사용 하 여 ATP 피싱 방지 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="adcbc-144">Use the Security & Compliance Center to create ATP anti-phishing policies</span></span>

<span data-ttu-id="adcbc-145">보안 & 준수 센터에서 사용자 지정 ATP 피싱 방지 정책을 만들면 두 가지 모두에 동일한 이름을 사용 하 여 피싱 규칙과 연결 된 피싱 정책이 동시에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-145">Creating a custom ATP anti-phishing policy in the Security & Compliance Center creates the anti-phish rule and the associated anti-phish policy at the same time using the same name for both.</span></span>

<span data-ttu-id="adcbc-146">ATP 피싱 방지 정책을 만들 때는 정책 이름, 설명 및 정책이 적용 되는 사람을 식별 하는 받는 사람 필터를 지정할 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-146">When you create an ATP anti-phishing policy, you can only specify the policy name, description, and the recipient filter that identifies who the policy applies to.</span></span> <span data-ttu-id="adcbc-147">정책을 만든 후에 정책을 수정 하 여 기본 피싱 방지 설정을 변경 하거나 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-147">After you create the policy, you can modify the policy to change or review the default anti-phishing settings.</span></span>

1. <span data-ttu-id="adcbc-148">보안 & 준수 센터에서 **위협 관리** \> **정책** \> **ATP 피싱 방지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-148">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="adcbc-149">**피싱 방지** 페이지에서 **만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-149">On the **Anti-phishing** page, click **Create**.</span></span>

3. <span data-ttu-id="adcbc-150">**새 피싱 방지 정책 만들기** 마법사가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-150">The **Create a new anti-phishing policy** wizard opens.</span></span> <span data-ttu-id="adcbc-151">**정책 이름** 설정 페이지에서 다음 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-151">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="adcbc-152">**이름**: 정책을 설명하는 고유한 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-152">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="adcbc-153">**설명**: 정책에 대한 선택적 설명을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-153">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="adcbc-154">작업을 마친 후 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-154">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="adcbc-155">**적용 대상** 페이지에서 정책이 적용 되는 내부 받는 사람을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-155">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="adcbc-156">조건이나 예외는 한 번만 사용할 수 있지만, 조건이나 예외에 대한 값을 여러 개 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-156">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="adcbc-157">동일한 조건이나 예외의 여러 값은 OR 논리를 사용합니다(예: _\<받는 사람1\>_ or _\<받는 사람2\>_).</span><span class="sxs-lookup"><span data-stu-id="adcbc-157">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="adcbc-158">다른 조건이나 예외에는 AND 논리를 사용합니다(예: _\<받는 사람1\>_ and _\<그룹 1의 구성원\>_).</span><span class="sxs-lookup"><span data-stu-id="adcbc-158">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="adcbc-159">**조건 추가를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-159">Click **Add a condition**.</span></span> <span data-ttu-id="adcbc-160">표시 되는 드롭다운 목록에서 다음의 **경우 적용**아래의 조건을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-160">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="adcbc-161">**받는 사람**: 조직의 사서함, 메일 사용자 또는 메일 연락처를 하나 이상 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-161">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="adcbc-162">**받는 사람이 다음 구성원 인**경우: 조직에서 그룹을 하나 이상 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-162">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="adcbc-163">**받는 사람 도메인은**: Office 365에서 구성된 허용 도메인 중 하나 이상에서 받는 사람을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-163">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in Office 365.</span></span>

   <span data-ttu-id="adcbc-164">조건을 선택한 후에는 **이러한 상자 중 하나** 에 해당 하는 dropdown이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-164">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="adcbc-165">상자를 클릭 하 고 선택할 값 목록을 스크롤합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-165">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="adcbc-166">상자를 클릭 하 고 입력을 시작 하 여 목록을 필터링 하 고 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-166">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="adcbc-167">값을 더 추가 하려면 상자에서 빈 영역을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-167">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="adcbc-168">개별 항목을 제거 하려면 값 **Remove** ![에서 제거 아이콘](../../media/scc-remove-icon.png) 제거를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-168">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="adcbc-169">전체 조건을 제거 하려면 조건에서 제거 **Remove** ![아이콘](../../media/scc-remove-icon.png) 제거를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-169">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="adcbc-170">조건을 더 추가 하려면 **조건 추가** 를 클릭 하 고 **적용 된 경우**에는 나머지 값을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-170">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="adcbc-171">예외를 추가 하려면 **조건 추가** 를 클릭 하 고 다음의 **경우 제외**에서 예외를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-171">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="adcbc-172">설정 및 동작은 조건과 정확히 같습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-172">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="adcbc-173">작업을 마친 후 **다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-173">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="adcbc-174">**설정 검토** 페이지가 나타나면 설정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-174">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="adcbc-175">각 설정에 대해 **편집** 을 클릭 하 여 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-175">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="adcbc-176">작업이 완료 되 면 **이 정책 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-176">When you're finished, click **Create this policy**.</span></span>

6. <span data-ttu-id="adcbc-177">나타나는 확인 대화 상자에서 **확인을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-177">Click **OK** in the confirmation dialog that appears.</span></span>

<span data-ttu-id="adcbc-178">이러한 일반 정책 설정을 사용 하 여 ATP 피싱 방지 정책을 만든 후에는 다음 섹션의 지침을 사용 하 여 정책에서 보호 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-178">After you create the ATP anti-phishing policy with these general policy settings, use the instructions in the next section to configure the protection settings in the policy.</span></span>

## <a name="use-the-security--compliance-center-to-modify-atp-anti-phishing-policies"></a><span data-ttu-id="adcbc-179">보안 & 준수 센터를 사용 하 여 ATP 피싱 방지 정책 수정</span><span class="sxs-lookup"><span data-stu-id="adcbc-179">Use the Security & Compliance Center to modify ATP anti-phishing policies</span></span>

<span data-ttu-id="adcbc-180">다음 절차에 따라 ATP 피싱 방지 정책, 즉 새로 만든 정책 또는 이미 사용자 지정한 기존 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-180">Use the following procedures to modify ATP anti-phishing policies: a new policy that you created, or existing policies that you've already customized.</span></span>

1. <span data-ttu-id="adcbc-181">아직 없는 경우 보안 & 준수 센터를 열고 **위협 관리** \> **정책** \> **ATP 피싱 방지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-181">If you're not already there, open the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="adcbc-182">수정 하려는 사용자 지정 ATP 피싱 방지 정책을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-182">Select the custom ATP anti-phishing policy that you want to modify.</span></span> <span data-ttu-id="adcbc-183">이미 선택 되어 있으면 선택을 취소 하 고 다시 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-183">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="adcbc-184">\*\*정책 \<이름\> \*\* 플라이 아웃 편집이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-184">The **Edit your policy \<name\>** flyout appears.</span></span> <span data-ttu-id="adcbc-185">섹션에서 **편집** 을 클릭 하면 해당 섹션의 설정에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-185">Clicking **Edit** in any section gives you access to the settings in that section.</span></span>

   - <span data-ttu-id="adcbc-186">다음 단계는 섹션에 표시 되는 순서 대로 제공 되지만 순서에 관계 없이 섹션을 선택 하 고 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-186">The following steps are presented in the order that the sections appear, but they aren't sequential (you can select and modify the sections in any order).</span></span>

   - <span data-ttu-id="adcbc-187">섹션에서 **편집** 을 클릭 하면 사용 가능한 설정이 마법사 형식으로 제공 되지만 페이지 내에서 언제 든 지 페이지를 이동할 수 있습니다 **Close** ![ **. 또는 닫기** 아이콘](../../media/scc-remove-icon.png) **을 클릭 하** 여 **정책 \<이름\> 편집** 페이지로 돌아갈 수 있습니다 (마법사의 마지막 페이지를 방문 하 여 저장 하거나 나갈 필요가 없음).</span><span class="sxs-lookup"><span data-stu-id="adcbc-187">After you click **Edit** in a section, the available settings are presented in a wizard format, but you can jump within the pages in any order, and you can click **Save** on any page (or **Cancel** or **Close** ![Close icon](../../media/scc-remove-icon.png) to return to the **Edit your policy \<name\>** page (you aren't required to visit the last page of the wizard to save or leave).</span></span>

4. <span data-ttu-id="adcbc-188">**정책 설정**: 이전 섹션에서 [정책을 만들](#use-the-security--compliance-center-to-create-atp-anti-phishing-policies) 때 사용 가능한 것과 동일한 설정을 수정 하려면 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-188">**Policy setting**: Click **Edit** to modify the same settings that were available when you [created the policy](#use-the-security--compliance-center-to-create-atp-anti-phishing-policies) in the previous section:</span></span>

   - <span data-ttu-id="adcbc-189">**이름**</span><span class="sxs-lookup"><span data-stu-id="adcbc-189">**Name**</span></span>
   - <span data-ttu-id="adcbc-190">**설명**</span><span class="sxs-lookup"><span data-stu-id="adcbc-190">**Description**</span></span>
   - <span data-ttu-id="adcbc-191">**적용 대상**</span><span class="sxs-lookup"><span data-stu-id="adcbc-191">**Applied to**</span></span>
   - <span data-ttu-id="adcbc-192">**설정 검토**</span><span class="sxs-lookup"><span data-stu-id="adcbc-192">**Review your settings**</span></span>

   <span data-ttu-id="adcbc-193">작업이 끝나면 모든 페이지에서 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-193">When you're finished, click **Save** on any page.</span></span>

5. <span data-ttu-id="adcbc-194">**가장**: 정책에서 **편집** 을 클릭 하 여 보호 된 보낸 사람 및 보호 된 도메인을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-194">**Impersonation**: Click **Edit** to modify the protected senders and protected domains in the policy.</span></span> <span data-ttu-id="adcbc-195">이러한 설정은 인바운드 메시지의 보낸 사람 주소에서 찾을 수 있도록 (개별적으로 또는 도메인) 확인 되는 정책에 대 한 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-195">These settings are a condition for the policy that identifies spoofed senders to look for (individually or by domain) in the From address of inbound messages.</span></span> <span data-ttu-id="adcbc-196">자세한 내용은 [ATP 피싱 방지 정책에서 가장 설정을](set-up-anti-phishing-policies.md#impersonation-settings-in-atp-anti-phishing-policies)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-196">For more information, see [Impersonation settings in ATP anti-phishing policies](set-up-anti-phishing-policies.md#impersonation-settings-in-atp-anti-phishing-policies).</span></span>

   - <span data-ttu-id="adcbc-197">**보호할 사용자 추가**: 기본값은 **Off**입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-197">**Add users to protect**: The default value is **Off**.</span></span> <span data-ttu-id="adcbc-198">설정 하려면 켜기/끄기를 **설정 하 고**표시 되는 **사용자 추가** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-198">To turn it on, slide the toggle to **On**, and then click the **Add user** button that appears.</span></span>

     <span data-ttu-id="adcbc-199">사용자 플라이 아웃 **추가** 가 표시 되 면 다음 값을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-199">In the **Add user** flyout that appears, configure the following values:</span></span>

     - <span data-ttu-id="adcbc-200">**전자 메일 주소**:</span><span class="sxs-lookup"><span data-stu-id="adcbc-200">**Email address**:</span></span>

        - <span data-ttu-id="adcbc-201">상자를 클릭 하 고 선택할 사용자 목록을 스크롤합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-201">Click in the box and scroll through the list of users to select.</span></span>
        - <span data-ttu-id="adcbc-202">상자를 클릭 하 고 입력을 시작 하 여 목록을 필터링 하 고 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-202">Click in the box and start typing to filter the list and select a user.</span></span>
        - <span data-ttu-id="adcbc-203">항목을 제거 하려면 사용자에 **Remove** ![대해 제거 아이콘](../../media/scc-remove-icon.png) 제거를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-203">To remove an entry, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user.</span></span>

     - <span data-ttu-id="adcbc-204">**이름**:이 값은 선택한 전자 메일 주소를 기준으로 채워지고 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-204">**Name**: This value is populated based on the email address you selected, but you can change it.</span></span>

     <span data-ttu-id="adcbc-205">작업이 끝나면 모든 페이지에서 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-205">When you're finished, click **Save** on any page.</span></span>

    <span data-ttu-id="adcbc-206">기존 항목을 편집 하려면 목록에서 보호 된 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-206">To edit an existing entry, select the protected user in the list.</span></span>

   - <span data-ttu-id="adcbc-207">**보호할 도메인 추가**: 다음 설정 중 하나 또는 둘 다를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-207">**Add domains to protect**: Configure one or both of the following settings:</span></span>

     - <span data-ttu-id="adcbc-208">**소유한 도메인을 자동으로 포함**: 기본값은 **Off**입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-208">**Automatically include the domains I own**: The default value is **Off**.</span></span> <span data-ttu-id="adcbc-209">설정 하려면 **슬라이드를 설정 합니다 .로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-209">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="adcbc-210">**사용자 지정 도메인 포함**: 기본값은 **Off**입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-210">**Include custom domains**: The default value is **Off**.</span></span> <span data-ttu-id="adcbc-211">이 옵션을 설정 하려면 켜기/끄기를 **켜**세요. 도메인 **추가** 상자에 도메인 이름 (예: contoso.com)을 입력 하 고 enter 키를 누른 다음 필요에 따라 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-211">To turn it on, slide the toggle to **On**, and in the **Add domains** box, enter the domain name (for example, contoso.com), press ENTER, and repeat as necessary.</span></span>

   - <span data-ttu-id="adcbc-212">**작업**: **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-212">**Actions**: Click **Edit**</span></span>

     - <span data-ttu-id="adcbc-213">**가장 된 사용자가 전자 메일을 보낸 경우**: 스푸핑된 보낸 사람이 **보호할 사용자 추가**에 지정한 보호 된 사용자 중 하나인 메시지에 대해 다음 작업 중 하나를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-213">**If email is sent by an impersonated user**: Configure one of the following actions for messages where the spoofed sender is one of the protected users you specified in **Add users to protect**:</span></span>

       - <span data-ttu-id="adcbc-214">**작업 적용 안 함**</span><span class="sxs-lookup"><span data-stu-id="adcbc-214">**Don't apply any action**</span></span>
       - <span data-ttu-id="adcbc-215">**메시지를 다른 전자 메일 주소로 리디렉션**</span><span class="sxs-lookup"><span data-stu-id="adcbc-215">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="adcbc-216">**정크 메일 폴더로 메시지 이동**</span><span class="sxs-lookup"><span data-stu-id="adcbc-216">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="adcbc-217">**메시지 격리**</span><span class="sxs-lookup"><span data-stu-id="adcbc-217">**Quarantine the message**</span></span>
       - <span data-ttu-id="adcbc-218">**메시지를 배달 하 고 숨은 참조 줄에 다른 주소 추가**</span><span class="sxs-lookup"><span data-stu-id="adcbc-218">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="adcbc-219">**메시지를 배달 하기 전에 삭제 합니다.**</span><span class="sxs-lookup"><span data-stu-id="adcbc-219">**Delete the message before it's delivered**</span></span>

     - <span data-ttu-id="adcbc-220">**가장 된 도메인이 전자 메일을 보낸 경우**: 스푸핑된 보낸 사람이 **보호할 도메인**에 지정 된 보호 된 도메인 중 하나에 있는 메시지에 대해 다음 작업 중 하나를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-220">**If email is sent by an impersonated domain**: Configure one of the following actions for messages where the spoofed sender is in one of the protected domains you specified in **Add domains to protect**:</span></span>

     - <span data-ttu-id="adcbc-221">**작업 적용 안 함**</span><span class="sxs-lookup"><span data-stu-id="adcbc-221">**Don't apply any action**</span></span>
     - <span data-ttu-id="adcbc-222">**메시지를 다른 전자 메일 주소로 리디렉션**</span><span class="sxs-lookup"><span data-stu-id="adcbc-222">**Redirect message to other email addresses**</span></span>
     - <span data-ttu-id="adcbc-223">**정크 메일 폴더로 메시지 이동**</span><span class="sxs-lookup"><span data-stu-id="adcbc-223">**Move message to Junk Email folder**</span></span>
     - <span data-ttu-id="adcbc-224">**메시지 격리**</span><span class="sxs-lookup"><span data-stu-id="adcbc-224">**Quarantine the message**</span></span>
     - <span data-ttu-id="adcbc-225">**메시지를 배달 하 고 숨은 참조 줄에 다른 주소 추가**</span><span class="sxs-lookup"><span data-stu-id="adcbc-225">**Deliver the message and add other addresses to the Bcc line**</span></span>
     - <span data-ttu-id="adcbc-226">**메시지를 배달 하기 전에 삭제 합니다.**</span><span class="sxs-lookup"><span data-stu-id="adcbc-226">**Delete the message before it's delivered**</span></span>

   - <span data-ttu-id="adcbc-227">**가장 안전 팁 사용** 을 클릭 하 고 다음 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-227">Click **turn on impersonation safety tips** and configure any of the following settings:</span></span>

     - <span data-ttu-id="adcbc-228">**가장 된 사용자에 대 한 팁 표시**: 기본값은 **Off**입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-228">**Show tip for impersonated users**: The default value is **Off**.</span></span> <span data-ttu-id="adcbc-229">설정 하려면 **슬라이드를 설정 합니다 .로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-229">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="adcbc-230">**가장 된 도메인에 대 한 팁 표시**: 기본값은 **Off**입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-230">**Show tip for impersonated domains**: The default value is **Off**.</span></span> <span data-ttu-id="adcbc-231">설정 하려면 **슬라이드를 설정 합니다 .로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-231">To turn it on, slide the toggle to **On**.</span></span>
     - <span data-ttu-id="adcbc-232">**비정상적인 캐릭터에 대 한 팁 표시**: 기본값은 **Off**입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-232">**Show tip for unusual characters**: The default value is **Off**.</span></span> <span data-ttu-id="adcbc-233">설정 하려면 **슬라이드를 설정 합니다 .로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-233">To turn it on, slide the toggle to **On**.</span></span>

     <span data-ttu-id="adcbc-234">작업을 마쳤으면 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-234">When you're finished, click **Save**.</span></span>

   - <span data-ttu-id="adcbc-235">**사서함 인텔리전스**:</span><span class="sxs-lookup"><span data-stu-id="adcbc-235">**Mailbox intelligence**:</span></span>

     - <span data-ttu-id="adcbc-236">**사서함 인텔리전스 사용 여부**: 기본값은 **On**입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-236">**Enable mailbox intelligence?**: The default value is **On**.</span></span> <span data-ttu-id="adcbc-237">해제 하려면 **토글을 끕니다.**</span><span class="sxs-lookup"><span data-stu-id="adcbc-237">To turn it off, slide the toggle to **Off**.</span></span>

     - <span data-ttu-id="adcbc-238">**Mailbox intelligence 기반 가장 보호 사용?**:이 설정은 **사서함 인텔리전스 사용** 이 설정 되어 있는 경우 **에**만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-238">**Enable mailbox intelligence based impersonation protection?**: This setting is only available if **Enable mailbox intelligence?** is **On**.</span></span>

       <span data-ttu-id="adcbc-239">에서 **가장 된 사용자가 전자 메일을 보낸 경우**에는 다음 작업 중 하나를 지정 하 여 사서함 인텔리전스 오류가 발생 한 메시지 (보호 되는 사용자와 보호 된 도메인에 사용할 수 있는 것과 동일한 작업)에 대해 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-239">In **If email is sent by an impersonated user**, you can specify one of the following actions to take on messages that fail mailbox intelligence (the same actions that are available for protected users and protected domains):</span></span>

       - <span data-ttu-id="adcbc-240">**작업 적용 안 함**</span><span class="sxs-lookup"><span data-stu-id="adcbc-240">**Don't apply any action**</span></span>
       - <span data-ttu-id="adcbc-241">**메시지를 다른 전자 메일 주소로 리디렉션**</span><span class="sxs-lookup"><span data-stu-id="adcbc-241">**Redirect message to other email addresses**</span></span>
       - <span data-ttu-id="adcbc-242">**정크 메일 폴더로 메시지 이동**</span><span class="sxs-lookup"><span data-stu-id="adcbc-242">**Move message to Junk Email folder**</span></span>
       - <span data-ttu-id="adcbc-243">**메시지 격리**</span><span class="sxs-lookup"><span data-stu-id="adcbc-243">**Quarantine the message**</span></span>
       - <span data-ttu-id="adcbc-244">**메시지를 배달 하 고 숨은 참조 줄에 다른 주소 추가**</span><span class="sxs-lookup"><span data-stu-id="adcbc-244">**Deliver the message and add other addresses to the Bcc line**</span></span>
       - <span data-ttu-id="adcbc-245">**메시지를 배달 하기 전에 삭제 합니다.**</span><span class="sxs-lookup"><span data-stu-id="adcbc-245">**Delete the message before it's delivered**</span></span>

   - <span data-ttu-id="adcbc-246">**신뢰할 수 있는 보낸 사람 및 도메인 추가**: 정책에 대 한 예외를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-246">**Add trusted senders and domains**: Specify exceptions for the policy:</span></span>

     - <span data-ttu-id="adcbc-247">**신뢰할 수 있는 보낸 사람**:</span><span class="sxs-lookup"><span data-stu-id="adcbc-247">**Trusted senders**:</span></span>

       - <span data-ttu-id="adcbc-248">상자를 클릭 하 고 선택할 사용자 목록을 스크롤합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-248">Click in the box and scroll through the list of users to select.</span></span>
       - <span data-ttu-id="adcbc-249">상자를 클릭 하 고 입력을 시작 하 여 목록을 필터링 하 고 사용자를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-249">Click in the box and start typing to filter the list and select a user.</span></span>
       - <span data-ttu-id="adcbc-250">항목을 제거 하려면 사용자에 **Remove** ![대해 제거 아이콘](../../media/scc-remove-icon.png) 제거를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-250">To remove an entry, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the user.</span></span>

     - <span data-ttu-id="adcbc-251">**신뢰할 수 있는 도메인**: contoso.com와 같은 도메인 이름을 입력 하 고 enter 키를 누른 다음 필요에 따라 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-251">**Trusted domains**: Enter the domain name (for example, contoso.com), press ENTER, and repeat as necessary.</span></span>

   - <span data-ttu-id="adcbc-252">**설정 검토**: 각 개별 단계를 클릭 하지 않고 설정이 요약으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-252">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="adcbc-253">각 섹션에서 **편집** 을 클릭 하 여 관련 페이지로 다시 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-253">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="adcbc-254">이 **페이지에서 다음** 설정을 직접 설정 하거나 **해제할** 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-254">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="adcbc-255">**보호 된 사용자**</span><span class="sxs-lookup"><span data-stu-id="adcbc-255">**Protected users**</span></span>
       - <span data-ttu-id="adcbc-256">**보호 된 도메인** \> 에 **소유한 도메인 포함**</span><span class="sxs-lookup"><span data-stu-id="adcbc-256">**Protected domains** \> **Include domains I own**</span></span>
       - <span data-ttu-id="adcbc-257">**보호 된 도메인** \> **보호 된** 도메인 (사용자 지정 도메인)</span><span class="sxs-lookup"><span data-stu-id="adcbc-257">**Protected domains** \> **Protected domains** (custom domains)</span></span>
       - <span data-ttu-id="adcbc-258">**사서함 인텔리전스**</span><span class="sxs-lookup"><span data-stu-id="adcbc-258">**Mailbox intelligence**</span></span>

   <span data-ttu-id="adcbc-259">작업이 끝나면 모든 페이지에서 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-259">When you're finished, click **Save** on any page.</span></span>

6. <span data-ttu-id="adcbc-260">**스푸핑**: **편집** 을 클릭 하 여 스푸핑 인텔리전스를 설정 하거나 해제 하 고, Outlook에서 인증 되지 않은 보낸 사람 id를 설정/해제 하 고, 차단 된 스푸핑된 보낸 사람 으로부터 메시지에 적용할 작업을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-260">**Spoof**: Click **Edit** to turn spoof intelligence on or off, turn unauthenticated sender identification in Outlook on or off, and configure the action to apply to messages from blocked spoofed senders.</span></span> <span data-ttu-id="adcbc-261">자세한 내용은 [피싱 방지 정책에서 스푸핑 설정을](set-up-anti-phishing-policies.md#spoof-settings)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-261">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

   <span data-ttu-id="adcbc-262">이러한 설정은 EOP의 기본 피싱 방지 정책에서 사용할 수 있는 설정과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-262">Note that these settings are identical to the settings that are available in the default anti-phishing policy in EOP.</span></span>

   - <span data-ttu-id="adcbc-263">**스푸핑 필터 설정**: 기본값은 **on**이며,이 값을 유지 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-263">**Spoofing filter settings**: The default value is **On**, and we recommend that you leave it on.</span></span> <span data-ttu-id="adcbc-264">해제 하려면 **토글을 끕니다.**</span><span class="sxs-lookup"><span data-stu-id="adcbc-264">To turn it off, slide the toggle to **Off**.</span></span> <span data-ttu-id="adcbc-265">자세한 내용은 [Office 365에서 스푸핑 인텔리전스를 구성](learn-about-spoof-intelligence.md)합니다 .를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-265">For more information, see [Configure spoof intelligence in Office 365](learn-about-spoof-intelligence.md).</span></span>

     > [!NOTE]
     > <span data-ttu-id="adcbc-266">MX 레코드가 Office 365를 가리키지 않으면 스푸핑 방지 보호를 사용 하지 않도록 설정할 필요가 없습니다. 대신 커넥터에 대 한 향상 된 필터링을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-266">You don't need to disable anti-spoofing protection if your MX record doesn't point to Office 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="adcbc-267">자세한 내용은 [Exchange Online의 커넥터에 대 한 향상 된 필터링](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-267">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   - <span data-ttu-id="adcbc-268">**인증 되지 않은 보낸 사람 기능 사용**: 기본값은 **On**입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-268">**Enable Unauthenticated Sender feature**: The default value is **On**.</span></span> <span data-ttu-id="adcbc-269">해제 하려면 **토글을 끕니다.**</span><span class="sxs-lookup"><span data-stu-id="adcbc-269">To turn it off, slide the toggle to **Off**.</span></span>

   - <span data-ttu-id="adcbc-270">**작업**: 스푸핑 인텔리전스에 실패 한 메시지에 대해 수행할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-270">**Actions**: Specify the action to take on messages that fail spoof intelligence:</span></span>

     <span data-ttu-id="adcbc-271">**도메인을 스푸핑할 수 없는 사용자가 전자 메일을 보낸 경우**:</span><span class="sxs-lookup"><span data-stu-id="adcbc-271">**If email is sent by someone who's not allowed to spoof your domain**:</span></span>

     - <span data-ttu-id="adcbc-272">**받는 사람의 정크 메일 폴더로 메시지 이동**</span><span class="sxs-lookup"><span data-stu-id="adcbc-272">**Move message to the recipients' Junk Email folders**</span></span>
     - <span data-ttu-id="adcbc-273">**메시지 격리**</span><span class="sxs-lookup"><span data-stu-id="adcbc-273">**Quarantine the message**</span></span>

   - <span data-ttu-id="adcbc-274">**설정 검토**: 각 개별 단계를 클릭 하지 않고 설정이 요약으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-274">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="adcbc-275">각 섹션에서 **편집** 을 클릭 하 여 관련 페이지로 다시 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-275">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="adcbc-276">이 **페이지에서 다음** 설정을 직접 설정 하거나 **해제할** 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-276">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="adcbc-277">**스푸핑 방지 보호 사용**</span><span class="sxs-lookup"><span data-stu-id="adcbc-277">**Enable antispoofing protection**</span></span>
       - <span data-ttu-id="adcbc-278">**인증 되지 않은 보낸 사람 기능 사용**</span><span class="sxs-lookup"><span data-stu-id="adcbc-278">**Enable Unauthenticated Sender feature**</span></span>

   <span data-ttu-id="adcbc-279">작업이 끝나면 모든 페이지에서 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-279">When you're finished, click **Save** on any page.</span></span>

7. <span data-ttu-id="adcbc-280">**고급 설정**: 고급 피싱 임계값을 구성 하려면 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-280">**Advanced settings**: Click **Edit** to configure the advanced phishing thresholds.</span></span> <span data-ttu-id="adcbc-281">자세한 내용은 [ATP 피싱 방지 정책에서 Advanced 피싱 임계값](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-atp-anti-phishing-policies)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-281">For more information, see [Advanced phishing thresholds in ATP anti-phishing policies](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-atp-anti-phishing-policies).</span></span>

   - <span data-ttu-id="adcbc-282">**고급 피싱 임계값**: 다음 값 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-282">**Advanced phishing thresholds**: Select one of the following values:</span></span>

   - <span data-ttu-id="adcbc-283">**1-표준** (이 값은 기본값입니다.)</span><span class="sxs-lookup"><span data-stu-id="adcbc-283">**1 - Standard** (This is the default value.)</span></span>
   - <span data-ttu-id="adcbc-284">**2-적극적인**</span><span class="sxs-lookup"><span data-stu-id="adcbc-284">**2 - Aggressive**</span></span>
   - <span data-ttu-id="adcbc-285">**3-적극적인**</span><span class="sxs-lookup"><span data-stu-id="adcbc-285">**3 - More aggressive**</span></span>
   - <span data-ttu-id="adcbc-286">**4-최대 적극적인**</span><span class="sxs-lookup"><span data-stu-id="adcbc-286">**4 - Most aggressive**</span></span>

   - <span data-ttu-id="adcbc-287">**설정 검토**: **편집** 을 클릭 하 여 **고급 피싱 임계값** 페이지로 다시 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-287">**Review your settings**: Click **Edit** to jump back to the **Advanced phishing thresholds** page.</span></span>

   <span data-ttu-id="adcbc-288">작업이 끝나면 두 페이지 중 하나에서 **저장** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-288">When you're finished, click **Save** on either page.</span></span>

8. <span data-ttu-id="adcbc-289">**정책 \<\> 이름 편집** 페이지에서 설정을 검토 하 고 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-289">Back on the **Edit your policy \<Name\>** page, review your settings and then click **Close**.</span></span>

### <a name="use-the-security--compliance-center-to-modify-the-default-atp-anti-phishing-policy"></a><span data-ttu-id="adcbc-290">보안 & 준수 센터를 사용 하 여 기본 ATP 피싱 방지 정책 수정</span><span class="sxs-lookup"><span data-stu-id="adcbc-290">Use the Security & Compliance Center to modify the default ATP anti-phishing policy</span></span>

<span data-ttu-id="adcbc-291">기본 ATP 피싱 방지 정책은 Office365 AntiPhish Default로 이름이 지정 되며 정책 목록에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-291">The default ATP anti-phishing policy is named Office365 AntiPhish Default, and it doesn't appear in the list of policies.</span></span> <span data-ttu-id="adcbc-292">기본 ATP 피싱 방지 정책을 수정 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-292">To modify the default ATP anti-phishing policy, do the following steps:</span></span>

1. <span data-ttu-id="adcbc-293">보안 & 준수 센터에서 **위협 관리** \> **정책** \> **ATP 피싱 방지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-293">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="adcbc-294">**피싱 방지** 페이지에서 **기본 정책을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-294">On the **Anti-phishing** page, click **Default policy**.</span></span>

3. <span data-ttu-id="adcbc-295">**정책 편집 Office365 AntiPhish 기본값** 페이지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-295">The **Edit your policy Office365 AntiPhish Default** page appears.</span></span> <span data-ttu-id="adcbc-296">다음 섹션에서는 [사용자 지정 정책을 수정할](#use-the-security--compliance-center-to-modify-atp-anti-phishing-policies)때의 설정이 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-296">The following sections are available, which contain identical settings for when you [modify a custom policy](#use-the-security--compliance-center-to-modify-atp-anti-phishing-policies):</span></span>

   - <span data-ttu-id="adcbc-297">**가장**</span><span class="sxs-lookup"><span data-stu-id="adcbc-297">**Impersonation**</span></span>
   - <span data-ttu-id="adcbc-298">**신분을**</span><span class="sxs-lookup"><span data-stu-id="adcbc-298">**Spoof**</span></span>
   - <span data-ttu-id="adcbc-299">**고급 설정**</span><span class="sxs-lookup"><span data-stu-id="adcbc-299">**Advanced settings**</span></span>

   <span data-ttu-id="adcbc-300">기본 정책을 수정 하는 경우에는 다음 설정을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-300">The following settings aren't available when you modify the default policy:</span></span>

   - <span data-ttu-id="adcbc-301">**정책 설정** 섹션 및 값을 볼 수는 있지만 **편집** 링크는 없는 경우에는 설정 (정책 이름, 설명 및 정책을 적용 하는 사람 (모든 받는 사람에 게 적용)을 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-301">You can see the **Policy setting** section and values, but there's no **Edit** link, so you can't modify the settings (policy name, description, and who the policy applies to (it applies to all recipients)).</span></span>
   - <span data-ttu-id="adcbc-302">기본 정책은 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-302">You can't delete the default policy.</span></span>
   - <span data-ttu-id="adcbc-303">기본 정책의 우선 순위를 변경할 수는 없습니다 (항상 마지막으로 적용 됨).</span><span class="sxs-lookup"><span data-stu-id="adcbc-303">You can't change the priority of the default policy (it's always applied last).</span></span>

4. <span data-ttu-id="adcbc-304">**Policy Office365 AntiPhish 기본값 편집** 페이지에서 설정을 검토 하 고 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-304">On the **Edit your policy Office365 AntiPhish Default** page, review your settings and then click **Close**.</span></span>

### <a name="enable-or-disable-custom-atp-anti-phishing-policies"></a><span data-ttu-id="adcbc-305">사용자 지정 ATP 피싱 방지 정책 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="adcbc-305">Enable or disable custom ATP anti-phishing policies</span></span>

1. <span data-ttu-id="adcbc-306">보안 & 준수 센터에서 **위협 관리** \> **정책** \> **ATP 피싱 방지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-306">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="adcbc-307">**상태** 열에서 다음 값을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-307">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="adcbc-308">정책을 사용 하지 않도록 설정 하려면이 설정을 **해제** 로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-308">Slide the toggle to **Off** to disable the policy.</span></span>

   - <span data-ttu-id="adcbc-309">정책을 **사용 하려면 토글을 설정으로 이동** 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-309">Slide the toggle to **On** to enable the policy.</span></span>

<span data-ttu-id="adcbc-310">기본 피싱 방지 정책을 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-310">You can't disable the default anti-phishing policy.</span></span>

### <a name="set-the-priority-of-custom-atp-anti-phishing-policies"></a><span data-ttu-id="adcbc-311">사용자 지정 ATP 피싱 방지 정책의 우선 순위 설정</span><span class="sxs-lookup"><span data-stu-id="adcbc-311">Set the priority of custom ATP anti-phishing policies</span></span>

<span data-ttu-id="adcbc-312">기본적으로 ATP 피싱 방지 정책에는 만든 순서를 기준으로 하는 우선 순위가 지정 됩니다 (최신 정책은 이전 정책 보다 낮은 우선 순위입니다).</span><span class="sxs-lookup"><span data-stu-id="adcbc-312">By default, ATP anti-phishing policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="adcbc-313">낮은 우선순위 번호는 정책의 높은 우선순위(0이 가장 높음)를 나타내고 정책은 우선순위 순서에 따라 처리됩니다(높은 우선순위 정책은 낮은 우선순위 정책보다 먼저 처리됨).</span><span class="sxs-lookup"><span data-stu-id="adcbc-313">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="adcbc-314">두 정책의 우선순위가 같을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-314">No two policies can have the same priority.</span></span>

<span data-ttu-id="adcbc-315">사용자 지정 ATP 피싱 방지 정책은 처리 되는 순서 대로 표시 됩니다 (첫 번째 정책의 **우선 순위** 값은 0).</span><span class="sxs-lookup"><span data-stu-id="adcbc-315">Custom ATP anti-phishing policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="adcbc-316">Office365 AntiPhish Default 라는 기본 피싱 방지 정책은 사용자 지정 우선 순위 값이 **가장 낮은**반면,이를 변경할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-316">The default anti-phishing policy named Office365 AntiPhish Default has the custom priority value **Lowest**, and you can't change it.</span></span>

 <span data-ttu-id="adcbc-317">**참고**: 보안 & 준수 센터에서는 ATP 피싱 방지 정책의 우선 순위를 만든 후에만 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-317">**Note**: In the Security & Compliance Center, you can only change the priority of the ATP anti-phishing policy after you create it.</span></span> <span data-ttu-id="adcbc-318">PowerShell에서는 기존 규칙의 우선 순위에 영향을 줄 수 있는 피싱 규칙을 만들 때 기본 우선 순위를 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-318">In PowerShell, you can override the default priority when you create the anti-phish rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="adcbc-319">정책의 우선 순위를 변경 하려면 정책의 속성에서 우선 **순위 높임** 또는 **우선 순위 낮추기** (보안 & 준수 센터에서 직접 **우선 순위** 번호를 수정할 수 없음)을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-319">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span> <span data-ttu-id="adcbc-320">정책 우선 순위를 변경 하는 것은 정책이 여러 개인 경우에만 의미가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-320">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

1. <span data-ttu-id="adcbc-321">보안 & 준수 센터에서 **위협 관리** \> **정책** \> **ATP 피싱 방지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-321">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="adcbc-322">수정 하려는 정책을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-322">Select the policy that you want to modify.</span></span> <span data-ttu-id="adcbc-323">이미 선택 되어 있으면 선택을 취소 하 고 다시 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-323">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="adcbc-324">\*\*정책 \<이름\> \*\* 플라이 아웃 편집이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-324">The **Edit your policy \<name\>** flyout appears.</span></span>

   - <span data-ttu-id="adcbc-325">**우선 순위** 값이 **0** 인 사용자 지정 ATP 피싱 방지 정책에는 **우선 순위 낮추기** 단추만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-325">The custom ATP anti-phishing policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="adcbc-326">가장 낮은 **우선 순위** 값을 갖는 사용자 지정 ATP 피싱 방지 정책 (예: **3**)에는 **우선 순위 향상** 단추만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-326">The custom ATP anti-phishing policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="adcbc-327">사용자 지정 피싱 방지 정책이 3 개 이상 있는 경우 가장 높거나 낮은 우선 순위 값 사이의 정책에는 **우선 순위 증가** 와 **우선 순위 낮추기** 단추가 모두 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-327">If you have three or more custom anti-phishing policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="adcbc-328">우선 **순위 높임** 또는 **우선 순위 낮추기** 를 클릭 하 여 **우선 순위** 값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-328">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="adcbc-329">작업을 마쳤으면 **닫기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-329">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-view-atp-anti-phishing-policies"></a><span data-ttu-id="adcbc-330">보안 & 준수 센터를 사용 하 여 ATP 피싱 방지 정책 보기</span><span class="sxs-lookup"><span data-stu-id="adcbc-330">Use the Security & Compliance Center to view ATP anti-phishing policies</span></span>

1. <span data-ttu-id="adcbc-331">보안 & 준수 센터에서 **위협 관리** \> **정책** \> **ATP 피싱 방지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-331">In the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="adcbc-332">다음 단계 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-332">Do one of the following steps:</span></span>

   - <span data-ttu-id="adcbc-333">보려는 사용자 지정 ATP 피싱 방지 정책을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-333">Select a custom ATP anti-phishing policy that you want to view.</span></span> <span data-ttu-id="adcbc-334">이미 선택 되어 있으면 선택을 취소 하 고 다시 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-334">If it's already selected, deselect it and select it again.</span></span>

   - <span data-ttu-id="adcbc-335">기본 **정책을** 클릭 하 여 기본 피싱 방지 정책을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-335">Click **Default policy** to view the default anti-phishing policy.</span></span>

3. <span data-ttu-id="adcbc-336">설정 및 값을 볼 수 있는 \*\*정책 \<이름\> \*\* 플라이 아웃 편집이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-336">The **Edit your policy \<name\>** flyout appears, where you can view the settings and values.</span></span>

## <a name="use-the-security--compliance-center-to-remove-atp-anti-phishing-policies"></a><span data-ttu-id="adcbc-337">보안 & 준수 센터를 사용 하 여 ATP 피싱 방지 정책 제거</span><span class="sxs-lookup"><span data-stu-id="adcbc-337">Use the Security & Compliance Center to remove ATP anti-phishing policies</span></span>

1. <span data-ttu-id="adcbc-338">보안 & 준수 센터에서 **위협 관리** \> **정책** \> **ATP 피싱 방지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-338">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="adcbc-339">제거할 정책을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-339">Select the policy that you want to remove.</span></span> <span data-ttu-id="adcbc-340">이미 선택 되어 있으면 선택을 취소 하 고 다시 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-340">If it's already selected, deselect it and select it again.</span></span>

3. <span data-ttu-id="adcbc-341">표시 되는 \*\*정책 \<이름\> \*\* 플라이 아웃 편집에서 **정책 삭제**를 클릭 한 다음 표시 되는 경고 대화 상자에서 **예** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-341">In the **Edit your policy \<name\>** flyout that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

<span data-ttu-id="adcbc-342">기본 정책은 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-342">You can't remove the default policy.</span></span>

## <a name="use-exchange-online-powershell-to-configure-atp-anti-phishing-policies"></a><span data-ttu-id="adcbc-343">Exchange Online PowerShell을 사용 하 여 ATP 피싱 방지 정책 구성</span><span class="sxs-lookup"><span data-stu-id="adcbc-343">Use Exchange Online PowerShell to configure ATP anti-phishing policies</span></span>

### <a name="use-powershell-to-create-anti-phishing-policies"></a><span data-ttu-id="adcbc-344">PowerShell을 사용 하 여 피싱 방지 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="adcbc-344">Use PowerShell to create anti-phishing policies</span></span>

<span data-ttu-id="adcbc-345">PowerShell에서 피싱 방지 정책을 만드는 과정은 다음 두 단계로 진행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-345">Creating an anti-phishing policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="adcbc-346">피싱 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-346">Create the anti-phish policy.</span></span>

2. <span data-ttu-id="adcbc-347">규칙이 적용 되는 피싱 정책을 지정 하는 피싱 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-347">Create the anti-phish rule that specifies the anti-phish policy that the rule applies to.</span></span>

 <span data-ttu-id="adcbc-348">**참고**:</span><span class="sxs-lookup"><span data-stu-id="adcbc-348">**Notes**:</span></span>

- <span data-ttu-id="adcbc-349">새 피싱 규칙을 만들고 연결 되지 않은 기존 피싱 정책을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-349">You can create a new anti-phish rule and assign an existing, unassociated anti-phish policy to it.</span></span> <span data-ttu-id="adcbc-350">피싱 규칙을 두 개 이상의 피싱 정책에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-350">An anti-phish rule can't be associated with more than one anti-phish policy.</span></span>

- <span data-ttu-id="adcbc-351">정책을 만든 후에 야 보안 & 준수 센터에서 사용할 수 없는 PowerShell의 새 피싱 정책에서 다음 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-351">You can configure the following settings on new anti-phish policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="adcbc-352">**AntiPhishRule** cmdlet에서_사용 하도록 설정_ `$false` 된 새 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-352">Create the new policy as disabled (_Enabled_ `$false` on the **New-AntiPhishRule** cmdlet).</span></span>

  - <span data-ttu-id="adcbc-353">**AntiPhishRule** cmdlet에 대해 만드는 동안 정책의 우선 순위 (_우선 순위_ _ \<번호\>_)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-353">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-AntiPhishRule** cmdlet).</span></span>

- <span data-ttu-id="adcbc-354">피싱 규칙에 정책을 할당 하기 전 까지는 PowerShell에서 만드는 새로운 피싱 정책이 보안 & 준수 센터에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-354">A new anti-phish policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to an anti-phish rule.</span></span>

#### <a name="step-1-use-powershell-to-create-an-anti-phish-policy"></a><span data-ttu-id="adcbc-355">1 단계: PowerShell을 사용 하 여 피싱 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="adcbc-355">Step 1: Use PowerShell to create an anti-phish policy</span></span>

<span data-ttu-id="adcbc-356">피싱 정책을 만들려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-356">To create an anti-phish policy, use this syntax:</span></span>

```PowerShell
New-AntiPhishPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] <Additional Settings>
```

<span data-ttu-id="adcbc-357">이 예에서는 다음 설정을 사용 하 여 Research Quarantine 라는 피싱 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-357">This example creates anti-phish policy named Research Quarantine with the following settings:</span></span>

- <span data-ttu-id="adcbc-358">정책이 사용 하도록 설정 되어 있습니다 ( _enabled_ 매개 변수를 사용 하지 않으며 기본값은 `$true`).</span><span class="sxs-lookup"><span data-stu-id="adcbc-358">The policy is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>
- <span data-ttu-id="adcbc-359">설명은 부서 정책 연구입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-359">The description is: Research department policy.</span></span>
- <span data-ttu-id="adcbc-360">모든 허용 도메인에 대해 조직 도메인을 보호 하 고 fabrikam.com에 대해 대상 도메인 보호를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-360">Enables organization domains protection for all accepted domains, and targeted domains protection for fabrikam.com.</span></span>
- <span data-ttu-id="adcbc-361">가장을 보호할 사용자에 게 Mai Fujito (mfujito@fabrikam.com)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-361">Specifies Mai Fujito (mfujito@fabrikam.com) as the user to protect from impersonation.</span></span>
- <span data-ttu-id="adcbc-362">사서함 인텔리전스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-362">Enables mailbox intelligence.</span></span>
- <span data-ttu-id="adcbc-363">사서함 인텔리전스 보호를 사용 하도록 설정 하 고 격리 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-363">Enables mailbox intelligence protection, and specifies the quarantine action.</span></span>
- <span data-ttu-id="adcbc-364">안전 팁을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-364">Enables safety tips.</span></span>

```powershell
New-AntiPhishPolicy -Name "Monitor Policy" -AdminDisplayName "Default monitoring policy" -EnableOrganizationDomainsProtection $true -EnableTargetedDomainsProtection $true -TargetedDomainsToProtect fabrikam.com -TargetedDomainProtectionAction Quarantine -EnableTargetedUserProtection $true -TargetedUsersToProtect "Mai Fujito;mfujito@fabrikam.com" -TargetedUserProtectionAction Quarantine -EnableMailboxIntelligence $true -EnableMailboxIntelligenceProtection $true -MailboxIntelligenceProtectionAction Quarantine -EnableSimilarUsersSafetyTips $true -EnableSimilarDomainsSafetyTips $true -EnableUnusualCharactersSafetyTips $true
```

<span data-ttu-id="adcbc-365">구문과 매개 변수에 대 한 자세한 내용은 [AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/New-AntiPhishPolicy)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-365">For detailed syntax and parameter information, see [New-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/New-AntiPhishPolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-an-anti-phish-rule"></a><span data-ttu-id="adcbc-366">2 단계: PowerShell을 사용 하 여 피싱 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="adcbc-366">Step 2: Use PowerShell to create an anti-phish rule</span></span>

<span data-ttu-id="adcbc-367">피싱 규칙을 만들려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-367">To create an anti-phish rule, use this syntax:</span></span>

```PowerShell
New-AntiPhishRule -Name "<RuleName>" -AntiPhishPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"]
```

<span data-ttu-id="adcbc-368">이 예에서는 다음 조건을 사용 하 여 Research 학과 라는 피싱 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-368">This example creates an anti-phish rule named Research Department with the following conditions:</span></span>

- <span data-ttu-id="adcbc-369">이 규칙은 조사 검역 이라는 피싱 정책에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-369">The rule is associated with the anti-phish policy named Research Quarantine.</span></span>
- <span data-ttu-id="adcbc-370">이 규칙은 Research Department 그룹의 구성원에게 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-370">The rule applies to members of the group named Research Department.</span></span>
- <span data-ttu-id="adcbc-371">_Priority_ 매개 변수를 사용 하지 않으므로 기본 우선 순위가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-371">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>

```powershell
New-AntiPhishRule -Name "Research Department" -AntiPhishPolicy "Research Quarantine" -SentToMemberOf "Research Department"
```

<span data-ttu-id="adcbc-372">구문과 매개 변수에 대 한 자세한 내용은 [AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/New-AntiPhishRule)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-372">For detailed syntax and parameter information, see [New-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/New-AntiPhishRule).</span></span>

### <a name="use-powershell-to-view-anti-phish-policies"></a><span data-ttu-id="adcbc-373">PowerShell을 사용 하 여 피싱 정책 보기</span><span class="sxs-lookup"><span data-stu-id="adcbc-373">Use PowerShell to view anti-phish policies</span></span>

<span data-ttu-id="adcbc-374">기존 피싱 정책을 보려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-374">To view existing anti-phish policies, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="adcbc-375">이 예제에서는 지정 된 속성과 함께 모든 피싱 정책의 요약 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-375">This example returns a summary list of all anti-phish policies along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishPolicy | Format-Table Name,IsDefault
```

<span data-ttu-id="adcbc-376">이 예제에서는 중역 이라는 피싱 정책에 대 한 모든 속성 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-376">This example returns all the property values for the anti-phish policy named Executives.</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Executives"
```

<span data-ttu-id="adcbc-377">구문과 매개 변수에 대 한 자세한 내용은 [AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishPolicy)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-377">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-view-anti-phish-rules"></a><span data-ttu-id="adcbc-378">PowerShell을 사용 하 여 피싱 규칙 보기</span><span class="sxs-lookup"><span data-stu-id="adcbc-378">Use PowerShell to view anti-phish rules</span></span>

<span data-ttu-id="adcbc-379">기존 피싱 규칙을 보려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-379">To view existing anti-phish rules, use the following syntax:</span></span>

```PowerShell
Get-AntiPhishRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="adcbc-380">이 예제에서는 지정 된 속성과 함께 모든 피싱 규칙의 요약 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-380">This example returns a summary list of all anti-phish rules along with the specified properties.</span></span>

```PowerShell
Get-AntiPhishRule | Format-Table Name,Priority,State
```

<span data-ttu-id="adcbc-381">활성화된 또는 비활성화된 규칙을 기준으로 목록을 필터링하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-381">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-AntiPhishRule -State Disabled | Format-Table Name,Priority
```

```PowerShell
Get-AntiPhishRule -State Enabled | Format-Table Name,Priority
```

<span data-ttu-id="adcbc-382">이 예에서는 Contoso 임원 이라는 피싱 규칙에 대 한 모든 속성 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-382">This example returns all the property values for the anti-phish rule named Contoso Executives.</span></span>

```PowerShell
Get-AntiPhishRule -Identity "Contoso Executives"
```

<span data-ttu-id="adcbc-383">구문과 매개 변수에 대 한 자세한 내용은 [AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishrule)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-383">For detailed syntax and parameter information, see [Get-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishrule).</span></span>

### <a name="use-powershell-to-modify-anti-phish-policies"></a><span data-ttu-id="adcbc-384">PowerShell을 사용 하 여 피싱 정책 수정</span><span class="sxs-lookup"><span data-stu-id="adcbc-384">Use PowerShell to modify anti-phish policies</span></span>

<span data-ttu-id="adcbc-385">다음 항목을 제외 하 고는이 항목 앞부분에 있는 [1 단계: powershell을 사용 하 여 피싱 정책 만들기](#step-1-use-powershell-to-create-an-anti-phish-policy) 섹션에 설명 된 대로, powershell을 만들 때 피싱 정책을 수정할 때도 같은 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-385">Other than the following items, the same settings are available when you modify an anti-phish policy in PowerShell as when you create the policy as described in the [Step 1: Use PowerShell to create an anti-phish policy](#step-1-use-powershell-to-create-an-anti-phish-policy) section earlier in this topic.</span></span>

- <span data-ttu-id="adcbc-386">지정 된 정책을 기본 정책으로 설정 하는 _makedefault_ 스위치 (모든 사용자에 게 적용 되며 항상 **가장 낮은** 우선 순위 이며 삭제할 수 없음)는 PowerShell에서 피싱 정책을 수정 하는 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-386">The _MakeDefault_ switch that turns the specified policy into the default policy (applied to everyone, always **Lowest** priority, and you can't delete it) is only available when you modify an anti-phish policy in PowerShell.</span></span>

- <span data-ttu-id="adcbc-387">피싱 정책의 이름을 바꿀 수는 없습니다 (AntiPhishPolicy cmdlet은 _Name_ 매개 변수를 **사용** 하지 않음).</span><span class="sxs-lookup"><span data-stu-id="adcbc-387">You can't rename an anti-phish policy (the **Set-AntiPhishPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="adcbc-388">보안 & 준수 센터에서 피싱 방지 정책의 이름을 바꾸면 피싱 _규칙_의 이름도 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-388">When you rename an anti-phishing policy in the Security & Compliance Center, you're only renaming the anti-phish _rule_.</span></span>

<span data-ttu-id="adcbc-389">피싱 정책을 수정 하려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-389">To modify an anti-phish policy, use this syntax:</span></span>

```PowerShell
Set-AntiPhishPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="adcbc-390">구문 및 매개 변수에 대 한 자세한 내용은 [AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-390">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-anti-phish-rules"></a><span data-ttu-id="adcbc-391">PowerShell을 사용 하 여 피싱 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="adcbc-391">Use PowerShell to modify anti-phish rules</span></span>

<span data-ttu-id="adcbc-392">PowerShell에서 피싱 규칙을 수정할 때 사용할 수 없는 설정은 사용 하지 않도록 설정 된 규칙을 만들 수 있는 _사용_ 가능한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-392">The only setting that isn't available when you modify an anti-phish rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="adcbc-393">기존 피싱 규칙을 사용 하거나 사용 하지 않도록 설정 하려면 다음 섹션을 참고 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-393">To enable or disable existing anti-phish rules, see the next section.</span></span>

<span data-ttu-id="adcbc-394">그렇지 않으면 PowerShell에서 피싱 규칙을 수정할 때 추가 설정을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-394">Otherwise, no additional settings are available when you modify an anti-phish rule in PowerShell.</span></span> <span data-ttu-id="adcbc-395">이 항목 앞부분에 있는 [2 단계: PowerShell을 사용 하 여 피싱 규칙 만들기](#step-2-use-powershell-to-create-an-anti-phish-rule) 섹션에 설명 된 대로 규칙을 만들 때도 같은 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-395">The same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create an anti-phish rule](#step-2-use-powershell-to-create-an-anti-phish-rule) section earlier in this topic.</span></span>

<span data-ttu-id="adcbc-396">피싱 규칙을 수정 하려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-396">To modify an anti-phish rule, use this syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="adcbc-397">구문 및 매개 변수에 대 한 자세한 내용은 [AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-antiphishrule)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-397">For detailed syntax and parameter information, see [Set-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/set-antiphishrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-anti-phish-rules"></a><span data-ttu-id="adcbc-398">PowerShell을 사용 하 여 피싱 규칙을 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="adcbc-398">Use PowerShell to enable or disable anti-phish rules</span></span>

<span data-ttu-id="adcbc-399">PowerShell에서 피싱 규칙을 사용 하거나 사용 하지 않도록 설정 하면 전체 피싱 방지 정책 (피싱 규칙 및 할당 된 피싱 정책)을 사용 하거나 사용 하지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-399">Enabling or disabling an anti-phish rule in PowerShell enables or disables the whole anti-phishing policy (the anti-phish rule and the assigned anti-phish policy).</span></span> <span data-ttu-id="adcbc-400">기본 피싱 방지 정책을 사용 하거나 사용 하지 않도록 설정할 수는 없습니다 (항상 모든 받는 사람에 게 적용 됨).</span><span class="sxs-lookup"><span data-stu-id="adcbc-400">You can't enable or disable the default anti-phishing policy (it's always applied to all recipients).</span></span>

<span data-ttu-id="adcbc-401">PowerShell에서 피싱 규칙을 사용 하거나 사용 하지 않도록 설정 하려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-401">To enable or disable an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-AntiPhishRule | Disable-AntiPhishRule> -Identity "<RuleName>"
```

<span data-ttu-id="adcbc-402">이 예에서는 Marketing 부서 라는 피싱 규칙을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-402">This example disables the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Disable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="adcbc-403">다음은 동일한 규칙을 사용하도록 설정하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-403">This example enables same rule.</span></span>

```PowerShell
Enable-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="adcbc-404">구문 및 매개 변수에 대 한 자세한 내용은 [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/enable-AntiPhishrule) 및 [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/disable-AntiPhishrule)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-404">For detailed syntax and parameter information, see [Enable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/enable-AntiPhishrule) and [Disable-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/disable-AntiPhishrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-anti-phish-rules"></a><span data-ttu-id="adcbc-405">PowerShell을 사용 하 여 피싱 규칙의 우선 순위 설정</span><span class="sxs-lookup"><span data-stu-id="adcbc-405">Use PowerShell to set the priority of anti-phish rules</span></span>

<span data-ttu-id="adcbc-406">규칙에 설정 가능한 가장 높은 우선 순위 값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-406">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="adcbc-407">설정할 수 있는 가장 낮은 값은 규칙 수에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-407">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="adcbc-408">예를 들어 규칙이 5개 있는 경우, 우선순위 값 0~4를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-408">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="adcbc-409">기존 규칙의 우선순위를 변경하면 다른 규칙에 계단식 효과를 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-409">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="adcbc-410">예를 들어 사용자 지정 규칙 5개(우선순위: 0~4)가 있고 규칙의 우선순위를 2로 변경하면, 우선순위 2인 기존 규칙이 우선순위 3으로 변경되고, 우선순위 3인 규칙이 우선순위 4로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-410">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="adcbc-411">PowerShell에서 피싱 규칙의 우선 순위를 설정 하려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-411">To set the priority of an anti-phish rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-AntiPhishRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="adcbc-412">다음은 Marketing Department라는 규칙의 우선순위를 2로 설정하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-412">This example sets the priority of the rule named Marketing Department to 2.</span></span> <span data-ttu-id="adcbc-413">우선순위가 2 이하인 모든 기존 규칙은 1씩 감소합니다(우선순위 번호는 1씩 증가함).</span><span class="sxs-lookup"><span data-stu-id="adcbc-413">All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-AntiPhishRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="adcbc-414">**참고:**</span><span class="sxs-lookup"><span data-stu-id="adcbc-414">**Notes**:</span></span>

- <span data-ttu-id="adcbc-415">새 규칙을 만들 때 우선 순위를 설정 하려면 대신 **AntiPhishRule** Cmdlet에서 _priority_ 매개 변수를 사용 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-415">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-AntiPhishRule** cmdlet instead.</span></span>

- <span data-ttu-id="adcbc-416">기본 피싱 정책에는 해당 하는 피싱 규칙이 없으며 항상 **가장 낮은**우선 순위 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-416">The default anti-phish policy doesn't have a corresponding anti-phish rule, and it always has the unmodifiable priority value **Lowest**.</span></span>

### <a name="use-powershell-to-remove-anti-phish-policies"></a><span data-ttu-id="adcbc-417">PowerShell을 사용 하 여 피싱 정책 제거</span><span class="sxs-lookup"><span data-stu-id="adcbc-417">Use PowerShell to remove anti-phish policies</span></span>

<span data-ttu-id="adcbc-418">PowerShell을 사용 하 여 피싱 정책을 제거 하면 해당 하는 피싱 규칙이 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-418">When you use PowerShell to remove an anti-phish policy, the corresponding anti-phish rule isn't removed.</span></span>

<span data-ttu-id="adcbc-419">PowerShell에서 피싱 정책을 제거 하려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-419">To remove an anti-phish policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="adcbc-420">이 예에서는 Marketing 학과 라는 피싱 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-420">This example removes the anti-phish policy named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishPolicy -Identity "Marketing Department"
```

<span data-ttu-id="adcbc-421">구문과 매개 변수에 대 한 자세한 내용은 [AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Remove-AntiPhishPolicy)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-421">For detailed syntax and parameter information, see [Remove-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Remove-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-remove-anti-phish-rules"></a><span data-ttu-id="adcbc-422">PowerShell을 사용 하 여 피싱 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="adcbc-422">Use PowerShell to remove anti-phish rules</span></span>

<span data-ttu-id="adcbc-423">PowerShell을 사용 하 여 피싱 규칙을 제거 하면 해당 하는 피싱 정책이 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-423">When you use PowerShell to remove an anti-phish rule, the corresponding anti-phish policy isn't removed.</span></span>

<span data-ttu-id="adcbc-424">PowerShell에서 피싱 규칙을 제거 하려면 다음 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-424">To remove an anti-phish rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "<PolicyName>"
```

<span data-ttu-id="adcbc-425">이 예에서는 Marketing 학과 라는 피싱 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-425">This example removes the anti-phish rule named Marketing Department.</span></span>

```PowerShell
Remove-AntiPhishRule -Identity "Marketing Department"
```

<span data-ttu-id="adcbc-426">구문과 매개 변수에 대 한 자세한 내용은 [AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Remove-AntiPhishRule)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="adcbc-426">For detailed syntax and parameter information, see [Remove-AntiPhishRule](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Remove-AntiPhishRule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="adcbc-427">이 절차가 제대로 수행되었는지 어떻게 확인하나요?</span><span class="sxs-lookup"><span data-stu-id="adcbc-427">How do you know these procedures worked?</span></span>

<span data-ttu-id="adcbc-428">ATP 피싱 방지 정책이 구성 되었는지 확인 하려면 다음 단계 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-428">To verify that you've successfully configured ATP anti-phishing policies, do any of the following steps:</span></span>

- <span data-ttu-id="adcbc-429">보안 & 준수 센터에서 **위협 관리** \> **정책** \> **ATP 피싱 방지**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-429">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span> <span data-ttu-id="adcbc-430">정책 목록, 해당 **상태** 값 및 해당 **우선 순위** 값을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-430">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="adcbc-431">자세한 정보를 보려면 다음 단계 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-431">To view more details do either of the following steps:</span></span>

  - <span data-ttu-id="adcbc-432">목록에서 정책을 선택 하 고 플라이 아웃의 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-432">Select the policy from the list, and view the details in the flyout.</span></span>
  - <span data-ttu-id="adcbc-433">**기본 정책을** 클릭 하 고 플라이 아웃에서 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-433">Click **Default policy** and view the details in the flyout.</span></span>

- <span data-ttu-id="adcbc-434">Exchange Online PowerShell에서 이름을 \<\> 정책 또는 규칙의 이름으로 바꾸고 다음 명령을 실행 하 고 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adcbc-434">In Exchange Online PowerShell, replace \<Name\> with the name of the policy or rule, and run the following command and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-AntiPhishRule -Identity "<Name>"
  ```