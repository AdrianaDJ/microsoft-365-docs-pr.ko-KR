---
title: SIEM과 Office 365 Advanced Threat Protection의 통합
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
ms.date: 11/22/2019
ms.collection:
- M365-security-compliance
description: Office 365 활동 관리 API에서 조직의 SIEM server를 Office 365 Advanced Threat Protection 및 관련 위협 이벤트와 통합 합니다.
ms.openlocfilehash: 93253982b9920cd133419e0fc61650cadfa9d192
ms.sourcegitcommit: 8c244b38c43dd00c4ef0102f8bed02ab36639a6b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2019
ms.locfileid: "39967931"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a><span data-ttu-id="4a601-103">SIEM과 Office 365 Advanced Threat Protection의 통합</span><span class="sxs-lookup"><span data-stu-id="4a601-103">SIEM integration with Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="4a601-104">조직에서 SIEM (보안 인시던트 및 이벤트 관리) 서버를 사용 하는 경우 Office 365 Advanced Threat Protection을 SIEM 서버와 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-104">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Advanced Threat Protection with your SIEM server.</span></span> <span data-ttu-id="4a601-105">SIEM 통합을 사용 하면 SIEM server reports에서 Office 365 고급 보호를 통해 검색 된 맬웨어 또는 피싱 같은 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-105">SIEM integration enables you to view information, such as malware or phish detected by Office 365 Advanced Protection, in your SIEM server reports.</span></span> <span data-ttu-id="4a601-106">SIEM 통합을 설정 하려면 [Office 365 활동 관리 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-106">To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="4a601-107">Office 365 활동 관리 API는 조직의 Office 365 및 Azure Active Directory 활동 로그에서 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-107">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="4a601-108">[Office 365 Advanced Threat protection 스키마](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) 는 Advanced threat protection과 함께 작동 하므로 조직에 Office 365 Advanced Threat protection 계획 1 또는 계획 2 또는 Office 365 E5가 있는 경우에도이 API를 사용 하 여 siem 서버 통합에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-108">The [Office 365 Advanced Threat Protection schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) works with Advanced Threat Protection, so if your organization has the Office 365 Advanced Threat Protection Plan 1 or Plan 2 or Office 365 E5, you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="4a601-109">최근 업데이트의 일환으로 Office 365 관리 활동 API 내에서 Office 365 ATP 계획 2의 자동화 된 조사 및 응답 기능의 이벤트가 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-109">As part of our recent updates, we have also added events from automated investigation and response capabilities in Office 365 ATP Plan 2 within the Office 365 Management Activity API.</span></span> <span data-ttu-id="4a601-110">ID, 이름 및 상태와 같은 핵심 조사 세부 정보에 대 한 데이터를 포함 하는 것 외에도 조사 작업 및 엔터티에 대 한 높은 수준의 정보도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-110">In addition to including data about core investigation details such as ID, name and status, it also contains high-level information about investigation actions and entities.</span></span>   

<span data-ttu-id="4a601-111">SIEM 서버 또는 기타 유사한 시스템에서 **감사의 일반적인** 작업을 폴링하여 검색 이벤트에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-111">The SIEM server or other similar system should poll the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="4a601-112">자세한 내용은 [Office 365 관리 api 시작](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a601-112">To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> <span data-ttu-id="4a601-113">또한 다음 **AuditLogRecordType** 값은 OFFICE 365 ATP 이벤트와 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-113">In addition, the following values of **AuditLogRecordType** are relevant for Office 365 ATP events:</span></span>

### <a name="enum-auditlogrecordtype---type-edmint32"></a><span data-ttu-id="4a601-114">Enum: AuditLogRecordType: Edm. i a i. Int32</span><span class="sxs-lookup"><span data-stu-id="4a601-114">Enum: AuditLogRecordType - Type: Edm.Int32</span></span>

#### <a name="auditlogrecordtype"></a><span data-ttu-id="4a601-115">AuditLogRecordType</span><span class="sxs-lookup"><span data-stu-id="4a601-115">AuditLogRecordType</span></span>

|<span data-ttu-id="4a601-116">값</span><span class="sxs-lookup"><span data-stu-id="4a601-116">Value</span></span>|<span data-ttu-id="4a601-117">멤버 이름</span><span class="sxs-lookup"><span data-stu-id="4a601-117">Member name</span></span>|<span data-ttu-id="4a601-118">설명</span><span class="sxs-lookup"><span data-stu-id="4a601-118">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a601-119">28@@</span><span class="sxs-lookup"><span data-stu-id="4a601-119">28</span></span>|<span data-ttu-id="4a601-120">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="4a601-120">ThreatIntelligence</span></span>|<span data-ttu-id="4a601-121">Exchange Online Protection 및 Office 365 Advanced Threat Protection의 피싱 및 맬웨어 이벤트</span><span class="sxs-lookup"><span data-stu-id="4a601-121">Phishing and malware events from Exchange Online Protection and Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="4a601-122">41</span><span class="sxs-lookup"><span data-stu-id="4a601-122">41</span></span>|<span data-ttu-id="4a601-123">ThreatIntelligenceUrl</span><span class="sxs-lookup"><span data-stu-id="4a601-123">ThreatIntelligenceUrl</span></span>|<span data-ttu-id="4a601-124">ATP Safe 링크는 Office 365 Advanced Threat Protection에서 차단 및 차단 이벤트 차단을 방지 하 고 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-124">ATP Safe Links time-of-block and block override events from Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="4a601-125">47</span><span class="sxs-lookup"><span data-stu-id="4a601-125">47</span></span>|<span data-ttu-id="4a601-126">ThreatIntelligenceAtpContent</span><span class="sxs-lookup"><span data-stu-id="4a601-126">ThreatIntelligenceAtpContent</span></span>|<span data-ttu-id="4a601-127">SharePoint Online, 비즈니스용 OneDrive 및 Office 365 Advanced Threat Protection의 파일에 대 한 피싱 및 맬웨어 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-127">Phishing and malware events for files in SharePoint Online, OneDrive for Business, and Microsoft Teams from Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="4a601-128">64</span><span class="sxs-lookup"><span data-stu-id="4a601-128">64</span></span>|<span data-ttu-id="4a601-129">방송 조사</span><span class="sxs-lookup"><span data-stu-id="4a601-129">AirInvestigation</span></span>|<span data-ttu-id="4a601-130">검사 세부 정보 및 Office 365 Advanced Threat Protection 계획 2의 관련 아티팩트와 같은 자동화 된 조사 및 응답 이벤트</span><span class="sxs-lookup"><span data-stu-id="4a601-130">Automated investigation and response events, such as investigation details and relevant artifacts from Office 365 Advanced Threat Protection Plan 2.</span></span>|


> [!IMPORTANT]
> <span data-ttu-id="4a601-131">Office 365 Advanced Threat Protection과 함께 SIEM 통합을 설정 하려면 Office 365 전역 관리자 이거나 보안 & 준수 센터에 대해 보안 관리자 역할이 할당 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-131">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="4a601-132">Office 365 환경에 대해 감사 로깅을 켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a601-132">Audit logging must be turned on for your Office 365 environment.</span></span> <span data-ttu-id="4a601-133">이에 대 한 도움말을 보려면 [Turn Office 365 감사 로그 검색 설정 또는 해제](../../compliance/turn-audit-log-search-on-or-off.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a601-133">To get help with this, see [Turn Office 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a601-134">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4a601-134">Related topics</span></span>

[<span data-ttu-id="4a601-135">Office 365 위협 조사 및 응답</span><span class="sxs-lookup"><span data-stu-id="4a601-135">Office 365 threat investigation and response</span></span>](office-365-ti.md)

[<span data-ttu-id="4a601-136">Office 365의 자동화 된 조사 및 응답 (AIR)</span><span class="sxs-lookup"><span data-stu-id="4a601-136">Automated investigation and response (AIR) in Office 365</span></span>](automated-investigation-response-office.md)

[<span data-ttu-id="4a601-137">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="4a601-137">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="4a601-138">Office 365 보안 &amp; 및 준수 센터의 Smart reports 및 정보</span><span class="sxs-lookup"><span data-stu-id="4a601-138">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="4a601-139">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="4a601-139">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  