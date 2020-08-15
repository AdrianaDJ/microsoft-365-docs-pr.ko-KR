---
title: Microsoft 365 그룹, 팀 및 SharePoint 간의 설정 상호 작용
ms.reviewer: ''
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-collaboration
ms.custom:
- M365solutions
f1.keywords: NOCSH
description: Microsoft 365 그룹, 팀 및 SharePoint 간의 설정 상호 작용에 대해 자세히 알아보기
ms.openlocfilehash: 3ad5011c2d7b4579e054b014237d5771049b3c91
ms.sourcegitcommit: 66f1f430b3dcae5f46cb362a32d6fb7da4cff5c1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "46662763"
---
# <a name="settings-interactions-between-microsoft-365-groups-teams-and-sharepoint"></a><span data-ttu-id="32519-103">Microsoft 365 그룹, 팀 및 SharePoint 간의 설정 상호 작용</span><span class="sxs-lookup"><span data-stu-id="32519-103">Settings interactions between Microsoft 365 Groups, Teams and SharePoint</span></span>

<span data-ttu-id="32519-104">Microsoft 365의 microsoft 365 그룹, Microsoft 팀 및 SharePoint에 대 한 일부 설정 (특히 공유 및 그룹/팀 및 SharePoint 사이트 작성과 관련)이 서로 겹칩니다.</span><span class="sxs-lookup"><span data-stu-id="32519-104">Some settings for Microsoft 365 Groups, Microsoft Teams, and SharePoint in Microsoft 365, particularly related to sharing and group/team and SharePoint site creation, overlap with each other.</span></span> <span data-ttu-id="32519-105">이 문서에서는 이러한 상호 작용 및 이러한 설정을 사용 하는 방법에 대 한 모범 사례에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-105">This article provides descriptions of these interactions and best practices for how to work with these settings.</span></span>

![SharePoint, 팀 및 그룹 기능의 벤 다이어그램](../media/teams-groups-sharepoint-venn.png)

## <a name="the-effects-of-sharepoint-settings-on-groups-and-teams"></a><span data-ttu-id="32519-107">그룹 및 팀에 대 한 SharePoint 설정의 영향</span><span class="sxs-lookup"><span data-stu-id="32519-107">The effects of SharePoint settings on groups and teams</span></span>

|<span data-ttu-id="32519-108">SharePoint 설정</span><span class="sxs-lookup"><span data-stu-id="32519-108">SharePoint setting</span></span>|<span data-ttu-id="32519-109">설명</span><span class="sxs-lookup"><span data-stu-id="32519-109">Description</span></span>|<span data-ttu-id="32519-110">Microsoft 365 그룹 및 팀에 대 한 영향</span><span class="sxs-lookup"><span data-stu-id="32519-110">Effect on Microsoft 365 groups and Teams</span></span>|<span data-ttu-id="32519-111">권장 사항</span><span class="sxs-lookup"><span data-stu-id="32519-111">Recommendation</span></span>|
|:-----------------|:----------|:---------------------------------------|:-------------|
|<span data-ttu-id="32519-112">조직 및 사이트에 대 한 외부 공유</span><span class="sxs-lookup"><span data-stu-id="32519-112">External sharing for organization and site</span></span>|<span data-ttu-id="32519-113">사이트, 파일 및 폴더를 조직 외부의 사용자와 공유할 수 있는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-113">Determines if sites, files, and folders can be shared with people outside the organization.</span></span>|<span data-ttu-id="32519-114">SharePoint, 그룹 및 팀 설정이 일치 하지 않는 경우 팀의 게스트가 사이트 액세스를 차단 하거나 예기치 않은 외부 액세스가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32519-114">If SharePoint, groups, and Teams settings don't match, guests in the team may be blocked from accessing the site, or unexpected external access may occur.</span></span>|<span data-ttu-id="32519-115">공유 설정을 변경 하는 경우 그룹에 연결 된 팀 사이트의 그룹 설정, 팀 설정 및 SharePoint 사이트 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-115">When changing sharing settings, check Groups settings, Teams settings, and SharePoint site settings for group-connected team sites.</span></span><br><br> <span data-ttu-id="32519-116">[팀에서 게스트와 공동 작업](https://docs.microsoft.com/microsoft-365/solutions/collaborate-as-team) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="32519-116">See [Collaborate with guests in a team](https://docs.microsoft.com/microsoft-365/solutions/collaborate-as-team)</span></span>|
|<span data-ttu-id="32519-117">도메인 허용/차단</span><span class="sxs-lookup"><span data-stu-id="32519-117">Domain allow/block</span></span>|<span data-ttu-id="32519-118">지정 된 도메인과 콘텐츠를 공유 하도록 허용 하거나 금지 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-118">Allows or prevents content being shared with specified domains.</span></span>|<span data-ttu-id="32519-119">그룹 및 팀은 SharePoint 허용 또는 차단 목록을 인식 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32519-119">Groups and Teams do not recognize SharePoint allow or block lists.</span></span> <span data-ttu-id="32519-120">SharePoint에서 허용 되지 않는 도메인의 사용자는 SharePoint 사이트 또는 팀을 통해 콘텐츠에 액세스 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32519-120">Users from domains disallowed in SharePoint could gain access to SharePoint sites or content through a team.</span></span>|<span data-ttu-id="32519-121">Azure AD 및 SharePoint에 대해 도메인 허용/차단 목록을 함께 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-121">Manage domain allow/block lists for Azure AD and SharePoint together.</span></span> <span data-ttu-id="32519-122">도메인 허용 및 차단에 대 한 조직 전체의 거 버 넌 스 프로세스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32519-122">Create an org-wide governance process for allowing and blocking domains.</span></span><br><br><span data-ttu-id="32519-123">[SharePoint 도메인 설정](https://docs.microsoft.com/sharepoint/restricted-domains-sharing) 및 [Azure AD 도메인 설정](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list) 참조</span><span class="sxs-lookup"><span data-stu-id="32519-123">See [SharePoint domain settings](https://docs.microsoft.com/sharepoint/restricted-domains-sharing) and [Azure AD domain settings](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list)</span></span>|
|<span data-ttu-id="32519-124">특정 보안 그룹의 사용자만 외부에서 공유할 수 있도록 허용</span><span class="sxs-lookup"><span data-stu-id="32519-124">Allow only users in specific security groups to share externally</span></span>|<span data-ttu-id="32519-125">외부에서 SharePoint 사이트, 폴더 및 파일을 공유할 수 있는 보안 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-125">Specifies security groups who can share SharePoint sites, folders, and files externally.</span></span>|<span data-ttu-id="32519-126">이 설정은 팀 소유자가 외부에서 팀을 공유 하는 것을 막지는 못합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-126">This setting does not prevent team owners from sharing teams externally.</span></span> <span data-ttu-id="32519-127">팀 게스트에는 연결 된 SharePoint 사이트에 대 한 액세스 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32519-127">Team guests have access to the associated SharePoint site.</span></span>||
|<span data-ttu-id="32519-128">SharePoint 사이트 공유 설정</span><span class="sxs-lookup"><span data-stu-id="32519-128">SharePoint site sharing settings</span></span>|<span data-ttu-id="32519-129">팀 구성원 외부에서 직접 사이트를 공유할 수 있는 사용자를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-129">Determines who can share the site directly outside of team membership.</span></span> <span data-ttu-id="32519-130">이는 팀 또는 사이트 소유자가 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-130">This is configured by the team or site owner.</span></span>|<span data-ttu-id="32519-131">이 설정은 팀에 직접 영향을 주지 않지만 사용자를 사이트에 추가 하 고 팀 자체 또는 기타 팀 리소스에 대 한 액세스 권한이 없는 경우에도 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-131">This setting does not affect the team directly, but it can allow users to be added to a site and not have access to the team itself or other Teams resources</span></span>|<span data-ttu-id="32519-132">이 설정을 사용 하 여 사이트 공유를 직접 제한 하 고 팀을 통해 사이트 액세스를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32519-132">Consider using this setting to limit sharing of the site directly and manage site access through the team.</span></span>|
|<span data-ttu-id="32519-133">사용자가 SharePoint 시작 페이지 및 OneDrive에서 사이트를 만들 수 있도록 허용</span><span class="sxs-lookup"><span data-stu-id="32519-133">Let users create sites from the SharePoint start page and OneDrive</span></span>|<span data-ttu-id="32519-134">사용자가 새 SharePoint 사이트를 만들 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-134">Specifies if users can create new SharePoint sites.</span></span>|<span data-ttu-id="32519-135">이 설정이 해제 된 경우에도 사용자는 팀을 만들어 그룹 연결 팀 사이트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32519-135">If this setting is turned off, users can still create group-connected team sites by creating a team.</span></span>||

## <a name="the-effects-of-groups-settings-on-teams"></a><span data-ttu-id="32519-136">팀에 대 한 그룹 설정의 영향</span><span class="sxs-lookup"><span data-stu-id="32519-136">The effects of groups settings on teams</span></span>

|<span data-ttu-id="32519-137">Microsoft 365 groups 설정</span><span class="sxs-lookup"><span data-stu-id="32519-137">Microsoft 365 groups setting</span></span>|<span data-ttu-id="32519-138">설명</span><span class="sxs-lookup"><span data-stu-id="32519-138">Description</span></span>|<span data-ttu-id="32519-139">팀에 대 한 영향</span><span class="sxs-lookup"><span data-stu-id="32519-139">Effect on Teams</span></span>|<span data-ttu-id="32519-140">권장 사항</span><span class="sxs-lookup"><span data-stu-id="32519-140">Recommendation</span></span>|
|:---------------------------|:----------|:--------------|:-------------|
|<span data-ttu-id="32519-141">이름 지정 정책</span><span class="sxs-lookup"><span data-stu-id="32519-141">Naming policies</span></span>|<span data-ttu-id="32519-142">그룹 만들기에 대 한 그룹 이름 접두사 및 접미사 및 차단 된 단어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-142">Specifies group name prefixes and suffixes, and blocked words for group creation</span></span>|<span data-ttu-id="32519-143">팀을 만드는 사용자에 게 정책이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32519-143">Policies are enforced for users creating teams.</span></span>||
|<span data-ttu-id="32519-144">그룹 게스트 액세스</span><span class="sxs-lookup"><span data-stu-id="32519-144">Group guest access</span></span>|<span data-ttu-id="32519-145">조직 외부의 사용자를 그룹에 추가할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-145">Specifies if people outside the organization can be added to groups.</span></span>|<span data-ttu-id="32519-146">그룹 또는 팀 게스트 공유 설정이 해제 된 경우 팀을 guests와 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="32519-146">If either the groups or Teams guest sharing settings are off, the team cannot be shared with guests.</span></span>|<span data-ttu-id="32519-147">게스트 공유 설정을 변경할 때는 팀과 연결 된 팀, 그룹 및 SharePoint 사이트에 대 한 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-147">When changing guest sharing settings, check the settings for Teams, Groups, and the SharePoint site associated with the team.</span></span><br><br> <span data-ttu-id="32519-148">[팀에서 게스트와 공동 작업](https://docs.microsoft.com/microsoft-365/solutions/collaborate-as-team) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="32519-148">See [Collaborate with guests in a team](https://docs.microsoft.com/microsoft-365/solutions/collaborate-as-team)</span></span>|
|<span data-ttu-id="32519-149">보안 그룹별 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="32519-149">Group creation by security group</span></span>|<span data-ttu-id="32519-150">그룹은 특정 보안 그룹의 구성원만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32519-150">Groups can only be created by members of a specific security group.</span></span>|<span data-ttu-id="32519-151">보안 그룹의 구성원이 아닌 사용자는 팀을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="32519-151">Users who are not members of the security group will not be able to create a team.</span></span>|<span data-ttu-id="32519-152">그룹을 요청 하는 프로세스에 팀 또는 SharePoint 사이트 요청에 대 한 지침이 포함 되어 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="32519-152">Be sure your process for requesting a group includes instructions for requesting a team or a SharePoint site.</span></span>|
|<span data-ttu-id="32519-153">그룹 만료 정책</span><span class="sxs-lookup"><span data-stu-id="32519-153">Group expiration policy</span></span>|<span data-ttu-id="32519-154">현재 사용 하지 않는 그룹이 자동으로 삭제 되는 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-154">Specifies a time period after which groups that are not actively used will be automatically deleted.</span></span>|<span data-ttu-id="32519-155">그룹을 삭제 하면 팀 및 연결 된 SharePoint 사이트도 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32519-155">When the group is deleted, the team and associated SharePoint site are also deleted.</span></span> <span data-ttu-id="32519-156">보존 정책에 의해 보호 되는 콘텐츠는 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32519-156">Content protected by retention policies is retained.</span></span>|<span data-ttu-id="32519-157">만료 정책을 사용 하 여 사용 되지 않는 팀, 그룹 및 사이트의 sprawl를 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="32519-157">Use expiration policies to avoid sprawl of unused teams, groups and sites.</span></span>|

## <a name="related-topics"></a><span data-ttu-id="32519-158">관련 항목</span><span class="sxs-lookup"><span data-stu-id="32519-158">Related topics</span></span>

[<span data-ttu-id="32519-159">조직 외부의 사용자와 공동 작업</span><span class="sxs-lookup"><span data-stu-id="32519-159">Collaborating with people outside your organization</span></span>](https://docs.microsoft.com/microsoft-365/solutions/collaborate-with-people-outside-your-organization)

[<span data-ttu-id="32519-160">SharePoint에서 사이트 만들기 관리</span><span class="sxs-lookup"><span data-stu-id="32519-160">Manage site creation in SharePoint</span></span>](https://docs.microsoft.com/sharepoint/manage-site-creation)