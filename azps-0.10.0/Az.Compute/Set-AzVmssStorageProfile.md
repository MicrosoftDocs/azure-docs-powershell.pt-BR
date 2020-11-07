---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: d19c039a5038c9327ea35a4f0b385e5472b748a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776808"
---
# <span data-ttu-id="73b7d-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="73b7d-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="73b7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="73b7d-103">Define as propriedades do perfil de armazenamento para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="73b7d-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="73b7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73b7d-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73b7d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="73b7d-106">O cmdlet **set-AzVmssStorageProfile** define as propriedades do perfil de armazenamento do conjunto de escala da máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="73b7d-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="73b7d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73b7d-107">EXAMPLES</span></span>

### <span data-ttu-id="73b7d-108">Exemplo 1: definir as propriedades do perfil de armazenamento do VMSS</span><span class="sxs-lookup"><span data-stu-id="73b7d-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="73b7d-109">Esse comando define as propriedades do perfil de armazenamento para o VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="73b7d-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="73b7d-110">OS</span><span class="sxs-lookup"><span data-stu-id="73b7d-110">PARAMETERS</span></span>

### <span data-ttu-id="73b7d-111">-Datadisk</span><span class="sxs-lookup"><span data-stu-id="73b7d-111">-DataDisk</span></span>
<span data-ttu-id="73b7d-112">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="73b7d-112">Specifies the data disk object.</span></span>

```yaml
Type: VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73b7d-113">-DefaultProfile</span></span>
<span data-ttu-id="73b7d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73b7d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73b7d-115">-Imagem</span><span class="sxs-lookup"><span data-stu-id="73b7d-115">-Image</span></span>
<span data-ttu-id="73b7d-116">Especifica o URI do blob para a imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="73b7d-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="73b7d-117">O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="73b7d-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="73b7d-118">-ImageReferenceId</span></span>
<span data-ttu-id="73b7d-119">Especifica a ID de referência da imagem.</span><span class="sxs-lookup"><span data-stu-id="73b7d-119">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="73b7d-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="73b7d-121">Especifica o tipo de oferta da máquina virtual da máquina (VMImage).</span><span class="sxs-lookup"><span data-stu-id="73b7d-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="73b7d-122">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="73b7d-122">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="73b7d-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="73b7d-124">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="73b7d-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="73b7d-125">Para obter um fornecedor, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="73b7d-125">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="73b7d-126">-ImageReferenceSku</span></span>
<span data-ttu-id="73b7d-127">Especifica o SKU da VMImage.</span><span class="sxs-lookup"><span data-stu-id="73b7d-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="73b7d-128">Para obter os SKUs, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="73b7d-128">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="73b7d-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="73b7d-130">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="73b7d-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="73b7d-131">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="73b7d-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="73b7d-132">-ManagedDisk</span></span>
<span data-ttu-id="73b7d-133">Especifica o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="73b7d-133">Specifies the managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="73b7d-134">-OsDiskCaching</span></span>
<span data-ttu-id="73b7d-135">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="73b7d-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="73b7d-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="73b7d-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73b7d-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="73b7d-137">ReadOnly</span></span>
- <span data-ttu-id="73b7d-138">Leitura</span><span class="sxs-lookup"><span data-stu-id="73b7d-138">ReadWrite</span></span>

<span data-ttu-id="73b7d-139">O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="73b7d-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="73b7d-140">Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="73b7d-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="73b7d-141">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="73b7d-141">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="73b7d-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="73b7d-143">Especifica como esse cmdlet cria as máquinas virtuais VMSS.</span><span class="sxs-lookup"><span data-stu-id="73b7d-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="73b7d-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="73b7d-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73b7d-145">Anexar: esse valor é usado quando você está usando um disco especializado para criar a máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="73b7d-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="73b7d-146">FromImage: esse valor é usado quando você está usando uma imagem para criar a máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="73b7d-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="73b7d-147">Se você estiver usando uma imagem de plataforma, também poderá usar o parâmetro *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="73b7d-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="73b7d-148">-OsDiskName</span></span>
<span data-ttu-id="73b7d-149">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="73b7d-149">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="73b7d-150">-OsDiskOsType</span></span>
<span data-ttu-id="73b7d-151">Especifica o tipo de sistema operacional no disco.</span><span class="sxs-lookup"><span data-stu-id="73b7d-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="73b7d-152">Isso só é necessário para cenários de imagem de usuário e não para uma imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="73b7d-152">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="73b7d-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="73b7d-154">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="73b7d-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="73b7d-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="73b7d-155">-VhdContainer</span></span>
<span data-ttu-id="73b7d-156">Especifica as URLs de contêiner usadas para armazenar discos do sistema operacional para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="73b7d-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73b7d-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="73b7d-158">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="73b7d-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="73b7d-159">Para obter o objeto, use o objeto New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="73b7d-159">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73b7d-160">-Confirm</span></span>
<span data-ttu-id="73b7d-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73b7d-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73b7d-162">-WhatIf</span></span>
<span data-ttu-id="73b7d-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73b7d-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73b7d-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73b7d-164">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73b7d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73b7d-165">CommonParameters</span></span>
<span data-ttu-id="73b7d-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73b7d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73b7d-167">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73b7d-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73b7d-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73b7d-168">INPUTS</span></span>

###  
<span data-ttu-id="73b7d-169">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="73b7d-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="73b7d-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73b7d-170">OUTPUTS</span></span>

### <span data-ttu-id="73b7d-171">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73b7d-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="73b7d-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73b7d-172">NOTES</span></span>

## <span data-ttu-id="73b7d-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73b7d-173">RELATED LINKS</span></span>

[<span data-ttu-id="73b7d-174">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="73b7d-174">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="73b7d-175">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="73b7d-175">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="73b7d-176">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="73b7d-176">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="73b7d-177">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="73b7d-177">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


