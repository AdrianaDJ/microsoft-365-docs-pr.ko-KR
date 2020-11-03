---
title: 권장 팀 정책-Microsoft 365 for enterprise | Microsoft Docs
description: 팀 통신과 파일 액세스를 보호 하는 방법에 대 한 Microsoft 권장 사항에 대 한 정책에 대해 설명 합니다.
author: MicrosoftHeidi
manager: serdars
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: heidip
ms.date: 09/30/2020
ms.reviewer: anmorgan
ms.custom:
- it-pro
- goldenconfig
ms.collection:
- M365-identity-device-management
- M365-security-compliance
- m365solution-identitydevice
- m365solution-scenario
ms.openlocfilehash: 56b712c73d63bfcb06d5d35d627facb229668c59
ms.sourcegitcommit: bcb88a6171f9e7bdb5b2d8c03cd628d11c5e7bbf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/14/2020
ms.locfileid: "48464147"
---
# <a name="policy-recommendations-for-securing-teams-chats-groups-and-files"></a><span data-ttu-id="b4d8d-103">팀 대화방, 그룹 및 파일을 보호 하기 위한 정책 권장 사항</span><span class="sxs-lookup"><span data-stu-id="b4d8d-103">Policy recommendations for securing Teams chats, groups, and files</span></span>

<span data-ttu-id="b4d8d-104">이 문서에서는 Microsoft 팀의 채팅, 그룹, 콘텐츠, 파일 및 일정 등을 보호 하기 위해 권장 되는 id 및 장치 액세스 정책을 구현 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-104">This article describes how to implement the recommended identity and device-access policies to protect Microsoft Teams chats, groups, and content such as files and calendars.</span></span> <span data-ttu-id="b4d8d-105">이 지침은 [일반적인 id 및 장치 액세스 정책](identity-access-policies.md)에 따라 구성 되며, 이러한 정책은 팀 관련 추가 정보와 함께 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-105">This guidance builds on the [common identity and device access policies](identity-access-policies.md), with additional information that's Teams-specific.</span></span> <span data-ttu-id="b4d8d-106">팀은 다른 제품과 통합 되므로 [전자 메일을 보호 하기 위한 정책](secure-email-recommended-policies.md)권장 사항 및 [SharePoint 사이트를 보호 하기 위한 정책 권장](sharepoint-file-access-policies.md) 사항도 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-106">Because Teams integrates with our other products, also see [Policy recommendations for securing SharePoint sites and files](sharepoint-file-access-policies.md) and [Policy recommendations for securing email](secure-email-recommended-policies.md).</span></span>

<span data-ttu-id="b4d8d-107">이러한 권장 사항은 초기 계획, 중요 및 높은 규제의 요구 사항에 따라 적용할 수 있는 팀에 대 한 세 가지 보안 및 보호 계층을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-107">These recommendations are based on three different tiers of security and protection for Teams that can be applied based on the granularity of your needs: baseline, sensitive, and highly regulated.</span></span> <span data-ttu-id="b4d8d-108">이러한 보안 계층에 대 한 자세한 내용을 확인 하 고 [id 및 장치 액세스 구성](microsoft-365-policies-configurations.md)에서 이러한 권장 사항을 참조 하는 권장 정책을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-108">You can learn more about these security tiers and the recommended policies referenced by these recommendations in the [Identity and device access configurations](microsoft-365-policies-configurations.md).</span></span>

<span data-ttu-id="b4d8d-109">이 문서에는 조직 외부의 사용자를 비롯 한 특정 인증 환경을 다루는 팀 구축과 관련 된 추가 권장 사항이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-109">Additional recommendations specific to Teams deployment are included in this article to cover specific authentication circumstances, including for users outside your organization.</span></span> <span data-ttu-id="b4d8d-110">이 지침을 따라 전체 보안 환경을 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-110">You will need to follow this guidance for a complete security experience.</span></span>

## <a name="getting-started-with-teams-before-other-dependent-services"></a><span data-ttu-id="b4d8d-111">다른 종속 서비스 이전의 팀 시작</span><span class="sxs-lookup"><span data-stu-id="b4d8d-111">Getting started with Teams before other dependent services</span></span>

<span data-ttu-id="b4d8d-112">Microsoft 팀을 시작 하기 위해 종속 서비스를 사용 하도록 설정할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-112">You don't need to enable dependent services to get started with Microsoft Teams.</span></span> <span data-ttu-id="b4d8d-113">이러한 모든 작업은 "작동" 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-113">These will all "just work."</span></span> <span data-ttu-id="b4d8d-114">그러나 다음을 관리할 준비를 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-114">However, you do need to be prepared to manage the following:</span></span>

- <span data-ttu-id="b4d8d-115">Microsoft 365 그룹</span><span class="sxs-lookup"><span data-stu-id="b4d8d-115">Microsoft 365 groups</span></span>
- <span data-ttu-id="b4d8d-116">SharePoint 팀 사이트</span><span class="sxs-lookup"><span data-stu-id="b4d8d-116">SharePoint team sites</span></span>
- <span data-ttu-id="b4d8d-117">비즈니스용 OneDrive</span><span class="sxs-lookup"><span data-stu-id="b4d8d-117">OneDrive for Business</span></span>
- <span data-ttu-id="b4d8d-118">Exchange 사서함</span><span class="sxs-lookup"><span data-stu-id="b4d8d-118">Exchange mailboxes</span></span>
- <span data-ttu-id="b4d8d-119">Stream 비디오 및 Planner 계획 (이러한 서비스를 사용 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="b4d8d-119">Stream videos and Planner plans (if these services are enabled)</span></span>

## <a name="updating-common-policies-to-include-teams"></a><span data-ttu-id="b4d8d-120">팀을 포함 하도록 일반 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="b4d8d-120">Updating common policies to include Teams</span></span>

<span data-ttu-id="b4d8d-121">다음 다이어그램에서는 팀의 채팅, 그룹 및 콘텐츠를 보호 하기 위해 일반 id 및 장치 액세스 정책에서 업데이트할 정책을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-121">To protect chat, groups and content in Teams, the following diagram illustrates which policies to update from the the common identity and device access policies.</span></span> <span data-ttu-id="b4d8d-122">업데이트할 각 정책에 대해 팀 및 종속 서비스가 클라우드 앱 할당에 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-122">For each policy to update, make sure that Teams and dependent services are included in the assignment of cloud apps.</span></span>

<span data-ttu-id="b4d8d-123">[![팀 및 해당 종속 서비스에 대 한 액세스를 보호 하기 위한 정책 업데이트 요약](../../media/microsoft-365-policies-configurations/identity-access-ruleset-teams.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-teams.png)</span><span class="sxs-lookup"><span data-stu-id="b4d8d-123">[![Summary of policy updates for protecting access to Teams and its dependent services](../../media/microsoft-365-policies-configurations/identity-access-ruleset-teams.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-teams.png)</span></span>

[<span data-ttu-id="b4d8d-124">이 이미지의 더 큰 버전 보기</span><span class="sxs-lookup"><span data-stu-id="b4d8d-124">See a larger version of this image</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-teams.png)

<span data-ttu-id="b4d8d-125">다음은 팀에 대 한 클라우드 앱 할당에 포함할 종속 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-125">These are the dependent services to include in the assignment of cloud apps for Teams:</span></span>

- <span data-ttu-id="b4d8d-126">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b4d8d-126">Microsoft Teams</span></span>
- <span data-ttu-id="b4d8d-127">SharePoint 및 비즈니스용 OneDrive</span><span class="sxs-lookup"><span data-stu-id="b4d8d-127">SharePoint and OneDrive for Business</span></span>
- <span data-ttu-id="b4d8d-128">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b4d8d-128">Exchange Online</span></span>
- <span data-ttu-id="b4d8d-129">비즈니스용 Skype Online</span><span class="sxs-lookup"><span data-stu-id="b4d8d-129">Skype for Business Online</span></span>
- <span data-ttu-id="b4d8d-130">Microsoft Stream (모임 녹음/녹화)</span><span class="sxs-lookup"><span data-stu-id="b4d8d-130">Microsoft Stream (meeting recordings)</span></span>
- <span data-ttu-id="b4d8d-131">Microsoft Planner (Planner 작업 및 계획 데이터)</span><span class="sxs-lookup"><span data-stu-id="b4d8d-131">Microsoft Planner (Planner tasks and plan data)</span></span>

<span data-ttu-id="b4d8d-132">이 표에는 모든 Office 응용 프로그램에 대해 설정 된 보다 광범위 한 정책을 가진 [일반 id 및 장치 액세스 정책](identity-access-policies.md)에서 다시 검토 하 고 각 정책에 연결 해야 하는 정책이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-132">This table lists the policies that need to be revisited and links to each policy in the [common identity and device access policies](identity-access-policies.md), which has the wider policy set for all Office applications.</span></span>

|<span data-ttu-id="b4d8d-133">보호 수준</span><span class="sxs-lookup"><span data-stu-id="b4d8d-133">Protection level</span></span>|<span data-ttu-id="b4d8d-134">정책</span><span class="sxs-lookup"><span data-stu-id="b4d8d-134">Policies</span></span>|<span data-ttu-id="b4d8d-135">팀 구현에 대 한 추가 정보</span><span class="sxs-lookup"><span data-stu-id="b4d8d-135">Further information for Teams implementation</span></span>|
|:---------------|:-------|:----------------|
|<span data-ttu-id="b4d8d-136">**기준**</span><span class="sxs-lookup"><span data-stu-id="b4d8d-136">**Baseline**</span></span>|[<span data-ttu-id="b4d8d-137">로그인 위험이 *보통* 또는 *높을* 때 MFA 필요</span><span class="sxs-lookup"><span data-stu-id="b4d8d-137">Require MFA when sign-in risk is *medium* or *high*</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="b4d8d-138">팀 및 종속 서비스가 앱 목록에 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-138">Be sure Teams and dependent services are included in the list of apps.</span></span> <span data-ttu-id="b4d8d-139">팀에서 게스트 액세스 및 외부 액세스 규칙을 고려해 야 하는 경우이 문서의 뒷부분에 나오는 이러한 항목에 대해 자세히 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-139">Teams has Guest Access and External Access rules to consider as well, you'll learn more about these later in this article.</span></span>|
|        |[<span data-ttu-id="b4d8d-140">최신 인증을 지원하지 않는 클라이언트 차단</span><span class="sxs-lookup"><span data-stu-id="b4d8d-140">Block clients that don't support modern authentication</span></span>](identity-access-policies.md#block-clients-that-dont-support-modern-authentication)|<span data-ttu-id="b4d8d-141">클라우드 앱 할당에 팀 및 종속 서비스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-141">Include Teams and dependent services in the assignment of cloud apps.</span></span>|
|        |[<span data-ttu-id="b4d8d-142">위험이 높은 사용자는 암호를 변경해야 함</span><span class="sxs-lookup"><span data-stu-id="b4d8d-142">High risk users must change password</span></span>](identity-access-policies.md#high-risk-users-must-change-password)|<span data-ttu-id="b4d8d-143">계정에 대해 높은 위험 활동이 검색 되는 경우 팀 사용자가 로그인 할 때 암호를 변경 하도록 강제 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-143">Forces Teams users to change their password when signing in if high-risk activity is detected for their account.</span></span> <span data-ttu-id="b4d8d-144">팀 및 종속 서비스가 앱 목록에 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-144">Be sure Teams and dependent services are included in the list of apps.</span></span>|
|        |[<span data-ttu-id="b4d8d-145">앱 데이터 보호 정책 적용</span><span class="sxs-lookup"><span data-stu-id="b4d8d-145">Apply APP data protection policies</span></span>](identity-access-policies.md#apply-app-data-protection-policies)|<span data-ttu-id="b4d8d-146">팀 및 종속 서비스가 앱 목록에 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-146">Be sure Teams and dependent services are included in the list of apps.</span></span> <span data-ttu-id="b4d8d-147">각 플랫폼 (iOS, Android, Windows)에 대 한 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-147">Update the policy for each platform (iOS, Android, Windows).</span></span>|
|        |[<span data-ttu-id="b4d8d-148">장치 준수 정책 정의</span><span class="sxs-lookup"><span data-stu-id="b4d8d-148">Define device compliance policies</span></span>](identity-access-policies.md#define-device-compliance-policies)|<span data-ttu-id="b4d8d-149">이 정책에 팀 및 종속 서비스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-149">Include Teams and dependent services in this policy.</span></span>|
|        |[<span data-ttu-id="b4d8d-150">호환 PC 필요</span><span class="sxs-lookup"><span data-stu-id="b4d8d-150">Require compliant PCs</span></span>](identity-access-policies.md#require-compliant-pcs-but-not-compliant-phones-and-tablets)|<span data-ttu-id="b4d8d-151">이 정책에 팀 및 종속 서비스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-151">Include Teams and dependent services in this policy.</span></span>|
|<span data-ttu-id="b4d8d-152">**중요**</span><span class="sxs-lookup"><span data-stu-id="b4d8d-152">**Sensitive**</span></span>|[<span data-ttu-id="b4d8d-153">로그인 위험이 *낮은* *경우 MFA* 필요 *high*</span><span class="sxs-lookup"><span data-stu-id="b4d8d-153">Require MFA when sign-in risk is *low*, *medium* or *high*</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="b4d8d-154">팀에서 게스트 액세스 및 외부 액세스 규칙을 고려해 야 하는 경우이 문서의 뒷부분에 나오는 이러한 항목에 대해 자세히 알아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-154">Teams has Guest Access and External Access rules to consider as well, you'll learn more about these later in this article.</span></span> <span data-ttu-id="b4d8d-155">이 정책에 팀 및 종속 서비스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-155">Include Teams and dependent services in this policy.</span></span>|
|         |[<span data-ttu-id="b4d8d-156">준수 Pc *및* 모바일 장치 요구</span><span class="sxs-lookup"><span data-stu-id="b4d8d-156">Require compliant PCs *and* mobile devices</span></span>](identity-access-policies.md#require-compliant-pcs-and-mobile-devices)|<span data-ttu-id="b4d8d-157">이 정책에 팀 및 종속 서비스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-157">Include Teams and dependent services in this policy.</span></span>|
|<span data-ttu-id="b4d8d-158">**매우 엄격한 규제**</span><span class="sxs-lookup"><span data-stu-id="b4d8d-158">**Highly regulated**</span></span>|[<span data-ttu-id="b4d8d-159">*항상* MFA 필요</span><span class="sxs-lookup"><span data-stu-id="b4d8d-159">*Always* require MFA</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="b4d8d-160">사용자 id와 상관 없이 MFA는 조직에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-160">Regardless of user identity, MFA will be used by your organization.</span></span> <span data-ttu-id="b4d8d-161">이 정책에 팀 및 종속 서비스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-161">Include Teams and dependent services in this policy.</span></span> |
| | |

## <a name="teams-dependent-services-architecture"></a><span data-ttu-id="b4d8d-162">팀 종속 서비스 아키텍처</span><span class="sxs-lookup"><span data-stu-id="b4d8d-162">Teams dependent services architecture</span></span>

<span data-ttu-id="b4d8d-163">참조용으로 다음 다이어그램에는 서비스 팀이 의존 하는 것이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-163">For reference, the following diagram illustrates the services Teams relies on.</span></span> <span data-ttu-id="b4d8d-164">자세한 내용 및 추가 그림은 [IT 설계자 용 microsoft 365의 Microsoft 팀 및 관련 생산성 서비스](../../solutions/productivity-illustrations.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-164">For more information and additional illustrations, see [Microsoft Teams and related productivity services in Microsoft 365 for IT architects](../../solutions/productivity-illustrations.md).</span></span>

<span data-ttu-id="b4d8d-165">[![SharePoint, 비즈니스용 OneDrive 및 Exchange의 팀 종속성을 보여 주는 다이어그램](../../media/microsoft-365-policies-configurations/identity-access-logical-architecture-teams.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-logical-architecture-teams.png)</span><span class="sxs-lookup"><span data-stu-id="b4d8d-165">[![Diagram showing Teams dependencies on SharePoint, OneDrive for Business, and Exchange](../../media/microsoft-365-policies-configurations/identity-access-logical-architecture-teams.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-logical-architecture-teams.png)</span></span>

[<span data-ttu-id="b4d8d-166">이 이미지의 더 큰 버전 보기</span><span class="sxs-lookup"><span data-stu-id="b4d8d-166">See a larger version of this image</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-logical-architecture-teams.png)

## <a name="guest-and-external-access-for-teams"></a><span data-ttu-id="b4d8d-167">게스트 및 팀에 대 한 외부 액세스</span><span class="sxs-lookup"><span data-stu-id="b4d8d-167">Guest and external access for Teams</span></span>

<span data-ttu-id="b4d8d-168">Microsoft 팀에서는 다음을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-168">Microsoft Teams defines the following:</span></span>

- <span data-ttu-id="b4d8d-169">**게스트 액세스** 에서는 팀 구성원으로 추가할 수 있는 게스트 또는 외부 사용자에 대해 AZURE AD B2B 계정을 사용 하며,이 경우 팀의 통신 및 리소스에 대 한 모든 고유한 액세스 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-169">**Guest access** uses an Azure AD B2B account for a guest or external user that can be added as a member of a team and have all permissioned access to the communication and resources of the team.</span></span>

- <span data-ttu-id="b4d8d-170">**외부 액세스** 는 AZURE AD B2B 계정이 없는 외부 사용자를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-170">**External access** is for an external user that does not have an Azure AD B2B account.</span></span> <span data-ttu-id="b4d8d-171">외부 액세스에는 초대 및 참여를 포함할 수 있지만 팀 구성원 자격 및 팀의 리소스에 대 한 액세스는 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-171">External access can include invitations and participation in calls, chats, and meetings, but does not include team membership and access to the resources of the team.</span></span>

<span data-ttu-id="b4d8d-172">조건부 액세스 정책은 해당 Azure AD B2B 계정이 있기 때문에 팀의 게스트 액세스에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-172">Conditional Access policies only apply to guest access in Teams because there is a corresponding Azure AD B2B account.</span></span>

<!--
In Azure AD, guest and external users are the same. The user type for both of these is Guest. Guest users are B2B users. Microsoft Teams differentiates between guest users and external users in the app. While it's important to understand how each of these are treated in Teams, both types of users are B2B users in Azure AD and the recommended policies for B2B users apply to both. 

--> 

<span data-ttu-id="b4d8d-173">게스트 및 Azure AD B2B 계정을 사용 하는 외부 사용자에 대 한 액세스를 허용 하는 권장 정책에 대해서는 [게스트 및 외부 B2B 계정 액세스를 허용 하기 위한 정책을](identity-access-policies-guest-access.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-173">For recommended policies to allow access for guest and external users with an Azure AD B2B account, see [Policies for allowing guest and external B2B account access](identity-access-policies-guest-access.md).</span></span>

### <a name="guest-access-in-teams"></a><span data-ttu-id="b4d8d-174">Teams의 게스트 액세스</span><span class="sxs-lookup"><span data-stu-id="b4d8d-174">Guest access in Teams</span></span>

<span data-ttu-id="b4d8d-175">비즈니스 또는 조직 내부에 있는 사용자에 대 한 정책 외에도 관리자는 게스트 액세스를 허용 하 고 사용자가 비즈니스 또는 조직 외부에 있는 사용자가 팀 리소스에 액세스 하 고 그룹 대화, 채팅 및 모임 등의 내부 사람들과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-175">In addition to the policies for users who are internal to your business or organization, administrators may enable guest access to allow, on a user-by-user basis, people who are external to your business or organization to access Teams resources and interact with internal people for things like group conversations, chat, and meetings.</span></span> 

<span data-ttu-id="b4d8d-176">게스트 액세스에 대 한 자세한 내용과 구현 방법에 대 한 자세한 내용은  [팀 게스트 액세스](https://docs.microsoft.com/microsoftteams/guest-access)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-176">For more information about guest access and how to implement it, see  [Teams guest access](https://docs.microsoft.com/microsoftteams/guest-access).</span></span>

### <a name="external-access-in-teams"></a><span data-ttu-id="b4d8d-177">팀의 외부 액세스</span><span class="sxs-lookup"><span data-stu-id="b4d8d-177">External access in Teams</span></span>

<span data-ttu-id="b4d8d-178">외부 액세스는 게스트 액세스와 혼동 하는 경우가 많지만, 이러한 두 가지 비 내부 액세스 메커니즘이 실제로 서로 다른 지는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-178">External access is sometimes confused with guest access, so it's important to be clear that these two non-internal access mechanisms are actually quite different.</span></span> 

<span data-ttu-id="b4d8d-179">외부 액세스는 팀의 사용자와 함께 회의를 찾고, 통화 하 고, 채팅 하 고, 사용자와 모임을 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-179">External access is a way for Teams users from an entire external domain to find, call, chat, and set up meetings with your users in Teams.</span></span> <span data-ttu-id="b4d8d-180">팀 관리자는 조직 수준에서 외부 액세스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-180">Teams administrators configure external access at the organization level.</span></span> <span data-ttu-id="b4d8d-181">자세한 내용은 [Microsoft 팀에서 외부 액세스 관리](https://docs.microsoft.com/microsoftteams/manage-external-access)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-181">For more information, see [Manage external access in Microsoft Teams](https://docs.microsoft.com/microsoftteams/manage-external-access).</span></span>

<span data-ttu-id="b4d8d-182">외부 액세스 사용자는 게스트 액세스를 통해 추가 된 개인 보다 더 적은 액세스 및 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-182">External access users have less access and functionality than an individual who's been added via guest access.</span></span> <span data-ttu-id="b4d8d-183">예를 들어 외부 액세스 사용자는 팀과의 내부 사용자와 채팅을 할 수 있지만 팀 채널, 파일 또는 기타 리소스에는 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-183">For example, external access users can chat with your internal users with Teams but cannot access team channels, files, or other resources.</span></span>

<span data-ttu-id="b4d8d-184">외부 액세스는 Azure AD B2B 사용자 계정을 사용 하지 않으므로 조건부 액세스 정책을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-184">External access does not use Azure AD B2B user accounts and therefore does not use Conditional Access policies.</span></span> 

## <a name="teams-policies"></a><span data-ttu-id="b4d8d-185">팀 정책</span><span class="sxs-lookup"><span data-stu-id="b4d8d-185">Teams policies</span></span>

<span data-ttu-id="b4d8d-186">위에 나열 된 일반적인 정책 외에도 다양 한 팀 기능을 관리 하기 위해 구성 해야 하는 팀 관련 정책이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-186">Outside of the common policies listed above, there are Teams-specific policies that can and should be configured to manage various Teams functionalities.</span></span>

### <a name="teams-and-channels-policies"></a><span data-ttu-id="b4d8d-187">팀 및 채널 정책</span><span class="sxs-lookup"><span data-stu-id="b4d8d-187">Teams and channels policies</span></span>

<span data-ttu-id="b4d8d-188">팀과 채널은 Microsoft 팀에서 일반적으로 사용 되는 두 가지 요소 이며, 팀 및 채널을 사용할 때 사용자가 수행할 수 있는 작업을 제어 하기 위해 배치할 수 있는 정책이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-188">Teams and channels are two commonly used elements in Microsoft Teams, and there are policies you can put in place to control what users can and cannot do when using teams and channels.</span></span> <span data-ttu-id="b4d8d-189">전역 팀을 만들 수 있지만 조직에 사용자가 5000 명 이하인 경우 조직의 요구 사항에 맞게 특정 목적으로 더 작은 팀과 채널을 사용 하는 것이 도움이 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-189">While you can create a global team, if your organization has 5000 users or less, you are likely to find it helpful to have smaller teams and channels for specific purposes, in-line with your organizational needs.</span></span>

<span data-ttu-id="b4d8d-190">기본 정책을 변경 하거나 사용자 지정 정책을 만드는 것이 권장 되며,이 링크에서 정책 관리에 대 한 자세한 내용을 보려면 [Microsoft 팀에서 팀 정책 관리](https://docs.microsoft.com/microsoftteams/teams-policies)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-190">Changing the default policy or creating custom policies would be recommended, and you can learn more about managing your policies at this link: [Manage teams policies in Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-policies).</span></span>

### <a name="messaging-policies"></a><span data-ttu-id="b4d8d-191">메시징 정책</span><span class="sxs-lookup"><span data-stu-id="b4d8d-191">Messaging policies</span></span>

<span data-ttu-id="b4d8d-192">메시징 또는 채팅은 기본 글로벌 정책 또는 사용자 지정 정책을 통해 관리할 수도 있으며,이를 통해 사용자가 조직에 적합 한 방식으로 서로 통신 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-192">Messaging, or chat, can also be managed through the default global policy, or through custom policies, and this can help your users communicate with one another in a way that's appropriate for your organization.</span></span> <span data-ttu-id="b4d8d-193">이 정보는 [팀의 메시징 정책 관리](https://docs.microsoft.com/microsoftteams/messaging-policies-in-teams)에서 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-193">This information can be reviewed at [Managing messaging policies in Teams](https://docs.microsoft.com/microsoftteams/messaging-policies-in-teams).</span></span>

### <a name="meeting-policies"></a><span data-ttu-id="b4d8d-194">모임 정책</span><span class="sxs-lookup"><span data-stu-id="b4d8d-194">Meeting policies</span></span>

<span data-ttu-id="b4d8d-195">팀 회의에 대 한 정책을 계획 및 구현 하지 않으면 팀에 대 한 토론이 완료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-195">No discussion of Teams would be complete without planning and implementing policies around Teams meetings.</span></span> <span data-ttu-id="b4d8d-196">회의는 팀의 필수 구성 요소 이며, 사용자가 동시에 여러 사용자에 게 공식적으로 회의를 하 고 소개 하 고 모임에 관련 된 콘텐츠를 공유할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-196">Meetings are an essential component of Teams, allowing people to formally meet and present to many users at once, as well as share content relevant to the meeting.</span></span> <span data-ttu-id="b4d8d-197">조직에서 모임에 적합 한 정책을 설정 하는 것은 필수 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-197">Setting the right policies for your organization around meetings is essential.</span></span>

<span data-ttu-id="b4d8d-198">자세한 내용은 [팀에서 모임 정책 관리](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams) 를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-198">Please review [Manage meeting policies in Teams](https://docs.microsoft.com/microsoftteams/meeting-policies-in-teams) for more information.</span></span>

### <a name="app-permission-policies"></a><span data-ttu-id="b4d8d-199">앱 권한 정책</span><span class="sxs-lookup"><span data-stu-id="b4d8d-199">App permission policies</span></span>

<span data-ttu-id="b4d8d-200">또한 팀에서는 채널 또는 개인 채팅 등의 다양 한 위치에서 앱을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-200">Teams also allows you to use apps in various places, such as channels or personal chats.</span></span> <span data-ttu-id="b4d8d-201">어떤 앱을 추가 하 고 사용할 수 있는지에 대 한 정책이 있고, 여기서는 보안이 향상 된 콘텐츠 환경을 유지 관리 하는 데 필수적입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-201">Having policies around what apps can be added and used, and where, is essential to maintaining a content-rich environment that is also secure.</span></span>

<span data-ttu-id="b4d8d-202">앱 사용 권한 정책에 대 한 자세한 내용은 [Microsoft 팀에서 앱 사용 권한 정책 관리](https://docs.microsoft.com/microsoftteams/teams-app-permission-policies)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4d8d-202">For more reading about App Permission Policies, check out [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-permission-policies).</span></span>

## <a name="next-steps"></a><span data-ttu-id="b4d8d-203">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b4d8d-203">Next steps</span></span>

![4 단계: Microsoft 365 클라우드 앱에 대 한 정책](../../media/microsoft-365-policies-configurations/identity-device-access-steps-next-step-4.png)

<span data-ttu-id="b4d8d-205">다음에 대 한 조건부 액세스 정책 구성:</span><span class="sxs-lookup"><span data-stu-id="b4d8d-205">Configure Conditional Access policies for:</span></span>

- [<span data-ttu-id="b4d8d-206">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b4d8d-206">Exchange Online</span></span>](secure-email-recommended-policies.md)
- [<span data-ttu-id="b4d8d-207">SharePoint</span><span class="sxs-lookup"><span data-stu-id="b4d8d-207">SharePoint</span></span>](sharepoint-file-access-policies.md)
