---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 60d525cc50b62350853755ae46698cbecb358654
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426915"
---
# <span data-ttu-id="336e5-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="336e5-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="336e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="336e5-102">SYNOPSIS</span></span>
<span data-ttu-id="336e5-103">Define as propriedades do perfil de armazenamento para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="336e5-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="336e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="336e5-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="336e5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="336e5-105">DESCRIPTION</span></span>
<span data-ttu-id="336e5-106">O cmdlet **set-AzureRmVmssStorageProfile** define as propriedades do perfil de armazenamento do conjunto de escala da máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="336e5-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="336e5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="336e5-107">EXAMPLES</span></span>

### <span data-ttu-id="336e5-108">Exemplo 1: definir as propriedades do perfil de armazenamento do VMSS</span><span class="sxs-lookup"><span data-stu-id="336e5-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="336e5-109">Esse comando define as propriedades do perfil de armazenamento para o VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="336e5-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="336e5-110">OS</span><span class="sxs-lookup"><span data-stu-id="336e5-110">PARAMETERS</span></span>

### <span data-ttu-id="336e5-111">-Datadisk</span><span class="sxs-lookup"><span data-stu-id="336e5-111">-DataDisk</span></span>
<span data-ttu-id="336e5-112">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="336e5-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="336e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336e5-113">-DefaultProfile</span></span>
<span data-ttu-id="336e5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="336e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="336e5-115">-Imagem</span><span class="sxs-lookup"><span data-stu-id="336e5-115">-Image</span></span>
<span data-ttu-id="336e5-116">Especifica o URI do blob para a imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="336e5-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="336e5-117">O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="336e5-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="336e5-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="336e5-118">-ImageReferenceId</span></span>
<span data-ttu-id="336e5-119">Especifica a ID de referência da imagem.</span><span class="sxs-lookup"><span data-stu-id="336e5-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="336e5-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="336e5-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="336e5-121">Especifica o tipo de oferta da máquina virtual da máquina (VMImage).</span><span class="sxs-lookup"><span data-stu-id="336e5-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="336e5-122">Para obter uma oferta de imagem, use o cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="336e5-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="336e5-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="336e5-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="336e5-124">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="336e5-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="336e5-125">Para obter um fornecedor, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="336e5-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="336e5-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="336e5-126">-ImageReferenceSku</span></span>
<span data-ttu-id="336e5-127">Especifica o SKU da VMImage.</span><span class="sxs-lookup"><span data-stu-id="336e5-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="336e5-128">Para obter os SKUs, use o cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="336e5-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="336e5-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="336e5-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="336e5-130">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="336e5-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="336e5-131">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="336e5-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="336e5-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="336e5-132">-ManagedDisk</span></span>
<span data-ttu-id="336e5-133">Especifica o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="336e5-133">Specifies the managed disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336e5-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="336e5-134">-OsDiskCaching</span></span>
<span data-ttu-id="336e5-135">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="336e5-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="336e5-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="336e5-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="336e5-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="336e5-137">ReadOnly</span></span>
- <span data-ttu-id="336e5-138">Leitura</span><span class="sxs-lookup"><span data-stu-id="336e5-138">ReadWrite</span></span>

<span data-ttu-id="336e5-139">O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="336e5-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="336e5-140">Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="336e5-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="336e5-141">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="336e5-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="336e5-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="336e5-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="336e5-143">Especifica como esse cmdlet cria as máquinas virtuais VMSS.</span><span class="sxs-lookup"><span data-stu-id="336e5-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="336e5-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="336e5-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="336e5-145">Anexar: esse valor é usado quando você está usando um disco especializado para criar a máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="336e5-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="336e5-146">FromImage: esse valor é usado quando você está usando uma imagem para criar a máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="336e5-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="336e5-147">Se você estiver usando uma imagem de plataforma, também poderá usar o parâmetro *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="336e5-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336e5-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="336e5-148">-OsDiskName</span></span>
<span data-ttu-id="336e5-149">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="336e5-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="336e5-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="336e5-150">-OsDiskOsType</span></span>
<span data-ttu-id="336e5-151">Especifica o tipo de sistema operacional no disco.</span><span class="sxs-lookup"><span data-stu-id="336e5-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="336e5-152">Isso só é necessário para cenários de imagem de usuário e não para uma imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="336e5-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="336e5-153">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="336e5-153">-VhdContainer</span></span>
<span data-ttu-id="336e5-154">Especifica as URLs de contêiner usadas para armazenar discos do sistema operacional para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="336e5-154">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="336e5-155">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="336e5-155">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="336e5-156">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="336e5-156">Specifies the VMSS object.</span></span>
<span data-ttu-id="336e5-157">Para obter o objeto, use o objeto New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="336e5-157">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

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

### <span data-ttu-id="336e5-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="336e5-158">-Confirm</span></span>
<span data-ttu-id="336e5-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="336e5-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="336e5-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="336e5-160">-WhatIf</span></span>
<span data-ttu-id="336e5-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="336e5-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="336e5-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="336e5-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="336e5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336e5-163">CommonParameters</span></span>
<span data-ttu-id="336e5-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="336e5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336e5-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="336e5-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336e5-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="336e5-166">INPUTS</span></span>

###  
<span data-ttu-id="336e5-167">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="336e5-167">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="336e5-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="336e5-168">OUTPUTS</span></span>

## <span data-ttu-id="336e5-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="336e5-169">NOTES</span></span>

## <span data-ttu-id="336e5-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="336e5-170">RELATED LINKS</span></span>

[<span data-ttu-id="336e5-171">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="336e5-171">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="336e5-172">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="336e5-172">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="336e5-173">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="336e5-173">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="336e5-174">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="336e5-174">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


