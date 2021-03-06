---
title: 조사를 위해 데이터를 처리할 때의 오류 수정
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
description: 오류 수정을 사용 하 여 콘텐츠를 올바르게 처리 하지 못할 수 있는 데이터 조사 (미리 보기)의 데이터 문제를 해결 하는 방법을 알아봅니다.
ms.custom:
- seo-marvel-mar2020
- seo-marvel-apr2020
ms.openlocfilehash: c6c62bb1a3191e369d553df5eb451d4656e704d7
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48286034"
---
# <a name="error-remediation-when-processing-data-for-an-investigation"></a>조사를 위해 데이터를 처리할 때의 오류 수정

오류 수정을 통해 데이터 조사 (미리 보기)가 콘텐츠를 제대로 처리 하지 못하게 하는 데이터 문제를 해결할 수 있습니다. 예를 들어 암호로 보호 된 파일은 파일을 잠그거나 암호화 한 후에 처리할 수 없습니다. 오류 수정 프로그램을 사용 하 여 investigators에서 이러한 오류가 발생 한 파일을 다운로드 하 고, 암호 보호를 제거 하 고, 재구성 된 파일을 업로드할 수 있습니다.

다음 워크플로를 사용 하 여 데이터 조사 (미리 보기) 사례에서 오류가 발생 한 파일을 수정 합니다.

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a>처리 오류가 발생 한 파일을 수정 하기 위한 오류 업데이트 관리 세션 만들기

>[!NOTE]
>다음 절차 중에 오류 수정 마법사를 언제 든 지 닫을 경우, **보기** 드롭다운 메뉴에서 **오류 remediations** 를 선택 하 여 **처리** 탭에서 오류 수정 세션으로 돌아갈 수 있습니다.

1. 데이터 조사의 **처리** 탭에서 **보기** 드롭다운 메뉴의 **오류** 를 선택 합니다.

2. 오류 유형 또는 파일 형식 옆의 라디오 단추를 클릭 하 여 수정할 오류를 선택 합니다.  다음 예제에서는 암호로 보호 된 파일을 수정 합니다.

3. **+ 새 오류 수정을**클릭 합니다.

    ![새 오류 수정 관리 단추를 클릭 합니다.](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    오류가 발생 한 파일을 다운로드할 수 있도록 안전한 Azure 위치에 복사 되는 준비 단계부터 시작 하는 오류 관리 세션이 시작 됩니다.

    ![오류 수정 준비](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. 준비가 완료 되 면 **다음: 파일 다운로드** 를 클릭 하 여 다운로드를 계속 합니다.

    ![수정 해야 하는 파일 다운로드](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. 파일을 다운로드 하려면 **다운로드 대상 경로**를 지정 합니다. 로컬 컴퓨터에서 파일을 다운로드 해야 하는 경로입니다.  기본 경로인%USERPROFILE%\Downloads\errors은 로그인 한 사용자의 다운로드 폴더를 가리킵니다. 이는 필요에 따라 변경할 수 있습니다.

    >[!NOTE]
    >최적의 성능을 위해 원격 네트워크 경로 대신 로컬 파일 경로를 사용 하는 것이 좋습니다.

    > [!NOTE]
    > AzCopy을 설치 하지 않은 경우 [AzCopy을 사용한 시작](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) 으로 이동 하 여 설치 합니다.

6. **클립보드에 복사를**클릭 하 여 미리 정의 된 명령을 복사 합니다. Windows 명령 프롬프트를 시작 하 고 명령을 붙여 넣은 다음 enter 키 **를 누릅니다.**  

    파일이 다운로드 됩니다.

    ![명령 프롬프트에 다운로드 한 파일에 대 한 정보](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > 이 명령을 실행 하는 동안 문제가 발생 한 경우 [에는 Advanced eDiscovery에서 AzCopy 문제 해결](troubleshooting-azcopy.md)을 참조 하세요.

7. 파일을 다운로드 한 후에는 적절 한 도구를 사용 하 여 수정할 수 있습니다. 암호로 보호 된 파일의 경우에는 여러 가지 암호 해독 도구를 사용할 수 있습니다. 파일에 대 한 암호를 알고 있으면 열고 암호 보호 기능을 제거할 수 있습니다.
    
   > [!NOTE]
    > 재구성 된 파일의 파일 이름 및 디렉터리 구조를 유지 하는 것이 중요 합니다. 다운로드 한 파일 및 폴더의 경로 이름을 사용 하면 재구성 한 파일을 원본 파일과 연결할 수 있습니다.  디렉터리 구조 또는 파일 이름이 변경 되 면 다음 오류가 표시 `Cannot apply Error Remediation to the current Evidenceset` 됩니다.

8. 이제 데이터 조사 (미리 보기)로 돌아가 **다음: 파일 업로드**를 클릭 합니다.  이렇게 하면 이제 파일을 업로드할 수 있는 다음 단계로 이동 합니다.

    ![파일 업로드 탭](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. **파일 위치 경로** 텍스트 상자에 재구성 된 파일의 위치를 지정 하 고 **클립보드에 복사를**클릭 합니다.

10. Windows 명령 프롬프트에 명령을 붙여 넣고 **enter 키를 눌러 파일을 업로드** 합니다.

    ![명령 프롬프트에 업로드 된 파일에 대 한 정보](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. 마지막으로 데이터 조사 (미리 보기)로 돌아가 **다음: 프로세스 파일**을 클릭 합니다.

12. 처리가 완료 되 면  작업 집합으로 돌아가 재구성 된 파일을 볼 수 있습니다.

## <a name="what-happens-when-files-are-remediated"></a>파일을 수정 하는 경우 수행 되는 작업

재구성 한 파일을 업로드 하면 다음 필드를 제외 하 고 원래 메타 데이터가 보존 됩니다. 

- ExtractedTextSize
- HasText
- IsErrorRemediate
- LoadId
- ProcessingErrorMessage
- ProcessingStatus
- 텍스트
- WordCount
- WorkingsetId

데이터 조사 (미리 보기)의 모든 문서 메타 데이터 필드에 대 한 정의를 보려면 [문서 메타 데이터 필드](document-metadata-fields.md)를 참조 하십시오.
