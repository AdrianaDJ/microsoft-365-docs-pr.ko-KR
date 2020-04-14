---
title: 중요 한 정보 형식을 찾습니다.
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 준비가 된 80 중요 한 정보 유형이 포함 되어 있습니다. 이 항목에서는 이러한 모든 중요한 정보 유형의 목록과 DLP 정책이 이러한 각 유형을 검색할 때 찾는 내용을 보여 줍니다.
ms.openlocfilehash: aa3a08961ccad92c9986db16c1d8180d9b0cd17e
ms.sourcegitcommit: 4ddbc1c3c29d79d3c4640b7b32f95576784efcca
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/13/2020
ms.locfileid: "43240288"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="3aed1-104">중요한 정보 형식이 찾는 항목</span><span class="sxs-lookup"><span data-stu-id="3aed1-104">What the sensitive information types look for</span></span>

<span data-ttu-id="3aed1-105">Office 365 보안 &amp; 및 준수 센터의 dlp (데이터 손실 방지)에는 dlp 정책에서 사용할 수 있는 중요 한 정보 유형이 많이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="3aed1-106">이 항목에서는 이러한 모든 중요한 정보 유형의 목록과 DLP 정책이 이러한 각 유형을 검색할 때 찾는 내용을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="3aed1-107">중요한 정보 유형은 정규식이나 함수로 식별될 수 있는 패턴으로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="3aed1-108">또한 키워드 및 체크섬과 같은 확증적인 증거를 사용하여 중요한 정보 유형을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="3aed1-109">이러한 평가 프로세스에서 신뢰 수준 및 근접성도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="3aed1-110">ABA 라우팅 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-111">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-111">Format</span></span>

<span data-ttu-id="3aed1-112">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-113">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-113">Pattern</span></span>

<span data-ttu-id="3aed1-114">서식이</span><span class="sxs-lookup"><span data-stu-id="3aed1-114">Formatted:</span></span>
- <span data-ttu-id="3aed1-115">0, 1, 2, 3, 6, 7 또는 8로 시작하는 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="3aed1-116">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-116">A hyphen</span></span>
- <span data-ttu-id="3aed1-117">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-117">Four digits</span></span>
- <span data-ttu-id="3aed1-118">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-118">A hyphen</span></span>
- <span data-ttu-id="3aed1-119">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-119">A digit</span></span>

<span data-ttu-id="3aed1-120">서식 없음: 0, 1, 2, 3, 6, 7 또는 8로 시작 하는 9 개의 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="3aed1-121">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-121">Checksum</span></span>

<span data-ttu-id="3aed1-122">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-123">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-123">Definition</span></span>

<span data-ttu-id="3aed1-124">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-125">Func_aba_routing 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-126">Keyword_ABA_Routing의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```xml
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="3aed1-127">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="3aed1-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="3aed1-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="3aed1-129">aba</span><span class="sxs-lookup"><span data-stu-id="3aed1-129">aba</span></span>
- <span data-ttu-id="3aed1-130">aba #</span><span class="sxs-lookup"><span data-stu-id="3aed1-130">aba #</span></span>
- <span data-ttu-id="3aed1-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="3aed1-131">aba routing #</span></span>
- <span data-ttu-id="3aed1-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="3aed1-132">aba routing number</span></span>
- <span data-ttu-id="3aed1-133">aba #</span><span class="sxs-lookup"><span data-stu-id="3aed1-133">aba#</span></span>
- <span data-ttu-id="3aed1-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="3aed1-134">abarouting#</span></span>
- <span data-ttu-id="3aed1-135">aba number</span><span class="sxs-lookup"><span data-stu-id="3aed1-135">aba number</span></span>
- <span data-ttu-id="3aed1-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-136">abaroutingnumber</span></span>
- <span data-ttu-id="3aed1-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="3aed1-137">american bank association routing #</span></span>
- <span data-ttu-id="3aed1-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="3aed1-138">american bank association routing number</span></span>
- <span data-ttu-id="3aed1-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="3aed1-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="3aed1-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="3aed1-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="3aed1-141">bank routing number</span></span>
- <span data-ttu-id="3aed1-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="3aed1-142">bankrouting#</span></span>
- <span data-ttu-id="3aed1-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-143">bankroutingnumber</span></span>
- <span data-ttu-id="3aed1-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="3aed1-144">routing transit number</span></span>
- <span data-ttu-id="3aed1-145">RTN</span><span class="sxs-lookup"><span data-stu-id="3aed1-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="3aed1-146">아르헨티나 국가 ID(DNI) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-147">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-147">Format</span></span>

<span data-ttu-id="3aed1-148">마침표로 구분된 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-149">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-149">Pattern</span></span>

<span data-ttu-id="3aed1-150">8자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-150">Eight digits:</span></span>
- <span data-ttu-id="3aed1-151">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-151">Two digits</span></span>
- <span data-ttu-id="3aed1-152">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-152">A period</span></span>
- <span data-ttu-id="3aed1-153">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-153">Three digits</span></span>
- <span data-ttu-id="3aed1-154">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-154">A period</span></span>
- <span data-ttu-id="3aed1-155">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-156">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-156">Checksum</span></span>

<span data-ttu-id="3aed1-157">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-158">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-158">Definition</span></span>

<span data-ttu-id="3aed1-159">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-160">정규식 Regex_argentina_national_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-161">Keyword_argentina_national_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```xml
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-162">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="3aed1-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="3aed1-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="3aed1-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="3aed1-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="3aed1-165">ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-165">Identity</span></span> 
- <span data-ttu-id="3aed1-166">식별 국가 Id 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="3aed1-167">DNI</span><span class="sxs-lookup"><span data-stu-id="3aed1-167">DNI</span></span> 
- <span data-ttu-id="3aed1-168">개인의 NIC 국내 레지스트리</span><span class="sxs-lookup"><span data-stu-id="3aed1-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="3aed1-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="3aed1-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="3aed1-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="3aed1-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="3aed1-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="3aed1-171">Identidad</span></span> 
- <span data-ttu-id="3aed1-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="3aed1-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="3aed1-173">호주 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-174">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-174">Format</span></span>

<span data-ttu-id="3aed1-175">6-10자리 숫자(은행 지점 번호 포함 또는 제외)</span><span class="sxs-lookup"><span data-stu-id="3aed1-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-176">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-176">Pattern</span></span>

<span data-ttu-id="3aed1-177">계좌 번호는 6-10자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="3aed1-178">호주 은행 지점 번호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="3aed1-179">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-179">Three digits</span></span> 
- <span data-ttu-id="3aed1-180">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-180">A hyphen</span></span> 
- <span data-ttu-id="3aed1-181">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-182">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-182">Checksum</span></span>

<span data-ttu-id="3aed1-183">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-184">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-184">Definition</span></span>

<span data-ttu-id="3aed1-185">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-186">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="3aed1-187">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="3aed1-188">Regex_australia_bank_account_number_bsb 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="3aed1-189">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-190">Regex_australia_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="3aed1-191">Keyword_australia_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```xml
<!-- Australia Bank Account Number -->
<Entity id="74a54de9-2a30-4aa0-a8aa-3d9327fc07c7" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
        <Match idRef="Regex_australia_bank_account_number_bsb" />
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
  </Pattern>
 </Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-192">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="3aed1-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="3aed1-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="3aed1-194">swift bank code</span></span>
- <span data-ttu-id="3aed1-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="3aed1-195">correspondent bank</span></span>
- <span data-ttu-id="3aed1-196">base currency</span><span class="sxs-lookup"><span data-stu-id="3aed1-196">base currency</span></span>
- <span data-ttu-id="3aed1-197">usa account</span><span class="sxs-lookup"><span data-stu-id="3aed1-197">usa account</span></span>
- <span data-ttu-id="3aed1-198">holder address</span><span class="sxs-lookup"><span data-stu-id="3aed1-198">holder address</span></span>
- <span data-ttu-id="3aed1-199">bank address</span><span class="sxs-lookup"><span data-stu-id="3aed1-199">bank address</span></span>
- <span data-ttu-id="3aed1-200">information account</span><span class="sxs-lookup"><span data-stu-id="3aed1-200">information account</span></span>
- <span data-ttu-id="3aed1-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="3aed1-201">fund transfers</span></span>
- <span data-ttu-id="3aed1-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="3aed1-202">bank charges</span></span>
- <span data-ttu-id="3aed1-203">bank details</span><span class="sxs-lookup"><span data-stu-id="3aed1-203">bank details</span></span>
- <span data-ttu-id="3aed1-204">banking information</span><span class="sxs-lookup"><span data-stu-id="3aed1-204">banking information</span></span>
- <span data-ttu-id="3aed1-205">full names</span><span class="sxs-lookup"><span data-stu-id="3aed1-205">full names</span></span>
- <span data-ttu-id="3aed1-206">iaea</span><span class="sxs-lookup"><span data-stu-id="3aed1-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="3aed1-207">호주 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-208">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-208">Format</span></span>

<span data-ttu-id="3aed1-209">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-210">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-210">Pattern</span></span>

<span data-ttu-id="3aed1-211">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="3aed1-212">2자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-213">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-213">Two digits</span></span> 
- <span data-ttu-id="3aed1-214">5자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="3aed1-215">또는</span><span class="sxs-lookup"><span data-stu-id="3aed1-215">OR</span></span>

- <span data-ttu-id="3aed1-216">1-2개의 선택적 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-217">4-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-217">4-9 digits</span></span>

<span data-ttu-id="3aed1-218">또는</span><span class="sxs-lookup"><span data-stu-id="3aed1-218">OR</span></span>

- <span data-ttu-id="3aed1-219">9자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-220">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-220">Checksum</span></span>

<span data-ttu-id="3aed1-221">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-222">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-222">Definition</span></span>

<span data-ttu-id="3aed1-223">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-224">Regex_australia_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-225">Keyword_australia_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="3aed1-226">Keyword_australia_drivers_license_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```xml
<!-- Australia Drivers License Number -->
<Entity id="1cbbc8f5-9216-4392-9eb5-5ac2298d1356" patternsProximity="300" recommendedConfidence="75">
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_drivers_license_number" />
        <Match idRef="Keyword_australia_drivers_license_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_australia_drivers_license_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-227">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="3aed1-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="3aed1-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="3aed1-229">international driving permits</span></span>
- <span data-ttu-id="3aed1-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="3aed1-230">australian automobile association</span></span>
- <span data-ttu-id="3aed1-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="3aed1-231">international driving permit</span></span>
- <span data-ttu-id="3aed1-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="3aed1-232">DriverLicence</span></span>
- <span data-ttu-id="3aed1-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="3aed1-233">DriverLicences</span></span>
- <span data-ttu-id="3aed1-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-234">Driver Lic</span></span>
- <span data-ttu-id="3aed1-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-235">Driver Licence</span></span>
- <span data-ttu-id="3aed1-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-236">Driver Licences</span></span>
- <span data-ttu-id="3aed1-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="3aed1-237">DriversLic</span></span>
- <span data-ttu-id="3aed1-238">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-238">DriversLicence</span></span>
- <span data-ttu-id="3aed1-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="3aed1-239">DriversLicences</span></span>
- <span data-ttu-id="3aed1-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-240">Drivers Lic</span></span>
- <span data-ttu-id="3aed1-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-241">Drivers Lics</span></span>
- <span data-ttu-id="3aed1-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-242">Drivers Licence</span></span>
- <span data-ttu-id="3aed1-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-243">Drivers Licences</span></span>
- <span data-ttu-id="3aed1-244">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-244">Driver'Lic</span></span>
- <span data-ttu-id="3aed1-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-245">Driver'Lics</span></span>
- <span data-ttu-id="3aed1-246">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-246">Driver'Licence</span></span>
- <span data-ttu-id="3aed1-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-247">Driver'Licences</span></span>
- <span data-ttu-id="3aed1-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-248">Driver' Lic</span></span>
- <span data-ttu-id="3aed1-249">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-249">Driver' Lics</span></span>
- <span data-ttu-id="3aed1-250">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-250">Driver' Licence</span></span>
- <span data-ttu-id="3aed1-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-251">Driver' Licences</span></span>
- <span data-ttu-id="3aed1-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="3aed1-252">Driver'sLic</span></span>
- <span data-ttu-id="3aed1-253">Drivers (Slics)</span><span class="sxs-lookup"><span data-stu-id="3aed1-253">Driver'sLics</span></span>
- <span data-ttu-id="3aed1-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="3aed1-254">Driver'sLicence</span></span>
- <span data-ttu-id="3aed1-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="3aed1-255">Driver'sLicences</span></span>
- <span data-ttu-id="3aed1-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-256">Driver's Lic</span></span>
- <span data-ttu-id="3aed1-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-257">Driver's Lics</span></span>
- <span data-ttu-id="3aed1-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-258">Driver's Licence</span></span>
- <span data-ttu-id="3aed1-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-259">Driver's Licences</span></span>
- <span data-ttu-id="3aed1-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-260">DriverLic#</span></span>
- <span data-ttu-id="3aed1-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-261">DriverLics#</span></span>
- <span data-ttu-id="3aed1-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="3aed1-262">DriverLicence#</span></span>
- <span data-ttu-id="3aed1-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="3aed1-263">DriverLicences#</span></span>
- <span data-ttu-id="3aed1-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-264">Driver Lic#</span></span>
- <span data-ttu-id="3aed1-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-265">Driver Lics#</span></span>
- <span data-ttu-id="3aed1-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="3aed1-266">Driver Licence#</span></span>
- <span data-ttu-id="3aed1-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="3aed1-267">Driver Licences#</span></span>
- <span data-ttu-id="3aed1-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-268">DriversLic#</span></span>
- <span data-ttu-id="3aed1-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-269">DriversLics#</span></span>
- <span data-ttu-id="3aed1-270">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-270">DriversLicence#</span></span>
- <span data-ttu-id="3aed1-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="3aed1-271">DriversLicences#</span></span>
- <span data-ttu-id="3aed1-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-272">Drivers Lic#</span></span>
- <span data-ttu-id="3aed1-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-273">Drivers Lics#</span></span>
- <span data-ttu-id="3aed1-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="3aed1-274">Drivers Licence#</span></span>
- <span data-ttu-id="3aed1-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="3aed1-275">Drivers Licences#</span></span>
- <span data-ttu-id="3aed1-276">Driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-276">Driver'Lic#</span></span>
- <span data-ttu-id="3aed1-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-277">Driver'Lics#</span></span>
- <span data-ttu-id="3aed1-278">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-278">Driver'Licence#</span></span>
- <span data-ttu-id="3aed1-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="3aed1-279">Driver'Licences#</span></span>
- <span data-ttu-id="3aed1-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-280">Driver' Lic#</span></span>
- <span data-ttu-id="3aed1-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-281">Driver' Lics#</span></span>
- <span data-ttu-id="3aed1-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="3aed1-282">Driver' Licence#</span></span>
- <span data-ttu-id="3aed1-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="3aed1-283">Driver' Licences#</span></span>
- <span data-ttu-id="3aed1-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-284">Driver'sLic#</span></span>
- <span data-ttu-id="3aed1-285">Drivers (Slics) #</span><span class="sxs-lookup"><span data-stu-id="3aed1-285">Driver'sLics#</span></span>
- <span data-ttu-id="3aed1-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="3aed1-286">Driver'sLicence#</span></span>
- <span data-ttu-id="3aed1-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="3aed1-287">Driver'sLicences#</span></span>
- <span data-ttu-id="3aed1-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-288">Driver's Lic#</span></span>
- <span data-ttu-id="3aed1-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-289">Driver's Lics#</span></span>
- <span data-ttu-id="3aed1-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="3aed1-290">Driver's Licence#</span></span>
- <span data-ttu-id="3aed1-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="3aed1-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="3aed1-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="3aed1-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="3aed1-293">aaa</span><span class="sxs-lookup"><span data-stu-id="3aed1-293">aaa</span></span>
- <span data-ttu-id="3aed1-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="3aed1-294">DriverLicense</span></span>
- <span data-ttu-id="3aed1-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-295">DriverLicenses</span></span>
- <span data-ttu-id="3aed1-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="3aed1-296">Driver License</span></span>
- <span data-ttu-id="3aed1-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-297">Driver Licenses</span></span>
- <span data-ttu-id="3aed1-298">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-298">DriversLicense</span></span>
- <span data-ttu-id="3aed1-299">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-299">DriversLicenses</span></span>
- <span data-ttu-id="3aed1-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="3aed1-300">Drivers License</span></span>
- <span data-ttu-id="3aed1-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-301">Drivers Licenses</span></span>
- <span data-ttu-id="3aed1-302">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-302">Driver'License</span></span>
- <span data-ttu-id="3aed1-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-303">Driver'Licenses</span></span>
- <span data-ttu-id="3aed1-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="3aed1-304">Driver' License</span></span>
- <span data-ttu-id="3aed1-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-305">Driver' Licenses</span></span>
- <span data-ttu-id="3aed1-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="3aed1-306">Driver'sLicense</span></span>
- <span data-ttu-id="3aed1-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-307">Driver'sLicenses</span></span>
- <span data-ttu-id="3aed1-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="3aed1-308">Driver's License</span></span>
- <span data-ttu-id="3aed1-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-309">Driver's Licenses</span></span>
- <span data-ttu-id="3aed1-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="3aed1-310">DriverLicense#</span></span>
- <span data-ttu-id="3aed1-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="3aed1-311">DriverLicenses#</span></span>
- <span data-ttu-id="3aed1-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-312">Driver License#</span></span>
- <span data-ttu-id="3aed1-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-313">Driver Licenses#</span></span>
- <span data-ttu-id="3aed1-314">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-314">DriversLicense#</span></span>
- <span data-ttu-id="3aed1-315">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-315">DriversLicenses#</span></span>
- <span data-ttu-id="3aed1-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-316">Drivers License#</span></span>
- <span data-ttu-id="3aed1-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-317">Drivers Licenses#</span></span>
- <span data-ttu-id="3aed1-318">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-318">Driver'License#</span></span>
- <span data-ttu-id="3aed1-319">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="3aed1-319">Driver'Licenses#</span></span>
- <span data-ttu-id="3aed1-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-320">Driver' License#</span></span>
- <span data-ttu-id="3aed1-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-321">Driver' Licenses#</span></span>
- <span data-ttu-id="3aed1-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="3aed1-322">Driver'sLicense#</span></span>
- <span data-ttu-id="3aed1-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="3aed1-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="3aed1-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-324">Driver's License#</span></span>
- <span data-ttu-id="3aed1-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="3aed1-326">호주 의료 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-327">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-327">Format</span></span>

<span data-ttu-id="3aed1-328">10-11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-329">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-329">Pattern</span></span>

<span data-ttu-id="3aed1-330">10-11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-330">10-11 digits:</span></span>
- <span data-ttu-id="3aed1-331">첫 번째 숫자는 2-6 범위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="3aed1-332">9번째 숫자는 검사 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="3aed1-333">10번째 숫자는 문제 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="3aed1-334">11번째 숫자(선택 사항)는 개인 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-335">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-335">Checksum</span></span>

<span data-ttu-id="3aed1-336">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-337">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-337">Definition</span></span>

<span data-ttu-id="3aed1-338">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-339">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-340">Keyword_Australia_Medical_Account_Number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="3aed1-341">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-341">The checksum passes.</span></span>

<span data-ttu-id="3aed1-342">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-343">Func_australian_medical_account_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-344">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-344">The checksum passes.</span></span>

```xml
  <!-- Australia Medical Account Number -->
<Entity id="104a99a0-3d3b-4542-a40d-ab0b9e1efe63" recommendedConfidence="85" patternsProximity="300">
    <Pattern confidenceLevel="95">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="1">
     <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
<Pattern confidenceLevel="85">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="0" maxMatches="0">
  <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-345">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="3aed1-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="3aed1-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="3aed1-347">bank account details</span></span>
- <span data-ttu-id="3aed1-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="3aed1-348">medicare payments</span></span>
- <span data-ttu-id="3aed1-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="3aed1-349">mortgage account</span></span>
- <span data-ttu-id="3aed1-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="3aed1-350">bank payments</span></span>
- <span data-ttu-id="3aed1-351">information branch</span><span class="sxs-lookup"><span data-stu-id="3aed1-351">information branch</span></span>
- <span data-ttu-id="3aed1-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="3aed1-352">credit card loan</span></span>
- <span data-ttu-id="3aed1-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="3aed1-353">department of human services</span></span>
- <span data-ttu-id="3aed1-354">local service</span><span class="sxs-lookup"><span data-stu-id="3aed1-354">local service</span></span>
- <span data-ttu-id="3aed1-355">medicare</span><span class="sxs-lookup"><span data-stu-id="3aed1-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="3aed1-356">호주 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-357">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-357">Format</span></span>

<span data-ttu-id="3aed1-358">문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-359">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-359">Pattern</span></span>

<span data-ttu-id="3aed1-360">1개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-361">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-361">Checksum</span></span>

<span data-ttu-id="3aed1-362">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-363">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-363">Definition</span></span>

<span data-ttu-id="3aed1-364">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-365">Regex_australia_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-366">Keyword_passport 또는 Keyword_australia_passport_number의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```xml
<!-- Australia Passport Number -->
<Entity id="29869db6-602d-4853-ab93-3484f905df50" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_australia_passport_number" />
        </Any>
   </Pattern>
</Entity>   
```

### <a name="keywords"></a><span data-ttu-id="3aed1-367">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="3aed1-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-368">Keyword_passport</span></span>

- <span data-ttu-id="3aed1-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-369">Passport Number</span></span>
- <span data-ttu-id="3aed1-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="3aed1-370">Passport No</span></span>
- <span data-ttu-id="3aed1-371">Passport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-371">Passport #</span></span>
- <span data-ttu-id="3aed1-372">여권 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-372">Passport#</span></span>
- <span data-ttu-id="3aed1-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="3aed1-373">PassportID</span></span>
- <span data-ttu-id="3aed1-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="3aed1-374">Passportno</span></span>
- <span data-ttu-id="3aed1-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-375">passportnumber</span></span>
- <span data-ttu-id="3aed1-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="3aed1-376">パスポート</span></span>
- <span data-ttu-id="3aed1-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-377">パスポート番号</span></span>
- <span data-ttu-id="3aed1-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="3aed1-378">パスポートのNum</span></span>
- <span data-ttu-id="3aed1-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-379">パスポート ＃</span></span> 
- <span data-ttu-id="3aed1-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="3aed1-380">Numéro de passeport</span></span>
- <span data-ttu-id="3aed1-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="3aed1-381">Passeport n °</span></span>
- <span data-ttu-id="3aed1-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="3aed1-382">Passeport Non</span></span>
- <span data-ttu-id="3aed1-383">Passeport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-383">Passeport #</span></span>
- <span data-ttu-id="3aed1-384">포트 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-384">Passeport#</span></span>
- <span data-ttu-id="3aed1-385">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="3aed1-385">PasseportNon</span></span>
- <span data-ttu-id="3aed1-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="3aed1-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="3aed1-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="3aed1-388">여권</span><span class="sxs-lookup"><span data-stu-id="3aed1-388">passport</span></span>
- <span data-ttu-id="3aed1-389">passport details</span><span class="sxs-lookup"><span data-stu-id="3aed1-389">passport details</span></span>
- <span data-ttu-id="3aed1-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="3aed1-390">immigration and citizenship</span></span>
- <span data-ttu-id="3aed1-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="3aed1-391">commonwealth of australia</span></span>
- <span data-ttu-id="3aed1-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="3aed1-392">department of immigration</span></span>
- <span data-ttu-id="3aed1-393">residential address</span><span class="sxs-lookup"><span data-stu-id="3aed1-393">residential address</span></span>
- <span data-ttu-id="3aed1-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="3aed1-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="3aed1-395">visa</span><span class="sxs-lookup"><span data-stu-id="3aed1-395">visa</span></span>
- <span data-ttu-id="3aed1-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="3aed1-396">national identity card</span></span>
- <span data-ttu-id="3aed1-397">passport number</span><span class="sxs-lookup"><span data-stu-id="3aed1-397">passport number</span></span>
- <span data-ttu-id="3aed1-398">travel document</span><span class="sxs-lookup"><span data-stu-id="3aed1-398">travel document</span></span>
- <span data-ttu-id="3aed1-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="3aed1-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="3aed1-400">호주 세금 파일 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-401">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-401">Format</span></span>

<span data-ttu-id="3aed1-402">8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-403">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-403">Pattern</span></span>

<span data-ttu-id="3aed1-404">일반적으로 다음과 같이 공백과 함께 표시되는 8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="3aed1-405">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-405">Three digits</span></span> 
- <span data-ttu-id="3aed1-406">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-406">An optional space</span></span> 
- <span data-ttu-id="3aed1-407">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-407">Three digits</span></span> 
- <span data-ttu-id="3aed1-408">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-408">An optional space</span></span> 
- <span data-ttu-id="3aed1-409">마지막 숫자가 검사 숫자인 2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-410">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-410">Checksum</span></span>

<span data-ttu-id="3aed1-411">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-412">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-412">Definition</span></span>

<span data-ttu-id="3aed1-413">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-414">Func_australian_tax_file_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-415">Keyword_Australia_Tax_File_Number 또는 Keyword_number_exclusions의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="3aed1-416">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-416">The checksum passes.</span></span>

```xml
   <!-- Australia Tax File Number -->
    <Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Match idRef="Keyword_Australia_Tax_File_Number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_number_exclusions" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-417">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="3aed1-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="3aed1-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="3aed1-419">australian business number</span></span>
- <span data-ttu-id="3aed1-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="3aed1-420">marginal tax rate</span></span>
- <span data-ttu-id="3aed1-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="3aed1-421">medicare levy</span></span>
- <span data-ttu-id="3aed1-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="3aed1-422">portfolio number</span></span>
- <span data-ttu-id="3aed1-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="3aed1-423">service veterans</span></span>
- <span data-ttu-id="3aed1-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="3aed1-424">withholding tax</span></span>
- <span data-ttu-id="3aed1-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="3aed1-425">individual tax return</span></span>
- <span data-ttu-id="3aed1-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="3aed1-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="3aed1-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="3aed1-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="3aed1-428">00000000</span><span class="sxs-lookup"><span data-stu-id="3aed1-428">00000000</span></span>
- <span data-ttu-id="3aed1-429">11111111</span><span class="sxs-lookup"><span data-stu-id="3aed1-429">11111111</span></span>
- <span data-ttu-id="3aed1-430">22222222</span><span class="sxs-lookup"><span data-stu-id="3aed1-430">22222222</span></span>
- <span data-ttu-id="3aed1-431">33333333</span><span class="sxs-lookup"><span data-stu-id="3aed1-431">33333333</span></span>
- <span data-ttu-id="3aed1-432">44444444</span><span class="sxs-lookup"><span data-stu-id="3aed1-432">44444444</span></span>
- <span data-ttu-id="3aed1-433">55555555</span><span class="sxs-lookup"><span data-stu-id="3aed1-433">55555555</span></span>
- <span data-ttu-id="3aed1-434">66666666</span><span class="sxs-lookup"><span data-stu-id="3aed1-434">66666666</span></span>
- <span data-ttu-id="3aed1-435">77777777</span><span class="sxs-lookup"><span data-stu-id="3aed1-435">77777777</span></span>
- <span data-ttu-id="3aed1-436">88888888</span><span class="sxs-lookup"><span data-stu-id="3aed1-436">88888888</span></span>
- <span data-ttu-id="3aed1-437">99999999</span><span class="sxs-lookup"><span data-stu-id="3aed1-437">99999999</span></span>
- <span data-ttu-id="3aed1-438">000000000</span><span class="sxs-lookup"><span data-stu-id="3aed1-438">000000000</span></span>
- <span data-ttu-id="3aed1-439">111111111</span><span class="sxs-lookup"><span data-stu-id="3aed1-439">111111111</span></span>
- <span data-ttu-id="3aed1-440">222222222</span><span class="sxs-lookup"><span data-stu-id="3aed1-440">222222222</span></span>
- <span data-ttu-id="3aed1-441">333333333</span><span class="sxs-lookup"><span data-stu-id="3aed1-441">333333333</span></span>
- <span data-ttu-id="3aed1-442">444444444</span><span class="sxs-lookup"><span data-stu-id="3aed1-442">444444444</span></span>
- <span data-ttu-id="3aed1-443">555555555</span><span class="sxs-lookup"><span data-stu-id="3aed1-443">555555555</span></span>
- <span data-ttu-id="3aed1-444">666666666</span><span class="sxs-lookup"><span data-stu-id="3aed1-444">666666666</span></span>
- <span data-ttu-id="3aed1-445">777777777</span><span class="sxs-lookup"><span data-stu-id="3aed1-445">777777777</span></span>
- <span data-ttu-id="3aed1-446">888888888</span><span class="sxs-lookup"><span data-stu-id="3aed1-446">888888888</span></span>
- <span data-ttu-id="3aed1-447">999999999</span><span class="sxs-lookup"><span data-stu-id="3aed1-447">999999999</span></span>
- <span data-ttu-id="3aed1-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="3aed1-448">0000000000</span></span>
- <span data-ttu-id="3aed1-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="3aed1-449">1111111111</span></span>
- <span data-ttu-id="3aed1-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="3aed1-450">2222222222</span></span>
- <span data-ttu-id="3aed1-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="3aed1-451">3333333333</span></span>
- <span data-ttu-id="3aed1-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="3aed1-452">4444444444</span></span>
- <span data-ttu-id="3aed1-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="3aed1-453">5555555555</span></span>
- <span data-ttu-id="3aed1-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="3aed1-454">6666666666</span></span>
- <span data-ttu-id="3aed1-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="3aed1-455">7777777777</span></span>
- <span data-ttu-id="3aed1-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="3aed1-456">8888888888</span></span>
- <span data-ttu-id="3aed1-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="3aed1-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="3aed1-458">Azure DocumentDB 인증 키</span><span class="sxs-lookup"><span data-stu-id="3aed1-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-459">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-459">Format</span></span>

<span data-ttu-id="3aed1-460">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "DocumentDb" 문자열</span><span class="sxs-lookup"><span data-stu-id="3aed1-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-461">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-461">Pattern</span></span>

- <span data-ttu-id="3aed1-462">"DocumentDb" 문자열</span><span class="sxs-lookup"><span data-stu-id="3aed1-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="3aed1-463">3-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-464">보다 큼 기호 (>), 등호 (=), 따옴표 (") 또는 아포스트로피 (')</span><span class="sxs-lookup"><span data-stu-id="3aed1-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="3aed1-465">86의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="3aed1-466">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-467">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-467">Checksum</span></span>

<span data-ttu-id="3aed1-468">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-469">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-469">Definition</span></span>

<span data-ttu-id="3aed1-470">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-471">정규식 CEP_Regex_AzureDocumentDBAuthKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-472">정규식 CEP_CommonExampleKeywords에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!-- Azure Document DB Auth Key -->
<Entity id="0f587d92-eb28-44a9-bd1c-90f2892b47aa" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureDocumentDBAuthKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
          </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-473">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="3aed1-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="3aed1-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="3aed1-475">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-476">극동</span><span class="sxs-lookup"><span data-stu-id="3aed1-476">contoso</span></span>
- <span data-ttu-id="3aed1-477">fabrikam</span><span class="sxs-lookup"><span data-stu-id="3aed1-477">fabrikam</span></span>
- <span data-ttu-id="3aed1-478">대양</span><span class="sxs-lookup"><span data-stu-id="3aed1-478">northwind</span></span>
- <span data-ttu-id="3aed1-479">샌드박스</span><span class="sxs-lookup"><span data-stu-id="3aed1-479">sandbox</span></span>
- <span data-ttu-id="3aed1-480">용 onebox</span><span class="sxs-lookup"><span data-stu-id="3aed1-480">onebox</span></span>
- <span data-ttu-id="3aed1-481">로컬</span><span class="sxs-lookup"><span data-stu-id="3aed1-481">localhost</span></span>
- <span data-ttu-id="3aed1-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="3aed1-482">127.0.0.1</span></span>
- <span data-ttu-id="3aed1-483">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-484">ccw</span><span class="sxs-lookup"><span data-stu-id="3aed1-484">com</span></span>
- <span data-ttu-id="3aed1-485">s-int</span><span class="sxs-lookup"><span data-stu-id="3aed1-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-486">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="3aed1-487">Azure IAAS 데이터베이스 연결 문자열 및 Azure SQL 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="3aed1-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-488">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-488">Format</span></span>

<span data-ttu-id="3aed1-489">"Server", "server" 또는 "data source" 라는 문자열은 "cloudapp. azure"를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-490">com "또는" cloudapp.</span><span class="sxs-lookup"><span data-stu-id="3aed1-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-491">net "또는" 데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="3aed1-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-492">net "과 문자열" Password "또는" password "또는" pwd "가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-493">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-493">Pattern</span></span>

- <span data-ttu-id="3aed1-494">문자열 "Server", "Server" 또는 "data source"</span><span class="sxs-lookup"><span data-stu-id="3aed1-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="3aed1-495">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-496">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-496">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-497">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-498">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-499">문자열 "cloudapp.</span><span class="sxs-lookup"><span data-stu-id="3aed1-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-500">com "," cloudapp.</span><span class="sxs-lookup"><span data-stu-id="3aed1-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-501">net "또는" database.</span><span class="sxs-lookup"><span data-stu-id="3aed1-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-502">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-502">net"</span></span>
- <span data-ttu-id="3aed1-503">1-300에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-504">문자열 "Password", "password" 또는 "pwd"</span><span class="sxs-lookup"><span data-stu-id="3aed1-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="3aed1-505">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-506">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-506">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-507">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-508">세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')가 아닌 하나 이상의 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="3aed1-509">세미콜론 (;), 따옴표 (") 또는 아포스트로피 (')</span><span class="sxs-lookup"><span data-stu-id="3aed1-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-510">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-510">Checksum</span></span>

<span data-ttu-id="3aed1-511">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-512">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-512">Definition</span></span>

<span data-ttu-id="3aed1-513">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-514">정규식 CEP_Regex_AzureConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-515">정규식 CEP_CommonExampleKeywords에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure IAAS Database Connection String and Azure SQL Connection String-->
<Entity id="ce1a126d-186f-4700-8c0c-486157b953fd" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-516">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="3aed1-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="3aed1-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="3aed1-518">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-519">극동</span><span class="sxs-lookup"><span data-stu-id="3aed1-519">contoso</span></span>
- <span data-ttu-id="3aed1-520">fabrikam</span><span class="sxs-lookup"><span data-stu-id="3aed1-520">fabrikam</span></span>
- <span data-ttu-id="3aed1-521">대양</span><span class="sxs-lookup"><span data-stu-id="3aed1-521">northwind</span></span>
- <span data-ttu-id="3aed1-522">샌드박스</span><span class="sxs-lookup"><span data-stu-id="3aed1-522">sandbox</span></span>
- <span data-ttu-id="3aed1-523">용 onebox</span><span class="sxs-lookup"><span data-stu-id="3aed1-523">onebox</span></span>
- <span data-ttu-id="3aed1-524">로컬</span><span class="sxs-lookup"><span data-stu-id="3aed1-524">localhost</span></span>
- <span data-ttu-id="3aed1-525">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="3aed1-525">127.0.0.1</span></span>
- <span data-ttu-id="3aed1-526">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-527">ccw</span><span class="sxs-lookup"><span data-stu-id="3aed1-527">com</span></span>
- <span data-ttu-id="3aed1-528">s-int</span><span class="sxs-lookup"><span data-stu-id="3aed1-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-529">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="3aed1-530">Azure IoT Connection 문자열</span><span class="sxs-lookup"><span data-stu-id="3aed1-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-531">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-531">Format</span></span>

<span data-ttu-id="3aed1-532">문자열 "HostName" 뒤에 "azure-devices" 라는 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-533">net "및" SharedAccessKey "</span><span class="sxs-lookup"><span data-stu-id="3aed1-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-534">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-534">Pattern</span></span>

- <span data-ttu-id="3aed1-535">문자열 "HostName"</span><span class="sxs-lookup"><span data-stu-id="3aed1-535">The string "HostName"</span></span>
- <span data-ttu-id="3aed1-536">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-537">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-537">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-538">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-539">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-540">문자열 "azure-장치</span><span class="sxs-lookup"><span data-stu-id="3aed1-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-541">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-541">net"</span></span>
- <span data-ttu-id="3aed1-542">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-543">"SharedAccessKey" 문자열</span><span class="sxs-lookup"><span data-stu-id="3aed1-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="3aed1-544">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-545">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-545">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-546">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-547">43의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="3aed1-548">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-549">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-549">Checksum</span></span>

<span data-ttu-id="3aed1-550">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-551">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-551">Definition</span></span>

<span data-ttu-id="3aed1-552">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-553">정규식 CEP_Regex_AzureIoTConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-554">정규식 CEP_CommonExampleKeywords에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure IoT Connection String-->
<Entity id="0b34bec3-d5d6-4974-b7b0-dcdb5c90c29d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureIoTConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-555">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="3aed1-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="3aed1-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="3aed1-557">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-558">극동</span><span class="sxs-lookup"><span data-stu-id="3aed1-558">contoso</span></span>
- <span data-ttu-id="3aed1-559">fabrikam</span><span class="sxs-lookup"><span data-stu-id="3aed1-559">fabrikam</span></span>
- <span data-ttu-id="3aed1-560">대양</span><span class="sxs-lookup"><span data-stu-id="3aed1-560">northwind</span></span>
- <span data-ttu-id="3aed1-561">샌드박스</span><span class="sxs-lookup"><span data-stu-id="3aed1-561">sandbox</span></span>
- <span data-ttu-id="3aed1-562">용 onebox</span><span class="sxs-lookup"><span data-stu-id="3aed1-562">onebox</span></span>
- <span data-ttu-id="3aed1-563">로컬</span><span class="sxs-lookup"><span data-stu-id="3aed1-563">localhost</span></span>
- <span data-ttu-id="3aed1-564">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="3aed1-564">127.0.0.1</span></span>
- <span data-ttu-id="3aed1-565">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-566">ccw</span><span class="sxs-lookup"><span data-stu-id="3aed1-566">com</span></span>
- <span data-ttu-id="3aed1-567">s-int</span><span class="sxs-lookup"><span data-stu-id="3aed1-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-568">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="3aed1-569">Azure 게시 설정 암호</span><span class="sxs-lookup"><span data-stu-id="3aed1-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-570">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-570">Format</span></span>

<span data-ttu-id="3aed1-571">문자열 "userpwd =" 다음에 영숫자 문자열이 나옵니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-572">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-572">Pattern</span></span>

- <span data-ttu-id="3aed1-573">문자열 "userpwd ="</span><span class="sxs-lookup"><span data-stu-id="3aed1-573">The string "userpwd="</span></span>
- <span data-ttu-id="3aed1-574">60 대 문자와 숫자의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="3aed1-575">큰따옴표 (")</span><span class="sxs-lookup"><span data-stu-id="3aed1-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-576">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-576">Checksum</span></span>

<span data-ttu-id="3aed1-577">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-578">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-578">Definition</span></span>

<span data-ttu-id="3aed1-579">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-580">정규식 CEP_Regex_AzurePublishSettingPasswords 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-581">정규식 CEP_CommonExampleKeywords에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```xml
<!--Azure Publish Setting Password-->
<Entity id="75f4cc8a-a68e-49e5-89ce-fa8f03d286a5" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="CEP_Regex_AzurePublishSettingPasswords" />
       <Any minMatches="0" maxMatches="0">
           <Match idRef="CEP_CommonExampleKeywords" />
       </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-582">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="3aed1-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="3aed1-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="3aed1-584">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-585">극동</span><span class="sxs-lookup"><span data-stu-id="3aed1-585">contoso</span></span>
- <span data-ttu-id="3aed1-586">fabrikam</span><span class="sxs-lookup"><span data-stu-id="3aed1-586">fabrikam</span></span>
- <span data-ttu-id="3aed1-587">대양</span><span class="sxs-lookup"><span data-stu-id="3aed1-587">northwind</span></span>
- <span data-ttu-id="3aed1-588">샌드박스</span><span class="sxs-lookup"><span data-stu-id="3aed1-588">sandbox</span></span>
- <span data-ttu-id="3aed1-589">용 onebox</span><span class="sxs-lookup"><span data-stu-id="3aed1-589">onebox</span></span>
- <span data-ttu-id="3aed1-590">로컬</span><span class="sxs-lookup"><span data-stu-id="3aed1-590">localhost</span></span>
- <span data-ttu-id="3aed1-591">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="3aed1-591">127.0.0.1</span></span>
- <span data-ttu-id="3aed1-592">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-593">ccw</span><span class="sxs-lookup"><span data-stu-id="3aed1-593">com</span></span>
- <span data-ttu-id="3aed1-594">s-int</span><span class="sxs-lookup"><span data-stu-id="3aed1-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-595">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="3aed1-596">Azure Redis 캐시 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="3aed1-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-597">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-597">Format</span></span>

<span data-ttu-id="3aed1-598">문자열 "redis.</span><span class="sxs-lookup"><span data-stu-id="3aed1-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-599">net "문자열" password "또는" pwd "를 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-600">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-600">Pattern</span></span>

- <span data-ttu-id="3aed1-601">문자열 "redis.</span><span class="sxs-lookup"><span data-stu-id="3aed1-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-602">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-602">net"</span></span>
- <span data-ttu-id="3aed1-603">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-604">문자열 "password" 또는 "pwd"</span><span class="sxs-lookup"><span data-stu-id="3aed1-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="3aed1-605">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-606">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-606">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-607">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-608">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="3aed1-609">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-610">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-610">Checksum</span></span>

<span data-ttu-id="3aed1-611">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-612">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-612">Definition</span></span>

<span data-ttu-id="3aed1-613">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-614">정규식 CEP_Regex_AzureRedisCacheConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="3aed1-615">정규식 CEP_CommonExampleKeywords에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure Redis Cache Connection String-->
<Entity id="095a7e6c-efd8-46d5-af7b-5298d53a49fc" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureRedisCacheConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-616">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="3aed1-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="3aed1-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="3aed1-618">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-619">극동</span><span class="sxs-lookup"><span data-stu-id="3aed1-619">contoso</span></span>
- <span data-ttu-id="3aed1-620">fabrikam</span><span class="sxs-lookup"><span data-stu-id="3aed1-620">fabrikam</span></span>
- <span data-ttu-id="3aed1-621">대양</span><span class="sxs-lookup"><span data-stu-id="3aed1-621">northwind</span></span>
- <span data-ttu-id="3aed1-622">샌드박스</span><span class="sxs-lookup"><span data-stu-id="3aed1-622">sandbox</span></span>
- <span data-ttu-id="3aed1-623">용 onebox</span><span class="sxs-lookup"><span data-stu-id="3aed1-623">onebox</span></span>
- <span data-ttu-id="3aed1-624">로컬</span><span class="sxs-lookup"><span data-stu-id="3aed1-624">localhost</span></span>
- <span data-ttu-id="3aed1-625">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="3aed1-625">127.0.0.1</span></span>
- <span data-ttu-id="3aed1-626">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-627">ccw</span><span class="sxs-lookup"><span data-stu-id="3aed1-627">com</span></span>
- <span data-ttu-id="3aed1-628">s-int</span><span class="sxs-lookup"><span data-stu-id="3aed1-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-629">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="3aed1-630">Azure SAS</span><span class="sxs-lookup"><span data-stu-id="3aed1-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-631">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-631">Format</span></span>

<span data-ttu-id="3aed1-632">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 문자열 "sig"</span><span class="sxs-lookup"><span data-stu-id="3aed1-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-633">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-633">Pattern</span></span>

- <span data-ttu-id="3aed1-634">문자열 "sig"</span><span class="sxs-lookup"><span data-stu-id="3aed1-634">The string "sig"</span></span>
- <span data-ttu-id="3aed1-635">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-636">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-636">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-637">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-638">대/소문자, 숫자 또는 백분율 기호 (%)가 43-53 자 사이의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="3aed1-639">문자열 "% 3d"</span><span class="sxs-lookup"><span data-stu-id="3aed1-639">The string "%3d"</span></span>
- <span data-ttu-id="3aed1-640">소문자 또는 대문자, 숫자 또는 백분율 기호 (%)가 아닌 모든 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-641">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-641">Checksum</span></span>

<span data-ttu-id="3aed1-642">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-643">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-643">Definition</span></span>

<span data-ttu-id="3aed1-644">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-645">정규식 CEP_Regex_AzureSAS 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```xml
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="3aed1-646">Azure Service Bus 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="3aed1-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-647">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-647">Format</span></span>

<span data-ttu-id="3aed1-648">문자열 "끝점" 뒤에 "servicebus" 라는 문자열을 포함 하 여 아래 패턴에 나와 있는 문자 및 문자열이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-649">net "및" SharedAccesKey "을 차례로 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-650">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-650">Pattern</span></span>

- <span data-ttu-id="3aed1-651">문자열 "끝점"</span><span class="sxs-lookup"><span data-stu-id="3aed1-651">The string "EndPoint"</span></span>
- <span data-ttu-id="3aed1-652">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-653">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-653">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-654">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-655">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-656">문자열 "servicebus.</span><span class="sxs-lookup"><span data-stu-id="3aed1-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-657">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-657">net"</span></span>
- <span data-ttu-id="3aed1-658">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-659">"SharedAccessKey" 문자열</span><span class="sxs-lookup"><span data-stu-id="3aed1-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="3aed1-660">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-661">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-661">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-662">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-663">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 43 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="3aed1-664">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-665">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-665">Checksum</span></span>

<span data-ttu-id="3aed1-666">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-667">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-667">Definition</span></span>

<span data-ttu-id="3aed1-668">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-669">정규식 CEP_Regex_AzureServiceBusConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="3aed1-670">정규식 CEP_CommonExampleKeywords에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure Service Bus Connection String-->
<Entity id="b9a6578f-a83f-4fcd-bf44-2130bae49a6f" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureServiceBusConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-671">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="3aed1-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="3aed1-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="3aed1-673">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-674">극동</span><span class="sxs-lookup"><span data-stu-id="3aed1-674">contoso</span></span>
- <span data-ttu-id="3aed1-675">fabrikam</span><span class="sxs-lookup"><span data-stu-id="3aed1-675">fabrikam</span></span>
- <span data-ttu-id="3aed1-676">대양</span><span class="sxs-lookup"><span data-stu-id="3aed1-676">northwind</span></span>
- <span data-ttu-id="3aed1-677">샌드박스</span><span class="sxs-lookup"><span data-stu-id="3aed1-677">sandbox</span></span>
- <span data-ttu-id="3aed1-678">용 onebox</span><span class="sxs-lookup"><span data-stu-id="3aed1-678">onebox</span></span>
- <span data-ttu-id="3aed1-679">로컬</span><span class="sxs-lookup"><span data-stu-id="3aed1-679">localhost</span></span>
- <span data-ttu-id="3aed1-680">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="3aed1-680">127.0.0.1</span></span>
- <span data-ttu-id="3aed1-681">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-682">ccw</span><span class="sxs-lookup"><span data-stu-id="3aed1-682">com</span></span>
- <span data-ttu-id="3aed1-683">s-int</span><span class="sxs-lookup"><span data-stu-id="3aed1-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-684">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="3aed1-685">Azure 저장소 계정 키</span><span class="sxs-lookup"><span data-stu-id="3aed1-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-686">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-686">Format</span></span>

<span data-ttu-id="3aed1-687">"DefaultEndpointsProtocol" 문자열은 "AccountKey" 문자열을 포함 하 여 아래 패턴에 설명 된 문자 및 문자열을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-688">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-688">Pattern</span></span>

- <span data-ttu-id="3aed1-689">문자열 "DefaultEndpointsProtocol"</span><span class="sxs-lookup"><span data-stu-id="3aed1-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="3aed1-690">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-691">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-691">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-692">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-693">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-694">문자열 "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="3aed1-694">The string "AccountKey"</span></span>
- <span data-ttu-id="3aed1-695">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-696">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-696">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-697">0-2 공백 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="3aed1-698">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="3aed1-699">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-700">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-700">Checksum</span></span>

<span data-ttu-id="3aed1-701">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-702">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-702">Definition</span></span>

<span data-ttu-id="3aed1-703">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-704">정규식 CEP_Regex_AzureStorageAccountKey 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-705">정규식 CEP_AzureEmulatorStorageAccountFilter에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-706">정규식 CEP_CommonExampleKeywords에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
<!--Azure Storage Account Key-->
<Entity id="c7bc98e8-551a-4c35-a92d-d2c8cda714a7" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_AzureEmulatorStorageAccountFilter" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-707">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="3aed1-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="3aed1-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="3aed1-709">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="3aed1-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="3aed1-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="3aed1-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="3aed1-712">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-713">극동</span><span class="sxs-lookup"><span data-stu-id="3aed1-713">contoso</span></span>
- <span data-ttu-id="3aed1-714">fabrikam</span><span class="sxs-lookup"><span data-stu-id="3aed1-714">fabrikam</span></span>
- <span data-ttu-id="3aed1-715">대양</span><span class="sxs-lookup"><span data-stu-id="3aed1-715">northwind</span></span>
- <span data-ttu-id="3aed1-716">샌드박스</span><span class="sxs-lookup"><span data-stu-id="3aed1-716">sandbox</span></span>
- <span data-ttu-id="3aed1-717">용 onebox</span><span class="sxs-lookup"><span data-stu-id="3aed1-717">onebox</span></span>
- <span data-ttu-id="3aed1-718">로컬</span><span class="sxs-lookup"><span data-stu-id="3aed1-718">localhost</span></span>
- <span data-ttu-id="3aed1-719">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="3aed1-719">127.0.0.1</span></span>
- <span data-ttu-id="3aed1-720">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-721">ccw</span><span class="sxs-lookup"><span data-stu-id="3aed1-721">com</span></span>
- <span data-ttu-id="3aed1-722">s-int</span><span class="sxs-lookup"><span data-stu-id="3aed1-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-723">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="3aed1-724">Azure 저장소 계정 키 (일반)</span><span class="sxs-lookup"><span data-stu-id="3aed1-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-725">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-725">Format</span></span>

<span data-ttu-id="3aed1-726">아래 패턴에 윤곽선이 있는 문자 앞 이나 뒤에 오는 86 문자의 대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-727">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-727">Pattern</span></span>

- <span data-ttu-id="3aed1-728">보다 큼 기호 (>), 아포스트로피 ('), 등호 (=), 따옴표 (") 또는 숫자 기호 (#) 0-1</span><span class="sxs-lookup"><span data-stu-id="3aed1-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="3aed1-729">대/소문자, 숫자, 슬래시 (/) 또는 더하기 기호 (+)가 있는 86 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="3aed1-730">두 개의 등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="3aed1-731">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-731">Checksum</span></span>

<span data-ttu-id="3aed1-732">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-733">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-733">Definition</span></span>

<span data-ttu-id="3aed1-734">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-735">정규식 CEP_Regex_AzureStorageAccountKeyGeneric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```xml
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="3aed1-736">벨기에 국가 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-737">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-737">Format</span></span>

<span data-ttu-id="3aed1-738">11자리 숫자와 구분 기호</span><span class="sxs-lookup"><span data-stu-id="3aed1-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-739">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-739">Pattern</span></span>

<span data-ttu-id="3aed1-740">11자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="3aed1-741">생년월일을 나타내는 YY.MM.DD 형식의 6자리 숫자와 마침표 2개 </span><span class="sxs-lookup"><span data-stu-id="3aed1-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="3aed1-742">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-742">A hyphen</span></span> 
- <span data-ttu-id="3aed1-743">세 개의 순차적 숫자(남성의 경우 홀수, 여성의 경우 짝수) </span><span class="sxs-lookup"><span data-stu-id="3aed1-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="3aed1-744">마침표</span><span class="sxs-lookup"><span data-stu-id="3aed1-744">A period</span></span> 
- <span data-ttu-id="3aed1-745">검사 숫자에 해당하는 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-746">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-746">Checksum</span></span>

<span data-ttu-id="3aed1-747">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-748">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-748">Definition</span></span>

<span data-ttu-id="3aed1-749">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-750">Func_belgium_national_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-751">Keyword_belgium_national_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="3aed1-752">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-752">The checksum passes.</span></span>

```xml
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-753">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="3aed1-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="3aed1-755">ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-755">Identity</span></span>
- <span data-ttu-id="3aed1-756">등록</span><span class="sxs-lookup"><span data-stu-id="3aed1-756">Registration</span></span>
- <span data-ttu-id="3aed1-757">확인과</span><span class="sxs-lookup"><span data-stu-id="3aed1-757">Identification</span></span> 
- <span data-ttu-id="3aed1-758">ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-758">ID</span></span> 
- <span data-ttu-id="3aed1-759">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="3aed1-759">Identiteitskaart</span></span>
- <span data-ttu-id="3aed1-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-760">Registratie nummer</span></span> 
- <span data-ttu-id="3aed1-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-761">Identificatie nummer</span></span> 
- <span data-ttu-id="3aed1-762">Identiteit</span><span class="sxs-lookup"><span data-stu-id="3aed1-762">Identiteit</span></span>
- <span data-ttu-id="3aed1-763">Registratie</span><span class="sxs-lookup"><span data-stu-id="3aed1-763">Registratie</span></span>
- <span data-ttu-id="3aed1-764">Identificatie</span><span class="sxs-lookup"><span data-stu-id="3aed1-764">Identificatie</span></span> 
- <span data-ttu-id="3aed1-765">Carte d'identité</span><span class="sxs-lookup"><span data-stu-id="3aed1-765">Carte d'identité</span></span> 
- <span data-ttu-id="3aed1-766">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="3aed1-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="3aed1-767">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="3aed1-767">numéro d'identification</span></span>
- <span data-ttu-id="3aed1-768">identité</span><span class="sxs-lookup"><span data-stu-id="3aed1-768">identité</span></span> 
- <span data-ttu-id="3aed1-769">inscription</span><span class="sxs-lookup"><span data-stu-id="3aed1-769">inscription</span></span> 
- <span data-ttu-id="3aed1-770">Identifikation</span><span class="sxs-lookup"><span data-stu-id="3aed1-770">Identifikation</span></span>
- <span data-ttu-id="3aed1-771">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="3aed1-771">Identifizierung</span></span>
- <span data-ttu-id="3aed1-772">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-772">Identifikationsnummer</span></span>
- <span data-ttu-id="3aed1-773">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="3aed1-773">Personalausweis</span></span>
- <span data-ttu-id="3aed1-774">Registrierung</span><span class="sxs-lookup"><span data-stu-id="3aed1-774">Registrierung</span></span>
- <span data-ttu-id="3aed1-775">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="3aed1-776">브라질 CPF 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-777">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-777">Format</span></span>

<span data-ttu-id="3aed1-778">서식이 있거나 서식이 없을 수 있는 검사 숫자를 포함하는 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-779">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-779">Pattern</span></span>

<span data-ttu-id="3aed1-780">서식이</span><span class="sxs-lookup"><span data-stu-id="3aed1-780">Formatted:</span></span>
- <span data-ttu-id="3aed1-781">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-781">Three digits</span></span> 
- <span data-ttu-id="3aed1-782">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-782">A period</span></span> 
- <span data-ttu-id="3aed1-783">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-783">Three digits</span></span> 
- <span data-ttu-id="3aed1-784">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-784">A period</span></span> 
- <span data-ttu-id="3aed1-785">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-785">Three digits</span></span> 
- <span data-ttu-id="3aed1-786">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-786">A hyphen</span></span> 
- <span data-ttu-id="3aed1-787">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-787">Two digits which are check digits</span></span>

<span data-ttu-id="3aed1-788">서식</span><span class="sxs-lookup"><span data-stu-id="3aed1-788">Unformatted:</span></span>
- <span data-ttu-id="3aed1-789">마지막 2자리 숫자가 검사 숫자인 11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-790">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-790">Checksum</span></span>

<span data-ttu-id="3aed1-791">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-792">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-792">Definition</span></span>

<span data-ttu-id="3aed1-793">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-794">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-795">Keyword_brazil_cpf에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="3aed1-796">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-796">The checksum passes.</span></span>

<span data-ttu-id="3aed1-797">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-798">Func_brazil_cpf 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-799">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-799">The checksum passes.</span></span>

```xml
<!-- Brazil CPF Number -->
<Entity id="78e09124-f2c3-4656-b32a-c1a132cd2711" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cpf"/>
     <Match idRef="Keyword_brazil_cpf"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cpf"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-800">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="3aed1-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="3aed1-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="3aed1-802">CPF</span><span class="sxs-lookup"><span data-stu-id="3aed1-802">CPF</span></span>
- <span data-ttu-id="3aed1-803">확인과</span><span class="sxs-lookup"><span data-stu-id="3aed1-803">Identification</span></span>
- <span data-ttu-id="3aed1-804">등록</span><span class="sxs-lookup"><span data-stu-id="3aed1-804">Registration</span></span>
- <span data-ttu-id="3aed1-805">별</span><span class="sxs-lookup"><span data-stu-id="3aed1-805">Revenue</span></span>
- <span data-ttu-id="3aed1-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="3aed1-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="3aed1-807">Imposto</span><span class="sxs-lookup"><span data-stu-id="3aed1-807">Imposto</span></span> 
- <span data-ttu-id="3aed1-808">Identificação</span><span class="sxs-lookup"><span data-stu-id="3aed1-808">Identificação</span></span> 
- <span data-ttu-id="3aed1-809">Inscrição</span><span class="sxs-lookup"><span data-stu-id="3aed1-809">Inscrição</span></span> 
- <span data-ttu-id="3aed1-810">고 eita</span><span class="sxs-lookup"><span data-stu-id="3aed1-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="3aed1-811">브라질 법인 번호(CNPJ)</span><span class="sxs-lookup"><span data-stu-id="3aed1-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-812">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-812">Format</span></span>

<span data-ttu-id="3aed1-813">등록 번호, 지점 번호, 검사 숫자 및 구분 기호를 포함하는 14자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-814">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-814">Pattern</span></span>
<span data-ttu-id="3aed1-815">14자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="3aed1-816">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-816">Two digits</span></span> 
- <span data-ttu-id="3aed1-817">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-817">A period</span></span> 
- <span data-ttu-id="3aed1-818">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-818">Three digits</span></span> 
- <span data-ttu-id="3aed1-819">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-819">A period</span></span> 
- <span data-ttu-id="3aed1-820">3자리 숫자(처음 8자리 숫자는 등록 번호임) </span><span class="sxs-lookup"><span data-stu-id="3aed1-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="3aed1-821">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="3aed1-821">A forward slash</span></span> 
- <span data-ttu-id="3aed1-822">4자리 지점 번호 </span><span class="sxs-lookup"><span data-stu-id="3aed1-822">Four-digit branch number</span></span> 
- <span data-ttu-id="3aed1-823">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-823">A hyphen</span></span> 
- <span data-ttu-id="3aed1-824">검사 숫자에 해당하는 2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-825">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-825">Checksum</span></span>

<span data-ttu-id="3aed1-826">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-827">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-827">Definition</span></span>

<span data-ttu-id="3aed1-828">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-829">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-830">Keyword_brazil_cnpj에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="3aed1-831">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-831">The checksum passes.</span></span>

<span data-ttu-id="3aed1-832">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-833">Func_brazil_cnpj 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-834">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-834">The checksum passes.</span></span>

```xml
<!-- Brazil Legal Entity Number (CNPJ) -->
<Entity id="9b58b5cd-5e90-4df6-b34f-1ebcc88ceae4" recommendedConfidence="85" patternsProximity="300">
   <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cnpj"/>
     <Match idRef="Keyword_brazil_cnpj"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cnpj"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-835">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="3aed1-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="3aed1-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="3aed1-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="3aed1-837">CNPJ</span></span> 
- <span data-ttu-id="3aed1-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="3aed1-838">CNPJ/MF</span></span> 
- <span data-ttu-id="3aed1-839">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="3aed1-839">CNPJ-MF</span></span> 
- <span data-ttu-id="3aed1-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="3aed1-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="3aed1-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="3aed1-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="3aed1-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="3aed1-842">Legal entity</span></span> 
- <span data-ttu-id="3aed1-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="3aed1-843">Legal entities</span></span> 
- <span data-ttu-id="3aed1-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="3aed1-844">Registration Status</span></span> 
- <span data-ttu-id="3aed1-845">비즈니스</span><span class="sxs-lookup"><span data-stu-id="3aed1-845">Business</span></span> 
- <span data-ttu-id="3aed1-846">Company</span><span class="sxs-lookup"><span data-stu-id="3aed1-846">Company</span></span>
- <span data-ttu-id="3aed1-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="3aed1-847">CNPJ</span></span> 
- <span data-ttu-id="3aed1-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="3aed1-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="3aed1-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="3aed1-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="3aed1-850">CGC</span><span class="sxs-lookup"><span data-stu-id="3aed1-850">CGC</span></span> 
- <span data-ttu-id="3aed1-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="3aed1-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="3aed1-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="3aed1-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="3aed1-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="3aed1-853">Situação cadastral</span></span> 
- <span data-ttu-id="3aed1-854">Inscrição</span><span class="sxs-lookup"><span data-stu-id="3aed1-854">Inscrição</span></span> 
- <span data-ttu-id="3aed1-855">포털</span><span class="sxs-lookup"><span data-stu-id="3aed1-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="3aed1-856">	브라질 국가 ID 카드(RG)</span><span class="sxs-lookup"><span data-stu-id="3aed1-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-857">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-857">Format</span></span>

<span data-ttu-id="3aed1-858">Registro Geral (이전 형식): 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="3aed1-859">Registro de Identidade (RIC) (새 형식): 11 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-860">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-860">Pattern</span></span>

<span data-ttu-id="3aed1-861">Registro Geral(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="3aed1-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="3aed1-862">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-862">Two digits</span></span> 
- <span data-ttu-id="3aed1-863">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-863">A period</span></span> 
- <span data-ttu-id="3aed1-864">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-864">Three digits</span></span> 
- <span data-ttu-id="3aed1-865">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-865">A period</span></span> 
- <span data-ttu-id="3aed1-866">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-866">Three digits</span></span> 
- <span data-ttu-id="3aed1-867">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-867">A hyphen</span></span> 
- <span data-ttu-id="3aed1-868">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-868">One digit which is a check digit</span></span>

<span data-ttu-id="3aed1-869">Registro de Identidade (RIC) (새 형식):</span><span class="sxs-lookup"><span data-stu-id="3aed1-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="3aed1-870">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-870">10 digits</span></span> 
- <span data-ttu-id="3aed1-871">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-871">A hyphen</span></span> 
- <span data-ttu-id="3aed1-872">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-873">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-873">Checksum</span></span>

<span data-ttu-id="3aed1-874">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-875">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-875">Definition</span></span>

<span data-ttu-id="3aed1-876">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-877">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-878">Keyword_brazil_rg에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="3aed1-879">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-879">The checksum passes.</span></span>

<span data-ttu-id="3aed1-880">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-881">Func_brazil_rg 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-882">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-882">The checksum passes.</span></span>

```xml
<!-- Brazil National ID Card (RG) -->
<Entity id="486de900-db70-41b3-a886-abdf25af119c" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_rg"/>
     <Match idRef="Keyword_brazil_rg"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_rg"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-883">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="3aed1-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="3aed1-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="3aed1-885">Cédula de identidade identity card 국립 id número de rregistro registro de Iidentidade registro geral RG (이 키워드는 대/소문자를 구분 함) RIC (이 키워드는 대/소문자를 구분 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="3aed1-886">캐나다 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-887">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-887">Format</span></span>

<span data-ttu-id="3aed1-888">7 또는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-889">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-889">Pattern</span></span>

<span data-ttu-id="3aed1-890">캐나다 은행 계좌 번호는 7 또는 12자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="3aed1-891">캐나다 은행 계좌 송금 번호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="3aed1-892">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-892">Five digits</span></span> 
- <span data-ttu-id="3aed1-893">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-893">A hyphen</span></span> 
- <span data-ttu-id="3aed1-894">3 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="3aed1-894">Three digits OR</span></span>
- <span data-ttu-id="3aed1-895">"0"</span><span class="sxs-lookup"><span data-stu-id="3aed1-895">A zero "0"</span></span> 
- <span data-ttu-id="3aed1-896">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-897">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-897">Checksum</span></span>

<span data-ttu-id="3aed1-898">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-899">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-899">Definition</span></span>

<span data-ttu-id="3aed1-900">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-901">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-902">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="3aed1-903">Regex_canada_bank_account_transit_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="3aed1-904">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-905">Regex_canada_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-906">Keyword_canada_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```xml
<!-- Canada Bank Account Number -->
<Entity id="552e814c-cb50-4d94-bbaa-bb1d1ffb34de" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
        <Match idRef="Regex_canada_bank_account_transit_number" />
   </Pattern>
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-907">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="3aed1-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="3aed1-909">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="3aed1-909">canada savings bonds</span></span>
- <span data-ttu-id="3aed1-910">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="3aed1-910">canada revenue agency</span></span>
- <span data-ttu-id="3aed1-911">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="3aed1-911">canadian financial institution</span></span>
- <span data-ttu-id="3aed1-912">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="3aed1-912">direct deposit form</span></span>
- <span data-ttu-id="3aed1-913">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="3aed1-913">canadian citizen</span></span>
- <span data-ttu-id="3aed1-914">legal representative</span><span class="sxs-lookup"><span data-stu-id="3aed1-914">legal representative</span></span>
- <span data-ttu-id="3aed1-915">notary public</span><span class="sxs-lookup"><span data-stu-id="3aed1-915">notary public</span></span>
- <span data-ttu-id="3aed1-916">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="3aed1-916">commissioner for oaths</span></span>
- <span data-ttu-id="3aed1-917">child care benefit</span><span class="sxs-lookup"><span data-stu-id="3aed1-917">child care benefit</span></span>
- <span data-ttu-id="3aed1-918">universal child care</span><span class="sxs-lookup"><span data-stu-id="3aed1-918">universal child care</span></span>
- <span data-ttu-id="3aed1-919">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="3aed1-919">canada child tax benefit</span></span>
- <span data-ttu-id="3aed1-920">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="3aed1-920">income tax benefit</span></span>
- <span data-ttu-id="3aed1-921">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="3aed1-921">harmonized sales tax</span></span>
- <span data-ttu-id="3aed1-922">social insurance number</span><span class="sxs-lookup"><span data-stu-id="3aed1-922">social insurance number</span></span>
- <span data-ttu-id="3aed1-923">income tax refund</span><span class="sxs-lookup"><span data-stu-id="3aed1-923">income tax refund</span></span>
- <span data-ttu-id="3aed1-924">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="3aed1-924">child tax benefit</span></span>
- <span data-ttu-id="3aed1-925">territorial payments</span><span class="sxs-lookup"><span data-stu-id="3aed1-925">territorial payments</span></span>
- <span data-ttu-id="3aed1-926">institution number</span><span class="sxs-lookup"><span data-stu-id="3aed1-926">institution number</span></span>
- <span data-ttu-id="3aed1-927">deposit request</span><span class="sxs-lookup"><span data-stu-id="3aed1-927">deposit request</span></span>
- <span data-ttu-id="3aed1-928">banking information</span><span class="sxs-lookup"><span data-stu-id="3aed1-928">banking information</span></span>
- <span data-ttu-id="3aed1-929">direct deposit</span><span class="sxs-lookup"><span data-stu-id="3aed1-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="3aed1-930">캐나다 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-931">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-931">Format</span></span>

<span data-ttu-id="3aed1-932">지역마다 다름</span><span class="sxs-lookup"><span data-stu-id="3aed1-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-933">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-933">Pattern</span></span>

<span data-ttu-id="3aed1-934">앨버타, 브리티시 콜롬비아, 매니토바, 뉴브런즈윅, 뉴펀들랜드/래브라도, 노바스코샤, 온타리오, 프린스에드워드아일랜드, 퀘벡 및 서스캐처원을 포함하는 다양한 패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-935">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-935">Checksum</span></span>

<span data-ttu-id="3aed1-936">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-937">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-937">Definition</span></span>

<span data-ttu-id="3aed1-938">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-939">Func_[province_name]_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-940">Keyword_[province_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="3aed1-941">Keyword_canada_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

```xml
<!-- Canada Driver's License Number -->
    <Entity id="37186abb-8e48-4800-ad3c-e3d1610b3db0" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_alberta_drivers_license_number" />
        <Match idRef="Keyword_alberta_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_british_columbia_drivers_license_number" />
        <Match idRef="Keyword_british_columbia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_manitoba_drivers_license_number" />
        <Match idRef="Keyword_manitoba_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_brunswick_drivers_license_number" />
        <Match idRef="Keyword_new_brunswick_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_newfoundland_labrador_drivers_license_number" />
        <Match idRef="Keyword_newfoundland_labrador_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_nova_scotia_drivers_license_number" />
        <Match idRef="Keyword_nova_scotia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_ontario_drivers_license_number" />
        <Match idRef="Keyword_ontario_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_prince_edward_island_drivers_license_number" />
        <Match idRef="Keyword_prince_edward_island_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_quebec_drivers_license_number" />
        <Match idRef="Keyword_quebec_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_saskatchewan_drivers_license_number" />
        <Match idRef="Keyword_saskatchewan_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-942">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="3aed1-943">Keyword_ [province_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="3aed1-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="3aed1-944">시/도 약어(예: AB)</span><span class="sxs-lookup"><span data-stu-id="3aed1-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="3aed1-945">시/도 이름(예: 앨버타)</span><span class="sxs-lookup"><span data-stu-id="3aed1-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="3aed1-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="3aed1-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="3aed1-947">DL</span><span class="sxs-lookup"><span data-stu-id="3aed1-947">DL</span></span>
- <span data-ttu-id="3aed1-948">된다</span><span class="sxs-lookup"><span data-stu-id="3aed1-948">DLS</span></span>
- <span data-ttu-id="3aed1-949">CDL</span><span class="sxs-lookup"><span data-stu-id="3aed1-949">CDL</span></span>
- <span data-ttu-id="3aed1-950">CDLS</span><span class="sxs-lookup"><span data-stu-id="3aed1-950">CDLS</span></span>
- <span data-ttu-id="3aed1-951">DriverLic</span><span class="sxs-lookup"><span data-stu-id="3aed1-951">DriverLic</span></span>
- <span data-ttu-id="3aed1-952">DriverLics</span><span class="sxs-lookup"><span data-stu-id="3aed1-952">DriverLics</span></span>
- <span data-ttu-id="3aed1-953">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="3aed1-953">DriverLicense</span></span>
- <span data-ttu-id="3aed1-954">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-954">DriverLicenses</span></span>
- <span data-ttu-id="3aed1-955">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="3aed1-955">DriverLicence</span></span>
- <span data-ttu-id="3aed1-956">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="3aed1-956">DriverLicences</span></span>
- <span data-ttu-id="3aed1-957">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-957">Driver Lic</span></span>
- <span data-ttu-id="3aed1-958">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-958">Driver Lics</span></span>
- <span data-ttu-id="3aed1-959">Driver License</span><span class="sxs-lookup"><span data-stu-id="3aed1-959">Driver License</span></span>
- <span data-ttu-id="3aed1-960">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-960">Driver Licenses</span></span>
- <span data-ttu-id="3aed1-961">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-961">Driver Licence</span></span>
- <span data-ttu-id="3aed1-962">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-962">Driver Licences</span></span>
- <span data-ttu-id="3aed1-963">DriversLic</span><span class="sxs-lookup"><span data-stu-id="3aed1-963">DriversLic</span></span>
- <span data-ttu-id="3aed1-964">DriversLics</span><span class="sxs-lookup"><span data-stu-id="3aed1-964">DriversLics</span></span>
- <span data-ttu-id="3aed1-965">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-965">DriversLicence</span></span>
- <span data-ttu-id="3aed1-966">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="3aed1-966">DriversLicences</span></span>
- <span data-ttu-id="3aed1-967">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-967">DriversLicense</span></span>
- <span data-ttu-id="3aed1-968">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-968">DriversLicenses</span></span>
- <span data-ttu-id="3aed1-969">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-969">Drivers Lic</span></span>
- <span data-ttu-id="3aed1-970">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-970">Drivers Lics</span></span>
- <span data-ttu-id="3aed1-971">Drivers License</span><span class="sxs-lookup"><span data-stu-id="3aed1-971">Drivers License</span></span>
- <span data-ttu-id="3aed1-972">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-972">Drivers Licenses</span></span>
- <span data-ttu-id="3aed1-973">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-973">Drivers Licence</span></span>
- <span data-ttu-id="3aed1-974">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-974">Drivers Licences</span></span>
- <span data-ttu-id="3aed1-975">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-975">Driver'Lic</span></span>
- <span data-ttu-id="3aed1-976">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-976">Driver'Lics</span></span>
- <span data-ttu-id="3aed1-977">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-977">Driver'License</span></span>
- <span data-ttu-id="3aed1-978">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-978">Driver'Licenses</span></span>
- <span data-ttu-id="3aed1-979">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-979">Driver'Licence</span></span>
- <span data-ttu-id="3aed1-980">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-980">Driver'Licences</span></span>
- <span data-ttu-id="3aed1-981">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-981">Driver' Lic</span></span>
- <span data-ttu-id="3aed1-982">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-982">Driver' Lics</span></span>
- <span data-ttu-id="3aed1-983">Driver' License</span><span class="sxs-lookup"><span data-stu-id="3aed1-983">Driver' License</span></span>
- <span data-ttu-id="3aed1-984">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-984">Driver' Licenses</span></span>
- <span data-ttu-id="3aed1-985">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-985">Driver' Licence</span></span>
- <span data-ttu-id="3aed1-986">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-986">Driver' Licences</span></span>
- <span data-ttu-id="3aed1-987">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="3aed1-987">Driver'sLic</span></span>
- <span data-ttu-id="3aed1-988">Drivers (Slics)</span><span class="sxs-lookup"><span data-stu-id="3aed1-988">Driver'sLics</span></span>
- <span data-ttu-id="3aed1-989">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="3aed1-989">Driver'sLicense</span></span>
- <span data-ttu-id="3aed1-990">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-990">Driver'sLicenses</span></span>
- <span data-ttu-id="3aed1-991">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="3aed1-991">Driver'sLicence</span></span>
- <span data-ttu-id="3aed1-992">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="3aed1-992">Driver'sLicences</span></span>
- <span data-ttu-id="3aed1-993">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-993">Driver's Lic</span></span>
- <span data-ttu-id="3aed1-994">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-994">Driver's Lics</span></span>
- <span data-ttu-id="3aed1-995">Driver's License</span><span class="sxs-lookup"><span data-stu-id="3aed1-995">Driver's License</span></span>
- <span data-ttu-id="3aed1-996">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-996">Driver's Licenses</span></span>
- <span data-ttu-id="3aed1-997">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-997">Driver's Licence</span></span>
- <span data-ttu-id="3aed1-998">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-998">Driver's Licences</span></span>
- <span data-ttu-id="3aed1-999">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="3aed1-999">Permis de Conduire</span></span>
- <span data-ttu-id="3aed1-1000">id</span><span class="sxs-lookup"><span data-stu-id="3aed1-1000">id</span></span>
- <span data-ttu-id="3aed1-1001">번호가</span><span class="sxs-lookup"><span data-stu-id="3aed1-1001">ids</span></span>
- <span data-ttu-id="3aed1-1002">idcard number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1002">idcard number</span></span>
- <span data-ttu-id="3aed1-1003">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="3aed1-1003">idcard numbers</span></span>
- <span data-ttu-id="3aed1-1004">idcard #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1004">idcard #</span></span>
- <span data-ttu-id="3aed1-1005">idcard #s</span><span class="sxs-lookup"><span data-stu-id="3aed1-1005">idcard #s</span></span>
- <span data-ttu-id="3aed1-1006">idcard card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1006">idcard card</span></span>
- <span data-ttu-id="3aed1-1007">idcard cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1007">idcard cards</span></span>
- <span data-ttu-id="3aed1-1008">idcard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1008">idcard</span></span>
- <span data-ttu-id="3aed1-1009">identification number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1009">identification number</span></span>
- <span data-ttu-id="3aed1-1010">identification numbers</span><span class="sxs-lookup"><span data-stu-id="3aed1-1010">identification numbers</span></span>
- <span data-ttu-id="3aed1-1011">identification #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1011">identification #</span></span>
- <span data-ttu-id="3aed1-1012">identification #s</span><span class="sxs-lookup"><span data-stu-id="3aed1-1012">identification #s</span></span>
- <span data-ttu-id="3aed1-1013">identification card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1013">identification card</span></span>
- <span data-ttu-id="3aed1-1014">identification cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1014">identification cards</span></span>
- <span data-ttu-id="3aed1-1015">확인과</span><span class="sxs-lookup"><span data-stu-id="3aed1-1015">identification</span></span> 
- <span data-ttu-id="3aed1-1016">DL #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1016">DL#</span></span>
- <span data-ttu-id="3aed1-1017">된다 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1017">DLS#</span></span> 
- <span data-ttu-id="3aed1-1018">CDL #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1018">CDL#</span></span> 
- <span data-ttu-id="3aed1-1019">CDLS #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1019">CDLS#</span></span> 
- <span data-ttu-id="3aed1-1020">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1020">DriverLic#</span></span> 
- <span data-ttu-id="3aed1-1021">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1021">DriverLics#</span></span> 
- <span data-ttu-id="3aed1-1022">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1022">DriverLicense#</span></span> 
- <span data-ttu-id="3aed1-1023">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="3aed1-1024">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1024">DriverLicence#</span></span> 
- <span data-ttu-id="3aed1-1025">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1025">DriverLicences#</span></span> 
- <span data-ttu-id="3aed1-1026">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1026">Driver Lic#</span></span>
- <span data-ttu-id="3aed1-1027">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1027">Driver Lics#</span></span> 
- <span data-ttu-id="3aed1-1028">Driver License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1028">Driver License#</span></span> 
- <span data-ttu-id="3aed1-1029">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="3aed1-1030">Driver License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1030">Driver License#</span></span> 
- <span data-ttu-id="3aed1-1031">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1031">Driver Licences#</span></span> 
- <span data-ttu-id="3aed1-1032">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1032">DriversLic#</span></span> 
- <span data-ttu-id="3aed1-1033">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1033">DriversLics#</span></span> 
- <span data-ttu-id="3aed1-1034">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1034">DriversLicense#</span></span> 
- <span data-ttu-id="3aed1-1035">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="3aed1-1036">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1036">DriversLicence#</span></span> 
- <span data-ttu-id="3aed1-1037">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1037">DriversLicences#</span></span> 
- <span data-ttu-id="3aed1-1038">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="3aed1-1039">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="3aed1-1040">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1040">Drivers License#</span></span> 
- <span data-ttu-id="3aed1-1041">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="3aed1-1042">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="3aed1-1043">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="3aed1-1044">Driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="3aed1-1045">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="3aed1-1046">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1046">Driver'License#</span></span> 
- <span data-ttu-id="3aed1-1047">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="3aed1-1048">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="3aed1-1049">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="3aed1-1050">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="3aed1-1051">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="3aed1-1052">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1052">Driver' License#</span></span> 
- <span data-ttu-id="3aed1-1053">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="3aed1-1054">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="3aed1-1055">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="3aed1-1056">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="3aed1-1057">Drivers (Slics) #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="3aed1-1058">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="3aed1-1059">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="3aed1-1060">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="3aed1-1061">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="3aed1-1062">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="3aed1-1063">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="3aed1-1064">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1064">Driver's License#</span></span> 
- <span data-ttu-id="3aed1-1065">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="3aed1-1066">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="3aed1-1067">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="3aed1-1068">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="3aed1-1069">i #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1069">id#</span></span> 
- <span data-ttu-id="3aed1-1070">번호가 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1070">ids#</span></span> 
- <span data-ttu-id="3aed1-1071">idcard card#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1071">idcard card#</span></span> 
- <span data-ttu-id="3aed1-1072">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1072">idcard cards#</span></span> 
- <span data-ttu-id="3aed1-1073">idcard #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1073">idcard#</span></span> 
- <span data-ttu-id="3aed1-1074">identification card#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1074">identification card#</span></span> 
- <span data-ttu-id="3aed1-1075">identification cards#</span><span class="sxs-lookup"><span data-stu-id="3aed1-1075">identification cards#</span></span> 
- <span data-ttu-id="3aed1-1076">확인과 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="3aed1-1077">캐나다 건강 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1078">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1078">Format</span></span>

<span data-ttu-id="3aed1-1079">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1080">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1080">Pattern</span></span>

<span data-ttu-id="3aed1-1081">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1082">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1082">Checksum</span></span>

<span data-ttu-id="3aed1-1083">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1084">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1084">Definition</span></span>

<span data-ttu-id="3aed1-1085">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1086">Regex_canada_health_service_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1087">Keyword_canada_health_service_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

```xml
<!-- Canada Health Service Number -->
<Entity id="59c0bf39-7fab-482c-af25-00faa4384c94" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_health_service_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_health_service_number" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1088">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="3aed1-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="3aed1-1090">personal health number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1090">personal health number</span></span>
- <span data-ttu-id="3aed1-1091">patient information</span><span class="sxs-lookup"><span data-stu-id="3aed1-1091">patient information</span></span>
- <span data-ttu-id="3aed1-1092">health services</span><span class="sxs-lookup"><span data-stu-id="3aed1-1092">health services</span></span>
- <span data-ttu-id="3aed1-1093">speciality services</span><span class="sxs-lookup"><span data-stu-id="3aed1-1093">speciality services</span></span>
- <span data-ttu-id="3aed1-1094">automobile accident</span><span class="sxs-lookup"><span data-stu-id="3aed1-1094">automobile accident</span></span>
- <span data-ttu-id="3aed1-1095">patient hospital</span><span class="sxs-lookup"><span data-stu-id="3aed1-1095">patient hospital</span></span>
- <span data-ttu-id="3aed1-1096">psychiatrist</span><span class="sxs-lookup"><span data-stu-id="3aed1-1096">psychiatrist</span></span>
- <span data-ttu-id="3aed1-1097">workers compensation</span><span class="sxs-lookup"><span data-stu-id="3aed1-1097">workers compensation</span></span>
- <span data-ttu-id="3aed1-1098">종류</span><span class="sxs-lookup"><span data-stu-id="3aed1-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="3aed1-1099">캐나다 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1100">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1100">Format</span></span>

<span data-ttu-id="3aed1-1101">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1102">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1102">Pattern</span></span>

<span data-ttu-id="3aed1-1103">2개의 대문자와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1104">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1104">Checksum</span></span>

<span data-ttu-id="3aed1-1105">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1106">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1106">Definition</span></span>

<span data-ttu-id="3aed1-1107">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1108">Regex_canada_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1109">Keyword_canada_passport_number 또는 Keyword_passport의 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

```xml 
<!-- Canada Passport Number -->
<Entity id="14d0db8b-498a-43ed-9fca-f6097ae687eb" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_passport_number" />
          <Match idRef="Keyword_passport" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1110">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="3aed1-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="3aed1-1112">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="3aed1-1112">canadian citizenship</span></span>
- <span data-ttu-id="3aed1-1113">canadian passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-1113">canadian passport</span></span>
- <span data-ttu-id="3aed1-1114">passport application</span><span class="sxs-lookup"><span data-stu-id="3aed1-1114">passport application</span></span>
- <span data-ttu-id="3aed1-1115">passport photos</span><span class="sxs-lookup"><span data-stu-id="3aed1-1115">passport photos</span></span>
- <span data-ttu-id="3aed1-1116">certified translator</span><span class="sxs-lookup"><span data-stu-id="3aed1-1116">certified translator</span></span>
- <span data-ttu-id="3aed1-1117">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="3aed1-1117">canadian citizens</span></span>
- <span data-ttu-id="3aed1-1118">processing times</span><span class="sxs-lookup"><span data-stu-id="3aed1-1118">processing times</span></span>
- <span data-ttu-id="3aed1-1119">renewal application</span><span class="sxs-lookup"><span data-stu-id="3aed1-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="3aed1-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-1120">Keyword_passport</span></span>

- <span data-ttu-id="3aed1-1121">Passport Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1121">Passport Number</span></span>
- <span data-ttu-id="3aed1-1122">Passport No</span><span class="sxs-lookup"><span data-stu-id="3aed1-1122">Passport No</span></span>
- <span data-ttu-id="3aed1-1123">Passport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1123">Passport #</span></span>
- <span data-ttu-id="3aed1-1124">여권 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1124">Passport#</span></span>
- <span data-ttu-id="3aed1-1125">PassportID</span><span class="sxs-lookup"><span data-stu-id="3aed1-1125">PassportID</span></span>
- <span data-ttu-id="3aed1-1126">Passportno</span><span class="sxs-lookup"><span data-stu-id="3aed1-1126">Passportno</span></span>
- <span data-ttu-id="3aed1-1127">passportnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-1127">passportnumber</span></span>
- <span data-ttu-id="3aed1-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="3aed1-1128">パスポート</span></span>
- <span data-ttu-id="3aed1-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-1129">パスポート番号</span></span>
- <span data-ttu-id="3aed1-1130">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1130">パスポートのNum</span></span>
- <span data-ttu-id="3aed1-1131">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-1131">パスポート＃</span></span>
- <span data-ttu-id="3aed1-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="3aed1-1132">Numéro de passeport</span></span>
- <span data-ttu-id="3aed1-1133">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="3aed1-1133">Passeport n °</span></span>
- <span data-ttu-id="3aed1-1134">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="3aed1-1134">Passeport Non</span></span>
- <span data-ttu-id="3aed1-1135">Passeport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1135">Passeport #</span></span>
- <span data-ttu-id="3aed1-1136">포트 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1136">Passeport#</span></span>
- <span data-ttu-id="3aed1-1137">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="3aed1-1137">PasseportNon</span></span>
- <span data-ttu-id="3aed1-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="3aed1-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="3aed1-1139">캐나다 PHIN(개인 건강 식별 번호)</span><span class="sxs-lookup"><span data-stu-id="3aed1-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1140">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1140">Format</span></span>

<span data-ttu-id="3aed1-1141">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1142">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1142">Pattern</span></span>

<span data-ttu-id="3aed1-1143">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1144">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1144">Checksum</span></span>

<span data-ttu-id="3aed1-1145">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1146">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1146">Definition</span></span>

<span data-ttu-id="3aed1-1147">DLP 정책은 300 Regex_canada_phin 문자 근사에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="3aed1-1148">Keyword_canada_phin 또는 Keyword_canada_provinces에서 키워드가 두 개 이상 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```xml
<!-- Canada PHIN -->
<Entity id="722e12ac-c89a-4ec8-a1b7-fea3469f89db" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_phin" />
        <Any minMatches="2">
          <Match idRef="Keyword_canada_phin" />
          <Match idRef="Keyword_canada_provinces" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1149">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="3aed1-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="3aed1-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="3aed1-1151">social insurance number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1151">social insurance number</span></span>
- <span data-ttu-id="3aed1-1152">health information act</span><span class="sxs-lookup"><span data-stu-id="3aed1-1152">health information act</span></span>
- <span data-ttu-id="3aed1-1153">income tax information</span><span class="sxs-lookup"><span data-stu-id="3aed1-1153">income tax information</span></span>
- <span data-ttu-id="3aed1-1154">manitoba health</span><span class="sxs-lookup"><span data-stu-id="3aed1-1154">manitoba health</span></span>
- <span data-ttu-id="3aed1-1155">health registration</span><span class="sxs-lookup"><span data-stu-id="3aed1-1155">health registration</span></span>
- <span data-ttu-id="3aed1-1156">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="3aed1-1156">prescription purchases</span></span>
- <span data-ttu-id="3aed1-1157">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="3aed1-1157">benefit eligibility</span></span>
- <span data-ttu-id="3aed1-1158">personal health</span><span class="sxs-lookup"><span data-stu-id="3aed1-1158">personal health</span></span>
- <span data-ttu-id="3aed1-1159">power of attorney</span><span class="sxs-lookup"><span data-stu-id="3aed1-1159">power of attorney</span></span>
- <span data-ttu-id="3aed1-1160">registration number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1160">registration number</span></span>
- <span data-ttu-id="3aed1-1161">personal health number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1161">personal health number</span></span>
- <span data-ttu-id="3aed1-1162">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="3aed1-1162">practitioner referral</span></span>
- <span data-ttu-id="3aed1-1163">wellness professional</span><span class="sxs-lookup"><span data-stu-id="3aed1-1163">wellness professional</span></span>
- <span data-ttu-id="3aed1-1164">patient referral</span><span class="sxs-lookup"><span data-stu-id="3aed1-1164">patient referral</span></span>
- <span data-ttu-id="3aed1-1165">health and wellness</span><span class="sxs-lookup"><span data-stu-id="3aed1-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="3aed1-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="3aed1-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="3aed1-1167">Nunavut</span><span class="sxs-lookup"><span data-stu-id="3aed1-1167">Nunavut</span></span>
- <span data-ttu-id="3aed1-1168">퀘벡</span><span class="sxs-lookup"><span data-stu-id="3aed1-1168">Quebec</span></span>
- <span data-ttu-id="3aed1-1169">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="3aed1-1169">Northwest Territories</span></span>
- <span data-ttu-id="3aed1-1170">온타리오</span><span class="sxs-lookup"><span data-stu-id="3aed1-1170">Ontario</span></span>
- <span data-ttu-id="3aed1-1171">British Columbia</span><span class="sxs-lookup"><span data-stu-id="3aed1-1171">British Columbia</span></span>
- <span data-ttu-id="3aed1-1172">앨버타</span><span class="sxs-lookup"><span data-stu-id="3aed1-1172">Alberta</span></span>
- <span data-ttu-id="3aed1-1173">서스캐처원</span><span class="sxs-lookup"><span data-stu-id="3aed1-1173">Saskatchewan</span></span>
- <span data-ttu-id="3aed1-1174">매니토바</span><span class="sxs-lookup"><span data-stu-id="3aed1-1174">Manitoba</span></span>
- <span data-ttu-id="3aed1-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="3aed1-1175">Yukon</span></span>
- <span data-ttu-id="3aed1-1176">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="3aed1-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="3aed1-1177">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="3aed1-1177">New Brunswick</span></span>
- <span data-ttu-id="3aed1-1178">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="3aed1-1178">Nova Scotia</span></span>
- <span data-ttu-id="3aed1-1179">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="3aed1-1179">Prince Edward Island</span></span>
- <span data-ttu-id="3aed1-1180">캐나다</span><span class="sxs-lookup"><span data-stu-id="3aed1-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="3aed1-1181">캐나다 사회 보험 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1182">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1182">Format</span></span>

<span data-ttu-id="3aed1-1183">선택적 하이픈 또는 공백을 포함하는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1184">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1184">Pattern</span></span>

<span data-ttu-id="3aed1-1185">서식이</span><span class="sxs-lookup"><span data-stu-id="3aed1-1185">Formatted:</span></span>
- <span data-ttu-id="3aed1-1186">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1186">Three digits</span></span> 
- <span data-ttu-id="3aed1-1187">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="3aed1-1187">A hyphen or space</span></span> 
- <span data-ttu-id="3aed1-1188">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1188">Three digits</span></span> 
- <span data-ttu-id="3aed1-1189">하이픈 또는 공백</span><span class="sxs-lookup"><span data-stu-id="3aed1-1189">A hyphen or space</span></span> 
- <span data-ttu-id="3aed1-1190">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1190">Three digits</span></span>

<span data-ttu-id="3aed1-1191">서식 없음: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1192">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1192">Checksum</span></span>

<span data-ttu-id="3aed1-1193">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1194">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1194">Definition</span></span>

<span data-ttu-id="3aed1-1195">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1196">Func_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1197">2개 이상의 다음 항목 조합:</span><span class="sxs-lookup"><span data-stu-id="3aed1-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="3aed1-1198">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="3aed1-1199">Keyword_sin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="3aed1-1200">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="3aed1-1201">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1201">The checksum passes.</span></span>

<span data-ttu-id="3aed1-1202">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1203">Func_unformatted_canadian_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1204">Keyword_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="3aed1-1205">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1205">The checksum passes.</span></span>

```xml
<!-- Canada Social Insurance Number -->
<Entity id="a2f29c85-ecb8-4514-a610-364790c0773e" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_canadian_sin" />
        <Any minMatches="2">
          <Match idRef="Keyword_sin" />
          <Match idRef="Keyword_sin_collaborative" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_canadian_sin" />
        <Match idRef="Keyword_sin" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1206">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="3aed1-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="3aed1-1207">Keyword_sin</span></span>

- <span data-ttu-id="3aed1-1208">sin</span><span class="sxs-lookup"><span data-stu-id="3aed1-1208">sin</span></span> 
- <span data-ttu-id="3aed1-1209">social insurance</span><span class="sxs-lookup"><span data-stu-id="3aed1-1209">social insurance</span></span> 
- <span data-ttu-id="3aed1-1210">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="3aed1-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="3aed1-1211">죄</span><span class="sxs-lookup"><span data-stu-id="3aed1-1211">sins</span></span> 
- <span data-ttu-id="3aed1-1212">ssn</span><span class="sxs-lookup"><span data-stu-id="3aed1-1212">ssn</span></span> 
- <span data-ttu-id="3aed1-1213">있는 ssn</span><span class="sxs-lookup"><span data-stu-id="3aed1-1213">ssns</span></span> 
- <span data-ttu-id="3aed1-1214">social security</span><span class="sxs-lookup"><span data-stu-id="3aed1-1214">social security</span></span> 
- <span data-ttu-id="3aed1-1215">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="3aed1-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="3aed1-1216">national identification number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1216">national identification number</span></span> 
- <span data-ttu-id="3aed1-1217">national id</span><span class="sxs-lookup"><span data-stu-id="3aed1-1217">national id</span></span> 
- <span data-ttu-id="3aed1-1218">sin #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1218">sin#</span></span> 
- <span data-ttu-id="3aed1-1219">soc ins</span><span class="sxs-lookup"><span data-stu-id="3aed1-1219">soc ins</span></span> 
- <span data-ttu-id="3aed1-1220">social ins</span><span class="sxs-lookup"><span data-stu-id="3aed1-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="3aed1-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="3aed1-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="3aed1-1222">driver's license</span><span class="sxs-lookup"><span data-stu-id="3aed1-1222">driver's license</span></span> 
- <span data-ttu-id="3aed1-1223">drivers license</span><span class="sxs-lookup"><span data-stu-id="3aed1-1223">drivers license</span></span> 
- <span data-ttu-id="3aed1-1224">driver's licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-1224">driver's licence</span></span> 
- <span data-ttu-id="3aed1-1225">drivers licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-1225">drivers licence</span></span> 
- <span data-ttu-id="3aed1-1226">DOB</span><span class="sxs-lookup"><span data-stu-id="3aed1-1226">DOB</span></span> 
- <span data-ttu-id="3aed1-1227">생년월일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1227">Birthdate</span></span> 
- <span data-ttu-id="3aed1-1228">생일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1228">Birthday</span></span> 
- <span data-ttu-id="3aed1-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="3aed1-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="3aed1-1230">	칠레 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1231">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1231">Format</span></span>

<span data-ttu-id="3aed1-1232">7-8 자리 숫자와 구분 기호 확인 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1233">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1233">Pattern</span></span>

<span data-ttu-id="3aed1-1234">7-8자리 숫자와 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="3aed1-1235">1-2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1235">1-2 digits</span></span> 
- <span data-ttu-id="3aed1-1236">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-1236">A period</span></span> 
- <span data-ttu-id="3aed1-1237">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1237">Three digits</span></span> 
- <span data-ttu-id="3aed1-1238">마침표 </span><span class="sxs-lookup"><span data-stu-id="3aed1-1238">A period</span></span> 
- <span data-ttu-id="3aed1-1239">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1239">Three digits</span></span> 
- <span data-ttu-id="3aed1-1240">대시 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-1240">A dash</span></span> 
- <span data-ttu-id="3aed1-1241">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1242">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1242">Checksum</span></span>

<span data-ttu-id="3aed1-1243">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1244">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1244">Definition</span></span>

<span data-ttu-id="3aed1-1245">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1246">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1247">Keyword_chile_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="3aed1-1248">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1248">The checksum passes.</span></span>

<span data-ttu-id="3aed1-1249">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1250">Func_chile_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1251">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1251">The checksum passes.</span></span>

```xml
<!-- Chile Identity Card Number -->
<Entity id="4e979794-49a0-407e-a0b9-2c536937b925" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_chile_id_card"/>
     <Match idRef="Keyword_chile_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_chile_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1252">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="3aed1-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="3aed1-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1254">National Identification Number</span></span> 
- <span data-ttu-id="3aed1-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1255">Identity card</span></span> 
- <span data-ttu-id="3aed1-1256">ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-1256">ID</span></span> 
- <span data-ttu-id="3aed1-1257">확인과</span><span class="sxs-lookup"><span data-stu-id="3aed1-1257">Identification</span></span> 
- <span data-ttu-id="3aed1-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="3aed1-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="3aed1-1259">실행</span><span class="sxs-lookup"><span data-stu-id="3aed1-1259">RUN</span></span> 
- <span data-ttu-id="3aed1-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="3aed1-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="3aed1-1261">RUT</span><span class="sxs-lookup"><span data-stu-id="3aed1-1261">RUT</span></span> 
- <span data-ttu-id="3aed1-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="3aed1-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="3aed1-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="3aed1-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="3aed1-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="3aed1-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="3aed1-1265">Identificación</span><span class="sxs-lookup"><span data-stu-id="3aed1-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="3aed1-1266">	중국 주민 ID 카드(PRC) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1267">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1267">Format</span></span>

<span data-ttu-id="3aed1-1268">18자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1269">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1269">Pattern</span></span>

<span data-ttu-id="3aed1-1270">18자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-1270">18 digits:</span></span>
- <span data-ttu-id="3aed1-1271">주소 코드에 해당하는 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="3aed1-1272">생년월일에 해당하는 YYYYMMDD 형식의 8자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="3aed1-1273">주문 코드에 해당하는 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="3aed1-1274">검사 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1275">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1275">Checksum</span></span>

<span data-ttu-id="3aed1-1276">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1277">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1277">Definition</span></span>

<span data-ttu-id="3aed1-1278">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1279">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1280">Keyword_china_resident_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="3aed1-1281">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1281">The checksum passes.</span></span>

<span data-ttu-id="3aed1-1282">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1283">Func_china_resident_id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1284">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1284">The checksum passes.</span></span>

```xml
<!-- China Resident Identity Card (PRC) Number -->
<Entity id="c92daa86-2d16-4871-901f-816b3f554fc1" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_china_resident_id"/>
     <Match idRef="Keyword_china_resident_id"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_china_resident_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1285">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="3aed1-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="3aed1-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="3aed1-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="3aed1-1288">중국</span><span class="sxs-lookup"><span data-stu-id="3aed1-1288">PRC</span></span> 
- <span data-ttu-id="3aed1-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1289">National Identification Card</span></span> 
- <span data-ttu-id="3aed1-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="3aed1-1290">身份证</span></span> 
- <span data-ttu-id="3aed1-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="3aed1-1291">居民 身份证</span></span> 
- <span data-ttu-id="3aed1-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="3aed1-1292">居民身份证</span></span> 
- <span data-ttu-id="3aed1-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="3aed1-1293">鉴定</span></span> 
- <span data-ttu-id="3aed1-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="3aed1-1294">身分證</span></span> 
- <span data-ttu-id="3aed1-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-1295">居民 身份證</span></span>
- <span data-ttu-id="3aed1-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="3aed1-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="3aed1-1297">신용 카드 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1298">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1298">Format</span></span>

<span data-ttu-id="3aed1-1299">서식이 있거나 서식이 없을 수 있는 (dddddddddddddddd), Luhn 테스트를 통과 해야 하는 16 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1299">14 to 16 digits which can be formatted or unformatted (dddddddddddddddd) and which must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1300">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1300">Pattern</span></span>

<span data-ttu-id="3aed1-1301">Visa, MasterCard, Discover Card, JCB, American Express, 상품권 및 식사권을 비롯하여 전 세계 모든 주요 브랜드 카드를 검색하는 매우 복잡하고 강력한 패턴입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1302">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1302">Checksum</span></span>

<span data-ttu-id="3aed1-1303">있음(Luhn 체크섬)</span><span class="sxs-lookup"><span data-stu-id="3aed1-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1304">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1304">Definition</span></span>

<span data-ttu-id="3aed1-1305">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1306">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1307">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1307">One of the following is true:</span></span>
    - <span data-ttu-id="3aed1-1308">Keyword_cc_verification의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="3aed1-1309">Keyword_cc_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="3aed1-1310">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="3aed1-1311">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1311">The checksum passes.</span></span>

<span data-ttu-id="3aed1-1312">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1313">Func_credit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1314">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1314">The checksum passes.</span></span>

```xml
<!-- Credit Card Number -->
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_credit_card" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1315">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="3aed1-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="3aed1-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="3aed1-1317">card verification</span><span class="sxs-lookup"><span data-stu-id="3aed1-1317">card verification</span></span>
- <span data-ttu-id="3aed1-1318">card identification number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1318">card identification number</span></span>
- <span data-ttu-id="3aed1-1319">cvn</span><span class="sxs-lookup"><span data-stu-id="3aed1-1319">cvn</span></span>
- <span data-ttu-id="3aed1-1320">cid</span><span class="sxs-lookup"><span data-stu-id="3aed1-1320">cid</span></span>
- <span data-ttu-id="3aed1-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="3aed1-1321">cvc2</span></span>
- <span data-ttu-id="3aed1-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="3aed1-1322">cvv2</span></span>
- <span data-ttu-id="3aed1-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="3aed1-1323">pin block</span></span>
- <span data-ttu-id="3aed1-1324">security code</span><span class="sxs-lookup"><span data-stu-id="3aed1-1324">security code</span></span>
- <span data-ttu-id="3aed1-1325">security number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1325">security number</span></span>
- <span data-ttu-id="3aed1-1326">security no</span><span class="sxs-lookup"><span data-stu-id="3aed1-1326">security no</span></span>
- <span data-ttu-id="3aed1-1327">issue number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1327">issue number</span></span>
- <span data-ttu-id="3aed1-1328">issue no</span><span class="sxs-lookup"><span data-stu-id="3aed1-1328">issue no</span></span>
- <span data-ttu-id="3aed1-1329">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="3aed1-1329">cryptogramme</span></span>
- <span data-ttu-id="3aed1-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="3aed1-1330">numéro de sécurité</span></span>
- <span data-ttu-id="3aed1-1331">numero de securite</span><span class="sxs-lookup"><span data-stu-id="3aed1-1331">numero de securite</span></span>
- <span data-ttu-id="3aed1-1332">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="3aed1-1333">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="3aed1-1334">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1334">prüfziffer</span></span>
- <span data-ttu-id="3aed1-1335">prufziffer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1335">prufziffer</span></span>
- <span data-ttu-id="3aed1-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="3aed1-1336">sicherheits Kode</span></span>
- <span data-ttu-id="3aed1-1337">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="3aed1-1337">sicherheitscode</span></span>
- <span data-ttu-id="3aed1-1338">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="3aed1-1339">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1339">verfalldatum</span></span>
- <span data-ttu-id="3aed1-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="3aed1-1340">codice di verifica</span></span>
- <span data-ttu-id="3aed1-1341">cod.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1341">cod.</span></span> <span data-ttu-id="3aed1-1342">sicurezza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1342">sicurezza</span></span>
- <span data-ttu-id="3aed1-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1343">cod sicurezza</span></span>
- <span data-ttu-id="3aed1-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="3aed1-1344">n autorizzazione</span></span>
- <span data-ttu-id="3aed1-1345">código</span><span class="sxs-lookup"><span data-stu-id="3aed1-1345">código</span></span>
- <span data-ttu-id="3aed1-1346">codigo</span><span class="sxs-lookup"><span data-stu-id="3aed1-1346">codigo</span></span>
- <span data-ttu-id="3aed1-1347">cod.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1347">cod.</span></span> <span data-ttu-id="3aed1-1348">seg</span><span class="sxs-lookup"><span data-stu-id="3aed1-1348">seg</span></span>
- <span data-ttu-id="3aed1-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="3aed1-1349">cod seg</span></span>
- <span data-ttu-id="3aed1-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1350">código de segurança</span></span>
- <span data-ttu-id="3aed1-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1351">codigo de seguranca</span></span>
- <span data-ttu-id="3aed1-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1352">codigo de segurança</span></span>
- <span data-ttu-id="3aed1-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1353">código de seguranca</span></span>
- <span data-ttu-id="3aed1-1354">cód.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1354">cód.</span></span> <span data-ttu-id="3aed1-1355">segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1355">segurança</span></span>
- <span data-ttu-id="3aed1-1356">cod.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1356">cod.</span></span> <span data-ttu-id="3aed1-1357">seguranca cod</span><span class="sxs-lookup"><span data-stu-id="3aed1-1357">seguranca cod.</span></span> <span data-ttu-id="3aed1-1358">segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1358">segurança</span></span>
- <span data-ttu-id="3aed1-1359">cód.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1359">cód.</span></span> <span data-ttu-id="3aed1-1360">seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1360">seguranca</span></span>
- <span data-ttu-id="3aed1-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1361">cód segurança</span></span>
- <span data-ttu-id="3aed1-1362">cod seguranca cod segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="3aed1-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1363">cód seguranca</span></span>
- <span data-ttu-id="3aed1-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="3aed1-1364">número de verificação</span></span>
- <span data-ttu-id="3aed1-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1365">numero de verificacao</span></span>
- <span data-ttu-id="3aed1-1366">ablauf</span><span class="sxs-lookup"><span data-stu-id="3aed1-1366">ablauf</span></span>
- <span data-ttu-id="3aed1-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="3aed1-1367">gültig bis</span></span>
- <span data-ttu-id="3aed1-1368">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="3aed1-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="3aed1-1369">gultig bis</span></span>
- <span data-ttu-id="3aed1-1370">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="3aed1-1371">scadenza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1371">scadenza</span></span>
- <span data-ttu-id="3aed1-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="3aed1-1372">data scad</span></span>
- <span data-ttu-id="3aed1-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="3aed1-1373">fecha de expiracion</span></span>
- <span data-ttu-id="3aed1-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="3aed1-1374">fecha de venc</span></span>
- <span data-ttu-id="3aed1-1375">vencimiento</span><span class="sxs-lookup"><span data-stu-id="3aed1-1375">vencimiento</span></span>
- <span data-ttu-id="3aed1-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1376">válido hasta</span></span>
- <span data-ttu-id="3aed1-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1377">valido hasta</span></span>
- <span data-ttu-id="3aed1-1378">vto</span><span class="sxs-lookup"><span data-stu-id="3aed1-1378">vto</span></span>
- <span data-ttu-id="3aed1-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="3aed1-1379">data de expiração</span></span>
- <span data-ttu-id="3aed1-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1380">data de expiracao</span></span>
- <span data-ttu-id="3aed1-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="3aed1-1381">data em que expira</span></span>
- <span data-ttu-id="3aed1-1382">유효한 ade</span><span class="sxs-lookup"><span data-stu-id="3aed1-1382">validade</span></span>
- <span data-ttu-id="3aed1-1383">valor</span><span class="sxs-lookup"><span data-stu-id="3aed1-1383">valor</span></span>
- <span data-ttu-id="3aed1-1384">vencimento</span><span class="sxs-lookup"><span data-stu-id="3aed1-1384">vencimento</span></span>
- <span data-ttu-id="3aed1-1385">Venc</span><span class="sxs-lookup"><span data-stu-id="3aed1-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="3aed1-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="3aed1-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="3aed1-1387">amex</span><span class="sxs-lookup"><span data-stu-id="3aed1-1387">amex</span></span>
- <span data-ttu-id="3aed1-1388">american express</span><span class="sxs-lookup"><span data-stu-id="3aed1-1388">american express</span></span>
- <span data-ttu-id="3aed1-1389">americanexpress</span><span class="sxs-lookup"><span data-stu-id="3aed1-1389">americanexpress</span></span>
- <span data-ttu-id="3aed1-1390">Visa</span><span class="sxs-lookup"><span data-stu-id="3aed1-1390">Visa</span></span>
- <span data-ttu-id="3aed1-1391">mastercard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1391">mastercard</span></span>
- <span data-ttu-id="3aed1-1392">master card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1392">master card</span></span>
- <span data-ttu-id="3aed1-1393">mc</span><span class="sxs-lookup"><span data-stu-id="3aed1-1393">mc</span></span> 
- <span data-ttu-id="3aed1-1394">mastercards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1394">mastercards</span></span>
- <span data-ttu-id="3aed1-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1395">master cards</span></span>
- <span data-ttu-id="3aed1-1396">diner's Club</span><span class="sxs-lookup"><span data-stu-id="3aed1-1396">diner's Club</span></span>
- <span data-ttu-id="3aed1-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="3aed1-1397">diners club</span></span>
- <span data-ttu-id="3aed1-1398">dinersclub</span><span class="sxs-lookup"><span data-stu-id="3aed1-1398">dinersclub</span></span>
- <span data-ttu-id="3aed1-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1399">discover card</span></span>
- <span data-ttu-id="3aed1-1400">discovercard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1400">discovercard</span></span>
- <span data-ttu-id="3aed1-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1401">discover cards</span></span>
- <span data-ttu-id="3aed1-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="3aed1-1402">JCB</span></span>
- <span data-ttu-id="3aed1-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="3aed1-1403">japanese card bureau</span></span>
- <span data-ttu-id="3aed1-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="3aed1-1404">carte blanche</span></span>
- <span data-ttu-id="3aed1-1405">carteblanche</span><span class="sxs-lookup"><span data-stu-id="3aed1-1405">carteblanche</span></span>
- <span data-ttu-id="3aed1-1406">credit card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1406">credit card</span></span>
- <span data-ttu-id="3aed1-1407">참조란 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1407">cc#</span></span>
- <span data-ttu-id="3aed1-1408">참조 #:</span><span class="sxs-lookup"><span data-stu-id="3aed1-1408">cc#:</span></span>
- <span data-ttu-id="3aed1-1409">expiration date</span><span class="sxs-lookup"><span data-stu-id="3aed1-1409">expiration date</span></span>
- <span data-ttu-id="3aed1-1410">exp date</span><span class="sxs-lookup"><span data-stu-id="3aed1-1410">exp date</span></span>
- <span data-ttu-id="3aed1-1411">expiry date</span><span class="sxs-lookup"><span data-stu-id="3aed1-1411">expiry date</span></span>
- <span data-ttu-id="3aed1-1412">날짜 d'expiration</span><span class="sxs-lookup"><span data-stu-id="3aed1-1412">date d'expiration</span></span>
- <span data-ttu-id="3aed1-1413">date d'exp</span><span class="sxs-lookup"><span data-stu-id="3aed1-1413">date d'exp</span></span>
- <span data-ttu-id="3aed1-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="3aed1-1414">date expiration</span></span>
- <span data-ttu-id="3aed1-1415">bank card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1415">bank card</span></span>
- <span data-ttu-id="3aed1-1416">bankcard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1416">bankcard</span></span>
- <span data-ttu-id="3aed1-1417">card number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1417">card number</span></span>
- <span data-ttu-id="3aed1-1418">card num</span><span class="sxs-lookup"><span data-stu-id="3aed1-1418">card num</span></span>
- <span data-ttu-id="3aed1-1419">전화 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1419">cardnumber</span></span>
- <span data-ttu-id="3aed1-1420">시 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1420">cardnumbers</span></span>
- <span data-ttu-id="3aed1-1421">card numbers</span><span class="sxs-lookup"><span data-stu-id="3aed1-1421">card numbers</span></span>
- <span data-ttu-id="3aed1-1422">카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1422">creditcard</span></span>
- <span data-ttu-id="3aed1-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1423">credit cards</span></span>
- <span data-ttu-id="3aed1-1424">creditcards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1424">creditcards</span></span>
- <span data-ttu-id="3aed1-1425">ccn</span><span class="sxs-lookup"><span data-stu-id="3aed1-1425">ccn</span></span>
- <span data-ttu-id="3aed1-1426">card holder</span><span class="sxs-lookup"><span data-stu-id="3aed1-1426">card holder</span></span>
- <span data-ttu-id="3aed1-1427">소유자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1427">cardholder</span></span>
- <span data-ttu-id="3aed1-1428">card holders</span><span class="sxs-lookup"><span data-stu-id="3aed1-1428">card holders</span></span>
- <span data-ttu-id="3aed1-1429">에이 홀더</span><span class="sxs-lookup"><span data-stu-id="3aed1-1429">cardholders</span></span>
- <span data-ttu-id="3aed1-1430">check card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1430">check card</span></span>
- <span data-ttu-id="3aed1-1431">checkcard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1431">checkcard</span></span>
- <span data-ttu-id="3aed1-1432">check cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1432">check cards</span></span>
- <span data-ttu-id="3aed1-1433">checkcards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1433">checkcards</span></span>
- <span data-ttu-id="3aed1-1434">debit card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1434">debit card</span></span>
- <span data-ttu-id="3aed1-1435">debitcard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1435">debitcard</span></span>
- <span data-ttu-id="3aed1-1436">debit cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1436">debit cards</span></span>
- <span data-ttu-id="3aed1-1437">debitcards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1437">debitcards</span></span>
- <span data-ttu-id="3aed1-1438">atm card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1438">atm card</span></span>
- <span data-ttu-id="3aed1-1439">atmcard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1439">atmcard</span></span>
- <span data-ttu-id="3aed1-1440">atm cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1440">atm cards</span></span>
- <span data-ttu-id="3aed1-1441">atmcards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1441">atmcards</span></span>
- <span data-ttu-id="3aed1-1442">enroute</span><span class="sxs-lookup"><span data-stu-id="3aed1-1442">enroute</span></span>
- <span data-ttu-id="3aed1-1443">en route</span><span class="sxs-lookup"><span data-stu-id="3aed1-1443">en route</span></span>
- <span data-ttu-id="3aed1-1444">card type</span><span class="sxs-lookup"><span data-stu-id="3aed1-1444">card type</span></span>
- <span data-ttu-id="3aed1-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="3aed1-1445">carte bancaire</span></span>
- <span data-ttu-id="3aed1-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="3aed1-1446">carte de crédit</span></span>
- <span data-ttu-id="3aed1-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="3aed1-1447">carte de credit</span></span>
- <span data-ttu-id="3aed1-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1448">numéro de carte</span></span>
- <span data-ttu-id="3aed1-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1449">numero de carte</span></span>
- <span data-ttu-id="3aed1-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1450">nº de la carte</span></span>
- <span data-ttu-id="3aed1-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1451">nº de carte</span></span>
- <span data-ttu-id="3aed1-1452">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1452">kreditkarte</span></span>
- <span data-ttu-id="3aed1-1453">karte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1453">karte</span></span>
- <span data-ttu-id="3aed1-1454">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="3aed1-1454">karteninhaber</span></span>
- <span data-ttu-id="3aed1-1455">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="3aed1-1455">karteninhabers</span></span>
- <span data-ttu-id="3aed1-1456">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="3aed1-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="3aed1-1457">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="3aed1-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="3aed1-1458">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="3aed1-1458">kreditkartentyp</span></span>
- <span data-ttu-id="3aed1-1459">eigentümername</span><span class="sxs-lookup"><span data-stu-id="3aed1-1459">eigentümername</span></span>
- <span data-ttu-id="3aed1-1460">kartennr</span><span class="sxs-lookup"><span data-stu-id="3aed1-1460">kartennr</span></span> 
- <span data-ttu-id="3aed1-1461">kartennummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1461">kartennummer</span></span>
- <span data-ttu-id="3aed1-1462">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1462">kreditkartennummer</span></span>
- <span data-ttu-id="3aed1-1463">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="3aed1-1464">carta di credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1464">carta di credito</span></span>
- <span data-ttu-id="3aed1-1465">carta credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1465">carta credito</span></span>
- <span data-ttu-id="3aed1-1466">카 ta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1466">carta</span></span>
- <span data-ttu-id="3aed1-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1467">n carta</span></span>
- <span data-ttu-id="3aed1-1468">veiligheid.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1468">nr.</span></span> <span data-ttu-id="3aed1-1469">카 ta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1469">carta</span></span>
- <span data-ttu-id="3aed1-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1470">nr carta</span></span>
- <span data-ttu-id="3aed1-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1471">numero carta</span></span>
- <span data-ttu-id="3aed1-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1472">numero della carta</span></span>
- <span data-ttu-id="3aed1-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1473">numero di carta</span></span>
- <span data-ttu-id="3aed1-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1474">tarjeta credito</span></span>
- <span data-ttu-id="3aed1-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1475">tarjeta de credito</span></span>
- <span data-ttu-id="3aed1-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1476">tarjeta crédito</span></span>
- <span data-ttu-id="3aed1-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="3aed1-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="3aed1-1478">tarjeta de atm</span></span>
- <span data-ttu-id="3aed1-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="3aed1-1479">tarjeta atm</span></span>
- <span data-ttu-id="3aed1-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1480">tarjeta debito</span></span>
- <span data-ttu-id="3aed1-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1481">tarjeta de debito</span></span>
- <span data-ttu-id="3aed1-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1482">tarjeta débito</span></span>
- <span data-ttu-id="3aed1-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1483">tarjeta de débito</span></span>
- <span data-ttu-id="3aed1-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1484">nº de tarjeta</span></span>
- <span data-ttu-id="3aed1-1485">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1485">no.</span></span> <span data-ttu-id="3aed1-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1486">de tarjeta</span></span>
- <span data-ttu-id="3aed1-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1487">no de tarjeta</span></span>
- <span data-ttu-id="3aed1-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1488">numero de tarjeta</span></span>
- <span data-ttu-id="3aed1-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1489">número de tarjeta</span></span>
- <span data-ttu-id="3aed1-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="3aed1-1490">tarjeta no</span></span>
- <span data-ttu-id="3aed1-1491">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="3aed1-1491">tarjetahabiente</span></span>
- <span data-ttu-id="3aed1-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1492">cartão de crédito</span></span>
- <span data-ttu-id="3aed1-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1493">cartão de credito</span></span>
- <span data-ttu-id="3aed1-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1494">cartao de crédito</span></span>
- <span data-ttu-id="3aed1-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1495">cartao de credito</span></span>
- <span data-ttu-id="3aed1-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1496">cartão de débito</span></span>
- <span data-ttu-id="3aed1-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1497">cartao de débito</span></span>
- <span data-ttu-id="3aed1-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1498">cartão de debito</span></span>
- <span data-ttu-id="3aed1-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1499">cartao de debito</span></span>
- <span data-ttu-id="3aed1-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="3aed1-1500">débito automático</span></span>
- <span data-ttu-id="3aed1-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="3aed1-1501">debito automatico</span></span>
- <span data-ttu-id="3aed1-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1502">número do cartão</span></span>
- <span data-ttu-id="3aed1-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1503">numero do cartão</span></span> 
- <span data-ttu-id="3aed1-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1504">número do cartao</span></span>
- <span data-ttu-id="3aed1-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1505">numero do cartao</span></span>
- <span data-ttu-id="3aed1-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1506">número de cartão</span></span>
- <span data-ttu-id="3aed1-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1507">numero de cartão</span></span>
- <span data-ttu-id="3aed1-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1508">número de cartao</span></span>
- <span data-ttu-id="3aed1-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1509">numero de cartao</span></span>
- <span data-ttu-id="3aed1-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1510">nº do cartão</span></span>
- <span data-ttu-id="3aed1-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1511">nº do cartao</span></span>
- <span data-ttu-id="3aed1-1512">n º</span><span class="sxs-lookup"><span data-stu-id="3aed1-1512">nº.</span></span> <span data-ttu-id="3aed1-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1513">do cartão</span></span>
- <span data-ttu-id="3aed1-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1514">no do cartão</span></span>
- <span data-ttu-id="3aed1-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1515">no do cartao</span></span>
- <span data-ttu-id="3aed1-1516">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1516">no.</span></span> <span data-ttu-id="3aed1-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1517">do cartão</span></span>
- <span data-ttu-id="3aed1-1518">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1518">no.</span></span> <span data-ttu-id="3aed1-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="3aed1-1520">크로아티아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1521">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1521">Format</span></span>

<span data-ttu-id="3aed1-1522">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1523">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1523">Pattern</span></span>

<span data-ttu-id="3aed1-1524">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1525">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1525">Checksum</span></span>

<span data-ttu-id="3aed1-1526">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1527">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1527">Definition</span></span>

<span data-ttu-id="3aed1-1528">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1529">Func_croatia_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1530">Keyword_croatia_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```xml
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1531">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="3aed1-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="3aed1-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1533">Croatian identity card</span></span>
- <span data-ttu-id="3aed1-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="3aed1-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="3aed1-1535">크로아티아 개인 식별(OIB) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1536">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1536">Format</span></span>

<span data-ttu-id="3aed1-1537">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1538">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1538">Pattern</span></span>

<span data-ttu-id="3aed1-1539">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-1539">11 digits:</span></span>
- <span data-ttu-id="3aed1-1540">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1540">10 digits</span></span> 
- <span data-ttu-id="3aed1-1541">최종 자릿수는 국제 데이터 교환 목적을 위한 검사 숫자 이며, HR는 11 자리 숫자 앞에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1542">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1542">Checksum</span></span>

<span data-ttu-id="3aed1-1543">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1544">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1544">Definition</span></span>

<span data-ttu-id="3aed1-1545">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1546">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1547">Keyword_croatia_oib_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="3aed1-1548">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1548">The checksum passes.</span></span>

<span data-ttu-id="3aed1-1549">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1550">Func_croatia_oib_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1551">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1551">The checksum passes.</span></span>

```xml
<!-- Croatia Personal Identification (OIB) Number -->
<Entity id="31983b6d-db95-4eb2-a630-b44bd091968d" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_croatia_oib_number"/>
     <Match idRef="Keyword_croatia_oib_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_oib_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1552">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="3aed1-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="3aed1-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1554">Personal Identification Number</span></span>
- <span data-ttu-id="3aed1-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="3aed1-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="3aed1-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="3aed1-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="3aed1-1557">체코어 개인 Id 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1558">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1558">Format</span></span>

<span data-ttu-id="3aed1-1559">선택적 슬래시 (이전 형식)가 있는 9 자리 숫자와 슬래시 (새 형식)가 있는 10 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1560">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1560">Pattern</span></span>

<span data-ttu-id="3aed1-1561">9 자리 숫자 (이전 형식):</span><span class="sxs-lookup"><span data-stu-id="3aed1-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="3aed1-1562">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1562">Nine digits</span></span>

<span data-ttu-id="3aed1-1563">또는</span><span class="sxs-lookup"><span data-stu-id="3aed1-1563">OR</span></span>

- <span data-ttu-id="3aed1-1564">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="3aed1-1565">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="3aed1-1565">A forward slash</span></span>
- <span data-ttu-id="3aed1-1566">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1566">Three digits</span></span>

<span data-ttu-id="3aed1-1567">10 자리 숫자 (새 형식):</span><span class="sxs-lookup"><span data-stu-id="3aed1-1567">10 digits (new format):</span></span>
- <span data-ttu-id="3aed1-1568">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1568">10 digits</span></span>

<span data-ttu-id="3aed1-1569">또는</span><span class="sxs-lookup"><span data-stu-id="3aed1-1569">OR</span></span>

- <span data-ttu-id="3aed1-1570">출생 날짜를 나타내는 6 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="3aed1-1571">정방향 슬래시</span><span class="sxs-lookup"><span data-stu-id="3aed1-1571">A forward slash</span></span> 
- <span data-ttu-id="3aed1-1572">마지막 숫자가 검사 숫자인 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1573">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1573">Checksum</span></span>

<span data-ttu-id="3aed1-1574">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1575">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1575">Definition</span></span>

<span data-ttu-id="3aed1-1576">DLP 정책은 300 Func_czech_id_card 문자에 근접 한 경우에는이 유형의 중요 한 정보를 검색 하는 것으로 85% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="3aed1-1577">Keyword_czech_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="3aed1-1578">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1578">The checksum passes.</span></span>

```xml
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="3aed1-1579">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1579">Keywords</span></span>

- <span data-ttu-id="3aed1-1580">체코어 개인 id 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1580">czech personal identity number</span></span>
- <span data-ttu-id="3aed1-1581">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="3aed1-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="3aed1-1582">덴마크 개인 식별 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1583">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1583">Format</span></span>

<span data-ttu-id="3aed1-1584">하이픈을 포함하는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1585">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1585">Pattern</span></span>

<span data-ttu-id="3aed1-1586">10자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-1586">10 digits:</span></span>
- <span data-ttu-id="3aed1-1587">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="3aed1-1588">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-1588">A hyphen</span></span> 
- <span data-ttu-id="3aed1-1589">마지막 숫자가 검사 숫자인 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1590">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1590">Checksum</span></span>

<span data-ttu-id="3aed1-1591">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1592">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1592">Definition</span></span>

<span data-ttu-id="3aed1-1593">DLP 정책은 300 Regex_denmark_id 문자 근사에서 해당 패턴과 일치 하는 콘텐츠를 찾는 경우이 유형의 중요 한 정보를 검색 한다는 것을 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="3aed1-1594">Keyword_denmark_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="3aed1-1595">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1595">The checksum passes.</span></span>

```xml
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1596">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="3aed1-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="3aed1-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="3aed1-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1598">Personal Identification Number</span></span>
- <span data-ttu-id="3aed1-1599">CPR</span><span class="sxs-lookup"><span data-stu-id="3aed1-1599">CPR</span></span>
- <span data-ttu-id="3aed1-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="3aed1-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="3aed1-1601">Personnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="3aed1-1602">DEA(약물 집행 기구) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1603">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1603">Format</span></span>

<span data-ttu-id="3aed1-1604">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1605">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1605">Pattern</span></span>

<span data-ttu-id="3aed1-1606">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="3aed1-1607">등록 코드에 해당하는 abcdefghjklmnprstux 중 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="3aed1-1608">등록자 성의 첫 문자에 해당하는 한 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="3aed1-1609">검사 숫자의 마지막 7개 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1610">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1610">Checksum</span></span>

<span data-ttu-id="3aed1-1611">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1612">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1612">Definition</span></span>

<span data-ttu-id="3aed1-1613">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1614">Func_dea_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1615">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1615">The checksum passes.</span></span>

```xml
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1616">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1616">Keywords</span></span>

<span data-ttu-id="3aed1-1617">없음</span><span class="sxs-lookup"><span data-stu-id="3aed1-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="3aed1-1618">유럽 직불 카드 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1619">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1619">Format</span></span>

<span data-ttu-id="3aed1-1620">16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1621">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1621">Pattern</span></span>

<span data-ttu-id="3aed1-1622">매우 복잡하고 강력한 패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1623">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1623">Checksum</span></span>

<span data-ttu-id="3aed1-1624">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1625">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1625">Definition</span></span>

<span data-ttu-id="3aed1-1626">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1627">Func_eu_debit_card 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1628">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="3aed1-1629">Keyword_eu_debit_card의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="3aed1-1630">Keyword_card_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="3aed1-1631">Keyword_card_security_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="3aed1-1632">Keyword_card_expiration_terms_dict의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="3aed1-1633">Func_expiration_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="3aed1-1634">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1634">The checksum passes.</span></span>

```xml
    <!-- EU Debit Card Number -->
    <Entity id="0e9b3178-9678-47dd-a509-37222ca96b42" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_eu_debit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_eu_debit_card" />
          <Match idRef="Keyword_card_terms_dict" />
          <Match idRef="Keyword_card_security_terms_dict" />
          <Match idRef="Keyword_card_expiration_terms_dict" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1635">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="3aed1-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="3aed1-1637">account number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1637">account number</span></span> 
- <span data-ttu-id="3aed1-1638">card number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1638">card number</span></span> 
- <span data-ttu-id="3aed1-1639">card no.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1639">card no.</span></span> 
- <span data-ttu-id="3aed1-1640">security number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1640">security number</span></span> 
- <span data-ttu-id="3aed1-1641">참조란 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="3aed1-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="3aed1-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="3aed1-1643">acct nbr</span><span class="sxs-lookup"><span data-stu-id="3aed1-1643">acct nbr</span></span> 
- <span data-ttu-id="3aed1-1644">acct num</span><span class="sxs-lookup"><span data-stu-id="3aed1-1644">acct num</span></span> 
- <span data-ttu-id="3aed1-1645">acct no</span><span class="sxs-lookup"><span data-stu-id="3aed1-1645">acct no</span></span> 
- <span data-ttu-id="3aed1-1646">american express</span><span class="sxs-lookup"><span data-stu-id="3aed1-1646">american express</span></span> 
- <span data-ttu-id="3aed1-1647">americanexpress</span><span class="sxs-lookup"><span data-stu-id="3aed1-1647">americanexpress</span></span> 
- <span data-ttu-id="3aed1-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="3aed1-1648">americano espresso</span></span> 
- <span data-ttu-id="3aed1-1649">amex</span><span class="sxs-lookup"><span data-stu-id="3aed1-1649">amex</span></span> 
- <span data-ttu-id="3aed1-1650">atm card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1650">atm card</span></span> 
- <span data-ttu-id="3aed1-1651">atm cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1651">atm cards</span></span> 
- <span data-ttu-id="3aed1-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="3aed1-1652">atm kaart</span></span> 
- <span data-ttu-id="3aed1-1653">atmcard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1653">atmcard</span></span> 
- <span data-ttu-id="3aed1-1654">atmcards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1654">atmcards</span></span> 
- <span data-ttu-id="3aed1-1655">atmkaart</span><span class="sxs-lookup"><span data-stu-id="3aed1-1655">atmkaart</span></span> 
- <span data-ttu-id="3aed1-1656">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="3aed1-1656">atmkaarten</span></span> 
- <span data-ttu-id="3aed1-1657">bancontact</span><span class="sxs-lookup"><span data-stu-id="3aed1-1657">bancontact</span></span> 
- <span data-ttu-id="3aed1-1658">bank card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1658">bank card</span></span> 
- <span data-ttu-id="3aed1-1659">bankkaart</span><span class="sxs-lookup"><span data-stu-id="3aed1-1659">bankkaart</span></span> 
- <span data-ttu-id="3aed1-1660">card holder</span><span class="sxs-lookup"><span data-stu-id="3aed1-1660">card holder</span></span> 
- <span data-ttu-id="3aed1-1661">card holders</span><span class="sxs-lookup"><span data-stu-id="3aed1-1661">card holders</span></span> 
- <span data-ttu-id="3aed1-1662">card num</span><span class="sxs-lookup"><span data-stu-id="3aed1-1662">card num</span></span> 
- <span data-ttu-id="3aed1-1663">card number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1663">card number</span></span> 
- <span data-ttu-id="3aed1-1664">card numbers</span><span class="sxs-lookup"><span data-stu-id="3aed1-1664">card numbers</span></span> 
- <span data-ttu-id="3aed1-1665">card type</span><span class="sxs-lookup"><span data-stu-id="3aed1-1665">card type</span></span> 
- <span data-ttu-id="3aed1-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="3aed1-1666">cardano numerico</span></span> 
- <span data-ttu-id="3aed1-1667">소유자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1667">cardholder</span></span> 
- <span data-ttu-id="3aed1-1668">에이 홀더</span><span class="sxs-lookup"><span data-stu-id="3aed1-1668">cardholders</span></span> 
- <span data-ttu-id="3aed1-1669">전화 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1669">cardnumber</span></span> 
- <span data-ttu-id="3aed1-1670">시 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1670">cardnumbers</span></span> 
- <span data-ttu-id="3aed1-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1671">carta bianca</span></span> 
- <span data-ttu-id="3aed1-1672">carta credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1672">carta credito</span></span> 
- <span data-ttu-id="3aed1-1673">carta di credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1673">carta di credito</span></span> 
- <span data-ttu-id="3aed1-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1674">cartao de credito</span></span> 
- <span data-ttu-id="3aed1-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1675">cartao de crédito</span></span> 
- <span data-ttu-id="3aed1-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1676">cartao de debito</span></span> 
- <span data-ttu-id="3aed1-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1677">cartao de débito</span></span> 
- <span data-ttu-id="3aed1-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="3aed1-1678">carte bancaire</span></span> 
- <span data-ttu-id="3aed1-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="3aed1-1679">carte blanche</span></span> 
- <span data-ttu-id="3aed1-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="3aed1-1680">carte bleue</span></span> 
- <span data-ttu-id="3aed1-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="3aed1-1681">carte de credit</span></span> 
- <span data-ttu-id="3aed1-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="3aed1-1682">carte de crédit</span></span> 
- <span data-ttu-id="3aed1-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1683">carte di credito</span></span> 
- <span data-ttu-id="3aed1-1684">carteblanche</span><span class="sxs-lookup"><span data-stu-id="3aed1-1684">carteblanche</span></span> 
- <span data-ttu-id="3aed1-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1685">cartão de credito</span></span> 
- <span data-ttu-id="3aed1-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1686">cartão de crédito</span></span> 
- <span data-ttu-id="3aed1-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1687">cartão de debito</span></span> 
- <span data-ttu-id="3aed1-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1688">cartão de débito</span></span> 
- <span data-ttu-id="3aed1-1689">cb</span><span class="sxs-lookup"><span data-stu-id="3aed1-1689">cb</span></span> 
- <span data-ttu-id="3aed1-1690">ccn</span><span class="sxs-lookup"><span data-stu-id="3aed1-1690">ccn</span></span> 
- <span data-ttu-id="3aed1-1691">check card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1691">check card</span></span> 
- <span data-ttu-id="3aed1-1692">check cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1692">check cards</span></span> 
- <span data-ttu-id="3aed1-1693">checkcard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1693">checkcard</span></span>
- <span data-ttu-id="3aed1-1694">checkcards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1694">checkcards</span></span> 
- <span data-ttu-id="3aed1-1695">chequekaart</span><span class="sxs-lookup"><span data-stu-id="3aed1-1695">chequekaart</span></span> 
- <span data-ttu-id="3aed1-1696">cirrus</span><span class="sxs-lookup"><span data-stu-id="3aed1-1696">cirrus</span></span> 
- <span data-ttu-id="3aed1-1697">cirrus-edc-maestro</span><span class="sxs-lookup"><span data-stu-id="3aed1-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="3aed1-1698">controlekaart</span><span class="sxs-lookup"><span data-stu-id="3aed1-1698">controlekaart</span></span> 
- <span data-ttu-id="3aed1-1699">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="3aed1-1699">controlekaarten</span></span> 
- <span data-ttu-id="3aed1-1700">credit card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1700">credit card</span></span> 
- <span data-ttu-id="3aed1-1701">credit cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1701">credit cards</span></span> 
- <span data-ttu-id="3aed1-1702">카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1702">creditcard</span></span> 
- <span data-ttu-id="3aed1-1703">creditcards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1703">creditcards</span></span> 
- <span data-ttu-id="3aed1-1704">debetkaart</span><span class="sxs-lookup"><span data-stu-id="3aed1-1704">debetkaart</span></span> 
- <span data-ttu-id="3aed1-1705">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="3aed1-1705">debetkaarten</span></span> 
- <span data-ttu-id="3aed1-1706">debit card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1706">debit card</span></span> 
- <span data-ttu-id="3aed1-1707">debit cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1707">debit cards</span></span> 
- <span data-ttu-id="3aed1-1708">debitcard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1708">debitcard</span></span> 
- <span data-ttu-id="3aed1-1709">debitcards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1709">debitcards</span></span> 
- <span data-ttu-id="3aed1-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="3aed1-1710">debito automatico</span></span> 
- <span data-ttu-id="3aed1-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="3aed1-1711">diners club</span></span> 
- <span data-ttu-id="3aed1-1712">dinersclub</span><span class="sxs-lookup"><span data-stu-id="3aed1-1712">dinersclub</span></span> 
- <span data-ttu-id="3aed1-1713">찾아보십시오</span><span class="sxs-lookup"><span data-stu-id="3aed1-1713">discover</span></span> 
- <span data-ttu-id="3aed1-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1714">discover card</span></span> 
- <span data-ttu-id="3aed1-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1715">discover cards</span></span> 
- <span data-ttu-id="3aed1-1716">discovercard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1716">discovercard</span></span> 
- <span data-ttu-id="3aed1-1717">discovercards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1717">discovercards</span></span> 
- <span data-ttu-id="3aed1-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="3aed1-1718">débito automático</span></span>
- <span data-ttu-id="3aed1-1719">edc</span><span class="sxs-lookup"><span data-stu-id="3aed1-1719">edc</span></span> 
- <span data-ttu-id="3aed1-1720">eigentümername</span><span class="sxs-lookup"><span data-stu-id="3aed1-1720">eigentümername</span></span> 
- <span data-ttu-id="3aed1-1721">european debit card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1721">european debit card</span></span> 
- <span data-ttu-id="3aed1-1722">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="3aed1-1722">hoofdkaart</span></span> 
- <span data-ttu-id="3aed1-1723">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="3aed1-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="3aed1-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="3aed1-1724">in viaggio</span></span> 
- <span data-ttu-id="3aed1-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="3aed1-1725">japanese card bureau</span></span> 
- <span data-ttu-id="3aed1-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="3aed1-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="3aed1-1727">jcb</span><span class="sxs-lookup"><span data-stu-id="3aed1-1727">jcb</span></span> 
- <span data-ttu-id="3aed1-1728">kaart</span><span class="sxs-lookup"><span data-stu-id="3aed1-1728">kaart</span></span> 
- <span data-ttu-id="3aed1-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="3aed1-1729">kaart num</span></span> 
- <span data-ttu-id="3aed1-1730">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="3aed1-1730">kaartaantal</span></span> 
- <span data-ttu-id="3aed1-1731">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="3aed1-1731">kaartaantallen</span></span> 
- <span data-ttu-id="3aed1-1732">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="3aed1-1732">kaarthouder</span></span> 
- <span data-ttu-id="3aed1-1733">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="3aed1-1733">kaarthouders</span></span> 
- <span data-ttu-id="3aed1-1734">karte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1734">karte</span></span>  
- <span data-ttu-id="3aed1-1735">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="3aed1-1735">karteninhaber</span></span> 
- <span data-ttu-id="3aed1-1736">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="3aed1-1736">karteninhabers</span></span>
- <span data-ttu-id="3aed1-1737">kartennr</span><span class="sxs-lookup"><span data-stu-id="3aed1-1737">kartennr</span></span> 
- <span data-ttu-id="3aed1-1738">kartennummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1738">kartennummer</span></span> 
- <span data-ttu-id="3aed1-1739">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1739">kreditkarte</span></span> 
- <span data-ttu-id="3aed1-1740">kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="3aed1-1741">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="3aed1-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="3aed1-1742">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="3aed1-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="3aed1-1743">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="3aed1-1744">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="3aed1-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="3aed1-1745">maestro</span><span class="sxs-lookup"><span data-stu-id="3aed1-1745">maestro</span></span> 
- <span data-ttu-id="3aed1-1746">master card</span><span class="sxs-lookup"><span data-stu-id="3aed1-1746">master card</span></span> 
- <span data-ttu-id="3aed1-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1747">master cards</span></span> 
- <span data-ttu-id="3aed1-1748">mastercard</span><span class="sxs-lookup"><span data-stu-id="3aed1-1748">mastercard</span></span> 
- <span data-ttu-id="3aed1-1749">mastercards</span><span class="sxs-lookup"><span data-stu-id="3aed1-1749">mastercards</span></span> 
- <span data-ttu-id="3aed1-1750">mc</span><span class="sxs-lookup"><span data-stu-id="3aed1-1750">mc</span></span> 
- <span data-ttu-id="3aed1-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="3aed1-1751">mister cash</span></span> 
- <span data-ttu-id="3aed1-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1752">n carta</span></span> 
- <span data-ttu-id="3aed1-1753">카 ta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1753">carta</span></span> 
- <span data-ttu-id="3aed1-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1754">no de tarjeta</span></span> 
- <span data-ttu-id="3aed1-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1755">no do cartao</span></span> 
- <span data-ttu-id="3aed1-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1756">no do cartão</span></span> 
- <span data-ttu-id="3aed1-1757">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1757">no.</span></span> <span data-ttu-id="3aed1-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1758">de tarjeta</span></span> 
- <span data-ttu-id="3aed1-1759">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1759">no.</span></span> <span data-ttu-id="3aed1-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1760">do cartao</span></span> 
- <span data-ttu-id="3aed1-1761">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1761">no.</span></span> <span data-ttu-id="3aed1-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1762">do cartão</span></span> 
- <span data-ttu-id="3aed1-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1763">nr carta</span></span> 
- <span data-ttu-id="3aed1-1764">veiligheid.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1764">nr.</span></span> <span data-ttu-id="3aed1-1765">카 ta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1765">carta</span></span> 
- <span data-ttu-id="3aed1-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="3aed1-1766">numeri di scheda</span></span> 
- <span data-ttu-id="3aed1-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1767">numero carta</span></span> 
- <span data-ttu-id="3aed1-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1768">numero de cartao</span></span> 
- <span data-ttu-id="3aed1-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1769">numero de carte</span></span> 
- <span data-ttu-id="3aed1-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1770">numero de cartão</span></span> 
- <span data-ttu-id="3aed1-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1771">numero de tarjeta</span></span>
- <span data-ttu-id="3aed1-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1772">numero della carta</span></span> 
- <span data-ttu-id="3aed1-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1773">numero di carta</span></span> 
- <span data-ttu-id="3aed1-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="3aed1-1774">numero di scheda</span></span> 
- <span data-ttu-id="3aed1-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1775">numero do cartao</span></span> 
- <span data-ttu-id="3aed1-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1776">numero do cartão</span></span> 
- <span data-ttu-id="3aed1-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1777">numéro de carte</span></span> 
- <span data-ttu-id="3aed1-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1778">nº carta</span></span> 
- <span data-ttu-id="3aed1-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1779">nº de carte</span></span> 
- <span data-ttu-id="3aed1-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="3aed1-1780">nº de la carte</span></span> 
- <span data-ttu-id="3aed1-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="3aed1-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1782">nº do cartao</span></span> 
- <span data-ttu-id="3aed1-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1783">nº do cartão</span></span> 
- <span data-ttu-id="3aed1-1784">n º</span><span class="sxs-lookup"><span data-stu-id="3aed1-1784">nº.</span></span> <span data-ttu-id="3aed1-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1785">do cartão</span></span> 
- <span data-ttu-id="3aed1-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1786">número de cartao</span></span> 
- <span data-ttu-id="3aed1-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="3aed1-1787">número de cartão</span></span> 
- <span data-ttu-id="3aed1-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1788">número de tarjeta</span></span> 
- <span data-ttu-id="3aed1-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1789">número do cartao</span></span> 
- <span data-ttu-id="3aed1-1790">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="3aed1-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="3aed1-1791">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="3aed1-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="3aed1-1792">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="3aed1-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="3aed1-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1793">scheda della banca</span></span> 
- <span data-ttu-id="3aed1-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="3aed1-1794">scheda di controllo</span></span> 
- <span data-ttu-id="3aed1-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1795">scheda di debito</span></span> 
- <span data-ttu-id="3aed1-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="3aed1-1796">scheda matrice</span></span> 
- <span data-ttu-id="3aed1-1797">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="3aed1-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="3aed1-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="3aed1-1798">schede di controllo</span></span> 
- <span data-ttu-id="3aed1-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1799">schede di debito</span></span> 
- <span data-ttu-id="3aed1-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="3aed1-1800">schede matrici</span></span> 
- <span data-ttu-id="3aed1-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="3aed1-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="3aed1-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="3aed1-1802">scoprono le schede</span></span> 
- <span data-ttu-id="3aed1-1803">분리</span><span class="sxs-lookup"><span data-stu-id="3aed1-1803">solo</span></span> 
- <span data-ttu-id="3aed1-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="3aed1-1804">supporti di scheda</span></span> 
- <span data-ttu-id="3aed1-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="3aed1-1805">supporto di scheda</span></span> 
- <span data-ttu-id="3aed1-1806">스위치</span><span class="sxs-lookup"><span data-stu-id="3aed1-1806">switch</span></span> 
- <span data-ttu-id="3aed1-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="3aed1-1807">tarjeta atm</span></span> 
- <span data-ttu-id="3aed1-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1808">tarjeta credito</span></span> 
- <span data-ttu-id="3aed1-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="3aed1-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="3aed1-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="3aed1-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="3aed1-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="3aed1-1812">tarjeta debito</span></span> 
- <span data-ttu-id="3aed1-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="3aed1-1813">tarjeta no</span></span>
- <span data-ttu-id="3aed1-1814">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="3aed1-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="3aed1-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="3aed1-1815">tipo della scheda</span></span> 
- <span data-ttu-id="3aed1-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="3aed1-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="3aed1-1817">scheda</span><span class="sxs-lookup"><span data-stu-id="3aed1-1817">scheda</span></span> 
- <span data-ttu-id="3aed1-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="3aed1-1818">v pay</span></span> 
- <span data-ttu-id="3aed1-1819">v-지급</span><span class="sxs-lookup"><span data-stu-id="3aed1-1819">v-pay</span></span> 
- <span data-ttu-id="3aed1-1820">visa</span><span class="sxs-lookup"><span data-stu-id="3aed1-1820">visa</span></span> 
- <span data-ttu-id="3aed1-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="3aed1-1821">visa plus</span></span> 
- <span data-ttu-id="3aed1-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="3aed1-1822">visa electron</span></span> 
- <span data-ttu-id="3aed1-1823">visto</span><span class="sxs-lookup"><span data-stu-id="3aed1-1823">visto</span></span> 
- <span data-ttu-id="3aed1-1824">visum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1824">visum</span></span> 
- <span data-ttu-id="3aed1-1825">vpay</span><span class="sxs-lookup"><span data-stu-id="3aed1-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="3aed1-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="3aed1-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="3aed1-1827">card identification number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1827">card identification number</span></span>
- <span data-ttu-id="3aed1-1828">card verification</span><span class="sxs-lookup"><span data-stu-id="3aed1-1828">card verification</span></span> 
- <span data-ttu-id="3aed1-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="3aed1-1829">cardi la verifica</span></span> 
- <span data-ttu-id="3aed1-1830">cid</span><span class="sxs-lookup"><span data-stu-id="3aed1-1830">cid</span></span> 
- <span data-ttu-id="3aed1-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="3aed1-1831">cod seg</span></span> 
- <span data-ttu-id="3aed1-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1832">cod seguranca</span></span> 
- <span data-ttu-id="3aed1-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1833">cod segurança</span></span> 
- <span data-ttu-id="3aed1-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1834">cod sicurezza</span></span> 
- <span data-ttu-id="3aed1-1835">cod.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1835">cod.</span></span> <span data-ttu-id="3aed1-1836">seg</span><span class="sxs-lookup"><span data-stu-id="3aed1-1836">seg</span></span> 
- <span data-ttu-id="3aed1-1837">cod.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1837">cod.</span></span> <span data-ttu-id="3aed1-1838">seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1838">seguranca</span></span> 
- <span data-ttu-id="3aed1-1839">cod.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1839">cod.</span></span> <span data-ttu-id="3aed1-1840">segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1840">segurança</span></span> 
- <span data-ttu-id="3aed1-1841">cod.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1841">cod.</span></span> <span data-ttu-id="3aed1-1842">sicurezza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1842">sicurezza</span></span> 
- <span data-ttu-id="3aed1-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="3aed1-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="3aed1-1844">codice di verifica</span></span> 
- <span data-ttu-id="3aed1-1845">codigo</span><span class="sxs-lookup"><span data-stu-id="3aed1-1845">codigo</span></span> 
- <span data-ttu-id="3aed1-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="3aed1-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1847">codigo de segurança</span></span> 
- <span data-ttu-id="3aed1-1848">crittogramma</span><span class="sxs-lookup"><span data-stu-id="3aed1-1848">crittogramma</span></span> 
- <span data-ttu-id="3aed1-1849">cryptogram</span><span class="sxs-lookup"><span data-stu-id="3aed1-1849">cryptogram</span></span> 
- <span data-ttu-id="3aed1-1850">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="3aed1-1850">cryptogramme</span></span> 
- <span data-ttu-id="3aed1-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="3aed1-1851">cv2</span></span> 
- <span data-ttu-id="3aed1-1852">cvc</span><span class="sxs-lookup"><span data-stu-id="3aed1-1852">cvc</span></span> 
- <span data-ttu-id="3aed1-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="3aed1-1853">cvc2</span></span> 
- <span data-ttu-id="3aed1-1854">cvn</span><span class="sxs-lookup"><span data-stu-id="3aed1-1854">cvn</span></span> 
- <span data-ttu-id="3aed1-1855">cvv</span><span class="sxs-lookup"><span data-stu-id="3aed1-1855">cvv</span></span> 
- <span data-ttu-id="3aed1-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="3aed1-1856">cvv2</span></span> 
- <span data-ttu-id="3aed1-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1857">cód seguranca</span></span> 
- <span data-ttu-id="3aed1-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1858">cód segurança</span></span> 
- <span data-ttu-id="3aed1-1859">cód.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1859">cód.</span></span> <span data-ttu-id="3aed1-1860">seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1860">seguranca</span></span> 
- <span data-ttu-id="3aed1-1861">cód.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1861">cód.</span></span> <span data-ttu-id="3aed1-1862">segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1862">segurança</span></span> 
- <span data-ttu-id="3aed1-1863">código</span><span class="sxs-lookup"><span data-stu-id="3aed1-1863">código</span></span> 
- <span data-ttu-id="3aed1-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="3aed1-1864">código de seguranca</span></span> 
- <span data-ttu-id="3aed1-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="3aed1-1865">código de segurança</span></span> 
- <span data-ttu-id="3aed1-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="3aed1-1866">de kaart controle</span></span> 
- <span data-ttu-id="3aed1-1867">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="3aed1-1867">geeft nr uit</span></span> 
- <span data-ttu-id="3aed1-1868">issue no</span><span class="sxs-lookup"><span data-stu-id="3aed1-1868">issue no</span></span> 
- <span data-ttu-id="3aed1-1869">issue number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1869">issue number</span></span> 
- <span data-ttu-id="3aed1-1870">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="3aed1-1871">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="3aed1-1872">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="3aed1-1873">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="3aed1-1873">kwestieaantal</span></span> 
- <span data-ttu-id="3aed1-1874">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1874">no.</span></span> <span data-ttu-id="3aed1-1875">dell'edizione</span><span class="sxs-lookup"><span data-stu-id="3aed1-1875">dell'edizione</span></span> 
- <span data-ttu-id="3aed1-1876">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1876">no.</span></span> <span data-ttu-id="3aed1-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1877">di sicurezza</span></span> 
- <span data-ttu-id="3aed1-1878">numero de securite</span><span class="sxs-lookup"><span data-stu-id="3aed1-1878">numero de securite</span></span> 
- <span data-ttu-id="3aed1-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1879">numero de verificacao</span></span> 
- <span data-ttu-id="3aed1-1880">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="3aed1-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="3aed1-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="3aed1-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="3aed1-1882">scheda</span><span class="sxs-lookup"><span data-stu-id="3aed1-1882">scheda</span></span> 
- <span data-ttu-id="3aed1-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="3aed1-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="3aed1-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="3aed1-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="3aed1-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="3aed1-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="3aed1-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="3aed1-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="3aed1-1887">número de verificação</span></span> 
- <span data-ttu-id="3aed1-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="3aed1-1888">perno il blocco</span></span> 
- <span data-ttu-id="3aed1-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="3aed1-1889">pin block</span></span> 
- <span data-ttu-id="3aed1-1890">prufziffer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1890">prufziffer</span></span> 
- <span data-ttu-id="3aed1-1891">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1891">prüfziffer</span></span> 
- <span data-ttu-id="3aed1-1892">security code</span><span class="sxs-lookup"><span data-stu-id="3aed1-1892">security code</span></span> 
- <span data-ttu-id="3aed1-1893">security no</span><span class="sxs-lookup"><span data-stu-id="3aed1-1893">security no</span></span> 
- <span data-ttu-id="3aed1-1894">security number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1894">security number</span></span> 
- <span data-ttu-id="3aed1-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="3aed1-1895">sicherheits kode</span></span> 
- <span data-ttu-id="3aed1-1896">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="3aed1-1896">sicherheitscode</span></span> 
- <span data-ttu-id="3aed1-1897">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="3aed1-1898">speldblok</span><span class="sxs-lookup"><span data-stu-id="3aed1-1898">speldblok</span></span> 
- <span data-ttu-id="3aed1-1899">veiligheid 번호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-1899">veiligheid nr</span></span> 
- <span data-ttu-id="3aed1-1900">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="3aed1-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="3aed1-1901">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="3aed1-1901">veiligheidscode</span></span> 
- <span data-ttu-id="3aed1-1902">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="3aed1-1903">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="3aed1-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="3aed1-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="3aed1-1905">ablauf</span><span class="sxs-lookup"><span data-stu-id="3aed1-1905">ablauf</span></span> 
- <span data-ttu-id="3aed1-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="3aed1-1906">data de expiracao</span></span> 
- <span data-ttu-id="3aed1-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="3aed1-1907">data de expiração</span></span> 
- <span data-ttu-id="3aed1-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="3aed1-1908">data del exp</span></span> 
- <span data-ttu-id="3aed1-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="3aed1-1909">data di exp</span></span> 
- <span data-ttu-id="3aed1-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1910">data di scadenza</span></span> 
- <span data-ttu-id="3aed1-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="3aed1-1911">data em que expira</span></span> 
- <span data-ttu-id="3aed1-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="3aed1-1912">data scad</span></span> 
- <span data-ttu-id="3aed1-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1913">data scadenza</span></span> 
- <span data-ttu-id="3aed1-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="3aed1-1914">date de validité</span></span> 
- <span data-ttu-id="3aed1-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="3aed1-1915">datum afloop</span></span> 
- <span data-ttu-id="3aed1-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="3aed1-1916">datum van exp</span></span> 
- <span data-ttu-id="3aed1-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="3aed1-1917">de afloop</span></span> 
- <span data-ttu-id="3aed1-1918">espira</span><span class="sxs-lookup"><span data-stu-id="3aed1-1918">espira</span></span> 
- <span data-ttu-id="3aed1-1919">espira</span><span class="sxs-lookup"><span data-stu-id="3aed1-1919">espira</span></span> 
- <span data-ttu-id="3aed1-1920">exp date</span><span class="sxs-lookup"><span data-stu-id="3aed1-1920">exp date</span></span> 
- <span data-ttu-id="3aed1-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1921">exp datum</span></span> 
- <span data-ttu-id="3aed1-1922">행사</span><span class="sxs-lookup"><span data-stu-id="3aed1-1922">expiration</span></span> 
- <span data-ttu-id="3aed1-1923">예정</span><span class="sxs-lookup"><span data-stu-id="3aed1-1923">expire</span></span> 
- <span data-ttu-id="3aed1-1924">expires</span><span class="sxs-lookup"><span data-stu-id="3aed1-1924">expires</span></span> 
- <span data-ttu-id="3aed1-1925">만료</span><span class="sxs-lookup"><span data-stu-id="3aed1-1925">expiry</span></span> 
- <span data-ttu-id="3aed1-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="3aed1-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="3aed1-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="3aed1-1927">fecha de venc</span></span> 
- <span data-ttu-id="3aed1-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="3aed1-1928">gultig bis</span></span> 
- <span data-ttu-id="3aed1-1929">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="3aed1-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="3aed1-1930">gültig bis</span></span> 
- <span data-ttu-id="3aed1-1931">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="3aed1-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1932">la scadenza</span></span> 
- <span data-ttu-id="3aed1-1933">scadenza</span><span class="sxs-lookup"><span data-stu-id="3aed1-1933">scadenza</span></span> 
- <span data-ttu-id="3aed1-1934">valable</span><span class="sxs-lookup"><span data-stu-id="3aed1-1934">valable</span></span> 
- <span data-ttu-id="3aed1-1935">유효한 ade</span><span class="sxs-lookup"><span data-stu-id="3aed1-1935">validade</span></span> 
- <span data-ttu-id="3aed1-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1936">valido hasta</span></span> 
- <span data-ttu-id="3aed1-1937">valor</span><span class="sxs-lookup"><span data-stu-id="3aed1-1937">valor</span></span> 
- <span data-ttu-id="3aed1-1938">venc</span><span class="sxs-lookup"><span data-stu-id="3aed1-1938">venc</span></span> 
- <span data-ttu-id="3aed1-1939">vencimento</span><span class="sxs-lookup"><span data-stu-id="3aed1-1939">vencimento</span></span> 
- <span data-ttu-id="3aed1-1940">vencimiento</span><span class="sxs-lookup"><span data-stu-id="3aed1-1940">vencimiento</span></span> 
- <span data-ttu-id="3aed1-1941">verloopt</span><span class="sxs-lookup"><span data-stu-id="3aed1-1941">verloopt</span></span> 
- <span data-ttu-id="3aed1-1942">vervaldag</span><span class="sxs-lookup"><span data-stu-id="3aed1-1942">vervaldag</span></span> 
- <span data-ttu-id="3aed1-1943">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-1943">vervaldatum</span></span> 
- <span data-ttu-id="3aed1-1944">vto</span><span class="sxs-lookup"><span data-stu-id="3aed1-1944">vto</span></span> 
- <span data-ttu-id="3aed1-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="3aed1-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="3aed1-1946">EU 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1946">EU Driver's License Number</span></span>

<span data-ttu-id="3aed1-1947">자세한 내용은 [EU 운전 면허 번호 중요 정보 유형을](eu-driver-s-license-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="3aed1-1948">EU 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1948">EU National Identification Number</span></span>

<span data-ttu-id="3aed1-1949">자세한 내용은 [EU 국가 식별 번호 중요 한 정보 유형을](eu-national-identification-number.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="3aed1-1950">EU 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1950">EU Passport Number</span></span>

<span data-ttu-id="3aed1-1951">자세한 내용은 [EU Passport 번호 중요 한 정보 유형을](eu-passport-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="3aed1-1952">EU 주민 등록 번호 또는 동등한 ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="3aed1-1953">자세한 내용은 [EU 주민 등록 번호 또는 동등한 ID 중요 정보 유형을](eu-social-security-number-or-equivalent-id.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="3aed1-1954">EU 세금 확인 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="3aed1-1955">자세한 내용은 [EU 세금 식별 번호 중요 한 정보 유형을](eu-tax-identification-number.md)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="3aed1-1956">핀란드 국가 ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1957">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1957">Format</span></span>

<span data-ttu-id="3aed1-1958">세기를 나타내는 6자리 숫자와 문자, 3자리 숫자와 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1959">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1959">Pattern</span></span>

<span data-ttu-id="3aed1-1960">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="3aed1-1961">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="3aed1-1962">세기 표시('-', '+' 또는 'a')</span><span class="sxs-lookup"><span data-stu-id="3aed1-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="3aed1-1963">3자리 개인 ID 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="3aed1-1964">검사 숫자에 해당하는 1자리 숫자 또는 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1965">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1965">Checksum</span></span>

<span data-ttu-id="3aed1-1966">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1967">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1967">Definition</span></span>

<span data-ttu-id="3aed1-1968">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1969">Func_finnish_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1970">Keyword_finnish_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="3aed1-1971">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1971">The checksum passes.</span></span>

```xml
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-1972">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1972">Keywords</span></span>

- <span data-ttu-id="3aed1-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="3aed1-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="3aed1-1974">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="3aed1-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="3aed1-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="3aed1-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="3aed1-1976">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="3aed1-1976">Personbeteckning</span></span>
- <span data-ttu-id="3aed1-1977">Personnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="3aed1-1978">핀란드 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1978">Finland Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1979">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1979">Format</span></span>
<span data-ttu-id="3aed1-1980">9개의 문자와 숫자의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-1980">Combination of nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1981">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1981">Pattern</span></span>
<span data-ttu-id="3aed1-1982">9 개의 문자 및 숫자 조합: 2 개 문자 (대/소문자 구분 안 함) 7 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1982">Combination of nine letters and digits: Two letters (not case sensitive) Seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1983">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1983">Checksum</span></span>
<span data-ttu-id="3aed1-1984">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-1984">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-1985">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-1985">Definition</span></span>
<span data-ttu-id="3aed1-1986">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-1987">정규식 Regex_finland_passport_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1987">The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-1988">Keyword_finland_passport_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-1988">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
```xml
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_finland_passport_number"/>
     <Match idRef="Keyword_finland_passport_number"/>
  </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="3aed1-1989">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-1989">Keywords</span></span>
- <span data-ttu-id="3aed1-1990">Keyword_finland_passport_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-1990">Keyword_finland_passport_number</span></span>
- <span data-ttu-id="3aed1-1991">여권</span><span class="sxs-lookup"><span data-stu-id="3aed1-1991">Passport</span></span>
- <span data-ttu-id="3aed1-1992">에이 si</span><span class="sxs-lookup"><span data-stu-id="3aed1-1992">Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="3aed1-1993">프랑스 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-1993">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-1994">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-1994">Format</span></span>

<span data-ttu-id="3aed1-1995">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1995">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-1996">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-1996">Pattern</span></span>

<span data-ttu-id="3aed1-1997">비슷한 패턴(예: 프랑스 전화 번호)을 무시하기 위한 유효성 검사 기능을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-1997">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-1998">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-1998">Checksum</span></span>

<span data-ttu-id="3aed1-1999">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-1999">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2000">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2000">Definition</span></span>

<span data-ttu-id="3aed1-2001">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2001">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2002">Func_french_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2002">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2003">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2003">At least one of the following is true:</span></span>
- <span data-ttu-id="3aed1-2004">Keyword_french_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2004">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="3aed1-2005">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2005">The function Func_eu_date finds a date in the right date format.</span></span>

```xml
<!-- France Driver's License Number -->
<Entity id="18e55a36-a01b-4b0f-943d-dc10282a1824" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_french_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_french_drivers_license" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2006">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2006">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="3aed1-2007">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="3aed1-2007">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="3aed1-2008">drivers licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-2008">drivers licence</span></span>
- <span data-ttu-id="3aed1-2009">drivers license</span><span class="sxs-lookup"><span data-stu-id="3aed1-2009">drivers license</span></span>
- <span data-ttu-id="3aed1-2010">driving licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-2010">driving licence</span></span>
- <span data-ttu-id="3aed1-2011">driving license</span><span class="sxs-lookup"><span data-stu-id="3aed1-2011">driving license</span></span>
- <span data-ttu-id="3aed1-2012">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="3aed1-2012">permis de conduire</span></span>
- <span data-ttu-id="3aed1-2013">licence number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2013">licence number</span></span>
- <span data-ttu-id="3aed1-2014">license number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2014">license number</span></span>
- <span data-ttu-id="3aed1-2015">licence numbers</span><span class="sxs-lookup"><span data-stu-id="3aed1-2015">licence numbers</span></span>
- <span data-ttu-id="3aed1-2016">license numbers</span><span class="sxs-lookup"><span data-stu-id="3aed1-2016">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="3aed1-2017">프랑스 국가 ID 카드(CNI)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2017">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2018">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2018">Format</span></span>

<span data-ttu-id="3aed1-2019">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2019">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2020">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2020">Pattern</span></span>

<span data-ttu-id="3aed1-2021">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2021">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2022">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2022">Checksum</span></span>

<span data-ttu-id="3aed1-2023">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2023">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2024">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2024">Definition</span></span>

<span data-ttu-id="3aed1-2025">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2025">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2026">Regex_france_cni 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2026">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```xml
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2027">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2027">Keywords</span></span>

<span data-ttu-id="3aed1-2028">없음</span><span class="sxs-lookup"><span data-stu-id="3aed1-2028">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="3aed1-2029">프랑스 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2029">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2030">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2030">Format</span></span>

<span data-ttu-id="3aed1-2031">9자리 숫자 및 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2031">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2032">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2032">Pattern</span></span>

<span data-ttu-id="3aed1-2033">9자리 숫자 및 문자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2033">Nine digits and letters:</span></span>
- <span data-ttu-id="3aed1-2034">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2034">Two digits</span></span> 
- <span data-ttu-id="3aed1-2035">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2035">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-2036">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2036">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2037">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2037">Checksum</span></span>

<span data-ttu-id="3aed1-2038">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2038">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2039">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2039">Definition</span></span>

<span data-ttu-id="3aed1-2040">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2040">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2041">Func_fr_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2041">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2042">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2042">A keyword from Keyword_passport is found.</span></span>

```xml
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2043">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2043">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="3aed1-2044">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-2044">Keyword_passport</span></span>

- <span data-ttu-id="3aed1-2045">Passport Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2045">Passport Number</span></span>
- <span data-ttu-id="3aed1-2046">Passport No</span><span class="sxs-lookup"><span data-stu-id="3aed1-2046">Passport No</span></span>
- <span data-ttu-id="3aed1-2047">Passport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2047">Passport #</span></span>
- <span data-ttu-id="3aed1-2048">여권 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2048">Passport#</span></span>
- <span data-ttu-id="3aed1-2049">PassportID</span><span class="sxs-lookup"><span data-stu-id="3aed1-2049">PassportID</span></span>
- <span data-ttu-id="3aed1-2050">Passportno</span><span class="sxs-lookup"><span data-stu-id="3aed1-2050">Passportno</span></span>
- <span data-ttu-id="3aed1-2051">passportnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-2051">passportnumber</span></span>
- <span data-ttu-id="3aed1-2052">パスポート</span><span class="sxs-lookup"><span data-stu-id="3aed1-2052">パスポート</span></span>
- <span data-ttu-id="3aed1-2053">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2053">パスポート番号</span></span>
- <span data-ttu-id="3aed1-2054">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="3aed1-2054">パスポートのNum</span></span>
- <span data-ttu-id="3aed1-2055">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-2055">パスポート ＃</span></span> 
- <span data-ttu-id="3aed1-2056">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="3aed1-2056">Numéro de passeport</span></span>
- <span data-ttu-id="3aed1-2057">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="3aed1-2057">Passeport n °</span></span>
- <span data-ttu-id="3aed1-2058">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="3aed1-2058">Passeport Non</span></span>
- <span data-ttu-id="3aed1-2059">Passeport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2059">Passeport #</span></span>
- <span data-ttu-id="3aed1-2060">포트 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2060">Passeport#</span></span>
- <span data-ttu-id="3aed1-2061">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="3aed1-2061">PasseportNon</span></span>
- <span data-ttu-id="3aed1-2062">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="3aed1-2062">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="3aed1-2063">프랑스 사회 보장 번호(INSEE)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2063">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2064">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2064">Format</span></span>

<span data-ttu-id="3aed1-2065">15자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2065">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2066">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2066">Pattern</span></span>

<span data-ttu-id="3aed1-2067">다음 두 패턴 중 하나가 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2067">Must match one of two patterns:</span></span>
- <span data-ttu-id="3aed1-2068">13 자리 숫자와 공백 다음 두 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2068">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="3aed1-2069">또는</span><span class="sxs-lookup"><span data-stu-id="3aed1-2069">or</span></span>
- <span data-ttu-id="3aed1-2070">15자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2070">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2071">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2071">Checksum</span></span>

<span data-ttu-id="3aed1-2072">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2072">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2073">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2073">Definition</span></span>

<span data-ttu-id="3aed1-2074">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2074">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2075">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2075">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2076">Keyword_fr_insee의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2076">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="3aed1-2077">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2077">The checksum passes.</span></span>

<span data-ttu-id="3aed1-2078">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2078">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2079">Func_french_insee 또는 Func_fr_insee 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2079">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2080">Keyword_fr_insee의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2080">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="3aed1-2081">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2081">The checksum passes.</span></span>

```xml
<!-- France INSEE -->
<Entity id="71f62b97-efe0-4aa1-aa49-e14de253619d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="95">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="1">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2082">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2082">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="3aed1-2083">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="3aed1-2083">Keyword_fr_insee</span></span>

- <span data-ttu-id="3aed1-2084">insee</span><span class="sxs-lookup"><span data-stu-id="3aed1-2084">insee</span></span>
- <span data-ttu-id="3aed1-2085">securité sociale</span><span class="sxs-lookup"><span data-stu-id="3aed1-2085">securité sociale</span></span>
- <span data-ttu-id="3aed1-2086">securite sociale</span><span class="sxs-lookup"><span data-stu-id="3aed1-2086">securite sociale</span></span>
- <span data-ttu-id="3aed1-2087">national id</span><span class="sxs-lookup"><span data-stu-id="3aed1-2087">national id</span></span>
- <span data-ttu-id="3aed1-2088">national identification</span><span class="sxs-lookup"><span data-stu-id="3aed1-2088">national identification</span></span>
- <span data-ttu-id="3aed1-2089">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="3aed1-2089">numéro d'identité</span></span>
- <span data-ttu-id="3aed1-2090">no d'identité</span><span class="sxs-lookup"><span data-stu-id="3aed1-2090">no d'identité</span></span>
- <span data-ttu-id="3aed1-2091">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2091">no.</span></span> <span data-ttu-id="3aed1-2092">d'identité</span><span class="sxs-lookup"><span data-stu-id="3aed1-2092">d'identité</span></span>
- <span data-ttu-id="3aed1-2093">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="3aed1-2093">numero d'identite</span></span>
- <span data-ttu-id="3aed1-2094">no d'identite</span><span class="sxs-lookup"><span data-stu-id="3aed1-2094">no d'identite</span></span>
- <span data-ttu-id="3aed1-2095">아니요.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2095">no.</span></span> <span data-ttu-id="3aed1-2096">d'identite</span><span class="sxs-lookup"><span data-stu-id="3aed1-2096">d'identite</span></span>
- <span data-ttu-id="3aed1-2097">social security number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2097">social security number</span></span>
- <span data-ttu-id="3aed1-2098">social security code</span><span class="sxs-lookup"><span data-stu-id="3aed1-2098">social security code</span></span>
- <span data-ttu-id="3aed1-2099">social insurance number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2099">social insurance number</span></span>
- <span data-ttu-id="3aed1-2100">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="3aed1-2100">le numéro d'identification nationale</span></span>
- <span data-ttu-id="3aed1-2101">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="3aed1-2101">d'identité nationale</span></span>
- <span data-ttu-id="3aed1-2102">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="3aed1-2102">numéro de sécurité sociale</span></span>
- <span data-ttu-id="3aed1-2103">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="3aed1-2103">le code de la sécurité sociale</span></span>
- <span data-ttu-id="3aed1-2104">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="3aed1-2104">numéro d'assurance sociale</span></span>
- <span data-ttu-id="3aed1-2105">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="3aed1-2105">numéro de sécu</span></span>
- <span data-ttu-id="3aed1-2106">code sécu</span><span class="sxs-lookup"><span data-stu-id="3aed1-2106">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="3aed1-2107">독일 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2107">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2108">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2108">Format</span></span>

<span data-ttu-id="3aed1-2109">11자리 숫자와 문자 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-2109">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2110">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2110">Pattern</span></span>

<span data-ttu-id="3aed1-2111">11자리 숫자와 문자(대/소문자 구분 안 함):</span><span class="sxs-lookup"><span data-stu-id="3aed1-2111">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="3aed1-2112">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2112">A digit or letter</span></span> 
- <span data-ttu-id="3aed1-2113">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2113">Two digits</span></span> 
- <span data-ttu-id="3aed1-2114">6자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2114">Six digits or letters</span></span> 
- <span data-ttu-id="3aed1-2115">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2115">A digit</span></span> 
- <span data-ttu-id="3aed1-2116">1자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2116">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2117">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2117">Checksum</span></span>

<span data-ttu-id="3aed1-2118">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2118">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2119">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2119">Definition</span></span>

<span data-ttu-id="3aed1-2120">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2120">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2121">Func_german_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2121">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2122">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2122">At least one of the following is true:</span></span>
    - <span data-ttu-id="3aed1-2123">Keyword_german_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2123">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="3aed1-2124">Keyword_german_drivers_license_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2124">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="3aed1-2125">Keyword_german_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2125">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="3aed1-2126">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2126">The checksum passes.</span></span>

```xml
<!-- German Driver's License Number -->
<Entity id="91da9335-1edb-45b7-a95f-5fe41a16c63c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_drivers_license_number" />
          <Match idRef="Keyword_german_drivers_license_collaborative" />
          <Match idRef="Keyword_german_drivers_license" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2127">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2127">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="3aed1-2128">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2128">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="3aed1-2129">Führerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2129">Führerschein</span></span>
- <span data-ttu-id="3aed1-2130">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2130">Fuhrerschein</span></span>
- <span data-ttu-id="3aed1-2131">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2131">Fuehrerschein</span></span>
- <span data-ttu-id="3aed1-2132">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2132">Führerscheinnummer</span></span>
- <span data-ttu-id="3aed1-2133">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2133">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="3aed1-2134">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2134">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="3aed1-2135">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="3aed1-2135">Führerschein-</span></span> 
- <span data-ttu-id="3aed1-2136">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="3aed1-2136">Fuhrerschein-</span></span> 
- <span data-ttu-id="3aed1-2137">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="3aed1-2137">Fuehrerschein-</span></span> 
- <span data-ttu-id="3aed1-2138">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2138">FührerscheinnummerNr</span></span>
- <span data-ttu-id="3aed1-2139">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2139">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="3aed1-2140">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2140">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="3aed1-2141">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2141">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="3aed1-2142">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2142">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="3aed1-2143">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2143">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="3aed1-2144">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2144">Führerschein- Nr</span></span>
- <span data-ttu-id="3aed1-2145">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2145">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="3aed1-2146">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2146">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="3aed1-2147">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2147">Führerschein- Klasse</span></span> 
- <span data-ttu-id="3aed1-2148">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2148">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="3aed1-2149">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2149">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="3aed1-2150">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2150">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="3aed1-2151">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2151">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="3aed1-2152">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2152">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="3aed1-2153">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2153">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="3aed1-2154">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2154">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="3aed1-2155">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2155">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="3aed1-2156">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2156">Führerschein- Nr</span></span> 
- <span data-ttu-id="3aed1-2157">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2157">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="3aed1-2158">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2158">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="3aed1-2159">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2159">Führerschein- Klasse</span></span> 
- <span data-ttu-id="3aed1-2160">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2160">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="3aed1-2161">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2161">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="3aed1-2162">DL</span><span class="sxs-lookup"><span data-stu-id="3aed1-2162">DL</span></span> 
- <span data-ttu-id="3aed1-2163">된다</span><span class="sxs-lookup"><span data-stu-id="3aed1-2163">DLS</span></span>
- <span data-ttu-id="3aed1-2164">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-2164">Driv Lic</span></span> 
- <span data-ttu-id="3aed1-2165">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="3aed1-2165">Driv Licen</span></span> 
- <span data-ttu-id="3aed1-2166">Driv License</span><span class="sxs-lookup"><span data-stu-id="3aed1-2166">Driv License</span></span>
- <span data-ttu-id="3aed1-2167">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-2167">Driv Licenses</span></span> 
- <span data-ttu-id="3aed1-2168">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-2168">Driv Licence</span></span> 
- <span data-ttu-id="3aed1-2169">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-2169">Driv Licences</span></span> 
- <span data-ttu-id="3aed1-2170">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-2170">Driv Lic</span></span> 
- <span data-ttu-id="3aed1-2171">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="3aed1-2171">Driver Licen</span></span> 
- <span data-ttu-id="3aed1-2172">Driver License</span><span class="sxs-lookup"><span data-stu-id="3aed1-2172">Driver License</span></span> 
- <span data-ttu-id="3aed1-2173">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-2173">Driver Licenses</span></span> 
- <span data-ttu-id="3aed1-2174">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-2174">Driver Licence</span></span> 
- <span data-ttu-id="3aed1-2175">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-2175">Driver Licences</span></span> 
- <span data-ttu-id="3aed1-2176">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-2176">Drivers Lic</span></span> 
- <span data-ttu-id="3aed1-2177">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="3aed1-2177">Drivers Licen</span></span> 
- <span data-ttu-id="3aed1-2178">Drivers License</span><span class="sxs-lookup"><span data-stu-id="3aed1-2178">Drivers License</span></span> 
- <span data-ttu-id="3aed1-2179">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-2179">Drivers Licenses</span></span> 
- <span data-ttu-id="3aed1-2180">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-2180">Drivers Licence</span></span> 
- <span data-ttu-id="3aed1-2181">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-2181">Drivers Licences</span></span> 
- <span data-ttu-id="3aed1-2182">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-2182">Driver's Lic</span></span> 
- <span data-ttu-id="3aed1-2183">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="3aed1-2183">Driver's Licen</span></span> 
- <span data-ttu-id="3aed1-2184">Driver's License</span><span class="sxs-lookup"><span data-stu-id="3aed1-2184">Driver's License</span></span> 
- <span data-ttu-id="3aed1-2185">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-2185">Driver's Licenses</span></span> 
- <span data-ttu-id="3aed1-2186">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-2186">Driver's Licence</span></span> 
- <span data-ttu-id="3aed1-2187">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-2187">Driver's Licences</span></span> 
- <span data-ttu-id="3aed1-2188">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-2188">Driving Lic</span></span> 
- <span data-ttu-id="3aed1-2189">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="3aed1-2189">Driving Licen</span></span> 
- <span data-ttu-id="3aed1-2190">Driving License</span><span class="sxs-lookup"><span data-stu-id="3aed1-2190">Driving License</span></span> 
- <span data-ttu-id="3aed1-2191">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-2191">Driving Licenses</span></span> 
- <span data-ttu-id="3aed1-2192">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-2192">Driving Licence</span></span> 
- <span data-ttu-id="3aed1-2193">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-2193">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="3aed1-2194">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="3aed1-2194">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="3aed1-2195">Veiligheid-Führerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2195">Nr-Führerschein</span></span> 
- <span data-ttu-id="3aed1-2196">Veiligheid-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2196">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="3aed1-2197">Veiligheid-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2197">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="3aed1-2198">Führerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2198">No-Führerschein</span></span> 
- <span data-ttu-id="3aed1-2199">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2199">No-Fuhrerschein</span></span> 
- <span data-ttu-id="3aed1-2200">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2200">No-Fuehrerschein</span></span> 
- <span data-ttu-id="3aed1-2201">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2201">N-Führerschein</span></span> 
- <span data-ttu-id="3aed1-2202">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2202">N-Fuhrerschein</span></span> 
- <span data-ttu-id="3aed1-2203">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2203">N-Fuehrerschein</span></span>
- <span data-ttu-id="3aed1-2204">Veiligheid-Führerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2204">Nr-Führerschein</span></span> 
- <span data-ttu-id="3aed1-2205">Veiligheid-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2205">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="3aed1-2206">Veiligheid-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2206">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="3aed1-2207">Führerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2207">No-Führerschein</span></span> 
- <span data-ttu-id="3aed1-2208">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2208">No-Fuhrerschein</span></span> 
- <span data-ttu-id="3aed1-2209">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2209">No-Fuehrerschein</span></span> 
- <span data-ttu-id="3aed1-2210">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2210">N-Führerschein</span></span> 
- <span data-ttu-id="3aed1-2211">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2211">N-Fuhrerschein</span></span> 
- <span data-ttu-id="3aed1-2212">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="3aed1-2212">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="3aed1-2213">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="3aed1-2213">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="3aed1-2214">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-2214">ausstellungsdatum</span></span>
- <span data-ttu-id="3aed1-2215">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="3aed1-2215">ausstellungsort</span></span>
- <span data-ttu-id="3aed1-2216">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="3aed1-2216">ausstellende behöde</span></span>
- <span data-ttu-id="3aed1-2217">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="3aed1-2217">ausstellende behorde</span></span>
- <span data-ttu-id="3aed1-2218">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="3aed1-2218">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="3aed1-2219">독일 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2219">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2220">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2220">Format</span></span>

<span data-ttu-id="3aed1-2221">10자리 숫자 또는 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2221">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2222">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2222">Pattern</span></span>

<span data-ttu-id="3aed1-2223">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2223">Pattern must include all of the following:</span></span>
- <span data-ttu-id="3aed1-2224">첫 번째 문자는 숫자 또는 (C, F, G, H, J, K) 집합의 문자임</span><span class="sxs-lookup"><span data-stu-id="3aed1-2224">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="3aed1-2225">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2225">Three digits</span></span> 
- <span data-ttu-id="3aed1-2226">5자리 숫자 또는 (C, -H, J-N, P, R, T, V-Z) 집합의 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2226">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="3aed1-2227">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2227">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2228">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2228">Checksum</span></span>

<span data-ttu-id="3aed1-2229">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2229">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2230">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2230">Definition</span></span>

<span data-ttu-id="3aed1-2231">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2231">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2232">Func_german_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2232">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2233">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2233">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="3aed1-2234">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2234">The checksum passes.</span></span>

<span data-ttu-id="3aed1-2235">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2235">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2236">Func_german_passport_data 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2236">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2237">5개의 키워드 목록 중에 포함된 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2237">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="3aed1-2238">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2238">The checksum passes.</span></span>

```xml
<!-- German Passport Number -->
<Entity id="2e3da144-d42b-47ed-b123-fbf78604e52c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_german_passport" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_passport_data" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2239">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2239">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="3aed1-2240">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-2240">Keyword_german_passport</span></span>

- <span data-ttu-id="3aed1-2241">reisepass</span><span class="sxs-lookup"><span data-stu-id="3aed1-2241">reisepass</span></span>
- <span data-ttu-id="3aed1-2242">reisepasse</span><span class="sxs-lookup"><span data-stu-id="3aed1-2242">reisepasse</span></span>
- <span data-ttu-id="3aed1-2243">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2243">reisepassnummer</span></span>
- <span data-ttu-id="3aed1-2244">여권</span><span class="sxs-lookup"><span data-stu-id="3aed1-2244">passport</span></span>
- <span data-ttu-id="3aed1-2245">passports</span><span class="sxs-lookup"><span data-stu-id="3aed1-2245">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="3aed1-2246">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="3aed1-2246">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="3aed1-2247">ge삼 부, tsdatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-2247">geburtsdatum</span></span>
- <span data-ttu-id="3aed1-2248">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="3aed1-2248">ausstellungsdatum</span></span>
- <span data-ttu-id="3aed1-2249">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="3aed1-2249">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="3aed1-2250">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2250">Keyword_german_passport_number</span></span>

<span data-ttu-id="3aed1-2251">Reisepass Veiligheid-Reisepass</span><span class="sxs-lookup"><span data-stu-id="3aed1-2251">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="3aed1-2252">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="3aed1-2252">Keyword_german_passport1</span></span>

<span data-ttu-id="3aed1-2253">Reisepass-Veiligheid</span><span class="sxs-lookup"><span data-stu-id="3aed1-2253">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="3aed1-2254">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="3aed1-2254">Keyword_german_passport2</span></span>

<span data-ttu-id="3aed1-2255">bnationalit</span><span class="sxs-lookup"><span data-stu-id="3aed1-2255">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="3aed1-2256">독일 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2256">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2257">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2257">Format</span></span>

<span data-ttu-id="3aed1-2258">2010 년 11 월 1 일 이후: 9 개 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2258">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="3aed1-2259">1 월 1987 년 10 월 31 일 (2010:10 자리 숫자)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2259">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2260">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2260">Pattern</span></span>

<span data-ttu-id="3aed1-2261">2010년 11월 1일 이후:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2261">Since 1 November 2010:</span></span>
- <span data-ttu-id="3aed1-2262">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2262">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-2263">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2263">Eight digits</span></span>

<span data-ttu-id="3aed1-2264">1 년 4 월 1987 일 ~ 10 2010 월 31 일까 지:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2264">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="3aed1-2265">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2265">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2266">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2266">Checksum</span></span>

<span data-ttu-id="3aed1-2267">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2267">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2268">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2268">Definition</span></span>

<span data-ttu-id="3aed1-2269">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2269">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2270">정규식 Regex_germany_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2270">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2271">Keyword_germany_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2271">A keyword from Keyword_germany_id_card is found.</span></span>

```xml
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2272">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2272">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="3aed1-2273">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2273">Keyword_germany_id_card</span></span>

- <span data-ttu-id="3aed1-2274">Identity Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2274">Identity Card</span></span>
- <span data-ttu-id="3aed1-2275">ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-2275">ID</span></span>
- <span data-ttu-id="3aed1-2276">확인과</span><span class="sxs-lookup"><span data-stu-id="3aed1-2276">Identification</span></span>
- <span data-ttu-id="3aed1-2277">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="3aed1-2277">Personalausweis</span></span>
- <span data-ttu-id="3aed1-2278">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2278">Identifizierungsnummer</span></span>
- <span data-ttu-id="3aed1-2279">Ausweis</span><span class="sxs-lookup"><span data-stu-id="3aed1-2279">Ausweis</span></span>
- <span data-ttu-id="3aed1-2280">Identifikation</span><span class="sxs-lookup"><span data-stu-id="3aed1-2280">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="3aed1-2281">그리스 국가 ID 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2281">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2282">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2282">Format</span></span>

<span data-ttu-id="3aed1-2283">7-8자리 문자 및 숫자와 대시의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-2283">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2284">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2284">Pattern</span></span>

<span data-ttu-id="3aed1-2285">7자리 문자 및 숫자(이전 형식):</span><span class="sxs-lookup"><span data-stu-id="3aed1-2285">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="3aed1-2286">1개 문자(그리스어 알파벳의 임의 문자) </span><span class="sxs-lookup"><span data-stu-id="3aed1-2286">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="3aed1-2287">대시 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-2287">A dash</span></span> 
- <span data-ttu-id="3aed1-2288">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2288">Six digits</span></span>

<span data-ttu-id="3aed1-2289">8자리 문자와 숫자(새로운 형식):</span><span class="sxs-lookup"><span data-stu-id="3aed1-2289">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="3aed1-2290">그리스어 및 라틴어 알파벳 둘 다에 해당 대문자가 포함된 2개 문자(ABEZHIKMNOPTYX) </span><span class="sxs-lookup"><span data-stu-id="3aed1-2290">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="3aed1-2291">대시 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-2291">A dash</span></span> 
- <span data-ttu-id="3aed1-2292">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2292">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2293">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2293">Checksum</span></span>

<span data-ttu-id="3aed1-2294">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2294">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2295">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2295">Definition</span></span>

<span data-ttu-id="3aed1-2296">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2296">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2297">정규식 Regex_greece_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2297">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2298">Keyword_greece_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2298">A keyword from Keyword_greece_id_card is found.</span></span>

```xml
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2299">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2299">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="3aed1-2300">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2300">Keyword_greece_id_card</span></span>

- <span data-ttu-id="3aed1-2301">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2301">Greek identity Card</span></span>
- <span data-ttu-id="3aed1-2302">Tautotita</span><span class="sxs-lookup"><span data-stu-id="3aed1-2302">Tautotita</span></span>
- <span data-ttu-id="3aed1-2303">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="3aed1-2303">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="3aed1-2304">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="3aed1-2304">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="3aed1-2305">HKID(홍콩 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2305">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2306">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2306">Format</span></span>

<span data-ttu-id="3aed1-2307">8-9자리 문자 및 숫자와 마지막 문자를 선택적 괄호로 묶어서 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-2307">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2308">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2308">Pattern</span></span>

<span data-ttu-id="3aed1-2309">8-9자리 문자 조합:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2309">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="3aed1-2310">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2310">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-2311">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2311">Six digits</span></span> 
- <span data-ttu-id="3aed1-2312">검사 숫자에 해당하고 선택적으로 괄호로 묶는 마지막 문자(임의 숫자 또는 문자 A)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2312">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2313">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2313">Checksum</span></span>

<span data-ttu-id="3aed1-2314">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2314">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2315">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2315">Definition</span></span>

<span data-ttu-id="3aed1-2316">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2316">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2317">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2317">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2318">Keyword_hong_kong_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2318">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="3aed1-2319">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2319">The checksum passes.</span></span>

<span data-ttu-id="3aed1-2320">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2320">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2321">Func_hong_kong_id_card 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2321">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2322">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2322">The checksum passes.</span></span>

```xml
<!-- Hong Kong Identity Card (HKID) number -->
<Entity id="e63c28a7-ad29-4c17-a41a-3d2a0b70fd9c" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_hong_kong_id_card"/>
     <Match idRef="Keyword_hong_kong_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_hong_kong_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2323">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2323">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="3aed1-2324">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2324">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="3aed1-2325">홍콩 특별 식별자 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2325">hong kong identity card</span></span>
- <span data-ttu-id="3aed1-2326">HKIDC</span><span class="sxs-lookup"><span data-stu-id="3aed1-2326">HKIDC</span></span>
- <span data-ttu-id="3aed1-2327">id card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2327">id card</span></span>
- <span data-ttu-id="3aed1-2328">identity card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2328">identity card</span></span>
- <span data-ttu-id="3aed1-2329">zh-hk id 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2329">hk identity card</span></span>
- <span data-ttu-id="3aed1-2330">홍콩 id</span><span class="sxs-lookup"><span data-stu-id="3aed1-2330">hong kong id</span></span>
- <span data-ttu-id="3aed1-2331">香港身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2331">香港身份證</span></span>
- <span data-ttu-id="3aed1-2332">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2332">香港永久性居民身份證</span></span>
- <span data-ttu-id="3aed1-2333">身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2333">身份證</span></span>
- <span data-ttu-id="3aed1-2334">身份証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2334">身份証</span></span>
- <span data-ttu-id="3aed1-2335">身分證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2335">身分證</span></span>
- <span data-ttu-id="3aed1-2336">身分証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2336">身分証</span></span>
- <span data-ttu-id="3aed1-2337">香港身份証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2337">香港身份証</span></span>
- <span data-ttu-id="3aed1-2338">香港身分證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2338">香港身分證</span></span>
- <span data-ttu-id="3aed1-2339">香港身分証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2339">香港身分証</span></span>
- <span data-ttu-id="3aed1-2340">香港身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2340">香港身份證</span></span>
- <span data-ttu-id="3aed1-2341">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2341">香港居民身份證</span></span>
- <span data-ttu-id="3aed1-2342">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2342">香港居民身份証</span></span>
- <span data-ttu-id="3aed1-2343">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2343">香港居民身分證</span></span>
- <span data-ttu-id="3aed1-2344">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2344">香港居民身分証</span></span>
- <span data-ttu-id="3aed1-2345">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2345">香港永久性居民身份証</span></span>
- <span data-ttu-id="3aed1-2346">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2346">香港永久性居民身分證</span></span>
- <span data-ttu-id="3aed1-2347">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2347">香港永久性居民身分証</span></span>
- <span data-ttu-id="3aed1-2348">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2348">香港永久性居民身份證</span></span>
- <span data-ttu-id="3aed1-2349">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2349">香港非永久性居民身份證</span></span>
- <span data-ttu-id="3aed1-2350">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2350">香港非永久性居民身份証</span></span>
- <span data-ttu-id="3aed1-2351">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2351">香港非永久性居民身分證</span></span>
- <span data-ttu-id="3aed1-2352">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2352">香港非永久性居民身分証</span></span>
- <span data-ttu-id="3aed1-2353">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2353">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="3aed1-2354">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2354">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="3aed1-2355">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2355">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="3aed1-2356">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2356">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="3aed1-2357">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2357">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="3aed1-2358">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2358">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="3aed1-2359">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="3aed1-2359">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="3aed1-2360">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2360">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="3aed1-2361">인도 PAN(영구 계정 번호)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2361">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2362">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2362">Format</span></span>

<span data-ttu-id="3aed1-2363">10자리 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2363">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2364">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2364">Pattern</span></span>

<span data-ttu-id="3aed1-2365">10자리 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2365">10 letters or digits:</span></span>
- <span data-ttu-id="3aed1-2366">5개 문자(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="3aed1-2366">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-2367">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2367">Four digits</span></span> 
- <span data-ttu-id="3aed1-2368">알파벳 검사 숫자에 해당하는 문자 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-2368">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2369">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2369">Checksum</span></span>

<span data-ttu-id="3aed1-2370">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2370">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2371">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2371">Definition</span></span>

<span data-ttu-id="3aed1-2372">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2372">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2373">정규식 Regex_india_permanent_account_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2373">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2374">Keyword_india_permanent_account_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2374">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="3aed1-2375">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2375">The checksum passes.</span></span>

```xml
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2376">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2376">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="3aed1-2377">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2377">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="3aed1-2378">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2378">Permanent Account Number</span></span> 
- <span data-ttu-id="3aed1-2379">확대</span><span class="sxs-lookup"><span data-stu-id="3aed1-2379">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="3aed1-2380">인도 고유 ID(Aadhaar) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2380">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2381">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2381">Format</span></span>

<span data-ttu-id="3aed1-2382">선택적 공백 또는 대시를 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2382">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2383">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2383">Pattern</span></span>

<span data-ttu-id="3aed1-2384">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2384">12 digits:</span></span>
- <span data-ttu-id="3aed1-2385">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2385">Four digits</span></span> 
- <span data-ttu-id="3aed1-2386">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2386">An optional space or dash</span></span> 
- <span data-ttu-id="3aed1-2387">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2387">Four digits</span></span> 
- <span data-ttu-id="3aed1-2388">선택적 공백 또는 대시 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2388">An optional space or dash</span></span> 
- <span data-ttu-id="3aed1-2389">검사 숫자에 해당하는 마지막 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2389">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2390">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2390">Checksum</span></span>

<span data-ttu-id="3aed1-2391">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2391">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2392">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2392">Definition</span></span>

<span data-ttu-id="3aed1-2393">DLP 정책은 300 Func_india_aadhaar 문자에 근접 한 경우에는이 유형의 중요 한 정보를 검색 하는 것으로 85% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2393">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="3aed1-2394">Keyword_india_aadhar에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2394">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="3aed1-2395">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2395">The checksum passes.</span></span>
<span data-ttu-id="3aed1-2396">DLP 정책은 300 Func_india_aadhaar 문자에 근접 한 경우에는이 유형의 중요 한 정보를 검색 하는 것으로 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="3aed1-2397">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2397">The checksum passes.</span></span>
```xml
<!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_india_aadhaar"/>
     <Match idRef="Keyword_india_aadhar"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_india_aadhaar"/>
  </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="3aed1-2398">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2398">Keywords</span></span>
   
#### <a name="keyword_india_aadhar"></a><span data-ttu-id="3aed1-2399">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="3aed1-2399">Keyword_india_aadhar</span></span>
- <span data-ttu-id="3aed1-2400">Aadhar</span><span class="sxs-lookup"><span data-stu-id="3aed1-2400">Aadhar</span></span>
- <span data-ttu-id="3aed1-2401">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="3aed1-2401">Aadhaar</span></span>
- <span data-ttu-id="3aed1-2402">UID</span><span class="sxs-lookup"><span data-stu-id="3aed1-2402">UID</span></span>
- <span data-ttu-id="3aed1-2403">आधार</span><span class="sxs-lookup"><span data-stu-id="3aed1-2403">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="3aed1-2404">인도네시아 ID 카드(KTP) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2404">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2405">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2405">Format</span></span>

<span data-ttu-id="3aed1-2406">선택적으로 마침표를 포함하는 16자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2406">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2407">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2407">Pattern</span></span>

<span data-ttu-id="3aed1-2408">16자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2408">16 digits:</span></span>
- <span data-ttu-id="3aed1-2409">2자리 시/도 코드 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2409">Two-digit province code</span></span> 
- <span data-ttu-id="3aed1-2410">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="3aed1-2410">A period (optional)</span></span> 
- <span data-ttu-id="3aed1-2411">2자리 지역 또는 구/군/시 코드 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2411">Two-digit regency or city code</span></span> 
- <span data-ttu-id="3aed1-2412">2자리 소구역 코드 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2412">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="3aed1-2413">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="3aed1-2413">A period (optional)</span></span> 
- <span data-ttu-id="3aed1-2414">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2414">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="3aed1-2415">마침표(옵션) </span><span class="sxs-lookup"><span data-stu-id="3aed1-2415">A period (optional)</span></span> 
- <span data-ttu-id="3aed1-2416">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2416">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2417">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2417">Checksum</span></span>

<span data-ttu-id="3aed1-2418">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2418">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2419">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2419">Definition</span></span>

<span data-ttu-id="3aed1-2420">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2420">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2421">정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2421">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2422">Keyword_indonesia_id_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2422">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="3aed1-2423">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2423">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2424">정규식 Regex_indonesia_id_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2424">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

```xml
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2425">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2425">Keywords</span></span>
   
#### <a name="keyword_indonesia_id_card"></a><span data-ttu-id="3aed1-2426">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2426">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="3aed1-2427">KTP</span><span class="sxs-lookup"><span data-stu-id="3aed1-2427">KTP</span></span>
- <span data-ttu-id="3aed1-2428">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="3aed1-2428">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="3aed1-2429">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="3aed1-2429">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="3aed1-2430">IBAN(국제 은행 계좌 번호)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2430">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2431">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2431">Format</span></span>

<span data-ttu-id="3aed1-2432">국가 코드 (두 문자) + 검사 숫자 (2 자리 숫자)와 bban 숫자 (최대 30 자)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2432">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2433">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2433">Pattern</span></span>

<span data-ttu-id="3aed1-2434">패턴에는 다음이 모두 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2434">Pattern must include all of the following:</span></span>

- <span data-ttu-id="3aed1-2435">두 글자로 된 국가 코드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2435">Two-letter country code</span></span>
- <span data-ttu-id="3aed1-2436">두 개의 검사 숫자 (선택적 공백)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2436">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="3aed1-2437">1-7 개 문자 또는 숫자의 그룹 (공백으로 구분 가능)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2437">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="3aed1-2438">1-3 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2438">1-3 letters or digits</span></span>

<span data-ttu-id="3aed1-2439">각 국가의 형식은 약간 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2439">The format for each country is slightly different.</span></span> <span data-ttu-id="3aed1-2440">IBAN 중요 한 정보 유형은 다음과 같은 60 국가를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2440">The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="3aed1-2441">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, to, do, ee, es, fi,,, fr, gb, ge, gi, gl, gr, hr, hu, kw, il, vg,, nl-nl, tn,,,,,,,,, </c12>,,,,,,,,,,,,, rs, l, se, si,</span><span class="sxs-lookup"><span data-stu-id="3aed1-2441">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2442">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2442">Checksum</span></span>

<span data-ttu-id="3aed1-2443">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2443">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2444">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2444">Definition</span></span>

<span data-ttu-id="3aed1-2445">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2445">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2446">Func_iban 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2446">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2447">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2447">The checksum passes.</span></span>

```xml
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2448">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2448">Keywords</span></span>

<span data-ttu-id="3aed1-2449">없음</span><span class="sxs-lookup"><span data-stu-id="3aed1-2449">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="3aed1-2450">IP 주소</span><span class="sxs-lookup"><span data-stu-id="3aed1-2450">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2451">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2451">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="3aed1-2452">IPv4</span><span class="sxs-lookup"><span data-stu-id="3aed1-2452">IPv4:</span></span>
<span data-ttu-id="3aed1-2453">IPv4 주소의 서식 있는 버전(마침표 있음) 및 서식 없는 버전(마침표 없음)으로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2453">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="3aed1-2454">IPv6</span><span class="sxs-lookup"><span data-stu-id="3aed1-2454">IPv6:</span></span>
<span data-ttu-id="3aed1-2455">서식 있는(콜론 포함) IPv6 번호로 구성된 복잡한 패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2455">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2456">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2456">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2457">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2457">Checksum</span></span>

<span data-ttu-id="3aed1-2458">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2458">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2459">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2459">Definition</span></span>

<span data-ttu-id="3aed1-2460">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2460">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2461">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2461">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2462">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2462">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="3aed1-2463">IPv4의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2463">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2464">Regex_ipv4_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2464">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2465">Keyword_ipaddress의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2465">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="3aed1-2466">IPv6의 경우 DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 95% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2466">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2467">Regex_ipv6_address 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2467">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2468">Keyword_ipaddress의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2468">No keyword from Keyword_ipaddress is found.</span></span>

```xml
    <!-- IP Address -->
    <Entity id="1daa4ad5-e2dd-4ca4-a788-54722c09efb2" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv4_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2469">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2469">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="3aed1-2470">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="3aed1-2470">Keyword_ipaddress</span></span>

- <span data-ttu-id="3aed1-2471">IP(이 키워드는 대/소문자를 구분함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2471">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="3aed1-2472">ip address</span><span class="sxs-lookup"><span data-stu-id="3aed1-2472">ip address</span></span> 
- <span data-ttu-id="3aed1-2473">ip addresses</span><span class="sxs-lookup"><span data-stu-id="3aed1-2473">ip addresses</span></span>
- <span data-ttu-id="3aed1-2474">internet protocol</span><span class="sxs-lookup"><span data-stu-id="3aed1-2474">internet protocol</span></span>
- <span data-ttu-id="3aed1-2475">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="3aed1-2475">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="3aed1-2476">Diseases의 국제 분류 (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2476">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2477">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2477">Format</span></span>

<span data-ttu-id="3aed1-2478">사전</span><span class="sxs-lookup"><span data-stu-id="3aed1-2478">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2479">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2479">Pattern</span></span>

<span data-ttu-id="3aed1-2480">Keyword</span><span class="sxs-lookup"><span data-stu-id="3aed1-2480">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2481">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2481">Checksum</span></span>

<span data-ttu-id="3aed1-2482">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2482">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2483">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2483">Definition</span></span>

<span data-ttu-id="3aed1-2484">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2484">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2485">Dictionary_icd_10_updated에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2485">A keyword from Dictionary_icd_10_updated is found.</span></span>
- <span data-ttu-id="3aed1-2486">Dictionary_icd_10_codes에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2486">A keyword from Dictionary_icd_10_codes is found.</span></span>

<span data-ttu-id="3aed1-2487">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2487">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2488">업데이트 된 Dictionary_icd_10_ 키워드를 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2488">A keyword from Dictionary_icd_10_ updated is found.</span></span>

```xml
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_updated" />
          <Match idRef="Dictionary_icd_10_codes" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Dictionary_icd_10_updated" />
        </Pattern>

```

<span data-ttu-id="3aed1-2489">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2489">Keywords</span></span>

<span data-ttu-id="3aed1-2490">[Diseases의 국제 분류, 10 번째 개정판, 임상 수정 (icd-10CM)](https://go.microsoft.com/fwlink/?linkid=852604)을 기반으로 하는 Dictionary_icd_10_updated 키워드 사전의 모든 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2490">Any term from the Dictionary_icd_10_updated keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="3aed1-2491">이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2491">This type looks only for the term, not the insurance codes.</span></span>

<span data-ttu-id="3aed1-2492">[Diseases의 국제 분류, 10 번째 개정판, 임상 수정 (icd-10CM)](https://go.microsoft.com/fwlink/?linkid=852604)을 기반으로 하는 Dictionary_icd_10_codes 키워드 사전의 모든 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2492">Any term from the Dictionary_icd_10_codes keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="3aed1-2493">이 유형은 설명에 해당 하는 보험 코드 에서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2493">This type looks only for insurance codes, not the description.</span></span>

## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="3aed1-2494">Diseases의 국제 분류 (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2494">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2495">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2495">Format</span></span>

<span data-ttu-id="3aed1-2496">사전</span><span class="sxs-lookup"><span data-stu-id="3aed1-2496">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2497">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2497">Pattern</span></span>

<span data-ttu-id="3aed1-2498">Keyword</span><span class="sxs-lookup"><span data-stu-id="3aed1-2498">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2499">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2499">Checksum</span></span>

<span data-ttu-id="3aed1-2500">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2500">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2501">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2501">Definition</span></span>

<span data-ttu-id="3aed1-2502">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2502">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2503">Dictionary_icd_9_updated에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2503">A keyword from Dictionary_icd_9_updated is found.</span></span>
- <span data-ttu-id="3aed1-2504">Dictionary_icd_9_codes에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2504">A keyword from Dictionary_icd_9_codes is found.</span></span>

<span data-ttu-id="3aed1-2505">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2505">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2506">Dictionary_icd_9_updated에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2506">A keyword from Dictionary_icd_9_updated is found.</span></span>

```xml
    <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_updated" />
          <Match idRef="Dictionary_icd_9_codes" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Dictionary_icd_9_updated" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2507">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2507">Keywords</span></span>

<span data-ttu-id="3aed1-2508">[Diseases, 아홉 번째 Revision, 임상 수정 (icd-9CM)의 국가별 분류](https://go.microsoft.com/fwlink/?linkid=852605)를 기반으로 하는 Dictionary_icd_9_updated 키워드 사전의 모든 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2508">Any term from the Dictionary_icd_9_updated keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="3aed1-2509">이 유형은 보험 코드가 아니라 용어에 대해서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2509">This type looks only for the term, not the insurance codes.</span></span>

<span data-ttu-id="3aed1-2510">[Diseases, 아홉 번째 Revision, 임상 수정 (icd-9CM)의 국가별 분류](https://go.microsoft.com/fwlink/?linkid=852605)를 기반으로 하는 Dictionary_icd_9_codes 키워드 사전의 모든 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2510">Any term from the Dictionary_icd_9_codes keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="3aed1-2511">이 유형은 설명에 해당 하는 보험 코드 에서만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2511">This type looks only for insurance codes, not the description.</span></span>

## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="3aed1-2512">아일랜드 PPS(개인 공공 서비스) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2512">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2513">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2513">Format</span></span>

<span data-ttu-id="3aed1-2514">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="3aed1-2514">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="3aed1-2515">7자리 숫자와 1-2개 문자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2515">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="3aed1-2516">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="3aed1-2516">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="3aed1-2517">7자리 숫자와 2개 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2517">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2518">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2518">Pattern</span></span>

<span data-ttu-id="3aed1-2519">이전 형식 (31 년 12 월 2012 일까지):</span><span class="sxs-lookup"><span data-stu-id="3aed1-2519">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="3aed1-2520">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2520">Seven digits</span></span> 
- <span data-ttu-id="3aed1-2521">1-2개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2521">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="3aed1-2522">새 형식 (1 년 1 월 2013 및 이후):</span><span class="sxs-lookup"><span data-stu-id="3aed1-2522">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="3aed1-2523">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2523">Seven digits</span></span> 
- <span data-ttu-id="3aed1-2524">알파벳 검사 숫자에 해당하는 문자 1개(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="3aed1-2524">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="3aed1-2525">문자 "A" 또는 "H"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2525">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2526">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2526">Checksum</span></span>

<span data-ttu-id="3aed1-2527">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2527">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2528">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2528">Definition</span></span>

<span data-ttu-id="3aed1-2529">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2529">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2530">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2530">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2531">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2531">One of the following is true:</span></span>
    - <span data-ttu-id="3aed1-2532">Keyword_ireland_pps에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2532">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="3aed1-2533">Func_eu_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2533">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="3aed1-2534">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2534">The checksum passes.</span></span>

<span data-ttu-id="3aed1-2535">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2535">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2536">Func_ireland_pps 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2536">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2537">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2537">The checksum passes.</span></span>

```xml
<!-- Ireland Personal Public Service (PPS) Number -->
<Entity id="1cdb674d-c19a-4fcf-9f4b-7f56cc87345a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_ireland_pps"/>
     <Any minMatches="1">
  <Match idRef="Keyword_ireland_pps"/>
  <Match idRef="Func_eu_date"/>
     </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_ireland_pps"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2538">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2538">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="3aed1-2539">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="3aed1-2539">Keyword_ireland_pps</span></span>

- <span data-ttu-id="3aed1-2540">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2540">Personal Public Service Number</span></span> 
- <span data-ttu-id="3aed1-2541">PPS Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2541">PPS Number</span></span> 
- <span data-ttu-id="3aed1-2542">PPS Num</span><span class="sxs-lookup"><span data-stu-id="3aed1-2542">PPS Num</span></span> 
- <span data-ttu-id="3aed1-2543">PPS No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2543">PPS No.</span></span> 
- <span data-ttu-id="3aed1-2544">PPS #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2544">PPS #</span></span> 
- <span data-ttu-id="3aed1-2545">.PPS #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2545">PPS#</span></span> 
- <span data-ttu-id="3aed1-2546">PPSN</span><span class="sxs-lookup"><span data-stu-id="3aed1-2546">PPSN</span></span> 
- <span data-ttu-id="3aed1-2547">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2547">Public Services Card</span></span> 
- <span data-ttu-id="3aed1-2548">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="3aed1-2548">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="3aed1-2549">Uimh</span><span class="sxs-lookup"><span data-stu-id="3aed1-2549">Uimh.</span></span> <span data-ttu-id="3aed1-2550">PSP</span><span class="sxs-lookup"><span data-stu-id="3aed1-2550">PSP</span></span> 
- <span data-ttu-id="3aed1-2551">PSP</span><span class="sxs-lookup"><span data-stu-id="3aed1-2551">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="3aed1-2552">이스라엘 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2552">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2553">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2553">Format</span></span>

<span data-ttu-id="3aed1-2554">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2554">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2555">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2555">Pattern</span></span>

<span data-ttu-id="3aed1-2556">서식이</span><span class="sxs-lookup"><span data-stu-id="3aed1-2556">Formatted:</span></span>
- <span data-ttu-id="3aed1-2557">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2557">Two digits</span></span> 
- <span data-ttu-id="3aed1-2558">대시 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-2558">A dash</span></span> 
- <span data-ttu-id="3aed1-2559">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2559">Three digits</span></span> 
- <span data-ttu-id="3aed1-2560">대시 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-2560">A dash</span></span> 
- <span data-ttu-id="3aed1-2561">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2561">Eight digits</span></span>

<span data-ttu-id="3aed1-2562">서식</span><span class="sxs-lookup"><span data-stu-id="3aed1-2562">Unformatted:</span></span>
- <span data-ttu-id="3aed1-2563">13자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2563">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2564">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2564">Checksum</span></span>

<span data-ttu-id="3aed1-2565">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2565">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2566">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2566">Definition</span></span>

<span data-ttu-id="3aed1-2567">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2567">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2568">Regex_israel_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2568">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2569">Keyword_israel_bank_account_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2569">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```xml
<!-- Israel Bank Account Number -->
<Entity id="7d08b2ff-a0b9-437f-957c-aeddbf9b2b25" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_israel_bank_account_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_israel_bank_account_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2570">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2570">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="3aed1-2571">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2571">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="3aed1-2572">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2572">Bank Account Number</span></span> 
- <span data-ttu-id="3aed1-2573">Bank Account</span><span class="sxs-lookup"><span data-stu-id="3aed1-2573">Bank Account</span></span> 
- <span data-ttu-id="3aed1-2574">Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2574">Account Number</span></span> 
- <span data-ttu-id="3aed1-2575">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="3aed1-2575">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="3aed1-2576">이스라엘 국가 ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-2576">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2577">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2577">Format</span></span>

<span data-ttu-id="3aed1-2578">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2578">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2579">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2579">Pattern</span></span>

<span data-ttu-id="3aed1-2580">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2580">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2581">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2581">Checksum</span></span>

<span data-ttu-id="3aed1-2582">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2582">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2583">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2583">Definition</span></span>

<span data-ttu-id="3aed1-2584">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2585">Func_israeli_national_id_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2585">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2586">Keyword_Israel_National_ID의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2586">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="3aed1-2587">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2587">The checksum passes.</span></span>

```xml
<!-- Israel National ID Number -->
<Entity id="e05881f5-1db1-418c-89aa-a3ac5c5277ee" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_israeli_national_id_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_Israel_National_ID" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2588">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2588">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="3aed1-2589">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-2589">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="3aed1-2590">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="3aed1-2590">מספר זהות</span></span> 
- <span data-ttu-id="3aed1-2591">National ID Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2591">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="3aed1-2592">이탈리아 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2592">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2593">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2593">Format</span></span>

<span data-ttu-id="3aed1-2594">10개의 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-2594">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2595">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2595">Pattern</span></span>

- <span data-ttu-id="3aed1-2596">10개의 문자 및 숫자 조합:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2596">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="3aed1-2597">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2597">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-2598">문자 "A" 또는 "V"(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2598">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-2599">7개 문자(대/소문자 구분 안 함), 숫자 또는 밑줄 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2599">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="3aed1-2600">1개 문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2600">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2601">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2601">Checksum</span></span>

<span data-ttu-id="3aed1-2602">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2602">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2603">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2603">Definition</span></span>

<span data-ttu-id="3aed1-2604">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2604">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2605">Regex_italy_drivers_license_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2605">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2606">Keyword_italy_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2606">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```xml
<!-- Italy Driver's license Number -->
<Entity id="97d6244f-9157-41bd-8e0c-9d669a5c4d71" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_italy_drivers_license_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_italy_drivers_license_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2607">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2607">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="3aed1-2608">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2608">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="3aed1-2609">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="3aed1-2609">numero di patente di guida</span></span> 
- <span data-ttu-id="3aed1-2610">patente di guida</span><span class="sxs-lookup"><span data-stu-id="3aed1-2610">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="3aed1-2611">일본 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2611">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2612">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2612">Format</span></span>

<span data-ttu-id="3aed1-2613">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2613">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2614">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2614">Pattern</span></span>

<span data-ttu-id="3aed1-2615">은행 계좌 번호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2615">Bank account number:</span></span>
- <span data-ttu-id="3aed1-2616">7 또는 8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2616">Seven or eight digits</span></span>
- <span data-ttu-id="3aed1-2617">은행 계좌 지점 코드:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2617">Bank account branch code:</span></span>
- <span data-ttu-id="3aed1-2618">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2618">Four digits</span></span> 
- <span data-ttu-id="3aed1-2619">공백 또는 대시(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2619">A space or dash (optional)</span></span> 
- <span data-ttu-id="3aed1-2620">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2620">Three digits</span></span>

<span data-ttu-id="3aed1-2621">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2621">Checksum</span></span>

<span data-ttu-id="3aed1-2622">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2622">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2623">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2623">Definition</span></span>

<span data-ttu-id="3aed1-2624">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2624">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2625">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2625">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2626">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2626">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="3aed1-2627">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2627">One of the following is true:</span></span>
- <span data-ttu-id="3aed1-2628">Func_jp_bank_account_branch_code 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2628">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2629">Keyword_jp_bank_branch_code의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2629">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="3aed1-2630">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2630">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2631">Func_jp_bank_account 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2631">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2632">Keyword_jp_bank_account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2632">A keyword from Keyword_jp_bank_account is found.</span></span>

```xml
<!-- Japan Bank Account Number -->
<Entity id="d354f95b-96ee-4b80-80bc-4377312b55bc" patternsProximity="300" recommendedConfidence="75">
  <Version minEngineVersion="15.01.0131.000">
    <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_jp_bank_account" />
          <Match idRef="Keyword_jp_bank_account" />
          <Any minMatches="1">
            <Match idRef="Func_jp_bank_account_branch_code" />
            <Match idRef="Keyword_jp_bank_branch_code" />
          </Any>
      </Pattern>
  </Version>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_bank_account" />
        <Match idRef="Keyword_jp_bank_account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2633">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2633">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="3aed1-2634">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="3aed1-2634">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="3aed1-2635">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2635">Checking Account Number</span></span> 
- <span data-ttu-id="3aed1-2636">Checking Account</span><span class="sxs-lookup"><span data-stu-id="3aed1-2636">Checking Account</span></span> 
- <span data-ttu-id="3aed1-2637">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2637">Checking Account #</span></span> 
- <span data-ttu-id="3aed1-2638">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2638">Checking Acct Number</span></span> 
- <span data-ttu-id="3aed1-2639">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2639">Checking Acct #</span></span> 
- <span data-ttu-id="3aed1-2640">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2640">Checking Acct No.</span></span> 
- <span data-ttu-id="3aed1-2641">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2641">Checking Account No.</span></span> 
- <span data-ttu-id="3aed1-2642">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2642">Bank Account Number</span></span> 
- <span data-ttu-id="3aed1-2643">Bank Account</span><span class="sxs-lookup"><span data-stu-id="3aed1-2643">Bank Account</span></span> 
- <span data-ttu-id="3aed1-2644">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2644">Bank Account #</span></span> 
- <span data-ttu-id="3aed1-2645">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2645">Bank Acct Number</span></span> 
- <span data-ttu-id="3aed1-2646">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2646">Bank Acct #</span></span> 
- <span data-ttu-id="3aed1-2647">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2647">Bank Acct No.</span></span> 
- <span data-ttu-id="3aed1-2648">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2648">Bank Account No.</span></span> 
- <span data-ttu-id="3aed1-2649">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2649">Savings Account Number</span></span> 
- <span data-ttu-id="3aed1-2650">Savings Account</span><span class="sxs-lookup"><span data-stu-id="3aed1-2650">Savings Account</span></span> 
- <span data-ttu-id="3aed1-2651">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2651">Savings Account #</span></span> 
- <span data-ttu-id="3aed1-2652">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2652">Savings Acct Number</span></span> 
- <span data-ttu-id="3aed1-2653">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2653">Savings Acct #</span></span> 
- <span data-ttu-id="3aed1-2654">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2654">Savings Acct No.</span></span> 
- <span data-ttu-id="3aed1-2655">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2655">Savings Account No.</span></span> 
- <span data-ttu-id="3aed1-2656">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2656">Debit Account Number</span></span> 
- <span data-ttu-id="3aed1-2657">Debit Account</span><span class="sxs-lookup"><span data-stu-id="3aed1-2657">Debit Account</span></span> 
- <span data-ttu-id="3aed1-2658">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2658">Debit Account #</span></span> 
- <span data-ttu-id="3aed1-2659">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2659">Debit Acct Number</span></span> 
- <span data-ttu-id="3aed1-2660">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2660">Debit Acct #</span></span> 
- <span data-ttu-id="3aed1-2661">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2661">Debit Acct No.</span></span> 
- <span data-ttu-id="3aed1-2662">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2662">Debit Account No.</span></span> 
- <span data-ttu-id="3aed1-2663">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="3aed1-2663">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="3aed1-2664">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="3aed1-2664">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="3aed1-2665">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="3aed1-2665">＃勘定の確認</span></span> 
- <span data-ttu-id="3aed1-2666">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="3aed1-2666">勘定番号の確認</span></span> 
- <span data-ttu-id="3aed1-2667">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="3aed1-2667">口座番号の確認</span></span> 
- <span data-ttu-id="3aed1-2668">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2668">銀行口座番号</span></span> 
- <span data-ttu-id="3aed1-2669">銀行口座</span><span class="sxs-lookup"><span data-stu-id="3aed1-2669">銀行口座</span></span> 
- <span data-ttu-id="3aed1-2670">銀行口座＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-2670">銀行口座＃</span></span> 
- <span data-ttu-id="3aed1-2671">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2671">銀行の勘定番号</span></span> 
- <span data-ttu-id="3aed1-2672">銀行のacct＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-2672">銀行のacct＃</span></span> 
- <span data-ttu-id="3aed1-2673">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="3aed1-2673">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="3aed1-2674">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2674">銀行口座番号</span></span>
- <span data-ttu-id="3aed1-2675">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2675">普通預金口座番号</span></span> 
- <span data-ttu-id="3aed1-2676">預金口座</span><span class="sxs-lookup"><span data-stu-id="3aed1-2676">預金口座</span></span> 
- <span data-ttu-id="3aed1-2677">貯蓄口座＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-2677">貯蓄口座＃</span></span> 
- <span data-ttu-id="3aed1-2678">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="3aed1-2678">貯蓄勘定の数</span></span> 
- <span data-ttu-id="3aed1-2679">貯蓄勘定＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-2679">貯蓄勘定＃</span></span> 
- <span data-ttu-id="3aed1-2680">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2680">貯蓄勘定番号</span></span> 
- <span data-ttu-id="3aed1-2681">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2681">普通預金口座番号</span></span> 
- <span data-ttu-id="3aed1-2682">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2682">引き落とし口座番号</span></span> 
- <span data-ttu-id="3aed1-2683">口座番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2683">口座番号</span></span> 
- <span data-ttu-id="3aed1-2684">口座番号＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-2684">口座番号＃</span></span> 
- <span data-ttu-id="3aed1-2685">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2685">デビットのacct番号</span></span> 
- <span data-ttu-id="3aed1-2686">デビット勘定＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-2686">デビット勘定＃</span></span> 
- <span data-ttu-id="3aed1-2687">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2687">デビットACCTの番号</span></span> 
- <span data-ttu-id="3aed1-2688">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2688">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="3aed1-2689">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="3aed1-2689">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="3aed1-2690">Otemachi</span><span class="sxs-lookup"><span data-stu-id="3aed1-2690">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="3aed1-2691">일본 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2691">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2692">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2692">Format</span></span>

<span data-ttu-id="3aed1-2693">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2693">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2694">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2694">Pattern</span></span>

<span data-ttu-id="3aed1-2695">12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2695">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2696">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2696">Checksum</span></span>

<span data-ttu-id="3aed1-2697">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2697">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2698">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2698">Definition</span></span>

<span data-ttu-id="3aed1-2699">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2699">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2700">Func_jp_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2700">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2701">Keyword_jp_drivers_license_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2701">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```xml
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2702">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2702">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="3aed1-2703">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2703">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="3aed1-2704">dl #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2704">dl#</span></span> 
- <span data-ttu-id="3aed1-2705">DL</span><span class="sxs-lookup"><span data-stu-id="3aed1-2705">DL＃</span></span> 
- <span data-ttu-id="3aed1-2706">된다 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2706">dls#</span></span> 
- <span data-ttu-id="3aed1-2707">된다</span><span class="sxs-lookup"><span data-stu-id="3aed1-2707">DLS＃</span></span> 
- <span data-ttu-id="3aed1-2708">driver license</span><span class="sxs-lookup"><span data-stu-id="3aed1-2708">driver license</span></span> 
- <span data-ttu-id="3aed1-2709">driver licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-2709">driver licenses</span></span> 
- <span data-ttu-id="3aed1-2710">drivers license</span><span class="sxs-lookup"><span data-stu-id="3aed1-2710">drivers license</span></span> 
- <span data-ttu-id="3aed1-2711">driver's license</span><span class="sxs-lookup"><span data-stu-id="3aed1-2711">driver's license</span></span> 
- <span data-ttu-id="3aed1-2712">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-2712">drivers licenses</span></span> 
- <span data-ttu-id="3aed1-2713">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-2713">driver's licenses</span></span> 
- <span data-ttu-id="3aed1-2714">driving licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-2714">driving licence</span></span> 
- <span data-ttu-id="3aed1-2715">lic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2715">lic#</span></span> 
- <span data-ttu-id="3aed1-2716">LIC</span><span class="sxs-lookup"><span data-stu-id="3aed1-2716">LIC＃</span></span> 
- <span data-ttu-id="3aed1-2717">driver'lics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2717">lics#</span></span> 
- <span data-ttu-id="3aed1-2718">state id</span><span class="sxs-lookup"><span data-stu-id="3aed1-2718">state id</span></span> 
- <span data-ttu-id="3aed1-2719">state identification</span><span class="sxs-lookup"><span data-stu-id="3aed1-2719">state identification</span></span> 
- <span data-ttu-id="3aed1-2720">state identification number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2720">state identification number</span></span> 
- <span data-ttu-id="3aed1-2721">低所得国＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-2721">低所得国＃</span></span> 
- <span data-ttu-id="3aed1-2722">免許証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2722">免許証</span></span> 
- <span data-ttu-id="3aed1-2723">状態ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-2723">状態ID</span></span>
- <span data-ttu-id="3aed1-2724">状態の識別</span><span class="sxs-lookup"><span data-stu-id="3aed1-2724">状態の識別</span></span> 
- <span data-ttu-id="3aed1-2725">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2725">状態の識別番号</span></span> 
- <span data-ttu-id="3aed1-2726">運転免許</span><span class="sxs-lookup"><span data-stu-id="3aed1-2726">運転免許</span></span> 
- <span data-ttu-id="3aed1-2727">運転免許証</span><span class="sxs-lookup"><span data-stu-id="3aed1-2727">運転免許証</span></span> 
- <span data-ttu-id="3aed1-2728">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2728">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="3aed1-2729">일본 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2729">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2730">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2730">Format</span></span>

<span data-ttu-id="3aed1-2731">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2731">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2732">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2732">Pattern</span></span>

<span data-ttu-id="3aed1-2733">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2733">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2734">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2734">Checksum</span></span>

<span data-ttu-id="3aed1-2735">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2736">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2736">Definition</span></span>

<span data-ttu-id="3aed1-2737">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2737">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2738">Func_jp_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2738">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2739">Keyword_jp_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2739">A keyword from Keyword_jp_passport is found.</span></span>

```xml
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2740">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2740">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="3aed1-2741">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-2741">Keyword_jp_passport</span></span>

- <span data-ttu-id="3aed1-2742">パスポート</span><span class="sxs-lookup"><span data-stu-id="3aed1-2742">パスポート</span></span> 
- <span data-ttu-id="3aed1-2743">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2743">パスポート番号</span></span> 
- <span data-ttu-id="3aed1-2744">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="3aed1-2744">パスポートのNum</span></span> 
- <span data-ttu-id="3aed1-2745">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-2745">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="3aed1-2746">일본 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2746">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2747">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2747">Format</span></span>

<span data-ttu-id="3aed1-2748">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2748">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2749">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2749">Pattern</span></span>

<span data-ttu-id="3aed1-2750">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2750">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2751">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2751">Checksum</span></span>

<span data-ttu-id="3aed1-2752">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2752">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2753">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2753">Definition</span></span>

<span data-ttu-id="3aed1-2754">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2754">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2755">Func_jp_resident_registration_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2755">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2756">Keyword_jp_resident_registration_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2756">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```xml
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2757">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2757">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="3aed1-2758">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2758">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="3aed1-2759">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2759">Resident Registration Number</span></span>
- <span data-ttu-id="3aed1-2760">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2760">Resident Register Number</span></span> 
- <span data-ttu-id="3aed1-2761">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2761">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="3aed1-2762">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2762">Resident Registration No.</span></span> 
- <span data-ttu-id="3aed1-2763">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2763">Resident Register No.</span></span> 
- <span data-ttu-id="3aed1-2764">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2764">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="3aed1-2765">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2765">Basic Resident Register No.</span></span> 
- <span data-ttu-id="3aed1-2766">住民登録番号、登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="3aed1-2766">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="3aed1-2767">住民基本登録番号、登録番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2767">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="3aed1-2768">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="3aed1-2768">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="3aed1-2769">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2769">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="3aed1-2770">일본 SIN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2770">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2771">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2771">Format</span></span>

<span data-ttu-id="3aed1-2772">7-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2772">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2773">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2773">Pattern</span></span>

<span data-ttu-id="3aed1-2774">7-12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2774">7-12 digits:</span></span>
- <span data-ttu-id="3aed1-2775">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2775">Four digits</span></span> 
- <span data-ttu-id="3aed1-2776">하이픈 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2776">A hyphen (optional)</span></span> 
- <span data-ttu-id="3aed1-2777">6 자리 숫자 또는</span><span class="sxs-lookup"><span data-stu-id="3aed1-2777">Six digits OR</span></span>
- <span data-ttu-id="3aed1-2778">7-12자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2778">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2779">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2779">Checksum</span></span>

<span data-ttu-id="3aed1-2780">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2780">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2781">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2781">Definition</span></span>

<span data-ttu-id="3aed1-2782">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2782">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2783">Func_jp_sin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2783">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2784">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2784">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="3aed1-2785">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2785">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2786">Func_jp_sin_pre_1997 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2786">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2787">Keyword_jp_sin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2787">A keyword from Keyword_jp_sin is found.</span></span>

```xml
<!-- Japan Social Insurance Number -->
<Entity id="c840e719-0896-45bb-84fd-1ed5c95e45ff" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_jp_sin" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_sin_pre_1997" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2788">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2788">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="3aed1-2789">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="3aed1-2789">Keyword_jp_sin</span></span>

- <span data-ttu-id="3aed1-2790">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2790">Social Insurance No.</span></span> 
- <span data-ttu-id="3aed1-2791">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="3aed1-2791">Social Insurance Num</span></span> 
- <span data-ttu-id="3aed1-2792">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2792">Social Insurance Number</span></span> 
- <span data-ttu-id="3aed1-2793">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="3aed1-2793">社会保険のテンキー</span></span> 
- <span data-ttu-id="3aed1-2794">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2794">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="3aed1-2795">일본어 거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2795">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2796">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2796">Format</span></span>

<span data-ttu-id="3aed1-2797">12 개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2797">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2798">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2798">Pattern</span></span>

<span data-ttu-id="3aed1-2799">12 개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2799">12 letters and digits:</span></span>
- <span data-ttu-id="3aed1-2800">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2800">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="3aed1-2801">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2801">Eight digits</span></span> 
- <span data-ttu-id="3aed1-2802">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2802">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2803">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2803">Checksum</span></span>

<span data-ttu-id="3aed1-2804">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2804">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2805">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2805">Definition</span></span>

<span data-ttu-id="3aed1-2806">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2806">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2807">정규식 Regex_jp_residence_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2807">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2808">Keyword_jp_residence_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2808">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```xml
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2809">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2809">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="3aed1-2810">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2810">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="3aed1-2811">거주지 카드 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2811">Residence card number</span></span>
- <span data-ttu-id="3aed1-2812">거주지 카드 아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2812">Residence card no</span></span>
- <span data-ttu-id="3aed1-2813">거주지 카드 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-2813">Residence card #</span></span>
- <span data-ttu-id="3aed1-2814">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-2814">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="3aed1-2815">말레이시아 ID 카드 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2815">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2816">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2816">Format</span></span>

<span data-ttu-id="3aed1-2817">선택적으로 하이픈을 포함하는 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2817">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2818">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2818">Pattern</span></span>

<span data-ttu-id="3aed1-2819">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2819">12 digits:</span></span>
- <span data-ttu-id="3aed1-2820">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2820">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="3aed1-2821">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2821">A dash (optional)</span></span> 
- <span data-ttu-id="3aed1-2822">2개 문자로 이루어진 출생지 코드 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2822">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="3aed1-2823">대시(옵션)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2823">A dash (optional)</span></span> 
- <span data-ttu-id="3aed1-2824">임의의 3자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2824">Three random digits</span></span> 
- <span data-ttu-id="3aed1-2825">1자리 성별 코드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2825">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2826">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2826">Checksum</span></span>

<span data-ttu-id="3aed1-2827">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2827">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2828">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2828">Definition</span></span>

<span data-ttu-id="3aed1-2829">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2829">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2830">정규식 Regex_malaysia_id_card_number 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2830">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2831">Keyword_malaysia_id_card_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2831">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```xml
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2832">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2832">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="3aed1-2833">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2833">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="3aed1-2834">디지털 응용 프로그램 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2834">digital application card</span></span>
- <span data-ttu-id="3aed1-2835">i/c</span><span class="sxs-lookup"><span data-stu-id="3aed1-2835">i/c</span></span>
- <span data-ttu-id="3aed1-2836">i/c 아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2836">i/c no</span></span>
- <span data-ttu-id="3aed1-2837">비용</span><span class="sxs-lookup"><span data-stu-id="3aed1-2837">ic</span></span>
- <span data-ttu-id="3aed1-2838">ic 아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2838">ic no</span></span>
- <span data-ttu-id="3aed1-2839">id card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2839">id card</span></span>
- <span data-ttu-id="3aed1-2840">식별 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2840">identification Card</span></span>
- <span data-ttu-id="3aed1-2841">identity card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2841">identity card</span></span>
- <span data-ttu-id="3aed1-2842">k/p</span><span class="sxs-lookup"><span data-stu-id="3aed1-2842">k/p</span></span>
- <span data-ttu-id="3aed1-2843">k/p 아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2843">k/p no</span></span>
- <span data-ttu-id="3aed1-2844">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="3aed1-2844">kad akuan diri</span></span>
- <span data-ttu-id="3aed1-2845">kad aplikasi 디지털</span><span class="sxs-lookup"><span data-stu-id="3aed1-2845">kad aplikasi digital</span></span>
- <span data-ttu-id="3aed1-2846">kad pengenalan 말레이시아</span><span class="sxs-lookup"><span data-stu-id="3aed1-2846">kad pengenalan malaysia</span></span>
- <span data-ttu-id="3aed1-2847">kp</span><span class="sxs-lookup"><span data-stu-id="3aed1-2847">kp</span></span>
- <span data-ttu-id="3aed1-2848">kp 아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2848">kp no</span></span>
- <span data-ttu-id="3aed1-2849">mykad</span><span class="sxs-lookup"><span data-stu-id="3aed1-2849">mykad</span></span>
- <span data-ttu-id="3aed1-2850">mykas</span><span class="sxs-lookup"><span data-stu-id="3aed1-2850">mykas</span></span>
- <span data-ttu-id="3aed1-2851">mykid</span><span class="sxs-lookup"><span data-stu-id="3aed1-2851">mykid</span></span>
- <span data-ttu-id="3aed1-2852">mypr</span><span class="sxs-lookup"><span data-stu-id="3aed1-2852">mypr</span></span>
- <span data-ttu-id="3aed1-2853">myta</span><span class="sxs-lookup"><span data-stu-id="3aed1-2853">mytentera</span></span>
- <span data-ttu-id="3aed1-2854">말레이시아 id 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2854">malaysia identity card</span></span>
- <span data-ttu-id="3aed1-2855">말레이지아 id 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2855">malaysian identity card</span></span>
- <span data-ttu-id="3aed1-2856">nric</span><span class="sxs-lookup"><span data-stu-id="3aed1-2856">nric</span></span>
- <span data-ttu-id="3aed1-2857">개인 식별 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2857">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="3aed1-2858">네덜란드 시민 서비스(BSN) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2858">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2859">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2859">Format</span></span>

<span data-ttu-id="3aed1-2860">선택적으로 공백을 포함하는 8-9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2860">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2861">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2861">Pattern</span></span>

<span data-ttu-id="3aed1-2862">8-9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2862">8-9 digits:</span></span>
- <span data-ttu-id="3aed1-2863">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2863">Three digits</span></span> 
- <span data-ttu-id="3aed1-2864">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2864">A space (optional)</span></span> 
- <span data-ttu-id="3aed1-2865">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2865">Three digits</span></span> 
- <span data-ttu-id="3aed1-2866">공백 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2866">A space (optional)</span></span> 
- <span data-ttu-id="3aed1-2867">2-3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2867">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2868">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2868">Checksum</span></span>

<span data-ttu-id="3aed1-2869">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2869">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2870">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2870">Definition</span></span>

<span data-ttu-id="3aed1-2871">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2871">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2872">Func_netherlands_bsn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2872">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2873">Keyword_netherlands_bsn에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2873">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="3aed1-2874">Func_eu_date2 함수는 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2874">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="3aed1-2875">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2875">The checksum passes.</span></span>

```xml
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2876">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2876">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="3aed1-2877">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="3aed1-2877">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="3aed1-2878">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2878">Citizen service number</span></span> 
- <span data-ttu-id="3aed1-2879">BSN</span><span class="sxs-lookup"><span data-stu-id="3aed1-2879">BSN</span></span> 
- <span data-ttu-id="3aed1-2880">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2880">Burgerservicenummer</span></span> 
- <span data-ttu-id="3aed1-2881">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2881">Sofinummer</span></span> 
- <span data-ttu-id="3aed1-2882">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2882">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="3aed1-2883">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2883">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="3aed1-2884">뉴질랜드 보건부 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2884">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2885">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2885">Format</span></span>

<span data-ttu-id="3aed1-2886">3개 문자, 공백 1개(선택 사항) 및 4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2886">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2887">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2887">Pattern</span></span>

<span data-ttu-id="3aed1-2888">3 개의 문자 (대/소문자 구분 안 함) 공백 (선택 사항) 4 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2888">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2889">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2889">Checksum</span></span>

<span data-ttu-id="3aed1-2890">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2890">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2891">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2891">Definition</span></span>

<span data-ttu-id="3aed1-2892">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2892">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2893">Func_new_zealand_ministry_of_health_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2893">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2894">Keyword_nz_terms의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2894">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="3aed1-2895">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2895">The checksum passes.</span></span>

```xml
<!-- New Zealand Health Number -->
<Entity id="2b71c1c8-d14e-4430-82dc-fd1ed6bf05c7" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_new_zealand_ministry_of_health_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_nz_terms" />
        </Any>
    </Pattern>
</Entity>
```

<span data-ttu-id="3aed1-2896">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2896">Keywords</span></span>

<span data-ttu-id="3aed1-2897">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="3aed1-2897">Keyword_nz_terms</span></span>

- <span data-ttu-id="3aed1-2898">NHI</span><span class="sxs-lookup"><span data-stu-id="3aed1-2898">NHI</span></span> 
- <span data-ttu-id="3aed1-2899">New Zealand</span><span class="sxs-lookup"><span data-stu-id="3aed1-2899">New Zealand</span></span> 
- <span data-ttu-id="3aed1-2900">상태</span><span class="sxs-lookup"><span data-stu-id="3aed1-2900">Health</span></span> 
- <span data-ttu-id="3aed1-2901">처리가</span><span class="sxs-lookup"><span data-stu-id="3aed1-2901">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="3aed1-2902">Norway Identification Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2902">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2903">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2903">Format</span></span>

<span data-ttu-id="3aed1-2904">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2904">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2905">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2905">Pattern</span></span>

<span data-ttu-id="3aed1-2906">11자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2906">11 digits:</span></span>
- <span data-ttu-id="3aed1-2907">생년월일에 해당하는 DDMMYY 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2907">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="3aed1-2908">3자리 개인 번호 </span><span class="sxs-lookup"><span data-stu-id="3aed1-2908">Three-digit individual number</span></span> 
- <span data-ttu-id="3aed1-2909">2개의 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2909">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2910">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2910">Checksum</span></span>

<span data-ttu-id="3aed1-2911">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2911">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2912">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2912">Definition</span></span>

<span data-ttu-id="3aed1-2913">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2913">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2914">Func_norway_id_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2914">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2915">Keyword_norway_id_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2915">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="3aed1-2916">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2916">The checksum passes.</span></span>
- <span data-ttu-id="3aed1-2917">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2917">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2918">Func_norway_id_numbe 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2918">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2919">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2919">The checksum passes.</span></span>

```xml
<!-- Norway Identification Number -->
<Entity id="d4c8a798-e9f2-4bd3-9652-500d24080fc3" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_norway_id_number"/>
     <Match idRef="Keyword_norway_id_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_norway_id_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2920">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2920">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="3aed1-2921">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2921">Keyword_norway_id_number</span></span>

- <span data-ttu-id="3aed1-2922">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2922">Personal identification number</span></span>
- <span data-ttu-id="3aed1-2923">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2923">Norwegian ID Number</span></span>
- <span data-ttu-id="3aed1-2924">ID Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2924">ID Number</span></span>
- <span data-ttu-id="3aed1-2925">확인과</span><span class="sxs-lookup"><span data-stu-id="3aed1-2925">Identification</span></span>
- <span data-ttu-id="3aed1-2926">Personnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2926">Personnummer</span></span>
- <span data-ttu-id="3aed1-2927">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="3aed1-2927">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="3aed1-2928">필리핀 통합 다목적 ID 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-2928">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2929">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2929">Format</span></span>

<span data-ttu-id="3aed1-2930">하이픈으로 구분된 12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2930">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2931">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2931">Pattern</span></span>

<span data-ttu-id="3aed1-2932">12자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-2932">12 digits:</span></span>
- <span data-ttu-id="3aed1-2933">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2933">Four digits</span></span> 
- <span data-ttu-id="3aed1-2934">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-2934">A hyphen</span></span> 
- <span data-ttu-id="3aed1-2935">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2935">Seven digits</span></span> 
- <span data-ttu-id="3aed1-2936">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-2936">A hyphen</span></span> 
- <span data-ttu-id="3aed1-2937">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2937">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2938">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2938">Checksum</span></span>

<span data-ttu-id="3aed1-2939">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-2939">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2940">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2940">Definition</span></span>

<span data-ttu-id="3aed1-2941">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2941">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2942">정규식 Regex_philippines_unified_id 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2942">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2943">Keyword_philippines_id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2943">A keyword from Keyword_philippines_id is found.</span></span>

```xml
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2944">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2944">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="3aed1-2945">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="3aed1-2945">Keyword_philippines_id</span></span>

- <span data-ttu-id="3aed1-2946">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-2946">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="3aed1-2947">UMID</span><span class="sxs-lookup"><span data-stu-id="3aed1-2947">UMID</span></span> 
- <span data-ttu-id="3aed1-2948">Identity Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-2948">Identity Card</span></span> 
- <span data-ttu-id="3aed1-2949">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-2949">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="3aed1-2950">폴란드 ID 카드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2950">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2951">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2951">Format</span></span>

<span data-ttu-id="3aed1-2952">3개의 문자 및 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2952">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2953">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2953">Pattern</span></span>

<span data-ttu-id="3aed1-2954">3개의 문자(대/소문자 구분 안 함)와 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2954">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2955">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2955">Checksum</span></span>

<span data-ttu-id="3aed1-2956">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2956">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2957">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2957">Definition</span></span>

<span data-ttu-id="3aed1-2958">DLP 정책은 300 Func_polish_national_id 문자에 근접 한 경우에는이 유형의 중요 한 정보를 검색 하는 것으로 75% 확신 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2958">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="3aed1-2959">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2959">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="3aed1-2960">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2960">The checksum passes.</span></span>

```xml
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2961">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2961">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="3aed1-2962">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2962">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="3aed1-2963">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="3aed1-2963">Dowód osobisty</span></span>
- <span data-ttu-id="3aed1-2964">U r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="3aed1-2964">Numer dowodu osobistego</span></span>
- <span data-ttu-id="3aed1-2965">Nazwa i u r i dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="3aed1-2965">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="3aed1-2966">Nazwa i veiligheid dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="3aed1-2966">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="3aed1-2967">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="3aed1-2967">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="3aed1-2968">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="3aed1-2968">Dowód Tożsamości</span></span>
- <span data-ttu-id="3aed1-2969">dow.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2969">dow.</span></span> <span data-ttu-id="3aed1-2970">르.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2970">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="3aed1-2971">폴란드 국가 ID(PESEL)</span><span class="sxs-lookup"><span data-stu-id="3aed1-2971">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2972">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2972">Format</span></span>

<span data-ttu-id="3aed1-2973">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2973">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2974">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2974">Pattern</span></span>

<span data-ttu-id="3aed1-2975">11자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2975">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2976">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2976">Checksum</span></span>

<span data-ttu-id="3aed1-2977">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2977">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2978">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2978">Definition</span></span>

<span data-ttu-id="3aed1-2979">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2979">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2980">Func_pesel_identification_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2980">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2981">Keyword_pesel_identification_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2981">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="3aed1-2982">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2982">The checksum passes.</span></span>

```xml
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2983">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2983">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="3aed1-2984">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-2984">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="3aed1-2985">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="3aed1-2985">Nr PESEL</span></span>
- <span data-ttu-id="3aed1-2986">PESEL</span><span class="sxs-lookup"><span data-stu-id="3aed1-2986">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="3aed1-2987">폴란드 여권</span><span class="sxs-lookup"><span data-stu-id="3aed1-2987">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-2988">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-2988">Format</span></span>

<span data-ttu-id="3aed1-2989">2개 문자와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2989">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-2990">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-2990">Pattern</span></span>

<span data-ttu-id="3aed1-2991">2개의 문자(대/소문자 구분 안 함)와 7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-2991">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-2992">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-2992">Checksum</span></span>

<span data-ttu-id="3aed1-2993">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-2993">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-2994">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-2994">Definition</span></span>

<span data-ttu-id="3aed1-2995">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2995">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-2996">Func_polish_passport_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2996">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-2997">Keyword_polish_national_id_passport_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2997">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="3aed1-2998">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-2998">The checksum passes.</span></span>

```xml
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-2999">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-2999">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="3aed1-3000">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3000">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="3aed1-3001">U r i (zportu)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3001">Numer paszportu</span></span>
- <span data-ttu-id="3aed1-3002">Veiligheid.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3002">Nr.</span></span> <span data-ttu-id="3aed1-3003">고 zportu</span><span class="sxs-lookup"><span data-stu-id="3aed1-3003">Paszportu</span></span>
- <span data-ttu-id="3aed1-3004">고 zport</span><span class="sxs-lookup"><span data-stu-id="3aed1-3004">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="3aed1-3005">포르투갈 시민 카드 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3005">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3006">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3006">Format</span></span>

<span data-ttu-id="3aed1-3007">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3007">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3008">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3008">Pattern</span></span>

<span data-ttu-id="3aed1-3009">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3009">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3010">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3010">Checksum</span></span>

<span data-ttu-id="3aed1-3011">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3011">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3012">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3012">Definition</span></span>

<span data-ttu-id="3aed1-3013">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3013">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3014">정규식 Regex_portugal_citizen_card 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3014">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3015">Keyword_portugal_citizen_card에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3015">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```xml
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3016">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3016">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="3aed1-3017">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3017">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="3aed1-3018">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3018">Citizen Card</span></span>
- <span data-ttu-id="3aed1-3019">National ID Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3019">National ID Card</span></span>
- <span data-ttu-id="3aed1-3020">참조란</span><span class="sxs-lookup"><span data-stu-id="3aed1-3020">CC</span></span>
- <span data-ttu-id="3aed1-3021">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="3aed1-3021">Cartão de Cidadão</span></span>
- <span data-ttu-id="3aed1-3022">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="3aed1-3022">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="3aed1-3023">사우디 아라비아 국가 ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-3023">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3024">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3024">Format</span></span>

<span data-ttu-id="3aed1-3025">10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3025">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3026">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3026">Pattern</span></span>

<span data-ttu-id="3aed1-3027">10자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3027">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3028">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3028">Checksum</span></span>

<span data-ttu-id="3aed1-3029">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3029">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3030">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3030">Definition</span></span>

<span data-ttu-id="3aed1-3031">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3031">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3032">Regex_saudi_arabia_national_id 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3032">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3033">Keyword_saudi_arabia_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3033">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```xml
<!-- Saudi Arabia National ID -->
<Entity id="8c5a0ba8-404a-41a3-8871-746aa21ee6c0" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_saudi_arabia_national_id" />
        <Any minMatches="1">
          <Match idRef="Keyword_saudi_arabia_national_id" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3034">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3034">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="3aed1-3035">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="3aed1-3035">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="3aed1-3036">Identification Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3036">Identification Card</span></span> 
- <span data-ttu-id="3aed1-3037">I card number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3037">I card number</span></span> 
- <span data-ttu-id="3aed1-3038">ID number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3038">ID number</span></span> 
- <span data-ttu-id="3aed1-3039">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="3aed1-3039">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="3aed1-3040">싱가포르 NRIC(국가 등록 ID 카드) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3040">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3041">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3041">Format</span></span>

<span data-ttu-id="3aed1-3042">9개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3042">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3043">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3043">Pattern</span></span>

- <span data-ttu-id="3aed1-3044">9개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3044">Nine letters and digits:</span></span>
- <span data-ttu-id="3aed1-3045">문자 "F", "G", "S" 또는 "T"(대/소문자 구분 안 함) </span><span class="sxs-lookup"><span data-stu-id="3aed1-3045">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-3046">7자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3046">Seven digits</span></span> 
- <span data-ttu-id="3aed1-3047">알파벳 검사 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3047">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3048">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3048">Checksum</span></span>

<span data-ttu-id="3aed1-3049">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3049">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3050">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3050">Definition</span></span>

<span data-ttu-id="3aed1-3051">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3051">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3052">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3052">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3053">Keyword_singapore_nric에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3053">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="3aed1-3054">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3054">The checksum passes.</span></span>

<span data-ttu-id="3aed1-3055">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3055">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3056">정규식 Regex_singapore_nric 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3056">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3057">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3057">The checksum passes.</span></span>

```xml
<!-- Singapore National Registration Identity Card (NRIC) Number -->
<Entity id="cead390a-dd83-4856-9751-fb6dc98c34da" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_singapore_nric"/>
     <Match idRef="Keyword_singapore_nric"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_singapore_nric"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3058">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3058">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="3aed1-3059">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="3aed1-3059">Keyword_singapore_nric</span></span>

- <span data-ttu-id="3aed1-3060">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3060">National Registration Identity Card</span></span> 
- <span data-ttu-id="3aed1-3061">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3061">Identity Card Number</span></span> 
- <span data-ttu-id="3aed1-3062">NRIC</span><span class="sxs-lookup"><span data-stu-id="3aed1-3062">NRIC</span></span> 
- <span data-ttu-id="3aed1-3063">비용</span><span class="sxs-lookup"><span data-stu-id="3aed1-3063">IC</span></span> 
- <span data-ttu-id="3aed1-3064">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3064">Foreign Identification Number</span></span> 
- <span data-ttu-id="3aed1-3065">삭제할</span><span class="sxs-lookup"><span data-stu-id="3aed1-3065">FIN</span></span> 
- <span data-ttu-id="3aed1-3066">身份证</span><span class="sxs-lookup"><span data-stu-id="3aed1-3066">身份证</span></span> 
- <span data-ttu-id="3aed1-3067">身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-3067">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="3aed1-3068">남아프리카 공화국 식별 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3068">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3069">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3069">Format</span></span>

<span data-ttu-id="3aed1-3070">공백을 포함할 수 있는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3070">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3071">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3071">Pattern</span></span>

<span data-ttu-id="3aed1-3072">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3072">13 digits:</span></span>
- <span data-ttu-id="3aed1-3073">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-3073">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="3aed1-3074">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3074">Four digits</span></span> 
- <span data-ttu-id="3aed1-3075">1자리 시민권 표시 </span><span class="sxs-lookup"><span data-stu-id="3aed1-3075">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="3aed1-3076">숫자 "8" 또는 "9" </span><span class="sxs-lookup"><span data-stu-id="3aed1-3076">The digit "8" or "9"</span></span> 
- <span data-ttu-id="3aed1-3077">체크섬 숫자에 해당하는 1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3077">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3078">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3078">Checksum</span></span>

<span data-ttu-id="3aed1-3079">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3079">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3080">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3080">Definition</span></span>

<span data-ttu-id="3aed1-3081">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3081">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3082">Func_south_africa_identification_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3082">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3083">Keyword_south_africa_identification_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3083">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="3aed1-3084">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3084">The checksum passes.</span></span>

```xml
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3085">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3085">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="3aed1-3086">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3086">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="3aed1-3087">Identity card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3087">Identity card</span></span>
- <span data-ttu-id="3aed1-3088">ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-3088">ID</span></span>
- <span data-ttu-id="3aed1-3089">확인과</span><span class="sxs-lookup"><span data-stu-id="3aed1-3089">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="3aed1-3090">한국 주민 등록 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3090">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3091">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3091">Format</span></span>

<span data-ttu-id="3aed1-3092">하이픈을 포함하는 13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3092">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3093">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3093">Pattern</span></span>

<span data-ttu-id="3aed1-3094">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3094">13 digits:</span></span>
- <span data-ttu-id="3aed1-3095">생년월일에 해당하는 YYMMDD 형식의 6자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-3095">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="3aed1-3096">하이픈</span><span class="sxs-lookup"><span data-stu-id="3aed1-3096">A hyphen</span></span> 
- <span data-ttu-id="3aed1-3097">세기 및 성별에 따라 결정되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-3097">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="3aed1-3098">4자리 출생 지역 코드 </span><span class="sxs-lookup"><span data-stu-id="3aed1-3098">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="3aed1-3099">앞 번호가 동일한 사람을 구분하기 위해 사용되는 1자리 숫자 </span><span class="sxs-lookup"><span data-stu-id="3aed1-3099">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="3aed1-3100">검사 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3100">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3101">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3101">Checksum</span></span>

<span data-ttu-id="3aed1-3102">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3102">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3103">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3103">Definition</span></span>

<span data-ttu-id="3aed1-3104">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3104">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3105">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3105">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3106">Keyword_south_korea_resident_number에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3106">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="3aed1-3107">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3107">The checksum passes.</span></span>

<span data-ttu-id="3aed1-3108">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3108">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3109">Func_south_korea_resident_number 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3109">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3110">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3110">The checksum passes.</span></span>

```xml
<!-- South Korea Resident Registration Number -->
<Entity id="5b802e18-ba80-44c4-bc83-bf2ad36ae36a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_korea_resident_number"/>
     <Match idRef="Keyword_south_korea_resident_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_south_korea_resident_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3111">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3111">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="3aed1-3112">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3112">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="3aed1-3113">National ID card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3113">National ID card</span></span> 
- <span data-ttu-id="3aed1-3114">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3114">Citizen's Registration Number</span></span> 
- <span data-ttu-id="3aed1-3115">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="3aed1-3115">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="3aed1-3116">RRN</span><span class="sxs-lookup"><span data-stu-id="3aed1-3116">RRN</span></span> 
- <span data-ttu-id="3aed1-3117">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3117">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="3aed1-3118">스페인 SSN(사회 보장 번호)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3118">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3119">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3119">Format</span></span>

<span data-ttu-id="3aed1-3120">11-12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3120">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3121">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3121">Pattern</span></span>

<span data-ttu-id="3aed1-3122">11-12 자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3122">11-12 digits:</span></span>
- <span data-ttu-id="3aed1-3123">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3123">Two digits</span></span> 
- <span data-ttu-id="3aed1-3124">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3124">A forward slash (optional)</span></span> 
- <span data-ttu-id="3aed1-3125">7-8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3125">7-8 digits</span></span> 
- <span data-ttu-id="3aed1-3126">정방향 슬래시 1개(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3126">A forward slash (optional)</span></span> 
- <span data-ttu-id="3aed1-3127">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3127">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3128">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3128">Checksum</span></span>

<span data-ttu-id="3aed1-3129">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3129">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3130">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3130">Definition</span></span>

<span data-ttu-id="3aed1-3131">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3131">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3132">Func_spanish_social_security_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3132">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3133">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3133">The checksum passes.</span></span>

```xml
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3134">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3134">Keywords</span></span>

<span data-ttu-id="3aed1-3135">없음</span><span class="sxs-lookup"><span data-stu-id="3aed1-3135">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="3aed1-3136">SQL Server 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="3aed1-3136">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3137">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3137">Format</span></span>

<span data-ttu-id="3aed1-3138">아래 패턴에 설명 된 문자 및 문자열이 뒤에 오는 "User Id", "User ID", "uid" 또는 "UserId"입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3138">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3139">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3139">Pattern</span></span>

- <span data-ttu-id="3aed1-3140">문자열 "User Id", "User ID", "uid" 또는 "UserId"</span><span class="sxs-lookup"><span data-stu-id="3aed1-3140">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="3aed1-3141">1-200에서 대/소문자, 숫자, 기호, 특수 문자 또는 공백 사이의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-3141">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="3aed1-3142">문자열 "Password" 또는 "pwd" (여기에서 "pwd" 앞에 소문자 문자가 오지 않음)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3142">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="3aed1-3143">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3143">An equal sign (=)</span></span>
- <span data-ttu-id="3aed1-3144">달러 기호 ($), 백분율 기호 (%, 부등호 (>), 기호 (@), 따옴표 ("), 세미콜론 (;), 왼쪽 중괄호 ([) 또는 왼쪽 대괄호 ({))가 아닌 모든 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3144">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="3aed1-3145">세미콜론 (;), 슬래시 (/) 또는 따옴표 (")가 아닌 7-128 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-3145">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="3aed1-3146">세미콜론 (;) 또는 따옴표 (")</span><span class="sxs-lookup"><span data-stu-id="3aed1-3146">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3147">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3147">Checksum</span></span>

<span data-ttu-id="3aed1-3148">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3148">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3149">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3149">Definition</span></span>

<span data-ttu-id="3aed1-3150">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3150">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3151">정규식 CEP_Regex_SQLServerConnectionString 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3151">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3152">CEP_GlobalFilter의 키워드를 찾을 수 **없습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-3152">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="3aed1-3153">정규식 CEP_PasswordPlaceHolder에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-3153">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3154">정규식 CEP_CommonExampleKeywords에서 해당 패턴과 일치 하는 콘텐츠 **를 찾지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="3aed1-3154">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```sql
<!---SQL Server Connection String>
<Entity id="e76b6205-d3cb-46f2-bd63-c90153f2f97d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_SQLServerConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_GlobalFilter" />
            <Match idRef="CEP_PasswordPlaceHolder" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3155">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3155">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="3aed1-3156">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="3aed1-3156">CEP_GlobalFilter</span></span>

- <span data-ttu-id="3aed1-3157">일부 암호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3157">some-password</span></span>
- <span data-ttu-id="3aed1-3158">somepassword</span><span class="sxs-lookup"><span data-stu-id="3aed1-3158">somepassword</span></span>
- <span data-ttu-id="3aed1-3159">secretPassword</span><span class="sxs-lookup"><span data-stu-id="3aed1-3159">secretPassword</span></span>
- <span data-ttu-id="3aed1-3160">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3160">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="3aed1-3161">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="3aed1-3161">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="3aed1-3162">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3162">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-3163">암호나 pwd에 0-2 공백, 등호 (=), 0-2 공백 및 별표 (\*)-----------------------</span><span class="sxs-lookup"><span data-stu-id="3aed1-3163">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="3aed1-3164">암호나 pwd 뒤에 다음이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3164">Password or pwd followed by:</span></span>
    - <span data-ttu-id="3aed1-3165">등호 (=)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3165">Equal sign (=)</span></span>
    - <span data-ttu-id="3aed1-3166">보다 작음 기호 (<)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3166">Less than symbol (<)</span></span>
    - <span data-ttu-id="3aed1-3167">대문자나 소문자, digits, 별표 (\*), 하이픈 (-), 밑줄 (_) 또는 공백 문자인 1-200 문자의 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-3167">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="3aed1-3168">보다 큼 기호 (>)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3168">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="3aed1-3169">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="3aed1-3169">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="3aed1-3170">기술적으로이 중요 한 정보 유형은 키워드 목록이 아니라 정규식을 사용 하 여 이러한 키워드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3170">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="3aed1-3171">극동</span><span class="sxs-lookup"><span data-stu-id="3aed1-3171">contoso</span></span>
- <span data-ttu-id="3aed1-3172">fabrikam</span><span class="sxs-lookup"><span data-stu-id="3aed1-3172">fabrikam</span></span>
- <span data-ttu-id="3aed1-3173">대양</span><span class="sxs-lookup"><span data-stu-id="3aed1-3173">northwind</span></span>
- <span data-ttu-id="3aed1-3174">샌드박스</span><span class="sxs-lookup"><span data-stu-id="3aed1-3174">sandbox</span></span>
- <span data-ttu-id="3aed1-3175">용 onebox</span><span class="sxs-lookup"><span data-stu-id="3aed1-3175">onebox</span></span>
- <span data-ttu-id="3aed1-3176">로컬</span><span class="sxs-lookup"><span data-stu-id="3aed1-3176">localhost</span></span>
- <span data-ttu-id="3aed1-3177">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="3aed1-3177">127.0.0.1</span></span>
- <span data-ttu-id="3aed1-3178">testacs입니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3178">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-3179">ccw</span><span class="sxs-lookup"><span data-stu-id="3aed1-3179">com</span></span>
- <span data-ttu-id="3aed1-3180">s-int</span><span class="sxs-lookup"><span data-stu-id="3aed1-3180">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="3aed1-3181">투자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3181">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="3aed1-3182">스웨덴 국가 ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-3182">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3183">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3183">Format</span></span>

<span data-ttu-id="3aed1-3184">10 또는 12자리 숫자와 선택적 구분 기호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3184">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3185">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3185">Pattern</span></span>

<span data-ttu-id="3aed1-3186">10 또는 12자리 숫자와 선택적 구분 기호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3186">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="3aed1-3187">2-4자리 숫자(선택 사항)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3187">2-4 digits (optional)</span></span> 
- <span data-ttu-id="3aed1-3188">YYMMDD 날짜 형식의 6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3188">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="3aed1-3189">구분 기호 "-" 또는 "+"(선택 사항) 및</span><span class="sxs-lookup"><span data-stu-id="3aed1-3189">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="3aed1-3190">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3190">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3191">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3191">Checksum</span></span>

<span data-ttu-id="3aed1-3192">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3192">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3193">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3193">Definition</span></span>

<span data-ttu-id="3aed1-3194">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3194">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3195">Func_swedish_national_identifier 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3195">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3196">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3196">The checksum passes.</span></span>

```xml
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3197">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3197">Keywords</span></span>

<span data-ttu-id="3aed1-3198">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3198">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="3aed1-3199">스웨덴 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3199">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3200">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3200">Format</span></span>

<span data-ttu-id="3aed1-3201">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3201">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3202">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3202">Pattern</span></span>

<span data-ttu-id="3aed1-3203">8자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3203">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3204">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3204">Checksum</span></span>

<span data-ttu-id="3aed1-3205">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3205">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3206">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3206">Definition</span></span>

<span data-ttu-id="3aed1-3207">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3207">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3208">Regex_sweden_passport_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3208">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3209">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3209">One of the following is true:</span></span>
    - <span data-ttu-id="3aed1-3210">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3210">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="3aed1-3211">Keyword_sweden_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3211">A keyword from Keyword_sweden_passport is found.</span></span>

```xml
<!-- Sweden Passport Number -->
<Entity id="ba4e7456-55a9-4d89-9140-c33673553526" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_sweden_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_sweden_passport" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3212">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3212">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="3aed1-3213">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-3213">Keyword_sweden_passport</span></span>

- <span data-ttu-id="3aed1-3214">visa requirements</span><span class="sxs-lookup"><span data-stu-id="3aed1-3214">visa requirements</span></span> 
- <span data-ttu-id="3aed1-3215">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3215">Alien Registration Card</span></span> 
- <span data-ttu-id="3aed1-3216">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="3aed1-3216">Schengen visas</span></span> 
- <span data-ttu-id="3aed1-3217">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="3aed1-3217">Schengen visa</span></span> 
- <span data-ttu-id="3aed1-3218">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="3aed1-3218">Visa Processing</span></span> 
- <span data-ttu-id="3aed1-3219">Visa Type</span><span class="sxs-lookup"><span data-stu-id="3aed1-3219">Visa Type</span></span> 
- <span data-ttu-id="3aed1-3220">Single Entry</span><span class="sxs-lookup"><span data-stu-id="3aed1-3220">Single Entry</span></span> 
- <span data-ttu-id="3aed1-3221">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="3aed1-3221">Multiple Entry</span></span> 
- <span data-ttu-id="3aed1-3222">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="3aed1-3222">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="3aed1-3223">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-3223">Keyword_passport</span></span>

- <span data-ttu-id="3aed1-3224">Passport Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3224">Passport Number</span></span> 
- <span data-ttu-id="3aed1-3225">Passport No</span><span class="sxs-lookup"><span data-stu-id="3aed1-3225">Passport No</span></span> 
- <span data-ttu-id="3aed1-3226">Passport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3226">Passport #</span></span> 
- <span data-ttu-id="3aed1-3227">여권 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3227">Passport#</span></span> 
- <span data-ttu-id="3aed1-3228">PassportID</span><span class="sxs-lookup"><span data-stu-id="3aed1-3228">PassportID</span></span> 
- <span data-ttu-id="3aed1-3229">Passportno</span><span class="sxs-lookup"><span data-stu-id="3aed1-3229">Passportno</span></span> 
- <span data-ttu-id="3aed1-3230">passportnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-3230">passportnumber</span></span> 
- <span data-ttu-id="3aed1-3231">パスポート</span><span class="sxs-lookup"><span data-stu-id="3aed1-3231">パスポート</span></span> 
- <span data-ttu-id="3aed1-3232">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-3232">パスポート番号</span></span> 
- <span data-ttu-id="3aed1-3233">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="3aed1-3233">パスポートのNum</span></span> 
- <span data-ttu-id="3aed1-3234">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-3234">パスポート＃</span></span> 
- <span data-ttu-id="3aed1-3235">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="3aed1-3235">Numéro de passeport</span></span> 
- <span data-ttu-id="3aed1-3236">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="3aed1-3236">Passeport n °</span></span> 
- <span data-ttu-id="3aed1-3237">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="3aed1-3237">Passeport Non</span></span> 
- <span data-ttu-id="3aed1-3238">Passeport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3238">Passeport #</span></span> 
- <span data-ttu-id="3aed1-3239">포트 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3239">Passeport#</span></span> 
- <span data-ttu-id="3aed1-3240">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="3aed1-3240">PasseportNon</span></span> 
- <span data-ttu-id="3aed1-3241">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="3aed1-3241">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="3aed1-3242">SWIFT 코드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3242">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3243">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3243">Format</span></span>

<span data-ttu-id="3aed1-3244">4개의 문자, 5-31개 문자 또는 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3244">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3245">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3245">Pattern</span></span>

<span data-ttu-id="3aed1-3246">4개의 문자, 5-31개 문자 또는 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3246">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="3aed1-3247">4문자 은행 코드(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3247">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-3248">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-3248">An optional space</span></span> 
- <span data-ttu-id="3aed1-3249">4-28개 문자 또는 숫자[BBAN(기본 은행 계좌 번호)]</span><span class="sxs-lookup"><span data-stu-id="3aed1-3249">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="3aed1-3250">선택적 공백 1개</span><span class="sxs-lookup"><span data-stu-id="3aed1-3250">An optional space</span></span> 
- <span data-ttu-id="3aed1-3251">1-3개 문자 또는 숫자(BBAN의 나머지)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3251">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3252">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3252">Checksum</span></span>

<span data-ttu-id="3aed1-3253">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3253">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3254">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3254">Definition</span></span>

<span data-ttu-id="3aed1-3255">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3255">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3256">Regex_swift 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3256">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3257">Keyword_swift의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3257">A keyword from Keyword_swift is found.</span></span>

```xml
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3258">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3258">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="3aed1-3259">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="3aed1-3259">Keyword_swift</span></span>

- <span data-ttu-id="3aed1-3260">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="3aed1-3260">international organization for standardization 9362</span></span> 
- <span data-ttu-id="3aed1-3261">iso 9362</span><span class="sxs-lookup"><span data-stu-id="3aed1-3261">iso 9362</span></span> 
- <span data-ttu-id="3aed1-3262">iso9362</span><span class="sxs-lookup"><span data-stu-id="3aed1-3262">iso9362</span></span> 
- <span data-ttu-id="3aed1-3263">swift\#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3263">swift\#</span></span> 
- <span data-ttu-id="3aed1-3264">swiftcode</span><span class="sxs-lookup"><span data-stu-id="3aed1-3264">swiftcode</span></span> 
- <span data-ttu-id="3aed1-3265">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-3265">swiftnumber</span></span> 
- <span data-ttu-id="3aed1-3266">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-3266">swiftroutingnumber</span></span> 
- <span data-ttu-id="3aed1-3267">swift code</span><span class="sxs-lookup"><span data-stu-id="3aed1-3267">swift code</span></span> 
- <span data-ttu-id="3aed1-3268">swift number #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3268">swift number #</span></span> 
- <span data-ttu-id="3aed1-3269">swift routing number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3269">swift routing number</span></span> 
- <span data-ttu-id="3aed1-3270">bic number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3270">bic number</span></span> 
- <span data-ttu-id="3aed1-3271">bic code</span><span class="sxs-lookup"><span data-stu-id="3aed1-3271">bic code</span></span> 
- <span data-ttu-id="3aed1-3272">bic\#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3272">bic \#</span></span> 
- <span data-ttu-id="3aed1-3273">bic\#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3273">bic\#</span></span> 
- <span data-ttu-id="3aed1-3274">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="3aed1-3274">bank identifier code</span></span> 
- <span data-ttu-id="3aed1-3275">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="3aed1-3275">標準化9362</span></span> 
- <span data-ttu-id="3aed1-3276">迅速＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-3276">迅速＃</span></span> 
- <span data-ttu-id="3aed1-3277">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="3aed1-3277">SWIFTコード</span></span> 
- <span data-ttu-id="3aed1-3278">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-3278">SWIFT番号</span></span> 
- <span data-ttu-id="3aed1-3279">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-3279">迅速なルーティング番号</span></span> 
- <span data-ttu-id="3aed1-3280">BIC番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-3280">BIC番号</span></span> 
- <span data-ttu-id="3aed1-3281">BICコード</span><span class="sxs-lookup"><span data-stu-id="3aed1-3281">BICコード</span></span> 
- <span data-ttu-id="3aed1-3282">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="3aed1-3282">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="3aed1-3283">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="3aed1-3283">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="3aed1-3284">rapide\#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3284">rapide \#</span></span> 
- <span data-ttu-id="3aed1-3285">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="3aed1-3285">code SWIFT</span></span> 
- <span data-ttu-id="3aed1-3286">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="3aed1-3286">le numéro de swift</span></span> 
- <span data-ttu-id="3aed1-3287">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="3aed1-3287">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="3aed1-3288">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="3aed1-3288">le numéro BIC</span></span> 
- <span data-ttu-id="3aed1-3289">\#BIC</span><span class="sxs-lookup"><span data-stu-id="3aed1-3289">\# BIC</span></span> 
- <span data-ttu-id="3aed1-3290">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="3aed1-3290">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="3aed1-3291">대만 국가 ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-3291">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3292">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3292">Format</span></span>

<span data-ttu-id="3aed1-3293">1개의 문자, 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3293">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3294">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3294">Pattern</span></span>

<span data-ttu-id="3aed1-3295">1개의 문자, 9자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3295">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="3aed1-3296">1개 문자(영문, 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3296">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-3297">숫자 "1" 또는 "2"</span><span class="sxs-lookup"><span data-stu-id="3aed1-3297">The digit "1" or "2"</span></span> 
- <span data-ttu-id="3aed1-3298">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3298">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3299">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3299">Checksum</span></span>

<span data-ttu-id="3aed1-3300">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3300">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3301">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3301">Definition</span></span>

<span data-ttu-id="3aed1-3302">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3302">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3303">Func_taiwanese_national_id 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3303">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3304">Keyword_taiwanese_national_id의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3304">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="3aed1-3305">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3305">The checksum passes.</span></span>

```xml
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3306">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3306">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="3aed1-3307">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="3aed1-3307">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="3aed1-3308">身份證字號</span><span class="sxs-lookup"><span data-stu-id="3aed1-3308">身份證字號</span></span> 
- <span data-ttu-id="3aed1-3309">身份證</span><span class="sxs-lookup"><span data-stu-id="3aed1-3309">身份證</span></span> 
- <span data-ttu-id="3aed1-3310">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="3aed1-3310">身份證號碼</span></span> 
- <span data-ttu-id="3aed1-3311">身份證號</span><span class="sxs-lookup"><span data-stu-id="3aed1-3311">身份證號</span></span> 
- <span data-ttu-id="3aed1-3312">身分證字號</span><span class="sxs-lookup"><span data-stu-id="3aed1-3312">身分證字號</span></span> 
- <span data-ttu-id="3aed1-3313">身分證</span><span class="sxs-lookup"><span data-stu-id="3aed1-3313">身分證</span></span> 
- <span data-ttu-id="3aed1-3314">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="3aed1-3314">身分證號碼</span></span> 
- <span data-ttu-id="3aed1-3315">身份證號</span><span class="sxs-lookup"><span data-stu-id="3aed1-3315">身份證號</span></span> 
- <span data-ttu-id="3aed1-3316">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="3aed1-3316">身分證統一編號</span></span> 
- <span data-ttu-id="3aed1-3317">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="3aed1-3317">國民身分證統一編號</span></span> 
- <span data-ttu-id="3aed1-3318">簽名</span><span class="sxs-lookup"><span data-stu-id="3aed1-3318">簽名</span></span> 
- <span data-ttu-id="3aed1-3319">蓋章</span><span class="sxs-lookup"><span data-stu-id="3aed1-3319">蓋章</span></span> 
- <span data-ttu-id="3aed1-3320">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="3aed1-3320">簽名或蓋章</span></span> 
- <span data-ttu-id="3aed1-3321">簽章</span><span class="sxs-lookup"><span data-stu-id="3aed1-3321">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="3aed1-3322">	대만 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3322">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3323">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3323">Format</span></span>

- <span data-ttu-id="3aed1-3324">생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3324">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="3aed1-3325">비-생체 인식 여권 번호: 9 자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3325">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3326">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3326">Pattern</span></span>
<span data-ttu-id="3aed1-3327">생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3327">Biometric passport number:</span></span>
- <span data-ttu-id="3aed1-3328">숫자 "3" </span><span class="sxs-lookup"><span data-stu-id="3aed1-3328">The digit "3"</span></span> 
- <span data-ttu-id="3aed1-3329">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3329">Eight digits</span></span>

<span data-ttu-id="3aed1-3330">비-생체 인식 여권 번호:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3330">Non-biometric passport number:</span></span>
- <span data-ttu-id="3aed1-3331">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3331">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3332">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3332">Checksum</span></span>

<span data-ttu-id="3aed1-3333">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3333">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3334">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3334">Definition</span></span>

<span data-ttu-id="3aed1-3335">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3336">정규식 Regex_taiwan_passport 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3336">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3337">Keyword_taiwan_passport에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3337">A keyword from Keyword_taiwan_passport is found.</span></span>

```xml
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3338">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3338">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="3aed1-3339">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-3339">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="3aed1-3340">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3340">ROC passport number</span></span> 
- <span data-ttu-id="3aed1-3341">Passport number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3341">Passport number</span></span> 
- <span data-ttu-id="3aed1-3342">Passport no</span><span class="sxs-lookup"><span data-stu-id="3aed1-3342">Passport no</span></span> 
- <span data-ttu-id="3aed1-3343">Passport Num</span><span class="sxs-lookup"><span data-stu-id="3aed1-3343">Passport Num</span></span> 
- <span data-ttu-id="3aed1-3344">Passport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3344">Passport #</span></span> 
- <span data-ttu-id="3aed1-3345">护照</span><span class="sxs-lookup"><span data-stu-id="3aed1-3345">护照</span></span> 
- <span data-ttu-id="3aed1-3346">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="3aed1-3346">中華民國護照</span></span> 
- <span data-ttu-id="3aed1-3347">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="3aed1-3347">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="3aed1-3348">대만 거주 인증(ARC/TARC) 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3348">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3349">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3349">Format</span></span>

<span data-ttu-id="3aed1-3350">10개의 문자 및 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3350">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3351">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3351">Pattern</span></span>

<span data-ttu-id="3aed1-3352">10개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3352">10 letters and digits:</span></span>
- <span data-ttu-id="3aed1-3353">2문자(대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3353">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="3aed1-3354">8자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3354">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3355">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3355">Checksum</span></span>

<span data-ttu-id="3aed1-3356">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3356">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3357">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3357">Definition</span></span>

<span data-ttu-id="3aed1-3358">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3358">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3359">정규식 Regex_taiwan_resident_certificate 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3359">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3360">Keyword_taiwan_resident_certificate에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3360">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```xml
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3361">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3361">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="3aed1-3362">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="3aed1-3362">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="3aed1-3363">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="3aed1-3363">Resident Certificate</span></span> 
- <span data-ttu-id="3aed1-3364">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="3aed1-3364">Resident Cert</span></span> 
- <span data-ttu-id="3aed1-3365">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3365">Resident Cert.</span></span> 
- <span data-ttu-id="3aed1-3366">Identification card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3366">Identification card</span></span> 
- <span data-ttu-id="3aed1-3367">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="3aed1-3367">Alien Resident Certificate</span></span> 
- <span data-ttu-id="3aed1-3368">ARC</span><span class="sxs-lookup"><span data-stu-id="3aed1-3368">ARC</span></span> 
- <span data-ttu-id="3aed1-3369">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="3aed1-3369">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="3aed1-3370">TARC</span><span class="sxs-lookup"><span data-stu-id="3aed1-3370">TARC</span></span> 
- <span data-ttu-id="3aed1-3371">居留證</span><span class="sxs-lookup"><span data-stu-id="3aed1-3371">居留證</span></span> 
- <span data-ttu-id="3aed1-3372">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="3aed1-3372">外僑居留證</span></span> 
- <span data-ttu-id="3aed1-3373">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="3aed1-3373">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="3aed1-3374">태국어 인구 식별 코드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3374">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3375">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3375">Format</span></span>

<span data-ttu-id="3aed1-3376">13자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3376">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3377">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3377">Pattern</span></span>

<span data-ttu-id="3aed1-3378">13자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3378">13 digits:</span></span>
- <span data-ttu-id="3aed1-3379">첫 번째 숫자가 0 또는 9가 아님</span><span class="sxs-lookup"><span data-stu-id="3aed1-3379">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="3aed1-3380">12자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3380">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3381">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3381">Checksum</span></span>

<span data-ttu-id="3aed1-3382">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3382">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3383">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3383">Definition</span></span>

<span data-ttu-id="3aed1-3384">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3384">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3385">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3385">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3386">Keyword_Thai_Citizen_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3386">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="3aed1-3387">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3387">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3388">Func_Thai_Citizen_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3388">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```xml
<!-- Thai Citizen ID -->
-<Entity id="44ca9e86-ead7-4c5d-884a-e2eaa401515e" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
      <Match idRef="Keyword_Thai_Citizen_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3389">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3389">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="3aed1-3390">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="3aed1-3390">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="3aed1-3391">ID Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3391">ID Number</span></span>
- <span data-ttu-id="3aed1-3392">Id 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3392">Identification Number</span></span>
- <span data-ttu-id="3aed1-3393">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="3aed1-3393">บัตรประชาชน</span></span>
- <span data-ttu-id="3aed1-3394">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="3aed1-3394">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="3aed1-3395">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="3aed1-3395">บัตรประชาชน</span></span>
- <span data-ttu-id="3aed1-3396">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="3aed1-3396">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="3aed1-3397">터키어 국가 식별 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3397">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3398">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3398">Format</span></span>

<span data-ttu-id="3aed1-3399">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3399">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3400">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3400">Pattern</span></span>

<span data-ttu-id="3aed1-3401">11자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3401">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3402">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3402">Checksum</span></span>

<span data-ttu-id="3aed1-3403">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3403">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3404">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3404">Definition</span></span>

<span data-ttu-id="3aed1-3405">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3405">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3406">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3406">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3407">Keyword_Turkish_National_Id에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3407">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="3aed1-3408">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3408">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3409">Func_Turkish_National_Id 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3409">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```xml
<!-- Turkish National Identity -->
-<Entity id="fb621f20-3876-4cfc-acec-8c8e73ca32c7" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Turkish_National_Id"/>
      <Match idRef="Keyword_Turkish_National_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Turkish_National_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3410">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3410">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="3aed1-3411">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="3aed1-3411">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="3aed1-3412">TC Kimlik 아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3412">TC Kimlik No</span></span>
- <span data-ttu-id="3aed1-3413">TC Kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="3aed1-3413">TC Kimlik numarası</span></span>
- <span data-ttu-id="3aed1-3414">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="3aed1-3414">Vatandaşlık numarası</span></span>
- <span data-ttu-id="3aed1-3415">Vatandaşlık 아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3415">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="3aed1-p142">영국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-p142">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3418">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3418">Format</span></span>

<span data-ttu-id="3aed1-3419">지정된 형식의 18개 문자 및 숫자 조합</span><span class="sxs-lookup"><span data-stu-id="3aed1-3419">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3420">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3420">Pattern</span></span>

<span data-ttu-id="3aed1-3421">18개의 문자 및 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3421">18 letters and digits:</span></span>
- <span data-ttu-id="3aed1-3422">5개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="3aed1-3422">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="3aed1-3423">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3423">One digit</span></span> 
- <span data-ttu-id="3aed1-3424">날짜 형식의 5 자리 숫자 MMDDY 생년월일 (드라이버가 암 인 경우 50이 고 62 51은 01부터 12까지)로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3424">Five digits in the date format MMDDY for date of birth (7th character is incremented by 50 if driver is female, i.e. 51 to 62 instead of 01 to 12)</span></span>
- <span data-ttu-id="3aed1-3425">2개 문자(대/소문자 구분 안 함) 또는 문자 대신 숫자 "9" 사용</span><span class="sxs-lookup"><span data-stu-id="3aed1-3425">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="3aed1-3426">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3426">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3427">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3427">Checksum</span></span>

<span data-ttu-id="3aed1-3428">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3428">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3429">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3429">Definition</span></span>

<span data-ttu-id="3aed1-3430">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3430">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3431">Func_uk_drivers_license 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3431">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3432">Keyword_uk_drivers_license의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3432">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="3aed1-3433">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3433">The checksum passes.</span></span>

```xml
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3434">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3434">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="3aed1-3435">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="3aed1-3435">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="3aed1-3436">DVLA</span><span class="sxs-lookup"><span data-stu-id="3aed1-3436">DVLA</span></span> 
- <span data-ttu-id="3aed1-3437">light vans</span><span class="sxs-lookup"><span data-stu-id="3aed1-3437">light vans</span></span> 
- <span data-ttu-id="3aed1-3438">quadbikes</span><span class="sxs-lookup"><span data-stu-id="3aed1-3438">quadbikes</span></span> 
- <span data-ttu-id="3aed1-3439">motor cars</span><span class="sxs-lookup"><span data-stu-id="3aed1-3439">motor cars</span></span> 
- <span data-ttu-id="3aed1-3440">125cc</span><span class="sxs-lookup"><span data-stu-id="3aed1-3440">125cc</span></span> 
- <span data-ttu-id="3aed1-3441">sidecar</span><span class="sxs-lookup"><span data-stu-id="3aed1-3441">sidecar</span></span> 
- <span data-ttu-id="3aed1-3442">tricycles</span><span class="sxs-lookup"><span data-stu-id="3aed1-3442">tricycles</span></span> 
- <span data-ttu-id="3aed1-3443">motorcycles</span><span class="sxs-lookup"><span data-stu-id="3aed1-3443">motorcycles</span></span> 
- <span data-ttu-id="3aed1-3444">photocard licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-3444">photocard licence</span></span> 
- <span data-ttu-id="3aed1-3445">learner drivers</span><span class="sxs-lookup"><span data-stu-id="3aed1-3445">learner drivers</span></span> 
- <span data-ttu-id="3aed1-3446">licence holder</span><span class="sxs-lookup"><span data-stu-id="3aed1-3446">licence holder</span></span> 
- <span data-ttu-id="3aed1-3447">licence holders</span><span class="sxs-lookup"><span data-stu-id="3aed1-3447">licence holders</span></span> 
- <span data-ttu-id="3aed1-3448">driving licences</span><span class="sxs-lookup"><span data-stu-id="3aed1-3448">driving licences</span></span> 
- <span data-ttu-id="3aed1-3449">driving licence</span><span class="sxs-lookup"><span data-stu-id="3aed1-3449">driving licence</span></span> 
- <span data-ttu-id="3aed1-3450">dual control car</span><span class="sxs-lookup"><span data-stu-id="3aed1-3450">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="3aed1-p143">영국 선거 롤 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-p143">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3453">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3453">Format</span></span>

<span data-ttu-id="3aed1-3454">2개의 문자, 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3454">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3455">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3455">Pattern</span></span>

<span data-ttu-id="3aed1-3456">2개의 문자(대/소문자 구분 안 함)와 1-4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3456">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3457">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3457">Checksum</span></span>

<span data-ttu-id="3aed1-3458">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3458">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3459">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3459">Definition</span></span>

<span data-ttu-id="3aed1-3460">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3460">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3461">Regex_uk_electoral 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3461">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3462">Keyword_uk_electoral의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3462">A keyword from Keyword_uk_electoral is found.</span></span>

```xml
<!-- U.K. Electoral Number -->
<Entity id="a3eea206-dc0c-4f06-9e22-aa1be3059963" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_uk_electoral" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_electoral" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3463">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3463">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="3aed1-3464">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="3aed1-3464">Keyword_uk_electoral</span></span>

- <span data-ttu-id="3aed1-3465">council nomination</span><span class="sxs-lookup"><span data-stu-id="3aed1-3465">council nomination</span></span> 
- <span data-ttu-id="3aed1-3466">nomination form</span><span class="sxs-lookup"><span data-stu-id="3aed1-3466">nomination form</span></span> 
- <span data-ttu-id="3aed1-3467">electoral register</span><span class="sxs-lookup"><span data-stu-id="3aed1-3467">electoral register</span></span> 
- <span data-ttu-id="3aed1-3468">electoral roll</span><span class="sxs-lookup"><span data-stu-id="3aed1-3468">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="3aed1-p144">영국 국립 보건 서비스 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-p144">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3471">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3471">Format</span></span>

<span data-ttu-id="3aed1-3472">공백으로 구분된 10-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3472">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3473">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3473">Pattern</span></span>

<span data-ttu-id="3aed1-3474">10-17자리 숫자:</span><span class="sxs-lookup"><span data-stu-id="3aed1-3474">10-17 digits:</span></span>
- <span data-ttu-id="3aed1-3475">3 또는 10자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3475">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="3aed1-3476">공백</span><span class="sxs-lookup"><span data-stu-id="3aed1-3476">A space</span></span> 
- <span data-ttu-id="3aed1-3477">3자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3477">Three digits</span></span> 
- <span data-ttu-id="3aed1-3478">공백</span><span class="sxs-lookup"><span data-stu-id="3aed1-3478">A space</span></span> 
- <span data-ttu-id="3aed1-3479">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3479">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3480">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3480">Checksum</span></span>

<span data-ttu-id="3aed1-3481">예</span><span class="sxs-lookup"><span data-stu-id="3aed1-3481">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3482">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3482">Definition</span></span>

<span data-ttu-id="3aed1-3483">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3483">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3484">Func_uk_nhs_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3484">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3485">다음 중 하나가 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3485">One of the following is true:</span></span>
    - <span data-ttu-id="3aed1-3486">Keyword_uk_nhs_number의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3486">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="3aed1-3487">Keyword_uk_nhs_number1의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3487">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="3aed1-3488">Keyword_uk_nhs_number_dob의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3488">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="3aed1-3489">체크섬이 통과됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3489">The checksum passes.</span></span>

```xml
<!-- U.K. NHS Number -->
<Entity id="3192014e-2a16-44e9-aa69-4b20375c9a78" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nhs_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nhs_number" />
          <Match idRef="Keyword_uk_nhs_number1" />
          <Match idRef="Keyword_uk_nhs_number_dob" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3490">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3490">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="3aed1-3491">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3491">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="3aed1-3492">국립 보건 서비스</span><span class="sxs-lookup"><span data-stu-id="3aed1-3492">national health service</span></span> 
- <span data-ttu-id="3aed1-3493">nhs</span><span class="sxs-lookup"><span data-stu-id="3aed1-3493">nhs</span></span> 
- <span data-ttu-id="3aed1-3494">health services authority</span><span class="sxs-lookup"><span data-stu-id="3aed1-3494">health services authority</span></span> 
- <span data-ttu-id="3aed1-3495">health authority</span><span class="sxs-lookup"><span data-stu-id="3aed1-3495">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="3aed1-3496">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="3aed1-3496">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="3aed1-3497">patient id</span><span class="sxs-lookup"><span data-stu-id="3aed1-3497">patient id</span></span> 
- <span data-ttu-id="3aed1-3498">patient identification</span><span class="sxs-lookup"><span data-stu-id="3aed1-3498">patient identification</span></span> 
- <span data-ttu-id="3aed1-3499">patient no</span><span class="sxs-lookup"><span data-stu-id="3aed1-3499">patient no</span></span> 
- <span data-ttu-id="3aed1-3500">patient number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3500">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="3aed1-3501">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="3aed1-3501">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="3aed1-3502">G</span><span class="sxs-lookup"><span data-stu-id="3aed1-3502">GP</span></span> 
- <span data-ttu-id="3aed1-3503">DOB</span><span class="sxs-lookup"><span data-stu-id="3aed1-3503">DOB</span></span> 
- <span data-ttu-id="3aed1-3504">D. O. B</span><span class="sxs-lookup"><span data-stu-id="3aed1-3504">D.O.B</span></span> 
- <span data-ttu-id="3aed1-3505">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="3aed1-3505">Date of Birth</span></span> 
- <span data-ttu-id="3aed1-3506">Birth Date</span><span class="sxs-lookup"><span data-stu-id="3aed1-3506">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="3aed1-p145">영국 NINO(국민 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="3aed1-p145">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3509">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3509">Format</span></span>

<span data-ttu-id="3aed1-3510">공백 또는 대시로 구분 된 7 자 또는 9 자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3510">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3511">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3511">Pattern</span></span>

<span data-ttu-id="3aed1-3512">다음과 같은 두 가지 패턴을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3512">Two possible patterns:</span></span>

- <span data-ttu-id="3aed1-3513">두 문자 (유효한 NINOs이 접두사의 특정 문자만 사용 하며이 패턴의 유효성 검사는 대/소문자를 구분 하지 않음)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3513">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="3aed1-3514">6자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3514">Six digits</span></span>
- <span data-ttu-id="3aed1-3515">' A ', ' B ', ' C ' 또는 ' d ' (접두사와 마찬가지로 접미사에서는 특정 문자만 허용 되며 대/소문자 구분 안 함)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3515">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="3aed1-3516">또는</span><span class="sxs-lookup"><span data-stu-id="3aed1-3516">OR</span></span>

- <span data-ttu-id="3aed1-3517">2 개 문자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3517">Two letters</span></span>
- <span data-ttu-id="3aed1-3518">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="3aed1-3518">A space or dash</span></span>
- <span data-ttu-id="3aed1-3519">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3519">Two digits</span></span>
- <span data-ttu-id="3aed1-3520">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="3aed1-3520">A space or dash</span></span>
- <span data-ttu-id="3aed1-3521">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3521">Two digits</span></span>
- <span data-ttu-id="3aed1-3522">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="3aed1-3522">A space or dash</span></span>
- <span data-ttu-id="3aed1-3523">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3523">Two digits</span></span>
- <span data-ttu-id="3aed1-3524">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="3aed1-3524">A space or dash</span></span>
- <span data-ttu-id="3aed1-3525">' A ', ' B ', ' C ' 또는 ' d ' 중 하나</span><span class="sxs-lookup"><span data-stu-id="3aed1-3525">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3526">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3526">Checksum</span></span>

<span data-ttu-id="3aed1-3527">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3527">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3528">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3528">Definition</span></span>

<span data-ttu-id="3aed1-3529">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3529">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3530">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3530">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3531">Keyword_uk_nino의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3531">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="3aed1-3532">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3532">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3533">Func_uk_nino 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3533">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3534">Keyword_uk_nino의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3534">No keyword from Keyword_uk_nino is found.</span></span>

```xml
<!-- U.K. NINO -->
<Entity id="16c07343-c26f-49d2-a987-3daf717e94cc" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3535">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3535">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="3aed1-3536">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="3aed1-3536">Keyword_uk_nino</span></span>

- <span data-ttu-id="3aed1-3537">national insurance number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3537">national insurance number</span></span> 
- <span data-ttu-id="3aed1-3538">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="3aed1-3538">national insurance contributions</span></span> 
- <span data-ttu-id="3aed1-3539">protection act</span><span class="sxs-lookup"><span data-stu-id="3aed1-3539">protection act</span></span> 
- <span data-ttu-id="3aed1-3540">소유권</span><span class="sxs-lookup"><span data-stu-id="3aed1-3540">insurance</span></span> 
- <span data-ttu-id="3aed1-3541">social security number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3541">social security number</span></span> 
- <span data-ttu-id="3aed1-3542">insurance application</span><span class="sxs-lookup"><span data-stu-id="3aed1-3542">insurance application</span></span> 
- <span data-ttu-id="3aed1-3543">medical application</span><span class="sxs-lookup"><span data-stu-id="3aed1-3543">medical application</span></span> 
- <span data-ttu-id="3aed1-3544">social insurance</span><span class="sxs-lookup"><span data-stu-id="3aed1-3544">social insurance</span></span> 
- <span data-ttu-id="3aed1-3545">medical attention</span><span class="sxs-lookup"><span data-stu-id="3aed1-3545">medical attention</span></span> 
- <span data-ttu-id="3aed1-3546">social security</span><span class="sxs-lookup"><span data-stu-id="3aed1-3546">social security</span></span> 
- <span data-ttu-id="3aed1-3547">great britain</span><span class="sxs-lookup"><span data-stu-id="3aed1-3547">great britain</span></span> 
- <span data-ttu-id="3aed1-3548">소유권</span><span class="sxs-lookup"><span data-stu-id="3aed1-3548">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="3aed1-p146">미국/영국 여권 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-p146">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3551">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3551">Format</span></span>

<span data-ttu-id="3aed1-3552">9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3552">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3553">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3553">Pattern</span></span>

<span data-ttu-id="3aed1-3554">9자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3554">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3555">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3555">Checksum</span></span>

<span data-ttu-id="3aed1-3556">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3556">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3557">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3557">Definition</span></span>

<span data-ttu-id="3aed1-3558">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3558">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3559">Func_usa_uk_passport 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3559">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3560">Keyword_passport의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3560">A keyword from Keyword_passport is found.</span></span>

```xml
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3561">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3561">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="3aed1-3562">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="3aed1-3562">Keyword_passport</span></span>

- <span data-ttu-id="3aed1-3563">Passport Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3563">Passport Number</span></span> 
- <span data-ttu-id="3aed1-3564">Passport No</span><span class="sxs-lookup"><span data-stu-id="3aed1-3564">Passport No</span></span> 
- <span data-ttu-id="3aed1-3565">Passport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3565">Passport #</span></span> 
- <span data-ttu-id="3aed1-3566">여권 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3566">Passport#</span></span> 
- <span data-ttu-id="3aed1-3567">PassportID</span><span class="sxs-lookup"><span data-stu-id="3aed1-3567">PassportID</span></span> 
- <span data-ttu-id="3aed1-3568">Passportno</span><span class="sxs-lookup"><span data-stu-id="3aed1-3568">Passportno</span></span> 
- <span data-ttu-id="3aed1-3569">passportnumber</span><span class="sxs-lookup"><span data-stu-id="3aed1-3569">passportnumber</span></span> 
- <span data-ttu-id="3aed1-3570">パスポート</span><span class="sxs-lookup"><span data-stu-id="3aed1-3570">パスポート</span></span> 
- <span data-ttu-id="3aed1-3571">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="3aed1-3571">パスポート番号</span></span> 
- <span data-ttu-id="3aed1-3572">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="3aed1-3572">パスポートのNum</span></span> 
- <span data-ttu-id="3aed1-3573">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="3aed1-3573">パスポート＃</span></span> 
- <span data-ttu-id="3aed1-3574">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="3aed1-3574">Numéro de passeport</span></span> 
- <span data-ttu-id="3aed1-3575">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="3aed1-3575">Passeport n °</span></span> 
- <span data-ttu-id="3aed1-3576">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="3aed1-3576">Passeport Non</span></span> 
- <span data-ttu-id="3aed1-3577">Passeport #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3577">Passeport #</span></span> 
- <span data-ttu-id="3aed1-3578">포트 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3578">Passeport#</span></span> 
- <span data-ttu-id="3aed1-3579">지/포트 아님</span><span class="sxs-lookup"><span data-stu-id="3aed1-3579">PasseportNon</span></span> 
- <span data-ttu-id="3aed1-3580">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="3aed1-3580">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="3aed1-3581">미국 은행 계좌 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3581">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3582">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3582">Format</span></span>

<span data-ttu-id="3aed1-3583">8-17자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3583">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3584">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3584">Pattern</span></span>

<span data-ttu-id="3aed1-3585">8-17자리 연속 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3585">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3586">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3586">Checksum</span></span>

<span data-ttu-id="3aed1-3587">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3587">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3588">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3588">Definition</span></span>

<span data-ttu-id="3aed1-3589">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3589">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3590">Regex_usa_bank_account_number 정규식이 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3590">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3591">Keyword_usa_Bank_Account의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3591">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```xml
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3592">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3592">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="3aed1-3593">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="3aed1-3593">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="3aed1-3594">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3594">Checking Account Number</span></span> 
- <span data-ttu-id="3aed1-3595">Checking Account</span><span class="sxs-lookup"><span data-stu-id="3aed1-3595">Checking Account</span></span> 
- <span data-ttu-id="3aed1-3596">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3596">Checking Account #</span></span> 
- <span data-ttu-id="3aed1-3597">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3597">Checking Acct Number</span></span> 
- <span data-ttu-id="3aed1-3598">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3598">Checking Acct #</span></span> 
- <span data-ttu-id="3aed1-3599">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3599">Checking Acct No.</span></span> 
- <span data-ttu-id="3aed1-3600">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3600">Checking Account No.</span></span> 
- <span data-ttu-id="3aed1-3601">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3601">Bank Account Number</span></span> 
- <span data-ttu-id="3aed1-3602">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3602">Bank Account #</span></span> 
- <span data-ttu-id="3aed1-3603">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3603">Bank Acct Number</span></span> 
- <span data-ttu-id="3aed1-3604">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3604">Bank Acct #</span></span> 
- <span data-ttu-id="3aed1-3605">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3605">Bank Acct No.</span></span> 
- <span data-ttu-id="3aed1-3606">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3606">Bank Account No.</span></span> 
- <span data-ttu-id="3aed1-3607">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3607">Savings Account Number</span></span> 
- <span data-ttu-id="3aed1-3608">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3608">Savings Account.</span></span> 
- <span data-ttu-id="3aed1-3609">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3609">Savings Account #</span></span> 
- <span data-ttu-id="3aed1-3610">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3610">Savings Acct Number</span></span> 
- <span data-ttu-id="3aed1-3611">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3611">Savings Acct #</span></span> 
- <span data-ttu-id="3aed1-3612">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3612">Savings Acct No.</span></span> 
- <span data-ttu-id="3aed1-3613">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3613">Savings Account No.</span></span> 
- <span data-ttu-id="3aed1-3614">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3614">Debit Account Number</span></span> 
- <span data-ttu-id="3aed1-3615">Debit Account</span><span class="sxs-lookup"><span data-stu-id="3aed1-3615">Debit Account</span></span> 
- <span data-ttu-id="3aed1-3616">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3616">Debit Account #</span></span> 
- <span data-ttu-id="3aed1-3617">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3617">Debit Acct Number</span></span> 
- <span data-ttu-id="3aed1-3618">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3618">Debit Acct #</span></span> 
- <span data-ttu-id="3aed1-3619">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3619">Debit Acct No.</span></span> 
- <span data-ttu-id="3aed1-3620">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3620">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="3aed1-3621">미국 운전 면허 번호</span><span class="sxs-lookup"><span data-stu-id="3aed1-3621">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3622">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3622">Format</span></span>

<span data-ttu-id="3aed1-3623">주마다 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3623">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3624">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3624">Pattern</span></span>

<span data-ttu-id="3aed1-3625">주마다 다릅니다(예: 뉴욕).</span><span class="sxs-lookup"><span data-stu-id="3aed1-3625">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="3aed1-3626">Ddd ddd ddd와 같이 9 자리 숫자는 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3626">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="3aed1-3627">Ddddddddd와 같은 9 자리 숫자가 일치 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3627">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3628">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3628">Checksum</span></span>

<span data-ttu-id="3aed1-3629">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3629">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3630">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3630">Definition</span></span>

<span data-ttu-id="3aed1-3631">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3631">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3632">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3632">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3633">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3633">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="3aed1-3634">Keyword_us_drivers_license에서 키워드가 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3634">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="3aed1-3635">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3635">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3636">Func_new_york_drivers_license_number 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3636">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3637">Keyword_[state_name]_drivers_license_name의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3637">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="3aed1-3638">Keyword_us_drivers_license_abbreviations의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3638">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="3aed1-3639">Keyword_us_drivers_license의 키워드가 발견되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3639">No keyword from Keyword_us_drivers_license is found.</span></span>

```xml
<Entity id="dfeb356f-61cd-459e-bf0f-7c6d28b458c6 patternsProximity="300">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license" />
    </Pattern>
    <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license_abbreviations" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_us_drivers_license" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3640">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3640">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="3aed1-3641">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="3aed1-3641">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="3aed1-3642">DL</span><span class="sxs-lookup"><span data-stu-id="3aed1-3642">DL</span></span> 
- <span data-ttu-id="3aed1-3643">된다</span><span class="sxs-lookup"><span data-stu-id="3aed1-3643">DLS</span></span> 
- <span data-ttu-id="3aed1-3644">CDL</span><span class="sxs-lookup"><span data-stu-id="3aed1-3644">CDL</span></span> 
- <span data-ttu-id="3aed1-3645">CDLS</span><span class="sxs-lookup"><span data-stu-id="3aed1-3645">CDLS</span></span> 
- <span data-ttu-id="3aed1-3646">ID</span><span class="sxs-lookup"><span data-stu-id="3aed1-3646">ID</span></span> 
- <span data-ttu-id="3aed1-3647">번호가</span><span class="sxs-lookup"><span data-stu-id="3aed1-3647">IDs</span></span> 
- <span data-ttu-id="3aed1-3648">DL #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3648">DL#</span></span> 
- <span data-ttu-id="3aed1-3649">된다 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3649">DLS#</span></span> 
- <span data-ttu-id="3aed1-3650">CDL #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3650">CDL#</span></span> 
- <span data-ttu-id="3aed1-3651">CDLS #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3651">CDLS#</span></span> 
- <span data-ttu-id="3aed1-3652">I #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3652">ID#</span></span>
- <span data-ttu-id="3aed1-3653">번호가 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3653">IDs#</span></span> 
- <span data-ttu-id="3aed1-3654">ID number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3654">ID number</span></span> 
- <span data-ttu-id="3aed1-3655">ID numbers</span><span class="sxs-lookup"><span data-stu-id="3aed1-3655">ID numbers</span></span> 
- <span data-ttu-id="3aed1-3656">LIC</span><span class="sxs-lookup"><span data-stu-id="3aed1-3656">LIC</span></span> 
- <span data-ttu-id="3aed1-3657">LIC #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3657">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="3aed1-3658">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="3aed1-3658">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="3aed1-3659">DriverLic</span><span class="sxs-lookup"><span data-stu-id="3aed1-3659">DriverLic</span></span> 
- <span data-ttu-id="3aed1-3660">DriverLics</span><span class="sxs-lookup"><span data-stu-id="3aed1-3660">DriverLics</span></span> 
- <span data-ttu-id="3aed1-3661">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="3aed1-3661">DriverLicense</span></span> 
- <span data-ttu-id="3aed1-3662">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-3662">DriverLicenses</span></span> 
- <span data-ttu-id="3aed1-3663">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-3663">Driver Lic</span></span> 
- <span data-ttu-id="3aed1-3664">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-3664">Driver Lics</span></span> 
- <span data-ttu-id="3aed1-3665">Driver License</span><span class="sxs-lookup"><span data-stu-id="3aed1-3665">Driver License</span></span> 
- <span data-ttu-id="3aed1-3666">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-3666">Driver Licenses</span></span> 
- <span data-ttu-id="3aed1-3667">DriversLic</span><span class="sxs-lookup"><span data-stu-id="3aed1-3667">DriversLic</span></span> 
- <span data-ttu-id="3aed1-3668">DriversLics</span><span class="sxs-lookup"><span data-stu-id="3aed1-3668">DriversLics</span></span> 
- <span data-ttu-id="3aed1-3669">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-3669">DriversLicense</span></span> 
- <span data-ttu-id="3aed1-3670">드라이버 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-3670">DriversLicenses</span></span> 
- <span data-ttu-id="3aed1-3671">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-3671">Drivers Lic</span></span> 
- <span data-ttu-id="3aed1-3672">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-3672">Drivers Lics</span></span> 
- <span data-ttu-id="3aed1-3673">Drivers License</span><span class="sxs-lookup"><span data-stu-id="3aed1-3673">Drivers License</span></span> 
- <span data-ttu-id="3aed1-3674">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-3674">Drivers Licenses</span></span> 
- <span data-ttu-id="3aed1-3675">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-3675">Driver'Lic</span></span> 
- <span data-ttu-id="3aed1-3676">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-3676">Driver'Lics</span></span> 
- <span data-ttu-id="3aed1-3677">Driver' 라이선스</span><span class="sxs-lookup"><span data-stu-id="3aed1-3677">Driver'License</span></span> 
- <span data-ttu-id="3aed1-3678">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-3678">Driver'Licenses</span></span> 
- <span data-ttu-id="3aed1-3679">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-3679">Driver' Lic</span></span> 
- <span data-ttu-id="3aed1-3680">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-3680">Driver' Lics</span></span> 
- <span data-ttu-id="3aed1-3681">Driver' License</span><span class="sxs-lookup"><span data-stu-id="3aed1-3681">Driver' License</span></span> 
- <span data-ttu-id="3aed1-3682">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-3682">Driver' Licenses</span></span>
- <span data-ttu-id="3aed1-3683">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="3aed1-3683">Driver'sLic</span></span> 
- <span data-ttu-id="3aed1-3684">Drivers (Slics)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3684">Driver'sLics</span></span> 
- <span data-ttu-id="3aed1-3685">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="3aed1-3685">Driver'sLicense</span></span> 
- <span data-ttu-id="3aed1-3686">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-3686">Driver'sLicenses</span></span> 
- <span data-ttu-id="3aed1-3687">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="3aed1-3687">Driver's Lic</span></span> 
- <span data-ttu-id="3aed1-3688">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="3aed1-3688">Driver's Lics</span></span> 
- <span data-ttu-id="3aed1-3689">Driver's License</span><span class="sxs-lookup"><span data-stu-id="3aed1-3689">Driver's License</span></span> 
- <span data-ttu-id="3aed1-3690">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="3aed1-3690">Driver's Licenses</span></span> 
- <span data-ttu-id="3aed1-3691">identification number</span><span class="sxs-lookup"><span data-stu-id="3aed1-3691">identification number</span></span> 
- <span data-ttu-id="3aed1-3692">identification numbers</span><span class="sxs-lookup"><span data-stu-id="3aed1-3692">identification numbers</span></span> 
- <span data-ttu-id="3aed1-3693">identification #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3693">identification #</span></span> 
- <span data-ttu-id="3aed1-3694">id card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3694">id card</span></span> 
- <span data-ttu-id="3aed1-3695">id cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-3695">id cards</span></span> 
- <span data-ttu-id="3aed1-3696">identification card</span><span class="sxs-lookup"><span data-stu-id="3aed1-3696">identification card</span></span> 
- <span data-ttu-id="3aed1-3697">identification cards</span><span class="sxs-lookup"><span data-stu-id="3aed1-3697">identification cards</span></span> 
- <span data-ttu-id="3aed1-3698">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3698">DriverLic#</span></span> 
- <span data-ttu-id="3aed1-3699">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3699">DriverLics#</span></span> 
- <span data-ttu-id="3aed1-3700">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3700">DriverLicense#</span></span> 
- <span data-ttu-id="3aed1-3701">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3701">DriverLicenses#</span></span> 
- <span data-ttu-id="3aed1-3702">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3702">Driver Lic#</span></span> 
- <span data-ttu-id="3aed1-3703">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3703">Driver Lics#</span></span> 
- <span data-ttu-id="3aed1-3704">Driver License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3704">Driver License#</span></span> 
- <span data-ttu-id="3aed1-3705">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3705">Driver Licenses#</span></span> 
- <span data-ttu-id="3aed1-3706">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3706">DriversLic#</span></span> 
- <span data-ttu-id="3aed1-3707">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3707">DriversLics#</span></span> 
- <span data-ttu-id="3aed1-3708">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3708">DriversLicense#</span></span> 
- <span data-ttu-id="3aed1-3709">드라이버 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3709">DriversLicenses#</span></span> 
- <span data-ttu-id="3aed1-3710">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3710">Drivers Lic#</span></span> 
- <span data-ttu-id="3aed1-3711">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3711">Drivers Lics#</span></span> 
- <span data-ttu-id="3aed1-3712">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3712">Drivers License#</span></span> 
- <span data-ttu-id="3aed1-3713">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3713">Drivers Licenses#</span></span> 
- <span data-ttu-id="3aed1-3714">Driver' Lic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3714">Driver'Lic#</span></span> 
- <span data-ttu-id="3aed1-3715">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3715">Driver'Lics#</span></span> 
- <span data-ttu-id="3aed1-3716">Driver' 라이선스 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3716">Driver'License#</span></span> 
- <span data-ttu-id="3aed1-3717">Driver'Licenses #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3717">Driver'Licenses#</span></span> 
- <span data-ttu-id="3aed1-3718">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3718">Driver' Lic#</span></span> 
- <span data-ttu-id="3aed1-3719">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3719">Driver' Lics#</span></span> 
- <span data-ttu-id="3aed1-3720">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3720">Driver' License#</span></span> 
- <span data-ttu-id="3aed1-3721">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3721">Driver' Licenses#</span></span> 
- <span data-ttu-id="3aed1-3722">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3722">Driver'sLic#</span></span> 
- <span data-ttu-id="3aed1-3723">Drivers (Slics) #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3723">Driver'sLics#</span></span> 
- <span data-ttu-id="3aed1-3724">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3724">Driver'sLicense#</span></span> 
- <span data-ttu-id="3aed1-3725">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3725">Driver'sLicenses#</span></span> 
- <span data-ttu-id="3aed1-3726">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3726">Driver's Lic#</span></span> 
- <span data-ttu-id="3aed1-3727">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3727">Driver's Lics#</span></span> 
- <span data-ttu-id="3aed1-3728">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3728">Driver's License#</span></span> 
- <span data-ttu-id="3aed1-3729">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3729">Driver's Licenses#</span></span> 
- <span data-ttu-id="3aed1-3730">id card#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3730">id card#</span></span> 
- <span data-ttu-id="3aed1-3731">id cards#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3731">id cards#</span></span> 
- <span data-ttu-id="3aed1-3732">identification card#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3732">identification card#</span></span> 
- <span data-ttu-id="3aed1-3733">identification cards#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3733">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="3aed1-3734">Keyword_ [state_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="3aed1-3734">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="3aed1-3735">주 약어(예: "NY")</span><span class="sxs-lookup"><span data-stu-id="3aed1-3735">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="3aed1-3736">주 이름(예: "New York")</span><span class="sxs-lookup"><span data-stu-id="3aed1-3736">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="3aed1-3737">미국 ITIN(개인 납세자 번호)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3737">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3738">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3738">Format</span></span>

<span data-ttu-id="3aed1-3739">"9"로 시작되고, "7" 또는 "8"을 4번째 숫자로 포함하고, 경우에 따라 공백이나 대시로 서식이 지정된 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3739">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3740">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3740">Pattern</span></span>

<span data-ttu-id="3aed1-3741">서식이</span><span class="sxs-lookup"><span data-stu-id="3aed1-3741">Formatted:</span></span>
- <span data-ttu-id="3aed1-3742">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3742">The digit "9"</span></span> 
- <span data-ttu-id="3aed1-3743">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3743">Two digits</span></span> 
- <span data-ttu-id="3aed1-3744">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="3aed1-3744">A space or dash</span></span> 
- <span data-ttu-id="3aed1-3745">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="3aed1-3745">A "7" or "8"</span></span> 
- <span data-ttu-id="3aed1-3746">1자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3746">A digit</span></span> 
- <span data-ttu-id="3aed1-3747">공백 또는 대시</span><span class="sxs-lookup"><span data-stu-id="3aed1-3747">A space, or dash</span></span> 
- <span data-ttu-id="3aed1-3748">4자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3748">Four digits</span></span>

<span data-ttu-id="3aed1-3749">서식</span><span class="sxs-lookup"><span data-stu-id="3aed1-3749">Unformatted:</span></span>
- <span data-ttu-id="3aed1-3750">"9"자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3750">The digit "9"</span></span> 
- <span data-ttu-id="3aed1-3751">2자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3751">Two digits</span></span> 
- <span data-ttu-id="3aed1-3752">"7" 또는 "8"</span><span class="sxs-lookup"><span data-stu-id="3aed1-3752">A "7" or "8"</span></span> 
- <span data-ttu-id="3aed1-3753">5자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3753">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3754">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3754">Checksum</span></span>

<span data-ttu-id="3aed1-3755">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3755">No</span></span>

### <a name="definition"></a><span data-ttu-id="3aed1-3756">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3756">Definition</span></span>

<span data-ttu-id="3aed1-3757">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3757">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3758">Func_formatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3758">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3759">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3759">At least one of the following is true:</span></span>
    - <span data-ttu-id="3aed1-3760">Keyword_itin의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3760">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="3aed1-3761">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3761">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="3aed1-3762">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3762">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="3aed1-3763">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3763">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="3aed1-3764">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3765">Func_unformatted_itin 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3765">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3766">다음 중 하나 이상이 충족됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3766">At least one of the following is true:</span></span>
    - <span data-ttu-id="3aed1-3767">Keyword_itin_collaborative의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3767">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="3aed1-3768">Func_us_address 함수가 올바른 날짜 형식의 주소를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3768">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="3aed1-3769">Func_us_date 함수가 올바른 날짜 형식의 날짜를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3769">The function Func_us_date finds a date in the right date format.</span></span>

```xml
<!-- U.S. Individual Taxpayer Identification Number (ITIN) -->
<Entity id="e55e2a32-f92d-4985-a35d-a0b269eb687b" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_formatted_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
          <Match idRef="Keyword_itin_collaborative" />
        </Any>
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_itin" />
        <Match idRef="Keyword_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin_collaborative" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3770">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3770">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="3aed1-3771">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="3aed1-3771">Keyword_itin</span></span>

- <span data-ttu-id="3aed1-3772">taxpayer</span><span class="sxs-lookup"><span data-stu-id="3aed1-3772">taxpayer</span></span> 
- <span data-ttu-id="3aed1-3773">tax id</span><span class="sxs-lookup"><span data-stu-id="3aed1-3773">tax id</span></span> 
- <span data-ttu-id="3aed1-3774">tax identification</span><span class="sxs-lookup"><span data-stu-id="3aed1-3774">tax identification</span></span> 
- <span data-ttu-id="3aed1-3775">itin</span><span class="sxs-lookup"><span data-stu-id="3aed1-3775">itin</span></span> 
- <span data-ttu-id="3aed1-3776">ssn</span><span class="sxs-lookup"><span data-stu-id="3aed1-3776">ssn</span></span> 
- <span data-ttu-id="3aed1-3777">언급</span><span class="sxs-lookup"><span data-stu-id="3aed1-3777">tin</span></span> 
- <span data-ttu-id="3aed1-3778">social security</span><span class="sxs-lookup"><span data-stu-id="3aed1-3778">social security</span></span> 
- <span data-ttu-id="3aed1-3779">tax payer</span><span class="sxs-lookup"><span data-stu-id="3aed1-3779">tax payer</span></span> 
- <span data-ttu-id="3aed1-3780">itins</span><span class="sxs-lookup"><span data-stu-id="3aed1-3780">itins</span></span> 
- <span data-ttu-id="3aed1-3781">taxid</span><span class="sxs-lookup"><span data-stu-id="3aed1-3781">taxid</span></span> 
- <span data-ttu-id="3aed1-3782">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="3aed1-3782">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="3aed1-3783">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="3aed1-3783">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="3aed1-3784">License</span><span class="sxs-lookup"><span data-stu-id="3aed1-3784">License</span></span> 
- <span data-ttu-id="3aed1-3785">DL</span><span class="sxs-lookup"><span data-stu-id="3aed1-3785">DL</span></span> 
- <span data-ttu-id="3aed1-3786">DOB</span><span class="sxs-lookup"><span data-stu-id="3aed1-3786">DOB</span></span> 
- <span data-ttu-id="3aed1-3787">생년월일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3787">Birthdate</span></span> 
- <span data-ttu-id="3aed1-3788">생일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3788">Birthday</span></span> 
- <span data-ttu-id="3aed1-3789">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="3aed1-3789">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="3aed1-3790">미국 SSN(사회 보험 번호)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3790">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="3aed1-3791">형식일</span><span class="sxs-lookup"><span data-stu-id="3aed1-3791">Format</span></span>

<span data-ttu-id="3aed1-3792">서식 있는 패턴 또는 서식 없는 패턴으로 표시될 수 있는 9자리 숫자</span><span class="sxs-lookup"><span data-stu-id="3aed1-3792">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="3aed1-3793">Mid가 2011 이전에 실행 된 경우 SSN은 특정 범위 내에서 번호의 특정 부분이 유효한 지 확인 하는 강력한 서식을 사용 해야 하지만 검사 값은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3793">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="3aed1-3794">패턴</span><span class="sxs-lookup"><span data-stu-id="3aed1-3794">Pattern</span></span>

<span data-ttu-id="3aed1-3795">다음의 네 가지 패턴에서 SSNs를 검색 하는 함수는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3795">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="3aed1-3796">Func_ssn는 대시 또는 공백으로 서식이 지정 된 2011 이전 수준의 서식으로 SSNs를 찾습니다 (ddd-dd-dddd 또는 ddd dd dddd).</span><span class="sxs-lookup"><span data-stu-id="3aed1-3796">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="3aed1-3797">Func_unformatted_ssn는 형식이 지정 되지 않은 2011 이전 형식으로 서식이 지정 된 SSNs를 찾고 (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="3aed1-3797">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="3aed1-3798">Func_randomized_formatted_ssn는 대시 또는 공백으로 서식이 지정 된 post-2011 SSNs를 찾습니다 (ddd-dd-dddd 또는 ddd dd dddd).</span><span class="sxs-lookup"><span data-stu-id="3aed1-3798">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="3aed1-3799">Func_randomized_unformatted_ssn는 형식 없는 2011 SSNs를 찾습니다 (ddddddddd).</span><span class="sxs-lookup"><span data-stu-id="3aed1-3799">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="3aed1-3800">제외</span><span class="sxs-lookup"><span data-stu-id="3aed1-3800">Checksum</span></span>

<span data-ttu-id="3aed1-3801">아니요</span><span class="sxs-lookup"><span data-stu-id="3aed1-3801">No</span></span>


### <a name="definition"></a><span data-ttu-id="3aed1-3802">정의</span><span class="sxs-lookup"><span data-stu-id="3aed1-3802">Definition</span></span>

<span data-ttu-id="3aed1-3803">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 85% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3803">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3804">Func_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3804">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3805">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3805">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="3aed1-3806">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 75% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3806">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3807">Func_unformatted_ssn 함수가 해당 패턴과 일치 하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3807">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3808">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3808">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="3aed1-3809">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 65% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3809">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3810">Func_randomized_formatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3810">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3811">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3811">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="3aed1-3812">DLP 정책은 다음과 같은 경우 이러한 유형의 중요한 정보가 300자 이내의 접근성으로 검색되었음을 55% 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3812">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="3aed1-3813">Func_randomized_unformatted_ssn 함수가 해당 패턴과 일치하는 콘텐츠를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3813">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="3aed1-3814">Keyword_ssn의 키워드가 발견되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3aed1-3814">A keyword from Keyword_ssn is found.</span></span>


```xml
<!-- U.S. Social Security Number (SSN) -->
  <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
  </Entity>
```

### <a name="keywords"></a><span data-ttu-id="3aed1-3815">키워드</span><span class="sxs-lookup"><span data-stu-id="3aed1-3815">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="3aed1-3816">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="3aed1-3816">Keyword_ssn</span></span>

- <span data-ttu-id="3aed1-3817">Social Security</span><span class="sxs-lookup"><span data-stu-id="3aed1-3817">Social Security</span></span> 
- <span data-ttu-id="3aed1-3818">Social Security#</span><span class="sxs-lookup"><span data-stu-id="3aed1-3818">Social Security#</span></span> 
- <span data-ttu-id="3aed1-3819">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="3aed1-3819">Soc Sec</span></span> 
- <span data-ttu-id="3aed1-3820">SSN</span><span class="sxs-lookup"><span data-stu-id="3aed1-3820">SSN</span></span> 
- <span data-ttu-id="3aed1-3821">있는 SSN</span><span class="sxs-lookup"><span data-stu-id="3aed1-3821">SSNS</span></span> 
- <span data-ttu-id="3aed1-3822">SSN #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3822">SSN#</span></span> 
- <span data-ttu-id="3aed1-3823">대비 #</span><span class="sxs-lookup"><span data-stu-id="3aed1-3823">SS#</span></span> 
- <span data-ttu-id="3aed1-3824">생길</span><span class="sxs-lookup"><span data-stu-id="3aed1-3824">SSID</span></span> 
   
