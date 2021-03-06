---
title: 데이터 조사의 문서 메타 데이터 필드 (미리 보기)
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
ms.assetid: ''
description: 데이터 조사 (미리 보기)에 증명 정보 집합의 문서에 대 한 메타 데이터 필드가 나열 된 표를 봅니다.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: f365ca6381fee2713f6e1c8e68eb9b1cd8e1fb88
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285394"
---
# <a name="document-metadata-fields-in-data-investigations-preview"></a>데이터 조사의 문서 메타 데이터 필드 (미리 보기)

다음 표에서는 데이터 조사 (미리 보기)의 조사에 따라 증명 정보 집합의 문서에 대 한 메타 데이터 필드를 보여 줍니다. 이 테이블은 증명 정보 집합에서 쿼리를 실행할 때 필드를 검색할 수 있는지 여부, 증명 정보 집합에서 선택한 문서의 파일 메타 데이터를 볼 때 필드가 표시 되는지 여부 및 문서를 내보낼 때 필드를 포함할지 여부를 나타냅니다. 

> [!NOTE]
> 검색 **가능한 증명 정보 집합** 열에서 괄호 안의 값은 검색할 수 있는 속성의 이름입니다. **파일 메타 데이터에** 표시할 수 있는 열에서 괄호 안의 값은 파일 메타 데이터를 볼 때 표시 되는 속성의 이름입니다.

|**필드 이름** </br>|**증명 정보 집합에서 검색 가능** |**파일 메타 데이터에서 보기 가능** |**내보내려면** |
|:-------------------------- |:---------------------------------------- |:------------------------|:------------------|
|사례 태그                  | 예 (태그)                                      |                         | 예         |
|준수 레이블          |                                                 |                         | 예         |
|컴파운드 경로              |                                                 |                         | 예         |
|컨테이너 ID               |                                                 |                         | 예         |
|대화 인덱스         |                                                 |                         | 예         |
|Custodian                  | 예 (custodian)                                 |   예 (Custodian)       | 예         |
|데이터 원본                | 예 (원본)                                    |   예 (작업)          | 예         |
|날짜                       | 예 (날짜)                                      |   예 (날짜 UTC)        | 예         |
|Deduped 컴파운드 경로      |                                                 |                         | 예         |
|Deduped custodians         |                                                 |                         | 예         |
|Deduped 파일 Id           |                                                 |                         | 예         |
|문서 작성자                | 예 (만든이) *                                   |    예 (만든이)         | 예         |
|문서 주석               | 예 (메모)                                  |                         | 예         |
|문서 회사                |                                                 |                         | 예         |
|만든 문서 날짜           | 예 (createdTime) *                              |    예 (만든 시간)   | 예         |
|문서 날짜 수정 됨          | 예 (lastModifiedDate) *                         |                         | 예         |
|Doc 키워드               |                                                 |                         | 예         |
|문서 마지막 저장 한 사람          |                                                 |                         | 예         |
|문서 수정한 사람            |                                                 |                         | 예         |
|문서 제목                |                                                 |  예 (제목/제목)    | 예         |
|Doc 서식 파일               |                                                 |                         | 예         |
|문서 제목                  | 예 (제목)                                     |  예 (제목)            | 예         |
|Doc 버전                |                                                 |                         | 예         |
|주요 테마             | 예 (dominantTheme)                             |  예 (주요 테마)   | 예         |
|중복 된 하위 집합           |                                                 |                         | 예         |
|전자 메일 작업               |                                                 |                         | 예         |
|전자 메일 숨은 참조                  | 예 (숨은 참조)                                       |                         | 예         |
|전자 메일 참조                   | 예 (cc)                                        |                         | 예         |
|전자 메일 대화 ID      |                                                 |                         | 예         |
|받은 전자 메일 날짜        | 예 (받은 날짜)                                  |   예 (받은 날짜)        | 예         |
|보낸 전자 메일 날짜            | 예 (보냄)                                      |   예 (보냄)            | 예         |
|전자 메일에 첨부 파일 있음       |                                                 |                         | 예         |
|전자 메일 중요도           |                                                 |                         | 예         |
|전자 메일 인터넷 머리글     |                                                 |                         | 예         |
|전자 메일 수준                |                                                 |                         | 예         |
|전자 메일 메시지 ID           |                                                 |                         | 예         |
|전자 메일 참가자 도메인  | 예 (participantDomains)                        |                         | 예         |
|전자 메일 참가자         | 예 (참가자)                              |                         | 예         |
|전자 메일 받는 사람 도메인    | 예 (recipientDomains)                          |                         | 예         |
|전자 메일 받는 사람           | 예 (받는 사람)                                |                         | 예         |
|전자 메일 보안             |                                                 |                         | 예         |
|전자 메일 보낸 사람               | 예 (보낸 사람)                                    |   예 (보낸 사람)          | 예         |
|전자 메일 보낸 사람 도메인        | 예 (senderDomain)                              |                         | 예         |
|전자 메일 민감도          |                                                 |                         | 예         |
|전자 메일 설정                  | 예 (emailSetId)                                |   예 (EmailSetID)      | 예         |
|전자 메일 제목              | 예 (제목)                                   |   예 (제목/제목)   | 예         |
|전자 메일 스레드               |                                                 |                         | 예         |
|전자 메일을                   | 예 (to)                                        |                         | 예         |
|오류 코드                 | 예 (processingStatus)                          |                         | 예         |
|네이티브 경로 내보내기         |                                                 |                         | 예         |
|추출 된 텍스트 길이      |                                                 |                         | 예         |
|추출 된 텍스트 경로        |                                                 |                         | 예         |
|가족 번호                  | 예 (familyId)                                  |   예 (FamilyId)        | 예         |
|패밀리 크기                |                                                 |                         | 예         |
|File 클래스                 | 예 (fileClass)                                 |   예 (파일 클래스)      | 예         |
|파일 ID                    | 예 (fileId)                                    |   예 (Id)              | 예         |
|텍스트 포함                   |                                                 |                         | 예         |
|포함 유형             | 예 (inclusiveType)                             |   예 (포함 유형)  | 예         |
|입력 날짜 수정        |                                                 |                         | 예         |
|입력 파일 ID              |                                                 |                         | 예         |
|입력 경로                 |                                                 |                         | 예         |
|인터넷 메시지 ID        |                                                 |                         | 예         |
|대표          | 예 (markAsRepresentative)                      |                         | 예         |
|Item 클래스                 |                                                 |                         | 예         |
|부하 ID                    | 예 (loadId)                                    |                         | 예         |
|위치 이름              |                                                 |                         | 예         |
|Pivot로 표시            | 예 (markAsPivot)                               |   예 (Pivot로 표시 됨) | 예         |
|메시지 종류               | 예 (messageKind)                               |                         | 예         |
|기본 확장           |                                                 |                         | 예         |
|기본 파일 이름           |                                                 |    예 (파일 이름)      | 예         |
|기본 MD5                 |                                                 |                         | 예         |
|Native SHA 256             |                                                 |                         | 예         |
|기본 크기                | 예 (크기)                                      |   예 (NativeSize)     | 예         |
|네이티브 형식                | 예 (fileType)                                  |   예 (파일 형식)       | 예         |
|ND ET sort excl attach     |                                                 |                         | 예         |
|ND ET sort incl attach     |                                                 |                         | 예         |
|ND 집합                     |                                                 |                         | 예         |
|O365 제작자               | 예 (만든이) *                                   |   예 (보낸 사람/만든이)   | 예         |
|O365을 만든 사람            |                                                 |                         | 예         |
|O365 작성일          | 예 (createdTime) *                              |                         | 예         |
|O365 날짜 수정 됨         | 예 (lastModifiedDate) *                         |   예 (마지막으로 수정한 날짜) | 예      |
|O365 수정한 사람           |                                                 |                         | 예         |
|부모 노드                |                                                 |                         | 예         |
|피벗 ID                   | 예 (pivotId)                                   |  예 (PivotID)          | 예         |
|받는 사람 수            |                                                 |                         | 예         |
|행 번호                 |                                                 |                         | 예         |
|집합 ID                     |                                                 |                         | 예         |
|순서 inclusives 먼저 설정 |                                                 |                         | 예         |
|유사성 비율         |                                                 |                         | 예         |
|테마 목록                | 예 (주소록 목록)                                | 예 (테마 목록)       | 예         |
|Word count                 | 예 (wordCount)                                 |                         | 예         |
|관련성 점수 (문제)    | 예 (relevanceScore_issueNum)                   |                         |             |
|읽기 백분위 수 (문제)    | 예 (readPercentile_issueNum)                   |                         |             |
|관련성 태그 (문제)      | 예 (relevanceTag_issueNum)                     |                         |             |
|||||

  \* 이러한 필드의 경우 문서에 포함 된 값이 있으면 검색에서 해당 값의 우선 순위를 지정 합니다. 그렇지 않은 경우에는 Office 365의 값을 표시 합니다.
