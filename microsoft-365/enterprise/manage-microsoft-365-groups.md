---
title: Microsoft 365 그룹 관리
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-mar2020
ms.collection:
- Ent_O365
- M365-subscription-management
search.appverid:
- MET150
- MOE150
- MED150
- BCS160
ms.assetid: 98ca5b3f-f720-4d8e-91be-fe656548a25a
description: Microsoft 365 그룹을 관리 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: a01bf5dcc0b87cbdce8d7044b666cfb3a16a5aa9
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48328555"
---
# <a name="manage-microsoft-365-groups"></a><span data-ttu-id="1e356-103">Microsoft 365 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="1e356-103">Manage Microsoft 365 groups</span></span>

<span data-ttu-id="1e356-104">*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*</span><span class="sxs-lookup"><span data-stu-id="1e356-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="1e356-105">구성에 따라 다양 한 방식으로 Microsoft 365 그룹을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-105">You can manage Microsoft 365 groups in several different ways, depending on your configuration.</span></span> <span data-ttu-id="1e356-106">[Microsoft 365 관리 센터](https://docs.microsoft.com/microsoft-365/admin/add-users/), POWERSHELL, AD DS (Active Directory 도메인 서비스) 또는 azure [Ad (active directory) 관리 센터](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)에서 사용자 계정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-106">You can manage user accounts in the [Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/add-users/), PowerShell, in Active Directory Domain Services (AD DS), or in the [Azure Active Directory (Azure AD) admin center](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span> 

## <a name="plan-for-where-and-how-you-will-manage-your-groups"></a><span data-ttu-id="1e356-107">그룹을 관리할 위치 및 방법 계획</span><span class="sxs-lookup"><span data-stu-id="1e356-107">Plan for where and how you will manage your groups</span></span>

<span data-ttu-id="1e356-108">사용자 계정을 관리할 수 있는 위치와 방법은 Microsoft 365에 사용할 id 모델에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-108">Where and how you can manage your user accounts depends on the identity model you want to use for your Microsoft 365.</span></span> <span data-ttu-id="1e356-109">전체 모델은 클라우드 전용 모델과 하이브리드입니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-109">The two overall models are cloud-only and hybrid.</span></span>
  
### <a name="cloud-only"></a><span data-ttu-id="1e356-110">클라우드 전용</span><span class="sxs-lookup"><span data-stu-id="1e356-110">Cloud-only</span></span>

<span data-ttu-id="1e356-111">다음을 사용 하 여 그룹을 만들고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-111">You create and manage groups with:</span></span>

- [<span data-ttu-id="1e356-112">Microsoft 365 관리 센터</span><span class="sxs-lookup"><span data-stu-id="1e356-112">The Microsoft 365 admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/add-users/)
- [<span data-ttu-id="1e356-113">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e356-113">PowerShell</span></span>](maintain-group-membership-with-microsoft-365-powershell.md)
- [<span data-ttu-id="1e356-114">Azure AD 관리 센터</span><span class="sxs-lookup"><span data-stu-id="1e356-114">Azure AD admin center</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
    
### <a name="hybrid"></a><span data-ttu-id="1e356-115">하이브리드</span><span class="sxs-lookup"><span data-stu-id="1e356-115">Hybrid</span></span>

<span data-ttu-id="1e356-116">AD DS 그룹은 AD DS에서 Microsoft 365와 동기화 되므로 이러한 그룹을 관리 하려면 온-프레미스 AD DS 도구를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-116">AD DS groups are synchronized with Microsoft 365 from AD DS, so you must use on-premises AD DS tools to manage these groups.</span></span>

<span data-ttu-id="1e356-117">AD DS 그룹과는 별도로 Azure AD 그룹을 만들고 관리할 수도 있지만 AD DS에서 사용자 및 그룹을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-117">You can also create and manage Azure AD groups that are separate from AD DS groups but can contain users and groups from AD DS.</span></span> <span data-ttu-id="1e356-118">이 경우 다음을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-118">In this case, you can use:</span></span>

- [<span data-ttu-id="1e356-119">Microsoft 365 관리 센터</span><span class="sxs-lookup"><span data-stu-id="1e356-119">The Microsoft 365 admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/add-users/)
- [<span data-ttu-id="1e356-120">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e356-120">PowerShell</span></span>](maintain-group-membership-with-microsoft-365-powershell.md)
- [<span data-ttu-id="1e356-121">Azure AD 관리 센터</span><span class="sxs-lookup"><span data-stu-id="1e356-121">Azure AD admin center</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

## <a name="allow-users-to-create-and-manage-their-own-groups"></a><span data-ttu-id="1e356-122">사용자가 자신의 그룹을 만들고 관리하도록 허용하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e356-122">Allow users to create and manage their own groups</span></span>

<span data-ttu-id="1e356-123">Azure AD는 IT 관리자가 아닌 그룹 소유자가 관리할 수 있는 그룹을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-123">Azure AD allows groups that can be managed by group owners instead of IT administrators.</span></span> <span data-ttu-id="1e356-124">*셀프 서비스 그룹 관리*로 알려진 기능은 관리역할이 할당되지 않은 그룹 소유자가 보안 그룹을 생성하고 관리할 수 있도록 해줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-124">Known as *self-service group management*, this feature allows group owners who are not assigned an administrative role to create and manage security groups.</span></span> 

<span data-ttu-id="1e356-p105">사용자는 보안 그룹에서 구성원을 요청할 수 있으며, 이 요청은 IT 관리자가 아니라 그룹 소유자에게 전달됩니다. 이를 통해 그룹의 비즈니스 사용을 이해하고 해당 구성원을 관리할 수 있는 팀, 프로젝트 또는 비즈니스 소유자에게 일상적인 그룹 구성원 제어를 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-p105">Users can request membership in a security group and that request goes to the group owner, rather than an IT administrator. This allows the day-to-day control of group membership to be delegated to team, project, or business owners who understand the business use for the group and can manage its membership.</span></span>

>[!Note]
><span data-ttu-id="1e356-127">셀프 서비스 그룹 관리는 Azure AD 보안 및 Microsoft 365 그룹에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-127">Self-service group management is available only for Azure AD security and Microsoft 365 groups.</span></span> <span data-ttu-id="1e356-128">메일 사용이 가능한 그룹, 메일 목록 또는 AD DS에서 동기화 된 그룹에는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-128">It is not available for mail-enabled groups, distribution lists, or any group that has been synchronized from AD DS.</span></span>
>

<span data-ttu-id="1e356-129">자세한 내용은 [셀프 서비스 관리에 대한 Azure AD(Microsoft Azure Active Directory) 그룹 구성 지침](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1e356-129">For more information, see the [instructions to configure an Azure AD group for self-service management](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management).</span></span>

## <a name="set-up-dynamic-group-membership"></a><span data-ttu-id="1e356-130">동적 그룹 구성원 설정</span><span class="sxs-lookup"><span data-stu-id="1e356-130">Set up dynamic group membership</span></span>

<span data-ttu-id="1e356-131">Azure AD는 Azure AD 그룹의 구성원으로 사용자 계정을 자동으로 추가 하거나 제거 하는 일련의 규칙을 구성할 수 있도록 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-131">Azure AD supports configuring a series of rules that automatically add or remove user accounts as members of an Azure AD group.</span></span> <span data-ttu-id="1e356-132">이를 *동적 그룹 구성원*이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-132">This is known as *dynamic group membership*.</span></span> <span data-ttu-id="1e356-133">이 규칙은 부서나 국가와 같은 사용자 계정 속성을 기반으로 하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-133">The rules are based on user account attributes, such as Department or Country.</span></span>

<span data-ttu-id="1e356-134">규칙이 적용되는 방식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-134">Here's how the rules are applied:</span></span>

- <span data-ttu-id="1e356-135">새 사용자 계정이 그룹에 대한 모든 규칙과 일치하는 경우 구성원이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-135">If a new user account matches all the rules for the group, it becomes a member.</span></span>
- <span data-ttu-id="1e356-136">사용자가 그룹의 구성원이 아니지만 해당 속성이 그룹에 대한 모든 규칙과 일치하도록 변경되는 경우 해당 그룹의 구성원이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-136">If a user account isn't a member of the group, but its attributes change so that it matches all the rules for the group, it becomes a member of that group.</span></span>
- <span data-ttu-id="1e356-137">사용자 계정이 그룹에 대한 일부 규칙과 일치하지 않는 경우 그룹에 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-137">If a user account doesn't match all the rules for the group, it isn't added to the group.</span></span>
- <span data-ttu-id="1e356-138">사용자가 그룹의 구성원이지만 해당 속성이 그룹에 대한 모든 규칙과 더 이상 일치하지 않도록 변경되는 경우 그룹의 구성원에서 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-138">If a user account is a member of the group, but its attributes change so that it no longer matches all the rules for the group, it is removed as a member of the group.</span></span>

<span data-ttu-id="1e356-p108">동적 구성원을 사용하려면 먼저 공통적인 사용자 계정 속성 집합이 있는 그룹 집합 확인해야 합니다. 예를 들어 Sales 부서의 모든 구성원은 “Sales”로 설정된 Department 사용자 계정 특성에 따라 Sales Azure AD 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-p108">To use dynamic membership, you must first determine the sets of groups that have a common set of user account attributes. For example, all members of the Sales department should be in the Sales Azure AD group, based on the user account attribute Department set to "Sales".</span></span>

<span data-ttu-id="1e356-141">[동적 Azure AD 그룹에 대한 규칙을 만들고 구성하는 지침](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1e356-141">See the [instructions to create and configure the rules for a dynamic Azure AD group](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span></span>

## <a name="set-up-automatic-licensing"></a><span data-ttu-id="1e356-142">자동 라이선싱 설정</span><span class="sxs-lookup"><span data-stu-id="1e356-142">Set up automatic licensing</span></span>

<span data-ttu-id="1e356-143">Azure AD에서 보안 그룹을 구성 하 여 구독 집합의 라이선스를 그룹의 모든 구성원에 게 자동으로 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-143">You can configure security groups in Azure AD to automatically assign licenses from a set of subscriptions to all the members of the group.</span></span> <span data-ttu-id="1e356-144">이를 *그룹 기반 라이센싱*이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-144">This is known as *group-based licensing*.</span></span> <span data-ttu-id="1e356-145">사용자 계정이 그룹에 추가되거나 제거된다면 그룹 구독 라이센스는 사용자 계정에서 자동으로 할당되거나 할당 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-145">If a user account is added to or removed from the group, the licenses for the group's subscriptions will be automatically assigned or unassigned from the user account.</span></span>

<span data-ttu-id="1e356-146">Microsoft 365 Enterprise의 경우 적절한 Microsoft 365 Enterprise 라이선스를 할당하도록 Azure AD 보안 그룹을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-146">For Microsoft 365 Enterprise, you'll configure Azure AD security groups to assign the appropriate Microsoft 365 Enterprise license.</span></span>

<span data-ttu-id="1e356-147">모든 그룹 구성원에 대한 충분한 라이센스가 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-147">Make sure you have enough licenses for all the group members.</span></span> <span data-ttu-id="1e356-148">라이선스가 부족할 경우 라이선스를 사용할 수 있게 될 때까지 신규 사용자에게 라이선스가 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-148">If you run out of licenses, new users won't be assigned licenses until licenses become available.</span></span>

>[!Note]
><span data-ttu-id="1e356-149">Azure B2B 계정이 포함된 그룹에 대해 그룹 기반 라이선싱을 구성해서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e356-149">You should not configure group-based licensing for groups that contain Azure business to business (B2B) accounts.</span></span>
>

<span data-ttu-id="1e356-150">자세한 내용은 [AZURE AD의 그룹 기반 라이선싱 기본 사항을](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e356-150">For more information, see [Group-based licensing basics in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal).</span></span>

<span data-ttu-id="1e356-151">[Azure 보안 그룹에 대 한 그룹 기반 라이선스를 구성 하는 지침](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e356-151">See the [instructions to configure group-based licensing for an Azure security group](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal).</span></span>