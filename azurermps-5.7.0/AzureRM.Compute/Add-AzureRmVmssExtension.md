---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426814"
---
# <span data-ttu-id="7465d-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7465d-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="7465d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7465d-102">SYNOPSIS</span></span>
<span data-ttu-id="7465d-103">Adiciona uma extensão ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="7465d-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7465d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7465d-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7465d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7465d-105">DESCRIPTION</span></span>
<span data-ttu-id="7465d-106">O cmdlet **Add-AzureRmVmssExtension** adiciona uma extensão ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="7465d-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="7465d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7465d-107">EXAMPLES</span></span>

### <span data-ttu-id="7465d-108">Exemplo 1: adicionar uma extensão ao VMSS</span><span class="sxs-lookup"><span data-stu-id="7465d-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="7465d-109">Esse comando adiciona uma extensão ao VMMS.</span><span class="sxs-lookup"><span data-stu-id="7465d-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="7465d-110">OS</span><span class="sxs-lookup"><span data-stu-id="7465d-110">PARAMETERS</span></span>

### <span data-ttu-id="7465d-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7465d-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7465d-112">Indica se a versão de extensão deve ser atualizada automaticamente para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="7465d-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7465d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7465d-113">-Name</span></span>
<span data-ttu-id="7465d-114">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="7465d-114">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="7465d-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="7465d-115">-ProtectedSetting</span></span>
<span data-ttu-id="7465d-116">Especifica a configuração particular para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7465d-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="7465d-117">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="7465d-117">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7465d-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7465d-118">-Publisher</span></span>
<span data-ttu-id="7465d-119">Especifica o nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="7465d-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="7465d-120">O fornecedor fornece um nome quando o Publicador registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="7465d-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="7465d-121">Isso pode usar o cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) para obter o editor.</span><span class="sxs-lookup"><span data-stu-id="7465d-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="7465d-122">-Configuração</span><span class="sxs-lookup"><span data-stu-id="7465d-122">-Setting</span></span>
<span data-ttu-id="7465d-123">Especifica a configuração pública, como uma cadeia de caracteres, para a extensão.</span><span class="sxs-lookup"><span data-stu-id="7465d-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="7465d-124">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="7465d-124">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7465d-125">-Digite</span><span class="sxs-lookup"><span data-stu-id="7465d-125">-Type</span></span>
<span data-ttu-id="7465d-126">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="7465d-126">Specifies the extension type.</span></span>
<span data-ttu-id="7465d-127">Você pode usar o cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) para obter o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="7465d-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="7465d-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7465d-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="7465d-129">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7465d-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="7465d-130">Você pode usar o cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) para obter a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="7465d-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="7465d-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7465d-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7465d-132">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="7465d-132">Specify the VMSS object.</span></span>
<span data-ttu-id="7465d-133">Você pode usar o [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="7465d-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7465d-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7465d-134">-Confirm</span></span>
<span data-ttu-id="7465d-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7465d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7465d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7465d-136">-WhatIf</span></span>
<span data-ttu-id="7465d-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7465d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7465d-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7465d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7465d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7465d-139">CommonParameters</span></span>
<span data-ttu-id="7465d-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7465d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7465d-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7465d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7465d-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7465d-142">INPUTS</span></span>

### <span data-ttu-id="7465d-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7465d-143">None</span></span>
<span data-ttu-id="7465d-144">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7465d-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7465d-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7465d-145">OUTPUTS</span></span>

###  
<span data-ttu-id="7465d-146">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7465d-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7465d-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7465d-147">NOTES</span></span>

## <span data-ttu-id="7465d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7465d-148">RELATED LINKS</span></span>

[<span data-ttu-id="7465d-149">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7465d-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="7465d-150">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7465d-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="7465d-151">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="7465d-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="7465d-152">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="7465d-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="7465d-153">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7465d-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
