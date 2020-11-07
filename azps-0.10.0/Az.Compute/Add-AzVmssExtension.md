---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777078"
---
# <span data-ttu-id="9a6d6-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9a6d6-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="9a6d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a6d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6d6-103">Adiciona uma extensão ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="9a6d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a6d6-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a6d6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a6d6-105">DESCRIPTION</span></span>
<span data-ttu-id="9a6d6-106">O cmdlet **Add-AzVmssExtension** adiciona uma extensão ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9a6d6-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="9a6d6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a6d6-107">EXAMPLES</span></span>

### <span data-ttu-id="9a6d6-108">Exemplo 1: adicionar uma extensão ao VMSS</span><span class="sxs-lookup"><span data-stu-id="9a6d6-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="9a6d6-109">Esse comando adiciona uma extensão ao VMMS.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="9a6d6-110">OS</span><span class="sxs-lookup"><span data-stu-id="9a6d6-110">PARAMETERS</span></span>

### <span data-ttu-id="9a6d6-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9a6d6-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9a6d6-112">Indica se a versão de extensão deve ser atualizada automaticamente para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="9a6d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6d6-113">-DefaultProfile</span></span>
<span data-ttu-id="9a6d6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a6d6-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="9a6d6-115">-ForceUpdateTag</span></span>
<span data-ttu-id="9a6d6-116">Se um valor for fornecido e for diferente do valor anterior, o manipulador de extensão será forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="9a6d6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a6d6-117">-Name</span></span>
<span data-ttu-id="9a6d6-118">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9a6d6-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="9a6d6-119">-ProtectedSetting</span></span>
<span data-ttu-id="9a6d6-120">Especifica a configuração particular para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="9a6d6-121">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="9a6d6-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9a6d6-122">-Publisher</span></span>
<span data-ttu-id="9a6d6-123">Especifica o nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="9a6d6-124">O fornecedor fornece um nome quando o Publicador registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="9a6d6-125">Isso pode usar o cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) para obter o editor.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-125">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="9a6d6-126">-Configuração</span><span class="sxs-lookup"><span data-stu-id="9a6d6-126">-Setting</span></span>
<span data-ttu-id="9a6d6-127">Especifica a configuração pública, como uma cadeia de caracteres, para a extensão.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="9a6d6-128">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="9a6d6-129">-Digite</span><span class="sxs-lookup"><span data-stu-id="9a6d6-129">-Type</span></span>
<span data-ttu-id="9a6d6-130">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-130">Specifies the extension type.</span></span>
<span data-ttu-id="9a6d6-131">Você pode usar o cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) para obter o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-131">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="9a6d6-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9a6d6-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="9a6d6-133">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="9a6d6-134">Você pode usar o cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) para obter a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-134">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="9a6d6-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a6d6-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9a6d6-136">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-136">Specify the VMSS object.</span></span>
<span data-ttu-id="9a6d6-137">Você pode usar o [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-137">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="9a6d6-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9a6d6-138">-Confirm</span></span>
<span data-ttu-id="9a6d6-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a6d6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a6d6-140">-WhatIf</span></span>
<span data-ttu-id="9a6d6-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a6d6-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a6d6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6d6-143">CommonParameters</span></span>
<span data-ttu-id="9a6d6-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6d6-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a6d6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6d6-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a6d6-146">INPUTS</span></span>

### <span data-ttu-id="9a6d6-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a6d6-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="9a6d6-148">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="9a6d6-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="9a6d6-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a6d6-149">OUTPUTS</span></span>

###  
<span data-ttu-id="9a6d6-150">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9a6d6-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9a6d6-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a6d6-151">NOTES</span></span>

## <span data-ttu-id="9a6d6-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a6d6-152">RELATED LINKS</span></span>

[<span data-ttu-id="9a6d6-153">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9a6d6-153">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="9a6d6-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9a6d6-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9a6d6-155">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="9a6d6-155">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="9a6d6-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9a6d6-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="9a6d6-157">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9a6d6-157">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
