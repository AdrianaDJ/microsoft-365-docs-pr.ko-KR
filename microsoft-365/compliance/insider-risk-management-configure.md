---
title: 참가자 위험 관리 시작 (미리 보기)
description: 조직에서 참가자 위험 관리를 구성 합니다.
keywords: Microsoft 365, 참가자 위험 관리, 위험 관리, 규정 준수
localization_priority: Normal
ms.prod: Microsoft-365-enterprise
ms.topic: article
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection: m365-security-compliance
ms.openlocfilehash: 5d32e28d53fccbb16d935bbd9348ad7c12bac365
ms.sourcegitcommit: 3dca80f268006658a0b721aa4f6df1224c7964dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/22/2020
ms.locfileid: "41259846"
---
# <a name="get-started-with-insider-risk-management-preview"></a><span data-ttu-id="e246f-104">참가자 위험 관리 시작 (미리 보기)</span><span class="sxs-lookup"><span data-stu-id="e246f-104">Get started with insider risk management (preview)</span></span>

<span data-ttu-id="e246f-105">참가자 위험 관리 정책을 사용 하 여 조직의 위험 경고에 대해 조치를 취할 위험 작업 및 관리 도구를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-105">Use insider risk management policies to identify risky activities and management tools to take action on risk alerts in your organization.</span></span> <span data-ttu-id="e246f-106">사용자의 참가자 위험 정책을 통해 조직의 위험을 관리 하는 방법에 대 한 자세한 내용은 [Microsoft 365의 참가자 위험 관리](insider-risk-management.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e246f-106">For more information about how insider risk policies can help you manage risk in your organization, see [Insider risk management in Microsoft 365](insider-risk-management.md).</span></span>

>[!IMPORTANT]
><span data-ttu-id="e246f-107">Microsoft 365의 참가자 위험 관리 솔루션은 사용자 수준에서 내부 거 버 넌 스를 사용 하는 데 도움이 되는 거주자 수준 옵션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-107">The Microsoft 365 insider risk management solution provides a tenant level option to help customers facilitate internal governance at the user level.</span></span> <span data-ttu-id="e246f-108">테 넌 트 수준 관리자는 조직의 구성원에 대해이 솔루션에 대 한 액세스 권한을 제공 하 고 Microsoft 365 준수 센터에서 데이터 커넥터를 설정 하 여 사용자 수준 식별을 지원 하기 위해 관련 데이터를 가져올 수 있는 권한 설정 가능 위험한 활동</span><span class="sxs-lookup"><span data-stu-id="e246f-108">Tenant level administrators can set up permissions to provide access to this solution for members of your organization and set up data connectors in the Microsoft 365 compliance center to import relevant data to support user level identification of potentially risky activity.</span></span> <span data-ttu-id="e246f-109">고객은 개별 사용자 동작, 문자 또는 고용와 관련 된 성능 materially 관련 된 정보를 관리자가 계산 하 고 조직의 다른 사용자가 사용할 수 있게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-109">Customers acknowledge insights related to the individual users behavior, character, or performance materially related to employment can be calculated by the administrator and made available to others in the organization.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="e246f-110">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="e246f-110">Before you begin</span></span>

<span data-ttu-id="e246f-111">참가자 위험 관리를 시작 하기 전에 Microsoft 365 구독을 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-111">Before you get started with insider risk management, you should confirm your Microsoft 365 subscription.</span></span> <span data-ttu-id="e246f-112">참가자 위험 관리 정책에 포함 된 사용자는 microsoft 365 E5 구독에 포함 되거나 microsoft 365 E5 규정 준수 라이선스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-112">Users included in insider risk management policies must have a Microsoft 365 E5 Compliance license or be included in a Microsoft 365 E5 subscription.</span></span>

<span data-ttu-id="e246f-113">Microsoft 365 Enterprise E5 요금제가 아직 없는 경우 microsoft 365을 기존 Office 365 구독에 [추가](https://docs.microsoft.com/office365/admin/try-or-buy-microsoft-365) 하거나 Microsoft 365 Enterprise E5 [평가판에 등록할](https://www.microsoft.com/microsoft-365/enterprise) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-113">If you don't have an existing Microsoft 365 Enterprise E5 plan and want to try insider risk management, you can [add Microsoft 365](https://docs.microsoft.com/office365/admin/try-or-buy-microsoft-365) to your existing Office 365 subscription or [sign up for a trial](https://www.microsoft.com/microsoft-365/enterprise) of Microsoft 365 Enterprise E5.</span></span>

<span data-ttu-id="e246f-114">Microsoft 365 조직에서 다음 단계를 완료 하 여 참가자 위험 관리를 설정 하 고 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-114">Complete these steps to set up and use insider risk management in your Microsoft 365 organization:</span></span>

## <a name="step-1-required-enable-permissions-for-insider-risk-management"></a><span data-ttu-id="e246f-115">1 단계 (필수 사항): 참가자 위험 관리에 대 한 사용 권한 설정</span><span class="sxs-lookup"><span data-stu-id="e246f-115">Step 1 (required): Enable permissions for insider risk management</span></span>

<span data-ttu-id="e246f-116">참가자 위험 관리를 구성 하 고 관리 하는 데 사용 되는 네 가지 권한 역할이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-116">There are four permission roles used to configure and manage insider risk management.</span></span> <span data-ttu-id="e246f-117">이러한 구성 단계를 계속 하려면 테 넌 트 관리자가 먼저 **참가자 위험 관리 관리자** 역할을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-117">To continue with these configuration steps, your tenant administrators must first assign you the **Insider Risk Management Admin** role.</span></span>

| <span data-ttu-id="e246f-118">**역할**</span><span class="sxs-lookup"><span data-stu-id="e246f-118">**Role**</span></span> | <span data-ttu-id="e246f-119">**역할 권한**</span><span class="sxs-lookup"><span data-stu-id="e246f-119">**Role permissions**</span></span> |
| ---- | ---------------- |
| <span data-ttu-id="e246f-120">**참가자 위험 관리 관리자**</span><span class="sxs-lookup"><span data-stu-id="e246f-120">**Insider Risk Management Admin**</span></span> | <span data-ttu-id="e246f-121">참가자 위험 관리 정책 만들기, 읽기, 업데이트 및 삭제</span><span class="sxs-lookup"><span data-stu-id="e246f-121">Create, read, update, and delete insider risk management policies</span></span> <br> <span data-ttu-id="e246f-122">참가자 위험 관리 사용 권한 및 역할 만들기, 읽기, 업데이트 및 삭제</span><span class="sxs-lookup"><span data-stu-id="e246f-122">Create, read, update, and delete insider risk management permissions and roles</span></span> |
| <span data-ttu-id="e246f-123">**참가자 위험 관리 분석가**</span><span class="sxs-lookup"><span data-stu-id="e246f-123">**Insider Risk Management Analysts**</span></span> | <span data-ttu-id="e246f-124">모든 참가자 위험 관리 알림, 사례 및 알림 액세스</span><span class="sxs-lookup"><span data-stu-id="e246f-124">Access to all insider risk management alerts, cases, and notices</span></span> |
| <span data-ttu-id="e246f-125">**참가자 위험 관리 Investigators**</span><span class="sxs-lookup"><span data-stu-id="e246f-125">**Insider Risk Management Investigators**</span></span> | <span data-ttu-id="e246f-126">모든 경우에 대 한 모든 참가자 위험 관리 알림, 사례, 알림 및 콘텐츠 탐색기에 대 한 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="e246f-126">Access to all insider risk management alerts, cases, notices, and the Content Explorer for all cases</span></span> |
| <span data-ttu-id="e246f-127">**참가자 위험 관리 뷰어**</span><span class="sxs-lookup"><span data-stu-id="e246f-127">**Insider Risk Management Viewer**</span></span> | <span data-ttu-id="e246f-128">모든 경우에 대 한 모든 참가자 위험 관리 알림, 사례, 알림 및 콘텐츠 탐색기에 대 한 보기 전용 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="e246f-128">View-only access to all insider risk management alerts, cases, notices, and the Content Explorer for all cases</span></span> |

<span data-ttu-id="e246f-129">준수 관리 팀의 구조에 따라 참가자 위험 관리 기능을 관리 하도록 역할을 구성 하기 위한 두 가지 권한 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-129">Depending on the structure of your compliance management team, you have two permission options to configure roles to manage insider risk management features.</span></span> <span data-ttu-id="e246f-130">참가자 위험 관리를 구성할 때 다음 역할 관리 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-130">Choose one of these role management options when configuring insider risk management:</span></span>

1. <span data-ttu-id="e246f-131">**기본 참가자 위험 관리 역할 그룹 사용**:이 역할 그룹을 사용 하 여 지정 된 관리자, 분석가 및 investigators에 대 한 모든 사용자 계정을 단일 그룹에 추가 하 여 조직의 참가자 위험 관리를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-131">**Use the default Insider Risk Management role group**: Use this role group to manage insider risk management for your organization by adding all user accounts for designated administrators, analysts, and investigators in a single group.</span></span> <span data-ttu-id="e246f-132">이 역할 그룹에는 모든 참가자 위험 관리 권한 역할이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-132">This role group contains all the insider risk management permission roles.</span></span> <span data-ttu-id="e246f-133">이 방법은 참가자 위험 관리를 빠르게 시작할 수 있는 가장 쉬운 방법 이며 개별 사용자 그룹에 대해 정의 된 별도의 사용 권한이 필요 하지 않은 조직에 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-133">This is the easiest way to quickly get started with insider risk management and is a good fit for organizations that do not need separate permissions defined for separate groups of users.</span></span>
2. <span data-ttu-id="e246f-134">**다른 관리 역할에 대해 서로 다른 그룹 만들기**: 참가자 위험 관리 구성 및 관리에 대 한 권한을 구분 해야 하는 조직에서는 새 역할 그룹을 만들고 해당 역할과 사용자를 새 그룹에 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-134">**Create different groups for different management roles**: For organizations that need to separate permissions for configuring and managing insider risk management, you'll need to create new role groups and assign appropriate roles and users to the new groups.</span></span> <span data-ttu-id="e246f-135">예를 들어 참가자 위험 관리 분석과 조사에 대해 서로 다른 사용 권한을 부여 하려면 분석가가 사용할 그룹을 만들고 investigators에 대해 별도의 그룹을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-135">For example, if you want different permissions for insider risk management analysis and investigations, you'll need to create a group for analysts and a separate group for investigators.</span></span> <span data-ttu-id="e246f-136">각 그룹에 대해 이러한 책임에 필요한 역할을 할당 한 다음 그룹에 할당 해야 하는 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-136">For each group, you'll assign the required roles for these responsibilities and then add the users that should be assigned to the group.</span></span>

<span data-ttu-id="e246f-137">각 역할에 대해 서로 다른 그룹을 구성 하려는 경우 다음 표를 사용 하 여 필요한 역할을 각 역할 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-137">If you decide to configure different groups for different roles, use the following table to assign the required roles to each role group:</span></span>

| <span data-ttu-id="e246f-138">**그룹 예제**</span><span class="sxs-lookup"><span data-stu-id="e246f-138">**Group example**</span></span> | <span data-ttu-id="e246f-139">**필요한 역할**</span><span class="sxs-lookup"><span data-stu-id="e246f-139">**Required roles**</span></span> |
| ---- | ---------------- |
| <span data-ttu-id="e246f-140">**관리자**</span><span class="sxs-lookup"><span data-stu-id="e246f-140">**Administrators**</span></span> | <span data-ttu-id="e246f-141">*참가자 위험 관리 관리자* 역할</span><span class="sxs-lookup"><span data-stu-id="e246f-141">*Insider Risk Management Admin* role</span></span> |
| <span data-ttu-id="e246f-142">**자가**</span><span class="sxs-lookup"><span data-stu-id="e246f-142">**Analysts**</span></span> | <span data-ttu-id="e246f-143">*참가자 위험 관리 분석가* 역할</span><span class="sxs-lookup"><span data-stu-id="e246f-143">*Insider Risk Management Analysts* role</span></span> <br> <span data-ttu-id="e246f-144">*사례 관리* 역할</span><span class="sxs-lookup"><span data-stu-id="e246f-144">*Case Management* role</span></span> |
| <span data-ttu-id="e246f-145">**Investigators**</span><span class="sxs-lookup"><span data-stu-id="e246f-145">**Investigators**</span></span> | <span data-ttu-id="e246f-146">*참가자 위험 관리 Investigators* 역할</span><span class="sxs-lookup"><span data-stu-id="e246f-146">*Insider Risk Management Investigators* role</span></span> <br> <span data-ttu-id="e246f-147">*사례 관리* 역할</span><span class="sxs-lookup"><span data-stu-id="e246f-147">*Case Management* role</span></span> |

### <a name="option-1-add-users-to-the-insider-risk-management-role-group"></a><span data-ttu-id="e246f-148">옵션 1: 참가자 위험 관리 역할 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="e246f-148">Option 1: Add users to the Insider Risk Management role group</span></span>

<span data-ttu-id="e246f-149">모든 사용자에 게 참가자 위험 관리를 구성 및 관리 하는 역할 그룹을 하나 사용 하려면 다음 단계를 완료 하 여 기본 **참가자 위험 관리** 역할 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-149">If you want to use one role group for all users configuring and managing insider risk management, complete the following steps to add users to the default **Insider Risk Management** role group:</span></span>

1. <span data-ttu-id="e246f-150">Microsoft 365 [https://protection.office.com/permissions](https://protection.office.com/permissions) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-150">Sign into [https://protection.office.com/permissions](https://protection.office.com/permissions) using credentials for an admin account in your Microsoft 365 organization.</span></span>

2. <span data-ttu-id="e246f-151">Microsoft Office 365 보안 및 준수 센터에서 **사용 권한**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-151">In the Microsoft Office 365 security and compliance center, go to **Permissions**.</span></span> <span data-ttu-id="e246f-152">Office 365에서 역할을 보고 관리 하는 링크를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-152">Select the link to view and manage roles in Office 365.</span></span>

3. <span data-ttu-id="e246f-153">*참가자 위험 관리* 역할 그룹을 선택 하 고 **역할 그룹 편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-153">Select the *Insider Risk Management* role group, then select **Edit role group**.</span></span>

4. <span data-ttu-id="e246f-154">왼쪽 탐색 창에서 **구성원 선택을** 선택 하 고 **편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-154">Select **Choose members** from the left navigation pane, then select **Edit**.</span></span>

5. <span data-ttu-id="e246f-155">**추가** 를 선택한 다음 역할 그룹에 추가 하려는 모든 사용자의 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-155">Select **Add** and then select the checkbox for all users you want to add to the role group.</span></span>

6. <span data-ttu-id="e246f-156">**추가**를 선택한 다음 **완료**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-156">Select **Add**, then select **Done**.</span></span>

7. <span data-ttu-id="e246f-157">**저장** 을 선택 하 여 역할 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-157">Select **Save** to add the users to the role group.</span></span> <span data-ttu-id="e246f-158">**닫기를** 선택 하 여 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-158">Select **Close** to complete the steps.</span></span>

### <a name="option-2-create-a-new-role-group"></a><span data-ttu-id="e246f-159">옵션 2: 새 역할 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="e246f-159">Option 2: Create a new role group</span></span>

<span data-ttu-id="e246f-160">다른 관리 역할에 대 한 별도의 역할 그룹을 만들어야 하는 경우에는 다음 단계를 완료 하 여 각각의 새 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-160">If you need to create separate role groups for different management roles, complete the following steps to create each new group:</span></span>

1. <span data-ttu-id="e246f-161">Microsoft 365 [https://protection.office.com/permissions](https://protection.office.com/permissions) 조직의 관리자 계정에 대 한 자격 증명을 사용 하 여 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-161">Sign into [https://protection.office.com/permissions](https://protection.office.com/permissions) using credentials for an admin account in your Microsoft 365 organization.</span></span>

2. <span data-ttu-id="e246f-162">Microsoft Office 365 보안 및 준수 센터에서 **사용 권한**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-162">In the Microsoft Office 365 security and compliance center, go to **Permissions**.</span></span> <span data-ttu-id="e246f-163">Office 365에서 역할을 보고 관리 하는 링크를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-163">Select the link to view and manage roles in Office 365.</span></span>

3. <span data-ttu-id="e246f-164">**만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-164">Select **Create**.</span></span>

4. <span data-ttu-id="e246f-165">**이름** 필드에서 새 역할 그룹에 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-165">In the **Name** field, give the new role group a friendly name.</span></span> <span data-ttu-id="e246f-166"> Select **Next**. </span><span class="sxs-lookup"><span data-stu-id="e246f-166">Select **Next**.</span></span>

5. <span data-ttu-id="e246f-167">**역할 선택을** 선택 하 고 **추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-167">Select **Choose roles** and then select **Add**.</span></span> <span data-ttu-id="e246f-168">할당 해야 하는 역할의 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-168">Select the checkbox for the roles you need to assign.</span></span> <span data-ttu-id="e246f-169">예를 들어이 그룹이 참가자 위험 분석가 인 경우에는 *참가자 위험 관리 분석가* 역할과 *사례 관리* 역할을 선택 하 고 **추가** 및 **완료**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-169">For example, if this group is for insider risk analysts, select the *Insider Risk Management Analysts* role and the *Case Management* role, then select **Add** and **Done**.</span></span> <span data-ttu-id="e246f-170"> Select **Next**. </span><span class="sxs-lookup"><span data-stu-id="e246f-170">Select **Next**.</span></span>

6. <span data-ttu-id="e246f-171">**구성원 선택을** 선택 하 고 **추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-171">Select **Choose members** and then select **Add**.</span></span> <span data-ttu-id="e246f-172">정책을 만들 모든 사용자 및 그룹에 대 한 확인란을 선택 하 고 정책 일치가 포함 된 메시지를 관리 한 다음 **추가** 및 **완료**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-172">Select the checkbox for all the users and groups you want create policies and manage messages with policy matches, then select **Add** and **Done**.</span></span> <span data-ttu-id="e246f-173"> Select **Next**. </span><span class="sxs-lookup"><span data-stu-id="e246f-173">Select **Next**.</span></span>

7. <span data-ttu-id="e246f-174">마칠 **역할 그룹 만들기** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-174">Select **Create role group** to finish.</span></span>

<span data-ttu-id="e246f-175">역할 그룹 및 사용 권한에 대 한 자세한 내용은 [준수 센터의 사용 권한을](../security/office-365-security/protect-against-threats.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e246f-175">For more information about role groups and permissions, see [Permissions in the Compliance Center](../security/office-365-security/protect-against-threats.md).</span></span>

## <a name="step-2-optional-configure-the-microsoft-365-human-resources-data-connector"></a><span data-ttu-id="e246f-176">2 단계 (선택 사항): Microsoft 365 인적 자원 데이터 커넥터 구성</span><span class="sxs-lookup"><span data-stu-id="e246f-176">Step 2 (optional): Configure the Microsoft 365 human resources data connector</span></span>

<span data-ttu-id="e246f-177">참가자 위험 관리는 타사 위험 관리 및 인적 자원 플랫폼에서 가져온 사용자 및 로그 데이터를 가져오는 것을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-177">Insider risk management supports importing user and log data imported from 3rd-party risk management and human resources platforms.</span></span> <span data-ttu-id="e246f-178">Microsoft 365 인적 자원 (HR) 데이터 커넥터를 사용 하면 사용자 종료 및 마지막 고용 날짜를 포함 하 여 CSV 파일에서 인적 자원 데이터를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-178">The Microsoft 365 Human Resources (HR) data connector allows you to pull in human resources data from CSV files, including user termination and last employment dates.</span></span> <span data-ttu-id="e246f-179">이 데이터는 참가자 위험 관리 정책에 대 한 경고 지표를 구동 하는 데 도움이 되며, 조직의 전체 위험 관리 범위를 구성 하는 중요 한 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-179">This data helps drive the alert indicators in insider risk management policies and is an important part of configuring full risk management coverage in your organization.</span></span>

<span data-ttu-id="e246f-180">조직에 대 한 Microsoft 365 HR 커넥터를 구성 하려면 단계별 지침을 보려면 [HR 데이터를 가져올 커넥터 설정](import-hr-data.md) 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e246f-180">See the [Set up a connector to import HR data](import-hr-data.md) topic for step-by-step guidance to configure the Microsoft 365 HR Connector for your organization.</span></span> <span data-ttu-id="e246f-181">HR 커넥터를 구성한 후에는 다음 구성 단계로 돌아가십시오.</span><span class="sxs-lookup"><span data-stu-id="e246f-181">After you've configured the HR Connector, return to these configuration steps.</span></span>

>[!IMPORTANT]
><span data-ttu-id="e246f-182">*Departing employee data 절도* 서식 파일을 사용 하 여 정책을 구성 하려는 경우에는 정책 템플릿의 전체 신호 검색 기능을 사용 하도록 HR 커넥터를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-182">If you plan on configuring a policy using the *Departing employee data theft* template, you'll need to configure the HR Connector to use the full signal detection features of the policy template.</span></span> <span data-ttu-id="e246f-183">조직에 대해 두 개 이상의 HR 커넥터를 구성 하는 경우, 참가자 위험 관리는 모든 HR 커넥터에서 자동으로 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-183">If you configure more than one HR Connector for your organization, insider risk management will automatically pull indicators from all HR Connectors.</span></span>

## <a name="step-3-optional-configure-data-loss-prevention-dlp-policies"></a><span data-ttu-id="e246f-184">3 단계 (선택 사항): DLP (데이터 손실 방지) 정책 구성</span><span class="sxs-lookup"><span data-stu-id="e246f-184">Step 3 (optional): Configure Data Loss Prevention (DLP) policies</span></span>

<span data-ttu-id="e246f-185">참가자 위험 관리는 DLP 정책을 사용 하 여 원하지 않는 사용자에 게 중요 한 정보를 고의적으로 또는 실수로 노출 하는 것을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-185">Insider risk management supports using DLP policies to help identify the intentional or accidental exposure of sensitive information to unwanted parties.</span></span> <span data-ttu-id="e246f-186">*데이터 누수* 템플릿을 사용 하 여 참가자 위험 관리 정책을 구성 하는 경우 정책에 특정 DLP 정책을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-186">When configuring an insider risk management policy with the *Data leaks* template, you have to assign a specific DLP policy to the policy.</span></span> <span data-ttu-id="e246f-187">이 정책은 중요 한 정보에 대 한 경고 표시기를 구성 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-187">This policy helps drive the alert indicators for sensitive information is an important part of configuring full risk management coverage in your organization.</span></span>

<span data-ttu-id="e246f-188">조직의 DLP 정책을 구성 하는 단계별 지침은 [dlp 정책 만들기, 테스트 및 조정](create-test-tune-dlp-policy.md) 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="e246f-188">See the [Create, test, and tune a DLP policy](create-test-tune-dlp-policy.md) topic for step-by-step guidance to configure DLP policies for your organization.</span></span> <span data-ttu-id="e246f-189">DLP 정책을 구성한 후에는 다음 구성 단계로 돌아가십시오.</span><span class="sxs-lookup"><span data-stu-id="e246f-189">After you've configured a DLP policy, return to these configuration steps.</span></span>

>[!IMPORTANT]
><span data-ttu-id="e246f-190">*데이터 누수* 템플릿을 사용 하 여 정책을 구성 하려는 경우에는 정책 템플릿의 전체 신호 검색 기능을 사용 하도록 하나 이상의 DLP 정책을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-190">If you plan on configuring a policy using the *Data leaks* template, you'll need to configure at least one DLP policy to use the full signal detection features of the policy template.</span></span> <span data-ttu-id="e246f-191">조직에 대해 두 개 이상의 DLP 정책을 구성 하는 경우에는 DLP 정책에 따라 참가자 위험 관리 정책을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-191">If you configure more than one DLP policy for your organization, you'll need to assign an insider risk management policy per DLP policy.</span></span>

## <a name="step-4-required-create-an-insider-risk-management-policy"></a><span data-ttu-id="e246f-192">4 단계 (필수 사항): 참가자 위험 관리 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e246f-192">Step 4 (required): Create an insider risk management policy</span></span>

<span data-ttu-id="e246f-193">참가자 위험 관리 정책에는 할당 된 사용자 및 경고에 대해 구성 된 위험 표시기 유형이 정의 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-193">Insider risk management policies include assigned users and define which types of risk indicators are configured for alerts.</span></span> <span data-ttu-id="e246f-194">활동이 알림을 트리거하도록 하려면 정책을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-194">Before activities can trigger alerts, a policy must be configured.</span></span>

1. <span data-ttu-id="e246f-195">[Microsoft 365 준수 센터](https://compliance.microsoft.com)에서 **참가자 위험 관리** 로 이동 하 여 **정책** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-195">In the [Microsoft 365 compliance center](https://compliance.microsoft.com), go to **Insider risk management** and select the **Policies** tab.</span></span>
2. <span data-ttu-id="e246f-196">**정책 만들기** 를 선택 하 여 정책 마법사를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-196">Select **Create policy** to open the policy wizard</span></span>
3. <span data-ttu-id="e246f-197">**새 참가자 위험 정책** 페이지에서 다음 필드를 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-197">On the **New insider risk policy** page, complete the following fields:</span></span>
    - <span data-ttu-id="e246f-198">**이름 (필수 사항)**: 정책의 친근 한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-198">**Name (required)**: Enter a friendly name for the policy</span></span>
    - <span data-ttu-id="e246f-199">**설명 (선택 사항)**: 정책에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-199">**Description (optional)**: Enter a description for the policy.</span></span>
    - <span data-ttu-id="e246f-200">**정책 템플릿 선택 (필수)**: 정책 [템플릿](insider-risk-management-policies.md#policy-templates) 중 하나를 선택 하 여 위험 지표 유형을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-200">**Choose policy template (required)**: Select one of the [policy templates](insider-risk-management-policies.md#policy-templates) to define the types of risk indicators are monitored by the policy.</span></span>

    >[!IMPORTANT]
    ><span data-ttu-id="e246f-201">*데이터 누수* 템플릿을 선택한 경우 나중에 마법사에서 할당할 하나 이상의 DLP 정책을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-201">If you select the *Data leaks* template, you'll need to configure at least one DLP policy that you'll assign later in the wizard.</span></span> <span data-ttu-id="e246f-202">*Departing employee data 절도* 서식 파일을 선택 하는 경우 정책 템플릿의 전체 신호 검색 기능을 사용 하도록 HR 커넥터를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-202">If you select the *Departing employee data theft* template, you'll need to configure the HR Connector to use the full signal detection features of the policy template.</span></span>

4. <span data-ttu-id="e246f-203">계속 하려면 **다음** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-203">Select **Next** to continue.</span></span>
5. <span data-ttu-id="e246f-204">**사용자** 페이지에서 **사용자 또는 그룹 추가** 를 선택 하 여 정책에 포함 되는 사용자를 정의 하거나 **모든 사용자 및 메일 사용이 가능한 그룹** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-204">On the **Users** page, select **Add user or group** to define which users are included in the policy or select **All users and mail-enabled groups** checkbox.</span></span> <span data-ttu-id="e246f-205">계속 하려면 **다음** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-205">Select **Next** to continue.</span></span>
6. <span data-ttu-id="e246f-206">**우선 순위를 지정할 콘텐츠 지정 (선택 사항)** 페이지에서 위험한 사용자 활동에 대해 우선 순위를 지정할 소스를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-206">On the **Specify what content to prioritize (optional)** page, you can assign the sources to prioritize for risky user activities:</span></span>
    - <span data-ttu-id="e246f-207">**Sharepoint 사이트**: **sharepoint 사이트 추가** 를 선택 하 고 우선 순위를 지정할 SharePoint 조직을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-207">**SharePoint sites**: Select **Add SharePoint site** and select the SharePoint organizations you want to prioritize.</span></span> <span data-ttu-id="e246f-208">예를 들면 *"group1@contoso.sharepoint.com/sites/group1"* 입니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-208">For example, *"group1@contoso.sharepoint.com/sites/group1"*.</span></span>
    - <span data-ttu-id="e246f-209">**중요 한 정보 유형**: **중요 한 정보 유형 추가** 를 선택 하 고 우선 순위를 지정할 민감도 유형을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-209">**Sensitive info type**: Select **Add sensitive info type** and select the sensitivity types you want to prioritize.</span></span> <span data-ttu-id="e246f-210">예를 들어 *"미국 은행 계좌 번호"* 및 *"신용 카드 번호"* 를 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-210">For example, *"U.S. Bank Account Number"* and *"Credit Card Number"*.</span></span>
    - <span data-ttu-id="e246f-211">**민감도 레이블**: **민감도 레이블 추가** 를 선택 하 고 우선 순위를 지정할 레이블을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-211">**Sensitivity labels**: Select **Add sensitivity label** and select the labels you want to prioritize.</span></span> <span data-ttu-id="e246f-212">예를 들어 *"기밀"* 및 *"비밀"* 가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-212">For example, *"Confidential"* and *"Secret"*.</span></span>
7. <span data-ttu-id="e246f-213">계속 하려면 **다음** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-213">Select **Next** to continue.</span></span>
8. <span data-ttu-id="e246f-214">**알림 지표 선택** 페이지에이 정책에 대해 선택한 서식 파일에 포함 된 표시기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-214">On the **Choose alert indicators** page, you'll see the indicators that are included in the template that you've chosen for this policy.</span></span> <span data-ttu-id="e246f-215">마법사 시작 부분에서 *데이터 누수* 템플릿을 선택한 경우 **dlp 정책** 드롭다운 목록에서 dlp 정책을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-215">If you selected the *Data leaks* template at the beginning of the wizard, you must select a DLP policy from the **DLP policy** dropdown list.</span></span>
9. <span data-ttu-id="e246f-216">**모니터링 창 선택** 페이지에서는 정책에 대 한 [모니터링 창 조건을](insider-risk-management-policies.md#monitoring-windows) 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-216">On the **Select monitoring window** page, you'll define the [monitoring window conditions](insider-risk-management-policies.md#monitoring-windows) for the policy.</span></span> <span data-ttu-id="e246f-217">모니터링 창을 적절 하 게 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-217">Configure the monitoring windows as appropriate.</span></span>
10. <span data-ttu-id="e246f-218">계속 하려면 **다음** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-218">Select **Next** to continue.</span></span>
11. <span data-ttu-id="e246f-219">**검토** 페이지에서 정책에 대해 선택한 설정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-219">On the **Review** page, review the settings you've chosen for the policy.</span></span> <span data-ttu-id="e246f-220">**편집** 을 선택 하 여 정책 값을 변경 하거나 **제출을** 선택 하 여 정책을 만들고 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-220">Select **Edit** to change any of the policy values or select **Submit** to create and activate the policy.</span></span>

<span data-ttu-id="e246f-221">첫 번째 참가자 위험 관리 정책을 만들기 위해 이러한 단계를 완료 한 후에는 약 24 시간 후에 활동 표시기에서 경고를 수신 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-221">After you've completed these steps to create your first insider risk management policy, you'll start to receive alerts from activity indicators after about 24 hours.</span></span> <span data-ttu-id="e246f-222">이 항목의 4 단계 또는 [새 참가자 위험 정책 만들기](insider-risk-management-policies.md#create-a-new-policy)의 단계에 나와 있는 지침을 사용 하 여 필요에 따라 추가 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e246f-222">Configure additional policies as needed using the guidance in Step 4 of this topic or the steps in [Create a new insider risk policy](insider-risk-management-policies.md#create-a-new-policy).</span></span>