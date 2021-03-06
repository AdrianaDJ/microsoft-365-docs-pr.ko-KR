---
title: Microsoft Defender for Office 365의 SIEM 통합
f1.keywords:
- NOCSH
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
ms.date: 08/21/2020
ms.collection:
- M365-security-compliance
description: Office 365 활동 관리 API에서 조직의 SIEM 서버를 Microsoft Defender for Office 365 및 관련 위협 이벤트와 통합 합니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 6253ed0133bf53bdbeca71bb595a850e25441311
ms.sourcegitcommit: 4debeb8f0fce67f361676340fc390f1b283a3069
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49561708"
---
# <a name="siem-integration-with-microsoft-defender-for-office-365"></a>Microsoft Defender for Office 365의 SIEM 통합

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


조직에서 SIEM (보안 정보 및 이벤트 관리) 서버를 사용 하는 경우 Office 365 용 Microsoft Defender를 SIEM 서버와 통합할 수 있습니다. [Office 365 활동 관리 API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)를 사용 하 여이 통합을 설정할 수 있습니다.

SIEM 통합을 사용 하면 SIEM server reports에서 Microsoft Defender for Office 365에서 검색 된 맬웨어 또는 피싱 같은 정보를 볼 수 있습니다.

- 365 Office 365 용 Microsoft Defender와의 SIEM 통합에 대 한 예를 보려면 [기술 커뮤니티 블로그: Office 365 용 Defender와 O365 관리 API의 효율성 향상](https://techcommunity.microsoft.com/t5/microsoft-security-and/improve-the-effectiveness-of-your-soc-with-office-365-atp-and/ba-p/1525185)을 참조 하세요.

- Office 365 관리 Api에 대 한 자세한 내용은 [office 365 관리 api 개요](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)를 참조 하세요.

## <a name="how-siem-integration-works"></a>SIEM 통합 작동 방식

Office 365 활동 관리 API는 조직의 Microsoft 365 및 Azure Active Directory 활동 로그에서 사용자, 관리자, 시스템 및 정책 작업과 이벤트에 대 한 정보를 검색 합니다. 조직에 Microsoft Defender for Office 365 계획 1 또는 2 또는 Office 365 E5가 있는 경우 [Microsoft defender For office 365 schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema)를 사용할 수 있습니다.

최근에 [Microsoft Defender For Office 365 계획 2](office-365-atp.md#microsoft-defender-for-office-365-plan-1-and-plan-2) 의 자동화 된 조사 및 응답 기능의 이벤트가 Office 365 관리 활동 API에 추가 되었습니다. API에는 ID, 이름 및 상태와 같은 핵심 조사 세부 정보에 대 한 데이터를 포함 하는 것 외에 조사 작업과 엔터티에 대 한 높은 수준의 정보도 포함 되어 있습니다.

SIEM 서버 또는 기타 유사한 시스템은 검색 이벤트에 액세스 하기 위한 **감사의 일반적인** 작업을 폴링합니다. 자세한 내용은 [Office 365 관리 api 시작](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)하기를 참조 하세요.

## <a name="enum-auditlogrecordtype---type-edmint32"></a>Enum: AuditLogRecordType: Edm. i a i. Int32

### <a name="auditlogrecordtype"></a>AuditLogRecordType

다음 표에는 Office 365 이벤트 용 Microsoft Defender와 관련 된 **AuditLogRecordType** 의 값이 요약 되어 있습니다.

|값|멤버 이름|설명|
|---|---|---|
|28@@|ThreatIntelligence|Exchange Online Protection의 피싱 및 맬웨어 이벤트 및 Office 365 용 Microsoft Defender|
|41|ThreatIntelligenceUrl|안전한 링크 차단 및 Office 용 Microsoft Defender 365의 무시 이벤트 차단 이벤트가 있습니다.|
|47|ThreatIntelligenceAtpContent|SharePoint Online, 비즈니스용 OneDrive 및 Microsoft 팀의 파일에 대 한 피싱 및 맬웨어 이벤트 (Office 365 용 Microsoft Defender)|
|64|방송 조사|Microsoft Defender for Office 365 계획 2의 조사 세부 정보 및 관련 아티팩트와 같은 자동화 된 조사 및 응답 이벤트|
|

> [!IMPORTANT]
> Microsoft Defender for Office 365와 함께 SIEM 통합을 설정 하려면 전역 관리자 이거나 보안 & 준수 센터에 대 한 보안 관리자 역할이 할당 되어 있어야 합니다.<br/>Microsoft 365 환경에 대해 감사 로깅을 켜야 합니다. 이에 대 한 도움말을 보려면 [Turn 감사 로그 검색 켜기 또는 끄기를](../../compliance/turn-audit-log-search-on-or-off.md)참조 하세요.

## <a name="see-also"></a>참고 항목

[Office 365 위협 조사 및 응답](office-365-ti.md)

[Office 365의 자동화 된 조사 및 응답 (AIR)](automated-investigation-response-office.md)

