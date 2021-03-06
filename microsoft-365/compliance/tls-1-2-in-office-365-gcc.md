---
title: 방식 TLS 1.0 및 1.1 in Office 365 GCC High 및 DoD
description: Microsoft가 Office 365의 GCC High 및 DoD 환경에서 TLS 1.1 및 1.0에 대 한 지원을 중단 하 고 TLS 1.2 사용을 준비 하는 방법에 대해 설명 합니다.
author: workshay
manager: laurawi
localization_priority: Normal
search.appverid:
- MET150
audience: ITPro
ms.collection: M365-security-compliance
ms.service: information-protection
ms.topic: article
ms.reviewer: krowley
ms.author: shmehta
appliesto:
- Office 365 Business
ms.openlocfilehash: 76e9b203e58ba7fa23942ea42810456e3bee377d
ms.sourcegitcommit: 42b618231e9f608f3ae7226a313b0366601d0ea2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45158883"
---
# <a name="deprecating-tls-10-and-11-in-office-365-gcc-high-and-dod"></a>방식 TLS 1.0 및 1.1 in Office 365 GCC High 및 DoD

## <a name="summary"></a>요약

FedRAMP (미 연방 위험 및 권한 부여 관리 프로그램)에 대 한 최신 준수 표준을 준수 하기 위해 방식은 GCC High 및 DoD 환경에 대해 Microsoft Office 365에서 TLS (전송 계층 보안) 버전 1.1 및 1.0를 제공 합니다. 이 변경 사항에 [대 한 자세한 내용을 보려면 Office 365에서 TLS 1.2의 필수 사용을 준비 하기 위한](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)Microsoft 지원 서비스를 통해 이전에 발표 되었습니다.

데이터 보안은 중요 하며, 서비스 사용에 영향을 줄 수 있는 변경 사항에 대 한 투명성을 반영 합니다.

[MICROSOFT TLS 1.0 구현](https://support.microsoft.com/help/3117336) 에는 알려진 보안 취약점이 없더라도 FedRAMP 준수 표준에 대 한 커밋된 상태로 유지 됩니다. 따라서 사용 중지는 GCC High 및 DoD 환경에서 2020, 1 월 15 일에 시작 하는 TLS 1.1 및 365 1.0을 제공 합니다. TLS 1.1 및 1.0 종속성을 제거 하는 방법에 대 한 자세한 내용은 다음 백서를 참조 하십시오.

[TLS 1.0 문제 해결](https://www.microsoft.com/download/details.aspx?id=55266)

TLS 1.1 및 1.0에 대 한이 변경 내용을 준비할 때는 대신 TLS 버전 1.2을 사용 하는 것이 좋습니다. 자세한 내용은 [Office 365에서 TLS 1.2의 필수 사용 준비](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)를 참조 하세요.

## <a name="more-information"></a>추가 정보

2020 년 1 월 15 일부터 시작 하 여 GCC High 및 DoD 환경에서 Office 365을 사용 중지 TLS 1.1 및 1.0이 발생 합니다.

2020 년 1 월 15 일까 지, 클라이언트 서버와 브라우저 서버의 모든 조합은 TLS 버전 1.2 (이상 버전)를 사용 하 여 Office 365 서비스에 문제가 없는 모든 연결을 설정할 수 있는지 확인 해야 합니다. 이렇게 하려면 클라이언트 서버 및 브라우저 서버의 특정 조합에 대 한 업데이트를 수행 해야 할 수 있습니다.

TLS 버전 1.2 이상 버전의 1 월 2020 15 일을 업데이트 하지 않으면 Office 365에 연결 하려고 할 때 문제가 발생 합니다. 또한 해결의 일부로 TLS 1.2 이상 버전으로 업데이트 해야 합니다.

다음 클라이언트는 TLS 1.2를 사용할 수 없습니다.

- Android 4.3 이하 버전
- Firefox 5.0 이하 버전
- Windows 7 및 이전 버전의 Internet Explorer 8 – 10
- Windows Phone 8.0의 Internet Explorer 10
- Safari 6.0.4/OS X 10.8.4 및 이전 버전

Office 365 GCC High 및 DoD에 대 한 중단 된 액세스를 유지 관리할 수 있도록 클라이언트를 업데이트 하는 것이 좋습니다.

Microsoft Online services에 대 한 연결을 분석 하 여 대부분의 서비스 및 끝점이 아주 작은 TLS 1.1 및 1.0 사용을 확인 하지만, TLS 1.1 및 1.0에 대 한 지원을 위해 필요에 따라 영향을 받는 클라이언트나 서버를 업데이트할 수 있도록이 변경 사항에 대 한 통지를 제공 하 고 있습니다. 하이브리드 시나리오 또는 AD FS (Active Directory Federation Services)에 대해 온-프레미스 인프라를 사용 하는 경우, 인프라에서 TLS 1.2 이상 버전을 사용 하는 인바운드 및 아웃 바운드 연결을 모두 지원할 수 있는지 확인 합니다.

TLS 1.2를 사용할 수 없는 나열 된 클라이언트를 사용 하는 경우 발생할 수 있는 중단 외에도 TLS 1.1 및 1.0를 제거 하면 다음 Microsoft 제품을 사용할 수 없습니다.

- Lync 전화

## <a name="references"></a>참조

다음 지원 문서에서는 클라이언트가 TLS 1.2을 사용 하 고 있는지 확인 하는 데 도움이 되는 지침 및 참조에 대해 설명 합니다.

[Office 365에서 TLS 1.2의 필수 사용 준비](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)
