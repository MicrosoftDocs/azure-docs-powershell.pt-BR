---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 21c15b0395479a1a22e6b8420a97a3a7c0b75bce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261385"
---
# <span data-ttu-id="186cc-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="186cc-101">New-AzVM</span></span>

## <span data-ttu-id="186cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="186cc-102">SYNOPSIS</span></span>
<span data-ttu-id="186cc-103">Cria uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="186cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="186cc-104">SYNTAX</span></span>

### <span data-ttu-id="186cc-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="186cc-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>]
 [-HostId <String>] [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186cc-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="186cc-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186cc-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="186cc-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="186cc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="186cc-108">DESCRIPTION</span></span>
<span data-ttu-id="186cc-109">O cmdlet **New-AzVM** cria uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="186cc-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="186cc-110">Esse cmdlet usa um objeto de máquina virtual como entrada.</span><span class="sxs-lookup"><span data-stu-id="186cc-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="186cc-111">Use o cmdlet New-AzVMConfig para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="186cc-112">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface e Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="186cc-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="186cc-113">O `SimpleParameterSet` fornece um método conveniente para criar uma VM, fazendo com que argumentos comuns de criação de VM sejam opcionais.</span><span class="sxs-lookup"><span data-stu-id="186cc-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="186cc-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="186cc-114">EXAMPLES</span></span>

### <span data-ttu-id="186cc-115">Exemplo 1: criar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="186cc-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="186cc-116">Este script de exemplo mostra como criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="186cc-117">O script solicitará um nome de usuário e uma senha para a VM.</span><span class="sxs-lookup"><span data-stu-id="186cc-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="186cc-118">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="186cc-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="186cc-119">Exemplo 2: criar uma máquina virtual a partir de uma imagem de usuário personalizada</span><span class="sxs-lookup"><span data-stu-id="186cc-119">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account.
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance.
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3"
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="186cc-120">Este exemplo assume uma imagem de sistema operacional personalizada generalizada e em um sys existente e anexa um disco de dados a ele, provisiona uma nova rede, implanta o VHD e executa-o.</span><span class="sxs-lookup"><span data-stu-id="186cc-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="186cc-121">Esse script pode ser usado para provisionamento automático porque ele usa as credenciais de administrador da máquina virtual local embutidas em vez de chamar **Get-Credential** que requer interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="186cc-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="186cc-122">Esse script pressupõe que você já esteja conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="186cc-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="186cc-123">Você pode confirmar seu status de logon usando o cmdlet **Get-AzSubscription** .</span><span class="sxs-lookup"><span data-stu-id="186cc-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="186cc-124">Exemplo 3: criar uma VM a partir de uma imagem do Marketplace sem um IP público</span><span class="sxs-lookup"><span data-stu-id="186cc-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="186cc-125">Este exemplo provisiona uma nova rede e implanta uma VM do Windows a partir do Marketplace sem criar um endereço IP público ou um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="186cc-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="186cc-126">Esse script pode ser usado para provisionamento automático porque ele usa as credenciais de administrador da máquina virtual local embutidas em vez de chamar **Get-Credential** que requer interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="186cc-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="186cc-127">OS</span><span class="sxs-lookup"><span data-stu-id="186cc-127">PARAMETERS</span></span>

### <span data-ttu-id="186cc-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="186cc-128">-AddressPrefix</span></span>
<span data-ttu-id="186cc-129">O prefixo de endereço para a rede virtual que será criada para a VM.</span><span class="sxs-lookup"><span data-stu-id="186cc-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="186cc-130">-AllocationMethod</span></span>
<span data-ttu-id="186cc-131">O método de alocação de IP para o IP público que será criado para a VM.</span><span class="sxs-lookup"><span data-stu-id="186cc-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="186cc-132">-AsJob</span></span>
<span data-ttu-id="186cc-133">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="186cc-133">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="186cc-134">-AvailabilitySetName</span></span>
<span data-ttu-id="186cc-135">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="186cc-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="186cc-136">-Credential</span></span>
<span data-ttu-id="186cc-137">As credenciais de administrador para a VM.</span><span class="sxs-lookup"><span data-stu-id="186cc-137">The administrator credentials for the VM.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="186cc-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="186cc-139">Especifica o tamanho dos discos de dados em GB.</span><span class="sxs-lookup"><span data-stu-id="186cc-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186cc-140">-DefaultProfile</span></span>
<span data-ttu-id="186cc-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="186cc-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="186cc-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="186cc-143">Indica que esse cmdlet não instala a extensão de **informações BG** na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-144">-DISKFILE</span><span class="sxs-lookup"><span data-stu-id="186cc-144">-DiskFile</span></span>
<span data-ttu-id="186cc-145">O caminho local para o arquivo de disco rígido virtual a ser carregado na nuvem e para a criação da VM, e ele deve ter '. vhd ' como sufixo.</span><span class="sxs-lookup"><span data-stu-id="186cc-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="186cc-146">-DomainNameLabel</span></span>
<span data-ttu-id="186cc-147">O rótulo de subdomínio para o nome de domínio totalmente qualificado (FQDN) da VM.</span><span class="sxs-lookup"><span data-stu-id="186cc-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="186cc-148">Isso vai pegar a forma `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="186cc-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="186cc-149">-EnableUltraSSD</span></span>
<span data-ttu-id="186cc-150">Use discos UltraSSD para a VM.</span><span class="sxs-lookup"><span data-stu-id="186cc-150">Use UltraSSD disks for the vm.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="186cc-151">-EvictionPolicy</span></span>
<span data-ttu-id="186cc-152">A política de remoção para a máquina virtual do Azure Spot.</span><span class="sxs-lookup"><span data-stu-id="186cc-152">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="186cc-153">Os valores com suporte são ' canallocate ' e ' Delete '.</span><span class="sxs-lookup"><span data-stu-id="186cc-153">Supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-154">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="186cc-154">-HostGroupId</span></span>
<span data-ttu-id="186cc-155">Especifica o grupo de hosts dedicados no qual a máquina virtual residirá.</span><span class="sxs-lookup"><span data-stu-id="186cc-155">Specifies the dedicated host group the virtual machine will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-156">-Hostid</span><span class="sxs-lookup"><span data-stu-id="186cc-156">-HostId</span></span>
<span data-ttu-id="186cc-157">A ID do host</span><span class="sxs-lookup"><span data-stu-id="186cc-157">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-158">-Imagem</span><span class="sxs-lookup"><span data-stu-id="186cc-158">-Image</span></span>
<span data-ttu-id="186cc-159">O nome da imagem amigável na qual a VM será criada.</span><span class="sxs-lookup"><span data-stu-id="186cc-159">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="186cc-160">Eles incluem: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="186cc-160">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-161">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="186cc-161">-LicenseType</span></span>
<span data-ttu-id="186cc-162">Especifica um tipo de licença, que indica que a imagem ou o disco da máquina virtual foram licenciados no local.</span><span class="sxs-lookup"><span data-stu-id="186cc-162">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="186cc-163">Os possíveis valores para o Windows Server são:</span><span class="sxs-lookup"><span data-stu-id="186cc-163">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="186cc-164">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="186cc-164">Windows_Client</span></span>
- <span data-ttu-id="186cc-165">Windows_Server possíveis valores para o sistema operacional do servidor Linux são:</span><span class="sxs-lookup"><span data-stu-id="186cc-165">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="186cc-166">RHEL_BYOS (para RHEL)</span><span class="sxs-lookup"><span data-stu-id="186cc-166">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="186cc-167">SLES_BYOS (para SUSE)</span><span class="sxs-lookup"><span data-stu-id="186cc-167">SLES_BYOS (for SUSE)</span></span> 

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="186cc-168">-Linux</span></span>
<span data-ttu-id="186cc-169">Indica se o arquivo de disco é para VM Linux, se especificado; ou Windows, se não especificado por padrão.</span><span class="sxs-lookup"><span data-stu-id="186cc-169">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-170">-Local</span><span class="sxs-lookup"><span data-stu-id="186cc-170">-Location</span></span>
<span data-ttu-id="186cc-171">Especifica um local para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-171">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-172">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="186cc-172">-MaxPrice</span></span>
<span data-ttu-id="186cc-173">O preço máximo da cobrança de uma máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="186cc-173">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-174">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="186cc-174">-EncryptionAtHost</span></span>
<span data-ttu-id="186cc-175">A propriedade EncryptionAtHost pode ser usada pelo usuário na solicitação para habilitar ou desabilitar a criptografia do host para a máquina virtual ou o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-175">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="186cc-176">Isso habilitará a criptografia para todos os discos, incluindo o disco de recursos/temporários no próprio host.</span><span class="sxs-lookup"><span data-stu-id="186cc-176">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="186cc-177">Padrão: a criptografia no host será desabilitada, a menos que essa propriedade seja definida como true para o recurso.</span><span class="sxs-lookup"><span data-stu-id="186cc-177">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskParameterSet
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="186cc-178">-Nome</span><span class="sxs-lookup"><span data-stu-id="186cc-178">-Name</span></span>
<span data-ttu-id="186cc-179">O nome do recurso VM.</span><span class="sxs-lookup"><span data-stu-id="186cc-179">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-180">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="186cc-180">-OpenPorts</span></span>
<span data-ttu-id="186cc-181">Uma lista de portas a serem abertas no grupo de segurança de rede (NSG) para a VM criada.</span><span class="sxs-lookup"><span data-stu-id="186cc-181">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="186cc-182">O valor padrão depende do tipo de imagem escolhido (isto é, Windows: 3389, 5985 e Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="186cc-182">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-183">-Priority</span><span class="sxs-lookup"><span data-stu-id="186cc-183">-Priority</span></span>
<span data-ttu-id="186cc-184">A prioridade da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-184">The priority for the virtual machine.</span></span>  <span data-ttu-id="186cc-185">Somente os valores com suporte são ' regular ', ' spot ' e ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="186cc-185">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="186cc-186">' Regular ' é para a máquina virtual normal.</span><span class="sxs-lookup"><span data-stu-id="186cc-186">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="186cc-187">' Spot ' é para máquina virtual Spot.</span><span class="sxs-lookup"><span data-stu-id="186cc-187">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="186cc-188">' Low ' também é para máquina virtual Spot, mas é substituído por ' spot '.</span><span class="sxs-lookup"><span data-stu-id="186cc-188">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="186cc-189">Use ' spot ' em vez de ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="186cc-189">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-190">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="186cc-190">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="186cc-191">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-191">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="186cc-192">-PublicIpAddressName</span></span>
<span data-ttu-id="186cc-193">O nome de um endereço IP público novo (ou existente) para o qual a VM criada deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="186cc-193">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="186cc-194">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="186cc-194">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="186cc-195">-ResourceGroupName</span></span>
<span data-ttu-id="186cc-196">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="186cc-196">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-197">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="186cc-197">-SecurityGroupName</span></span>
<span data-ttu-id="186cc-198">O nome de um novo (ou existente) grupo de segurança de rede (NSG) para a VM criada a ser usada.</span><span class="sxs-lookup"><span data-stu-id="186cc-198">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="186cc-199">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="186cc-199">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-200">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="186cc-200">-Size</span></span>
<span data-ttu-id="186cc-201">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-201">The Virtual Machine Size.</span></span>  <span data-ttu-id="186cc-202">O valor padrão é: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="186cc-202">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="186cc-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="186cc-204">O prefixo de endereço para a sub-rede que será criada para a VM.</span><span class="sxs-lookup"><span data-stu-id="186cc-204">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-205">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="186cc-205">-SubnetName</span></span>
<span data-ttu-id="186cc-206">O nome de uma nova sub-rede (ou existente) para a VM criada usar.</span><span class="sxs-lookup"><span data-stu-id="186cc-206">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="186cc-207">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="186cc-207">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-208">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="186cc-208">-SystemAssignedIdentity</span></span>
<span data-ttu-id="186cc-209">Se o parâmetro estiver presente, a VM será atribuída a uma identidade do sistema gerenciada que é gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="186cc-209">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-210">-Marca</span><span class="sxs-lookup"><span data-stu-id="186cc-210">-Tag</span></span>
<span data-ttu-id="186cc-211">Especifica que recursos e grupos de recursos podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="186cc-211">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="186cc-212">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="186cc-212">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="186cc-213">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="186cc-213">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="186cc-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="186cc-215">O nome de uma identidade de serviço gerenciado que deve ser atribuída à VM.</span><span class="sxs-lookup"><span data-stu-id="186cc-215">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-216">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="186cc-216">-VirtualNetworkName</span></span>
<span data-ttu-id="186cc-217">O nome de uma nova rede virtual (ou existente) para a VM criada usar.</span><span class="sxs-lookup"><span data-stu-id="186cc-217">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="186cc-218">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="186cc-218">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-219">-VM</span><span class="sxs-lookup"><span data-stu-id="186cc-219">-VM</span></span>
<span data-ttu-id="186cc-220">Especifica uma máquina virtual local a ser criada.</span><span class="sxs-lookup"><span data-stu-id="186cc-220">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="186cc-221">Para obter um objeto de máquina virtual, use o cmdlet New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="186cc-221">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="186cc-222">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzVMOperatingSystem, Set-AzVMSourceImage e Add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="186cc-222">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-223">-VmssId</span><span class="sxs-lookup"><span data-stu-id="186cc-223">-VmssId</span></span>
<span data-ttu-id="186cc-224">A ID do conjunto de escala de máquina virtual ao qual esta VM será associada</span><span class="sxs-lookup"><span data-stu-id="186cc-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-225">-Zone</span><span class="sxs-lookup"><span data-stu-id="186cc-225">-Zone</span></span>
<span data-ttu-id="186cc-226">Especifica a lista de zonas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-226">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-227">-Confirme</span><span class="sxs-lookup"><span data-stu-id="186cc-227">-Confirm</span></span>
<span data-ttu-id="186cc-228">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="186cc-228">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-229">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="186cc-229">-WhatIf</span></span>
<span data-ttu-id="186cc-230">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="186cc-230">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="186cc-231">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="186cc-231">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186cc-232">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186cc-232">CommonParameters</span></span>
<span data-ttu-id="186cc-233">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="186cc-233">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186cc-234">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="186cc-234">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186cc-235">SENSORES</span><span class="sxs-lookup"><span data-stu-id="186cc-235">INPUTS</span></span>

### <span data-ttu-id="186cc-236">System. String</span><span class="sxs-lookup"><span data-stu-id="186cc-236">System.String</span></span>

### <span data-ttu-id="186cc-237">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="186cc-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="186cc-238">System. String []</span><span class="sxs-lookup"><span data-stu-id="186cc-238">System.String[]</span></span>

### <span data-ttu-id="186cc-239">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="186cc-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="186cc-240">EXIBE</span><span class="sxs-lookup"><span data-stu-id="186cc-240">OUTPUTS</span></span>

### <span data-ttu-id="186cc-241">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="186cc-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="186cc-242">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="186cc-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="186cc-243">INFORMA</span><span class="sxs-lookup"><span data-stu-id="186cc-243">NOTES</span></span>

## <span data-ttu-id="186cc-244">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="186cc-244">RELATED LINKS</span></span>

[<span data-ttu-id="186cc-245">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="186cc-245">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="186cc-246">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="186cc-246">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="186cc-247">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="186cc-247">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="186cc-248">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="186cc-248">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="186cc-249">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="186cc-249">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="186cc-250">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="186cc-250">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="186cc-251">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="186cc-251">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="186cc-252">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="186cc-252">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="186cc-253">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="186cc-253">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="186cc-254">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="186cc-254">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="186cc-255">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="186cc-255">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="186cc-256">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="186cc-256">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


