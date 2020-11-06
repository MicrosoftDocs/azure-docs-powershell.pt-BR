---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: a5a15ed27b5a862513b15667b343e932dc2571e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441168"
---
# <span data-ttu-id="ad2d8-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad2d8-101">New-AzureRmVM</span></span>

## <span data-ttu-id="ad2d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad2d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2d8-103">Cria uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad2d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad2d8-104">SYNTAX</span></span>

```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tags <Hashtable>] [-LicenseType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad2d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ad2d8-106">O cmdlet **New-AzureRmVM** cria uma máquina virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-106">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="ad2d8-107">Esse cmdlet usa um objeto de máquina virtual como entrada.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-107">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="ad2d8-108">Use o cmdlet New-AzureRmVMConfig para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-108">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="ad2d8-109">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-109">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="ad2d8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad2d8-110">EXAMPLES</span></span>

### <span data-ttu-id="ad2d8-111">Exemplo 1: criar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ad2d8-111">Example 1: Create a virtual machine</span></span>
```
PS C:\> # Variables    
## Global
$ResourceGroupName = "ResourceGroup11"
$Location = "WestEurope"

## Storage
$StorageName = "generalstorage6cc"
$StorageType = "Standard_GRS"

## Network
$InterfaceName = "ServerInterface06"
$Subnet1Name = "Subnet1"
$VNetName = "VNet09"
$VNetAddressPrefix = "10.0.0.0/16"
$VNetSubnetAddressPrefix = "10.0.0.0/24"

## Compute
$VMName = "VirtualMachine12"
$ComputerName = "Server22"
$VMSize = "Standard_A2"
$OSDiskName = $VMName + "OSDisk"

# Resource Group
New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Type $StorageType -Location $Location

# Network
$PIp = New-AzureRmPublicIpAddress -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -AllocationMethod Dynamic
$SubnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name $Subnet1Name -AddressPrefix $VNetSubnetAddressPrefix
$VNet = New-AzureRmVirtualNetwork -Name $VNetName -ResourceGroupName $ResourceGroupName -Location $Location -AddressPrefix $VNetAddressPrefix -Subnet $SubnetConfig
$Interface = New-AzureRmNetworkInterface -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -SubnetId $VNet.Subnets[0].Id -PublicIpAddressId $PIp.Id

# Compute

## Setup local VM object
$Credential = Get-Credential
$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2012-R2-Datacenter -Version "latest"
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $Interface.Id
$OSDiskUri = $StorageAccount.PrimaryEndpoints.Blob.ToString() + "vhds/" + $OSDiskName + ".vhd"
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -CreateOption FromImage

## Create the VM in Azure
New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $Location -VM $VirtualMachine
```

<span data-ttu-id="ad2d8-112">Este script de exemplo mostra como criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-112">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="ad2d8-113">Esse script usa vários outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="ad2d8-114">Exemplo 2: criar uma máquina virtual a partir de uma imagem de usuário personalizada</span><span class="sxs-lookup"><span data-stu-id="ad2d8-114">Example 2: Create a virtual machine from a custom user image</span></span>
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

$Crededntial = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword); 

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="ad2d8-115">Este exemplo assume uma imagem de sistema operacional personalizada generalizada e em um sys existente e anexa um disco de dados a ele, provisiona uma nova rede, implanta o VHD e executa-o.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-115">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="ad2d8-116">Esse script pode ser usado para provisionamento automático porque ele usa as credenciais de administrador da máquina virtual local embutidas em vez de chamar **Get-Credential** que requer interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-116">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="ad2d8-117">Esse script pressupõe que você já esteja conectado à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-117">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="ad2d8-118">Você pode confirmar seu status de logon usando o cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="ad2d8-118">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="ad2d8-119">OS</span><span class="sxs-lookup"><span data-stu-id="ad2d8-119">PARAMETERS</span></span>

### <span data-ttu-id="ad2d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2d8-120">-DefaultProfile</span></span>
<span data-ttu-id="ad2d8-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad2d8-122">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="ad2d8-122">-DisableBginfoExtension</span></span>
<span data-ttu-id="ad2d8-123">Indica que esse cmdlet não instala a extensão de **informações BG** na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-123">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="ad2d8-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ad2d8-124">-LicenseType</span></span>
<span data-ttu-id="ad2d8-125">Especifica um tipo de licença, que indica que a imagem ou o disco da máquina virtual foram licenciados no local.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-125">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="ad2d8-126">Esse valor é usado apenas para imagens que contêm o sistema operacional Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-126">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="ad2d8-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ad2d8-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad2d8-128">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="ad2d8-128">Windows_Client</span></span> 
- <span data-ttu-id="ad2d8-129">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="ad2d8-129">Windows_Server</span></span>

<span data-ttu-id="ad2d8-130">Esse valor não pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-130">This value cannot be updated.</span></span>
<span data-ttu-id="ad2d8-131">Se você especificar esse parâmetro para uma atualização, o valor deve coincidir com o valor inicial da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-131">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d8-132">-Local</span><span class="sxs-lookup"><span data-stu-id="ad2d8-132">-Location</span></span>
<span data-ttu-id="ad2d8-133">Especifica um local para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-133">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2d8-134">-ResourceGroupName</span></span>
<span data-ttu-id="ad2d8-135">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-135">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d8-136">-Marcas</span><span class="sxs-lookup"><span data-stu-id="ad2d8-136">-Tags</span></span>
<span data-ttu-id="ad2d8-137">Especifica que recursos e grupos de recursos podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-137">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="ad2d8-138">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-138">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="ad2d8-139">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-139">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d8-140">-VM</span><span class="sxs-lookup"><span data-stu-id="ad2d8-140">-VM</span></span>
<span data-ttu-id="ad2d8-141">Especifica uma máquina virtual local a ser criada.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-141">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="ad2d8-142">Para obter um objeto de máquina virtual, use o cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-142">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="ad2d8-143">Outros cmdlets podem ser usados para configurar a máquina virtual, como Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage e Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-143">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d8-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="ad2d8-144">-Zone</span></span>
<span data-ttu-id="ad2d8-145">Especifica a lista de zonas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-145">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2d8-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ad2d8-146">-Confirm</span></span>
<span data-ttu-id="ad2d8-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2d8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2d8-148">-WhatIf</span></span>
<span data-ttu-id="ad2d8-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-149">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ad2d8-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2d8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2d8-151">CommonParameters</span></span>
<span data-ttu-id="ad2d8-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad2d8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2d8-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2d8-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2d8-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad2d8-154">INPUTS</span></span>

## <span data-ttu-id="ad2d8-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad2d8-155">OUTPUTS</span></span>

## <span data-ttu-id="ad2d8-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad2d8-156">NOTES</span></span>

## <span data-ttu-id="ad2d8-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad2d8-157">RELATED LINKS</span></span>

[<span data-ttu-id="ad2d8-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad2d8-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ad2d8-159">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad2d8-159">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="ad2d8-160">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad2d8-160">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="ad2d8-161">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad2d8-161">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="ad2d8-162">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad2d8-162">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="ad2d8-163">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad2d8-163">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="ad2d8-164">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ad2d8-164">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="ad2d8-165">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ad2d8-165">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="ad2d8-166">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="ad2d8-166">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="ad2d8-167">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ad2d8-167">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="ad2d8-168">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="ad2d8-168">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="ad2d8-169">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="ad2d8-169">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


