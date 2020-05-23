---
title: 고급 헌팅 스키마의 DeviceTvmSoftwareVulnerabilitiesKB 표
description: 고급 헌팅 스키마의 DeviceTvmSoftwareVulnerabilitiesKB 표에서 위협 및 취약성 관리를 통해 추적하는 소프트웨어 취약성에 대해 알아봅니다.
keywords: 고급 구하기, 위협 검색, 사이버 위협 검색, microsoft threat protection, microsoft 365, mtp, m365, 검색, 쿼리, 원격 분석, 스키마, 참조, kusto, table, column, data type, description, threat & 취약성 관리, TVM, 장치 관리, 소프트웨어, 인벤토리, 취약성, CVE ID, CVSS, DeviceTvmSoftwareVulnerabilitiesKB
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 378ffee34a24af225b1b6deebd7cc514c62e1926
ms.sourcegitcommit: f6840dfcfdbcadc53cda591fd6cf9ddcb749d303
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/20/2020
ms.locfileid: "44328001"
---
# <a name="devicetvmsoftwarevulnerabilitieskb"></a><span data-ttu-id="acbf2-104">DeviceTvmSoftwareVulnerabilitiesKB</span><span class="sxs-lookup"><span data-stu-id="acbf2-104">DeviceTvmSoftwareVulnerabilitiesKB</span></span>

<span data-ttu-id="acbf2-105">**적용 대상:**</span><span class="sxs-lookup"><span data-stu-id="acbf2-105">**Applies to:**</span></span>
- <span data-ttu-id="acbf2-106">Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="acbf2-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="acbf2-107">고급 헌팅 스키마의 `DeviceTvmSoftwareVulnerabilitiesKB` 표에는 [위협 및 취약성 관리](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)에서 장치를 평가하는 취약성 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acbf2-107">The `DeviceTvmSoftwareVulnerabilitiesKB` table in the advanced hunting schema contains the list of vulnerabilities [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) assesses devices for.</span></span> <span data-ttu-id="acbf2-108">이 참조를 사용하여 표의 정보를 반환하는 쿼리를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="acbf2-108">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="acbf2-109">고급 헌팅 스키마의 다른 표에 대한 자세한 내용은 [고급 헌팅 참조](advanced-hunting-schema-tables.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="acbf2-109">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="acbf2-110">열 이름</span><span class="sxs-lookup"><span data-stu-id="acbf2-110">Column name</span></span> | <span data-ttu-id="acbf2-111">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="acbf2-111">Data type</span></span> | <span data-ttu-id="acbf2-112">설명</span><span class="sxs-lookup"><span data-stu-id="acbf2-112">Description</span></span> |
|-------------|-----------|-------------|
| `CveId` | <span data-ttu-id="acbf2-113">문자열</span><span class="sxs-lookup"><span data-stu-id="acbf2-113">string</span></span> | <span data-ttu-id="acbf2-114">CVE(Common Vulnerabilities and Exposures) 시스템에서 보안 취약점에 할당된 고유 식별자</span><span class="sxs-lookup"><span data-stu-id="acbf2-114">Unique identifier assigned to the security vulnerability under the Common Vulnerabilities and Exposures (CVE) system</span></span> |
| `CvssScore` | <span data-ttu-id="acbf2-115">문자열</span><span class="sxs-lookup"><span data-stu-id="acbf2-115">string</span></span> | <span data-ttu-id="acbf2-116">CVSS(Common Vulnerability Scoring System)에서 보안 취약점에 할당된 심각도 점수</span><span class="sxs-lookup"><span data-stu-id="acbf2-116">Severity score assigned to the security vulnerability under th Common Vulnerability Scoring System (CVSS)</span></span> |
| `IsExploitAvailable` | <span data-ttu-id="acbf2-117">부울</span><span class="sxs-lookup"><span data-stu-id="acbf2-117">boolean</span></span> | <span data-ttu-id="acbf2-118">취약점에 대한 악용 코드를 공개적으로 사용할 수 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="acbf2-118">Indicates whether exploit code for the vulnerability is publicly available</span></span> |
| `VulnerabilitySeverityLevel` | <span data-ttu-id="acbf2-119">문자열</span><span class="sxs-lookup"><span data-stu-id="acbf2-119">string</span></span> | <span data-ttu-id="acbf2-120">CVSS 점수 및 위협의 영향을 받은 동적 요인에 따라 보안 취약성에 할당된 심각도 수준</span><span class="sxs-lookup"><span data-stu-id="acbf2-120">Severity level assigned to the security vulnerability based on the CVSS score and dynamic factors influenced by the threat landscape</span></span> |
| `LastModifiedTime` | <span data-ttu-id="acbf2-121">datetime</span><span class="sxs-lookup"><span data-stu-id="acbf2-121">datetime</span></span> | <span data-ttu-id="acbf2-122">항목 또는 관련된 메타 데이터가 마지막으로 수정된 날짜와 시간</span><span class="sxs-lookup"><span data-stu-id="acbf2-122">Date and time the item or related metadata was last modified</span></span> |
| `PublishedDate` | <span data-ttu-id="acbf2-123">날짜/시간</span><span class="sxs-lookup"><span data-stu-id="acbf2-123">datetime</span></span> | <span data-ttu-id="acbf2-124">취약점이 공개된 날짜</span><span class="sxs-lookup"><span data-stu-id="acbf2-124">Date vulnerability was disclosed to public</span></span> |
| `VulnerabilityDescription` | <span data-ttu-id="acbf2-125">문자열</span><span class="sxs-lookup"><span data-stu-id="acbf2-125">string</span></span> | <span data-ttu-id="acbf2-126">취약점과 관련된 위험에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="acbf2-126">Description of vulnerability and associated risks</span></span> |
| `AffectedSoftware` | <span data-ttu-id="acbf2-127">문자열</span><span class="sxs-lookup"><span data-stu-id="acbf2-127">string</span></span> | <span data-ttu-id="acbf2-128">취약점에 영향을 받는 모든 소프트웨어 제품 목록</span><span class="sxs-lookup"><span data-stu-id="acbf2-128">List of all software products affected by the vulnerability</span></span> |

## <a name="related-topics"></a><span data-ttu-id="acbf2-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="acbf2-129">Related topics</span></span>

- [<span data-ttu-id="acbf2-130">사전 대응식 위협 탐지</span><span class="sxs-lookup"><span data-stu-id="acbf2-130">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="acbf2-131">쿼리 언어 배우기</span><span class="sxs-lookup"><span data-stu-id="acbf2-131">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="acbf2-132">공유 쿼리 사용</span><span class="sxs-lookup"><span data-stu-id="acbf2-132">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="acbf2-133">여러 장치 및 전자 메일에서 위협을 탐지</span><span class="sxs-lookup"><span data-stu-id="acbf2-133">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="acbf2-134">스키마의 이해</span><span class="sxs-lookup"><span data-stu-id="acbf2-134">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="acbf2-135">쿼리 모범 사례 적용</span><span class="sxs-lookup"><span data-stu-id="acbf2-135">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="acbf2-136">위협 및 취약성 관리 개요</span><span class="sxs-lookup"><span data-stu-id="acbf2-136">Overview of Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)