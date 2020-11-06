---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: ad87e4e556263889de23640abad391ee28d7b397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432320"
---
# <span data-ttu-id="cf282-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cf282-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="cf282-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf282-102">SYNOPSIS</span></span>
<span data-ttu-id="cf282-103">Adiciona uma extensão ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf282-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf282-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf282-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf282-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf282-105">DESCRIPTION</span></span>
<span data-ttu-id="cf282-106">O cmdlet **Add-AzureRmVmssExtension** adiciona uma extensão ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cf282-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="cf282-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf282-107">EXAMPLES</span></span>

### <span data-ttu-id="cf282-108">Exemplo 1: adicionar uma extensão ao VMSS</span><span class="sxs-lookup"><span data-stu-id="cf282-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="cf282-109">Esse comando adiciona uma extensão ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf282-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="cf282-110">Exemplo 2: adicionar uma extensão ao VMSS com configurações e configurações protegidas</span><span class="sxs-lookup"><span data-stu-id="cf282-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="cf282-111">Esse comando adiciona uma extensão ao VMSS com um exemplo de script de bash em um armazenamento de BLOB, especifica a URL do armazenamento de BLOB e o comando executável em configurações e acesso de segurança em Configurações protegidas.</span><span class="sxs-lookup"><span data-stu-id="cf282-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="cf282-112">OS</span><span class="sxs-lookup"><span data-stu-id="cf282-112">PARAMETERS</span></span>

### <span data-ttu-id="cf282-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cf282-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="cf282-114">Indica se a versão de extensão deve ser atualizada automaticamente para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="cf282-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf282-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf282-115">-DefaultProfile</span></span>
<span data-ttu-id="cf282-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf282-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf282-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="cf282-117">-ForceUpdateTag</span></span>
<span data-ttu-id="cf282-118">Se um valor for fornecido e for diferente do valor anterior, o manipulador de extensão será forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="cf282-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="cf282-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf282-119">-Name</span></span>
<span data-ttu-id="cf282-120">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="cf282-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cf282-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="cf282-121">-ProtectedSetting</span></span>
<span data-ttu-id="cf282-122">Especifica a configuração particular para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf282-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="cf282-123">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="cf282-123">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf282-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="cf282-124">-Publisher</span></span>
<span data-ttu-id="cf282-125">Especifica o nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="cf282-125">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="cf282-126">O fornecedor fornece um nome quando o Publicador registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="cf282-126">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="cf282-127">Isso pode usar o cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) para obter o editor.</span><span class="sxs-lookup"><span data-stu-id="cf282-127">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="cf282-128">-Configuração</span><span class="sxs-lookup"><span data-stu-id="cf282-128">-Setting</span></span>
<span data-ttu-id="cf282-129">Especifica a configuração pública, como uma cadeia de caracteres, para a extensão.</span><span class="sxs-lookup"><span data-stu-id="cf282-129">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="cf282-130">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="cf282-130">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf282-131">-Digite</span><span class="sxs-lookup"><span data-stu-id="cf282-131">-Type</span></span>
<span data-ttu-id="cf282-132">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="cf282-132">Specifies the extension type.</span></span>
<span data-ttu-id="cf282-133">Você pode usar o cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) para obter o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="cf282-133">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="cf282-134">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cf282-134">-TypeHandlerVersion</span></span>
<span data-ttu-id="cf282-135">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cf282-135">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="cf282-136">Você pode usar o cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) para obter a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="cf282-136">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="cf282-137">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf282-137">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cf282-138">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf282-138">Specify the VMSS object.</span></span>
<span data-ttu-id="cf282-139">Você pode usar o [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="cf282-139">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="cf282-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf282-140">-Confirm</span></span>
<span data-ttu-id="cf282-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf282-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf282-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf282-142">-WhatIf</span></span>
<span data-ttu-id="cf282-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf282-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf282-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf282-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf282-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf282-145">CommonParameters</span></span>
<span data-ttu-id="cf282-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf282-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf282-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf282-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf282-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf282-148">INPUTS</span></span>

### <span data-ttu-id="cf282-149">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf282-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="cf282-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cf282-150">System.String</span></span>

### <span data-ttu-id="cf282-151">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cf282-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="cf282-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="cf282-152">System.Object</span></span>

## <span data-ttu-id="cf282-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf282-153">OUTPUTS</span></span>

### <span data-ttu-id="cf282-154">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf282-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cf282-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf282-155">NOTES</span></span>

## <span data-ttu-id="cf282-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf282-156">RELATED LINKS</span></span>

[<span data-ttu-id="cf282-157">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cf282-157">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="cf282-158">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="cf282-158">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="cf282-159">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="cf282-159">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="cf282-160">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="cf282-160">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="cf282-161">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cf282-161">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
