---
title: Microsoft 365의 고급 eDiscovery 솔루션 개요
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365solution-aed
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: 이 문서에서는 내부 및 외부 조사 도구인 Microsoft 365의 고급 eDiscovery에 대 한 개요를 제공 합니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 6225411bcd3051c19e22fcb205cc7dee92f99f82
ms.sourcegitcommit: ce46d1bd67091d4ed0e2b776dfed55e2d88cdbf4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49131031"
---
# <a name="overview-of-the-advanced-ediscovery-solution-in-microsoft-365"></a>Microsoft 365의 고급 eDiscovery 솔루션 개요

Microsoft 365의 고급 eDiscovery 솔루션은 Office 365의 기존 eDiscovery 및 분석 기능을 기반으로 작성 되었습니다. *Advanced eDiscovery* 라는이 새로운 솔루션은 조직의 내부 및 외부 조사에 응답 하는 콘텐츠를 보존, 수집, 검토, 분석 및 내보내기 위한 종단 간 워크플로를 제공 합니다. 또한 법률 팀에서 법적 보존 알림 워크플로 전체를 관리 하 여 사례와 관련 된 custodians와 통신할 수 있습니다. 

> [!NOTE]
> 고급 eDiscovery에는 Office 365 또는 Microsoft 365 E5 Enterprise 구독이 필요 합니다. 고급 eDiscovery 라이선스에 대 한 자세한 내용은 [보안 & 준수에 대 한 Microsoft 365 라이선스 지침](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#advanced-ediscovery)을 참조 하세요.

## <a name="alignment-with-edrm"></a>EDRM과 맞춤

기본 제공 되는 고급 eDiscovery 워크플로는 EDRM (전자식 Discovery Reference Model)에 의해 개요 된 eDiscovery 프로세스와 정렬 됩니다. 

![EDRM (전자 검색 참조 모델)](../media/EDRMv1.png)

(Edrm.net의 이미지 원본 관례입니다. 원본 이미지는 Creative Creative commons 특성 3.0이 아니라 Ported 라이선스를 통해 사용할 수 있습니다.

높은 수준에서 고급 eDiscovery는 EDRM 워크플로를 지 원하는 방법에 대해 설명 합니다.

- **확인과.** 조사에서 관심 있는 잠재적 사용자를 확인 한 후에는 조사와 관련 된 정보를 custodians ( *데이터 custodians* 라고도 함)로 고급 eDiscovery 사례에 추가할 수 있습니다. Custodians를 식별 하 고이를 사례에 추가한 후에는 연결 된 custodial 데이터를 쉽게 보존, 수집, 검토 및 분석할 수 있습니다.

- **보관.** 조사와 관련 된 데이터를 보존 하 고 보호 하기 위해 Advanced eDiscovery를 사용 하면 custodians와 연결 된 데이터 원본을 한 사례에 보관할 수 있습니다. Custodial이 아닌 데이터를 보존 (일반적으로 SharePoint 사이트 또는 공유 팀 채널과 같은 공유 그룹 리소스)에 배치할 수도 있습니다. 또한 Advanced eDiscovery에는 custodians에 법적 보존 알림을 전송 하 고 해당 승인을 추적할 수 있는 기본 제공 되는 통신 워크플로가 포함 되어 있습니다.

- **모음.** 조사와 관련 된 데이터 원본을 식별 하 여 선택적으로 유지 한 후에는 고급 eDiscovery의 기본 제공 검색 도구를 사용 하 여 custodial 데이터 원본 (해당 되는 경우)에서 사례와 관련 될 수 있는 라이브 데이터를 검색 하 고 수집할 수 있습니다.

- **처리.** 사례와 관련 된 모든 데이터를 수집한 후에는 추가 검토 및 분석을 위해 처리 해야 합니다. 고급 eDiscovery에서 수집 단계에서 식별 된 원본 위치 데이터는 사례 데이터의 정적 보기를 제공 하는 Azure 저장 위치 ( *검토 집합* 이라고 함)로 복사 됩니다.

- **검토.** 데이터를 검토 집합에 추가한 후에는 특정 문서를 보고 검토 집합 내의 추가 쿼리를 실행 하 여 데이터를 가장 관련성이 높은 문서로 축소할 수 있습니다. 또한 특정 문서에 주석을 달고 태그를 지정할 수 있습니다.

- **분석할.** Advanced eDiscovery는 검토 집합에서 관련성이 없는 데이터를 지능적으로 cull 하는 데 사용할 수 있는 강력한 통합 분석 도구 집합을 제공 하며,이를 통해 프로덕션 환경에 대 한 관련 데이터의 양을 효율적으로 줄임으로써 법적 검토 비용을 절감할 수 있습니다.

- **프로덕션** 및 **프레젠테이션** 준비가 완료 되 면 검토 집합에서 법률 검토를 위해 문서를 내보낼 수 있습니다. 타사 검토 응용 프로그램으로 가져올 수 있도록 문서를 EDRM으로 지정한 형식으로 내보낼 수 있습니다.

## <a name="advanced-ediscovery-architecture"></a>고급 eDiscovery 아키텍처

다음은 단일 지리적 환경 및 다중 위치 환경에서 종단간 워크플로를 보여 주는 고급 eDiscovery 아키텍처 다이어그램입니다. 종단 간 데이터 흐름을 EDRM과 맞춥니다.

[![모델 포스터: Microsoft 365의 고급 eDiscovery 아키텍처](../media/solutions-architecture-center/ediscovery-poster-thumb.png)](../media/solutions-architecture-center/m365-advanced-ediscovery-architecture.png)

[이미지로 보기](../media/solutions-architecture-center/m365-advanced-ediscovery-architecture.png)

[PDF 파일로 다운로드](https://download.microsoft.com/download/d/1/c/d1ce536d-9bcf-4d31-b75b-fcf0dc560665/m365-advanced-ediscovery-architecture.pdf)

[Visio 파일로 다운로드](https://download.microsoft.com/download/d/1/c/d1ce536d-9bcf-4d31-b75b-fcf0dc560665/m365-advanced-ediscovery-architecture.vsdx)

Advanced eDiscovery의 종단 간 워크플로에 대 한 자세한 내용은이 [Microsoft 메커니즘 비디오](https://go.microsoft.com/fwlink/?linkid=2066133)를 참조 하세요.

다음 섹션에서는 고급 eDiscovery에서 기본 제공 워크플로의 각 단계에 대해 설명 합니다. 다음 스크린샷에서는 *2020.11.03* 이라는 사례에 대 한 **개요** 탭을 보여 줍니다.

![기본 제공 되는 고급 eDiscovery 워크플로의 탭](../media/AeD-Case-Screenshot1.png)

## <a name="managing-custodians-and-non-custodial-data-sources"></a>Custodians 및 비 custodial 데이터 원본 관리

**데이터 원본** 탭을 사용 하 여 custodian와 연결 되지 않을 수도 있는 사용자를 사례 및 기타 데이터 원본으로 식별 한 사람을 추가 하 고 관리 합니다. Custodians 또는 비 custodial 데이터 원본을 추가 하는 경우 custodian 및 비 custodial 데이터 원본에 법적 보존 기능을 배치 하 고, custodians, 검색 custodian 및 비-custodial 데이터 원본을 사용 하 여 사례와 관련 된 콘텐츠를 수집 하는 등의 작업을 빠르게 수행할 수 있습니다. 사례가 진행 됨에 따라 새 custodians 또는 비 custodial 데이터 원본을 추가 하거나 사례에서 릴리스 하기가 쉽습니다. 자세한 내용은 [Advanced eDiscovery에서 custodians 사용](managing-custodians.md)을 참조 하십시오.

## <a name="managing-legal-hold-notifications"></a>법적 보존 알림 관리

**통신** 탭을 사용 하 여 사례에서 custodians와 통신 하는 프로세스를 관리 합니다. 법적 고 지 사항에서는 사례와 관련 된 모든 콘텐츠를 보존 하도록 custodians에 지시 합니다. 법률 팀은 custodians에서 수신, 읽기 및 승인 된 알림을 추적 해야 합니다. 고급 eDiscovery의 통신 워크플로를 사용 하면 custodians에서 보류 알림을 승인 하지 못할 경우 초기 알림, 미리 알림, 릴리스 알림 및 에스컬레이션을 만들고 보낼 수 있습니다. 자세한 내용은 [Advanced eDiscovery에서 통신에](managing-custodian-communications.md)대 한 작업을 참조 하세요.

## <a name="managing-content-preservation"></a>콘텐츠 보존 관리

Custodian를 사례에 추가할 때 custodial 데이터를 보유할 수 있습니다. **보류** 탭을 사용 하 여 custodians을 추가 하 고 사례와 관련 된 다른 법적 보유를 관리 하는 경우 생성 되는 보류를 관리 합니다. 예를 들어 custodial이 아닌 데이터 원본을 확인 하 고 보류할 수 있습니다. 또한 사례에서 보류를 편집 하 고 쿼리 기반 유지로 설정 하 여 쿼리와 일치 하는 콘텐츠만 보존할 수 있습니다. 예를 들어 날짜 범위를 보류에 추가 하 여 특정 날짜 이내에 만들어진 콘텐츠만 유지 되도록 할 수 있습니다. 보류 중인 콘텐츠에 대 한 통계를 가져오거나 사례에 더 이상 관련 되지 않은 보류를 제거 하거나 삭제할 수도 있습니다. 자세한 내용은 [Advanced eDiscovery에서 보류 관리](managing-holds.md)를 참조 하세요.

## <a name="indexing-custodian-data"></a>Custodian 데이터 인덱싱

Custodian 및 해당 하는 custodial 데이터 원본을 사례에 추가할 때 custodian 데이터 원본의 모든 부분적으로 인덱싱된 항목은 *고급 인덱싱* 프로세스에 의해 reindexed 됩니다. 이를 통해 이미지, 지원 되지 않는 파일 형식 및 기타 잠재적으로 인덱싱되지 않은 콘텐츠와 같은 custodial 콘텐츠가 검색을 실행 하 여 사례에 대 한 데이터를 수집할 때 완벽 하 게 검색할 수 있습니다. **처리** 탭을 사용 하 여 *오류 수정 관리* 라는 프로세스를 사용 하 여 고급 인덱싱의 상태를 모니터링 하 고 처리 오류를 해결 합니다. 자세한 내용은 [Advanced eDiscovery의 처리 오류 수정을](processing-data-for-case.md)참조 하세요.

## <a name="collecting-case-data"></a>사례 데이터 수집하기

**검색 탭을** 사용 하 여 검색을 만들어 해당 사례와 관련 된 콘텐츠에 대 한 원본 위치 custodial 및 비 custodial 데이터 원본을 검색 합니다. 쿼리 기반 검색 (키워드 및 조건 사용)을 만들고 실행 하 여 사례와 관련 된 전자 메일 메시지 및 문서 집합을 식별 하 고 eDiscovery 워크플로의 이후 단계에서 더 자세히 검토 하 고 분석할 수 있습니다. 사례와 연결 된 검색을 하나 이상 만들 수 있습니다. 또한 검색 도구를 사용 하 여 예제 문서를 미리 보고 검색 통계를 확인 하 여 검색 결과를 구체화 하 고 개선 하는 데 도움이 될 수 있습니다. 사례와 관련 된 모든 데이터를 검색 하 고 수집한 후 추가 검토, 분석 및 culling에 대 한 검토 집합에 검색 결과를 추가할 수 있습니다. 자세한 내용은 [Advanced eDiscovery에서 사례 데이터 수집](collecting-data-for-ediscovery.md)을 참조 하십시오.

## <a name="reviewing-and-analyzing-case-data"></a>사례 데이터 검토 및 분석

**검토 집합** 탭을 사용 하 여 라이브 시스템에서 수집한 콘텐츠를 검토 및 분석 하 고 검토 집합에 추가 합니다. *검토 집합* 은 해당 데이터의 정적 컬렉션 (즉, 데이터의 오프 라인 복사본)은 eDiscovery 워크플로의 이전 단계에서 수집한 custodial 데이터 (해당 하는 경우에는 custodial 데이터)를 모아 놓은 것입니다. 검토 집합에 검색 결과를 추가 하는 경우 프로세스를 트리거되어 컨테이너에서 파일을 추출 하 고 메타 데이터를 추출 하 고 텍스트를 추출 합니다. 이 프로세스가 완료 되 면 시스템은 custodians에서 수집한 모든 데이터의 새 인덱스를 작성 하 고이를 검토 집합에 추가 합니다. 데이터를 검토 집합에 추가한 후 쿼리를 더 많이 실행 하 여 사례 데이터의 범위를 좁히거나, 데이터를 텍스트로 보거나 네이티브 파일 형식으로 표시 하 고, 검토 집합에서 문서에 주석을 달고, 교정 하 고, 태그를 지정할 수 있습니다. 문서 복제, 전자 메일 스레딩 및 테마 식별과 같은 고급 분석을 수행할 수도 있습니다. 사례와 관련 된 데이터에만 culled 후에는 문서를 직접 다운로드 하거나 파일 메타 데이터, 주석 및 모든 태그와 함께 내보낼 수 있습니다. 자세한 내용은 다음을 참조하시기 바랍니다.

- [검토 집합에서 문서 보기](view-documents-in-review-set.md)

- [검토 집합에서 데이터 쿼리](review-set-search.md)

- [검토 집합에서 문서 태그 지정](tagging-documents.md)

- [검토 집합의 데이터 분석](analyzing-data-in-review-set.md)

## <a name="exporting-data-for-review-and-presentation"></a>검토 및 프레젠테이션으로 데이터 내보내기

검토 집합에서 데이터를 내보낸 후에는 **내보내기 탭을 사용 하 여 export** 작업을 관리 하 고 검토 집합에서 데이터를 다운로드 합니다. 검토 집합을 내보낼 때 데이터는 Microsoft에서 제공한 Azure 저장소 위치 또는 조직에서 관리 하는 Azure 저장소 위치에 업로드 됩니다. Azure에 업로드 되 면 로컬 컴퓨터로 다운로드할 수 있습니다. **내보내기** 탭에서 내보낸 데이터를 다운로드 하는 데 필요한 저장소 액세스 키를 가져올 수 있습니다. 자세한 내용은 [Advanced eDiscovery에서 케이스 데이터 내보내기를](exporting-data-ediscover20.md)참조 하십시오.

## <a name="managing-jobs"></a>작업 관리

**작업** 탭을 사용 하 여 시작한 사례 관련 작업에 대 한 장기 실행 프로세스를 모니터링 합니다. 작업의 예로는 사례 데이터의 다시 인덱스, 검색 및 내보내기와 관련 된 내용이 있습니다. 예를 들어 여러 데이터 원본을 포함 **하는 검색 탭에** 검색할 경우 **작업** 탭에이 검색 프로세스의 상태가 표시 됩니다. 자세한 내용은 [Advanced eDiscovery에서 작업 관리](managing-jobs-ediscovery20.md)를 참조 하세요.

## <a name="configuring-case-settings"></a>사례 설정 구성

**설정** 탭을 사용 하 여 대/소문자 전체의 설정을 구성 합니다. 여기에는 사례에 구성원 추가, 사례 닫기 또는 삭제, 검색 및 분석 설정 구성 등이 포함 됩니다.
