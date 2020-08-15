---
title: Microsoft 365의 관리 액세스 제어
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: seo-marvel-apr2020
description: 이 문서에서는 Microsoft 365의 관리 액세스 제어 및 데이터 분류에 대 한 개요를 제공 합니다.
ms.openlocfilehash: b5063f89e89b6cffffda53a5df3088a80f89c242
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692341"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="0bfc8-103">Microsoft 365의 관리 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="0bfc8-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="0bfc8-104">Microsoft는 microsoft의 고객 콘텐츠에 대 한 액세스를 의도적으로 제한 하면서 대부분의 Microsoft 365 운영을 자동화 하는 시스템 및 컨트롤에 크게 투자 했습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="0bfc8-105">서비스를 관리 하 고 소프트웨어가 서비스를 운영 하는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="0bfc8-106">이를 통해 Microsoft는 확장 시 Microsoft 365을 관리 하 고 고객 콘텐츠에 대 한 내부 위협의 위험을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-106">This enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="0bfc8-107">기본적으로 Microsoft 엔지니어가 관리 권한을 보유 하 고 있으며 Microsoft 365의 고객 콘텐츠에 대 한 액세스 권한이 0으로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="0bfc8-108">제한 된 기간 동안 Microsoft 엔지니어가 고객 콘텐츠에 대 한 액세스를 제한 하 고 감사 하 고 보안을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="0bfc8-109">액세스는 서비스 작업에 필요한 경우에만 사용 되며 Microsoft의 선임 관리 구성원이 승인 하는 경우에만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="0bfc8-110">고객 인증 키 저장소 사용이 허가 된 고객의 경우 고객은 Microsoft 365에서 호스트 되는 콘텐츠에 대 한 액세스 승인을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="0bfc8-111">Microsoft는 다양 한 형태의 클라우드 전달을 사용 하 여 온라인 서비스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="0bfc8-112">**공용 클라우드:** Microsoft 365, Azure 및 북미, 남미, 유럽, 아시아, 오스트레일리아 등에 호스트 되는 기타 서비스의 다중 테 넌 트 버전을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="0bfc8-113">**국가 클라우드:** 이전에 언급 한 것 처럼 미국 외부에 있는 sovereign 클라우드에 및 타사에서 운영 하는 모든 클라우드 (예: microsoft에서 운영 하는 microsoft 365) 및 독일 (독일어 데이터 트러스티를 사용 하는 모델에 따라 microsoft는 고객 데이터를 포함 하는 고객 데이터 및 시스템에 대 한 액세스를 제어 하 고 모니터링 하는 microsoft 365)를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="0bfc8-114">**정부 클라우드:** 미국 정부 고객에 게 제공 되는 Microsoft 365 및 Azure 서비스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="0bfc8-115">이 문서에서 제공 하는 Microsoft 365 서비스에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="0bfc8-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="0bfc8-116">Exchange Online</span></span>](https://docs.microsoft.com/Exchange/exchange-online)
- [<span data-ttu-id="0bfc8-117">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="0bfc8-117">Exchange Online Protection</span></span>](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="0bfc8-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0bfc8-118">SharePoint Online</span></span>](https://docs.microsoft.com/sharepoint/sharepoint-online)
- [<span data-ttu-id="0bfc8-119">비즈니스용 OneDrive</span><span class="sxs-lookup"><span data-stu-id="0bfc8-119">OneDrive for Business</span></span>](https://docs.microsoft.com/OneDrive/onedrive)
- [<span data-ttu-id="0bfc8-120">비즈니스용 Skype</span><span class="sxs-lookup"><span data-stu-id="0bfc8-120">Skype for Business</span></span>](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="0bfc8-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0bfc8-121">Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="0bfc8-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="0bfc8-122">Yammer</span></span>](https://docs.microsoft.com/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="0bfc8-123">Microsoft 365 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="0bfc8-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="0bfc8-124">액세스 제어를 위해 microsoft는 Microsoft 365 데이터를 고객 데이터 또는 기타 데이터 형식으로 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="0bfc8-125">고객 데이터</span><span class="sxs-lookup"><span data-stu-id="0bfc8-125">Customer data</span></span>

<span data-ttu-id="0bfc8-126">고객 데이터는 Microsoft 365 서비스를 사용 하는 경우 고객을 대신 하 여 또는에서 제공 하는 모든 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="0bfc8-127">다음을 포함 하 여 Microsoft 365 사용자가 직접 만들거나 업로드 한 고객 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-127">This is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="0bfc8-128">전자 메일</span><span class="sxs-lookup"><span data-stu-id="0bfc8-128">Emails</span></span>
- <span data-ttu-id="0bfc8-129">SharePoint Online 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="0bfc8-129">SharePoint Online content</span></span>
- <span data-ttu-id="0bfc8-130">인스턴트 메시지</span><span class="sxs-lookup"><span data-stu-id="0bfc8-130">Instant messages</span></span>
- <span data-ttu-id="0bfc8-131">일정 항목</span><span class="sxs-lookup"><span data-stu-id="0bfc8-131">Calendar items</span></span>
- <span data-ttu-id="0bfc8-132">문서</span><span class="sxs-lookup"><span data-stu-id="0bfc8-132">Documents</span></span>
- <span data-ttu-id="0bfc8-133">Contacts</span><span class="sxs-lookup"><span data-stu-id="0bfc8-133">Contacts</span></span>
- <span data-ttu-id="0bfc8-134">EUII (최종 사용자 식별 가능 정보) (사용자에 게는 고유 하거나 개별 사용자에 게 linkable 하지만 고객 콘텐츠는 포함 하지 않는 데이터)</span><span class="sxs-lookup"><span data-stu-id="0bfc8-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="0bfc8-135">기타 데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0bfc8-135">Other types of data</span></span>

<span data-ttu-id="0bfc8-136">다른 데이터 형식에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-136">Other types of data include:</span></span>

- <span data-ttu-id="0bfc8-137">**계정 데이터:** 관리 데이터 (관리자가 서비스를 등록 하거나 구매할 때 제공 하는 정보) 및 지불 데이터 (신용 카드 정보와 같은 결제 방식 정보)를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="0bfc8-138">**조직 차원 식별이 가능한 정보:** 테 넌 트, 사용 현황 데이터를 식별 하 고 개별 사용자에 게 linkable 하는 데 사용 되거나 고객 콘텐츠에 포함 되지 않은 데이터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="0bfc8-139">**시스템 메타 데이터:** 구성 설정, 시스템 상태, Microsoft IP 주소 및 구독 및 테 넌 트에 대 한 기술 정보가 포함 된 서비스 로그를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="0bfc8-140">Microsoft는 고객 데이터 또는 액세스 제어 데이터에 대 한 승인 되지 않은 액세스를 사용 하지 않도록 액세스 제어 메커니즘을 설정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="0bfc8-141">액세스 제어 데이터는 고객 콘텐츠 또는 EUII, Microsoft 암호, 보안 인증서 및 기타 인증 관련 데이터에 대 한 액세스를 포함 하 여 환경 내에서 다른 유형의 데이터 또는 기능에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="0bfc8-142">또한 액세스 제어 메커니즘은 Microsoft 365 프로덕션 환경에 대 한 승인 되지 않은 물리적, 논리적 또는 원격 액세스를 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="0bfc8-143">Microsoft 365 운영에 사용 되는 세 가지 종류의 access 컨트롤이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="0bfc8-144">격리 컨트롤</span><span class="sxs-lookup"><span data-stu-id="0bfc8-144">Isolation controls</span></span>
- <span data-ttu-id="0bfc8-145">인적 컨트롤</span><span class="sxs-lookup"><span data-stu-id="0bfc8-145">Personnel controls</span></span>
- <span data-ttu-id="0bfc8-146">기술 컨트롤</span><span class="sxs-lookup"><span data-stu-id="0bfc8-146">Technology controls</span></span>

<span data-ttu-id="0bfc8-147">이러한 컨트롤을 결합 하면 Microsoft 365의 악의적인 작업을 방지 하 고 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="0bfc8-148">Microsoft에서 사용 하는 격리, 인력 및 기술 제어 외에도 customer에서 구현 하는 컨트롤의 네 번째 범주를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those implemented by customers.</span></span>

<span data-ttu-id="0bfc8-149">Microsoft 365에서는 온-프레미스 환경에서 데이터를 관리 하는 것과 동일한 방식으로 데이터를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="0bfc8-150">Microsoft 365 조직에 로그인 하는 사용자는 자동으로 전역 관리자가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="0bfc8-151">전역 관리자는 관리 포털의 모든 기능에 액세스할 수 있으며 다음이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-151">The global admin has access to all features in management portals and can:</span></span>

- <span data-ttu-id="0bfc8-152">사용자 만들기 또는 편집</span><span class="sxs-lookup"><span data-stu-id="0bfc8-152">Create or edit users</span></span>
- <span data-ttu-id="0bfc8-153">다른 사용자에 게 관리자 역할 할당</span><span class="sxs-lookup"><span data-stu-id="0bfc8-153">Assign admin roles to others</span></span>
- <span data-ttu-id="0bfc8-154">사용자 암호 다시 설정</span><span class="sxs-lookup"><span data-stu-id="0bfc8-154">Reset user passwords</span></span>
- <span data-ttu-id="0bfc8-155">사용자 라이선스 관리</span><span class="sxs-lookup"><span data-stu-id="0bfc8-155">Manage user licenses</span></span>
- <span data-ttu-id="0bfc8-156">도메인 관리</span><span class="sxs-lookup"><span data-stu-id="0bfc8-156">Manage domains</span></span>
- <span data-ttu-id="0bfc8-157">고객 Lockbox 요청 승인</span><span class="sxs-lookup"><span data-stu-id="0bfc8-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="0bfc8-158">각 조직에서는 최소 두 개의 관리자 계정을 구성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="0bfc8-159">대규모 엔터프라이즈 조직의 경우 다른 기능을 제공 하는 특수 한 관리자 계정을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="0bfc8-160">관리자 역할 및 사용 권한을 할당 하는 방법에 대 한 자세한 내용은 [관리자 역할 할당](https://docs.microsoft.com/microsoft-365/admin/add-users/assign-admin-roles) 및 [관리 역할 정보](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0bfc8-160">For information about assigning admin roles and permissions, see [Assign admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="0bfc8-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bfc8-161">Related Links</span></span>

- [<span data-ttu-id="0bfc8-162">격리 컨트롤</span><span class="sxs-lookup"><span data-stu-id="0bfc8-162">Isolation Controls</span></span>](microsoft-365-isolation-controls.md)
- [<span data-ttu-id="0bfc8-163">인적 컨트롤</span><span class="sxs-lookup"><span data-stu-id="0bfc8-163">Personnel Controls</span></span>](microsoft-365-personnel-controls.md)
- [<span data-ttu-id="0bfc8-164">기술 컨트롤</span><span class="sxs-lookup"><span data-stu-id="0bfc8-164">Technology Controls</span></span>](microsoft-365-technology-controls.md)
- [<span data-ttu-id="0bfc8-165">액세스 제어 모니터링 및 감사</span><span class="sxs-lookup"><span data-stu-id="0bfc8-165">Monitoring and Auditing Access Controls</span></span>](microsoft-365-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="0bfc8-166">Yammer Enterprise 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="0bfc8-166">Yammer Enterprise Access Controls</span></span>](microsoft-365-yammer-enterprise-access-controls.md)