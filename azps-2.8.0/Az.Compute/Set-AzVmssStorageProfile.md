---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 883c976df7223a03421550f2a27c2baf51be4dcb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597187"
---
# <span data-ttu-id="08bdf-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="08bdf-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="08bdf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="08bdf-103">Define as propriedades do perfil de armazenamento para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="08bdf-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="08bdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08bdf-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08bdf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="08bdf-106">O cmdlet **set-AzVmssStorageProfile** define as propriedades do perfil de armazenamento do conjunto de escala da máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="08bdf-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="08bdf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08bdf-107">EXAMPLES</span></span>

### <span data-ttu-id="08bdf-108">Exemplo 1: definir as propriedades do perfil de armazenamento do VMSS</span><span class="sxs-lookup"><span data-stu-id="08bdf-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="08bdf-109">Esse comando define as propriedades do perfil de armazenamento para o VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="08bdf-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="08bdf-110">OS</span><span class="sxs-lookup"><span data-stu-id="08bdf-110">PARAMETERS</span></span>

### <span data-ttu-id="08bdf-111">-Datadisk</span><span class="sxs-lookup"><span data-stu-id="08bdf-111">-DataDisk</span></span>
<span data-ttu-id="08bdf-112">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="08bdf-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bdf-113">-DefaultProfile</span></span>
<span data-ttu-id="08bdf-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08bdf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08bdf-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="08bdf-115">-DiffDiskSetting</span></span>
<span data-ttu-id="08bdf-116">Especifica as configurações de disco diferencial para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08bdf-116">Specifies the differencing disk settings for operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-117">-Imagem</span><span class="sxs-lookup"><span data-stu-id="08bdf-117">-Image</span></span>
<span data-ttu-id="08bdf-118">Especifica o URI do blob para a imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="08bdf-118">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="08bdf-119">O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="08bdf-119">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-120">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="08bdf-120">-ImageReferenceId</span></span>
<span data-ttu-id="08bdf-121">Especifica a ID de referência da imagem.</span><span class="sxs-lookup"><span data-stu-id="08bdf-121">Specifies the image reference ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-122">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="08bdf-122">-ImageReferenceOffer</span></span>
<span data-ttu-id="08bdf-123">Especifica o tipo de oferta da máquina virtual da máquina (VMImage).</span><span class="sxs-lookup"><span data-stu-id="08bdf-123">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="08bdf-124">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="08bdf-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-125">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="08bdf-125">-ImageReferencePublisher</span></span>
<span data-ttu-id="08bdf-126">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="08bdf-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="08bdf-127">Para obter um fornecedor, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="08bdf-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-128">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="08bdf-128">-ImageReferenceSku</span></span>
<span data-ttu-id="08bdf-129">Especifica o SKU da VMImage.</span><span class="sxs-lookup"><span data-stu-id="08bdf-129">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="08bdf-130">Para obter os SKUs, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="08bdf-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-131">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="08bdf-131">-ImageReferenceVersion</span></span>
<span data-ttu-id="08bdf-132">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="08bdf-132">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="08bdf-133">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="08bdf-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-134">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="08bdf-134">-ManagedDisk</span></span>
<span data-ttu-id="08bdf-135">Especifica o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="08bdf-135">Specifies the managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-136">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="08bdf-136">-OsDiskCaching</span></span>
<span data-ttu-id="08bdf-137">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08bdf-137">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="08bdf-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08bdf-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08bdf-139">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="08bdf-139">ReadOnly</span></span>
- <span data-ttu-id="08bdf-140">ReadWrite o valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="08bdf-140">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="08bdf-141">Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08bdf-141">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="08bdf-142">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="08bdf-142">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-143">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="08bdf-143">-OsDiskCreateOption</span></span>
<span data-ttu-id="08bdf-144">Especifica como esse cmdlet cria as máquinas virtuais VMSS.</span><span class="sxs-lookup"><span data-stu-id="08bdf-144">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="08bdf-145">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08bdf-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08bdf-146">Anexar: esse valor é usado quando você está usando um disco especializado para criar a máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="08bdf-146">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="08bdf-147">FromImage: esse valor é usado quando você está usando uma imagem para criar a máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="08bdf-147">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="08bdf-148">Se você estiver usando uma imagem de plataforma, também poderá usar o parâmetro *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="08bdf-148">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-149">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="08bdf-149">-OsDiskName</span></span>
<span data-ttu-id="08bdf-150">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08bdf-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-151">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="08bdf-151">-OsDiskOsType</span></span>
<span data-ttu-id="08bdf-152">Especifica o tipo de sistema operacional no disco.</span><span class="sxs-lookup"><span data-stu-id="08bdf-152">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="08bdf-153">Isso só é necessário para cenários de imagem de usuário e não para uma imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="08bdf-153">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-154">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="08bdf-154">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="08bdf-155">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08bdf-155">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="08bdf-156">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="08bdf-156">-VhdContainer</span></span>
<span data-ttu-id="08bdf-157">Especifica as URLs de contêiner usadas para armazenar discos do sistema operacional para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="08bdf-157">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-158">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="08bdf-158">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="08bdf-159">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="08bdf-159">Specifies the VMSS object.</span></span>
<span data-ttu-id="08bdf-160">Para obter o objeto, use o objeto New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="08bdf-160">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="08bdf-161">-Confirm</span></span>
<span data-ttu-id="08bdf-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08bdf-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08bdf-163">-WhatIf</span></span>
<span data-ttu-id="08bdf-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08bdf-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08bdf-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08bdf-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08bdf-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bdf-166">CommonParameters</span></span>
<span data-ttu-id="08bdf-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bdf-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bdf-168">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08bdf-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bdf-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08bdf-169">INPUTS</span></span>

### <span data-ttu-id="08bdf-170">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="08bdf-170">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="08bdf-171">System. String</span><span class="sxs-lookup"><span data-stu-id="08bdf-171">System.String</span></span>

### <span data-ttu-id="08bdf-172">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="08bdf-172">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="08bdf-173">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="08bdf-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="08bdf-174">System. String []</span><span class="sxs-lookup"><span data-stu-id="08bdf-174">System.String[]</span></span>

### <span data-ttu-id="08bdf-175">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="08bdf-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="08bdf-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08bdf-176">OUTPUTS</span></span>

### <span data-ttu-id="08bdf-177">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="08bdf-177">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="08bdf-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08bdf-178">NOTES</span></span>

## <span data-ttu-id="08bdf-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08bdf-179">RELATED LINKS</span></span>

[<span data-ttu-id="08bdf-180">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="08bdf-180">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="08bdf-181">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="08bdf-181">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="08bdf-182">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="08bdf-182">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="08bdf-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="08bdf-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


