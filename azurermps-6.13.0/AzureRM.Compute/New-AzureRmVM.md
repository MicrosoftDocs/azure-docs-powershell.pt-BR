---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: da307e1bc5bca5c3127e33a32bb4480148fe14a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603000"
---
# <span data-ttu-id="5bffb-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5bffb-101">New-AzureRmVM</span></span>

## <span data-ttu-id="5bffb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bffb-102">SYNOPSIS</span></span>
<span data-ttu-id="5bffb-103">Cria uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bffb-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bffb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bffb-104">SYNTAX</span></span>

### <span data-ttu-id="5bffb-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5bffb-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bffb-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bffb-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bffb-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bffb-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bffb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5bffb-108">DESCRIPTION</span></span>
<span data-ttu-id="5bffb-109">O cmdlet **New-AzureRmVM** cria uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="5bffb-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="5bffb-110">Esse cmdlet usa um objeto de máquina virtual como entrada.</span><span class="sxs-lookup"><span data-stu-id="5bffb-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="5bffb-111">Use o cmdlet New-AzureRmVMConfig para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bffb-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="5bffb-112">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="5bffb-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>
<span data-ttu-id="5bffb-113">O `SimpleParameterSet` fornece um método conveniente para criar uma VM, fazendo com que argumentos comuns de criação de VM sejam opcionais.</span><span class="sxs-lookup"><span data-stu-id="5bffb-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="5bffb-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bffb-114">EXAMPLES</span></span>

### <span data-ttu-id="5bffb-115">Exemplo 1: criar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="5bffb-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="5bffb-116">Este script de exemplo mostra como criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bffb-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="5bffb-117">O script solicitará um nome de usuário e uma senha para a VM.</span><span class="sxs-lookup"><span data-stu-id="5bffb-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="5bffb-118">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5bffb-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="5bffb-119">Exemplo 2: criar uma máquina virtual a partir de uma imagem de usuário personalizada</span><span class="sxs-lookup"><span data-stu-id="5bffb-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="5bffb-120">Este exemplo assume uma imagem de sistema operacional personalizada generalizada e em um sys existente e anexa um disco de dados a ele, provisiona uma nova rede, implanta o VHD e executa-o.</span><span class="sxs-lookup"><span data-stu-id="5bffb-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="5bffb-121">Esse script pode ser usado para provisionamento automático porque ele usa as credenciais de administrador da máquina virtual local embutidas em vez de chamar **Get-Credential** que requer interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5bffb-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="5bffb-122">Esse script pressupõe que você já esteja conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="5bffb-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="5bffb-123">Você pode confirmar seu status de logon usando o cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="5bffb-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

### <span data-ttu-id="5bffb-124">Exemplo 3: criar uma VM a partir de uma imagem do Marketplace sem um IP público</span><span class="sxs-lookup"><span data-stu-id="5bffb-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="5bffb-125">Este exemplo provisiona uma nova rede e implanta uma VM do Windows a partir do Marketplace sem criar um endereço IP público ou um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="5bffb-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="5bffb-126">Esse script pode ser usado para provisionamento automático porque ele usa as credenciais de administrador da máquina virtual local embutidas em vez de chamar **Get-Credential** que requer interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5bffb-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="5bffb-127">OS</span><span class="sxs-lookup"><span data-stu-id="5bffb-127">PARAMETERS</span></span>

### <span data-ttu-id="5bffb-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5bffb-128">-AddressPrefix</span></span>
<span data-ttu-id="5bffb-129">O prefixo de endereço para a rede virtual que será criada para a VM.</span><span class="sxs-lookup"><span data-stu-id="5bffb-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="5bffb-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="5bffb-130">-AllocationMethod</span></span>
<span data-ttu-id="5bffb-131">O método de alocação de IP para o IP público que será criado para a VM.</span><span class="sxs-lookup"><span data-stu-id="5bffb-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="5bffb-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bffb-132">-AsJob</span></span>
<span data-ttu-id="5bffb-133">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="5bffb-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5bffb-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="5bffb-134">-AvailabilitySetName</span></span>
<span data-ttu-id="5bffb-135">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5bffb-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="5bffb-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="5bffb-136">-Credential</span></span>
<span data-ttu-id="5bffb-137">As credenciais de administrador para a VM.</span><span class="sxs-lookup"><span data-stu-id="5bffb-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="5bffb-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="5bffb-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="5bffb-139">Especifica o tamanho dos discos de dados em GB.</span><span class="sxs-lookup"><span data-stu-id="5bffb-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="5bffb-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bffb-140">-DefaultProfile</span></span>
<span data-ttu-id="5bffb-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5bffb-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bffb-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="5bffb-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="5bffb-143">Indica que esse cmdlet não instala a extensão de **informações BG** na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bffb-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="5bffb-144">-DISKFILE</span><span class="sxs-lookup"><span data-stu-id="5bffb-144">-DiskFile</span></span>
<span data-ttu-id="5bffb-145">O caminho local para o arquivo de disco rígido virtual a ser carregado na nuvem e para a criação da VM, e ele deve ter '. vhd ' como sufixo.</span><span class="sxs-lookup"><span data-stu-id="5bffb-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="5bffb-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="5bffb-146">-DomainNameLabel</span></span>
<span data-ttu-id="5bffb-147">O rótulo de subdomínio para o nome de domínio totalmente qualificado (FQDN) da VM.</span><span class="sxs-lookup"><span data-stu-id="5bffb-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="5bffb-148">Isso vai pegar a forma `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="5bffb-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="5bffb-149">-Imagem</span><span class="sxs-lookup"><span data-stu-id="5bffb-149">-Image</span></span>
<span data-ttu-id="5bffb-150">O nome da imagem amigável na qual a VM será criada.</span><span class="sxs-lookup"><span data-stu-id="5bffb-150">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="5bffb-151">Eles incluem: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="5bffb-151">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="5bffb-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5bffb-152">-LicenseType</span></span>
<span data-ttu-id="5bffb-153">Especifica um tipo de licença, que indica que a imagem ou o disco da máquina virtual foram licenciados no local.</span><span class="sxs-lookup"><span data-stu-id="5bffb-153">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="5bffb-154">Esse valor é usado apenas para imagens que contêm o sistema operacional Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5bffb-154">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="5bffb-155">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5bffb-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5bffb-156">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="5bffb-156">Windows_Client</span></span>
- <span data-ttu-id="5bffb-157">Windows_Server não é possível atualizar esse valor.</span><span class="sxs-lookup"><span data-stu-id="5bffb-157">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="5bffb-158">Se você especificar esse parâmetro para uma atualização, o valor deve coincidir com o valor inicial da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bffb-158">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="5bffb-159">-Linux</span><span class="sxs-lookup"><span data-stu-id="5bffb-159">-Linux</span></span>
<span data-ttu-id="5bffb-160">Indica se o arquivo de disco é para VM Linux, se especificado; ou Windows, se não especificado por padrão.</span><span class="sxs-lookup"><span data-stu-id="5bffb-160">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="5bffb-161">-Local</span><span class="sxs-lookup"><span data-stu-id="5bffb-161">-Location</span></span>
<span data-ttu-id="5bffb-162">Especifica um local para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bffb-162">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="5bffb-163">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bffb-163">-Name</span></span>
<span data-ttu-id="5bffb-164">O nome do recurso VM.</span><span class="sxs-lookup"><span data-stu-id="5bffb-164">The name of the VM resource.</span></span>

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

### <span data-ttu-id="5bffb-165">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="5bffb-165">-OpenPorts</span></span>
<span data-ttu-id="5bffb-166">Uma lista de portas a serem abertas no grupo de segurança de rede (NSG) para a VM criada.</span><span class="sxs-lookup"><span data-stu-id="5bffb-166">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="5bffb-167">O valor padrão depende do tipo de imagem escolhido (isto é, Windows: 3389, 5985 e Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="5bffb-167">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="5bffb-168">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="5bffb-168">-PublicIpAddressName</span></span>
<span data-ttu-id="5bffb-169">O nome de um endereço IP público novo (ou existente) para o qual a VM criada deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="5bffb-169">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="5bffb-170">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="5bffb-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="5bffb-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bffb-171">-ResourceGroupName</span></span>
<span data-ttu-id="5bffb-172">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5bffb-172">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5bffb-173">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="5bffb-173">-SecurityGroupName</span></span>
<span data-ttu-id="5bffb-174">O nome de um novo (ou existente) grupo de segurança de rede (NSG) para a VM criada a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5bffb-174">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="5bffb-175">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="5bffb-175">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="5bffb-176">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="5bffb-176">-Size</span></span>
<span data-ttu-id="5bffb-177">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bffb-177">The Virtual Machine Size.</span></span>  <span data-ttu-id="5bffb-178">O valor padrão é: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="5bffb-178">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="5bffb-179">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5bffb-179">-SubnetAddressPrefix</span></span>
<span data-ttu-id="5bffb-180">O prefixo de endereço para a sub-rede que será criada para a VM.</span><span class="sxs-lookup"><span data-stu-id="5bffb-180">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="5bffb-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5bffb-181">-SubnetName</span></span>
<span data-ttu-id="5bffb-182">O nome de uma nova sub-rede (ou existente) para a VM criada usar.</span><span class="sxs-lookup"><span data-stu-id="5bffb-182">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="5bffb-183">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="5bffb-183">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="5bffb-184">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5bffb-184">-SystemAssignedIdentity</span></span>
<span data-ttu-id="5bffb-185">Se o parâmetro estiver presente, a VM será atribuída a uma identidade do sistema gerenciada que é gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5bffb-185">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="5bffb-186">-Marca</span><span class="sxs-lookup"><span data-stu-id="5bffb-186">-Tag</span></span>
<span data-ttu-id="5bffb-187">Especifica que recursos e grupos de recursos podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="5bffb-187">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="5bffb-188">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="5bffb-188">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="5bffb-189">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="5bffb-189">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="5bffb-190">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5bffb-190">-UserAssignedIdentity</span></span>
<span data-ttu-id="5bffb-191">O nome de uma identidade de serviço gerenciado que deve ser atribuída à VM.</span><span class="sxs-lookup"><span data-stu-id="5bffb-191">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="5bffb-192">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5bffb-192">-VirtualNetworkName</span></span>
<span data-ttu-id="5bffb-193">O nome de uma nova rede virtual (ou existente) para a VM criada usar.</span><span class="sxs-lookup"><span data-stu-id="5bffb-193">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="5bffb-194">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="5bffb-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="5bffb-195">-VM</span><span class="sxs-lookup"><span data-stu-id="5bffb-195">-VM</span></span>
<span data-ttu-id="5bffb-196">Especifica uma máquina virtual local a ser criada.</span><span class="sxs-lookup"><span data-stu-id="5bffb-196">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="5bffb-197">Para obter um objeto de máquina virtual, use o cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="5bffb-197">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="5bffb-198">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage e Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="5bffb-198">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="5bffb-199">-Zone</span><span class="sxs-lookup"><span data-stu-id="5bffb-199">-Zone</span></span>
<span data-ttu-id="5bffb-200">Especifica a lista de zonas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bffb-200">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="5bffb-201">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5bffb-201">-Confirm</span></span>
<span data-ttu-id="5bffb-202">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bffb-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bffb-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bffb-203">-WhatIf</span></span>
<span data-ttu-id="5bffb-204">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5bffb-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bffb-205">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bffb-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bffb-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bffb-206">CommonParameters</span></span>
<span data-ttu-id="5bffb-207">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bffb-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bffb-208">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bffb-208">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bffb-209">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5bffb-209">INPUTS</span></span>

### <span data-ttu-id="5bffb-210">System. String</span><span class="sxs-lookup"><span data-stu-id="5bffb-210">System.String</span></span>

### <span data-ttu-id="5bffb-211">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5bffb-211">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5bffb-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="5bffb-212">System.String[]</span></span>

### <span data-ttu-id="5bffb-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5bffb-213">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5bffb-214">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5bffb-214">OUTPUTS</span></span>

### <span data-ttu-id="5bffb-215">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5bffb-215">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="5bffb-216">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5bffb-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5bffb-217">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5bffb-217">NOTES</span></span>

## <span data-ttu-id="5bffb-218">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bffb-218">RELATED LINKS</span></span>

[<span data-ttu-id="5bffb-219">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5bffb-219">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5bffb-220">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5bffb-220">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="5bffb-221">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5bffb-221">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="5bffb-222">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5bffb-222">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="5bffb-223">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5bffb-223">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="5bffb-224">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5bffb-224">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="5bffb-225">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5bffb-225">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="5bffb-226">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5bffb-226">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="5bffb-227">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="5bffb-227">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="5bffb-228">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5bffb-228">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="5bffb-229">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5bffb-229">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="5bffb-230">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="5bffb-230">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


