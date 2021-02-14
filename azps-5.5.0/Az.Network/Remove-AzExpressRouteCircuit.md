---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117348"
---
# <span data-ttu-id="96d2b-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="96d2b-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="96d2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="96d2b-103">Remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="96d2b-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="96d2b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96d2b-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96d2b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="96d2b-105">DESCRIPTION</span></span>
<span data-ttu-id="96d2b-106">O cmdlet **Remove-AzExpressRoute Circuit** remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="96d2b-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="96d2b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96d2b-107">EXAMPLES</span></span>

### <span data-ttu-id="96d2b-108">Exemplo 1: Excluir um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="96d2b-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="96d2b-109">Exemplo 2: Excluir um circuito do ExpressRoute usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="96d2b-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="96d2b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96d2b-110">PARAMETERS</span></span>

### <span data-ttu-id="96d2b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96d2b-111">-AsJob</span></span>
<span data-ttu-id="96d2b-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="96d2b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96d2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d2b-113">-DefaultProfile</span></span>
<span data-ttu-id="96d2b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="96d2b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96d2b-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="96d2b-115">-Force</span></span>
<span data-ttu-id="96d2b-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="96d2b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96d2b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="96d2b-117">-Name</span></span>
<span data-ttu-id="96d2b-118">O nome do circuito do ExpressRoute a ser removido.</span><span class="sxs-lookup"><span data-stu-id="96d2b-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="96d2b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96d2b-119">-PassThru</span></span>
<span data-ttu-id="96d2b-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="96d2b-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="96d2b-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="96d2b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96d2b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d2b-122">-ResourceGroupName</span></span>
<span data-ttu-id="96d2b-123">Especifica o nome do grupo de recursos ao que este circuito do ExpressRoute pertence.</span><span class="sxs-lookup"><span data-stu-id="96d2b-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="96d2b-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="96d2b-124">-Confirm</span></span>
<span data-ttu-id="96d2b-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96d2b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96d2b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96d2b-126">-WhatIf</span></span>
<span data-ttu-id="96d2b-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="96d2b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96d2b-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96d2b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96d2b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d2b-129">CommonParameters</span></span>
<span data-ttu-id="96d2b-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d2b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d2b-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d2b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d2b-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="96d2b-132">INPUTS</span></span>

### <span data-ttu-id="96d2b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="96d2b-133">System.String</span></span>

## <span data-ttu-id="96d2b-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="96d2b-134">OUTPUTS</span></span>

### <span data-ttu-id="96d2b-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96d2b-135">System.Boolean</span></span>

## <span data-ttu-id="96d2b-136">Notas</span><span class="sxs-lookup"><span data-stu-id="96d2b-136">NOTES</span></span>

## <span data-ttu-id="96d2b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96d2b-137">RELATED LINKS</span></span>

[<span data-ttu-id="96d2b-138">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="96d2b-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="96d2b-139">Move-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="96d2b-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="96d2b-140">New-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="96d2b-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="96d2b-141">Set-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="96d2b-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
