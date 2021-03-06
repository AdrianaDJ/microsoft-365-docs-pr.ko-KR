---
title: Microsoft 365 사용 현황 분석 문제 해결
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: a73632a1-62c8-4a13-8115-913773b30f93
description: Microsoft 365 Usage Analytics 서식 파일 앱의 문제를 해결 하는 방법을 알아봅니다.
ms.openlocfilehash: bf8e4ece7b1e310d91f418f5388cae9aa27f2aa7
ms.sourcegitcommit: e56894917d2aae05705c3b9447388d10e2156183
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48841438"
---
# <a name="troubleshooting-microsoft-365-usage-analytics"></a>Microsoft 365 사용 현황 분석 문제 해결

다음 오류 메시지 목록을 살펴보고 Microsoft 365 사용 현황 분석에서 가장 일반적인 문제에 대 한 도움말을 확인 하세요.
  
    
## <a name="we-are-unable-to-process-your-request-you-have-to-first-subscribe-to-this-data-from-the-microsoft-365-admin-center"></a>요청을 처리할 수 없습니다. 먼저 Microsoft 365 관리 센터에서이 데이터를 구독 해야 합니다.

 **오류 코드:** 422 
  
 **이 메시지가 표시 되는 위치:** Microsoft 365 사용 현황 분석 서식 파일 앱에 연결 하거나 Microsoft 365 보고 Api를 직접 호출 하는 경우 Power BI에서 사용할 수 있습니다. 
  
 **원인:** 앱에 연결 하려면 먼저 Microsoft 365 관리 센터에서 데이터를 구독 해야 합니다. 이 단계를 먼저 수행 하지 않으면 Microsoft 365 테 넌 트 ID를 제공한 경우에도 서식 파일 앱에 연결할 수 없게 됩니다. 
  
 **이 오류를 해결 하려면** 데이터를 구독 하려면 관리 센터의 사용 현황 보고서로 이동 하 여 \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> 기본 대시보드 페이지에서 Microsoft 365 Usage analytics 타일을 찾습니다. **시작** 단추를 선택 하 고 열리는 **보고서** 창에서 **Power BI 설정에 대 한 Microsoft 365 사용 현황 분석을 사용 하 여 데이터를 사용할 수 있도록** 설정 하 고 **저장** 합니다.
  
## <a name="we-are-processing-your-data"></a>데이터를 처리하고 있습니다.

 **이 메시지가 표시 되는 위치:** Microsoft 365 관리 센터에서 **사용** 대시보드의 **microsoft 365 usage analytics** 타일 
  
 **원인:** Microsoft 365 관리 센터에서 [서식 파일 앱의 데이터](enable-usage-analytics.md) 를 표시 하도록 선택 하면 microsoft 365 시스템에서 조직의 기록 사용 현황 데이터를 생성 하기 시작 합니다. 테넌트의 크기에 따라 이 단계는 2시간에서 48시간까지 걸릴 수 있습니다. 
  
 **이 문제를 해결 하려면** 하지만 3 일 후에 **데이터가** 변경 되지 않으면 [Microsoft 365에 문의 하 여 비즈니스 지원을](../contact-support-for-business-products.md)받을 수 있습니다.
  
## <a name="we-are-unable-to-process-your-request-at-this-time-we-are-still-preparing-the-data-for-your-organization"></a>현재 요청을 처리할 수 없습니다. 아직 조직의 데이터를 준비하고 있습니다.

 **오류 코드:** 423 
  
 **이 메시지가 표시 되는 위치:** Power BI에서 Microsoft 365 사용 현황 분석 서식 파일 앱에 연결 하거나 Microsoft 365 보고 Api를 직접 호출 하는 경우 
  
 **원인:** 관리 센터에서 [서식 파일 앱의 데이터](enable-usage-analytics.md) 를 표시 하도록 선택 하면 Microsoft 365 시스템에서 조직의 기록 사용 현황 데이터를 생성 하기 시작 합니다. 테 넌 트의 크기에 따라이 단계는 두 시간에서 48 시간까지 소요 될 수 있습니다. 
  
 **이 문제를 해결 하려면** 단, 메시지가 시작 된 후 3 일 이내에 **데이터가** 변경 되지 않는 경우 [Microsoft 365에 문의 하 여 비즈니스 지원을](../contact-support-for-business-products.md)받을 수 있습니다.
  
## <a name="the-tenant-id-you-provided-is-not-in-the-correct-format"></a>입력하신 테넌트 ID의 형식이 올바르지 않습니다.

 **오류 코드:** 4:00 
  
 **이 메시지가 표시 되는 위치:** Power BI에서 Microsoft 365 사용 현황 분석 서식 파일 앱에 연결 하거나 Microsoft 365 보고 Api를 직접 호출 하는 경우 
  
 **원인:** 테 넌 트 ID는 guid 이며,이 형식은 xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx 형식 이어야 합니다. 테 넌 트 입력 상자에 다른 문자열을 입력 하면이 오류가 발생 합니다. 
  
 **이 오류를 해결 하려면** 관리 센터의 \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">사용 현황</a> 보고서로 이동 하 여 기본 대시보드 페이지에서 Microsoft 365 Usage analytics 타일을 찾습니다. 테 넌 트 ID가 타일에 나열 됩니다. 서식 파일 앱에 연결 하기 위해 여기에서 복사 하 여 대화 상자에 붙여 넣을 수 있습니다. 
  
## <a name="the-tenant-id-you-provided-is-not-recognized-by-our-system"></a>입력하신 테넌트 ID가 시스템에서 인식되지 않습니다.

 **오류 코드:** 404 
  
 **이 메시지가 표시 되는 위치:** Microsoft 365 사용 현황 분석 서식 파일 앱에 연결 하거나 Microsoft 365 보고 Api를 직접 호출 하는 경우 Power BI에서 사용할 수 있습니다. 
  
 **원인:** 입력 한 테 넌 트 ID가 올바르지 않거나 존재 하지 않습니다. 
  
 **이 오류를 해결 하려면** 관리 센터의 \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">사용 현황</a> 보고서로 이동 하 여 기본 대시보드 페이지에서 Microsoft 365 Usage analytics 타일을 찾습니다. 테 넌 트 ID가 타일에 나열 됩니다. 서식 파일 앱에 연결 하기 위해 여기에서 복사 하 여 대화 상자에 붙여 넣을 수 있습니다. 
  
## <a name="please-re-enter-your-credentials-to-sign-in-to-power-bi-again"></a>Power BI에 다시 로그인하려면 자격 증명을 다시 입력하세요.

오류 코드: 302
  
 **이 메시지가 표시 되는 위치:** Microsoft 365 사용 현황 분석 서식 파일 앱에 연결 하거나 Microsoft 365 보고 Api를 직접 호출 하는 경우 Power BI에서 사용할 수 있습니다. 
  
 **원인:** 인증 코드 확인에 실패하여 자격 증명을 다시 입력해야 할 수 있습니다. 
  
 **오류 수정 방법:** Power BI에서 로그아웃한 다음 다시 로그인합니다. 
  
## <a name="you-do-not-have-the-right-authorization-to-access-to-this-data-to-be-able-to-gain-access-to-the-data-from-this-service-you-need-to-be-either-a-global-admin-or-any-one-of-the-product-admins"></a>이 데이터에 액세스할 수 있는 권한이 없습니다. 이 서비스에서 데이터에 대한 액세스 권한을 얻으려면 전역 관리자 또는 제품 관리자여야 합니다.

 **오류 코드:** 403 
  
 **이 메시지가 표시 되는 위치:** Microsoft 365 사용 현황 분석 서식 파일 앱에 연결 하거나 Microsoft 365 보고 Api를 직접 호출 하는 경우 Power BI에서 사용할 수 있습니다. 
  
 **원인:** 서식 파일 앱에 연결을 시도한 사용자에 게이 데이터에 액세스 하기 위한 권한 부여 수준이 없기 때문에 인증 코드가 실패 했습니다. 
  
 **이 오류를 해결 하려면** **전역 관리자** , **Exchange 관리자** , **비즈니스용 Skype 관리자** , **SharePoint 관리자** , **전역 독자** 또는 **보고서 구독자** 인 사용자 자격 증명을 제공 하 여 서식 파일 앱에 연결 합니다. 자세한 내용은 [관리자 역할 정보](../add-users/about-admin-roles.md) 를 참조 하세요. 
  
## <a name="refresh-failed"></a>새로 고치지 못했습니다.

 **이 메시지가 표시되는 위치:** Power BI 전자 메일 또는 새로 고침 기록의 실패 상태. 
  
 **원인:** 경우에 따라 서식 파일 앱에 연결 된 사용자의 자격 증명이 다시 설정 되 고 서식 파일 앱의 연결 설정에서 업데이트 되지 않아 사용자가 새로 고침 실패 오류가 표시 되는 경우가 있습니다. 
  
 **이 오류를 해결 하려면** Power BI에서 Microsoft 365 사용 현황 분석 서식 파일 앱에 해당 하는 데이터 집합을 찾고 **새로 고침 예약** 및 관리자 자격 증명 제공을 선택 합니다. 
  
그래도 문제가 해결 되지 않으면 캐시를 지우고 서식 파일 앱을 다시 만듭니다.
  
  
