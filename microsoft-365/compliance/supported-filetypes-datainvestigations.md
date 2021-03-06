---
title: 데이터 조사에서 지원 되는 파일 형식 (미리 보기)
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
description: 지원 되는 파일 형식 및 데이터 조사 (미리 보기)에 대해 볼 수 있는 뷰어를 나열 하는 표
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 826ad69b1fb0074cd0c8bc1b3b0208bb8e77d528
ms.sourcegitcommit: 153f413402f93b79be421741f3b9fed318d6d270
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48600417"
---
# <a name="supported-file-types-in-data-investigations-preview"></a>데이터 조사에서 지원 되는 파일 형식 (미리 보기)

데이터 조사 (미리 보기) 도구는 다음과 같은 여러 가지 방식으로 다양 한 파일 형식을 지원 합니다. 이 목록은 마무리 되지 않으며 유효성 검사 테스트를 계속할 때 새 파일 형식을 추가 합니다. 또한 증거를 검토할 때 사용할 수 있는 보기에서 파일 형식을 볼 수 있는지 여부도이 표에 나와 있습니다.

| Mime 형식 | File 클래스 | 네이티브 뷰어 | 텍스트 뷰어 | 주석 달기 보기 | 컨테이너 추출 | Extensions |
|:------|:------|:------|:------|:------|:------|:------|
|application/msword | 문서 | 예 | 예 | 예 | 아니요 | .doc; .dat |
|application/pdf | 문서 | 예 | 예 | 예 | 아니요 | .pdf |
|application/rtf | 문서 | 예 | 예 | 예 | 아니요 | .rtf; .doc |
|application/vnd | 문서 | 예 | 예 | 예 | 아니요 | .xls; .dat |
|application/vnd macroenabled. 12 | 생산성/열린 문서 형식 | 예 | 예 | 아니요 | 아니요 | .xlsb |
|application/vnd macroenabled. 12 | 문서 | 예 | 예 | 예 | 아니요 | .xlsm |
|application/vnd macroenabled. 12 | 생산성/열린 문서 형식 | 아니요 | 예 | 아니요 | 아니요 | . .xltm |
|application/vnd | 생산성 | 아니요 | 아니요 | 아니요 | 아니요 | .msg |
|application/vnd | 생산성/공동 작업 | 아니요 | 아니요 | 아니요 | 예 | .pst |
|application/vnd | 문서 | 예 | 예 | 예 | 아니요 | .ppt; .pps; .pot |
|응용 프로그램/vnd.ms-word.document macroenabled. 12 | 문서 | 예 | 예 | 예 | 아니요 | .docm |
|application/vnd macroenabled. 12 | 문서 | 예 | 예 | 예 | 아니요 | normal.dotm |
|응용 프로그램/vnd. 텍스트 | 문서 | 예 | 예 | 예 | 아니요 | odt  |
|응용 프로그램/vnd presentationml presentation | 문서 | 예 | 예 | 예 | 아니요 | .pptx |
|응용 프로그램/vnd. presentationml | 생산성/열린 문서 형식 | 예 | 예 | 예 | 아니요 | . ppsx |
|application/vnd. presentationml | 문서 | 예 | 예 | 예 | 아니요 | . potx |
| apadsheetml | 문서 | 예 | 예 | 예 | 아니요 | .xlsx |
|application/vnd. spreadsheetml | 문서 | 예 | 예 | 예 | 아니요 | . .xltx |
|응용 프로그램/vnd.openxmlformats-officedocument.wordprocessingml.document | 문서 | 예 | 예 | 예 | 아니요 | .docx |
|application/vnd. wordprocessingml | 문서 | 예 | 예 | 예 | 아니요 | . dotx |
|응용 프로그램/vnd. visio | 문서 | 예 | 예 | 예 | 아니요 | .vsd |
|application/x-y-7z-압축 | 보관/컨테이너 | 아니요 | 아니요 | 아니요 | 예 | .7z |
|응용 프로그램/xhtml + xml | 문서 | 예 | 예 | 예 | 아니요 | . xhtml |
|application/xml | 문서 | 예 | 예 | 예 | 아니요 | .xml |
|응용 프로그램/x-msaccess.exe | 문서 | 예 | 예 | 예 | 아니요 | .mdb |
|응용 프로그램/x-mspublisher | 문서 | 예 | 예 | 예 | 아니요 | .pub |
|응용 프로그램/x-rar-압축 | 보관/컨테이너 | 아니요 | 아니요 | 아니요 | 예 | rar |
| 응용 프로그램/우편 번호 | 보관/컨테이너 | 아니요 | 아니요 | 아니요 | 예 | .zip |
|image/bmp | 이미지 | 예 | 예 | 예 | 아니요 | .bmp |
|image/emf | 이미지 | 예 | 예 | 예 | 아니요 | .emf |
|이미지/gif | 문서 | 예 | 예 | 예 | 아니요 | .gif |
|image/jpeg | 이미지 | 예 | 예 | 예 | 아니요 | .jpg; .jpeg; .dat; jpgt |
|이미지/png | 이미지 | 예 | 예 | 예 | 아니요 | .png |
|이미지/tiff | 이미지 | 예 | 예 | 예 | 아니요 | .tif |
|image/vnd | 문서 | 예 | 예 | 예 | 아니요 | dwg; dxf; |
|image/wmf | 문서 | 예 | 예 | 예 | 아니요 | .wmf |
| message/rfc822-headers | 생산성/공동 작업 | 아니요 | 아니요 | 아니요 | 아니요 | .eml |
|text/csv | 문서 | 예 | 예 | 예 | 아니요 | .csv |
|텍스트/html | 문서 | 예 | 예 | 예 | 아니요 | .html; shtml.dll; .htm |
|텍스트/일반 | 문서 | 예 | 예 | 예 | 아니요 | .txt; .css; con, pl; .csv; .dat |
|텍스트/vcard-연락처 | 문서 | 예 | 예 | 예 | 아니요 | .vcf |
||||||||
