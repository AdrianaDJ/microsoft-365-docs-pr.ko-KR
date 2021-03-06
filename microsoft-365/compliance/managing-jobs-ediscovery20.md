---
title: Advanced eDiscovery에서 작업 관리
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 고급 eDiscovery 작업은 다양 한 고급 eDiscovery 작업을 수행 하는 데 관련 된 장기 실행 프로세스의 상태를 추적 하는 데 도움이 됩니다.
ms.openlocfilehash: d41ac3572c462b85ff8f0bac0cc7205a5c012ce9
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285172"
---
# <a name="manage-jobs-in-advanced-ediscovery"></a>Advanced eDiscovery에서 작업 관리

다음은 Advanced eDiscovery에서 사례의 **작업** 탭에 대해 추적 되는 작업 (일반적으로 장기 실행 프로세스) 목록입니다. 이러한 작업은 사례 사용 및 관리 시 사용자 작업에 의해 트리거됩니다.

| 작업 유형           | 설명     |
| :----------------- | :----------     |
|검토 집합에 데이터 추가 | 사용자가 검색 결과를 검토 집합에 추가 합니다. 이 작업은 다음과 같은 두 개의 하위 작업으로 구성 됩니다. </br>• **GatheringItems** -검색 쿼리와 일치 하는 항목 목록 (및 해당 사용자가 있는 Microsoft 365 데이터 원본)이 생성 됩니다. </br>• **& Indexing** 수집-검색 쿼리와 일치 하는 항목은 azure 저장 위치 ( *수집 이라는 프로세스*)로 복사 된 다음 azure 저장소 위치에 있는 해당 항목은 reindexed 됩니다. 이 새 인덱스는 데이터 집합의 항목을 쿼리하고 분석할 때 사용 됩니다. </br></br>자세한 내용은 [검토 집합에 검색 결과 추가](add-data-to-review-set.md)를 참조 하세요. |
|다른 검토 집합에 데이터 추가 | 한 검토 집합의 문서를 동일한 대/소문자로 다른 검토 집합으로 추가 합니다. 자세한 내용은 [다른 검토 집합에서 검토 집합에 데이터 추가](add-data-to-review-set-from-another-review-set.md)를 참조 하세요.|
|검토 집합에 Microsoft 제품이 아닌 365 데이터 추가 | 사용자가 타사 365 데이터를 검토 집합으로 업로드 합니다. 이 프로세스 중에도 데이터가 인덱싱됩니다. 예를 들어 온-프레미스 파일 서버 또는 클라이언트 컴퓨터의 파일은 검토 집합에 업로드 됩니다. 자세한 내용은 타사 [365 데이터를 검토 집합으로 로드](load-non-office365-data.md)를 참조 하세요.| 
|재구성 된 데이터를 검토 집합에 추가 | 처리 오류가 발생 한 데이터는 재구성 되 고 검토 집합으로 다시 로드 됩니다. 자세한 내용은 다음을 참조하세요.</br>• [데이터 처리 시 오류 수정](error-remediation-when-processing-data-in-advanced-ediscovery.md)</br>• [단일 항목 오류 수정](single-item-error-remediation.md)| 
|부하 집합 비교 | 사용자가 검토 집합에서 서로 다른 부하 집합 간의 차이점을 살펴봅니다. 부하 집합은 검토 집합에 데이터를 추가 하는 인스턴스입니다. 예를 들어 서로 다른 두 검색의 결과를 동일한 검토 집합에 추가 하는 경우 각각은 로드 집합을 나타냅니다. 자세한 내용은 [부하 집합 관리](manage-load-sets.md)를 참조 하세요. |
|대화 재구성|사용자가 검색 결과를 대화 검토 집합에 추가 하면 Microsoft 팀과 같은 서비스의 인스턴트 메시지 대화 ( *스레드된 대화*라고도 함)가 PDF 파일에 다시 만들어집니다. 이 작업은 사용자가 검토 집합에서 **대화 pdf를 만드는 동작 >** 클릭 하는 경우에도 트리거됩니다. 자세한 내용은 [Advanced eDiscovery에서 대화 검토](conversation-review-sets.md)를 참조 하세요.
|Redacted 문서를 PDF로 변환|사용자가 문서를 검토 집합으로 annotates 한 부분을 redacts 후에는 redacted 문서를 PDF 파일로 변환 하도록 선택할 수 있습니다. 이렇게 하면 프레젠테이션을 위해 문서를 내보낼 때 redacted 부분이 표시 되지 않습니다. 자세한 내용은 [문서 보기의 검토 집합](annotating-and-redacting-documents.md)을 참조 하십시오. |
|검색 결과 예측 | 사용자가 새 검색을 만들고 실행 한 후, 즉 검색 도구에서 검색 쿼리와 일치 하는 항목에 대 한 인덱스를 검색 하 고 검색을 통해 모든 항목의 수와 총 크기를 포함 하는 예상 값과 검색할 데이터 원본의 수를 준비 합니다.  자세한 내용은 [사례에 대 한 데이터 수집](collecting-data-for-ediscovery.md)을 참조 하십시오. | 
|내보내기를 위해 데이터 준비 | 사용자가 검토 집합에서 문서를 내보냅니다. 내보내기 프로세스가 완료 되 면 내보낸 데이터를 로컬 컴퓨터에 다운로드할 수 있습니다. 자세한 내용은 [수출 사례 데이터](exporting-data-ediscover20.md)를 참조 하십시오. | 
|오류 해결 준비 |사용자가 파일을 선택 하 고 사례 **처리** 탭의 오류 보기에 새 오류 수정을 만드는 경우 프로세스의 첫 번째 단계는 처리 오류가 발생 한 파일을 Microsoft 클라우드의 Azure Storage 위치에 업로드 하는 것입니다. 이 작업은 업로드 프로세스의 진행 상태를 추적 합니다. 오류 수정 워크플로 작업에 대 한 자세한 내용은 [데이터를 처리할 때 오류 수정을](error-remediation.md)참조 하십시오. | 
|검색 미리 보기 준비 | 사용자가 새 검색을 만들고 실행 한 후에 검색 도구에서 미리 볼 수 있도록 검색 쿼리와 일치 하는 항목의 예제 하위 집합을 준비 합니다. 검색 결과 미리 보기는 검색 효율성을 결정 하는 데 도움이 됩니다.  자세한 내용은 [사례에 대 한 데이터 수집](collecting-data-for-ediscovery.md#view-search-results-and-statistics)을 참조 하십시오. | 
|Custodian 데이터 다시 인덱싱 | Custodian를 사례에 추가 하면 custodian에서 선택한 데이터 원본의 모든 부분 인덱싱된 항목이 *고급 인덱싱*프로세스에 의해 reindexed 됩니다. 또한이 작업은 서비스 케이스의 **처리** 탭에서 **인덱스 업데이트** 를 클릭 하 고 custodian 속성 플라이 아웃 페이지에서 특정 custodian에 대 한 인덱스를 업데이트할 때 트리거됩니다. 자세한 내용은 [고급 인덱싱 custodian 데이터](indexing-custodian-data.md)를 참조 하세요.
|분석 실행 | 사용자가 중복 검색, 전자 메일 스레딩 분석 및 테마 분석과 같은 고급 eDiscovery 분석 도구를 실행 하 여 검토 집합의 데이터를 분석 합니다. 자세한 내용은 [분석 데이터를 검토 집합에서](analyzing-data-in-review-set.md)참조 하십시오. | 
|문서 태그 지정 | 이 작업은 검토 집합의 문서를 검토할 때 **태그 지정 패널** 에서 **태그 지정 작업 시작** 을 클릭 하면 트리거됩니다. 사용자는 검토 집합에서 문서에 태그를 지정한 다음 문서 보기 패널에서이를 일괄 선택 하 여이 작업을 시작할 수 있습니다. 자세한 내용은 [검토 집합의 태그 문서](tagging-documents.md)를 참조 하세요. | 
|||

## <a name="job-status"></a>작업 상태

다음 표에서는 작업에 대 한 다양 한 상태 상태에 대해 설명 합니다.

| 상태           | 설명     |
| :----------------- | :----------     |
| 양식의 | 새 작업을 만들었습니다.  작업이 제출 된 날짜 및 시간은 **작업** 탭의 **작성** 된 열에 표시 됩니다. |
| 전송 실패 | 작업을 전송 하지 못했습니다.  작업을 트리거한 작업을 다시 실행 해 보십시오. |
| 진행 중 | 작업이 진행 중 이므로 **작업 탭에서** 작업의 진행 상태를 모니터링할 수 있습니다. |
| 성공 | 작업이 성공적으로 완료 되었습니다. 작업이 완료 된 날짜 및 시간이 **작업** 탭의 **완료 됨** 열에 표시 됩니다. |
| 부분적으로 성공한 | 작업이 부분적으로 완료 되었습니다. 이 상태는 일반적으로 작업에서 일부 custodian 데이터 원본에 있는 부분적으로 인덱싱된 데이터 ( *인덱싱되지 않은 데이터*라고도 함)를 찾지 못한 경우 반환 됩니다.  |
| Failed | 작업이 실패 했습니다.  작업을 트리거한 작업을 다시 실행 해 보십시오. 작업을 두 번 실패 하면 Microsoft 지원 서비스에 문의 하 여 작업에 대 한 지원 정보를 제공 하는 것이 좋습니다. |
|||
