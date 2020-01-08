---
title: 고급 헌팅 스키마의 DeviceTvmSecureConfigurationAssessment 표
description: 고급 헌팅 스키마의 DeviceTvmSecureConfigurationAssessment 표에서 위협 및 취약성 관리 보안 평가 이벤트에 대해 알아보세요. 이러한 이벤트는 시스템 정보, 보안 구성 세부 정보, 영향, 준수 정보를 제공합니다.
keywords: 고급 헌팅, 위협 헌팅, 사이버 위협 헌팅, 검색, 쿼리, 원격 분석, 스키마 참조, kusto, 표, 열, 데이터 형식, 설명, 위협 및 취약성 관리, TVM, 장치 관리, 보안 구성, DeviceTvmSecureConfigurationAssessment
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
ms.openlocfilehash: d03b278fbf029b08b476f20292315807a3f5e32a
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40808623"
---
# <a name="devicetvmsecureconfigurationassessment"></a><span data-ttu-id="f878c-105">DeviceTvmSecureConfigurationAssessment</span><span class="sxs-lookup"><span data-stu-id="f878c-105">DeviceTvmSecureConfigurationAssessment</span></span>

<span data-ttu-id="f878c-106">**적용 대상:**</span><span class="sxs-lookup"><span data-stu-id="f878c-106">**Applies to:**</span></span>
- <span data-ttu-id="f878c-107">Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="f878c-107">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="f878c-108">`DeviceTvmSecureConfigurationAssessment` 표의 각 행에는 [위협 및 취약성 관리](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)의 특정 보안 구성에 대한 평가 이벤트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f878c-108">Each row in the `DeviceTvmSecureConfigurationAssessment` table contains an assessment event for a specific security configuration from [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt).</span></span> <span data-ttu-id="f878c-109">이 참조를 사용하여 최신 평가 결과를 확인하고 장치가 호환되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f878c-109">Use this reference to check the latest assessment results and determine whether devices are compliant.</span></span>

<span data-ttu-id="f878c-110">고급 헌팅 스키마의 다른 표에 대한 자세한 내용은 [고급 헌팅 참조](advanced-hunting-schema-tables.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f878c-110">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="f878c-111">열 이름</span><span class="sxs-lookup"><span data-stu-id="f878c-111">Column name</span></span> | <span data-ttu-id="f878c-112">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="f878c-112">Data type</span></span> | <span data-ttu-id="f878c-113">설명</span><span class="sxs-lookup"><span data-stu-id="f878c-113">Description</span></span> |
|-------------|-----------|-------------|
| `DeviceId` | <span data-ttu-id="f878c-114">문자열</span><span class="sxs-lookup"><span data-stu-id="f878c-114">string</span></span> | <span data-ttu-id="f878c-115">서비스에서 시스템의 고유 식별자</span><span class="sxs-lookup"><span data-stu-id="f878c-115">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="f878c-116">문자열</span><span class="sxs-lookup"><span data-stu-id="f878c-116">string</span></span> | <span data-ttu-id="f878c-117">컴퓨터의 FQDN(정규화된 도메인 이름)</span><span class="sxs-lookup"><span data-stu-id="f878c-117">Fully qualified domain name (FQDN) of the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="f878c-118">문자열</span><span class="sxs-lookup"><span data-stu-id="f878c-118">string</span></span> | <span data-ttu-id="f878c-119">컴퓨터에서 실행 중인 운영 체제의 플랫폼</span><span class="sxs-lookup"><span data-stu-id="f878c-119">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="f878c-120">이는 Windows 10 및 Windows 7과 같이 동일한 제품군 내의 변형을 포함하여 특정 운영 체제를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f878c-120">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span>|
| `Timestamp` | <span data-ttu-id="f878c-121">날짜 시간</span><span class="sxs-lookup"><span data-stu-id="f878c-121">datetime</span></span> | <span data-ttu-id="f878c-122">레코드 생성 날짜 및 시간</span><span class="sxs-lookup"><span data-stu-id="f878c-122">Date and time when the record was generated</span></span> |
| `ConfigurationId` | <span data-ttu-id="f878c-123">문자열</span><span class="sxs-lookup"><span data-stu-id="f878c-123">string</span></span> | <span data-ttu-id="f878c-124">특정 구성의 고유 식별자</span><span class="sxs-lookup"><span data-stu-id="f878c-124">Unique identifier for a specific configuration</span></span> |
| `ConfigurationCategory` | <span data-ttu-id="f878c-125">문자열</span><span class="sxs-lookup"><span data-stu-id="f878c-125">string</span></span> | <span data-ttu-id="f878c-126">구성이 속해 있는 범주 또는 그룹(응용 프로그램, OS, 네트워크, 계정, 보안 제어)</span><span class="sxs-lookup"><span data-stu-id="f878c-126">Category or grouping to which the configuration belongs: Application, OS, Network, Accounts, Security controls</span></span> |
| `ConfigurationSubcategory` | <span data-ttu-id="f878c-127">문자열</span><span class="sxs-lookup"><span data-stu-id="f878c-127">string</span></span> | <span data-ttu-id="f878c-128">구성이 속한 하위 범주나 하위 그룹</span><span class="sxs-lookup"><span data-stu-id="f878c-128">Subcategory or subgrouping to which the configuration belongs.</span></span> <span data-ttu-id="f878c-129">대부분의 경우 이는 특정 기능이나 특징을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f878c-129">In many cases, this describes specific capabilities or features.</span></span> |
| `ConfigurationImpact` | <span data-ttu-id="f878c-130">문자열</span><span class="sxs-lookup"><span data-stu-id="f878c-130">string</span></span> | <span data-ttu-id="f878c-131">구성의 등급이 전반적인 구성 점수에 미치는 영향(1-10)</span><span class="sxs-lookup"><span data-stu-id="f878c-131">Rated impact of the configuration to the overall configuration score (1-10)</span></span> |
| `IsCompliant` | <span data-ttu-id="f878c-132">부울</span><span class="sxs-lookup"><span data-stu-id="f878c-132">boolean</span></span> | <span data-ttu-id="f878c-133">구성 또는 정책이 올바르게 구성되어 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="f878c-133">Indicates whether the configuration or policy is properly configured</span></span> |

## <a name="related-topics"></a><span data-ttu-id="f878c-134">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f878c-134">Related topics</span></span>

- [<span data-ttu-id="f878c-135">사전 대응식 위협 탐지</span><span class="sxs-lookup"><span data-stu-id="f878c-135">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="f878c-136">쿼리 언어 배우기</span><span class="sxs-lookup"><span data-stu-id="f878c-136">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="f878c-137">공유 쿼리 사용</span><span class="sxs-lookup"><span data-stu-id="f878c-137">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="f878c-138">여러 장치 및 전자 메일에서 위협을 탐지</span><span class="sxs-lookup"><span data-stu-id="f878c-138">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="f878c-139">스키마의 이해</span><span class="sxs-lookup"><span data-stu-id="f878c-139">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="f878c-140">쿼리 모범 사례 적용</span><span class="sxs-lookup"><span data-stu-id="f878c-140">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="f878c-141">위협 및 취약성 관리 개요</span><span class="sxs-lookup"><span data-stu-id="f878c-141">Overview of Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)