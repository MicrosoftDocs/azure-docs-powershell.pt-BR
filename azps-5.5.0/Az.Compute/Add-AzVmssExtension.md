---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 152d6e861d7622e262279c1f665565347e0ab2cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117878"
---
# <span data-ttu-id="02014-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="02014-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="02014-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02014-102">SYNOPSIS</span></span>
<span data-ttu-id="02014-103">Adiciona uma extensão ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="02014-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="02014-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02014-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02014-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="02014-105">DESCRIPTION</span></span>
<span data-ttu-id="02014-106">O **cmdlet Add-AzVmssExtension** adiciona uma extensão ao VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="02014-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="02014-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="02014-107">EXAMPLES</span></span>

### <span data-ttu-id="02014-108">Exemplo 1: Adicionar uma extensão ao VMSS</span><span class="sxs-lookup"><span data-stu-id="02014-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="02014-109">Esse comando adiciona uma extensão ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="02014-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="02014-110">Exemplo 2: Adicionar uma extensão ao VMSS com configurações e configurações protegidas</span><span class="sxs-lookup"><span data-stu-id="02014-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="02014-111">Este comando adiciona uma extensão ao VMSS com um script bash de exemplo em um armazenamento de blob, especifique a url de armazenamento de blob e comando executável em configurações e acesso de segurança em configurações protegidas.</span><span class="sxs-lookup"><span data-stu-id="02014-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="02014-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02014-112">PARAMETERS</span></span>

### <span data-ttu-id="02014-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="02014-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="02014-114">Indica se a versão de extensão deve ser atualizada automaticamente para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="02014-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="02014-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02014-115">-DefaultProfile</span></span>
<span data-ttu-id="02014-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="02014-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02014-117">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="02014-117">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="02014-118">Indica se a extensão deve ser atualizada automaticamente pela plataforma se houver uma versão mais recente da extensão disponível.</span><span class="sxs-lookup"><span data-stu-id="02014-118">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02014-119">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="02014-119">-ForceUpdateTag</span></span>
<span data-ttu-id="02014-120">Se um valor for fornecido e for diferente do valor anterior, o manipulador de extensão será obrigado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="02014-120">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="02014-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="02014-121">-Name</span></span>
<span data-ttu-id="02014-122">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="02014-122">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="02014-123">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="02014-123">-ProtectedSetting</span></span>
<span data-ttu-id="02014-124">Especifica a configuração privada para a extensão, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="02014-124">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="02014-125">Este cmdlet criptografa a configuração privada.</span><span class="sxs-lookup"><span data-stu-id="02014-125">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="02014-126">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="02014-126">-ProvisionAfterExtension</span></span>
<span data-ttu-id="02014-127">Conjunto de nomes de extensão após os quais essa extensão precisa ser provisionada.</span><span class="sxs-lookup"><span data-stu-id="02014-127">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="02014-128">-Publisher</span><span class="sxs-lookup"><span data-stu-id="02014-128">-Publisher</span></span>
<span data-ttu-id="02014-129">Especifica o nome do editor de extensão.</span><span class="sxs-lookup"><span data-stu-id="02014-129">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="02014-130">O editor fornece um nome quando o editor registra uma extensão.</span><span class="sxs-lookup"><span data-stu-id="02014-130">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="02014-131">Isso pode usar [o cmdlet Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) para obter o editor.</span><span class="sxs-lookup"><span data-stu-id="02014-131">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="02014-132">-Configuração</span><span class="sxs-lookup"><span data-stu-id="02014-132">-Setting</span></span>
<span data-ttu-id="02014-133">Especifica a configuração pública, como uma cadeia de caracteres, para a extensão.</span><span class="sxs-lookup"><span data-stu-id="02014-133">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="02014-134">Este cmdlet não criptografa a configuração pública.</span><span class="sxs-lookup"><span data-stu-id="02014-134">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="02014-135">-Tipo</span><span class="sxs-lookup"><span data-stu-id="02014-135">-Type</span></span>
<span data-ttu-id="02014-136">Especifica o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="02014-136">Specifies the extension type.</span></span>
<span data-ttu-id="02014-137">Você pode usar [o cmdlet Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) para obter o tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="02014-137">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="02014-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="02014-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="02014-139">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="02014-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="02014-140">Você pode usar [o cmdlet Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) para obter a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="02014-140">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="02014-141">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="02014-141">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="02014-142">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="02014-142">Specify the VMSS object.</span></span>
<span data-ttu-id="02014-143">Você pode usar [o New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="02014-143">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="02014-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="02014-144">-Confirm</span></span>
<span data-ttu-id="02014-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02014-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02014-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02014-146">-WhatIf</span></span>
<span data-ttu-id="02014-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="02014-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02014-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02014-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02014-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02014-149">CommonParameters</span></span>
<span data-ttu-id="02014-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02014-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02014-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02014-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02014-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="02014-152">INPUTS</span></span>

### <span data-ttu-id="02014-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="02014-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="02014-154">System.String</span><span class="sxs-lookup"><span data-stu-id="02014-154">System.String</span></span>

### <span data-ttu-id="02014-155">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="02014-155">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="02014-156">System.Object</span><span class="sxs-lookup"><span data-stu-id="02014-156">System.Object</span></span>

## <span data-ttu-id="02014-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="02014-157">OUTPUTS</span></span>

### <span data-ttu-id="02014-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="02014-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="02014-159">Notas</span><span class="sxs-lookup"><span data-stu-id="02014-159">NOTES</span></span>

## <span data-ttu-id="02014-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02014-160">RELATED LINKS</span></span>

[<span data-ttu-id="02014-161">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="02014-161">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="02014-162">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="02014-162">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="02014-163">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="02014-163">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="02014-164">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="02014-164">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="02014-165">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="02014-165">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
