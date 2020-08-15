---
title: Microsoft 365 끝점
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/07/2018
audience: ITPro
ms.topic: hub-page
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_TLGs
- seo-marvel-apr2020
ms.assetid: ''
description: Microsoft 365 트래픽에 대 한 대상 IP 주소 및 Url을 보려면 다른 Microsoft 365 클라우드의 인터넷 끝점에 대 한이 문서 목록을 사용 하십시오.
ms.openlocfilehash: b0d8468eaa1b56d1151e54d8e05e6ada51845118
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692632"
---
# <a name="microsoft-365-endpoints"></a><span data-ttu-id="0d6ca-103">Microsoft 365 끝점</span><span class="sxs-lookup"><span data-stu-id="0d6ca-103">Microsoft 365 endpoints</span></span>

<span data-ttu-id="0d6ca-104">*이 문서는 Microsoft 365 Enterprise와 Office 365 Enterprise에 모두 적용됩니다.*</span><span class="sxs-lookup"><span data-stu-id="0d6ca-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="0d6ca-105">끝점은 인터넷에서 Microsoft 365 트래픽에 대 한 대상 IP 주소, DNS 도메인 이름 및 Url의 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-105">Endpoints are the set of destination IP addresses, DNS domain names, and URLs for Microsoft 365 traffic on the Internet.</span></span> 

<span data-ttu-id="0d6ca-106">Microsoft 365 클라우드 기반 서비스에 대 한 성능을 최적화 하기 위해 이러한 끝점에는 클라이언트 브라우저 및에 지 네트워크의 장치에서 특별 하 게 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-106">To optimize performance to Microsoft 365 cloud-based services, these endpoints need special handling by your client browsers and the devices in your edge network.</span></span> <span data-ttu-id="0d6ca-107">이러한 장치에는 방화벽, SSL 중단 및 검사 및 패킷 검사 장치 및 데이터 손실 방지 시스템이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-107">These devices include firewalls, SSL Break and Inspect and packet inspection devices, and data loss prevention systems.</span></span>

<span data-ttu-id="0d6ca-108">자세한 내용은 [Microsoft 365 Endpoints 관리](managing-office-365-endpoints.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-108">See [Managing Microsoft 365 endpoints](managing-office-365-endpoints.md) for the details.</span></span>

<span data-ttu-id="0d6ca-109">현재 다섯 가지 Microsoft 365 클라우드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-109">There are currently five different Microsoft 365 clouds.</span></span> <span data-ttu-id="0d6ca-110">이 표에서는 각 항목에 대 한 끝점 목록으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-110">This table takes you to the list of endpoints for each one.</span></span>

| <span data-ttu-id="0d6ca-111">클라우드</span><span class="sxs-lookup"><span data-stu-id="0d6ca-111">Cloud</span></span> | <span data-ttu-id="0d6ca-112">설명</span><span class="sxs-lookup"><span data-stu-id="0d6ca-112">Description</span></span> |
|:-------|:-----|
| [<span data-ttu-id="0d6ca-113">전 세계 끝점</span><span class="sxs-lookup"><span data-stu-id="0d6ca-113">Worldwide endpoints</span></span>](urls-and-ip-address-ranges.md) | <span data-ttu-id="0d6ca-114">미국 GCC (정부 커뮤니티 클라우드)를 포함 하는 전 세계 Microsoft 365 구독의 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-114">The endpoints for worldwide Microsoft 365 subscriptions, which include the United States Government Community Cloud (GCC).</span></span> |
| [<span data-ttu-id="0d6ca-115">미국 정부 DoD 엔드포인트</span><span class="sxs-lookup"><span data-stu-id="0d6ca-115">U.S. Government DoD endpoints</span></span>](microsoft-365-u-s-government-dod-endpoints.md) | <span data-ttu-id="0d6ca-116">미국 DoD(국방부) 구독의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-116">The endpoints for United States Department of Defense (DoD) subscriptions.</span></span> |
| [<span data-ttu-id="0d6ca-117">미국 정부 GCC High 엔드포인트</span><span class="sxs-lookup"><span data-stu-id="0d6ca-117">U.S. Government GCC High endpoints</span></span>](microsoft-365-u-s-government-gcc-high-endpoints.md) | <span data-ttu-id="0d6ca-118">미국 GCC(정부 커뮤니티 클라우드) High 구독의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-118">The endpoints for United States Government Community Cloud High (GCC High) subscriptions.</span></span> |
| [<span data-ttu-id="0d6ca-119">21Vianet에서 운영 하는 Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0d6ca-119">Microsoft 365 operated by 21Vianet endpoints</span></span>](urls-and-ip-address-ranges-21vianet.md) | <span data-ttu-id="0d6ca-120">중국의 Microsoft 365에 대 한 요구를 충족 하도록 설계 된 21Vianet에서 운영 하는 Microsoft 365의 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-120">The endpoints for Microsoft 365 operated by 21Vianet, which is designed to meet the needs for Microsoft 365 in China.</span></span> |
| [<span data-ttu-id="0d6ca-121">Microsoft 365 독일 끝점</span><span class="sxs-lookup"><span data-stu-id="0d6ca-121">Microsoft 365 Germany endpoints</span></span>](microsoft-365-germany-endpoints.md) | <span data-ttu-id="0d6ca-122">독일, EU(유럽 연합), EFTA(유럽 자유 무역 연합)의 가장 규제를 많이 받는 고객을 위해 유럽에 있는 별도 클라우드의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-122">The endpoints for a separate cloud in Europe for the most regulated customers in Germany, the European Union (EU), and the European Free Trade Association (EFTA).</span></span> |
|||

<span data-ttu-id="0d6ca-123">Microsoft 365 클라우드의 최신 끝점 목록을 자동으로 가져오려면 [Office 365 IP 주소 및 URL 웹 서비스](microsoft-365-ip-web-service.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-123">To automate getting the latest list of endpoints for your Microsoft 365 cloud, see the [Office 365 IP Address and URL Web service](microsoft-365-ip-web-service.md).</span></span>

<span data-ttu-id="0d6ca-124">엔드포인트에 대한 추가 내용은 다음 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-124">For additional endpoints, see these articles:</span></span>

- [<span data-ttu-id="0d6ca-125">웹 서비스에 포함되지 않는 추가 엔드포인트</span><span class="sxs-lookup"><span data-stu-id="0d6ca-125">Additional endpoints not included in the Web service</span></span>](additional-office365-ip-addresses-and-urls.md)
- [<span data-ttu-id="0d6ca-126">Mac용 Office 2016의 네트워크 요청</span><span class="sxs-lookup"><span data-stu-id="0d6ca-126">Network requests in Office 2016 for Mac</span></span>](network-requests-in-office-2016-for-mac.md)

<span data-ttu-id="0d6ca-127">네트워크 장비 공급 업체가 면 [Office 365 네트워킹 파트너 프로그램](microsoft-365-networking-partner-program.md)에 가입 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-127">If you are a network equipment vendor, join the [Office 365 Networking Partner Program](microsoft-365-networking-partner-program.md).</span></span> <span data-ttu-id="0d6ca-128">제품 및 솔루션에 Microsoft 365 네트워크 연결 원리를 빌드하기 위해 프로그램에 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d6ca-128">Enroll in the program to build Microsoft 365 network connectivity principles into your products and solutions.</span></span> 