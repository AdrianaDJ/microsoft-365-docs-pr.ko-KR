---
title: 고가용성 페더레이션 인증 3 단계 AD FS 서버 구성
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/25/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- Ent_Solutions
- seo-marvel-apr2020
ms.assetid: 202b76ff-74a6-4486-ada1-a9bf099dab8f
description: Microsoft Azure에서 Microsoft 365에 대 한 고가용성 페더레이션 인증을 위해 AD FS 서버를 만들고 구성 하는 방법에 대해 알아봅니다.
ms.openlocfilehash: bf8b52f4cd0dead0c264b71363fd5248397ae88d
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692904"
---
# <a name="high-availability-federated-authentication-phase-3-configure-ad-fs-servers"></a><span data-ttu-id="35c74-103">고가용성 페더레이션 인증 3단계: AD FS 서버 구성</span><span class="sxs-lookup"><span data-stu-id="35c74-103">High availability federated authentication Phase 3: Configure AD FS servers</span></span>

<span data-ttu-id="35c74-104">Azure 인프라 서비스에서 Microsoft 365 페더레이션 인증을 위해 고가용성을 배포 하는이 단계에서는 내부 부하 분산 장치 및 두 개의 AD FS 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-104">In this phase of deploying high availability for Microsoft 365 federated authentication in Azure infrastructure services, you create an internal load balancer and two AD FS servers.</span></span>
  
<span data-ttu-id="35c74-105">[4 단계: 웹 응용 프로그램 프록시 구성](high-availability-federated-authentication-phase-4-configure-web-application-pro.md)으로 넘어가기 전에이 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-105">You must complete this phase before moving on to [Phase 4: Configure web application proxies](high-availability-federated-authentication-phase-4-configure-web-application-pro.md).</span></span> <span data-ttu-id="35c74-106">모든 단계에 대 한 자세한 내용은 [Azure에서 Microsoft 365에 대 한 고가용성 페더레이션 인증 배포](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35c74-106">See [Deploy high availability federated authentication for Microsoft 365 in Azure](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md) for all of the phases.</span></span>
  
## <a name="create-the-ad-fs-server-virtual-machines-in-azure"></a><span data-ttu-id="35c74-107">Azure에서 AD FS 서버 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="35c74-107">Create the AD FS server virtual machines in Azure</span></span>

<span data-ttu-id="35c74-p102">PowerShell 명령의 다음 블록을 사용하여 두 AD FS 서버의 가상 컴퓨터를 만듭니다. PowerShell 명령 집합은 다음 테이블의 값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-p102">Use the following block of PowerShell commands to create the virtual machines for the two AD FS servers. This PowerShell command set uses values from the following tables:</span></span>
  
- <span data-ttu-id="35c74-110">테이블 M, 가상 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="35c74-110">Table M, for your virtual machines</span></span>
    
- <span data-ttu-id="35c74-111">테이블 R, 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="35c74-111">Table R, for your resource groups</span></span>
    
- <span data-ttu-id="35c74-112">테이블 V, 가상 네트워크 설정</span><span class="sxs-lookup"><span data-stu-id="35c74-112">Table V, for your virtual network settings</span></span>
    
- <span data-ttu-id="35c74-113">테이블 S, 서브넷</span><span class="sxs-lookup"><span data-stu-id="35c74-113">Table S, for your subnets</span></span>
    
- <span data-ttu-id="35c74-114">테이블 I, 고정 IP 주소</span><span class="sxs-lookup"><span data-stu-id="35c74-114">Table I, for your static IP addresses</span></span>
    
- <span data-ttu-id="35c74-115">테이블 A, 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="35c74-115">Table A, for your availability sets</span></span>
    
<span data-ttu-id="35c74-116">[2 단계: 도메인 컨트롤러](high-availability-federated-authentication-phase-2-configure-domain-controllers.md) 와 테이블 R, V, S, I, A를 [1 단계: configure Azure](high-availability-federated-authentication-phase-1-configure-azure.md)에서 정의한 표 M을 정의 했습니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-116">Recall that you defined Table M in [Phase 2: Configure domain controllers](high-availability-federated-authentication-phase-2-configure-domain-controllers.md) and Tables R, V, S, I, and A in [Phase 1: Configure Azure](high-availability-federated-authentication-phase-1-configure-azure.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="35c74-117">다음 명령 집합은 최신 버전의 Azure PowerShell을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-117">The following command sets use the latest version of Azure PowerShell.</span></span> <span data-ttu-id="35c74-118">[Azure PowerShell을 시작 하기를](https://docs.microsoft.com/powershell/azure/get-started-azureps)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35c74-118">See [Get started with Azure PowerShell](https://docs.microsoft.com/powershell/azure/get-started-azureps).</span></span> 
  
<span data-ttu-id="35c74-119">먼저, 두 개의 AD FS 서버용 Azure 내부 부하 분산 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-119">First, you create an Azure internal load balancer for the two AD FS servers.</span></span> <span data-ttu-id="35c74-120">변수 값을 지정 하 고 문자를 제거 \< and > 합니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-120">Specify the values for the variables, removing the \< and > characters.</span></span> <span data-ttu-id="35c74-121">모든 적절한 값이 제공되면 Azure PowerShell 명령 프롬프트나 PowerShell ISE에서 결과 블록을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-121">When you have supplied all the proper values, run the resulting block at the Azure PowerShell command prompt or in the PowerShell ISE.</span></span>
  
> [!TIP]
> <span data-ttu-id="35c74-122">사용자 지정 설정에 따라 실행 가능한 PowerShell 명령 블록을 생성 하려면이 [Microsoft Excel 구성 통합 문서](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/O365FedAuthInAzure_Config.xlsx)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-122">To generate ready-to-run PowerShell command blocks based on your custom settings, use this [Microsoft Excel configuration workbook](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/O365FedAuthInAzure_Config.xlsx).</span></span> 

```powershell
# Set up key variables
$locName="<your Azure location>"
$vnetName="<Table V - Item 1 - Value column>"
$subnetName="<Table R - Item 2 - Subnet name column>"
$privIP="<Table I - Item 4 - Value column>"
$rgName=<Table R - Item 4 - Resource group name column>"

$vnet=Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgName
$subnet=Get-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name $subnetName

$frontendIP=New-AzLoadBalancerFrontendIpConfig -Name "ADFSServers-LBFE" -PrivateIPAddress $privIP -Subnet $subnet
$beAddressPool=New-AzLoadBalancerBackendAddressPoolConfig -Name "ADFSServers-LBBE"

$healthProbe=New-AzLoadBalancerProbeConfig -Name WebServersProbe -Protocol "TCP" -Port 443 -IntervalInSeconds 15 -ProbeCount 2
$lbrule=New-AzLoadBalancerRuleConfig -Name "HTTPSTraffic" -FrontendIpConfiguration $frontendIP -BackendAddressPool $beAddressPool -Probe $healthProbe -Protocol "TCP" -FrontendPort 443 -BackendPort 443
New-AzLoadBalancer -ResourceGroupName $rgName -Name "ADFSServers" -Location $locName -LoadBalancingRule $lbrule -BackendAddressPool $beAddressPool -Probe $healthProbe -FrontendIpConfiguration $frontendIP
```

<span data-ttu-id="35c74-123">다음으로 AD FS 서버 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-123">Next, create the AD FS server virtual machines.</span></span>
  
<span data-ttu-id="35c74-124">모든 적절한 값이 제공되면 Azure PowerShell 명령 프롬프트나 PowerShell ISE에서 결과 블록을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-124">When you have supplied all the proper values, run the resulting block at the Azure PowerShell command prompt or in the PowerShell ISE.</span></span>
  
```powershell
# Set up variables common to both virtual machines
$locName="<your Azure location>"
$vnetName="<Table V - Item 1 - Value column>"
$subnetName="<Table R - Item 2 - Subnet name column>"
$avName="<Table A - Item 2 - Availability set name column>"
$rgNameTier="<Table R - Item 2 - Resource group name column>"
$rgNameInfra="<Table R - Item 4 - Resource group name column>"

$rgName=$rgNameInfra
$vnet=Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgName
$subnet=Get-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name $subnetName
$backendSubnet=Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet
$webLB=Get-AzLoadBalancer -ResourceGroupName $rgName -Name "ADFSServers"

$rgName=$rgNameTier
$avSet=Get-AzAvailabilitySet -Name $avName -ResourceGroupName $rgName

# Create the first ADFS server virtual machine
$vmName="<Table M - Item 4 - Virtual machine name column>"
$vmSize="<Table M - Item 4 - Minimum size column>"
$staticIP="<Table I - Item 5 - Value column>"
$diskStorageType="<Table M - Item 4 - Storage type column>"

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName -Subnet $backendSubnet -LoadBalancerBackendAddressPool $webLB.BackendAddressPools[0] -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize -AvailabilitySetId $avset.Id

$cred=Get-Credential -Message "Type the name and password of the local administrator account for the first AD FS server." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm

# Create the second AD FS virtual machine
$vmName="<Table M - Item 5 - Virtual machine name column>"
$vmSize="<Table M - Item 5 - Minimum size column>"
$staticIP="<Table I - Item 6 - Value column>"
$diskStorageType="<Table M - Item 5 - Storage type column>"

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName  -Subnet $backendSubnet -LoadBalancerBackendAddressPool $webLB.BackendAddressPools[0] -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize -AvailabilitySetId $avset.Id

$cred=Get-Credential -Message "Type the name and password of the local administrator account for the second AD FS server." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm

```

> [!NOTE]
> <span data-ttu-id="35c74-p105">이러한 가상 컴퓨터는 인트라넷 응용 프로그램용이므로 공용 IP 주소나 DNS 도메인 이름 레이블에 할당되지 않으며 인터넷에 표시되지 않습니다. 그러나 이는 Azure Portal에서 연결할 수 없음을 의미합니다. 가상 컴퓨터의 속성을 보면 이 **연결** 옵션을 사용할 수 없습니다. 원격 데스크톱 연결 액세서리 또는 다른 원격 데스크톱 도구를 사용하여 개인 IP 주소나 인트라넷 DNS 이름을 사용하는 가상 컴퓨터에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-p105">Because these virtual machines are for an intranet application, they are not assigned a public IP address or a DNS domain name label and exposed to the Internet. However, this also means that you cannot connect to them from the Azure portal. The **Connect** option is unavailable when you view the properties of the virtual machine. Use the Remote Desktop Connection accessory or another Remote Desktop tool to connect to the virtual machine using its private IP address or intranet DNS name.</span></span>
  
<span data-ttu-id="35c74-p106">각 가상 컴퓨터에 원하는 원격 데스크톱 클라이언트를 사용하고 원격 데스크톱 연결을 만듭니다. 인트라넷 DNS나 컴퓨터 이름 및 로컬 관리자 계정의 자격 증명을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-p106">For each virtual machine, use the remote desktop client of your choice and create a remote desktop connection. Use its intranet DNS or computer name and the credentials of the local administrator account.</span></span>
  
<span data-ttu-id="35c74-131">각 가상 컴퓨터에 대해 Windows PowerShell 프롬프트에서 이러한 명령을 사용 하 여 해당 하는 AD DS (Active Directory 도메인 서비스) 도메인에 참가 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-131">For each virtual machine, join them to the appropriate Active Directory Domain Services (AD DS) domain with these commands at the Windows PowerShell prompt.</span></span>
  
```powershell
$domName="<AD DS domain name to join, such as corp.contoso.com>"
$cred=Get-Credential -Message "Type the name and password of a domain acccount."
Add-Computer -DomainName $domName -Credential $cred
Restart-Computer
```

<span data-ttu-id="35c74-132">이 단계를 성공적으로 완료하면 자리 표시자 컴퓨터 이름이 포함된 다음 구성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-132">Here is the configuration resulting from the successful completion of this phase, with placeholder computer names.</span></span>
  
<span data-ttu-id="35c74-133">**3단계: Azure의 고가용성 페더레이션 인증 인프라용 AD FS 서버 및 내부 부하 분산 장치**</span><span class="sxs-lookup"><span data-stu-id="35c74-133">**Phase 3: The AD FS servers and internal load balancer for your high availability federated authentication infrastructure in Azure**</span></span>

![AD FS 서버를 사용 하는 Azure의 고가용성 Microsoft 365 페더레이션 인증 인프라 3 단계](../media/f39b2d2f-8a5b-44da-b763-e1f943fcdbc4.png)
  
## <a name="next-step"></a><span data-ttu-id="35c74-135">다음 단계</span><span class="sxs-lookup"><span data-stu-id="35c74-135">Next step</span></span>

<span data-ttu-id="35c74-136">[4 단계: 웹 응용 프로그램 프록시 구성](high-availability-federated-authentication-phase-4-configure-web-application-pro.md) 을 사용 하 여이 작업을 계속 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="35c74-136">Use [Phase 4: Configure web application proxies](high-availability-federated-authentication-phase-4-configure-web-application-pro.md) to continue configuring this workload.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="35c74-137">참고 항목</span><span class="sxs-lookup"><span data-stu-id="35c74-137">See Also</span></span>

[<span data-ttu-id="35c74-138">Azure에서 Microsoft 365용 고가용성 페더레이션 인증 배포</span><span class="sxs-lookup"><span data-stu-id="35c74-138">Deploy high availability federated authentication for Microsoft 365 in Azure</span></span>](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md)
  
[<span data-ttu-id="35c74-139">Microsoft 365 개발/테스트 환경용 페더레이션 id</span><span class="sxs-lookup"><span data-stu-id="35c74-139">Federated identity for your Microsoft 365 dev/test environment</span></span>](federated-identity-for-your-microsoft-365-dev-test-environment.md)

