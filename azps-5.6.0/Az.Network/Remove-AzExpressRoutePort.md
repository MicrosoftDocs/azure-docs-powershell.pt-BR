---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: c0110186277df7e41b9110b1cfdf2fa7b948b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891148"
---
# <span data-ttu-id="8eea7-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8eea7-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="8eea7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eea7-102">SYNOPSIS</span></span>
<span data-ttu-id="8eea7-103">Remove um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8eea7-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="8eea7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8eea7-104">SYNTAX</span></span>

### <span data-ttu-id="8eea7-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8eea7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eea7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eea7-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eea7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eea7-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eea7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8eea7-108">DESCRIPTION</span></span>
<span data-ttu-id="8eea7-109">O cmdlet **Remove-AzExpressRoutePort** remove um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8eea7-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="8eea7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8eea7-110">EXAMPLES</span></span>

### <span data-ttu-id="8eea7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8eea7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="8eea7-112">Remove $PortName recurso ExpressRoutePort no $rg de recursos em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="8eea7-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="8eea7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8eea7-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="8eea7-114">Remove o recurso ExpressRoutePort em InputObject.</span><span class="sxs-lookup"><span data-stu-id="8eea7-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="8eea7-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8eea7-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="8eea7-116">Remove o recurso ExpressRoutePort com ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="8eea7-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="8eea7-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8eea7-117">PARAMETERS</span></span>

### <span data-ttu-id="8eea7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8eea7-118">-AsJob</span></span>
<span data-ttu-id="8eea7-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8eea7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8eea7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eea7-120">-DefaultProfile</span></span>
<span data-ttu-id="8eea7-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8eea7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eea7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8eea7-122">-Force</span></span>
<span data-ttu-id="8eea7-123">Não peça confirmação se você deseja excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="8eea7-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8eea7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eea7-124">-InputObject</span></span>
<span data-ttu-id="8eea7-125">O objeto de porta de rota expressa</span><span class="sxs-lookup"><span data-stu-id="8eea7-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eea7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8eea7-126">-Name</span></span>
<span data-ttu-id="8eea7-127">O nome do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8eea7-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eea7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8eea7-128">-PassThru</span></span>
<span data-ttu-id="8eea7-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8eea7-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8eea7-130">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8eea7-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8eea7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eea7-131">-ResourceGroupName</span></span>
<span data-ttu-id="8eea7-132">O nome do grupo de recursos do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8eea7-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eea7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eea7-133">-ResourceId</span></span>
<span data-ttu-id="8eea7-134">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="8eea7-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eea7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8eea7-135">-Confirm</span></span>
<span data-ttu-id="8eea7-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eea7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eea7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eea7-137">-WhatIf</span></span>
<span data-ttu-id="8eea7-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8eea7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eea7-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8eea7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eea7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eea7-140">CommonParameters</span></span>
<span data-ttu-id="8eea7-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eea7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eea7-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eea7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eea7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8eea7-143">INPUTS</span></span>

### <span data-ttu-id="8eea7-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8eea7-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="8eea7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8eea7-145">System.String</span></span>

## <span data-ttu-id="8eea7-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8eea7-146">OUTPUTS</span></span>

### <span data-ttu-id="8eea7-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8eea7-147">System.Boolean</span></span>

## <span data-ttu-id="8eea7-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="8eea7-148">NOTES</span></span>

## <span data-ttu-id="8eea7-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eea7-149">RELATED LINKS</span></span>

[<span data-ttu-id="8eea7-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8eea7-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="8eea7-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8eea7-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="8eea7-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8eea7-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
