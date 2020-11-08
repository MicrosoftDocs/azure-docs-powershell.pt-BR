---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115729"
---
# <span data-ttu-id="3a738-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3a738-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="3a738-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a738-102">SYNOPSIS</span></span>
<span data-ttu-id="3a738-103">Adiciona uma extensão ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="3a738-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="3a738-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a738-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a738-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a738-105">DESCRIPTION</span></span>
<span data-ttu-id="3a738-106">O cmdlet **Add-AzVmssExtension** adiciona uma extensão ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3a738-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="3a738-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a738-107">EXAMPLES</span></span>

### <span data-ttu-id="3a738-108">Exemplo 1: adicionar uma extensão ao VMSS</span><span class="sxs-lookup"><span data-stu-id="3a738-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="3a738-109">Esse comando adiciona uma extensão ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="3a738-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="3a738-110">Exemplo 2: adicionar uma extensão ao VMSS com configurações e configurações protegidas</span><span class="sxs-lookup"><span data-stu-id="3a738-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="3a738-111">Esse comando adiciona uma extensão ao VMSS com um exemplo de script de bash em um armazenamento de BLOB, especifica a URL do armazenamento de BLOB e o comando executável em configurações e acesso de segurança em Configurações protegidas.</span><span class="sxs-lookup"><span data-stu-id="3a738-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="3a738-112">OS</span><span class="sxs-lookup"><span data-stu-id="3a738-112">PARAMETERS</span></span>

### <span data-ttu-id="3a738-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3a738-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3a738-114">Indica se a versão de extensão deve ser atualizada automaticamente para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="3a738-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="3a738-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a738-115">-DefaultProfile</span></span>
<span data-ttu-id="3a738-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a738-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a738-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="3a738-117">-ForceUpdateTag</span></span>
<span data-ttu-id="3a738-118">Se um valor for fornecido e for diferente do valor anterior, o manipulador de extensão será forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="3a738-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="3a738-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a738-119">-Name</span></span>
<span data-ttu-id="3a738-120">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="3a738-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3a738-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="3a738-121">-ProtectedSetting</span></span>
<span data-ttu-id="3a738-122">Especifica a configuração particular para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3a738-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="3a738-123">Esse cmdlet criptografa a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="3a738-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="3a738-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="3a738-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="3a738-125">Coleção de nomes de extensão após o qual essa extensão precisa ser provisionada.</span><span class="sxs-lookup"><span data-stu-id="3a738-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a738-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3a738-126">-Publisher</span></span>
<span data-ttu-id="3a738-127">Especifica o nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="3a738-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="3a738-128">O fornecedor fornece um nome quando o Publicador registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="3a738-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="3a738-129">Isso pode usar o cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) para obter o editor.</span><span class="sxs-lookup"><span data-stu-id="3a738-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="3a738-130">-Configuração</span><span class="sxs-lookup"><span data-stu-id="3a738-130">-Setting</span></span>
<span data-ttu-id="3a738-131">Especifica a configuração pública, como uma cadeia de caracteres, para a extensão.</span><span class="sxs-lookup"><span data-stu-id="3a738-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="3a738-132">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="3a738-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="3a738-133">-Digite</span><span class="sxs-lookup"><span data-stu-id="3a738-133">-Type</span></span>
<span data-ttu-id="3a738-134">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="3a738-134">Specifies the extension type.</span></span>
<span data-ttu-id="3a738-135">Você pode usar o cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) para obter o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="3a738-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="3a738-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3a738-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="3a738-137">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a738-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="3a738-138">Você pode usar o cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) para obter a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="3a738-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="3a738-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3a738-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3a738-140">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="3a738-140">Specify the VMSS object.</span></span>
<span data-ttu-id="3a738-141">Você pode usar o [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="3a738-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="3a738-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a738-142">-Confirm</span></span>
<span data-ttu-id="3a738-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a738-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a738-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a738-144">-WhatIf</span></span>
<span data-ttu-id="3a738-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a738-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a738-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a738-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a738-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a738-147">CommonParameters</span></span>
<span data-ttu-id="3a738-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a738-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a738-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a738-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a738-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a738-150">INPUTS</span></span>

### <span data-ttu-id="3a738-151">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3a738-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3a738-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3a738-152">System.String</span></span>

### <span data-ttu-id="3a738-153">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3a738-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3a738-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="3a738-154">System.Object</span></span>

## <span data-ttu-id="3a738-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a738-155">OUTPUTS</span></span>

### <span data-ttu-id="3a738-156">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3a738-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3a738-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a738-157">NOTES</span></span>

## <span data-ttu-id="3a738-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a738-158">RELATED LINKS</span></span>

[<span data-ttu-id="3a738-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3a738-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="3a738-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3a738-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="3a738-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="3a738-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="3a738-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3a738-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="3a738-163">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3a738-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
