---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: 94730c362ae9854179525212971dda5c2ad1feae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891155"
---
# <span data-ttu-id="71954-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71954-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="71954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71954-102">SYNOPSIS</span></span>
<span data-ttu-id="71954-103">Remove um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="71954-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="71954-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="71954-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71954-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="71954-105">DESCRIPTION</span></span>
<span data-ttu-id="71954-106">O cmdlet **Remove-AzExpressRouteCircuit** remove um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="71954-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="71954-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71954-107">EXAMPLES</span></span>

### <span data-ttu-id="71954-108">Exemplo 1: Excluir um circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="71954-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="71954-109">Exemplo 2: Excluir um circuito ExpressRoute usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="71954-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="71954-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="71954-110">PARAMETERS</span></span>

### <span data-ttu-id="71954-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71954-111">-AsJob</span></span>
<span data-ttu-id="71954-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="71954-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71954-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71954-113">-DefaultProfile</span></span>
<span data-ttu-id="71954-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="71954-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71954-115">-Force</span><span class="sxs-lookup"><span data-stu-id="71954-115">-Force</span></span>
<span data-ttu-id="71954-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="71954-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71954-117">-Name</span><span class="sxs-lookup"><span data-stu-id="71954-117">-Name</span></span>
<span data-ttu-id="71954-118">O nome do circuito ExpressRoute a ser removido.</span><span class="sxs-lookup"><span data-stu-id="71954-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71954-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71954-119">-PassThru</span></span>
<span data-ttu-id="71954-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="71954-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="71954-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="71954-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71954-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71954-122">-ResourceGroupName</span></span>
<span data-ttu-id="71954-123">Especifica o nome do grupo de recursos ao que este circuito ExpressRoute pertence.</span><span class="sxs-lookup"><span data-stu-id="71954-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71954-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71954-124">-Confirm</span></span>
<span data-ttu-id="71954-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71954-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71954-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71954-126">-WhatIf</span></span>
<span data-ttu-id="71954-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71954-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71954-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71954-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71954-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71954-129">CommonParameters</span></span>
<span data-ttu-id="71954-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71954-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71954-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71954-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71954-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71954-132">INPUTS</span></span>

### <span data-ttu-id="71954-133">System.String</span><span class="sxs-lookup"><span data-stu-id="71954-133">System.String</span></span>

## <span data-ttu-id="71954-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="71954-134">OUTPUTS</span></span>

### <span data-ttu-id="71954-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71954-135">System.Boolean</span></span>

## <span data-ttu-id="71954-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="71954-136">NOTES</span></span>

## <span data-ttu-id="71954-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71954-137">RELATED LINKS</span></span>

[<span data-ttu-id="71954-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71954-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="71954-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71954-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="71954-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71954-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="71954-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71954-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
