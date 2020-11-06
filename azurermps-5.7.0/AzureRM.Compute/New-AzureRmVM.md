---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427617"
---
# <span data-ttu-id="9eb55-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb55-101">New-AzureRmVM</span></span>

## <span data-ttu-id="9eb55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9eb55-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb55-103">Cria uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9eb55-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eb55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9eb55-104">SYNTAX</span></span>

### <span data-ttu-id="9eb55-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9eb55-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eb55-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eb55-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eb55-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eb55-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eb55-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9eb55-108">DESCRIPTION</span></span>
<span data-ttu-id="9eb55-109">O cmdlet **New-AzureRmVM** cria uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="9eb55-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="9eb55-110">Esse cmdlet usa um objeto de máquina virtual como entrada.</span><span class="sxs-lookup"><span data-stu-id="9eb55-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="9eb55-111">Use o cmdlet New-AzureRmVMConfig para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9eb55-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="9eb55-112">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="9eb55-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="9eb55-113">O `SimpleParameterSet` fornece um método conveniente para criar uma VM, fazendo com que argumentos comuns de criação de VM sejam opcionais.</span><span class="sxs-lookup"><span data-stu-id="9eb55-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="9eb55-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9eb55-114">EXAMPLES</span></span>

### <span data-ttu-id="9eb55-115">Exemplo 1: criar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="9eb55-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="9eb55-116">Este script de exemplo mostra como criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9eb55-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="9eb55-117">O script solicitará um nome de usuário e uma senha para a VM.</span><span class="sxs-lookup"><span data-stu-id="9eb55-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="9eb55-118">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="9eb55-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="9eb55-119">Exemplo 2: criar uma máquina virtual a partir de uma imagem de usuário personalizada</span><span class="sxs-lookup"><span data-stu-id="9eb55-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="9eb55-120">Este exemplo assume uma imagem de sistema operacional personalizada generalizada e em um sys existente e anexa um disco de dados a ele, provisiona uma nova rede, implanta o VHD e executa-o.</span><span class="sxs-lookup"><span data-stu-id="9eb55-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="9eb55-121">Esse script pode ser usado para provisionamento automático porque ele usa as credenciais de administrador da máquina virtual local embutidas em vez de chamar **Get-Credential** que requer interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9eb55-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="9eb55-122">Esse script pressupõe que você já esteja conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="9eb55-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="9eb55-123">Você pode confirmar seu status de logon usando o cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="9eb55-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="9eb55-124">OS</span><span class="sxs-lookup"><span data-stu-id="9eb55-124">PARAMETERS</span></span>

### <span data-ttu-id="9eb55-125">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9eb55-125">-AddressPrefix</span></span>
<span data-ttu-id="9eb55-126">O prefixo de endereço para a rede virtual que será criada para a VM.</span><span class="sxs-lookup"><span data-stu-id="9eb55-126">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-127">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="9eb55-127">-AllocationMethod</span></span>
<span data-ttu-id="9eb55-128">O método de alocação de IP para o IP público que será criado para a VM.</span><span class="sxs-lookup"><span data-stu-id="9eb55-128">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9eb55-129">-AsJob</span></span>
<span data-ttu-id="9eb55-130">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="9eb55-130">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-131">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="9eb55-131">-AvailabilitySetName</span></span>
<span data-ttu-id="9eb55-132">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="9eb55-132">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-133">-Credential</span><span class="sxs-lookup"><span data-stu-id="9eb55-133">-Credential</span></span>
<span data-ttu-id="9eb55-134">As credenciais de administrador para a VM.</span><span class="sxs-lookup"><span data-stu-id="9eb55-134">The administrator credentials for the VM.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-135">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="9eb55-135">-DataDiskSizeInGb</span></span>
<span data-ttu-id="9eb55-136">Especifica o tamanho dos discos de dados em GB.</span><span class="sxs-lookup"><span data-stu-id="9eb55-136">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb55-137">-DefaultProfile</span></span>
<span data-ttu-id="9eb55-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9eb55-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-139">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="9eb55-139">-DisableBginfoExtension</span></span>
<span data-ttu-id="9eb55-140">Indica que esse cmdlet não instala a extensão de **informações BG** na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9eb55-140">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-141">-DISKFILE</span><span class="sxs-lookup"><span data-stu-id="9eb55-141">-DiskFile</span></span>
<span data-ttu-id="9eb55-142">O caminho local para o arquivo de disco rígido virtual a ser carregado na nuvem e para a criação da VM, e ele deve ter '. vhd ' como sufixo.</span><span class="sxs-lookup"><span data-stu-id="9eb55-142">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-143">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="9eb55-143">-DomainNameLabel</span></span>
<span data-ttu-id="9eb55-144">O rótulo de subdomínio para o nome de domínio totalmente qualificado (FQDN) da VM.</span><span class="sxs-lookup"><span data-stu-id="9eb55-144">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="9eb55-145">Isso vai pegar a forma `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="9eb55-145">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-146">-ImageName</span><span class="sxs-lookup"><span data-stu-id="9eb55-146">-ImageName</span></span>
<span data-ttu-id="9eb55-147">O nome da imagem amigável na qual a VM será criada.</span><span class="sxs-lookup"><span data-stu-id="9eb55-147">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="9eb55-148">Eles incluem: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="9eb55-148">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9eb55-149">-LicenseType</span></span>
<span data-ttu-id="9eb55-150">Especifica um tipo de licença, que indica que a imagem ou o disco da máquina virtual foram licenciados no local.</span><span class="sxs-lookup"><span data-stu-id="9eb55-150">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="9eb55-151">Esse valor é usado apenas para imagens que contêm o sistema operacional Windows Server.</span><span class="sxs-lookup"><span data-stu-id="9eb55-151">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="9eb55-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9eb55-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9eb55-153">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="9eb55-153">Windows_Client</span></span>
- <span data-ttu-id="9eb55-154">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="9eb55-154">Windows_Server</span></span>

<span data-ttu-id="9eb55-155">Esse valor não pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9eb55-155">This value cannot be updated.</span></span>
<span data-ttu-id="9eb55-156">Se você especificar esse parâmetro para uma atualização, o valor deve coincidir com o valor inicial da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9eb55-156">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-157">-Linux</span><span class="sxs-lookup"><span data-stu-id="9eb55-157">-Linux</span></span>
<span data-ttu-id="9eb55-158">Indica se o arquivo de disco é para VM Linux, se especificado; ou Windows, se não especificado por padrão.</span><span class="sxs-lookup"><span data-stu-id="9eb55-158">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-159">-Local</span><span class="sxs-lookup"><span data-stu-id="9eb55-159">-Location</span></span>
<span data-ttu-id="9eb55-160">Especifica um local para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9eb55-160">Specifies a location for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-161">-Nome</span><span class="sxs-lookup"><span data-stu-id="9eb55-161">-Name</span></span>
<span data-ttu-id="9eb55-162">O nome do recurso VM.</span><span class="sxs-lookup"><span data-stu-id="9eb55-162">The name of the VM resource.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-163">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="9eb55-163">-OpenPorts</span></span>
<span data-ttu-id="9eb55-164">Uma lista de portas a serem abertas no grupo de segurança de rede (NSG) para a VM criada.</span><span class="sxs-lookup"><span data-stu-id="9eb55-164">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="9eb55-165">O valor padrão depende do tipo de imagem escolhido (isto é, Windows: 3389, 5985 e Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="9eb55-165">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-166">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="9eb55-166">-PublicIpAddressName</span></span>
<span data-ttu-id="9eb55-167">O nome de um endereço IP público novo (ou existente) para o qual a VM criada deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="9eb55-167">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="9eb55-168">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="9eb55-168">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb55-169">-ResourceGroupName</span></span>
<span data-ttu-id="9eb55-170">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9eb55-170">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-171">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb55-171">-SecurityGroupName</span></span>
<span data-ttu-id="9eb55-172">O nome de um novo (ou existente) grupo de segurança de rede (NSG) para a VM criada a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9eb55-172">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="9eb55-173">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="9eb55-173">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-174">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="9eb55-174">-Size</span></span>
<span data-ttu-id="9eb55-175">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9eb55-175">The Virtual Machine Size.</span></span>  <span data-ttu-id="9eb55-176">O valor padrão é: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="9eb55-176">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-177">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9eb55-177">-SubnetAddressPrefix</span></span>
<span data-ttu-id="9eb55-178">O prefixo de endereço para a sub-rede que será criada para a VM.</span><span class="sxs-lookup"><span data-stu-id="9eb55-178">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-179">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="9eb55-179">-SubnetName</span></span>
<span data-ttu-id="9eb55-180">O nome de uma nova sub-rede (ou existente) para a VM criada usar.</span><span class="sxs-lookup"><span data-stu-id="9eb55-180">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="9eb55-181">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="9eb55-181">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-182">-Marca</span><span class="sxs-lookup"><span data-stu-id="9eb55-182">-Tag</span></span>
<span data-ttu-id="9eb55-183">Especifica que recursos e grupos de recursos podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="9eb55-183">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="9eb55-184">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="9eb55-184">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="9eb55-185">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="9eb55-185">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-186">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="9eb55-186">-VirtualNetworkName</span></span>
<span data-ttu-id="9eb55-187">O nome de uma nova rede virtual (ou existente) para a VM criada usar.</span><span class="sxs-lookup"><span data-stu-id="9eb55-187">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="9eb55-188">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="9eb55-188">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-189">-VM</span><span class="sxs-lookup"><span data-stu-id="9eb55-189">-VM</span></span>
<span data-ttu-id="9eb55-190">Especifica uma máquina virtual local a ser criada.</span><span class="sxs-lookup"><span data-stu-id="9eb55-190">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="9eb55-191">Para obter um objeto de máquina virtual, use o cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="9eb55-191">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="9eb55-192">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage e Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="9eb55-192">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-193">-Zone</span><span class="sxs-lookup"><span data-stu-id="9eb55-193">-Zone</span></span>
<span data-ttu-id="9eb55-194">Especifica a lista de zonas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9eb55-194">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-195">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9eb55-195">-Confirm</span></span>
<span data-ttu-id="9eb55-196">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eb55-196">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb55-197">-WhatIf</span></span>
<span data-ttu-id="9eb55-198">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9eb55-198">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9eb55-199">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9eb55-199">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb55-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb55-200">CommonParameters</span></span>
<span data-ttu-id="9eb55-201">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eb55-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb55-202">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eb55-202">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb55-203">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9eb55-203">INPUTS</span></span>

### <span data-ttu-id="9eb55-204">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9eb55-204">PSVirtualMachine</span></span>
<span data-ttu-id="9eb55-205">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="9eb55-205">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9eb55-206">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9eb55-206">OUTPUTS</span></span>

### <span data-ttu-id="9eb55-207">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9eb55-207">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9eb55-208">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9eb55-208">NOTES</span></span>

## <span data-ttu-id="9eb55-209">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9eb55-209">RELATED LINKS</span></span>

[<span data-ttu-id="9eb55-210">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb55-210">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9eb55-211">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb55-211">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="9eb55-212">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb55-212">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="9eb55-213">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb55-213">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="9eb55-214">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb55-214">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="9eb55-215">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb55-215">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="9eb55-216">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9eb55-216">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="9eb55-217">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9eb55-217">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="9eb55-218">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9eb55-218">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="9eb55-219">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9eb55-219">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="9eb55-220">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="9eb55-220">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="9eb55-221">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="9eb55-221">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


