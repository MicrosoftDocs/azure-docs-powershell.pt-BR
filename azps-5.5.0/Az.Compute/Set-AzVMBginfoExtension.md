---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a98a2f5cbc8034e8cec4d324bb7ecaa28297e772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116884"
---
# <span data-ttu-id="e5fe3-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="e5fe3-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="e5fe3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fe3-103">Adiciona a extensão BGInfo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="e5fe3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5fe3-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5fe3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5fe3-105">DESCRIPTION</span></span>
<span data-ttu-id="e5fe3-106">O cmdlet **Set-AzVMBGInfoExtension** adiciona a extensão BGInfo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="e5fe3-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e5fe3-107">EXAMPLES</span></span>

### <span data-ttu-id="e5fe3-108">Exemplo 1: Adicionar a extensão BGInfo para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e5fe3-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="e5fe3-109">Esse comando adiciona a extensão BGInfo a uma máquina virtual chamada ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="e5fe3-110">O comando especifica o grupo de recursos e o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="e5fe3-111">O comando especifica o nome e a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="e5fe3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5fe3-112">PARAMETERS</span></span>

### <span data-ttu-id="e5fe3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fe3-113">-DefaultProfile</span></span>
<span data-ttu-id="e5fe3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5fe3-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e5fe3-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e5fe3-116">Indica que esse cmdlet impede que o agente convidado do Azure atualiza automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="e5fe3-117">Por padrão, esse cmdlet permite que o agente convidado atualize a extensão.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe3-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="e5fe3-118">-ForceRerun</span></span>
<span data-ttu-id="e5fe3-119">Especifica que a extensão deve ser executado novamente com as mesmas configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="e5fe3-120">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="e5fe3-121">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="e5fe3-122">-Local</span><span class="sxs-lookup"><span data-stu-id="e5fe3-122">-Location</span></span>
<span data-ttu-id="e5fe3-123">Especifica a localização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="e5fe3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5fe3-124">-Name</span></span>
<span data-ttu-id="e5fe3-125">Especifica o nome da extensão BGInfo que este cmdlet adiciona a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe3-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e5fe3-126">-NoWait</span></span>
<span data-ttu-id="e5fe3-127">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e5fe3-128">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e5fe3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5fe3-129">-ResourceGroupName</span></span>
<span data-ttu-id="e5fe3-130">Especifica o nome do grupo de recursos da máquina virtual à qual este cmdlet adiciona uma extensão.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe3-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e5fe3-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="e5fe3-132">Especifica a versão da extensão que este cmdlet adiciona à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe3-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="e5fe3-133">-VMName</span></span>
<span data-ttu-id="e5fe3-134">Especifica o nome da máquina virtual à qual este cmdlet adiciona a extensão BGInfo.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe3-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e5fe3-135">-Confirm</span></span>
<span data-ttu-id="e5fe3-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5fe3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5fe3-137">-WhatIf</span></span>
<span data-ttu-id="e5fe3-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5fe3-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5fe3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fe3-140">CommonParameters</span></span>
<span data-ttu-id="e5fe3-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fe3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fe3-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5fe3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fe3-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="e5fe3-143">INPUTS</span></span>

### <span data-ttu-id="e5fe3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e5fe3-144">System.String</span></span>

### <span data-ttu-id="e5fe3-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e5fe3-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e5fe3-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="e5fe3-146">OUTPUTS</span></span>

### <span data-ttu-id="e5fe3-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e5fe3-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e5fe3-148">Notas</span><span class="sxs-lookup"><span data-stu-id="e5fe3-148">NOTES</span></span>

## <span data-ttu-id="e5fe3-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5fe3-149">RELATED LINKS</span></span>
