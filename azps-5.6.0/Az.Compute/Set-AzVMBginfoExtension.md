---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: 9b8eafaead04c2e2f727676c78bd717b1c6e97c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891052"
---
# <span data-ttu-id="cdd57-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="cdd57-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="cdd57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdd57-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd57-103">Adiciona a extensão BGInfo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cdd57-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="cdd57-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cdd57-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd57-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cdd57-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd57-106">O cmdlet **Set-AzVMBGInfoExtension** adiciona a extensão BGInfo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cdd57-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="cdd57-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdd57-107">EXAMPLES</span></span>

### <span data-ttu-id="cdd57-108">Exemplo 1: Adicionar a extensão BGInfo para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="cdd57-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="cdd57-109">Este comando adiciona a extensão BGInfo a uma máquina virtual chamada ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="cdd57-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="cdd57-110">O comando especifica o grupo de recursos e o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cdd57-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="cdd57-111">O comando especifica o nome e a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="cdd57-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="cdd57-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cdd57-112">PARAMETERS</span></span>

### <span data-ttu-id="cdd57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd57-113">-DefaultProfile</span></span>
<span data-ttu-id="cdd57-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cdd57-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdd57-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cdd57-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="cdd57-116">Indica que esse cmdlet impede que o agente convidado do Azure atualiza automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="cdd57-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="cdd57-117">Por padrão, esse cmdlet permite que o agente convidado atualize a extensão.</span><span class="sxs-lookup"><span data-stu-id="cdd57-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="cdd57-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="cdd57-118">-ForceRerun</span></span>
<span data-ttu-id="cdd57-119">Especifica que a extensão deve ser executado novamente com as mesmas configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="cdd57-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="cdd57-120">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="cdd57-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="cdd57-121">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="cdd57-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="cdd57-122">-Location</span><span class="sxs-lookup"><span data-stu-id="cdd57-122">-Location</span></span>
<span data-ttu-id="cdd57-123">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cdd57-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="cdd57-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cdd57-124">-Name</span></span>
<span data-ttu-id="cdd57-125">Especifica o nome da extensão BGInfo que este cmdlet adiciona a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cdd57-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="cdd57-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cdd57-126">-NoWait</span></span>
<span data-ttu-id="cdd57-127">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="cdd57-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cdd57-128">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="cdd57-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cdd57-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd57-129">-ResourceGroupName</span></span>
<span data-ttu-id="cdd57-130">Especifica o nome do grupo de recursos da máquina virtual à qual este cmdlet adiciona uma extensão.</span><span class="sxs-lookup"><span data-stu-id="cdd57-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="cdd57-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cdd57-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="cdd57-132">Especifica a versão da extensão que este cmdlet adiciona à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cdd57-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="cdd57-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="cdd57-133">-VMName</span></span>
<span data-ttu-id="cdd57-134">Especifica o nome da máquina virtual à qual este cmdlet adiciona a extensão BGInfo.</span><span class="sxs-lookup"><span data-stu-id="cdd57-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="cdd57-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdd57-135">-Confirm</span></span>
<span data-ttu-id="cdd57-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd57-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd57-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd57-137">-WhatIf</span></span>
<span data-ttu-id="cdd57-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cdd57-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd57-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cdd57-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd57-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd57-140">CommonParameters</span></span>
<span data-ttu-id="cdd57-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd57-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd57-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdd57-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd57-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdd57-143">INPUTS</span></span>

### <span data-ttu-id="cdd57-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cdd57-144">System.String</span></span>

### <span data-ttu-id="cdd57-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cdd57-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cdd57-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cdd57-146">OUTPUTS</span></span>

### <span data-ttu-id="cdd57-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cdd57-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cdd57-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="cdd57-148">NOTES</span></span>

## <span data-ttu-id="cdd57-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdd57-149">RELATED LINKS</span></span>
