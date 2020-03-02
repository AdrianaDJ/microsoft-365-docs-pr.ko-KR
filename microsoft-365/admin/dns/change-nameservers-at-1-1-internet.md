---
title: 이름 서버를 변경 하 여 Office 365을 설정 하 고 1&1gb 이상 OS
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 31efc571-c8b9-46fb-b42d-203c2fb25289
description: 1&인터넷이 DNS 호스팅 공급자 일 때 21Vianet에서 운영 하는 Office 365을 설정 하 여 DNS 레코드를 관리 하는 방법을 알아봅니다.
ms.openlocfilehash: 907e4fe097634d28ad44e4d44ba8c6ff2da9164d
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42246810"
---
# <a name="change-nameservers-to-set-up-office-365-with-11-ionos"></a>이름 서버를 변경 하 여 Office 365을 설정 하 고 1&1gb 이상 OS

 **원하는 정보는 찾지 못한 경우 [도메인 질문과 대답을 확인](../setup/domains-faq.md)** 하세요. 
  
Office 365에서 Office 365 DNS 레코드를 관리하도록 하려면 다음 지침을 따릅니다. 원하는 경우 [모든 Office 365 DNS 레코드를 1&1GB os)로 관리할](create-dns-records-at-1-1-internet.md)수 있습니다. 
  

    
## <a name="add-a-txt-record-for-verification"></a>확인을 위해 TXT 레코드 추가


Office 365에서 사용자 도메인을 사용하려면 먼저 도메인을 소유하고 있어야 합니다. 도메인 등록 기관에서 사용자의 계정으로 로그인하고 DNS 레코드를 만들 수 있으면 Office 365에 도메인을 소유하고 있음을 증명할 수 있습니다.
  
> [!NOTE]
> 이 레코드는 사용자가 도메인을 소유하고 있는지 확인하는 데만 사용되며 그 밖에 아무런 영향도 주지 않습니다. 원하는 경우 나중에 삭제할 수 있습니다. 
  
아래 단계를 따르거나 [비디오를 시청하세요(0:42에 시작)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-1-1-Internet-0ef1b3b5-d27a-4004-8ca1-fbe0453a0ea3?ui=en-US&amp;rs=en-US&amp;ad=US).
  
1. 시작 하려면 [이 링크](https://account.1and1.com/?redirect_url=https%3A%2F%2Fmy.1and1.com%2F)를 통해 1&1gb os의 도메인 페이지로 이동 합니다. You'll be prompted to log in. 
    
2. **내 도메인**아래에서 **도메인 관리**를 선택 합니다.
    
3. **Domain Center (도메인 센터** ) 페이지에서 업데이트 하려는 도메인을 찾습니다. 그런 다음 해당 도메인에 대 한 **패널** ( **v**) 컨트롤을 선택 합니다.
    
4. **도메인 설정** 영역에서 **DNS 설정 편집**을 선택 합니다.
    
5. **TXT 및 SRV 레코드** 섹션에서 **레코드 추가**를 선택 합니다.
    
    (You may have to scroll down.) 
    
6. In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
||||
|:-----|:-----|:-----|
|**종류** <br/> |**Prefix(접두사)** <br/> |**Name Value(이름 값)** <br/> |
|TXT  <br/> |(Leave this field empty.)  <br/> |MS=ms *XXXXXXXX* <br/> **참고**:이는 예입니다. 여기에는 Office 365의 표에 있는 특정 **대상 또는 주소 가리키기** 값을 사용합니다. [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md) <br/> |

   
7. **저장**을 선택한 다음 다시 **저장** 을 선택 합니다. 
    
8. **DNS 설정 편집** 대화 상자에서 **예**를 선택 합니다.
    
9. 방금 만든 레코드가 인터넷에서 업데이트될 수 있도록 몇 분 정도 기다립니다.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. 관리 센터에서 **설정** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">도메인</a> 페이지로 이동 합니다.
    
2. **도메인** 페이지에서 확인 하려는 도메인을 선택 합니다. 
    
3. **설정** 페이지에서 **설정 시작**을 선택 합니다.
    
4. **도메인 확인** 페이지에서 **확인**을 선택 합니다.
    
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. DNS 레코드를 추가한 후 메일 흐름 또는 기타 문제에 문제가 있는 경우 [Office 365에서 도메인 또는 DNS 레코드를 추가한 후 문제 찾기 및 해결](../get-help-with-domains/find-and-fix-issues.md)을 참조 하세요. 
  
## <a name="change-your-domains-nameserver-ns-records"></a>도메인의 NS(이름 서버) 레코드 변경

Office 365에서 도메인 설정을 완료하려면 도메인 등록 기관에서 도메인의 NS 레코드가 Office 365 기본 및 보조 이름 서버를 가리키도록 변경합니다. 이렇게 하면 Office 365가 사용자 대신 도메인의 DNS 레코드를 업데이트하도록 설정됩니다. 전자 메일, 비즈니스용 Skype Online, 공개 웹 사이트가 사용자의 도메인을 사용하도록 모든 레코드가 자동으로 추가되고 모든 설정이 완료됩니다.
  
> [!CAUTION]
> Office 365 이름 서버를 가리키도록 도메인 NS 레코드를 변경하면 현재 도메인에 연결되는 모든 서비스가 영향을 받습니다. 예를 들어 이 변경 내용을 적용하면 사용자의 도메인(예: rob@ *사용자_도메인*  .com)으로 보낸 전자 메일이 Office 365로 수신됩니다. 
  
Office 365에서 도메인을 설정할 수 있도록 NS 레코드를 변경할 준비가 되면 아래 단계를 따르거나 [비디오를 시청하세요(2:47에 시작)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-1-1-Internet-0ef1b3b5-d27a-4004-8ca1-fbe0453a0ea3?ui=en-US&amp;rs=en-US&amp;ad=US).
  
> [!IMPORTANT]
>  다음 절차에서는 목록에서 원치 않는 이름 서버를 삭제 하는 방법 및 올바른 이름 서버가 나열 되어 있지 않은 경우 추가 하는 방법을 보여 줍니다. >이 섹션의 단계를 완료 한 후에는 > ns1.bdm.microsoftonline.com > ns2.bdm.microsoftonline.com > ns3.bdm.microsoftonline.com > ns4.bdm.microsoftonline.com와 같은 4 가지 이름 서버를 나열 해야 합니다. 
  
1. 시작 하려면 [이 링크](https://account.1and1.com/?redirect_url=https%3A%2F%2Fmy.1and1.com%2F)를 사용 하 여 1&1gb os의 도메인 페이지로 이동 합니다. You'll be prompted to log in. 
    
2. **내 도메인**아래에서 **도메인 관리**를 선택 합니다.
    
3. **Domain Center (도메인 센터** ) 페이지에서 업데이트 하려는 도메인을 찾은 다음 해당 도메인에 대 한 **패널** ( **v**) 컨트롤을 선택 합니다.
    
4. **도메인 설정** 영역에서 **DNS 설정 편집**을 선택 합니다.
    
5. **이름 서버 설정** 구역에서 **다른 이름 서버**를 선택합니다.
    
    (아래로 스크롤해야 할 수 있습니다.)
    
6. 현재 표시된 페이지에 이름 서버가 이미 나열되어 있는지 여부에 따라 다음 두 가지 절차 중 하나를 계속합니다.
    
  - 이미 나열된 이름 서버가 **없으면**[나열된 이름 서버가 없으면](#if-there-are-no-nameservers-already-listed).
    
  - 이미 나열된 이름 서버가 **있으면**[이름 서버가 나열되어 있는 경우](#if-there-are-nameservers-already-listed).
    
### <a name="if-there-are-no-nameservers-already-listed"></a>나열된 이름 서버가 없으면

1. **이름 서버 1** 상자에서 다음 표의 값을 입력하거나 복사하여 붙여넣습니다. 
    
|||
|:-----|:-----|
|**이름 서버 1** <br/> |ns1.bdm.microsoftonline.com  <br/> |
   
   ![이름 서버 1 상자에 값 입력](../media/34509935-461f-427f-9796-c3cf840bd9be.png)
  
2. **다른 이름 서버** 드롭다운 목록에서 **내 보조 이름 서버**를 선택합니다.
    
    ![Choosing My secondary name servers in the list](../media/7eb14856-86da-45c2-910c-c72312250a18.png)
  
3. **이름 서버 2, 3, 4** 상자에서 다음 표의 값을 입력하거나 복사하여 붙여넣습니다. 
    
|||
|:-----|:-----|
|**이름 서버 2** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**이름 서버 3** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**이름 서버 4** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
    ![Entering name server values](../media/0f15880c-88b6-4133-8f31-62f0d98ee63f.png)
  
4. **저장**을 선택합니다.
    
    ![이름 서버 설정 페이지에서 저장 선택](../media/864f7927-7127-4784-b8d2-dadfea2f9dc8.png)
  
5. **DNS 설정 편집** 대화 상자에서 **예**를 선택 합니다.
    
    ![DNS 설정 편집 대화 상자에서 저장 선택](../media/0558e24c-17cd-428c-9ec1-5ed46481af7c.png)
  
> [!NOTE]
> 이름 서버 레코드 업데이트가 인터넷의 DNS 시스템 전체에 업데이트되기까지 몇 시간이 걸릴 수 있습니다. 그 후에는 Office 365 전자 메일 및 기타 서비스가 모두 사용자의 도메인을 사용하도록 설정됩니다. 
  
### <a name="if-there-are-nameservers-already-listed"></a>이름 서버가 나열되어 있는 경우

> [!CAUTION]
> 네 개의  *올바른*  이름 서버 외에 기존 이름 서버가 있는 경우에  *만*  다음 단계를 따릅니다(즉, 이름이 *ns1.bdm.microsoftonline.com*, *ns2.bdm.microsoftonline.com*, **ns3.bdm.microsoftonline.com** 또는 **ns4.bdm.microsoftonline.com** 이  **아닌**  현재 모든 이름 서버  **만**  삭제). 
  
1. **이름 서버** 상자에 이미 이름 서버가 나열되어 있으면 하나씩 선택한 후 키보드의 **Delete** 키를 눌러 삭제합니다. 
    
    ![Deleting name servers](../media/af0a68cc-b058-4925-b3b1-52dfded003c1.png)
  
2. **이름 서버 1, 2, 3, 4** 상자에서 다음 표의 값을 입력하거나 복사하여 붙여넣습니다. 
    
|||
|:-----|:-----|
|**이름 서버 1** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**이름 서버 2** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**이름 서버 3** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**이름 서버 4** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
   ![이름 서버 값 입력](../media/52826bd1-0596-4103-a728-d5d28b9610d2.png)
  
3. **저장**을 선택합니다.
    
    ![이름 서버 설정 페이지에서 저장 선택](../media/cd10e4fb-b7fa-480f-855b-a443f2705cf2.png)
  
4. **DNS 설정 편집** 대화 상자에서 **예**를 선택 합니다.
    
    ![DNS 설정 편집 대화 상자에서 저장 선택](../media/0558e24c-17cd-428c-9ec1-5ed46481af7c.png)
  
> [!NOTE]
> 이름 서버 레코드 업데이트가 인터넷의 DNS 시스템 전체에 업데이트되기까지 몇 시간이 걸릴 수 있습니다. 그 후에는 Office 365 전자 메일 및 기타 서비스가 모두 사용자의 도메인을 사용하도록 설정됩니다. 
  

