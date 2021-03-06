---
title: 검색 결과를 검토 집합에 추가
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
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: 고급 eDiscovery 사례 검토 집합에 해당 검색 결과의 검색 결과 또는 샘플을 추가 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: 25ea5fe076753d4a5685f1224b98a2005d334f5f
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48919980"
---
# <a name="add-search-results-to-a-review-set"></a>검색 결과를 검토 집합에 추가

검색 결과가 만족 스 러 우면 해당 검색 결과를 검토 하 고 분석할 준비가 되 면 대/소문자에서 검토 집합에 해당 결과를 추가할 수 있습니다. 원본 데이터를 검토 집합에 복사 하면 테마 검색, 거의 중복 검색 및 전자 메일 스레드 식별과 같은 고급 분석 도구를 제공 하 여 검토 및 분석 프로세스를 쉽게 수행할 수 있습니다. Microsoft 365에서 수집한 데이터와 함께 데이터를 검토할 수 있도록 타사 365 데이터 원본의 데이터를 검토 집합에 추가할 수도 있습니다.

검색 결과를 검토 집합에 추가 하면 (사례에 대 한 검토 집합이 **검토 집합** 탭에 나열 됨) 다음과 같은 상황이 발생 합니다.

- 검색이 다시 실행 됩니다. 즉, 검토 집합에 복사 되는 실제 검색 결과는 검색을 마지막으로 실행 했을 때 반환 된 예상 결과와 다를 수 있습니다.

- 검색 결과의 모든 항목은 라이브 서비스의 원본 데이터 원본에서 복사 되 고 Microsoft 클라우드의 안전한 Azure 저장소 위치로 복사 됩니다.

- 모든 항목 (콘텐츠 및 메타 데이터 포함)은 사례 데이터를 검토 하는 동안 검토 집합의 모든 데이터를 완벽 하 게 검색할 수 있도록 reindexed 합니다. 사례 조사 중에 검토 집합에서 데이터를 검색할 때 데이터를 정밀 검색 및 빠르게 검색할 수 있습니다.

- [Microsoft 암호화 기술로](encryption.md) 암호화 되 고 전자 메일 메시지와 첨부 된 파일을 검토 집합에 추가할 때 검색 결과에 반환 되는 전자 메일 메시지에 첨부 되는 파일의 암호를 해독 합니다. 검토 집합에서 해독 된 파일을 검토 하 고 쿼리할 수 있습니다. 암호 해독 된 전자 메일 첨부 파일을 검토 집합에 추가 하려면 RMS 암호 해독 역할을 할당 받아야 합니다. 자세한 내용은 [Microsoft 365 eDiscovery 도구에서 암호 해독](ediscovery-decryption.md)를 참조 하세요.

검토 집합에 데이터를 추가 하려면 검색 탭에서 검색을 클릭 하 고 플라이 아웃 페이지에서 **집합을 검토 하려면 결과 추가를** **클릭 합니다.**

기존 검토 집합에 추가 하거나 새 검토 집합을 만들 수 있습니다.  새 검토 집합에 추가 하는 경우 이름을 지정 하 고 **추가** 를 클릭 하 여 플라이 아웃 페이지를 표시 합니다.

![검토 집합 선택 및 컬렉션 구성 옵션](../media/AeD_AddToReviewSet.png)

검토 집합에 데이터를 추가 하는 것은 장시간 실행 되는 프로세스입니다. 이 프로세스에는 Microsoft 365 (예: 사서함 및 사이트)의 원본 데이터 원본에서 항목을 수집 하 여 Azure 저장소 위치로 복사한 다음 (이 복사 프로세스를 수집 하는 것이 *라고도 함)* 해당 항목을 다시 인덱싱하도록 포함 됩니다. **작업** 탭 또는 **검색** 탭의 진행 상태를 추적 하 여 **추가 된 데이터를 검토 집합** 열에서 모니터링할 수 있습니다. 검토 집합 처리가 완료 되 면 사례에서 **검토** 집합 탭을 클릭 한 다음 검토 집합을 클릭 하 여 검토 집합에서 데이터를 필터링, 검토, 태그 지정 및 내보내는 프로세스를 시작 합니다.

## <a name="define-options-to-scope-your-collection-for-review"></a>검토할 컬렉션 범위를 지정 하는 옵션 정의

기존 또는 새 검토 집합에 검색 콘텐츠를 추가할 때 검토를 위해 콘텐츠를 수집 하는 방법에 대 한 다음 옵션을 사용할 수 있습니다.

- **Sharepoint의 버전 포함 (베타)** :이 옵션을 사용 하 여 컬렉션의 버전 제한과 검색 매개 변수에 따라 모든 SharePoint 문서 버전의 컬렉션을 사용 하도록 설정 합니다. 이 옵션을 선택 하면 검토 집합에 추가 되는 항목의 크기가 크게 증가 합니다.

- **대화 검색 옵션** : 검토 집합에 추가 된 항목은 스레드 대화에서 앞뒤로 진행 되는 대화의 맥락에서 콘텐츠를 검토 하는 데 도움이 됩니다. 자세한 내용은 [Advanced eDiscovery에서 대화 검토](conversation-review-sets.md)를 참조 하세요.

- **최신 첨부 파일에 대 한 검색 사용** :이 옵션을 사용 하 여 나중에 검토할 수 있도록 컬렉션에 최신 첨부 파일이 나 연결 된 파일을 포함 합니다. 최신 첨부 파일과 관련 된 검색 가능한 속성에 대 한 자세한 내용은 [Advanced eDiscovery의 문서 메타 데이터 필드](document-metadata-fields-in-Advanced-eDiscovery.md)를 참조 하십시오.

## <a name="add-a-sample-to-a-review-set"></a>검토 집합에 샘플 추가

검색 결과의 유효성을 검토 집합에 추가 하기 전에 보다 철저히 확인 하려는 경우 모든 항목을 추가 하는 대신 검토 집합에 검색 결과의 예제를 추가할 수 있습니다.

검토 집합에 샘플을 추가 하려면 검색 탭에서 검색을 클릭 하 고 플라이 아웃 페이지에서 **샘플** 을 **클릭 합니다.** **매개 변수 샘플링** 페이지에서 다음 옵션 중 하나를 선택 합니다.

- **신뢰 수준%** 및 **신뢰도 간격%** -검토 집합에 추가 된 항목은 설정한 통계 매개 변수에 의해 결정 됩니다. 일반적으로 결과를 샘플링할 때 신뢰 수준과 간격을 사용 하는 경우에는 드롭다운 상자에서이를 지정 합니다. 그렇지 않으면 기본 설정을 사용 합니다.

- **무작위 샘플%** -검토 집합에 추가 되는 항목은 검색에서 반환 되는 총 항목 수에 대 한 지정 된 백분율을 임의로 선택 하 여 결정 합니다.

이전 옵션 중 하나를 선택 하 고 구성한 후에는 예제를 추가할 검토 집합을 선택한 다음 **보내기를** 클릭 합니다. 다시 말하지만 **작업** 탭 이나 **검색** 탭에서 **검토 집합에 추가 된 데이터** 열에서 상태를 모니터링 하 여 진행 상황을 추적할 수 있습니다.

## <a name="optical-character-recognition"></a>광학 인식

검토 집합에 검색 결과를 추가 하면 고급 eDiscovery의 OCR (광학 인식) 기능은 이미지에서 텍스트를 자동으로 추출 하며, 검토 집합에 추가 되는 데이터와 함께 이미지 텍스트를 포함 합니다. 검토 집합에서 선택한 이미지 파일의 텍스트 뷰어에서 추출한 텍스트를 볼 수 있습니다. 이렇게 하면 이미지의 텍스트에 대 한 추가 검토 및 분석을 수행할 수 있습니다. OCR은 느슨한 파일, 전자 메일 첨부 파일 및 포함 된 이미지에 대해 지원 됩니다. OCR에 대해 지원 되는 이미지 파일 형식 목록은 [Advanced eDiscovery에서 지원 되는 파일 형식을](supported-filetypes-ediscovery20.md#image)참조 하세요.

고급 eDiscovery에서 만드는 각 사례에 대해 OCR 기능을 사용 하도록 설정 해야 합니다. 자세한 내용은 [Configure search and analytics settings](configure-search-and-analytics-settings-in-advanced-ediscovery.md#optical-character-recognition-ocr)을 참조 하십시오.
