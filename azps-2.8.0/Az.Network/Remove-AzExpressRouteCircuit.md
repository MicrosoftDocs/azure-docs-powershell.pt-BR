---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: a4672e459a692ce8c0c19b35bf68240d979e75ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771537"
---
# <span data-ttu-id="c4563-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c4563-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="c4563-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4563-102">SYNOPSIS</span></span>
<span data-ttu-id="c4563-103">Remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c4563-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c4563-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4563-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4563-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4563-105">DESCRIPTION</span></span>
<span data-ttu-id="c4563-106">O cmdlet **Remove-AzExpressRouteCircuit** remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c4563-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c4563-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4563-107">EXAMPLES</span></span>

### <span data-ttu-id="c4563-108">Exemplo 1: excluir um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c4563-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="c4563-109">Exemplo 2: excluir um circuito do ExpressRoute usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="c4563-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="c4563-110">OS</span><span class="sxs-lookup"><span data-stu-id="c4563-110">PARAMETERS</span></span>

### <span data-ttu-id="c4563-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4563-111">-AsJob</span></span>
<span data-ttu-id="c4563-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c4563-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4563-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4563-113">-DefaultProfile</span></span>
<span data-ttu-id="c4563-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4563-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4563-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c4563-115">-Force</span></span>
<span data-ttu-id="c4563-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c4563-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4563-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4563-117">-Name</span></span>
<span data-ttu-id="c4563-118">O nome do circuito do ExpressRoute a ser removido.</span><span class="sxs-lookup"><span data-stu-id="c4563-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="c4563-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4563-119">-PassThru</span></span>
<span data-ttu-id="c4563-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c4563-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="c4563-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c4563-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c4563-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4563-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4563-123">Especifica o nome do grupo de recursos ao qual este circuito do ExpressRoute pertence.</span><span class="sxs-lookup"><span data-stu-id="c4563-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="c4563-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4563-124">-Confirm</span></span>
<span data-ttu-id="c4563-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4563-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4563-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4563-126">-WhatIf</span></span>
<span data-ttu-id="c4563-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4563-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4563-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4563-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4563-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4563-129">CommonParameters</span></span>
<span data-ttu-id="c4563-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4563-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4563-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4563-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4563-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4563-132">INPUTS</span></span>

### <span data-ttu-id="c4563-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c4563-133">System.String</span></span>

## <span data-ttu-id="c4563-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4563-134">OUTPUTS</span></span>

### <span data-ttu-id="c4563-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4563-135">System.Boolean</span></span>

## <span data-ttu-id="c4563-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4563-136">NOTES</span></span>

## <span data-ttu-id="c4563-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4563-137">RELATED LINKS</span></span>

[<span data-ttu-id="c4563-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c4563-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c4563-139">Mover-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c4563-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="c4563-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c4563-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="c4563-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c4563-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
