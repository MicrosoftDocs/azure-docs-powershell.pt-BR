---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: ec233765f401348895275291ddad0571d1ddfc85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888571"
---
# <span data-ttu-id="cf284-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="cf284-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="cf284-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf284-102">SYNOPSIS</span></span>
<span data-ttu-id="cf284-103">Define as propriedades de perfil de armazenamento do VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf284-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="cf284-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cf284-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf284-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cf284-105">DESCRIPTION</span></span>
<span data-ttu-id="cf284-106">O cmdlet **Set-AzVmssStorageProfile** define as propriedades de perfil de armazenamento do Conjunto de Escala de Máquina Virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cf284-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="cf284-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf284-107">EXAMPLES</span></span>

### <span data-ttu-id="cf284-108">Exemplo 1: definir as propriedades de perfil de armazenamento para o VMSS</span><span class="sxs-lookup"><span data-stu-id="cf284-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="cf284-109">Este comando define as propriedades de perfil de armazenamento para o VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="cf284-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="cf284-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cf284-110">PARAMETERS</span></span>

### <span data-ttu-id="cf284-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="cf284-111">-DataDisk</span></span>
<span data-ttu-id="cf284-112">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="cf284-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="cf284-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf284-113">-DefaultProfile</span></span>
<span data-ttu-id="cf284-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cf284-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf284-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="cf284-115">-DiffDiskSetting</span></span>
<span data-ttu-id="cf284-116">Especifica as configurações de disco de diferenciação para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cf284-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="cf284-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="cf284-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="cf284-118">Especifica a ID de recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="cf284-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="cf284-119">Isso só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cf284-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="cf284-120">-Image</span><span class="sxs-lookup"><span data-stu-id="cf284-120">-Image</span></span>
<span data-ttu-id="cf284-121">Especifica o URI blob para a imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="cf284-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="cf284-122">O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="cf284-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="cf284-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="cf284-123">-ImageReferenceId</span></span>
<span data-ttu-id="cf284-124">Especifica a ID de referência da imagem.</span><span class="sxs-lookup"><span data-stu-id="cf284-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="cf284-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="cf284-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="cf284-126">Especifica o tipo de oferta de imagem de máquina virtual (VMImage).</span><span class="sxs-lookup"><span data-stu-id="cf284-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="cf284-127">Para obter uma oferta de imagem, use Get-AzVMImageOffer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf284-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="cf284-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="cf284-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="cf284-129">Especifica o nome de um editor de um VMImage.</span><span class="sxs-lookup"><span data-stu-id="cf284-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="cf284-130">Para obter um editor, use o Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf284-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="cf284-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="cf284-131">-ImageReferenceSku</span></span>
<span data-ttu-id="cf284-132">Especifica o SKU do VMImage.</span><span class="sxs-lookup"><span data-stu-id="cf284-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="cf284-133">Para obter SKUs, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="cf284-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="cf284-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="cf284-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="cf284-135">Especifica a versão do VMImage.</span><span class="sxs-lookup"><span data-stu-id="cf284-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="cf284-136">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="cf284-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="cf284-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="cf284-137">-ManagedDisk</span></span>
<span data-ttu-id="cf284-138">Especifica o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cf284-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="cf284-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="cf284-139">-OsDiskCaching</span></span>
<span data-ttu-id="cf284-140">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cf284-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="cf284-141">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cf284-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf284-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="cf284-142">ReadOnly</span></span>
- <span data-ttu-id="cf284-143">ReadWrite O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="cf284-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="cf284-144">Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cf284-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="cf284-145">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="cf284-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="cf284-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="cf284-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="cf284-147">Especifica como esse cmdlet cria as máquinas virtuais VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf284-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="cf284-148">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cf284-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf284-149">Anexar : esse valor é usado quando você está usando um disco especializado para criar a máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf284-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="cf284-150">FromImage : esse valor é usado quando você está usando uma imagem para criar a máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf284-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="cf284-151">Se você estiver usando uma imagem de plataforma, também usará o *parâmetro imageReference.*</span><span class="sxs-lookup"><span data-stu-id="cf284-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="cf284-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="cf284-152">-OsDiskName</span></span>
<span data-ttu-id="cf284-153">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cf284-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="cf284-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="cf284-154">-OsDiskOsType</span></span>
<span data-ttu-id="cf284-155">Especifica o tipo de sistema operacional no disco.</span><span class="sxs-lookup"><span data-stu-id="cf284-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="cf284-156">Isso só é necessário para cenários de imagem do usuário e não para uma imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="cf284-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="cf284-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="cf284-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="cf284-158">Especifica se WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cf284-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="cf284-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="cf284-159">-VhdContainer</span></span>
<span data-ttu-id="cf284-160">Especifica as URLs de contêiner que são usadas para armazenar discos do sistema operacional para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf284-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="cf284-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf284-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cf284-162">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf284-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="cf284-163">Para obter o objeto, use o objeto New-AzVmssConfig objeto.</span><span class="sxs-lookup"><span data-stu-id="cf284-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="cf284-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf284-164">-Confirm</span></span>
<span data-ttu-id="cf284-165">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf284-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf284-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf284-166">-WhatIf</span></span>
<span data-ttu-id="cf284-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf284-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf284-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf284-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf284-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf284-169">CommonParameters</span></span>
<span data-ttu-id="cf284-170">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf284-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf284-171">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf284-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf284-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf284-172">INPUTS</span></span>

### <span data-ttu-id="cf284-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf284-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="cf284-174">System.String</span><span class="sxs-lookup"><span data-stu-id="cf284-174">System.String</span></span>

### <span data-ttu-id="cf284-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cf284-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cf284-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cf284-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cf284-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cf284-177">System.String[]</span></span>

### <span data-ttu-id="cf284-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="cf284-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="cf284-179">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cf284-179">OUTPUTS</span></span>

### <span data-ttu-id="cf284-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf284-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cf284-181">NOTES</span><span class="sxs-lookup"><span data-stu-id="cf284-181">NOTES</span></span>

## <span data-ttu-id="cf284-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf284-182">RELATED LINKS</span></span>

[<span data-ttu-id="cf284-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="cf284-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="cf284-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="cf284-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="cf284-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="cf284-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="cf284-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cf284-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


