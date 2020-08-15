---
title: Office 365 관리 작업 API
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
f1.keywords:
- NOCSH
description: 이 문서에서는 Office 365 관리 활동 API 및 활동 로그에서 제공 하는 정보에 대 한 간략 한 요약을 확인할 수 있습니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: ea08673f4c26c9ee4b7093ba420b69bed91abc81
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692765"
---
# <a name="office-365-management-activity-api"></a><span data-ttu-id="2f425-103">Office 365 관리 작업 API</span><span class="sxs-lookup"><span data-stu-id="2f425-103">Office 365 Management Activity API</span></span>

<span data-ttu-id="2f425-104">Microsoft는 Office 365 테 넌 트에 대 한 집계 된 트랜잭션 정보를 가져오는 데 사용할 수 있는 보고 서비스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-104">Microsoft provides reporting services you can use to obtain aggregated transactional information about your Office 365 tenant.</span></span> <span data-ttu-id="2f425-105">[Office 365 관리 활동 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview#office-365-management-activity-api) 는 인증을 위해 업계 표준 RESTful 디자인 및 OAuth v2를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-105">The [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview#office-365-management-activity-api) uses an industry-standard RESTful design and OAuth v2 for authentication.</span></span> <span data-ttu-id="2f425-106">따라서 데이터 검색 및 시각화 도구와 응용 프로그램으로의 ingesting 쉽게 실험해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-106">This makes it easy to start experimenting with retrieving data and ingesting it into visualization tools and applications.</span></span> <span data-ttu-id="2f425-107">이 API는 Office 365의 사용자, 관리자, 작업 및 보안 작업에 대 한 정보가 포함 된 데이터 피드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-107">The API provides a data feed with information about user, administrator, operations, and security activity in Office 365.</span></span> <span data-ttu-id="2f425-108">데이터는 규정 목적에 따라 유지 하거나 온-프레미스 인프라 또는 기타 원본에서 확보 된 로그 데이터와 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-108">The data can be kept for regulatory purposes, or combined with log data procured from an on-premises infrastructure or other sources.</span></span> <span data-ttu-id="2f425-109">이렇게 하면 기업 전체의 운영, 보안 및 규정 준수를 위한 모니터링 솔루션을 구축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-109">This helps build a monitoring solution for operations, security, and compliance across the enterprise.</span></span>

<span data-ttu-id="2f425-110">Office 365 관리 활동 API는 Office 365 및 Azure Active Directory 활동 로그에서 다양 한 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-110">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="2f425-111">이 API는 모든 서비스에서 공통 되는 10 개 이상의 필드와 일관성 있는 감사 스키마를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-111">The API provides a consistent audit schema with over 10 fields common across all the services.</span></span> <span data-ttu-id="2f425-112">이 API를 사용 하면 조직에서 이벤트 간의 쉬운 연결을 가능 하 게 하 고 데이터에 대 한 이유를 새로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-112">The API allows organizations to make easy connections between events, and enables new ways to reason over the data.</span></span>

<span data-ttu-id="2f425-113">Microsoft와 제휴 하 고 API를 기반으로 만든 솔루션을 포함 하는 수십 개의 독립 소프트웨어 공급 업체 (Isv)</span><span class="sxs-lookup"><span data-stu-id="2f425-113">Dozens of Independent Software Vendors (ISVs) partnered with Microsoft and have built solutions based on the API.</span></span> <span data-ttu-id="2f425-114">일부 솔루션은 Office 365 데이터와 여러 클라우드 공급자 및 온-프레미스 시스템의 다른 원본 데이터에만 초점을 둔 후 운영, 보안 및 준수 관련 활동의 통합 된 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f425-114">Some solutions focus solely on Office 365 data and others source data from multiple cloud providers and on-premises systems to create a unified view of operations, security, and compliance-related activity.</span></span> 

<span data-ttu-id="2f425-115">자세한 내용은 [Office 365 관리 활동 API 참조](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2f425-115">For more information, see the [Office 365 Management Activity API reference](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>