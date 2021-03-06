---
title: Microsoft 365의 데이터 조사 (미리 보기)에 대 한 릴리스 정보
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
- seo-marvel-mar2020
- seo-marvel-apr2020
description: 이 문서에는 Microsoft 365의 데이터 조사 (미리 보기) 도구에 대 한 변경 내용 및 새로운 기능이 포함 된 릴리스 정보가 나와 있습니다.
ms.openlocfilehash: 2a46236d000c62c4ab73f8a47e9c9f661fb17a61
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285414"
---
# <a name="release-notes-for-data-investigations-preview-in-microsoft-365"></a>Microsoft 365의 데이터 조사 (미리 보기)에 대 한 릴리스 정보

Microsoft 365의 새 데이터 조사 (미리 보기) 도구를 사용 하 여 데이터 유출 사고나 내부 조사와 같은 데이터 관련 인시던트를 심사, 조사 및 수정할 수 있습니다. 데이터 조사의 공개 미리 보기를 통해 예정 된 기능 및 업데이트에 빠르게 액세스할 수 있습니다. 최신 기능에 빨리 액세스 하려면 보안 & 준수 센터에서 데이터 조사 (미리 보기)에 새로운 조사를 작성 합니다. 자세한 내용은 [Microsoft 365에서 data 유출 인시던트 관리](manage-data-spillage-incidents.md)를 참조 하세요.

## <a name="whats-new"></a>새로운 기능 

- **조사** -조사를 만들어 검색 및 인시던트를 그룹화 할 수 있습니다. 구성원을 추가 하거나 제거 하 여 조사에 액세스할 수 있는 사용자를 관리 합니다.  또한 즐겨찾기 조사를 선택 하 고 표시할 수 있습니다. 새 대시보드를 사용 하 여 조사 내의 및 간 활동을 추적 하 고 모니터링 합니다. 조사를 완료 한 후에는 닫거나 삭제할 수 있습니다.

- **관심** 사용자-사용자를 조사에 추가할 때 관심 있는 사서함, 비즈니스용 OneDrive 계정 및 Microsoft 팀 사이트를 볼 수 있습니다. 이를 사용 하 여 조사 콘텐츠 검색의 범위를 지정할 수 있습니다. 관심 있는 사람을 추가로 조사 하기 위해 Microsoft 365 및 기타 Microsoft 서비스의 작업과 관련 된 감사 레코드를 볼 수도 있습니다.

- **검색** -다양 한 검색 조건을 사용 하 여 조직 전체 검색을 만듭니다. 검색 하려는 사용자 또는 사이트를 알고 있는 경우 해당 사용자를 관심 있는 사람으로 추가 하거나 검색 만들기 마법사에서 사이트 위치를 지정 하 여이 작업을 수행할 수 있습니다. 

- **증거** -새 증거 집합을 만들고 검토 하려는 검색 결과를 추가 합니다. 개별 문서를 검토 하 고 조사 메모를 남기기 위해 주석을 달고 다른 환경으로 이동 하 여 결과를 내보낼 수 있습니다. 

- **검토** -인시던트에 추가 된 문서를 검토 하려면 native, text 및 near 기본 보기를 사용 합니다. 중복, 전자 메일 스레드 및 테마를 기준으로 항목을 그룹화 하 여 문서에 분석을 적용할 수도 있으며,이를 통해 인시던트 검토에 도움이 될 수 있습니다. 

- 문서를 검토할 때 텍스트 교정 **, 태그 지정 및 주석 달기** /태그 적용 및 주석 만들기
  
- **고급 인덱싱** -부분적으로 인덱싱된 항목이 있으면 모든 데이터를 검색할 수 있도록 요청 시 reindexed 됩니다.

- **오류** 해결 방법-처리 오류를 수정 하거나 다운로드 합니다. 여기에는 큰 파일 형식, 암호로 보호 된 파일 및 인덱싱 오류와 관련 된 기타 문제에 대 한 재구성 지원이 포함 됩니다. 

- **작업** -장기 실행 프로세스의 상태를 추적 합니다.

- **사서함 항목 영구 삭제** -긴급 상황에서 잘못 된 항목을 영구적으로 삭제 해야 할 수 있습니다. 이렇게 하려면 Security & 준수 센터 PowerShell에서 **PurgeType 하드 삭제** 명령을 실행 하 여 사서함에서 항목을 영구적으로 제거 하면 됩니다. 자세한 내용은 [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/new-compliancesearchaction)을 참조하세요.
