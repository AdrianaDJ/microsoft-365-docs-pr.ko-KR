---
title: Microsoft 365 클라이언트 앱 지원-Single Sign-on
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: Normal
ms.collection:
- Strat_O365_Enterprise
- M365-subscription-management
search.appverid:
- MET150
f1.keywords:
- NOCSH
description: 이 문서에서는 Microsoft 365에 대 한 single sign-on을 지 원하는 플랫폼, 클라이언트 및 Powershell 모듈에 대해 설명 합니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: c0171e277d6072515e7fe0ca8ede8b8005ad8fe2
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692498"
---
# <a name="microsoft-365-client-app-support--single-sign-on"></a><span data-ttu-id="5c29a-103">Microsoft 365 클라이언트 앱 지원-Single Sign-on</span><span class="sxs-lookup"><span data-stu-id="5c29a-103">Microsoft 365 Client App Support — Single Sign-On</span></span>

<span data-ttu-id="5c29a-104">*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*</span><span class="sxs-lookup"><span data-stu-id="5c29a-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="5c29a-105">SSO (Single sign-on)는 사용자가 Azure Active Directory (Azure AD)의 응용 프로그램에 로그온 할 때 보안 및 편의성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c29a-105">Single sign-on (SSO) adds security and convenience when your users sign on to applications in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="5c29a-106">Single sign-on을 사용 하는 경우 사용자는 도메인에 가입 된 장치, 회사 리소스, SaaS (software as a service) 응용 프로그램 및 웹 응용 프로그램에 액세스 하기 위해 한 계정으로 한 번씩 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c29a-106">With single sign-on, users sign in once with one account to access domain-joined devices, company resources, software as a service (SaaS) applications, and web applications.</span></span>

<span data-ttu-id="5c29a-107">자세한 내용은 [single sign-on](https://docs.microsoft.com/azure/active-directory/manage-apps/what-is-single-sign-on)을 참고 하세요.</span><span class="sxs-lookup"><span data-stu-id="5c29a-107">Learn more about [single sign-on](https://docs.microsoft.com/azure/active-directory/manage-apps/what-is-single-sign-on).</span></span>

## <a name="supported-platforms"></a><span data-ttu-id="5c29a-108">지원되는 플랫폼</span><span class="sxs-lookup"><span data-stu-id="5c29a-108">Supported platforms</span></span>

 - <span data-ttu-id="5c29a-109">Windows 10 데스크톱<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-109">Windows 10 Desktop<sup>2</sup></span></span>
 - <span data-ttu-id="5c29a-110">Windows 10 최신 앱</span><span class="sxs-lookup"><span data-stu-id="5c29a-110">Windows 10 Modern Apps</span></span>
 - <span data-ttu-id="5c29a-111">웹 브라우저</span><span class="sxs-lookup"><span data-stu-id="5c29a-111">Web browsers</span></span>
 - <span data-ttu-id="5c29a-112">Android<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-112">Android<sup>3</sup></span></span>
 - <span data-ttu-id="5c29a-113">iOS<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-113">iOS<sup>1</sup></span></span>
 - <span data-ttu-id="5c29a-114">macOS<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-114">macOS<sup>4</sup></span></span>

<span data-ttu-id="5c29a-115">Microsoft 365의 플랫폼 지원에 대 한 자세한 내용은 [microsoft 365의 시스템 요구 사항을](https://products.office.com/office-system-requirements)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5c29a-115">For more information about platform support in Microsoft 365, see [System requirements for Microsoft 365](https://products.office.com/office-system-requirements).</span></span>

## <a name="supported-clients"></a><span data-ttu-id="5c29a-116">지원되는 클라이언트</span><span class="sxs-lookup"><span data-stu-id="5c29a-116">Supported clients</span></span>

<span data-ttu-id="5c29a-117">최신 버전의 다음 클라이언트는 single sign-on을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c29a-117">The latest versions of the following clients support single sign-on:</span></span>

| | | | | | |
|:---:|:---:|:---:|:---:|:---:|:---:|
| <span data-ttu-id="5c29a-118">![Access 아이콘](../media/o365-access-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-118">![Access icon](../media/o365-access-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-119">Access</span><span class="sxs-lookup"><span data-stu-id="5c29a-119">Access</span></span>](https://products.office.com/access) | <span data-ttu-id="5c29a-120">![회사 포털 아이콘](../media/o365-microsoft-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-120">![Company portal icon](../media/o365-microsoft-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-121">회사 <br> 포털<sup>3, 4</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-121">Company <br> Portal<sup>3,4</sup> </span></span>](https://docs.microsoft.com/intune-user-help/sign-in-to-the-company-portal) | <span data-ttu-id="5c29a-122">![Delve 아이콘](../media/o365-delve-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-122">![Delve icon](../media/o365-delve-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-123">Delve</span><span class="sxs-lookup"><span data-stu-id="5c29a-123">Delve</span></span>](https://products.office.com/business/intelligent-search) | <span data-ttu-id="5c29a-124">![에 지 아이콘](../media/o365-edge-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-124">![Edge icon](../media/o365-edge-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-125">에 지<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-125">Edge<sup>1</sup></span></span>](https://www.microsoft.com/windows/microsoft-edge) | <span data-ttu-id="5c29a-126">![Excel 아이콘](../media/o365-excel-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-126">![Excel icon](../media/o365-excel-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-127">Excel</span><span class="sxs-lookup"><span data-stu-id="5c29a-127">Excel</span></span>](https://products.office.com/excel) 
| <span data-ttu-id="5c29a-128">![Kaizala 아이콘](../media/o365-kaizala-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-128">![Kaizala icon](../media/o365-kaizala-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-129">Kaizala<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-129">Kaizala<sup>1</sup></span></span>](https://products.office.com/en/business/microsoft-kaizala) | <span data-ttu-id="5c29a-130">![Office.com 아이콘](../media/o365-office-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-130">![Office.com icon](../media/o365-office-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-131">Office.com</span><span class="sxs-lookup"><span data-stu-id="5c29a-131">Office.com</span></span>](https://www.office.com/) | <span data-ttu-id="5c29a-132">![렌즈 아이콘](../media/o365-lens-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-132">![Lens icon](../media/o365-lens-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-133">Office Lens</span><span class="sxs-lookup"><span data-stu-id="5c29a-133">Office Lens</span></span>](https://www.microsoft.com/p/office-lens/9wzdncrfj3t8?activetab=pivot%3Aoverviewtab) | <span data-ttu-id="5c29a-134">![비즈니스용 OneDrive 아이콘](../media/o365-OneDrive-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-134">![OneDrive for Business icon](../media/o365-OneDrive-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-135">OneDrive</span><span class="sxs-lookup"><span data-stu-id="5c29a-135">OneDrive</span></span>](https://products.office.com/onedrive-for-business/online-cloud-storage) | <span data-ttu-id="5c29a-136">![OneNote 아이콘](../media/o365-OneNote-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-136">![OneNote icon](../media/o365-OneNote-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-137">OneNote<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-137">OneNote<sup>2</sup></span></span>](https://products.office.com/onenote) 
| <span data-ttu-id="5c29a-138">![Outlook 아이콘](../media/o365-outlook-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-138">![Outlook icon](../media/o365-outlook-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-139">Outlook<sup>4</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-139">Outlook<sup>4</sup></span></span>](https://products.office.com/outlook) | <span data-ttu-id="5c29a-140">![Planner 아이콘](../media/o365-planner-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-140">![Planner icon](../media/o365-planner-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-141">Planner</span><span class="sxs-lookup"><span data-stu-id="5c29a-141">Planner</span></span>](https://products.office.com/business/task-management-software) | <span data-ttu-id="5c29a-142">![전원 자동화 아이콘](../media/o365-flow-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-142">![Power Automate icon](../media/o365-flow-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-143">전원 <br> 자동화</span><span class="sxs-lookup"><span data-stu-id="5c29a-143">Power <br> Automate</span></span>](https://flow.microsoft.com) | <span data-ttu-id="5c29a-144">![PowerBI 아이콘](../media/o365-powerbi-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-144">![PowerBI icon](../media/o365-powerbi-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-145">Power BI<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-145">Power BI<sup>2</sup></span></span>](https://powerbi.microsoft.com)| <span data-ttu-id="5c29a-146">![PowerPoint 아이콘](../media/o365-powerpoint-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-146">![PowerPoint icon](../media/o365-powerpoint-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-147">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="5c29a-147">PowerPoint</span></span>](https://products.office.com/powerpoint) 
| <span data-ttu-id="5c29a-148">![Project 아이콘](../media/o365-project-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-148">![Project icon](../media/o365-project-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-149">Project</span><span class="sxs-lookup"><span data-stu-id="5c29a-149">Project</span></span>](https://products.office.com/project) | <span data-ttu-id="5c29a-150">![Publisher 아이콘](../media/o365-publisher-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-150">![Publisher icon](../media/o365-publisher-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-151">Publisher</span><span class="sxs-lookup"><span data-stu-id="5c29a-151">Publisher</span></span>](https://products.office.com/publisher) | <span data-ttu-id="5c29a-152">![SharePoint 아이콘](../media/o365-sharepoint-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-152">![SharePoint icon](../media/o365-sharepoint-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-153">Sharepoint</span><span class="sxs-lookup"><span data-stu-id="5c29a-153">Sharepoint</span></span>](https://products.office.com/sharepoint) | <span data-ttu-id="5c29a-154">![스티커 메모 아이콘](../media/o365-stickynotes-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-154">![Sticky Notes icon](../media/o365-stickynotes-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-155">스티커 메모</span><span class="sxs-lookup"><span data-stu-id="5c29a-155">Sticky Notes</span></span>](https://www.microsoft.com/p/microsoft-sticky-notes/9nblggh4qghw)  | <span data-ttu-id="5c29a-156">![Sway 아이콘](../media/o365-sway-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-156">![Sway icon](../media/o365-sway-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-157">Sway</span><span class="sxs-lookup"><span data-stu-id="5c29a-157">Sway</span></span>](https://sway.com) 
| <span data-ttu-id="5c29a-158">![Teams 아이콘](../media/o365-teams-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-158">![Teams icon](../media/o365-teams-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-159">팀<sup>2, 4</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-159">Teams<sup>2,4</sup></span></span>](https://products.office.com/microsoft-teams/group-chat-software) | <span data-ttu-id="5c29a-160">![할 일 아이콘](../media/o365-todo-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-160">![To Do icon](../media/o365-todo-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-161">To Do</span><span class="sxs-lookup"><span data-stu-id="5c29a-161">To Do</span></span>](https://todo.microsoft.com) | <span data-ttu-id="5c29a-162">![Visio 아이콘](../media/o365-visio-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-162">![Visio icon](../media/o365-visio-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-163">Visio</span><span class="sxs-lookup"><span data-stu-id="5c29a-163">Visio</span></span>](https://products.office.com/visio/flowchart-software) | <span data-ttu-id="5c29a-164">![Whiteboard 아이콘](../media/o365-whiteboard-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-164">![Whiteboard icon](../media/o365-whiteboard-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-165">화이트 보드<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-165">Whiteboard<sup>3</sup></span></span>](https://whiteboard.microsoft.com/) | <span data-ttu-id="5c29a-166">![Word 아이콘](../media/o365-word-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-166">![Word icon](../media/o365-word-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-167">Word</span><span class="sxs-lookup"><span data-stu-id="5c29a-167">Word</span></span>](https://products.office.com/word) 
| <span data-ttu-id="5c29a-168">![Yammer 아이콘](../media/o365-yammer-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-168">![Yammer icon](../media/o365-yammer-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-169">Yammer<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="5c29a-169">Yammer<sup>2</sup></span></span>](https://products.office.com/yammer/yammer-overview) |

## <a name="supported-powershell-modules"></a><span data-ttu-id="5c29a-170">지원 되는 PowerShell 모듈</span><span class="sxs-lookup"><span data-stu-id="5c29a-170">Supported PowerShell modules</span></span>

| | | | | | |
|:---:|:---:|:---:|:---:|:---:|:---:|
| <span data-ttu-id="5c29a-171">![Azure 아이콘](../media/o365-azure-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-171">![Azure icon](../media/o365-azure-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-172">Azure AD <br> PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c29a-172">Azure AD <br> PowerShell</span></span>](https://docs.microsoft.com/powershell/azure/active-directory/overview?view=azureadps-2.0) | <span data-ttu-id="5c29a-173">![Exchange 아이콘](../media/o365-exchange-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-173">![Exchange icon](../media/o365-exchange-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-174">Exchange Online <br> PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c29a-174">Exchange Online <br> PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps) | <span data-ttu-id="5c29a-175">![SharePoint 아이콘](../media/o365-sharepoint-64x64.png)</span><span class="sxs-lookup"><span data-stu-id="5c29a-175">![SharePoint icon](../media/o365-sharepoint-64x64.png)</span></span> <br> [<span data-ttu-id="5c29a-176">SharePoint Online <br> PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c29a-176">SharePoint Online <br> PowerShell</span></span>](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

> [!NOTE]
> <span data-ttu-id="5c29a-177"><sup>1</sup> IOS의 Edge 및 Kaizala에 대 한 지원이 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="5c29a-177"><sup>1</sup> Support for Edge and Kaizala on iOS available soon.</span></span> <br>
> <span data-ttu-id="5c29a-178"><sup>2</sup> Windows 10 데스크톱의 OneNote, PowerBI, 팀 및 Yammer에 대 한 지원이 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="5c29a-178"><sup>2</sup> Support for OneNote, PowerBI, Teams, and Yammer on Windows 10 Desktop available soon.</span></span> <br>
> <span data-ttu-id="5c29a-179"><sup>3</sup> Android의 화이트 보드 지원 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="5c29a-179"><sup>3</sup> Support for Whiteboard on Android available soon.</span></span> <br>
> <span data-ttu-id="5c29a-180"><sup>4</sup> Macos에서 Outlook, 팀 및 회사 포털에 대 한 지원이 곧 제공 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="5c29a-180"><sup>4</sup> Support for Outlook, Teams, and Company Portal on macOS available soon.</span></span> <br>

## <a name="see-also"></a><span data-ttu-id="5c29a-181">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5c29a-181">See also</span></span>

[<span data-ttu-id="5c29a-182">Microsoft 365 Enterprise 개요</span><span class="sxs-lookup"><span data-stu-id="5c29a-182">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)