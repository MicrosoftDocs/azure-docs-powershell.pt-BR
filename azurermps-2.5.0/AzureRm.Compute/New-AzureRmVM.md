---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: f7f19a46a8a7f0bfd0e9ec20fe40201e4bea668a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786171"
---
# <span data-ttu-id="d9a06-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d9a06-101">New-AzureRmVM</span></span>

## <span data-ttu-id="d9a06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9a06-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a06-103">Cria uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9a06-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9a06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9a06-104">SYNTAX</span></span>

### <span data-ttu-id="d9a06-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9a06-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a06-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9a06-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a06-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9a06-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a06-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9a06-108">DESCRIPTION</span></span>
<span data-ttu-id="d9a06-109">O cmdlet **New-AzureRmVM** cria uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a06-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="d9a06-110">Esse cmdlet usa um objeto de máquina virtual como entrada.</span><span class="sxs-lookup"><span data-stu-id="d9a06-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="d9a06-111">Use o cmdlet New-AzureRmVMConfig para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9a06-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="d9a06-112">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="d9a06-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="d9a06-113">O `SimpleParameterSet` fornece um método conveniente para criar uma VM, fazendo com que argumentos comuns de criação de VM sejam opcionais.</span><span class="sxs-lookup"><span data-stu-id="d9a06-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="d9a06-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9a06-114">EXAMPLES</span></span>

### <span data-ttu-id="d9a06-115">Exemplo 1: criar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d9a06-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm
```

<span data-ttu-id="d9a06-116">Este script de exemplo mostra como criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9a06-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="d9a06-117">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d9a06-117">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="d9a06-118">Exemplo 2: criar uma máquina virtual a partir de uma imagem de usuário personalizada</span><span class="sxs-lookup"><span data-stu-id="d9a06-118">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="d9a06-119">Este exemplo assume uma imagem de sistema operacional personalizada generalizada e em um sys existente e anexa um disco de dados a ele, provisiona uma nova rede, implanta o VHD e executa-o.</span><span class="sxs-lookup"><span data-stu-id="d9a06-119">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="d9a06-120">Esse script pode ser usado para provisionamento automático porque ele usa as credenciais de administrador da máquina virtual local embutidas em vez de chamar **Get-Credential** que requer interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d9a06-120">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="d9a06-121">Esse script pressupõe que você já esteja conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a06-121">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="d9a06-122">Você pode confirmar seu status de logon usando o cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="d9a06-122">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="d9a06-123">OS</span><span class="sxs-lookup"><span data-stu-id="d9a06-123">PARAMETERS</span></span>

### <span data-ttu-id="d9a06-124">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d9a06-124">-AddressPrefix</span></span>
<span data-ttu-id="d9a06-125">O prefixo de endereço para a rede virtual que será criada para a VM.</span><span class="sxs-lookup"><span data-stu-id="d9a06-125">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="d9a06-126">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="d9a06-126">-AllocationMethod</span></span>
<span data-ttu-id="d9a06-127">O método de alocação de IP para o IP público que será criado para a VM.</span><span class="sxs-lookup"><span data-stu-id="d9a06-127">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="d9a06-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9a06-128">-AsJob</span></span>
<span data-ttu-id="d9a06-129">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="d9a06-129">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d9a06-130">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="d9a06-130">-AvailabilitySetName</span></span>
<span data-ttu-id="d9a06-131">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d9a06-131">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="d9a06-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="d9a06-132">-Credential</span></span>
<span data-ttu-id="d9a06-133">As credenciais de administrador para a VM.</span><span class="sxs-lookup"><span data-stu-id="d9a06-133">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="d9a06-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a06-134">-DefaultProfile</span></span>
<span data-ttu-id="d9a06-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a06-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9a06-136">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="d9a06-136">-DisableBginfoExtension</span></span>
<span data-ttu-id="d9a06-137">Indica que esse cmdlet não instala a extensão de **informações BG** na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9a06-137">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="d9a06-138">-DISKFILE</span><span class="sxs-lookup"><span data-stu-id="d9a06-138">-DiskFile</span></span>
<span data-ttu-id="d9a06-139">O caminho local para o arquivo de disco rígido virtual a ser carregado na nuvem e para a criação da VM, e ele deve ter '. vhd ' como sufixo.</span><span class="sxs-lookup"><span data-stu-id="d9a06-139">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="d9a06-140">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="d9a06-140">-DomainNameLabel</span></span>
<span data-ttu-id="d9a06-141">O rótulo de subdomínio para o nome de domínio totalmente qualificado (FQDN) da VM.</span><span class="sxs-lookup"><span data-stu-id="d9a06-141">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="d9a06-142">Isso vai pegar a forma `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="d9a06-142">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="d9a06-143">-ImageName</span><span class="sxs-lookup"><span data-stu-id="d9a06-143">-ImageName</span></span>
<span data-ttu-id="d9a06-144">O nome da imagem amigável na qual a VM será criada.</span><span class="sxs-lookup"><span data-stu-id="d9a06-144">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="d9a06-145">Eles incluem: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="d9a06-145">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="d9a06-146">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d9a06-146">-LicenseType</span></span>
<span data-ttu-id="d9a06-147">Especifica um tipo de licença, que indica que a imagem ou o disco da máquina virtual foram licenciados no local.</span><span class="sxs-lookup"><span data-stu-id="d9a06-147">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="d9a06-148">Esse valor é usado apenas para imagens que contêm o sistema operacional Windows Server.</span><span class="sxs-lookup"><span data-stu-id="d9a06-148">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="d9a06-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d9a06-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9a06-150">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="d9a06-150">Windows_Client</span></span> 
- <span data-ttu-id="d9a06-151">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="d9a06-151">Windows_Server</span></span>

<span data-ttu-id="d9a06-152">Esse valor não pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="d9a06-152">This value cannot be updated.</span></span>
<span data-ttu-id="d9a06-153">Se você especificar esse parâmetro para uma atualização, o valor deve coincidir com o valor inicial da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9a06-153">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="d9a06-154">-Linux</span><span class="sxs-lookup"><span data-stu-id="d9a06-154">-Linux</span></span>
<span data-ttu-id="d9a06-155">Indica se o arquivo de disco é para VM Linux, se especificado; ou Windows, se não especificado por padrão.</span><span class="sxs-lookup"><span data-stu-id="d9a06-155">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="d9a06-156">-Local</span><span class="sxs-lookup"><span data-stu-id="d9a06-156">-Location</span></span>
<span data-ttu-id="d9a06-157">Especifica um local para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9a06-157">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="d9a06-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9a06-158">-Name</span></span>
<span data-ttu-id="d9a06-159">O nome do recurso VM.</span><span class="sxs-lookup"><span data-stu-id="d9a06-159">The name of the VM resource.</span></span>

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

### <span data-ttu-id="d9a06-160">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="d9a06-160">-OpenPorts</span></span>
<span data-ttu-id="d9a06-161">Uma lista de portas a serem abertas no grupo de segurança de rede (NSG) para a VM criada.</span><span class="sxs-lookup"><span data-stu-id="d9a06-161">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="d9a06-162">O valor padrão depende do tipo de imagem escolhido (isto é, Windows: 3389, 5985 e Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="d9a06-162">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="d9a06-163">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="d9a06-163">-PublicIpAddressName</span></span>
<span data-ttu-id="d9a06-164">O nome de um endereço IP público novo (ou existente) para o qual a VM criada deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="d9a06-164">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="d9a06-165">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="d9a06-165">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="d9a06-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a06-166">-ResourceGroupName</span></span>
<span data-ttu-id="d9a06-167">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9a06-167">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d9a06-168">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a06-168">-SecurityGroupName</span></span>
<span data-ttu-id="d9a06-169">O nome de um novo (ou existente) grupo de segurança de rede (NSG) para a VM criada a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d9a06-169">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="d9a06-170">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="d9a06-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="d9a06-171">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="d9a06-171">-Size</span></span>
<span data-ttu-id="d9a06-172">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9a06-172">The Virtual Machine Size.</span></span>  <span data-ttu-id="d9a06-173">O valor padrão é: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="d9a06-173">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="d9a06-174">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d9a06-174">-SubnetAddressPrefix</span></span>
<span data-ttu-id="d9a06-175">O prefixo de endereço para a sub-rede que será criada para a VM.</span><span class="sxs-lookup"><span data-stu-id="d9a06-175">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="d9a06-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d9a06-176">-SubnetName</span></span>
<span data-ttu-id="d9a06-177">O nome de uma nova sub-rede (ou existente) para a VM criada usar.</span><span class="sxs-lookup"><span data-stu-id="d9a06-177">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="d9a06-178">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="d9a06-178">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="d9a06-179">-Marca</span><span class="sxs-lookup"><span data-stu-id="d9a06-179">-Tag</span></span>
<span data-ttu-id="d9a06-180">Especifica que recursos e grupos de recursos podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="d9a06-180">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="d9a06-181">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="d9a06-181">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="d9a06-182">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="d9a06-182">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="d9a06-183">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d9a06-183">-VirtualNetworkName</span></span>
<span data-ttu-id="d9a06-184">O nome de uma nova rede virtual (ou existente) para a VM criada usar.</span><span class="sxs-lookup"><span data-stu-id="d9a06-184">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="d9a06-185">Se não for especificado, um nome será gerado.</span><span class="sxs-lookup"><span data-stu-id="d9a06-185">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="d9a06-186">-VM</span><span class="sxs-lookup"><span data-stu-id="d9a06-186">-VM</span></span>
<span data-ttu-id="d9a06-187">Especifica uma máquina virtual local a ser criada.</span><span class="sxs-lookup"><span data-stu-id="d9a06-187">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="d9a06-188">Para obter um objeto de máquina virtual, use o cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="d9a06-188">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="d9a06-189">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage e Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="d9a06-189">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="d9a06-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="d9a06-190">-Zone</span></span>
<span data-ttu-id="d9a06-191">Especifica a lista de zonas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9a06-191">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="d9a06-192">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9a06-192">-Confirm</span></span>
<span data-ttu-id="d9a06-193">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9a06-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a06-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a06-194">-WhatIf</span></span>
<span data-ttu-id="d9a06-195">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9a06-195">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d9a06-196">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9a06-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a06-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a06-197">CommonParameters</span></span>
<span data-ttu-id="d9a06-198">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a06-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a06-199">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a06-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a06-200">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9a06-200">INPUTS</span></span>

### <span data-ttu-id="d9a06-201">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d9a06-201">PSVirtualMachine</span></span>
<span data-ttu-id="d9a06-202">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d9a06-202">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d9a06-203">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9a06-203">OUTPUTS</span></span>

### <span data-ttu-id="d9a06-204">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d9a06-204">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d9a06-205">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9a06-205">NOTES</span></span>

## <span data-ttu-id="d9a06-206">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9a06-206">RELATED LINKS</span></span>

[<span data-ttu-id="d9a06-207">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d9a06-207">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="d9a06-208">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d9a06-208">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="d9a06-209">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d9a06-209">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="d9a06-210">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d9a06-210">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="d9a06-211">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d9a06-211">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="d9a06-212">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d9a06-212">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="d9a06-213">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d9a06-213">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="d9a06-214">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d9a06-214">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="d9a06-215">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="d9a06-215">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="d9a06-216">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d9a06-216">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="d9a06-217">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="d9a06-217">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="d9a06-218">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="d9a06-218">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


