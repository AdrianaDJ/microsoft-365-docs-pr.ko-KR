---
title: 고급 구하기 스키마의 IdentityLogonEvents 테이블
description: 고급 구하기 스키마의 IdentityLogonEvents 테이블에서 Active Directory가 기록한 인증 이벤트에 대해 자세히 알아보기
keywords: 고급 구하기, 위협 검색, 사이버 threat 사냥, microsoft threat protection, microsoft 365, mtp, m365, 검색, 쿼리, 원격 분석, 스키마 참조, kusto, table, column, IdentityLogonEvents, Azure AD, Active Directory, Azure ATP, id
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
ms.openlocfilehash: 17e12e9095219b7ad7923f7b5664946fff6ce724
ms.sourcegitcommit: ab10c042e5e9c6a7b2afef930ab0d247a6aa275d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "44899378"
---
# <a name="identitylogonevents"></a><span data-ttu-id="2370b-104">IdentityLogonEvents</span><span class="sxs-lookup"><span data-stu-id="2370b-104">IdentityLogonEvents</span></span>

<span data-ttu-id="2370b-105">**적용 대상:**</span><span class="sxs-lookup"><span data-stu-id="2370b-105">**Applies to:**</span></span>
- <span data-ttu-id="2370b-106">Microsoft 위협 방지</span><span class="sxs-lookup"><span data-stu-id="2370b-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="2370b-107">`IdentityLogonEvents` [고급 구하기](advanced-hunting-overview.md) 스키마의 표에는 Azure Active Directory 및 기타 Microsoft 클라우드 앱 및 서비스에 의해 기록 되는 인증 작업에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-107">The `IdentityLogonEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about authentication activities recorded by Azure Active Directory and other Microsoft cloud apps and services.</span></span> <span data-ttu-id="2370b-108">이 참조를 사용하여 이 표의 정보를 반환하는 쿼리를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="2370b-109">고급 헌팅 스키마의 다른 표에 대한 자세한 내용은 [고급 헌팅 참조](advanced-hunting-schema-tables.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2370b-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="2370b-110">열 이름</span><span class="sxs-lookup"><span data-stu-id="2370b-110">Column name</span></span> | <span data-ttu-id="2370b-111">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="2370b-111">Data type</span></span> | <span data-ttu-id="2370b-112">설명</span><span class="sxs-lookup"><span data-stu-id="2370b-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="2370b-113">datetime</span><span class="sxs-lookup"><span data-stu-id="2370b-113">datetime</span></span> | <span data-ttu-id="2370b-114">이벤트가 기록된 날짜와 시간</span><span class="sxs-lookup"><span data-stu-id="2370b-114">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="2370b-115">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-115">string</span></span> | <span data-ttu-id="2370b-116">이벤트를 트리거한 작업의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-116">Type of activity that triggered the event</span></span> |
| `LogonType` | <span data-ttu-id="2370b-117">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-117">string</span></span> | <span data-ttu-id="2370b-118">로그온 세션의 유형 (특히 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-118">Type of logon session, specifically:</span></span><br><br> <span data-ttu-id="2370b-119">- **대화형** -사용자가 로컬 키보드 및 화면을 사용 하 여 컴퓨터와 물리적으로 상호 작용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-119">- **Interactive** - User physically interacts with the machine using the local keyboard and screen</span></span><br><br> <span data-ttu-id="2370b-120">- **RDP (원격 대화형) 로그온** -사용자가 원격 데스크톱, 터미널 서비스, 원격 지원 또는 기타 RDP 클라이언트를 사용 하 여 원격으로 컴퓨터와 상호 작용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-120">- **Remote interactive (RDP) logons** - User interacts with the machine remotely using Remote Desktop, Terminal Services, Remote Assistance, or other RDP clients</span></span><br><br> <span data-ttu-id="2370b-121">- PsExec를 사용 하 여 컴퓨터에 액세스 하거나 프린터 및 공유 폴더와 같은 컴퓨터의 공유 리소스에 액세스 하는 경우 **네트워크** 세션이 시작 됨</span><span class="sxs-lookup"><span data-stu-id="2370b-121">- **Network** - Session initiated when the machine is accessed using PsExec or when shared resources on the machine, such as printers and shared folders, are accessed</span></span><br><br> <span data-ttu-id="2370b-122">- 예약 된 작업에 의해 시작 되는 **일괄** 세션</span><span class="sxs-lookup"><span data-stu-id="2370b-122">- **Batch** - Session initiated by scheduled tasks</span></span><br><br> <span data-ttu-id="2370b-123">- **서비스** 시작 시 서비스에 의해 시작 된 세션</span><span class="sxs-lookup"><span data-stu-id="2370b-123">- **Service** - Session initiated by services as they start</span></span> |
| `Application` | <span data-ttu-id="2370b-124">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-124">string</span></span> | <span data-ttu-id="2370b-125">기록 된 작업을 수행한 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="2370b-125">Application that performed the recorded action</span></span> |
| `Protocol` | <span data-ttu-id="2370b-126">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-126">string</span></span> | <span data-ttu-id="2370b-127">통신 중에 사용 되는 프로토콜</span><span class="sxs-lookup"><span data-stu-id="2370b-127">Protocol used during the communication</span></span> |
| `AccountName` | <span data-ttu-id="2370b-128">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-128">string</span></span> | <span data-ttu-id="2370b-129">계정의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-129">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="2370b-130">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-130">string</span></span> | <span data-ttu-id="2370b-131">계정의 도메인</span><span class="sxs-lookup"><span data-stu-id="2370b-131">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="2370b-132">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-132">string</span></span> | <span data-ttu-id="2370b-133">계정의 UPN (사용자 계정 이름)</span><span class="sxs-lookup"><span data-stu-id="2370b-133">User principal name (UPN) of the account</span></span> |
| `AccountSid` | <span data-ttu-id="2370b-134">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-134">string</span></span> | <span data-ttu-id="2370b-135">계정의 SID (보안 식별자)</span><span class="sxs-lookup"><span data-stu-id="2370b-135">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="2370b-136">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-136">string</span></span> | <span data-ttu-id="2370b-137">Azure AD의 계정에 대 한 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-137">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="2370b-138">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-138">string</span></span> | <span data-ttu-id="2370b-139">주소록에 표시 되는 계정 사용자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-139">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="2370b-140">일반적으로 주어진 이름이 나 이름, 중간 시작, 성 또는 성의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-140">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="2370b-141">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-141">string</span></span> | <span data-ttu-id="2370b-142">컴퓨터의 FQDN(정규화된 도메인 이름)</span><span class="sxs-lookup"><span data-stu-id="2370b-142">Fully qualified domain name (FQDN) of the machine</span></span> |
| `DeviceType` | <span data-ttu-id="2370b-143">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-143">string</span></span> | <span data-ttu-id="2370b-144">장치 유형</span><span class="sxs-lookup"><span data-stu-id="2370b-144">Type of device</span></span> |
| `OSPlatform` | <span data-ttu-id="2370b-145">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-145">string</span></span> | <span data-ttu-id="2370b-146">컴퓨터에서 실행 중인 운영 체제의 플랫폼</span><span class="sxs-lookup"><span data-stu-id="2370b-146">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="2370b-147">이는 Windows 10 및 Windows 7과 같이 동일한 제품군 내의 변형을 포함하여 특정 운영 체제를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2370b-147">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `IPAddress` | <span data-ttu-id="2370b-148">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-148">string</span></span> | <span data-ttu-id="2370b-149">끝점에 할당 되 고 관련 네트워크 통신 중에 사용 되는 IP 주소</span><span class="sxs-lookup"><span data-stu-id="2370b-149">IP address assigned to the endpoint and used during related network communications</span></span> |
| `Location` | <span data-ttu-id="2370b-150">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-150">string</span></span> | <span data-ttu-id="2370b-151">이벤트와 관련 된 구/군/시, 국가 또는 기타 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="2370b-151">City, country, or other geographic location associated with the event</span></span> |
| `Isp` | <span data-ttu-id="2370b-152">문자열</span><span class="sxs-lookup"><span data-stu-id="2370b-152">string</span></span> | <span data-ttu-id="2370b-153">끝점 IP 주소와 연결 된 ISP (인터넷 서비스 공급자)</span><span class="sxs-lookup"><span data-stu-id="2370b-153">Internet service provider (ISP) associated with the endpoint IP address</span></span> |

## <a name="related-topics"></a><span data-ttu-id="2370b-154">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2370b-154">Related topics</span></span>
- [<span data-ttu-id="2370b-155">고급 헌팅 개요</span><span class="sxs-lookup"><span data-stu-id="2370b-155">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="2370b-156">쿼리 언어 배우기</span><span class="sxs-lookup"><span data-stu-id="2370b-156">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="2370b-157">공유 쿼리 사용</span><span class="sxs-lookup"><span data-stu-id="2370b-157">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="2370b-158">여러 장치 및 전자 메일에서 위협을 탐지</span><span class="sxs-lookup"><span data-stu-id="2370b-158">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="2370b-159">스키마의 이해</span><span class="sxs-lookup"><span data-stu-id="2370b-159">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="2370b-160">쿼리 모범 사례 적용</span><span class="sxs-lookup"><span data-stu-id="2370b-160">Apply query best practices</span></span>](advanced-hunting-best-practices.md)