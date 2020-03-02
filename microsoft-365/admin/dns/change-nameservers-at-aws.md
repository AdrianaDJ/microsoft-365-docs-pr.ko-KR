---
title: AWS(Amazon Web Services)에서 이름 서버를 변경하여 Office 365 설정
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
ms.assetid: 0ddbe33c-81ea-4c02-8db9-e71d3810c0ec
description: 'AWS (Amazon Web Services)에서 DNS 레코드를 관리 하기 위해 Office 365을 설정 하는 방법을 알아봅니다. '
ms.openlocfilehash: 08deba83738ba0e530e719cd6fd57bee423df5e0
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42246763"
---
# <a name="change-nameservers-to-set-up-office-365-with-amazon-web-services-aws"></a>AWS(Amazon Web Services)에서 이름 서버를 변경하여 Office 365 설정

 **원하는 정보는 찾지 못한 경우 [도메인 질문과 대답을 확인](../setup/domains-faq.md)** 하세요. 
  
Office 365에서 Office 365 DNS 레코드를 관리하려는 경우 다음 지침을 따릅니다. 원하는 경우 [모든 Office 365 DNS 레코드를 AWS에서 관리](create-dns-records-at-aws.md)할 수 있습니다.
  
    
## <a name="add-a-txt-record-for-verification"></a>확인을 위해 TXT 레코드 추가

Office 365에서 사용자 도메인을 사용하려면 먼저 도메인을 소유하고 있어야 합니다. 도메인 등록 기관에서 사용자의 계정으로 로그인하고 DNS 레코드를 만들 수 있으면 Office 365에 도메인을 소유하고 있음을 증명할 수 있습니다.
  
> [!NOTE]
> 이 레코드는 사용자가 도메인을 소유하고 있는지 확인하는 데만 사용되며 그 밖에 아무런 영향도 주지 않습니다. 원하는 경우 나중에 삭제할 수 있습니다. 
  
1. 시작하려면 [이 링크](https://console.aws.amazon.com/route53/home)를 사용하여 AWS의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
2. **리소스** 페이지에서 **호스트 된 영역**을 선택 합니다.
    
3. **호스팅된 영역** 페이지의 **Domain Name (도메인 이름** ) 열에서 편집 하려는 도메인의 이름을 선택 합니다. 
    
4. **레코드 집합 만들기**를 선택 합니다.
    
5. In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Choose the **Type** and **Routing Policy** values from the drop-down lists.) 
    
    > [!TIP]
    > The quotation marks required by the onscreen instructions are supplied automatically. You don't need to type them manually. 
  
|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
|**이름** <br/> |**종류** <br/> |**별칭** <br/> |**TTL(초)** <br/> |**값** <br/> |**라우팅 정책** <br/> |
|(이 필드는 비워 둡니다.)  <br/> |TXT - Text  <br/> |아니요  <br/> |300  <br/> |MS=ms *XXXXXXXX* <br/> **참고:** 예를 들면 다음과 같습니다. 여기에는 Office 365의 표에 있는 특정 **대상 또는 주소 가리키기** 값을 사용합니다. [이 값을 찾는 방법](../get-help-with-domains/information-for-dns-records.md)  <br/>  |Simple(단순형) <br/> |
   
6. **만들기**를 선택합니다.
    
7. 방금 만든 레코드가 인터넷에서 업데이트될 수 있도록 몇 분 정도 기다립니다.
    
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
  
> [!IMPORTANT]
>  다음 절차에서는 목록에서 원치 않는 이름 서버를 삭제 하는 방법 및 올바른 이름 서버가 나열 되어 있지 않은 경우 추가 하는 방법을 보여 줍니다. >이 섹션의 단계를 완료 한 후에는 > ns1.bdm.microsoftonline.com > ns2.bdm.microsoftonline.com > ns3.bdm.microsoftonline.com > ns4.bdm.microsoftonline.com와 같은 4 가지 이름 서버를 나열 해야 합니다. 
  
1. 시작하려면 [이 링크](https://console.aws.amazon.com/route53/home)를 사용하여 AWS의 도메인 페이지로 이동합니다. 먼저 로그인하라는 메시지가 표시됩니다.
    
2. **리소스** 페이지에서 **호스트 된 영역**을 선택 합니다.
    
3. **호스팅된 영역** 페이지의 **Domain Name (도메인 이름** ) 열에서 편집 하려는 도메인의 이름을 선택 합니다. 
    
4. **이름 서버** 레코드 집합을 선택합니다. 
    
    ![Select the recordset](../media/24e618e4-0a16-43a2-9886-f4f5dac79374.png)
  
5. **NS - Name server(NS - 이름 서버)** 레코드 집합의 **Value(값)** 상자에서 모든 이름 서버를 선택한 다음 키보드의 **Delete** 키를 눌러 모든 이름 서버를 삭제합니다. 
    
    > [!CAUTION]
    > Follow these steps only if you have existing nameservers other than the four correct nameservers. (즉, **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**또는 **ns4.bdm.microsoftonline.com**로 이름이 지정 *되지* 않은 현재 이름 서버 삭제 합니다.) 
  
    ![Select and delete all of the nameservers in the Value box](../media/ecf1e897-fa7d-4abc-b00b-bf55b8ed2139.png)
  
6. **TTL (초):** 영역에서 **1H** (1 시간)을 선택 합니다. 
    
    ![1 시간 동안 1H 선택](../media/c70070e1-4bde-41a7-b271-9d22c475edf6.png)
  
7. 계속해서 **NS - Name server**(NS - 이름 서버) 레코드 집합의 **Value**(값) 상자에 다음 표의 **First line**(첫 줄)에 있는 값을 입력하거나 복사하여 붙여넣고 키보드의 **Enter** 키를 누른 후 다음 **line**(줄)에 있는 값을 입력하거나 복사하여 붙여넣습니다. 
    
    > [!IMPORTANT]
    > 이름 서버 값은 다음 그림과 같이 *Value(값)* 상자 안의 각기 다른 줄에  **있어야 합니다**  . 
  
|||
|:-----|:-----|
|**첫 줄** <br/> |ns1.bdm.microsoftonline.com  <br/> **This value MUST end with a period (.)** <br/> |
|**둘째 줄** <br/> |ns2.bdm.microsoftonline.com  <br/> **This value MUST end with a period (.)** <br/> |
|**셋째 줄** <br/> |ns3.bdm.microsoftonline.com  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |
|**넷째 줄** <br/> |ns4.bdm.microsoftonline.com  <br/> **이 값은 마침표(.)로 끝나야 합니다.** <br/> |
   
   ![값 상자에 첫 번째 줄 값 입력 또는 붙여넣기](../media/b63f41e0-51ef-4ab2-a4b8-ee7380e5ab35.png)
  
8. **레코드 집합 저장**을 선택 합니다.
    
    ![레코드 집합 저장을 선택 합니다.](../media/ab3c0558-bb7c-41e4-871e-ea82f1553476.png)
  
> [!NOTE]
> 이름 서버 레코드 업데이트가 인터넷의 DNS 시스템 전체에 업데이트되기까지 몇 시간이 걸릴 수 있습니다. 그 후에는 Office 365 전자 메일 및 기타 서비스가 모두 사용자의 도메인을 사용하도록 설정됩니다. 