---
title: 예약에서 서비스 제공 정의
ms.author: kwekua
author: kwekuako
manager: scotv
audience: Admin
ms.topic: article
ms.service: bookings
localization_priority: Normal
ms.assetid: 4a1c391e-524f-48e0-bef8-185df3a9634b
description: 서비스 이름, 설명, 위치, 기간 및 가격 산정을 비롯 한 서비스 제공 정보를 입력 하기 위한 지침입니다. 또한 서비스를 제공 하도록 자격이 부여 된 직원에 게 태그를 지정할 수도 있습니다.
ms.openlocfilehash: 095188546c01149a793a478a3cbd5ac9fbeb5524
ms.sourcegitcommit: 7c0873d2a804f17697844fb13f1a100fabce86c4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2020
ms.locfileid: "47962540"
---
# <a name="define-your-service-offerings-in-bookings"></a>예약에서 서비스 제공 정의

Microsoft 예약에서 서비스 제공을 정의 하는 경우 서비스 이름, 설명, 위치 (사용자에 게 회의를 하거나 온라인 모임을 사용할 것인지 선택), 기간, 고객 및 직원에 대 한 기본 미리 알림, 서비스에 대 한 내부 참고 사항 및 가격 책정을 설정 합니다. 또한 서비스를 제공 하도록 자격이 부여 된 직원에 게 태그를 지정할 수도 있습니다. 그런 다음 고객은 회사 웹 사이트에 약속을 예약할 때 사용할 수 있는 약속 유형을 정확히 확인 하 고, 서비스를 제공 하려는 사용자 및 서비스 비용을 선택할 수 있습니다.

예약 페이지를 통해 서비스를 사용할 수 있는 경우 사용자가 보내는 전자 메일 확인 및 미리 알림에 사용자 지정 된 정보 및 Url을 추가할 수도 있습니다.

## <a name="create-the-service-details"></a>서비스 정보 만들기

1. [서비스 관리 페이지로](https://outlook.office.com/bookings/services) 이동 하 여 **서비스 추가**를 선택 합니다.

2. **서비스 이름**: 서비스의 이름을 입력 합니다. 일정 페이지의 드롭다운 메뉴에 표시 되는 이름입니다. 사용자가 일정 페이지에 약속을 수동으로 추가 하면이 이름이 여기에도 나타나며 셀프 서비스 페이지에 바둑판식으로 표시 됩니다.

3. **설명**: 입력 한 설명은 사용자가 셀프 서비스 페이지에서 정보 아이콘을 클릭할 때 표시 되는 내용입니다.

4. **기본 위치**:이 위치는 직원 및 고객에 대 한 확인 및 미리 알림 전자 메일에 표시 되는 것으로, 예약을 위해 만들어지는 일정 이벤트에 표시 됩니다.

5. **온라인 모임 추가**:이 설정은 교직원 구성원에 대 한 기본 클라이언트로 구성 하는 경우에 따라 팀 또는 Skype를 통해 각 약속에 대해 온라인 모임을 사용 하거나 사용 하지 않도록 설정 합니다.

    - 된

        - 예약에 고유한 팀 또는 Skype 모임에 대 한 링크는 직원 및 고객의 일정 및 전화 접속 정보와 함께 calendar 이벤트에 추가 됩니다.
        - 모임 참가 링크는 다음 예와 같이 모든 확인 및 미리 알림 전자 메일에 추가 됩니다.

        :::image type="content" source="media/bookings-teams-meeting-link.jpg" alt-text="예약에서 팀 모임 참가 링크의 예":::

        > [!NOTE]
        > 팀 회의는 팀 모바일 앱, 팀 데스크톱 응용 프로그램, 웹 브라우저 또는 전화 전화 접속을 통해 참가할 수 있습니다. 가상 약속을 가장 효율적으로 예약 하려면 테 넌 트에 대 한 기본 온라인 모임 서비스로 팀을 사용 하도록 설정 하는 것이 좋습니다.

    - 있지
        - 약속에는 모임 옵션이 포함 되지 않으며, **온라인 모임 추가** 가 사용 하도록 설정 되어 있을 때 나타나는 모든 모임 관련 필드는 표시 되지 않습니다.

6. **기본 기간**: 모든 모임이 예약 되는 시간입니다. 시간은 예약 중에 선택 되는 시작 시간부터 차단 됩니다. 직원의 일정에서 전체 약속 시간이 차단 됩니다.

7. **버퍼링 시간 고객이 책을 사용할 수 없음**:이 설정을 사용 하면 약속을 예약할 때마다 직원의 일정에 추가 시간을 추가할 수 있습니다.

    시간은 직원의 일정 및 약속 있음/없음 정보에 대해 차단 됩니다. 즉, 약속이 오후 3:00 시에 종료 되 고 10 분의 버퍼 시간이 모임 끝에 추가 되 면 직원의 일정은 약속 있음/없음, 3:10 시까지 사용할 수 있는 약속이 없는 것으로 표시 됩니다. 이 기능은 환자 차트에 대 한 의사 검토 또는 관련 계정 정보를 준비 하는 재무 관리자와 같이 직원에 게 준비 해야 하는 시간이 필요한 경우에 유용할 수 있습니다. 다른 위치로 이동 하는 데 시간이 필요한 경우와 같이 모임 후에도 유용 하 게 사용할 수 있습니다.

8. **고객에 게 예약을 관리할 수 있도록**합니다 .이 설정은 예약 웹 앱의 일정 탭을 통해 예약 된 것으로 확인 된 고객을 결정 합니다.

    - 된

        **예약 관리** 단추가 고객 확인 전자 메일에 표시 됩니다. 고객이이 단추를 선택 하면 세 가지 옵션이 나타납니다.
        - **일정** 변경 이 옵션을 선택 하면 사용자가 서비스 관련 셀프 서비스 페이지가 되며,이 페이지에서 동일한 서비스에 대해 새 시간 및/또는 날짜를 선택 하 고 원래 예약에서 동일한 교직원 구성원을 선택할 수 있습니다. 원래 교직원 구성원은 기본적으로 일정 다시 예약에 첨부 되지만 직원 구성원을 변경할 수도 있습니다.
        - **예약 취소** 이렇게 하면 예약이 취소 되 고 직원의 일정에서 해당 일정이 제거 됩니다.
        - **새 예약** 이 옵션은 새 예약을 예약 하기 위해 나열 된 모든 서비스 및 직원과 함께 셀프 서비스 페이지를 사용자에 게 제공 합니다.

        :::image type="content" source="media/bookings-manage-booking-button.jpg" alt-text="예약의 예약 관리 단추":::

        셀프 서비스 페이지에 액세스 하는 고객에 게 익숙한 경우에만이 설정을 사용 하도록 설정 하는 것이 좋습니다.

    - 있지

        사용자는 예약 웹 앱의 일정 탭에서 예약할 때 예약을 다시 예약 하거나 취소할 수 없습니다. 그러나 셀프 서비스 페이지를 통해 예약 하는 경우에도이 설정을 사용 하지 않도록 설정 해도 고객은 **예약 관리** 단추와 모든 옵션을 계속 유지 합니다.

        셀프 서비스 페이지에 대 한 액세스를 제한 하려면이 설정을 사용 하지 않도록 설정 하는 것이 좋습니다. 또한 office를 호출 하거나 지원 센터에 전자 메일을 보내는 등 다른 방법으로 예약을 변경 하는 방법을 고객에 게 안내 하는 텍스트를 확인 및 미리 알림 전자 메일에 추가 하는 것이 좋습니다.

9. **이벤트 당 최대 참석자** 수 이 설정을 사용 하면 여러 사용자가 동일한 약속 시간 및 동일한 직원 (예: 적합성 클래스)을 예약할 수 있는 기능을 필요로 하는 서비스를 만들 수 있습니다. 선택한 서비스, 직원 및 시간에 대 한 약속 시간 슬롯은 사용자가 지정 하는 최대 참석자 수에 도달할 때까지 책에 제공 될 예정입니다. 현재 약속 용량 및 참석자는 예약 웹 앱의 일정 탭에서 볼 수 있습니다.

    :::image type="content" source="media/bookings-maximum-attendees.jpg" alt-text="예약에서 최대 참석자를 설정 하는 예제":::

10. **기본 가격**  셀프 서비스 페이지에 표시 되는 가격입니다. **가격이 설정 되지 않은** 경우 비용 또는 가격 산정에 대 한 가격이 나 참조가 표시 되지 않습니다.

11. **참고 사항** 이 필드는 예약 된 직원에 대 한 예약 이벤트 뿐만 아니라 일정 탭에 표시 되는 이벤트에도 표시 됩니다.

12. **사용자 정의 필드** 이 섹션에서는 고객이 책을 성공적으로 사용 하기 위해 답을 받아야 하는 경우 질문을 추가 하거나 제거할 수 있습니다.

    - 고객 전자 메일, 전화 번호, 주소 및 메모는 이동식이 아닌 필드 이지만 각 필드 옆에 있는 **필수** 선택을 취소 하 여 선택적으로 만들 수 있습니다.

    - **질문 추가**를 선택 하 여 여러 선택 또는 텍스트 응답 질문을 추가할 수 있습니다.

        사용자 정의 필드는 특정 약속이 예약 될 때마다 필요한 정보를 수집할 때 유용할 수 있습니다. 이 예에는 클리닉 방문 이전의 보험 공급자, 대출에 대 한 대출 유형, 교육에 대 한 consultations, 지원자 인터뷰에 대 한 신청자 ID 등이 포함 됩니다.

13. **미리 알림 및** 확인 두 유형의 전자 메일은 모두 고객, 직원 구성원 또는 둘 다에 게 약속 이전에 지정 된 기간에 전송 됩니다. 사용자의 기본 설정에 따라 각 약속에 대해 여러 메시지를 만들 수 있습니다.

    - 기본 확인 및 미리 알림 전자 메일에는 고객/클라이언트 이름, 스태프 구성원 이름, 예약 된 서비스 또는 약속과 같은 약속에 대 한 기본 정보가 포함 되어 있습니다. 온라인 모임의 경우 연결에 대 한 연결도 포함 됩니다. 이 설정을 사용 하는 경우 (8 단계에서 설명한 대로) 예약을 관리 하는 기능이 포함 될 수도 있습니다.

        :::image type="content" source="media/bookings-remind-confirm.jpg" alt-text="예약에서 받은 확인 전자 메일":::

    - 필요에 따라 일정 재조정에 대 한 정보 또는 고객이 약속을 위해 가져와야 하는 고객에 대 한 정보와 같이 원하는 추가 텍스트를 포함할 수 있습니다. 다음은 **전자 메일 확인에 대 한 추가 정보** 필드에 표시 된, 원래 확인 전자 메일에 추가 된 사용자 지정 텍스트의 예입니다.

        :::image type="content" source="media/bookings-additional-info.jpg" alt-text="예약 전자 메일의 추가 정보":::

14. **고객에 대해 문자 메시지 알림 사용** 선택 하는 경우 SMS 메시지가 고객에 게 전송 됩니다 (옵트인 인 경우에만 해당).

    - 수동 예약 및 셀프 서비스 페이지의 옵트인 상자:

        :::image type="content" source="media/bookings-opt-In-boc.jpg" alt-text="예약의 옵트인 상자":::

    - SMS 알림은 현재 북미 에서만 사용할 수 있는 것 처럼 문자 메시지 알림이 다음과 같이 표시 됩니다.

        :::image type="content" source="media/bookings-text-notifications.jpg" alt-text="예약의 텍스트 알림":::

15. **게시 옵션** 이 서비스가 해당 서비스를 셀프 서비스 페이지에 표시할지 여부를 선택 하거나, 서비스를 예약 웹 앱 내의 일정 탭 에서만 사용할 수 있도록 합니다.

16. **예약 정책** 이 설정은 약속 시간을 표시 하는 방법 및 예약을 만들거나 취소할 수 있는 기간을 결정 합니다.

17. **전자 메일 알림** 전자 메일이 조직 직원과 고객 또는 클라이언트에 게 전송 되는 시기를 설정 합니다.

18. **직원** 이 확인란을 선택 하면 고객 또는 클라이언트가 약속에 대 한 특정 교직원 구성원을 선택할 수 있습니다.

    - 된

        고객은 셀프 서비스 페이지에서 예약 될 때 약속에 할당 된 모든 직원을 선택할 수 있습니다. **모든 사용자** 의 예약 옵션을 선택 하면 약속에 할당할 수 있는 사용 가능한 스태프 구성원이 무작위로 선택 됩니다.

    - 있지

        셀프 서비스 페이지를 통해 예약 된 고객은 서비스와 시간 및 날짜를 선택할 수 있습니다. 사용 가능한 직원은 임의로 예약 됩니다. 예약 웹 앱의 일정 탭에서 예약할 경우에도 특정 직원을 선택할 수 있습니다.

19. **가용성** 다음 옵션은 서비스를 예약할 수 있는 시기를 결정 합니다.

    - **직원이 무료 인 경우에 사용할 수 있는 bookable 서비스는 직원 들이 업무 시간 내에 약속 없는 시간을 기준으로 가용성을 유지 관리 합니다.**

    - **사용자 지정 시간 (매주 되풀이)** 이 서비스에는 업무 시간 또는 직원 시간을 제한 하는 것 외에 추가로 제한 될 수 있는 가용성 계층이 추가 되었습니다. 서비스를 특정 시간에만 제공 하거나 수행할 수 있도록 하려면이 옵션을 사용 합니다.

    - **날짜 범위에 대해 다른 가용성 설정** 이 설정은 반복 되는 것이 아니라 특정 시점에서 가용성에 영향을 줍니다. 예를 들어 서비스에 필요한 컴퓨터를 일시적으로 서비스를 제공 하 고 사용할 수 없는 경우 또는 휴일에 대해 조직을 닫은 경우에이 방법을 사용할 수 있습니다.

20. **직원 할당** 직원에 게 해당 특정 서비스에 사용할 수 있는 직원을 선택 합니다. 개별 직원을 선택 하지 않으면 모든 직원이 서비스에 할당 됩니다.