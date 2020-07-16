---
title: GDPR용 Windows용 DPIA 데이터 프로세서 서비스
description: Windows용 Microsoft 데이터 프로세서 서비스를 사용할 때 DPIA(데이터 보호 영향 평가)가 필요한지 여부를 확인하는 정보를 찾습니다.
keywords: DPIA, Microsoft 365, Microsoft 365 Education, Microsoft 365 설명서, GDPR
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: Microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: daniha
author: DaniHalfin
manager: dansimp
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
ms.openlocfilehash: c594bbca6383874346719a477d3f86f3dac99409
ms.sourcegitcommit: 3ddcf08e8deec087df1fe524147313f1cb12a26d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2020
ms.locfileid: "45023624"
---
# <a name="data-protection-impact-assessments-guidance-for-data-controllers-using-microsoft-data-processor-service-for-windows"></a>데이터 보호 영향 평가는 다음과 같습니다. Windows용 Microsoft 데이터 프로세서 서비스를 사용하는 데이터 컨트롤러에 대한 지침입니다.

>[!NOTE]
>이 항목은 Windows 미리 보기 프로그램용 데이터 프로세서 서비스 참여자를 대상으로 하며 특정 사용 약관을 수락해야 합니다. 프로그램에 대해 자세히 알아보고 사용 조건에 동의하려면 [https://aka.ms/dpswpublicpreview](https://aka.ms/dpswpublicpreview)을(를) 참조하시기 바랍니다.

GDPR(General Data Protection Regulation)에 따르면 데이터 컨트롤러는 "자연인의 권리와 자유에 높은 위험을 초래하는" 처리 작업을 위한 DPIA(데이터 보호 영향 평가)를 준비해야 합니다. Windows용 데이터 프로세서 서비스 자체에는 데이터 컨트롤러를 사용하여 DPIA를 생성해야 하는 고유한 기능이 없습니다. 대신 DPIA가 필요한지 여부는 데이터 컨트롤러가 Windows용 데이터 프로세서 서비스를 배포, 구성 및 사용하는 방법에 대한 세부 정보와 컨텍스트에 따라 달라집니다. 

이 문서의 목적은 데이터 컨트롤러에 Windows용 데이터 프로세서 서비스에 대한 정보를 제공함으로써 DPIA가 필요한지 여부 및 필요한 경우 포함할 세부 정보를 결정하는 데 도움이 되는 정보를 제공하기 위한 것입니다.

>[!Note]
>Microsoft는이 문서에 법적 자문을 제공하지 않습니다. 이 문서는 정보 제공의 목적으로만 제공됩니다. 고객은 개인 정보 보호 담당자 및 법률 고문과 협력하여 Windows용 데이터 프로세서 서비스 또는 기타 Microsoft 온라인 서비스용 데이터 프로세서 서비스 사용과 관련된 모든 DPIA의 필요성과 내용을 파악해야 합니다.

## <a name="part-1--determining-whether-a-dpia-is-needed"></a>1부 – DPIA가 필요한지 여부를 판단

GDPR 제35조에는 데이터 컨트롤러가 DPIA(Data Protection Impact Assessment) "특히 새로운 기술을 이용한 처리 유형을 생성해야 하며, 처리의 성격, 범위, 맥락 및 목적을 고려한다면 자연인의 권리와 자유에 대한 위험성이 높아지기 쉽습니다." 또한 다음과 같은 높은 위험을 나타내는 특정 요인을 자세히 설명합니다. DPIA가 필요한지 여부를 판단할 때 데이터 컨트롤러는 컨트롤러의 특정 구현 및 Windows용 데이터 프로세서 서비스 사용에 비추어 이러한 요인과 기타 관련 요인을 고려해야 합니다.

## <a name="table-1--data-processor-service-for-windows-dpia-risk-factors"></a>표 1 – Windows DPIA 위험 요인에 대한 데이터 프로세서 서비스 

|||
|:----|:----|
|**고위험 요소**|**Windows용 데이터 프로세서 서비스에 대한 관련 정보**|
| 프로파일링을 포함한 자동화된 처리의 기반이 되고 자연인에 관한 법적 영향을 행사하거나 유사하게 자연인에게 중대한 영향을 주는 의사 결정의 기반이 되는 자연인과 관련된 개인 측면의 체계적이고 광범위한 평가. |Windows용 데이터 프로세서 서비스는 특정 데이터 자동 처리를 수행할 수 있는 기능을 제공하지 않습니다.<br><br> 그러나 다른 서비스에서는 Windows용 데이터 프로세서 서비스를 데이터 소스로 사용하기 때문에 데이터 컨트롤러는 이러한 서비스를 이러한 처리에 사용하도록 구성할 수 있습니다. 컨트롤러는 Windows용 데이터 프로세서 서비스에 연결된 서비스의 사용을 기준으로 이러한 결정을 내려야 합니다.|   
| 특정 범주의 대규모 데이터(인종 또는 민족 태생, 정치적 견해, 종교적 또는 철학적 신념, 노동 조합 회원 및 유전자 데이터, 자연인의 고유한 식별을 목적으로 하는 생체 데이터, 건강 또는 자연인의 성생활이나 성적 취향에 관한 데이터의 처리) 처리 또는 범죄 유죄 판결 및 범죄와 관련된 개인 데이터 처리. | Windows용 데이터 프로세서 서비스는 특별한 범주의 개인 데이터를 처리하도록 특별히 설계되지 않았으며 Windows용 데이터 프로세서 서비스를 사용해도 컨트롤러의 처리 고유의 위험이 증가하지는 않습니다.<br><br> 그러나 데이터 컨트롤러는 Windows용 데이터 프로세서 서비스에 연결된 서비스를 사용하여 열거된 특수 범주의 데이터를 처리할 수 있습니다. Windows용 데이터 프로세서 서비스를 데이터 소스로 사용하는 서비스는 고객이 개인 데이터의 특수 범주를 포함한 모든 유형의 데이터를 추적하거나 다른 방식으로 처리할 수 있도록 지원합니다. 그러나 데이터 프로세서는 Microsoft가 이러한 사용을 제어할 수 없으며 이러한 사용에 대한 통찰력도 거의 또는 전혀 없습니다. 데이터 컨트롤러는 데이터 컨트롤러의 데이터를 적절하게 사용해야 합니다. |

## <a name="part-2--contents-of-a-dpia"></a>2부 - DPIA의 내용 

Article 35(7) mandates that a Data Protection Impact Assessment specify the purposes of processing and a systematic description of the envisioned processing. A systematic description of a comprehensive DPIA might include factors such as the types of data processed, how long data is retained, where the data is located and transferred, and what third parties may have access to the data. In addition, the DPIA must include: 

목적과 관련한 처리 작업의 필요성 및 비례의 원칙 평가; 

자연인의 권리와 자유에 대한 위험 평가; 

위험을 해결하기 위한 세이프가드, 보안 조치 등의 계획된 조치, 개인 데이터의 보호를 보장하고 데이터 주체 및 기타 관련자의 권리와 합법적 이익을 고려하여 이 규정을 준수함을 입증하기 위한 메커니즘. 

아래 표에는 이러한 각 요소와 관련된 Windows용 데이터 프로세서 서비스에 대한 정보가 나와 있습니다. 파트 1에서와 같이 데이터 컨트롤러는 컨트롤러의 특정 구현 및 Windows용 데이터 프로세서 서비스 사용의 맥락에서 다른 관련 요소와 함께 아래에 제공된 세부 정보를 고려해야 합니다. 

## <a name="table-2--data-processor-service-for-windows-dpia-elements"></a>표 2 – Windows DPIA 요소를 위한 데이터 프로세서 서비스입니다. 

||||
|:---|:---|:--|
|**DPIA의 요소**|**Windows용 데이터 프로세서 서비스에 대한 관련 정보**| |
| 처리 목적 | Windows용 데이터 프로세서 서비스를 사용하여 진단 데이터를 처리하는 목적은 진단 데이터를 구현, 구성 및 사용하는 컨트롤러에 의해 결정됩니다. <br><br> [OST(온라인 서비스 약관)](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46)에서 지정한 대로 Microsoft는 데이터 프로세서로 고객 데이터를 처리하여 고객인 데이터 컨트롤러에게 요청된 서비스를 제공합니다. Microsoft는 광고 또는 유사한 상업적 목적으로 고객 데이터 또는 파생된 정보를 사용하지 않습니다. |
| 처리된 개인 데이터의 범주 | **고객 데이터** - 모든 텍스트, 사운드, 비디오 또는 이미지 파일 및 소프트웨어를 포함한 모든 데이터와 엔터프라이즈 서비스를 사용하여 고객이 또는 대신하여 Microsoft에 제공합니다. 고객 데이터에는 최종 사용자의 식별 가능한 정보(예: Azure Active Directory의 사용자 이름 및 연락처 정보 또는 Windows 진단 데이터를 통한 장치 정보)가 포함됩니다. <br><br> **시스템 생성 데이터** - Microsoft가 사용자에게 엔터프라이즈 서비스를 제공하는 데 도움이 되는 Microsoft에서 생성한 데이터입니다. 시스템에서 생성된 데이터에는 시스템에서 생성된 고유 식별자와 같이 주로 가명화된 데이터가 포함되며, 이 데이터는 개별 사용자를 식별할 수는 없지만 사용자에게 엔터프라이즈 서비스를 제공하는 데 사용됩니다. 시스템에서 생성된 데이터에는 사용자 이름과 같은 최종 사용자에 대한 식별 가능한 정보도 포함될 수 있습니다. <br><br> **지원 데이터** - 온라인 서비스에 대한 기술 지원을 얻기 위해 Microsoft와의 계약을 통해 고객이 Microsoft 또는 고객을 대신하여 Microsoft에서 제공한 데이터(또는 고객이 Microsoft가 온라인 서비스에서 얻도록 허가한 데이터)입니다. <br><br> Windows용 데이터 프로세서 서비스에서 처리한 데이터에 대한 자세한 내용은 [온라인 서비스 약관](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) 및 [Microsoft 신뢰 센터](https://www.microsoft.com/trustcenter)를 참조하시기 바랍니다. |
| 데이터 보존 | Microsoft는 고객이 온라인 서비스를 사용할 수있는 기간 동안 그리고 모든 고객 데이터가 고객에 의해 검색되거나 OST의 조건에 따라 삭제될 때까지 고객 데이터를 보유 및 처리합니다. 고객은 가입 기간 동안 항상 Windows용 데이터 프로세서 서비스에 저장된 고객 데이터를 내보낼 수 있습니다. 고객은 [GDPR 설명서에 대한 데이터 프로세서 서비스](https://servicetrust.microsoft.com/ViewPage/GDPRDSR)에 설명된 기능을 사용하여 데이터 제목 요청에 따라 개인 데이터를 삭제할 수 있습니다.
| 개인 데이터의 위치 및 전송 | Windows 고객 데이터를 위한 데이터 프로세서 서비스는 미국의 Microsoft 데이터 센터에 상주합니다. |
| 타사와 데이터 공유 | Microsoft shares data with third parties acting as our subprocessors (i.e., subcontractors which process personal data) to support functions such as customer and technical support, service maintenance, and other operations. Any subcontractors to which Microsoft transfers Customer Data or Support Data will have entered into written agreements with Microsoft that are no less protective than the Data Protection Terms of the [Online Services Terms](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46). All third-party subcontractors with which Customer Data or Support Data is shared are included in the [Lists of subcontractors](https://www.microsoft.com/trustcenter/privacy/who-can-access-your-data-and-on-what-terms#subcontractors) (see “We limit access by subprocessors”). <br><br> Information regarding Microsoft’s response to law enforcement and third party requests for Customer Data and Support Data is located in the Online Services Terms. Unless Microsoft is legally prohibited from doing so, Microsoft will attempt to redirect the law enforcement agency or third party directly to the Customer. |
| 데이터 주체 권리 | 프로세서로 작동할 때 Microsoft는 GDPR에 따라 권한을 행사할 때 데이터 주체의 개인 데이터와 데이터 주체의 요청을 수행할 수 있는 기능을 고객(컨트롤러)에게 제공합니다. Microsoft는 제품의 기능 및 데이터 프로세서로서의 역할과 일치하는 방식으로 이를 수행합니다.  Microsoft가 고객의 데이터 주체로부터 GDPR에 따라 하나 이상의 권한을 행사하라는 요청을 받으면 해당 요청이 데이터 컨트롤러로 리디렉션됩니다. <br><br> Windows용 [데이터 프로세서 서비스(Windows 데이터 주체 요청 GDPR 설명서](https://servicetrust.microsoft.com/ViewPage/GDPRDSR))는 Windows용 데이터 프로세서 서비스의 기능을 사용하여 데이터 주체 권한을 지원하는 방법에 대한 설명을 제공합니다. |
| 목적과 관련한 처리 작업의 필요성 및 비례의 원칙 평가 | 이러한 평가는 데이터 컨트롤러의 요구와 처리 목적에 따라 달라집니다. <br><br> With regard to the processing carried out by Microsoft, such processing is necessary and proportional for the purpose of providing the services to the data controller. Microsoft makes this commitment in the OST. |
| 데이터 주체의 권리와 자유에 대한 위험 평가 | Windows용 데이터 프로세서 서비스 사용으로 인한 데이터 주체의 권한과 자유에 대한 주요 위험은 컨트롤러가 Windows용 데이터 프로세서 서비스를 구현, 구성 및 사용하는 방법과 맥락에 따라 결정됩니다. <br><br> However, as with any service, personal data held in the service may be at risk of unauthorized access or inadvertent disclosure. Measures Microsoft takes to address such risks are discussed in the OST, as further detailed below. |
| 위험을 해결하기 위한 세이프가드, 보안 조치 등의 계획된 조치, 개인 데이터의 보호를 보장하고 데이터 주체 및 기타 관련자의 권리와 합법적 이익을 고려하여 GDPR을 준수함을 입증하기 위한 메커니즘 | Microsoft is committed to helping protect the security of Customer Data. The security measures Microsoft takes are described in detail in the OST. <br><br> Microsoft는 처리하는 개인 데이터를 보호하기 위해 합리적이고 적절한 기술 및 조직적 조치를 취합니다. 이러한 조치에는 내부 개인 정보 보호 정책 및 관행, 계약 약정, 국제 및 지역 표준 인증이 포함되며 이에 국한되지는 않습니다. 자세한 내용은 [신뢰 센터의 개인 정보 표준 페이지](https://www.microsoft.com/trustcenter/privacy/we-set-and-adhere-to-stringent-standards)에서 확인할 수 있습니다. <br><br> Microsoft provides significant, transparent customer facing security and privacy materials to help explain Microsoft’s use and processing of personal data. Customers are encouraged to contact Microsoft with questions. <br><br> 또한 Microsoft는 데이터 보호 영향 평가 및 기록 유지를 포함하지만 국한되지 않는 데이터 프로세스에 적용되는 모든 기타 GDPR 의무를 준수합니다.| 