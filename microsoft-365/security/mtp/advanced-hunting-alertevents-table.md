---
title: 고급 헌팅 스키마의 AlertEvents 표
description: 고급 헌팅 스키마의 AlertEvents 표에서 경고 생성 이벤트 알아보기
keywords: 고급 헌팅, 위협 헌팅, 사이버 위협 헌팅, 검색, 쿼리, 원격 분석, 스키마 참조, kusto, 표, 열, 데이터 형식, 설명, alertevents, 경고, 심각도, 분류
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: ee14dcc1c2ae0a2bc6fa3c094d757441515f00de
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40807017"
---
# <a name="alertevents"></a><span data-ttu-id="d1696-104">AlertEvents</span><span class="sxs-lookup"><span data-stu-id="d1696-104">AlertEvents</span></span>

<span data-ttu-id="d1696-105">**적용 대상:**</span><span class="sxs-lookup"><span data-stu-id="d1696-105">**Applies to:**</span></span>
- <span data-ttu-id="d1696-106">Microsoft 위협 방지</span><span class="sxs-lookup"><span data-stu-id="d1696-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="d1696-107">[고급 헌팅](advanced-hunting-overview.md) 스키마의 `AlertEvents` 표에는 Microsoft Defender ATP 경고에 대한 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1696-107">The `AlertEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about Microsoft Defender ATP alerts.</span></span> <span data-ttu-id="d1696-108">이 참조를 사용하여 이 표의 정보를 반환하는 쿼리를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d1696-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="d1696-109">고급 헌팅 스키마의 다른 표에 대한 자세한 내용은 [고급 헌팅 참조](advanced-hunting-schema-tables.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1696-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="d1696-110">열 이름</span><span class="sxs-lookup"><span data-stu-id="d1696-110">Column name</span></span> | <span data-ttu-id="d1696-111">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d1696-111">Data type</span></span> | <span data-ttu-id="d1696-112">설명</span><span class="sxs-lookup"><span data-stu-id="d1696-112">Description</span></span> |
|-------------|-----------|-------------|
| `AlertId` | <span data-ttu-id="d1696-113">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-113">string</span></span> | <span data-ttu-id="d1696-114">경고의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d1696-114">Unique identifier for the alert</span></span> |
| `Timestamp` | <span data-ttu-id="d1696-115">datetime</span><span class="sxs-lookup"><span data-stu-id="d1696-115">datetime</span></span> | <span data-ttu-id="d1696-116">이벤트가 기록된 날짜와 시간</span><span class="sxs-lookup"><span data-stu-id="d1696-116">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="d1696-117">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-117">string</span></span> | <span data-ttu-id="d1696-118">서비스에서 시스템의 고유 식별자</span><span class="sxs-lookup"><span data-stu-id="d1696-118">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="d1696-119">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-119">string</span></span> | <span data-ttu-id="d1696-120">컴퓨터의 FQDN(정규화된 도메인 이름)</span><span class="sxs-lookup"><span data-stu-id="d1696-120">Fully qualified domain name (FQDN) of the machine</span></span> |
| `Severity` | <span data-ttu-id="d1696-121">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-121">string</span></span> | <span data-ttu-id="d1696-122">경고로 식별되는 위협 표시기 또는 위반 활동의 잠재적인 영향(높음, 중간 또는 낮음)을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d1696-122">Indicates the potential impact (high, medium, or low) of the threat indicator or breach activity identified by the alert</span></span> |
| `Category` | <span data-ttu-id="d1696-123">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-123">string</span></span> | <span data-ttu-id="d1696-124">경고로 식별되는 위협 표시기 또는 위반 활동 유형</span><span class="sxs-lookup"><span data-stu-id="d1696-124">Type of threat indicator or breach activity identified by the alert</span></span> |
| `Title` | <span data-ttu-id="d1696-125">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-125">string</span></span> | <span data-ttu-id="d1696-126">경고의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="d1696-126">Title of the alert</span></span> |
| `FileName` | <span data-ttu-id="d1696-127">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-127">string</span></span> | <span data-ttu-id="d1696-128">기록된 조치가 적용된 파일의 이름</span><span class="sxs-lookup"><span data-stu-id="d1696-128">Name of the file that the recorded action was applied to</span></span> |
| `SHA1` | <span data-ttu-id="d1696-129">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-129">string</span></span> | <span data-ttu-id="d1696-130">기록된 조치가 적용된 파일의 SHA-1</span><span class="sxs-lookup"><span data-stu-id="d1696-130">SHA-1 of the file that the recorded action was applied to</span></span> |
| `RemoteUrl` | <span data-ttu-id="d1696-131">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-131">string</span></span> | <span data-ttu-id="d1696-132">연결된 URL 또는 FQDN(정규화된 도메인 이름)</span><span class="sxs-lookup"><span data-stu-id="d1696-132">URL or fully qualified domain name (FQDN) that was being connected to</span></span> |
| `RemoteIP` | <span data-ttu-id="d1696-133">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-133">string</span></span> | <span data-ttu-id="d1696-134">연결된 IP 주소</span><span class="sxs-lookup"><span data-stu-id="d1696-134">IP address that was being connected to</span></span> |
| `ReportId` | <span data-ttu-id="d1696-135">long</span><span class="sxs-lookup"><span data-stu-id="d1696-135">long</span></span> | <span data-ttu-id="d1696-136">반복 카운터를 기반으로 하는 이벤트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d1696-136">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="d1696-137">고유 이벤트를 식별 하려면이 열을 장치 이름 및 타임 스탬프 열과 함께 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1696-137">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
| `Table` | <span data-ttu-id="d1696-138">문자열</span><span class="sxs-lookup"><span data-stu-id="d1696-138">string</span></span> | <span data-ttu-id="d1696-139">이벤트에 대한 세부 정보를 포함하는 표</span><span class="sxs-lookup"><span data-stu-id="d1696-139">Table that contains the details of the event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="d1696-140">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d1696-140">Related topics</span></span>
- [<span data-ttu-id="d1696-141">사전 대응식 위협 탐지</span><span class="sxs-lookup"><span data-stu-id="d1696-141">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="d1696-142">쿼리 언어 배우기</span><span class="sxs-lookup"><span data-stu-id="d1696-142">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="d1696-143">공유 쿼리 사용</span><span class="sxs-lookup"><span data-stu-id="d1696-143">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="d1696-144">여러 장치 및 전자 메일에서 위협을 탐지</span><span class="sxs-lookup"><span data-stu-id="d1696-144">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="d1696-145">스키마의 이해</span><span class="sxs-lookup"><span data-stu-id="d1696-145">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="d1696-146">쿼리 모범 사례 적용</span><span class="sxs-lookup"><span data-stu-id="d1696-146">Apply query best practices</span></span>](advanced-hunting-best-practices.md)