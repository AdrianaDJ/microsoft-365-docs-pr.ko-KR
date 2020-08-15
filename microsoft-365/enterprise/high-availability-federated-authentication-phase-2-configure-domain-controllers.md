---
title: 고가용성 페더레이션 인증 2 단계 도메인 컨트롤러 구성
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
ms.custom: Ent_Solutions
ms.assetid: 6b0eff4c-2c5e-4581-8393-a36f7b36a72f
description: '요약: Microsoft Azure에서 Microsoft 365에 대 한 고가용성 페더레이션 인증용 도메인 컨트롤러 및 디렉터리 동기화 서버를 구성 합니다.'
ms.openlocfilehash: 1c3fd686ee553a57d66dcfd51a6045167a12de8a
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46692677"
---
# <a name="high-availability-federated-authentication-phase-2-configure-domain-controllers"></a><span data-ttu-id="31b2a-103">고가용성 페더레이션 인증 2단계: 도메인 컨트롤러 구성</span><span class="sxs-lookup"><span data-stu-id="31b2a-103">High availability federated authentication Phase 2: Configure domain controllers</span></span>

<span data-ttu-id="31b2a-104">Azure 인프라 서비스에서 Microsoft 365 페더레이션 인증을 위해 고가용성을 배포 하는이 단계에서는 Azure virtual network에서 두 개의 도메인 컨트롤러 및 디렉터리 동기화 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-104">In this phase of deploying high availability for Microsoft 365 federated authentication in Azure infrastructure services, you configure two domain controllers and the directory synchronization server in the Azure virtual network.</span></span> <span data-ttu-id="31b2a-105">인증에 대 한 클라이언트 웹 요청은 온-프레미스 네트워크에 대 한 사이트 간 VPN 연결을 통해 인증 트래픽을 전송 하는 것이 아니라 Azure virtual network에서 인증 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-105">Client web requests for authentication can then be authenticated in the Azure virtual network, rather than sending that authentication traffic across the site-to-site VPN connection to your on-premises network.</span></span>
  
> [!NOTE]
> <span data-ttu-id="31b2a-106">AD FS (active Directory Federation Services)는 AD DS (Active directory 도메인 서비스) 도메인 컨트롤러 대신 Azure Active Directory (Azure AD)를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-106">Active Directory Federation Services (AD FS) cannot use Azure Active Directory (Azure AD) as a substitute for Active Directory Domain Services (AD DS) domain controllers.</span></span> 
  
<span data-ttu-id="31b2a-107">[3 단계: AD FS 서버 구성](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md)으로 넘어가기 전에이 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-107">You must complete this phase before moving on to [Phase 3: Configure AD FS servers](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md).</span></span> <span data-ttu-id="31b2a-108">모든 단계에 대 한 자세한 내용은 [Azure에서 Microsoft 365에 대 한 고가용성 페더레이션 인증 배포](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31b2a-108">See [Deploy high availability federated authentication for Microsoft 365 in Azure](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md) for all of the phases.</span></span>
  
## <a name="create-the-domain-controller-virtual-machines-in-azure"></a><span data-ttu-id="31b2a-109">Azure에서 도메인 컨트롤러 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="31b2a-109">Create the domain controller virtual machines in Azure</span></span>

<span data-ttu-id="31b2a-110">먼저, 테이블 M의 **가상 컴퓨터 이름** 열을 채우고 **최소 크기** 열에서 가상 컴퓨터 크기를 필요한만큼 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-110">First, you need to fill out the **Virtual machine name** column of Table M and modify virtual machine sizes as needed in the **Minimum size** column.</span></span>
  
|<span data-ttu-id="31b2a-111">**항목**</span><span class="sxs-lookup"><span data-stu-id="31b2a-111">**Item**</span></span>|<span data-ttu-id="31b2a-112">**가상 컴퓨터 이름**</span><span class="sxs-lookup"><span data-stu-id="31b2a-112">**Virtual machine name**</span></span>|<span data-ttu-id="31b2a-113">**갤러리 이미지**</span><span class="sxs-lookup"><span data-stu-id="31b2a-113">**Gallery image**</span></span>|<span data-ttu-id="31b2a-114">**저장소 유형**</span><span class="sxs-lookup"><span data-stu-id="31b2a-114">**Storage type**</span></span>|<span data-ttu-id="31b2a-115">**최소 크기**</span><span class="sxs-lookup"><span data-stu-id="31b2a-115">**Minimum size**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="31b2a-116">1.</span><span class="sxs-lookup"><span data-stu-id="31b2a-116">1.</span></span>  <br/> |![라인](../media/Common-Images/TableLine.png) <span data-ttu-id="31b2a-118">(첫 번째 도메인 컨트롤러, 예: DC1)</span><span class="sxs-lookup"><span data-stu-id="31b2a-118">(first domain controller, example DC1)</span></span>  <br/> |<span data-ttu-id="31b2a-119">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="31b2a-119">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="31b2a-120">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="31b2a-120">Standard_LRS</span></span>  <br/> |<span data-ttu-id="31b2a-121">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="31b2a-121">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="31b2a-122">2.</span><span class="sxs-lookup"><span data-stu-id="31b2a-122">2.</span></span>  <br/> |![라인](../media/Common-Images/TableLine.png) <span data-ttu-id="31b2a-124">(두 번째 도메인 컨트롤러, 예: DC2)</span><span class="sxs-lookup"><span data-stu-id="31b2a-124">(second domain controller, example DC2)</span></span>  <br/> |<span data-ttu-id="31b2a-125">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="31b2a-125">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="31b2a-126">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="31b2a-126">Standard_LRS</span></span>  <br/> |<span data-ttu-id="31b2a-127">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="31b2a-127">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="31b2a-128">3.</span><span class="sxs-lookup"><span data-stu-id="31b2a-128">3.</span></span>  <br/> |![라인](../media/Common-Images/TableLine.png) <span data-ttu-id="31b2a-130">(디렉터리 동기화 서버, 예: DS1)</span><span class="sxs-lookup"><span data-stu-id="31b2a-130">(directory synchronization server, example DS1)</span></span>  <br/> |<span data-ttu-id="31b2a-131">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="31b2a-131">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="31b2a-132">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="31b2a-132">Standard_LRS</span></span>  <br/> |<span data-ttu-id="31b2a-133">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="31b2a-133">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="31b2a-134">4.</span><span class="sxs-lookup"><span data-stu-id="31b2a-134">4.</span></span>  <br/> |![라인](../media/Common-Images/TableLine.png) <span data-ttu-id="31b2a-136">(첫 번째 AD FS 서버, 예: ADFS1)</span><span class="sxs-lookup"><span data-stu-id="31b2a-136">(first AD FS server, example ADFS1)</span></span>  <br/> |<span data-ttu-id="31b2a-137">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="31b2a-137">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="31b2a-138">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="31b2a-138">Standard_LRS</span></span>  <br/> |<span data-ttu-id="31b2a-139">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="31b2a-139">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="31b2a-140">5.</span><span class="sxs-lookup"><span data-stu-id="31b2a-140">5.</span></span>  <br/> |![라인](../media/Common-Images/TableLine.png) <span data-ttu-id="31b2a-142">(두 번째 AD FS 서버, 예:: ADFS2)</span><span class="sxs-lookup"><span data-stu-id="31b2a-142">(second AD FS server, example ADFS2)</span></span>  <br/> |<span data-ttu-id="31b2a-143">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="31b2a-143">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="31b2a-144">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="31b2a-144">Standard_LRS</span></span>  <br/> |<span data-ttu-id="31b2a-145">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="31b2a-145">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="31b2a-146">6.</span><span class="sxs-lookup"><span data-stu-id="31b2a-146">6.</span></span>  <br/> |![라인](../media/Common-Images/TableLine.png) <span data-ttu-id="31b2a-148">(첫 번째 웹 응용 프로그램 프록시 서버, 예: WEB1)</span><span class="sxs-lookup"><span data-stu-id="31b2a-148">(first web application proxy server, example WEB1)</span></span>  <br/> |<span data-ttu-id="31b2a-149">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="31b2a-149">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="31b2a-150">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="31b2a-150">Standard_LRS</span></span>  <br/> |<span data-ttu-id="31b2a-151">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="31b2a-151">Standard_D2</span></span>  <br/> |
|<span data-ttu-id="31b2a-152">7.</span><span class="sxs-lookup"><span data-stu-id="31b2a-152">7.</span></span>  <br/> |![라인](../media/Common-Images/TableLine.png) <span data-ttu-id="31b2a-154">(두 번째 웹 응용 프로그램 프록시 서버, 예: WEB2)</span><span class="sxs-lookup"><span data-stu-id="31b2a-154">(second web application proxy server, example WEB2)</span></span>  <br/> |<span data-ttu-id="31b2a-155">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="31b2a-155">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="31b2a-156">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="31b2a-156">Standard_LRS</span></span>  <br/> |<span data-ttu-id="31b2a-157">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="31b2a-157">Standard_D2</span></span>  <br/> |
   
 <span data-ttu-id="31b2a-158">**테이블 M-Azure의 Microsoft 365에 대 한 고가용성 페더레이션 인증용 가상 컴퓨터**</span><span class="sxs-lookup"><span data-stu-id="31b2a-158">**Table M - Virtual machines for the high availability federated authentication for Microsoft 365 in Azure**</span></span>
  
<span data-ttu-id="31b2a-159">가상 컴퓨터 크기의 전체 목록은 [가상 컴퓨터 크기](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-sizes)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31b2a-159">For the complete list of virtual machine sizes, see [Sizes for virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-sizes).</span></span>
  
<span data-ttu-id="31b2a-160">다음 Azure PowerShell 명령 블록은 두 도메인 컨트롤러에 대 한 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-160">The following Azure PowerShell command block creates the virtual machines for the two domain controllers.</span></span> <span data-ttu-id="31b2a-161">변수 값을 지정 하 고 문자를 제거 \< and > 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-161">Specify the values for the variables, removing the \< and > characters.</span></span> <span data-ttu-id="31b2a-162">이 Azure PowerShell 명령 블록은 다음 테이블의 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-162">Note that this Azure PowerShell command block uses values from the following tables:</span></span>
  
- <span data-ttu-id="31b2a-163">테이블 M, 가상 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="31b2a-163">Table M, for your virtual machines</span></span>
    
- <span data-ttu-id="31b2a-164">테이블 R, 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="31b2a-164">Table R, for your resource groups</span></span>
    
- <span data-ttu-id="31b2a-165">테이블 V, 가상 네트워크 설정</span><span class="sxs-lookup"><span data-stu-id="31b2a-165">Table V, for your virtual network settings</span></span>
    
- <span data-ttu-id="31b2a-166">테이블 S, 서브넷</span><span class="sxs-lookup"><span data-stu-id="31b2a-166">Table S, for your subnets</span></span>
    
- <span data-ttu-id="31b2a-167">테이블 I, 고정 IP 주소</span><span class="sxs-lookup"><span data-stu-id="31b2a-167">Table I, for your static IP addresses</span></span>
    
- <span data-ttu-id="31b2a-168">테이블 A, 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="31b2a-168">Table A, for your availability sets</span></span>
    
<span data-ttu-id="31b2a-169">[1 단계: Azure 구성](high-availability-federated-authentication-phase-1-configure-azure.md)에서 테이블 R, V, S, I 및 A를 정의한 것을 기억 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-169">Recall that you defined Tables R, V, S, I, and A in [Phase 1: Configure Azure](high-availability-federated-authentication-phase-1-configure-azure.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="31b2a-170">다음 명령 집합은 최신 버전의 Azure PowerShell을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-170">The following command sets use the latest version of Azure PowerShell.</span></span> <span data-ttu-id="31b2a-171">[Azure PowerShell을 시작 하기를](https://docs.microsoft.com/powershell/azure/get-started-azureps)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31b2a-171">See [Get started with Azure PowerShell](https://docs.microsoft.com/powershell/azure/get-started-azureps).</span></span> 
  
<span data-ttu-id="31b2a-172">올바른 값을 모두 제공하면 Azure PowerShell 프롬프트나 로컬 컴퓨터의 PowerShell ISE(통합 스크립트 환경)에서 결과 블록을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-172">When you have supplied all the correct values, run the resulting block at the Azure PowerShell prompt or in the PowerShell Integrated Script Environment (ISE) on your local computer.</span></span>
  
> [!TIP]
> <span data-ttu-id="31b2a-173">사용자 지정 설정에 따라 실행 가능한 PowerShell 명령 블록을 생성 하려면이 [Microsoft Excel 구성 통합 문서](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/O365FedAuthInAzure_Config.xlsx)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-173">To generate ready-to-run PowerShell command blocks based on your custom settings, use this [Microsoft Excel configuration workbook](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/O365FedAuthInAzure_Config.xlsx).</span></span> 

```powershell
# Set up variables common to both virtual machines
$locName="<your Azure location>"
$vnetName="<Table V - Item 1 - Value column>"
$subnetName="<Table S - Item 1 - Value column>"
$avName="<Table A - Item 1 - Availability set name column>"
$rgNameTier="<Table R - Item 1 - Resource group name column>"
$rgNameInfra="<Table R - Item 4 - Resource group name column>"

$rgName=$rgNameInfra
$vnet=Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgName
$subnet=Get-AzVirtualNetworkSubnetConfig -VirtualNetwork $vnet -Name $subnetName

$rgName=$rgNameTier
$avSet=Get-AzAvailabilitySet -Name $avName -ResourceGroupName $rgName 

# Create the first domain controller
$vmName="<Table M - Item 1 - Virtual machine name column>"
$vmSize="<Table M - Item 1 - Minimum size column>"
$staticIP="<Table I - Item 1 - Value column>"
$diskStorageType="<Table M - Item 1 - Storage type column>"
$diskSize=<size of the extra disk for Active Directory Domain Services (AD DS) data in GB>

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName -Subnet $subnet -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize -AvailabilitySetId $avset.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
$diskConfig=New-AzDiskConfig -AccountType $diskStorageType -Location $locName -CreateOption Empty -DiskSizeGB $diskSize
$dataDisk1=New-AzDisk -DiskName ($vmName + "-DataDisk1") -Disk $diskConfig -ResourceGroupName $rgName
$vm=Add-AzVMDataDisk -VM $vm -Name ($vmName + "-DataDisk1") -CreateOption Attach -ManagedDiskId $dataDisk1.Id -Lun 1
$cred=Get-Credential -Message "Type the name and password of the local administrator account for the first domain controller." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm

# Create the second domain controller
$vmName="<Table M - Item 2 - Virtual machine name column>"
$vmSize="<Table M - Item 2 - Minimum size column>"
$staticIP="<Table I - Item 2 - Value column>"
$diskStorageType="<Table M - Item 2 - Storage type column>"
$diskSize=<size of the extra disk for AD DS data in GB>

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName -Subnet $subnet -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize -AvailabilitySetId $avset.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
$diskConfig=New-AzDiskConfig -AccountType $diskStorageType -Location $locName -CreateOption Empty -DiskSizeGB $diskSize
$dataDisk1=New-AzDisk -DiskName ($vmName + "-DataDisk1") -Disk $diskConfig -ResourceGroupName $rgName
$vm=Add-AzVMDataDisk -VM $vm -Name ($vmName + "-DataDisk1") -CreateOption Attach -ManagedDiskId $dataDisk1.Id -Lun 1
$cred=Get-Credential -Message "Type the name and password of the local administrator account for the second domain controller." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm

# Create the directory synchronization server
$vmName="<Table M - Item 3 - Virtual machine name column>"
$vmSize="<Table M - Item 3 - Minimum size column>"
$staticIP="<Table I - Item 3 - Value column>"
$diskStorageType="<Table M - Item 3 - Storage type column>"

$nic=New-AzNetworkInterface -Name ($vmName +"-NIC") -ResourceGroupName $rgName -Location $locName -Subnet $subnet -PrivateIpAddress $staticIP
$vm=New-AzVMConfig -VMName $vmName -VMSize $vmSize

$cred=Get-Credential -Message "Type the name and password of the local administrator account for the directory synchronization server." 
$vm=Set-AzVMOperatingSystem -VM $vm -Windows -ComputerName $vmName -Credential $cred -ProvisionVMAgent -EnableAutoUpdate
$vm=Set-AzVMSourceImage -VM $vm -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version "latest"
$vm=Add-AzVMNetworkInterface -VM $vm -Id $nic.Id
$vm=Set-AzVMOSDisk -VM $vm -Name ($vmName +"-OS") -DiskSizeInGB 128 -CreateOption FromImage -StorageAccountType $diskStorageType
New-AzVM -ResourceGroupName $rgName -Location $locName -VM $vm
```

> [!NOTE]
> <span data-ttu-id="31b2a-p105">이러한 가상 컴퓨터는 인트라넷 응용 프로그램용이므로 공용 IP 주소나 DNS 도메인 이름 레이블에 할당되지 않으며 인터넷에 표시되지 않습니다. 그러나 이는 Azure Portal에서 연결할 수 없음을 의미합니다. 가상 컴퓨터의 속성을 보면 이 **연결** 옵션을 사용할 수 없습니다. 원격 데스크톱 연결 액세서리 또는 다른 원격 데스크톱 도구를 사용하여 개인 IP 주소나 인트라넷 DNS 이름을 사용하는 가상 컴퓨터에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-p105">Because these virtual machines are for an intranet application, they are not assigned a public IP address or a DNS domain name label and exposed to the Internet. However, this also means that you cannot connect to them from the Azure portal. The **Connect** option is unavailable when you view the properties of the virtual machine. Use the Remote Desktop Connection accessory or another Remote Desktop tool to connect to the virtual machine using its private IP address or intranet DNS name.</span></span>
  
## <a name="configure-the-first-domain-controller"></a><span data-ttu-id="31b2a-178">첫 번째 도메인 컨트롤러 구성</span><span class="sxs-lookup"><span data-stu-id="31b2a-178">Configure the first domain controller</span></span>

<span data-ttu-id="31b2a-p106">원하는 원격 데스크톱 클라이언트를 사용하고 첫 번째 도메인 컨트롤러 가상 컴퓨터에 대한 원격 데스크톱 연결을 만듭니다. 인트라넷 DNS나 컴퓨터 이름 및 로컬 관리자 계정의 자격 증명을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-p106">Use the remote desktop client of your choice and create a remote desktop connection to the first domain controller virtual machine. Use its intranet DNS or computer name and the credentials of the local administrator account.</span></span>
  
<span data-ttu-id="31b2a-181">다음으로 **첫 번째 도메인 컨트롤러 가상 컴퓨터의**Windows PowerShell 명령 프롬프트에서 다음 명령을 사용 하 여 첫 번째 도메인 컨트롤러에 추가 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-181">Next, add the extra data disk to the first domain controller with this command from a Windows PowerShell command prompt **on the first domain controller virtual machine**:</span></span>
  
```powershell
Get-Disk | Where PartitionStyle -eq "RAW" | Initialize-Disk -PartitionStyle MBR -PassThru | New-Partition -AssignDriveLetter -UseMaximumSize | Format-Volume -FileSystem NTFS -NewFileSystemLabel "WSAD Data"
```

<span data-ttu-id="31b2a-182">그런 다음 **ping** 명령으로 조직 네트워크의 리소스 이름과 IP 주소를 ping하여 조직 네트워크의 위치에 대한 첫 번째 도메인 컨트롤러의 연결을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-182">Next, test the first domain controller's connectivity to locations on your organization network by using the **ping** command to ping names and IP addresses of resources on your organization network.</span></span>
  
<span data-ttu-id="31b2a-p107">이 프로시저에서는 DNS 이름 확인이 제대로 작동하는지(가상 컴퓨터가 온-프레미스 DNS 서버와 올바르게 구성되었는지)와 프레미스 간 가상 네트워크에서 이 패킷을 보낼 수 있는지 확인합니다. 기본 테스트가 실패하면 DNS 이름 확인 및 패킷 배달 문제의 해결 방법을 IT 부서에 문의합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-p107">This procedure ensures that DNS name resolution is working correctly (that the virtual machine is correctly configured with on-premises DNS servers) and that packets can be sent to and from the cross-premises virtual network. If this basic test fails, contact your IT department to troubleshoot the DNS name resolution and packet delivery issues.</span></span>
  
<span data-ttu-id="31b2a-185">다음으로 첫 번째 도메인 컨트롤러의 Windows PowerShell 명령 프롬프트에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-185">Next, from the Windows PowerShell command prompt on the first domain controller, run the following commands:</span></span>
  
```powershell
$domname="<DNS domain name of the domain for which this computer will be a domain controller, such as corp.contoso.com>"
$cred = Get-Credential -Message "Enter credentials of an account with permission to join a new domain controller to the domain"
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSDomainController -InstallDns -DomainName $domname  -DatabasePath "F:\NTDS" -SysvolPath "F:\SYSVOL" -LogPath "F:\Logs" -Credential $cred
```

<span data-ttu-id="31b2a-p108">도메인 관리자 계정의 자격 증명을 제공하라는 메시지가 나타납니다. 컴퓨터가 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-p108">You will be prompted to supply the credentials of a domain administrator account. The computer will restart.</span></span>
  
## <a name="configure-the-second-domain-controller"></a><span data-ttu-id="31b2a-188">두 번째 도메인 컨트롤러 구성</span><span class="sxs-lookup"><span data-stu-id="31b2a-188">Configure the second domain controller</span></span>

<span data-ttu-id="31b2a-p109">원하는 원격 데스크톱 클라이언트를 사용하고 두 번째 도메인 컨트롤러 가상 컴퓨터에 대한 원격 데스크톱 연결을 만듭니다.  인트라넷 DNS나 컴퓨터 이름 및 로컬 관리자 계정의 자격 증명을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-p109">Use the remote desktop client of your choice and create a remote desktop connection to the second domain controller virtual machine. Use its intranet DNS or computer name and the credentials of the local administrator account.</span></span>
  
<span data-ttu-id="31b2a-191">다음으로 **두 번째 도메인 컨트롤러 가상 컴퓨터의**Windows PowerShell 명령 프롬프트에서 다음 명령을 사용 하 여 추가 데이터 디스크를 두 번째 도메인 컨트롤러에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-191">Next, you need to add the extra data disk to the second domain controller with this command from a Windows PowerShell command prompt **on the second domain controller virtual machine**:</span></span>
  
```powershell
Get-Disk | Where PartitionStyle -eq "RAW" | Initialize-Disk -PartitionStyle MBR -PassThru | New-Partition -AssignDriveLetter -UseMaximumSize | Format-Volume -FileSystem NTFS -NewFileSystemLabel "WSAD Data"
```

<span data-ttu-id="31b2a-192">그리고 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-192">Next, run the following commands:</span></span>
  
```powershell
$domname="<DNS domain name of the domain for which this computer will be a domain controller, such as corp.contoso.com>"
$cred = Get-Credential -Message "Enter credentials of an account with permission to join a new domain controller to the domain"
Install-WindowsFeature AD-Domain-Services -IncludeManagementTools
Install-ADDSDomainController -InstallDns -DomainName $domname  -DatabasePath "F:\NTDS" -SysvolPath "F:\SYSVOL" -LogPath "F:\Logs" -Credential $cred

```

<span data-ttu-id="31b2a-p110">도메인 관리자 계정의 자격 증명을 제공하라는 메시지가 나타납니다. 컴퓨터가 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-p110">You will be prompted to supply the credentials of a domain administrator account. The computer will restart.</span></span>
  
<span data-ttu-id="31b2a-195">다음으로 Azure가 두 개의 새 도메인 컨트롤러의 IP 주소를 DNS 서버로 사용할 가상 컴퓨터를 할당하도록 가상 네트워크의 DNS 서버를 업데이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-195">Next, you need to update the DNS servers for your virtual network so that Azure assigns virtual machines the IP addresses of the two new domain controllers to use as their DNS servers.</span></span> <span data-ttu-id="31b2a-196">변수를 입력 하 고 로컬 컴퓨터의 Windows PowerShell 명령 프롬프트에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-196">Fill in the variables and then run these commands from a Windows PowerShell command prompt on your local computer:</span></span>
  
```powershell
$rgName="<Table R - Item 4 - Resource group name column>"
$adrgName="<Table R - Item 1 - Resource group name column>"
$locName="<your Azure location>"
$vnetName="<Table V - Item 1 - Value column>"
$onpremDNSIP1="<Table D - Item 1 - DNS server IP address column>"
$onpremDNSIP2="<Table D - Item 2 - DNS server IP address column>"
$staticIP1="<Table I - Item 1 - Value column>"
$staticIP2="<Table I - Item 2 - Value column>"
$firstDCName="<Table M - Item 1 - Virtual machine name column>"
$secondDCName="<Table M - Item 2 - Virtual machine name column>"

$vnet=Get-AzVirtualNetwork -ResourceGroupName $rgName -Name $vnetName
$vnet.DhcpOptions.DnsServers.Add($staticIP1)
$vnet.DhcpOptions.DnsServers.Add($staticIP2) 
$vnet.DhcpOptions.DnsServers.Remove($onpremDNSIP1)
$vnet.DhcpOptions.DnsServers.Remove($onpremDNSIP2) 
Set-AzVirtualNetwork -VirtualNetwork $vnet
Restart-AzVM -ResourceGroupName $adrgName -Name $firstDCName
Restart-AzVM -ResourceGroupName $adrgName -Name $secondDCName
```

<span data-ttu-id="31b2a-p112">이제 온-프레미스 DNS 서버가 DNS 서버로 구성되지 않도록 두 도메인 컨트롤러를 다시 시작합니다. 모두 DNS 서버이므로 도메인 컨트롤러로 수준을 올리면 온-프레미스 DNS 서버가 DNS 전달자로 자동 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-p112">Note that we restart the two domain controllers so that they are not configured with the on-premises DNS servers as DNS servers. Because they are both DNS servers themselves, they were automatically configured with the on-premises DNS servers as DNS forwarders when they were promoted to domain controllers.</span></span>
  
<span data-ttu-id="31b2a-199">다음으로 Azure Virtual Network의 서버가 로컬 도메인 컨트롤러를 사용하도록 Active Directory 복제 사이트를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-199">Next, we need to create an Active Directory replication site to ensure that servers in the Azure virtual network use the local domain controllers.</span></span> <span data-ttu-id="31b2a-200">도메인 관리자 계정을 사용 하 여 도메인 컨트롤러에 연결 하 고 관리자 수준 Windows PowerShell 프롬프트에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-200">Connect to either domain controller with a domain administrator account and run the following commands from an administrator-level Windows PowerShell prompt:</span></span>
  
```powershell
$vnet="<Table V - Item 1 - Value column>"
$vnetSpace="<Table V - Item 4 - Value column>"
New-ADReplicationSite -Name $vnet 
New-ADReplicationSubnet -Name $vnetSpace -Site $vnet
```

## <a name="configure-the-directory-synchronization-server"></a><span data-ttu-id="31b2a-201">디렉터리 동기화 서버 구성</span><span class="sxs-lookup"><span data-stu-id="31b2a-201">Configure the directory synchronization server</span></span>

<span data-ttu-id="31b2a-202">원하는 원격 데스크톱 클라이언트를 사용 하 고 디렉터리 동기화 서버 가상 컴퓨터에 대 한 원격 데스크톱 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-202">Use the remote desktop client of your choice and create a remote desktop connection to the directory synchronization server virtual machine.</span></span> <span data-ttu-id="31b2a-203">인트라넷 DNS나 컴퓨터 이름 및 로컬 관리자 계정의 자격 증명을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-203">Use its intranet DNS or computer name and the credentials of the local administrator account.</span></span>
  
<span data-ttu-id="31b2a-204">다음으로, Windows PowerShell 프롬프트에서 다음 명령을 사용 하 여 해당 AD DS 도메인에 가입 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-204">Next, join it to the appropriate AD DS domain with these commands at the Windows PowerShell prompt.</span></span>
  
```powershell
$domName="<AD DS domain name to join, such as corp.contoso.com>"
$cred=Get-Credential -Message "Type the name and password of a domain acccount."
Add-Computer -DomainName $domName -Credential $cred
Restart-Computer
```

<span data-ttu-id="31b2a-205">이 단계를 성공적으로 완료하면 자리 표시자 컴퓨터 이름이 포함된 다음 구성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-205">Here is the configuration resulting from the successful completion of this phase, with placeholder computer names.</span></span>
  
<span data-ttu-id="31b2a-206">**2 단계: Azure의 고가용성 페더레이션 인증 인프라에 대 한 도메인 컨트롤러 및 디렉터리 동기화 서버**</span><span class="sxs-lookup"><span data-stu-id="31b2a-206">**Phase 2: The domain controllers and directory synchronization server for your high availability federated authentication infrastructure in Azure**</span></span>

![도메인 컨트롤러와 함께 Azure의 고가용성 Microsoft 365 페더레이션 인증 인프라 2 단계](../media/b0c1013b-3fb4-499e-93c1-bf310d8f4c32.png)
  
## <a name="next-step"></a><span data-ttu-id="31b2a-208">다음 단계</span><span class="sxs-lookup"><span data-stu-id="31b2a-208">Next step</span></span>

<span data-ttu-id="31b2a-209">[3 단계: CONFIGURE AD FS servers](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md) 을 사용 하 여이 작업을 계속 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b2a-209">Use [Phase 3: Configure AD FS servers](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md) to continue configuring this workload.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31b2a-210">참고 항목</span><span class="sxs-lookup"><span data-stu-id="31b2a-210">See Also</span></span>

[<span data-ttu-id="31b2a-211">Azure에서 Microsoft 365용 고가용성 페더레이션 인증 배포</span><span class="sxs-lookup"><span data-stu-id="31b2a-211">Deploy high availability federated authentication for Microsoft 365 in Azure</span></span>](deploy-high-availability-federated-authentication-for-microsoft-365-in-azure.md)
  
[<span data-ttu-id="31b2a-212">Microsoft 365 개발/테스트 환경용 페더레이션 id</span><span class="sxs-lookup"><span data-stu-id="31b2a-212">Federated identity for your Microsoft 365 dev/test environment</span></span>](federated-identity-for-your-microsoft-365-dev-test-environment.md)
  
[<span data-ttu-id="31b2a-213">Microsoft 365 솔루션 및 아키텍처 센터</span><span class="sxs-lookup"><span data-stu-id="31b2a-213">Microsoft 365 solution and architecture center</span></span>](../solutions/solution-architecture-center.md)

