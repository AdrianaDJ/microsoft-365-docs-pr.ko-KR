---
title: 콘텐츠 검색 결과 내보내기
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: how-to
f1_keywords:
- ms.o365.cc.CustomizeExport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: ed48d448-3714-4c42-85f5-10f75f6a4278
description: Microsoft 365 준수 센터의 콘텐츠 검색에서 로컬 컴퓨터로 검색 결과를 내보냅니다. 전자 메일 결과를 PST 파일로 내보냅니다. SharePoint의 콘텐츠 및 비즈니스용 OneDrive 사이트는 기본 Office 문서로 내보내집니다.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 48f5cab4c25199873c795cdfb9afac54f4f402a0
ms.sourcegitcommit: 8ad481ed61cb6dabf8afb0fb04296666fa166450
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49422877"
---
# <a name="export-content-search-results"></a>콘텐츠 검색 결과 내보내기

콘텐츠 검색을 성공적으로 실행 한 후에는 검색 결과를 로컬 컴퓨터로 내보낼 수 있습니다. 전자 메일 결과 내보내면 컴퓨터에 PST 파일로 다운로드됩니다. SharePoint 및 비즈니스용 OneDrive 사이트에서 콘텐츠를 내보낼 때 기본 Office 문서의 복사본을 내보냅니다. 내보낸 검색 결과에는 다른 문서 및 보고서가 포함 되어 있습니다.
  
콘텐츠 검색 결과를 내보내면 결과가 준비 된 후 로컬 컴퓨터로 다운로드 됩니다.
  
## <a name="before-you-export-content-search-results"></a>콘텐츠 검색 결과를 내보내기 전에

- 검색 결과를 내보내려면 보안 & 준수 센터에서 내보내기 관리 역할을 할당 받아야 합니다. 이 역할은 기본 제공 eDiscovery 관리자 역할 그룹에 할당됩니다. 기본적으로 조직 관리 역할 그룹에는 할당되지 않습니다. 자세한 내용은 [eDiscovery 권한 할당](assign-ediscovery-permissions.md)을 참조하세요.

- 검색 결과를 PST 파일로 내보내는 데 사용하는 컴퓨터는 다음과 같은 시스템 요구 사항을 충족해야 합니다.
  
  - 32 비트 또는 64 비트 버전의 Windows 7 이상 버전
  
  - Microsoft .NET Framework 4.7
  
- EDiscovery 내보내기 도구<sup>1</sup>을 실행 하려면 다음과 같은 지원 되는 브라우저 중 하나를 사용 해야 합니다.

  - Microsoft Edge <sup>2</sup>
  
    또는

  - Microsoft Internet Explorer 10 이상 버전
  
  > [!NOTE]
  > <sup>1</sup> Microsoft는 ClickOnce 응용 프로그램에 대 한 타사 확장 또는 추가 기능을 제조 하지 않습니다. 타사 확장 또는 추가 기능에서 지원 되지 않는 브라우저를 사용 하 여 검색 결과를 내보낼 수는 없습니다.<br/>
  > <sup>2</sup> Microsoft Edge의 최근 변경 사항으로 인해 ClickOnce 지원은 더 이상 기본적으로 사용 되지 않도록 설정 되어 있습니다. 에 지에 ClickOnce 지원을 사용 하는 방법에 대 한 자세한 내용은 [Microsoft Edge에서 EDiscovery 내보내기 도구 사용](configure-edge-to-export-search-results.md)을 참조 하십시오.
  
- 로컬 컴퓨터에 검색 결과를 다운로드 하는 것이 좋습니다. 그러나 회사의 방화벽 또는 프록시 인프라에서 검색 결과를 다운로드할 때 문제가 발생 하지 않도록 하려면 검색 결과를 네트워크 외부의 가상 데스크톱으로 다운로드 하는 것이 좋습니다. 이렇게 하면 많은 수의 파일을 내보낼 때 Azure 데이터 연결에서 발생 하는 시간 초과가 줄어들 수 있습니다. 가상 데스크톱에 대 한 자세한 내용은 [Windows 가상 데스크톱](https://azure.microsoft.com/services/virtual-desktop)을 참조 하십시오. 

- 검색 결과를 다운로드할 때 성능을 개선 하려면 큰 결과 집합을 반환 하는 검색을 더 작은 검색으로 나누는 것이 좋습니다. 예를 들어 검색 쿼리에 날짜 범위를 사용 하 여 더 빠르게 다운로드할 수 있는 더 작은 결과 집합을 반환할 수 있습니다.
  
- 검색 결과를 내보낼 때 데이터가 로컬 컴퓨터로 다운로드 되기 전에 Microsoft 클라우드에서 Microsoft가 제공한 Azure 저장소 위치에 일시적으로 저장 됩니다. 조직이 Azure의 끝점에 연결할 수 있는지 (와일드 카드는 내보내기에 대 한 고유 식별자를 나타냄) **\* blob.core.windows.net 합니다** . 검색 결과 데이터는 만들어진 후 2 주 후 Azure 저장소 위치에서 삭제 됩니다. 
  
- 조직에서 프록시 서버를 사용 하 여 인터넷에 통신 하는 경우 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 프록시 서버 설정을 정의 해야 합니다 (따라서 내보내기 도구를 프록시 서버에서 인증할 수 있음). 이렇게 하려면 사용자의 Windows 버전과 일치 하는 위치에서  *machine.config*  파일을 엽니다. 
  
  - **32 비트:**`%windir%\Microsoft.NET\Framework\[version]\Config\machine.config`
  
  - **64 비트:**`%windir%\Microsoft.NET\Framework64\[version]\Config\machine.config`
  
    과 태그 사이의 아무  *machine.config*  파일에 다음 줄을 추가  `<configuration>` 합니다  `</configuration>` . `ProxyServer` `Port` 예를 들어,와 같이 조직의 올바른 값을 교체 해야 `proxy01.contoso.com:80` 합니다. 
  
    ```xml
    <system.net>
       <defaultProxy enabled="true" useDefaultCredentials="true">
         <proxy proxyaddress="https://ProxyServer :Port " 
                usesystemdefault="False" 
                bypassonlocal="True" 
                autoDetect="False" />
       </defaultProxy>
    </system.net>
    ```

## <a name="step-1-prepare-search-results-for-export"></a>1 단계: 내보내기에 대 한 검색 결과 준비

첫 번째 단계는 검색 결과의 내보내기를 준비하는 것입니다. 결과를 준비할 때 microsoft 클라우드에서 Microsoft가 제공한 Azure Storage 위치에 업로드 됩니다. 사서함 및 사이트의 콘텐츠는 시간당 최대 2gb로 업로드 됩니다.
  
1. [https://protection.office.com](https://protection.office.com)으로 이동합니다.
  
2. 회사 또는 학교 계정을 사용하여 로그인합니다.
  
3. 보안 & 준수 센터의 왼쪽 창에서 **Search** \> **콘텐츠 검색** 검색을 클릭 합니다.
  
4. **콘텐츠 검색** 페이지에서 검색을 선택 합니다. 
  
5. 세부 정보 창에서 **컴퓨터에 결과 내보내기** 아래의 **내보내기 시작** 을 클릭합니다.
  
    > [!NOTE]
    > 검색 결과 7 일 보다 오래 된 경우 검색 결과 업데이트 하 라는 메시지가 표시. 이런 경우 내보내기를 취소 클릭 합니다 **업데이트 검색 결과** 선택한 검색 한 다음 시작 결과 후 다시 내보내기에 대 한 세부 정보 창에서 업데이트 됩니다.  
  
6. **검색 결과 내보내기** 페이지의 **출력 옵션** 에서 다음 옵션 중 하나를 선택 합니다.
  
    - 형식을 인식할 수 없거나, 암호화 되거나, 다른 이유로 인덱싱되지 않은 모든 항목을 제외 합니다.
  
    - 형식을 인식할 수 없거나 암호화 되었거나 다른 이유로 인덱싱되지 않은 모든 항목
  
    - 다른 이유로 인해 형식이 인식 되지 않거나 암호화 되거나 인덱싱되지 않은 항목만
  
    부분적으로 인덱싱된 항목을 내보내는 방법에 대 한 설명은 [추가 정보](#more-information) 섹션을 참조 하십시오. 부분적으로 인덱싱된 항목에 대 한 자세한 내용은 [콘텐츠 검색에서 부분적으로 인덱싱된 항목](partially-indexed-items-in-content-search.md)을 참조 하십시오.
  
7. **Exchange 콘텐츠를 다음으로 내보내기** 에서 다음 옵션 중 하나를 선택 합니다.
  
    - **각 사서함에 대 한 PST 파일 1 개:** 검색 결과를 포함 하는 각 사용자 사서함에 대해 PST 파일 하나를 내보냅니다. 사용자의 보관 사서함에 포함 된 모든 결과는 동일한 PST 파일에 들어 있습니다. 이 옵션은 원본 사서함에서 사서함 폴더 구조를 reproduces 합니다.
  
    - **모든 메시지를 포함 하는 PST 파일 하나:** 검색에 포함 된 모든 원본 사서함의 검색 결과를 포함 하는 단일 PST 파일 (이름이 *Exchange .pst*)을 내보냅니다. 이 옵션은 각 메시지에 대 한 사서함 폴더 구조를 reproduces 합니다.
  
    - **단일 폴더에 있는 모든 메시지를 포함 하는 PST 파일 하나:** 모든 메시지가 최상위 단일 폴더에 있는 단일 PST 파일로 검색 결과를 내보냅니다. 이 옵션을 사용 하면 검토자가 각 항목의 원래 사서함 폴더 구조를 탐색할 필요 없이 시간순으로 항목을 검토할 수 있습니다 (보낸 날짜별로 항목이 정렬 됨).
  
    - **개별 메시지:** .Msg 형식을 사용 하 여 검색 결과를 개별 전자 메일 메시지로 내보냅니다. 이 옵션을 선택 하면 전자 메일 검색 결과가 파일 시스템의 폴더로 내보내집니다. 개별 메시지에 대 한 폴더 경로는 결과를 PST 파일로 내보낸 경우 사용 하는 것과 같습니다.
  
      > [!IMPORTANT]
      > RMS로 보호 된 메시지를 내보낼 때 암호를 해독 하려면 전자 메일 검색 결과를 개별 메시지로 내보내야 합니다. 검색 결과를 PST 파일로 내보내는 경우 암호화 된 메시지는 암호화 된 상태로 유지 됩니다. 자세한 내용은이 문서에서 [RMS로 보호 된 전자 메일 메시지 및 암호화 된 첨부 파일 암호 해독](#decrypting-rms-protected-email-messages-and-encrypted-file-attachments) 을 참조 하십시오.
  
8. 중복 메시지를 제외 하려면 **중복 제거 사용** 확인란을 클릭 합니다. 이 옵션은 검색의 콘텐츠 원본에 Exchange 사서함 또는 공용 폴더가 포함 되어 있는 경우에만 표시 됩니다. 
  
    이 옵션을 선택 하면 검색 된 사서함에서 같은 메시지의 복사본을 여러 개 찾은 경우에도 하나의 메시지 복사본만 내보내집니다. 중복 메시지의 복사본을 포함 하는 사서함 (또는 공용 폴더)을 식별할 수 있도록 중복 메시지의 모든 복사본에 대 한 행이 포함 된 결과 내보내기 보고서 (Results.csv) 복제 제거 및 중복 항목이 식별 되는 방식에 대 한 자세한 내용은 [eDiscovery 검색 결과의 중복](de-duplication-in-ediscovery-search-results.md)제거를 참조 하십시오.
  
9. **Sharepoint 문서 버전 포함** 확인란을 클릭 하 여 모든 sharepoint 문서 버전을 내보냅니다. 이 옵션은 검색의 콘텐츠 원본에 SharePoint 또는 비즈니스용 OneDrive 사이트를 포함 하는 경우에만 표시 됩니다. 
  
10. **압축 (zip) 폴더에서 파일 내보내기** 확인란을 클릭 하 여 검색 결과를 압축 된 폴더로 내보냅니다. 이 옵션은 Exchange 항목을 개별 메시지로 내보내도록 선택 하 고 검색 결과에 SharePoint 또는 OneDrive 문서가 포함 되어 있는 경우에만 사용할 수 있습니다. 이 옵션은 항목을 내보낼 때 Windows 파일 경로 이름의 260 문자 제한을 해결 하는 데 주로 사용 됩니다. [추가 정보](#more-information) 섹션에서 "내보낸 항목의 파일 이름"을 참조 하세요. 
  
11. **내보내기 시작** 을 클릭합니다. 검색 결과를 다운로드 하기 위해 준비 중 이며,이는 Microsoft 클라우드의 Azure 저장소 위치에 업로드 되 고 있음을 의미 합니다. 이 작업에는 몇 분이 걸릴 수 있습니다.

내보낸 검색 결과를 다운로드 하는 방법에 대 한 지침은 다음 섹션을 참조 하십시오.
  
## <a name="step-2-download-the-search-results"></a>2 단계: 검색 결과 다운로드

다음 단계에서는 Azure 저장소 위치에서 로컬 컴퓨터로의 검색 결과를 다운로드 합니다.
  
1. **콘텐츠 검색** 페이지에서 **내보내기** 탭을 클릭 합니다. 
  
   **새로 고침** 을 클릭 하 여 만든 내보내기 작업이 표시 되도록 내보내기 작업 목록을 업데이트 해야 할 수 있습니다. 내보내기 작업의 이름은 검색 이름에 **_Export** 추가 된 해당 검색과 같습니다.
  
2. 1 단계에서 만든 내보내기 작업을 선택 합니다.

3. 플라이 아웃 페이지의 **내보내기 키** 에서 **클립보드에 복사** 를 클릭 합니다. 6 단계에서이 키를 사용 하 여 검색 결과를 다운로드 합니다.
  
4. **결과 다운로드** 를 클릭합니다.

5. **EDiscovery 내보내기 도구** 를 설치 하 라는 메시지가 표시 되 면 **설치** 를 클릭 합니다.

6. **EDiscovery 내보내기 도구** 에서 다음을 수행 합니다.

   ![eDiscovery 내보내기 도구](../media/eDiscoveryExportTool.png)

   1. 3 단계에서 복사한 내보내기 키를 해당 상자에 붙여 넣습니다.
  
   2. **찾아보기** 를 클릭하여 검색 결과 파일을 다운로드하려는 위치를 지정합니다.
  
      > [!NOTE]
      > 디스크 작업 양이 많은 경우 (읽기 및 쓰기), 검색 결과를 로컬 디스크 드라이브로 다운로드 해야 합니다. 매핑된 네트워크 드라이브 또는 다른 네트워크 위치로 다운로드 하지 마십시오. 
  
6. **시작** 을 클릭하여 컴퓨터에 검색 결과를 다운로드합니다.
  
    **eDiscovery 내보내기 도구** 는 다운로드할 남은 항목의 예상 개수(크기)를 포함하여 내보내기 프로세스에 대한 상태 정보를 표시합니다. 내보내기 프로세스가 완료 되 면 다운로드 한 위치에서 파일에 액세스할 수 있습니다.

## <a name="more-information"></a>추가 정보

검색 결과를 내보내는 방법에 대 한 자세한 내용은 다음과 같습니다.
  
[내보내기 제한](#export-limits)
  
[보고서 내보내기](#export-reports)
  
[부분적으로 인덱싱된 항목 내보내기](#exporting-partially-indexed-items)

[개별 메시지 또는 PST 파일 내보내기](#exporting-individual-messages-or-pst-files)
  
[10만 개 이상의 사서함에서 결과 내보내기](#exporting-results-from-more-than-100000-mailboxes)

[RMS로 보호 된 전자 메일 메시지 및 암호화 된 첨부 파일의 암호 해독](#decrypting-rms-protected-email-messages-and-encrypted-file-attachments)

[내보낸 항목의 파일 이름](#filenames-of-exported-items)  
  
[없으며](#miscellaneous)
  
### <a name="export-limits"></a>내보내기 제한
  
- 보안 & 준수 센터에서 검색 결과를 내보낼 경우 다음과 같은 제한이 있습니다.

  - 단일 콘텐츠 검색에서 최대 2tb 데이터를 내보낼 수 있습니다. 검색 결과가 2TB 보다 크면 날짜 범위 또는 기타 필터를 사용 하 여 검색 결과의 총 크기를 줄이는 것이 좋습니다.
  
  - 조직은 하루 중 최대 2tb의 데이터를 내보낼 수 있습니다.
  
  - 조직 내에서 동시에 최대 10개의 내보내기를 실행할 수 있습니다.

  - 단일 사용자가 동시에 최대 3 개의 내보내기를 실행할 수 있습니다.
  
  - Office 365 보안 & 준수 센터 또는 Microsoft 365 준수 센터의 eDiscovery 내보내기 도구를 사용 하 여 최대 10만 사서함에서 검색 결과를 다운로드할 수 있습니다. 10만 개 이상의 사서함에서 검색 결과를 다운로드 하려면 보안 & 준수 센터 PowerShell을 사용 해야 합니다. 자세한 내용은 10만 개 [이상의 사서함에서 결과 내보내기](#exporting-results-from-more-than-100000-mailboxes)를 참조 하십시오.

  > [!NOTE]
  > 또한 콘텐츠 검색에서 보고서를 내보낼 때 동시에 실행 되는 내보내기 수와 단일 사용자가 실행할 수 있는 내보내기 수에 대해 계산 됩니다.
  
- 앞에서 설명한 것 처럼 사서함 및 사이트의 검색 결과는 1 단계: Microsoft에서 제공 하는 Azure 저장소 위치로 업로드 되며,이 위치에 [대 한 검색 결과 준비를 수행](#step-1-prepare-search-results-for-export)하는 데 사용 됩니다.
  
- 내보낼 수 있는 최대 PST 파일 크기는 기본적으로 10gb입니다. 즉, 사용자 사서함의 검색 결과가 10gb 보다 크면 사서함에 대 한 검색 결과를 두 개 이상의 개별 PST 파일로 내보냅니다. 모든 검색 결과를 단일 PST 파일에 내보내도록 선택한 경우 총 검색 결과 크기가 10gb 보다 크면 PST 파일이 추가 PST 파일로 spilt 됩니다. 이 기본 크기를 변경 하려는 경우 검색 결과를 내보내는 데 사용 하는 컴퓨터에서 Windows 레지스트리를 편집할 수 있습니다. [EDiscovery 검색 결과를 내보낼 때 PST 파일 크기 변경을](change-the-size-of-pst-files-when-exporting-results.md)참조 하세요.
  
    또한 단일 사서함의 콘텐츠가 10gb 보다 많은 경우 특정 사서함의 검색 결과는 여러 PST 파일로 분할 되지 않습니다. 단일 폴더에 있는 모든 메시지를 포함 하는 하나의 PST 파일로 검색 결과를 내보내고 검색 결과가 10gb 보다 크면 해당 항목은 계속 해 서 시간순으로 구성 되므로 보낸 날짜를 기준으로 추가 PST 파일에 spilt 됩니다.
  
### <a name="export-reports"></a>보고서 내보내기
  
- 검색 결과를 내보낼 때 검색 결과 외에 다음과 같은 보고서가 포함 됩니다.
  
  - **내보내기 요약** 내보내기에 대 한 요약이 포함 된 Excel 문서입니다. 여기에는 검색 된 콘텐츠 원본 수, 예상 및 다운로드 되는 search 결과 크기, 그리고 내보낸 항목의 예상 및 다운로드 된 항목과 같은 정보가 포함 됩니다.
  
  - **매니페스트** 검색 결과에 포함 된 각 항목에 대 한 정보를 포함 하는 매니페스트 파일 (XML 형식)입니다.
  
  - **결과가** 검색 결과로 다운로드 되는 각 항목에 대 한 정보가 포함 된 Excel 문서입니다. 전자 메일의 경우 결과 로그에 다음을 비롯 한 각 메시지에 대 한 정보가 포함 됩니다.
  
    - 원본 사서함에 있는 메시지의 위치 (포함 여부는 주 메시지는 보관 사서함 또는).
  
    - 메시지가 전송된 날짜

    - 메시지의 제목 줄입니다.

    - 보낸 사람 및 메시지 받는 사람입니다.

    - 검색 결과를 내보낼 때 중복 제거 옵션을 사용 하도록 설정한 경우 메시지가 중복 메시지 인지 여부 중복 메시지에는 중복 된 메시지를 식별 하는 **중복 항목** 열에 대 한 값이 포함 되어 있습니다. **중복 항목** 열에 있는 값은 내보낸 메시지의 항목 id를 포함 합니다. 자세한 내용은 [eDiscovery 검색 결과의 중복](de-duplication-in-ediscovery-search-results.md)제거를 참조 하세요.

      SharePoint 및 비즈니스용 OneDrive 사이트의 문서에 대해 결과 로그에 다음을 비롯 한 각 문서에 대 한 정보가 포함 됩니다.

      - 문서에 대 한 URL입니다.

      - 문서가 있는 사이트 모음의 URL입니다.

      - 문서를 마지막으로 수정한 날짜입니다.

      - 이름 (에 있는 제목 열 결과 로그에서) 문서입니다.

  - **인덱싱되지 않은 항목** 검색 결과에 포함 될 부분 인덱싱된 모든 항목에 대 한 정보가 포함 된 Excel 문서입니다. 검색 결과 보고서를 생성할 때 부분적으로 인덱싱된 항목을 포함 하지 않으면이 보고서는 계속 다운로드 되지만 비어 있게 됩니다.

  - **오류 및 경고** 내보내는 동안 발생 한 파일에 대 한 오류 및 경고를 포함 합니다. 각 개별 오류 또는 경고와 관련 된 정보는 오류 세부 정보 열을 참조 하십시오.

  - **건너뛴 항목** SharePoint 및 비즈니스용 OneDrive 사이트에서 검색 결과를 내보낼 때 내보내기에는 대개 건너뛴 항목 보고서 (SkippedItems.csv)가 포함 됩니다. 이 보고서에 언급 된 항목은 일반적으로 폴더 또는 문서 집합과 같이 다운로드 되지 않는 항목입니다. 이러한 유형의 항목을 내보내지 않는 것은 의도적으로 설계 된 것입니다. 건너뛴 다른 항목의 경우 건너뛴 항목 보고서의 ' 오류 유형 ' 및 ' 오류 세부 정보 ' 필드에는 항목이 건너뛰고 다른 검색 결과와 함께 다운로드 되지 않은 이유가 표시 됩니다.

  - **추적 로그** 내보내기 프로세스에 대 한 자세한 로깅 정보와 내보내기 중 문제를 파악 하는 데 도움이 되는 정보를 포함 합니다.
  
    > [!NOTE]
    > 실제 검색 결과를 내보내지 않고도 이러한 문서를 내보낼 수 있습니다. [콘텐츠 검색 보고서 내보내기를](export-a-content-search-report.md)참조 하세요. 
  
### <a name="exporting-partially-indexed-items"></a>부분적으로 인덱싱된 항목 내보내기
  
- 검색 결과의 모든 사서함 항목을 반환 하는 콘텐츠 검색에서 사서함 항목을 내보내는 경우 (검색 쿼리에 포함 된 키워드가 없는 경우) 부분적으로 인덱싱된 항목이 인덱싱되지 않은 항목을 포함 하는 PST 파일에 복사 되지 않습니다. 이는 부분적으로 인덱싱된 항목을 비롯 한 모든 항목이 일반 검색 결과에 자동으로 포함 되기 때문입니다. 즉, 부분적으로 인덱싱된 항목은 인덱싱된 다른 항목을 포함 하는 PST 파일이 나 개별 메시지에 포함 됩니다.

    인덱싱된 항목과 부분적으로 인덱싱된 항목을 모두 내보내거나 모든 항목을 반환 하는 콘텐츠 검색에서 인덱싱된 항목만 내보내는 경우 같은 수의 항목이 다운로드 됩니다. 콘텐츠 검색에 대 한 예상 검색 결과 (보안 & 준수 센터의 검색 통계에 표시 됨)가 여전히 부분적으로 인덱싱된 항목의 수에 대 한 별도의 추정치를 포함 하는 경우에도 마찬가지입니다. 예를 들어 검색 쿼리에 키워드가 없는 모든 항목을 포함 하는 검색에 대 한 예상은 1000 항목이 발견 되 고 해당 200 부분 인덱싱된 항목도 검색 되었음을 나타냅니다. 이 경우에는 검색에서 모든 항목이 반환 되므로 1000 항목에 부분적으로 인덱싱된 항목이 포함 되어 있습니다. 즉, 검색에서 반환 되는 총 항목은 1000, 1200 항목 (예상 대로)은 아닙니다. 이 검색의 결과를 내보내고 인덱싱된 및 부분 인덱싱된 항목을 내보내도록 선택 하거나 부분적으로 인덱싱된 항목만 내보내려면 1000 항목이 다운로드 됩니다. 다시 말하지만, 빈 검색 쿼리를 사용 하 여 모든 항목을 반환 하면 부분적으로 인덱싱된 항목이 일반 (인덱싱된) 결과에 포함 되기 때문입니다. 이 예에서 부분적으로 인덱싱된 항목만 내보내도록 선택한 경우 200 인덱싱되지 않은 항목만 다운로드 됩니다.

    또한 이전 예제에서 인덱싱 및 부분적으로 인덱싱된 항목을 내보내거나 인덱싱된 항목만 내보내는 경우 내보낸 검색 결과에 포함 된 **내보내기 요약** 보고서에는 1000 개 항목을 나열 하 고, 앞에서 설명한 것과 같은 이유로 다운로드 한 항목 1000을 나열할 수 있습니다. 

- 결과를 내보내려는 검색에서 특정 콘텐츠 위치나 조직의 모든 콘텐츠 위치를 검색 한 경우 검색 조건과 일치 하는 항목을 포함 하는 콘텐츠 위치의 일부 항목만 내보내집니다. 즉, 사서함 이나 사이트에서 검색 결과가 발견 되지 않으면 해당 사서함 이나 사이트에서 부분적으로 인덱싱된 항목을 내보내지 않습니다. 이는 조직의 여러 위치에서 부분적으로 인덱싱된 항목을 내보낼 때 내보내기 오류가 발생할 가능성이 높아지고 검색 결과를 내보내고 다운로드 하는 데 걸리는 시간이 길어질 수 있기 때문입니다.

    검색에 대 한 모든 콘텐츠 위치에서 부분적으로 인덱싱된 항목을 내보내려면 검색 쿼리에서 키워드를 제거 하 여 모든 항목을 반환 하도록 검색을 구성한 다음 검색 결과를 내보낼 때 부분적으로 인덱싱된 항목만 내보냅니다.

    ![세 번째 내보내기 옵션을 사용 하 여 인덱싱되지 않은 항목만 내보내기](../media/5d7be338-a0e5-425f-8ba5-92769c24bf75.png)
  
- SharePoint 또는 비즈니스용 OneDrive 사이트에서 검색 결과를 내보낼 때에는 사용자가 선택한 내보내기 옵션 및 검색 된 사이트에 search 조건과 일치 하는 인덱싱된 항목이 포함 되어 있는지 여부에 따라 인덱싱되지 않은 항목을 내보낼 수 있습니다. 예를 들어 특정 SharePoint 또는 비즈니스용 OneDrive 사이트를 검색 하는 경우 검색 결과가 발견 되지 않으면 두 번째 내보내기 옵션을 선택 하 여 인덱싱된 항목과 인덱싱되지 않은 항목을 모두 내보내는 경우 해당 사이트에서 인덱싱되지 않은 항목을 내보내지 않습니다. 사이트의 인덱싱된 항목이 검색 조건과 일치 하는 경우 인덱싱된 항목과 인덱싱되지 않은 항목을 모두 내보낼 때 해당 사이트에서 인덱싱되지 않은 모든 항목을 내보냅니다. 다음 그림에서는 사이트에 검색 조건과 일치 하는 인덱싱된 항목이 포함 되어 있는지 여부에 따라 내보내기 옵션을 설명 합니다.

    ![사이트에 검색 조건과 일치 하는 인덱싱된 항목이 포함 되어 있는지 여부에 따라 내보내기 옵션을 선택 합니다.](../media/94f78786-c6bb-42fb-96b3-7ea3998bcd39.png)

    1. 검색 조건과 일치 하는 인덱싱된 항목만 내보내집니다. 부분적으로 인덱싱되지 않은 항목은 내보내지지 않습니다.

    2. 사이트에서 검색 조건과 일치 하는 인덱스 된 항목이 없는 경우 해당 사이트에서 부분적으로 인덱싱된 항목을 내보내지 않습니다. 사이트의 인덱싱된 항목이 검색 결과에 반환 되 면 해당 사이트에서 부분적으로 인덱싱된 항목이 내보내집니다. 즉, 검색 조건과 일치 하는 항목을 포함 하는 사이트의 부분적으로 인덱싱된 항목만 내보내집니다.

    3. 사이트에 검색 조건과 일치 하는 항목이 포함 되어 있는지 여부에 관계 없이 검색의 모든 사이트에서 모든 부분적으로 인덱싱된 항목을 내보냅니다.

    부분적으로 인덱싱된 항목을 내보내도록 선택 하는 경우에는 **Exchange 콘텐츠를 내보낼 때** 선택한 옵션에 관계 없이 부분적으로 인덱싱된 사서함 항목이 별도의 PST 파일로 내보내집니다.

- 부분적으로 인덱싱된 항목이 검색 결과에 반환 되는 경우, 부분적으로 인덱싱된 항목의 다른 속성이 검색 조건과 일치 하는 경우 해당 부분 인덱스는 일반 검색 결과와 함께 내보내집니다. 따라서 인덱싱된 항목과 부분적으로 인덱싱된 항목을 모두 선택 하는 경우 ( **형식을 인식할 수 없거나, 암호화 되거나, 다른 이유** 내보내기 옵션을 사용 하지 않은 항목을 포함 하는 경우)에는 일반 결과로 내보낸 부분적으로 인덱싱된 항목이 Results.csv 보고서에 나열 됩니다. 인덱싱되지 않은 items.csv 보고서에는 나열 되지 않습니다.
  
### <a name="exporting-individual-messages-or-pst-files"></a>개별 메시지 또는 PST 파일 내보내기
  
- 메시지의 파일 경로 이름이 Windows의 최대 문자 제한을 초과 하는 경우 파일 경로 이름이 잘립니다. 하지만 원본 파일 경로 이름이 매니페스트 및 ResultsLog에 나열 됩니다.
  
- 앞에서 설명한 것 처럼 전자 메일 검색 결과는 파일 시스템의 폴더로 내보내집니다. 개별 메시지의 폴더 경로는 사용자 사서함의 폴더 경로를 복제 합니다. 예를 들어 사용자의 받은 편지함에 있는 "ContosoCase101" 라는 검색 메시지는 폴더 경로에 있습니다  `~ContosoCase101\\<date of export\Exchange\user@contoso.com (Primary)\Top of Information Store\Inbox` .

- 단일 폴더에 있는 모든 메시지를 포함 하는 하나의 PST 파일에 전자 메일 메시지를 내보내도록 선택한 경우 **지운** 편지함 폴더와 **검색 폴더** 폴더는 최상위 pst 폴더에 포함 됩니다. 이러한 폴더는 비어 있습니다.

- 앞에서 설명한 것 처럼, 내보낼 때 RMS 보호 메시지를 해독 하려면 전자 메일 검색 결과를 개별 메시지로 내보내야 합니다. 전자 메일 검색 결과를 PST 파일로 내보내는 경우 암호화 된 메시지는 암호화 된 상태로 유지 됩니다.
  
### <a name="exporting-results-from-more-than-100000-mailboxes"></a>10만 개 이상의 사서함에서 결과 내보내기

- 앞에서 설명한 것 처럼, 10만 개 이상의 사서함에서 검색 결과를 다운로드 하려면 보안 & 준수 센터 PowerShell을 사용 해야 합니다. 이 섹션의 다음 스크립트를 실행 하 여 이러한 검색 결과를 다운로드할 수 있습니다. 이 스크립트를 사용 하는 경우 검색 결과를 이미 내보낸 것 이며 (내보내기 작업은 콘텐츠 검색 도구의 **내보내기 탭에** 표시 됨) 지금 다운로드 하려고 한다고 가정 합니다.

   ```powershell
   $export=Get-ComplianceSearchAction SEARCHNAME_Export -IncludeCredential;
   $exportUrl=   [System.Uri]::EscapeDataString(($export.Results.Split(";") | ?{$_ -like '*Container url*'} | %{$_.Split(":",2)} | select -last 1).Trim());
   $exportToken=($export.Results.Split(";") | ?{$_ -like '*SAS Token*'} | %{$_.Split(":",2)} | select -last 1).Trim();
   ."$env:ProgramFiles\Internet Explorer\IEXPLORE.EXE" "https://complianceclientsdf.blob.core.windows.net/v16/Microsoft.Office.Client.Discovery.UnifiedExportTool.application?name=$($export.Name)&source=$exportUrl&zip=allow&trace=1";
   $exportToken | clip;
   ```

  스크립트에서 결과를 내보내려는 검색의 이름을 지정 해야 합니다. 예를 들어 이라는 검색에는 `SearchAllMailboxes` SEARCHNAME_Export를으로 바꿉니다 `SearchAllMailboxes_Export` .

  스크립트에 검색 이름을 추가한 후 스크립트 텍스트를 복사한 다음 [Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell)된 Windows PowerShell 창에 붙여넣을 수 있습니다. 스크립트를 붙여 넣은 후 eDiscovery 내보내기 도구가 표시 됩니다 (예: UI를 사용 하 여 검색 결과를 다운로드 하는 경우).

  ![eDiscovery 내보내기 도구](../media/eDiscoveryExportTool.png)

  내보내기 키 상자를 클릭 한 다음 키를 눌러 `CTRL + V` export 키를 붙여 넣습니다 (스크립트는 내보내기 키를 클립보드에 복사). **찾아보기를** 클릭 하 여 파일을 다운로드 하려는 위치를 지정한 다음 다운로드를 시작 합니다.

  앞에서 설명한 것 처럼 디스크 작업의 양이 많아 (읽기 및 쓰기), 검색 결과를 로컬 디스크 드라이브에 다운로드 하는 것이 좋습니다. 검색 결과를 매핑된 네트워크 드라이브 또는 다른 네트워크 위치로 다운로드 하지 않습니다.

### <a name="decrypting-rms-protected-email-messages-and-encrypted-file-attachments"></a>RMS로 보호 된 전자 메일 메시지 및 암호화 된 첨부 파일의 암호 해독

콘텐츠 검색 결과에 포함 된 모든 권한 보호 (RMS 보호) 전자 메일 메시지는 내보낼 때 암호가 해독 됩니다. 또한 [Microsoft 암호화 기술로](encryption.md) 암호화 되 고 검색 결과에 포함 된 전자 메일 메시지에 첨부 되는 모든 파일은 내보내기 시에도 암호 해독 됩니다. 이 암호 해독 기능은 eDiscovery 관리자 역할 그룹의 구성원에 대해 기본적으로 사용 하도록 설정 됩니다. 이는 RMS 암호 해독 관리 역할이 기본적으로이 역할 그룹에 할당 되기 때문입니다. 암호화 된 전자 메일 메시지 및 첨부 파일을 내보낼 때는 다음 사항을 염두에 두어야 합니다.
  
- 앞에서 설명한 것 처럼 RMS 보호 메시지를 내보낼 때 암호를 해독 하려면 검색 결과를 개별 메시지로 내보내야 합니다. 검색 결과를 PST 파일로 내보내는 경우 RMS로 보호 된 메시지는 암호화 된 상태로 유지 됩니다.

- 해독 된 메시지는 **ResultsLog** 보고서에서 식별 됩니다. 이 보고서에는 **디코드 상태** 라는 열이 있으며이 열에서 **디코딩된** 값은 암호 해독 된 메시지를 식별 합니다.

- 검색 결과를 내보낼 때 첨부 파일의 암호를 해독 하는 것 외에도 검색 결과를 미리 볼 때 해독 된 파일을 미리 볼 수 있습니다. 권한으로 보호 된 전자 메일 메시지는 내보낸 후에만 볼 수 있습니다.

- 현재, 검색 결과를 내보낼 때 암호 해독 기능에는 SharePoint 및 비즈니스용 OneDrive 사이트의 암호화 된 콘텐츠가 포함 되지 않습니다. 그러나 Microsoft 암호화 기술을 사용 하 여 암호화 되 고 SharePoint Online 및 비즈니스용 OneDrive에 저장 된 문서에 대 한 지원이 곧 제공 될 예정입니다.

- 누군가가 RMS 보호 메시지 및 암호화 된 첨부 파일의 암호를 해독할 수 없도록 하려면 기본 제공 eDiscovery 관리자 역할 그룹을 복사 하 여 사용자 지정 역할 그룹을 만든 다음 사용자 지정 역할 그룹에서 RMS 암호 해독 관리 역할을 제거 해야 합니다. 그런 다음 메시지의 암호를 해독 하지 않으려는 사용자를 사용자 지정 역할 그룹의 구성원으로 추가 합니다.
  
### <a name="filenames-of-exported-items"></a>내보낸 항목의 파일 이름
  
- 로컬 컴퓨터로 내보낸 전자 메일 메시지 및 사이트 문서에 대 한 전체 경로 이름에는 260 자 제한이 있습니다 (운영 체제에 의해 부과 됨). 내보낸 항목의 전체 경로 이름에는 항목의 원래 위치와 검색 결과가 다운로드 되는 로컬 컴퓨터의 폴더 위치가 포함 됩니다. 예를 들어 eDiscovery 내보내기 도구에서 검색 결과를 다운로드 하도록 지정 하는 경우  `C:\Users\Admin\Desktop\SearchResults` 다운로드 한 전자 메일 항목의 전체 경로 이름은  `C:\Users\Admin\Desktop\SearchResults\ContentSearch1\03.15.2017-1242PM\Exchange\sarad@contoso.com (Primary)\Top of Information Store\Inbox\Insider trading investigation.msg` 입니다.

    260 문자 제한이 초과 되는 경우에는 항목의 전체 경로 이름이 잘립니다.

  - 전체 경로 이름이 260 자를 넘으면 파일 이름이 제한 미만으로 단축 됩니다. 잘린 파일 이름 (확장명 제외)은 8 자 미만 이어야 합니다.

  - 파일 이름을 단축 하 고 전체 경로 이름이 여전히 너무 긴 경우에는 항목이 현재 위치에서 상위 폴더로 이동 됩니다. 경로 이름이 여전히 너무 길면 프로세스가 반복 되 고, 파일 이름을 짧게 줄인 다음 다시 상위 폴더로 이동 합니다. 이 프로세스는 전체 경로 이름이 260 문자 제한 미만으로 반복 됩니다.

  - 잘린 전체 경로 이름이 이미 있으면 파일 이름 끝에 버전 번호가 추가 됩니다. 예를 들면  `statusmessage(2).msg` 입니다.

    이 문제를 완화 하려면 짧은 경로 이름을 사용 하 여 검색 결과를 위치에 다운로드 하는 것이 좋습니다. 예를 들어 이름이 이라는 폴더로 검색 결과를 다운로드 하는  `C:\Results` 것 보다 내보낸 항목의 경로 이름에 대 한 문자가 추가 됩니다  `C:\Users\Admin\Desktop\Results` .

- 사이트 문서를 내보낼 때 문서의 원래 파일 이름도 수정 될 수 있습니다. 이 작업은 보류 중인 SharePoint 또는 비즈니스용 OneDrive 사이트에서 삭제 된 문서에 대해 특별히 수행 됩니다. 보류 중인 사이트에 있는 문서를 삭제 하면 삭제 된 문서가 사이트를 보류 했을 때 만들어진 사이트에 대 한 보존 보류 라이브러리로 자동으로 이동 됩니다. 삭제 된 문서를 보존 보류 라이브러리로 이동 하면 해당 문서의 원래 파일 이름에 임의로 생성 된 고유 ID가 추가 됩니다. 예를 들어 문서에 대 한 파일 이름이  `FY2017Budget.xlsx` 있고 나중에 해당 문서를 삭제 하 여 보존 보류 라이브러리로 이동한 경우에는 보존 보류 라이브러리로 이동 된 문서의 파일 이름이 다음과 같이 수정 됩니다  `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx` . 보존 보류 라이브러리의 문서가 콘텐츠 검색의 쿼리와 일치 하 고 해당 검색의 결과를 내보내는 경우 내보낸 파일의 파일 이름이 수정 됩니다. 이 예에서 내보낸 문서의 파일 이름은  `FY2017Budget_DEAF727D-0478-4A7F-87DE-5487F033C81A2000-07-05T10-37-55.xlsx` 입니다.

    보류 중인 사이트의 문서가 수정 되 고 사이트의 문서 라이브러리에 대 한 버전 관리를 사용 하도록 설정한 경우 파일의 복사본이 보존 보류 라이브러리에 자동으로 만들어집니다. 이 경우에는 보존 보류 라이브러리에 복사 되는 문서의 파일 이름에 임의로 생성 되는 고유 ID도 추가 됩니다.

    보존 보류 라이브러리로 이동 되거나 복사 되는 문서의 파일 이름이 충돌 하는 것을 방지 하기 위한 이유는 다음과 같습니다. 사이트 및 보존 보류 라이브러리를 유지 하는 방법에 대 한 자세한 내용은 [SharePoint Server 2016의 원본 위치 유지 개요](https://support.office.com/article/5e400d68-cd51-444a-8fe6-e4df1d20aa95)를 참조 하세요.

### <a name="miscellaneous"></a>없으며
  
- 모든 검색 결과 및 내보내기 보고서는 콘텐츠 검색과 동일한 이름의 폴더에 포함됩니다. 내보낸 전자 메일 메시지는 **Exchange** 라는 폴더에 있습니다. 문서는 **SharePoint** 라는 폴더에 있습니다.

- SharePoint의 문서 및 비즈니스용 OneDrive 사이트에 대 한 파일 시스템 메타 데이터는 로컬 컴퓨터로 문서를 내보낼 때 유지 됩니다. 즉, 만든 날짜 및 마지막으로 수정한 날짜와 같은 문서 속성은 문서를 내보낼 때도 변경되지 않습니다.

- 검색 결과에 검색 쿼리와 일치 하는 SharePoint의 목록 항목이 포함 되어 있으면 목록에 있는 모든 행과 검색 쿼리와 일치 하는 항목 및 목록의 모든 첨부 파일이 내보내집니다. 이 동작은 검색 결과에서 반환 되는 목록 항목에 대 한 컨텍스트를 제공 하는 데 있습니다. 또한 추가 목록 항목 및 첨부 파일의 경우 내보낸 항목의 수가 검색 결과의 원래 예상 값과 다를 수 있습니다.
