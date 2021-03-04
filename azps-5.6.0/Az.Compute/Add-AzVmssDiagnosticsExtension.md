---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 93e9f660b0667286e5ce8c799b5404caae0ba0c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887581"
---
# <span data-ttu-id="b92e1-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b92e1-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="b92e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b92e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b92e1-103">Adiciona uma extensão de diagnóstico ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="b92e1-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="b92e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b92e1-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b92e1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b92e1-105">DESCRIPTION</span></span>
<span data-ttu-id="b92e1-106">O cmdlet **Add-AzVmssDiagnosticsExtension** adiciona uma extensão de diagnóstico à instância do Conjunto de Escala de Máquina Virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b92e1-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b92e1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b92e1-107">EXAMPLES</span></span>

### <span data-ttu-id="b92e1-108">Exemplo 1: Adicionar uma extensão de diagnóstico ao VMSS</span><span class="sxs-lookup"><span data-stu-id="b92e1-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="b92e1-109">Este comando adiciona uma extensão de diagnóstico ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="b92e1-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="b92e1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b92e1-110">PARAMETERS</span></span>

### <span data-ttu-id="b92e1-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b92e1-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b92e1-112">Indica se esse cmdlet permite que o agente convidado do Azure atualize automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="b92e1-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b92e1-113">-DefaultProfile</span></span>
<span data-ttu-id="b92e1-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b92e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b92e1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b92e1-115">-Force</span></span>
<span data-ttu-id="b92e1-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b92e1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b92e1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b92e1-117">-Name</span></span>
<span data-ttu-id="b92e1-118">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="b92e1-118">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92e1-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="b92e1-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="b92e1-120">Especifica o caminho do arquivo de configuração particular.</span><span class="sxs-lookup"><span data-stu-id="b92e1-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="b92e1-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="b92e1-121">-SettingFilePath</span></span>
<span data-ttu-id="b92e1-122">Especifica o caminho do arquivo de configuração pública.</span><span class="sxs-lookup"><span data-stu-id="b92e1-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="b92e1-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b92e1-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="b92e1-124">Especifica a versão da extensão a ser usada para este VMSS.</span><span class="sxs-lookup"><span data-stu-id="b92e1-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="b92e1-125">Para obter a versão, execute o cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) com um valor Microsoft.Azure.Diagnostics para o parâmetro *PublisherName* e IaaSDiagnosticstics para o *parâmetro Type.*</span><span class="sxs-lookup"><span data-stu-id="b92e1-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92e1-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b92e1-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b92e1-127">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="b92e1-127">Specify the VMSS object.</span></span>
<span data-ttu-id="b92e1-128">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="b92e1-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="b92e1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b92e1-129">-Confirm</span></span>
<span data-ttu-id="b92e1-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b92e1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b92e1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b92e1-131">-WhatIf</span></span>
<span data-ttu-id="b92e1-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b92e1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b92e1-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b92e1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b92e1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b92e1-134">CommonParameters</span></span>
<span data-ttu-id="b92e1-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b92e1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b92e1-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b92e1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b92e1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b92e1-137">INPUTS</span></span>

### <span data-ttu-id="b92e1-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b92e1-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b92e1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b92e1-139">System.String</span></span>

### <span data-ttu-id="b92e1-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b92e1-140">System.Boolean</span></span>

## <span data-ttu-id="b92e1-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b92e1-141">OUTPUTS</span></span>

### <span data-ttu-id="b92e1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b92e1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b92e1-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="b92e1-143">NOTES</span></span>

## <span data-ttu-id="b92e1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b92e1-144">RELATED LINKS</span></span>

[<span data-ttu-id="b92e1-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b92e1-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="b92e1-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b92e1-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="b92e1-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b92e1-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
