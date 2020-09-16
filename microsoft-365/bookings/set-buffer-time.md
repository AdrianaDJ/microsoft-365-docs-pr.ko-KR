---
title: Microsoft 예약에서 버퍼 시간 설정
ms.author: kwekua
author: kwekuako
manager: scotv
audience: Admin
ms.topic: article
ms.service: bookings
localization_priority: Normal
ms.assetid: 271f43e4-b8f7-4d63-8059-b5747679bb7e
description: 장비를 청소 하거나 다시 설정할 시간을 허용 하기 위해 Microsoft 예약에서 약속 전후에 버퍼 시간을 설정 합니다.
ms.openlocfilehash: dceb777f9ddba9f1ddabfee00608813afae57a86
ms.sourcegitcommit: 41fd71ec7175ea3b94f5d3ea1ae2c8fb8dc84227
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2020
ms.locfileid: "47419926"
---
# <a name="set-buffer-time-in-microsoft-bookings"></a>Microsoft 예약에서 버퍼 시간 설정

일부 약속은 고객과 회의를 하 여 회의실 및 장비를 설정, 정리 또는 다시 설정 하기 위해 몇 시간이 걸릴 수 있습니다. 또는 고객 약속 간의 이동에 대 한 작업을 수행 하는 경우에는 사용자와 팀이 고객을 대기 시 키 지 않고 약속 간을 이동할 수 있도록 해야 할 수 있습니다.

약속을 시작 하기 전, 약속 끝까지 또는 둘 다에 대해 버퍼 시간을 설정 하 여 직원 들이 다음 약속을 준비 하는 데 필요한 추가 시간을 제공할 수 있습니다.

> [!NOTE]
> Microsoft 365 Business Standard, Microsoft 365 A3 또는 Microsoft 365 A5 구독이 있는 고객의 경우 기본적으로 예약이 설정 됩니다. Office 365 Enterprise E3 및 Office 365 Enterprise E5가 있는 고객 에게도 예약을 사용할 수 있지만 기본적으로이 기능은 해제 되어 있습니다. 시작 하려면 [Microsoft 예약에 대 한 get 액세스](get-access.md)를 참조 하세요. 예약을 설정 하거나 해제 하려면 [조직에 대해 예약 설정 또는 해제](turn-bookings-on-or-off.md)를 참조 하세요.

## <a name="set-buffer-time-defaults"></a>버퍼 시간 기본값 설정

버퍼링 시간 기본값은 예약의 **서비스 세부 정보** 페이지에서 설정 됩니다. 이 페이지에 설정 된 모든 서비스 기본값과 마찬가지로, 이러한 기본값은 특정 고객 요구를 충족 하기 위해 특정 예약을 위해 편집할 수 있습니다.

버퍼 시간 설정은 **서비스 세부 정보** 페이지의 **기본 기간** 선택 바로 아래에서 찾을 수 있습니다. 지정한 서비스에 대해 설정 하려면 먼저 버퍼 시간 설정을 선택 해야 합니다. 이렇게 하면 다음과 같이 각 예약 전후에 보존 되는 기본 시간을 선택 하는 데 사용 되는 **before** 및 **after** 드롭다운이 표시 됩니다.

   ![버퍼링 시간을 사용 하는 예약 이미지](../media/bookings-buffertime.png)

## <a name="buffer-time-and-appointment-timing"></a>버퍼링 시간 및 약속 타이밍

고객이 사용자를 만날 때 혼란을 방지 하기 위해 예약에서는 버퍼 시간과 실제 약속 시간 (고객이 사용자에 게 기대 하는 시간)과 관련 직원에 대 한 전자 메일 확인 및 미리 알림을 표시 합니다. 예를 들어 다음은 약속이 있는 약속에 대해 예약에서 제공 하는 일정 중에서 15 분 동안의 약속 없는 시간을 포함 하는 것입니다.

이벤트 자체 (아래 이미지의 왼쪽에)에는 실제 고객 약속의 버퍼 시간 및 더 어두운 음영에 대 한 더 밝은 음영이 표시 됩니다. 통화 제한 (이벤트를 선택할 때 열리는 약속)은 약속 시간이 9:00AM이 고 약속 보다 15 분이 지난 5 분이 포함 되어 있다는 것을 명시 합니다. 담당자에 대 한 확인 및 미리 알림 또한 고객은 특정 버퍼 및 약속 시간을 참조 하 고 9:00AM에서 10까지를 참조 하는 확인 및 미리 알림이 제공 되는 경우도 있습니다.

   ![버퍼 시간이 표시 된 예약 약속 통화 아웃 이미지](../media/bookings-buffertime-callout.png)

## <a name="buffer-time-and-availability"></a>버퍼 시간 및 가용성

고객이 설정한 버퍼 시간을 직접 확인 하 여 변경할 수 없습니다. 그러나 버퍼 시간이 전체 서비스 기간을 계산 하는 데 사용 되므로 고객은 사용자와 관련 직원이 버퍼 및 일반 약속 시간 중에 예약 된 상태로 표시 됩니다. 또한 고객은 약속 및 해당 버퍼 시간에 모두 시간이 충분 한 경우에만 사용 가능 여부와 직원을 볼 수 있습니다.

예를 들어, 15 분 동안의 약속 이전 버퍼링 시간이 있는 1 시간 약속에는 최소 1 시간 및 15 분의 사용 가능한 시간 블록이 필요 합니다. 따라서이 서비스의 약속을 사용 하 여 일정에 75 분의 시간을 채우고, 충돌 없이 75 분의 가용성이 통합 문서에 포함 되도록 해야 합니다.