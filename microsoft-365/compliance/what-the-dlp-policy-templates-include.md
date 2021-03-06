---
title: DLP 정책 템플릿에 포함되는 내용
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.DLPNewPolicyFromTemplate
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Office 365 보안 & 준수 센터의 DLP (데이터 손실 방지) 정책 템플릿에 대해 알아봅니다.
ms.openlocfilehash: 80f1d4f93ecf7c3cb327633b1626ddb4ccbcbaa9
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44819268"
---
# <a name="what-the-dlp-policy-templates-include"></a>DLP 정책 템플릿에 포함되는 내용

보안 및 준수 센터의 DLP (데이터 손실 방지)에는 &amp; HIPAA (미국 의료 보험 act), 미국 금융-gramm-leach-bliley-Gramm-leach-bliley act (GLBA) 또는 미국 Patriot act의 중요 한 정보를 보호 하는 데 도움이 되는 일반적인 준수 요구 사항을 해결 하는 기본 제공 정책 템플릿이 포함 되어 있습니다. 이 항목에는 모든 정책 템플릿, 사용자가 찾은 중요 한 정보의 유형 및 기본 조건 및 작업에 대 한 정보가 나와 있습니다. 이 항목에 각 정책 템플릿 구성 방식에 대한 모든 세부 사항이 나와 있지는 않지만 사용자의 상황에서 시작점으로 사용하기 가장 적합한 템플릿을 결정하는 데 충분한 정보를 제공합니다. 이러한 정책 템플릿을 특정 요구 사항에 맞게 사용자 지정할 수 있습니다.
  
## <a name="australia-financial-data"></a>호주 재무 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|호주 재무: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  SWIFT 코드 — 최소 개수 1, 최대 개수 9  <br/>  호주 세금 파일 번호 - 최소 개수 1, 최대 개수 9  <br/>  호주 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|호주 재무: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  SWIFT 코드 — 최소 개수 10, 최대 개수 모두  <br/>  호주 세금 파일 번호 - 최소 개수 10, 최대 개수 모두  <br/>  호주 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="australia-health-records-act-hrip-act"></a>호주 HRIP Act(Health Records Act)

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|호주 HRIP: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  호주 세금 파일 번호 - 최소 개수 1, 최대 개수 9  <br/>  호주 의료 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|호주 HRIP: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  호주 세금 파일 번호 - 최소 개수 10, 최대 개수 모두  <br/>  호주 의료 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="australia-personally-identifiable-information-pii-data"></a>호주 PII(개인 식별 정보) 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|호주 PII: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  호주 세금 파일 번호 - 최소 개수 1, 최대 개수 9  <br/>  호주 운전 면허 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|호주 PII: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  호주 세금 파일 번호 - 최소 개수 10, 최대 개수 모두  <br/>  호주 운전 면허 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="australia-privacy-act"></a>호주 개인 정보 보호법

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|호주 개인 정보 보호: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  호주 운전 면허 번호 - 최소 개수 1, 최대 개수 9  <br/>  호주 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|호주 개인 정보 보호: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  호주 운전 면허 번호 - 최소 개수 10, 최대 개수 모두  <br/>  호주 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="canada-financial-data"></a>캐나다 재무 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|캐나다 재무 데이터: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|캐나다 재무 데이터: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="canada-health-information-act-hia"></a>캐나다 HIA(Health Information Act)

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|캐나다 HIA: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 사회 보험 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 보건 서비스 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|캐나다 HIA: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 사회 보험 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 보건 서비스 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="canada-personal-health-act-phipa---ontario"></a>캐나다 PHIPA(Personal Health Act) - 온타리오

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|캐나다 PHIPA: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 사회 보험 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 보건 서비스 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|캐나다 PHIPA: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 사회 보험 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 보건 서비스 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="canada-personal-health-information-act-phia---manitoba"></a>캐나다 PHIA(Personal Health Information Act) - 매니토바

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|캐나다 PHIA: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 사회 보험 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 보건 서비스 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|캐나다 PHIA: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 사회 보험 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 보건 서비스 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="canada-personal-information-protection-act-pipa"></a>캐나다 PIPA(Personal Information Protection Act)

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|캐나다 PIPA: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 사회 보험 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 보건 서비스 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|캐나다 PIPA: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 사회 보험 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 보건 서비스 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="canada-personal-information-protection-act-pipeda"></a>캐나다 PIPEDA(Personal Information Protection Act)

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|캐나다 PIPEDA: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 운전 면허 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 사회 보험 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 보건 서비스 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|캐나다 PIPEDA: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 운전 면허 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 사회 보험 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 보건 서비스 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="canada-personally-identifiable-information-pii-data"></a>캐나다 PII(개인 식별 정보) 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|캐나다 PII: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 운전 면허 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 사회 보험 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 보건 서비스 번호 - 최소 개수 1, 최대 개수 9  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|캐나다 PII: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  캐나다 운전 면허 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 사회 보험 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 보건 서비스 번호 - 최소 개수 10, 최대 개수 모두  <br/>  캐나다 PHIN(개인 건강 식별 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="france-data-protection-act"></a>프랑스 데이터 보호법

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|프랑스 DPA: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  프랑스 국가 ID 카드(CNI) - 최소 개수 1, 최대 개수 9  <br/>  프랑스 사회 보험 번호(INSEE) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|프랑스 DPA: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  프랑스 국가 ID 카드(CNI) - 최소 개수 10, 최대 개수 모두  <br/>  프랑스 사회 보험 번호(INSEE) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="france-financial-data"></a>프랑스 재무 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|프랑스 재무: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  유럽 직불 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|프랑스 재무: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  유럽 직불 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="france-personally-identifiable-information-pii-data"></a>프랑스 PII(개인 식별 정보) 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|프랑스 PII: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  프랑스 사회 보험 번호(INSEE) - 최소 개수 1, 최대 개수 9  <br/>  프랑스 운전 면허 번호 - 최소 개수 1, 최대 개수 9  <br/>  프랑스 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  프랑스 국가 ID 카드(CNI) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|프랑스 PII: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  프랑스 사회 보험 번호(INSEE) - 최소 개수 10, 최대 개수 모두  <br/>  프랑스 운전 면허 번호 - 최소 개수 10, 최대 개수 모두  <br/>  프랑스 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  프랑스 국가 ID 카드(CNI) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="general-data-protection-regulation-gdpr"></a>GDPR(일반 데이터 보호 규정)

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|낮은 볼륨 EU 중요 한 콘텐츠 검색 됨  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  유럽 직불 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  EU 운전 면허 번호-최소 개수 1, 최대 개수 9  <br/>  EU 국가 식별 번호-최소 개수 1, 최대 개수 9  <br/>  EU 여권 번호-최소 개수 1, 최대 개수 9  <br/>  EU (주민 등록 번호) 또는 동등한 ID-최소 개수 1, 최대 개수 9  <br/>  EU 세금 식별 번호 (언급)-최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |관리자에 게 문제 보고서 보내기  <br/> |
|대용량의 유럽 중요 콘텐츠가 발견 됨  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  유럽 직불 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  EU 운전 면허 번호-최소 개수 1, 최대 개수 9  <br/>  EU 국가 식별 번호-최소 개수 1, 최대 개수 9  <br/>  EU 여권 번호-최소 개수 1, 최대 개수 9  <br/>  EU (주민 등록 번호) 또는 동등한 ID-최소 개수 1, 최대 개수 9  <br/>  EU 세금 식별 번호 (언급)-최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 외부 사용자에 대 한 콘텐츠에 대 한 액세스 제한  <br/>  전자 메일 및 정책 팁으로 사용자에 게 알림  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  관리자에 게 문제 보고서 보내기  <br/> |
   
## <a name="germany-financial-data"></a>독일 재무 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|독일 재무 데이터: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  유럽 직불 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|독일 재무 데이터: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  유럽 직불 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="germany-personally-identifiable-information-pii-data"></a>독일 PII(개인 식별 정보) 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|독일 PII: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  독일 운전 면허 번호 - 최소 개수 1, 최대 개수 9  <br/>  독일 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|독일 PII: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  독일 운전 면허 번호 - 최소 개수 10, 최대 개수 모두  <br/>  독일 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="israel-financial-data"></a>이스라엘 재무 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|이스라엘 재무 데이터: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  이스라엘 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  SWIFT 코드 — 최소 개수 1, 최대 개수 9  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|이스라엘 재무 데이터: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  이스라엘 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  SWIFT 코드 — 최소 개수 10, 최대 개수 모두  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="israel-personally-identifiable-information-pii-data"></a>이스라엘 PII(개인 식별 정보) 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|이스라엘 PII: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  이스라엘 국가 코드 — 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|이스라엘 PII: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  이스라엘 국가 코드 — 최소 개수 10, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="israel-protection-of-privacy"></a>이스라엘 개인 정보 보호

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|이스라엘 개인 정보 보호: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  이스라엘 국가 코드 — 최소 개수 1, 최대 개수 9  <br/>  이스라엘 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|이스라엘 개인 정보 보호: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  이스라엘 국가 코드 — 최소 개수 10, 최대 개수 9  <br/>  이스라엘 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="japan-financial-data"></a>일본 재무 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|일본 재무: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  일본 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|일본 재무: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  일본 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="japan-personally-identifiable-information-pii-data"></a>일본 PII(개인 식별 정보) 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|일본 PII: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  일본 거주자 등록 번호 - 최소 개수 1, 최대 개수 9  <br/>  일본 SIN(사회 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|일본 PII: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  일본 거주자 등록 번호 - 최소 개수 10, 최대 개수 모두  <br/>  일본 SIN(사회 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="japan-protection-of-personal-information"></a>일본 개인 정보 보호

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|일본 PPI: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  일본 거주자 등록 번호 - 최소 개수 1, 최대 개수 9  <br/>  일본 SIN(사회 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|일본 PPI: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  일본 거주자 등록 번호 - 최소 개수 10, 최대 개수 모두  <br/>  일본 SIN(사회 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="pci-data-security-standard-pci-dss"></a>PCI DSS(PCI Data Security Standard)

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|PCI-DSS 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|PCI-DSS 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="saudi-arabia---anti-cyber-crime-law"></a>사우디 아라비아 - 사이버 범죄 방지법

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|사우디아라비아 ACC: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  SWIFT 코드 — 최소 개수 1, 최대 개수 9  <br/>  IBAN(국제 은행 계좌 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|사우디아라비아 ACC: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  SWIFT 코드 — 최소 개수 10, 최대 개수 모두  <br/>  IBAN(국제 은행 계좌 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="saudi-arabia-financial-data"></a>사우디 아라비아 재무 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|사우디 아라비아 재무: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  SWIFT 코드 — 최소 개수 1, 최대 개수 9  <br/>  IBAN(국제 은행 계좌 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|사우디 아라비아 재무: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  SWIFT 코드 — 최소 개수 10, 최대 개수 모두  <br/>  IBAN(국제 은행 계좌 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="saudi-arabia-personally-identifiable-information-pii-data"></a>사우디 아라비아 PII(개인 식별 정보) 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|사우디아라비아 PII: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  사우디 아라비아 국가 코드 — 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|사우디아라비아 PII: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  사우디 아라비아 국가 코드 — 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="uk-access-to-medical-reports-act"></a>영국 의료 보고 접근 규제법

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|영국 AMRA: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  영국 국가 의료 서비스 번호-최소 개수 1, 최대 개수 9  <br/>  영국 국가 보험 번호 (NINO)-최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|영국 AMRA: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  영국 국가 의료 서비스 번호-최소 개수 10, 최대 개수 모두  <br/>  영국 국가 보험 번호 (NINO)-최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="uk-data-protection-act"></a>영국 데이터 보호법

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|영국 DPA: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  영국 NINO(국민 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  미국/영국 여권 번호-최소 개수 1, 최대 개수 9  <br/>  SWIFT 코드 — 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|영국 DPA: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  영국 NINO(국민 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  미국/영국 여권 번호-최소 개수 10, 최대 개수 모두  <br/>  SWIFT 코드 — 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="uk-financial-data"></a>영국 재무 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|영국 재무: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  유럽 직불 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  SWIFT 코드 — 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|영국 재무: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  유럽 직불 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  SWIFT 코드 — 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="uk-personal-information-online-code-of-practice-piocp"></a>영국 PIOCP(Personal Information Online Code of Practice)

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|영국 PIOCP: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  영국 NINO(국민 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  영국 국립 보건 서비스 번호 - 최소 개수 1, 최대 개수 9  <br/>  SWIFT 코드 — 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|영국 PIOCP: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  영국 NINO(국민 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  영국 국립 보건 서비스 번호 - 최소 개수 10, 최대 개수 모두  <br/>  SWIFT 코드 — 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="uk-personally-identifiable-information-pii-data"></a>영국 PII(개인 식별 정보) 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|영국 PII: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  영국 NINO(국민 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  미국/영국 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|영국 PII: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  영국 NINO(국민 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  미국/영국 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="uk-privacy-and-electronic-communications-regulations"></a>영국 개인 정보 보호 및 전자 통신 규정

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|영국 PECR: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  SWIFT 코드 — 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|영국 PECR: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  SWIFT 코드 — 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="us-federal-trade-commission-ftc-consumer-rules"></a>미국 FTC(Federal Trade Commission) 소비자 규약

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|미국 FTC 규칙: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  미국 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  ABA 라우팅 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|미국 FTC 규칙: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  미국 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  ABA 라우팅 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="us-financial-data"></a>미국 재무 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|미국 재무: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  미국 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  ABA 라우팅 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|미국 재무: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  미국 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  ABA 라우팅 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="us-gramm-leach-bliley-act-glba"></a>미국 GLBA(Gramm-Leach-Bliley Act)

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|미국 GLBA: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  미국 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  미국 ITIN(개인 납세자 번호) - 최소 개수 1, 최대 개수 9  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|미국 GLBA: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  미국 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  미국 ITIN(개인 납세자 번호) - 최소 개수 10, 최대 개수 모두  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="us-health-insurance-act-hipaa"></a>미국 HIPAA(Health Insurance Act)

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|콘텐츠가 미국 HIPAA와 일치 합니다.  <br/> | 다음과 같은 중요 한 정보가 들어 있습니다.  <br/>  미국 SSN (사회 보장 번호)-최소 개수 1, 최대 개수 모두  <br/>  DEA (약품 집행 기관) 번호-최소 개수 1, 최대 개수 모두  <br/> **AND** <br/>  콘텐츠는 다음 용어 중 하나를 포함 합니다.  <br/>  Diseases의 국제 분류 (ICD-9-CM)-최소 개수 1, 최대 개수 모두  <br/>  Diseases의 국제 분류 (ICD-10cm)-최소 개수 1, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
   
## <a name="us-patriot-act"></a>미국 애국법

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|미국 애국법: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  미국 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  미국 ITIN(개인 납세자 번호) - 최소 개수 1, 최대 개수 9  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|미국 애국법: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  미국 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  미국 ITIN(개인 납세자 번호) - 최소 개수 10, 최대 개수 모두  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="us-personally-identifiable-information-pii-data"></a>미국 PII(개인 식별 정보) 데이터

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|미국 PII: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  미국 ITIN(개인 납세자 번호) - 최소 개수 1, 최대 개수 9  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  미국/영국 여권 번호 - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|미국 PII: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  미국 ITIN(개인 납세자 번호) - 최소 개수 10, 최대 개수 모두  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  미국/영국 여권 번호 - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="us-state-breach-notification-laws"></a>미국 개인 정보 침해 고지법

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|미국 개인 정보 침해: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 1, 최대 개수 9  <br/>  미국 은행 계좌 번호 - 최소 개수 1, 최대 개수 9  <br/>  미국 운전 면허 번호 - 최소 개수 1, 최대 개수 9  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|미국 개인 정보 침해: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  신용 카드 번호 - 최소 개수 10, 최대 개수 모두  <br/>  미국 은행 계좌 번호 - 최소 개수 10, 최대 개수 모두  <br/>  미국 운전 면허 번호 - 최소 개수 10, 최대 개수 모두  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   
## <a name="us-state-social-security-number-confidentiality-laws"></a>미국 사회 보장 번호 기밀 유지법

|**규칙 이름**|**조건 <br/> (중요 한 정보 유형 포함)**|**작업**|
|:-----|:-----|:-----|
|미국 SSN 법률: 외부 공유 콘텐츠 검색 - 낮은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 1, 최대 개수 9  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> |알림 보내기  <br/> |
|미국 SSN 법률: 외부 공유 콘텐츠 검색 - 높은 수  <br/> | 콘텐츠에 중요한 정보가 포함됨:  <br/>  미국 SSN(사회 보험 번호) - 최소 개수 10, 최대 개수 모두  <br/>  콘텐츠 공유 대상:  <br/>  조직 외부의 사용자  <br/> | 콘텐츠에 대한 액세스 차단  <br/>  알림 보내기  <br/>  재정의 허용  <br/>  업무 정당성 필요  <br/>  사고 보고서 보내기  <br/> |
   

