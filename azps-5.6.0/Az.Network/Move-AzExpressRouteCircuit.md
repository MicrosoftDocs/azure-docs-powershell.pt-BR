---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 6964767438fac6a1afd8da4333560f49cfe1bb44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885411"
---
# <span data-ttu-id="f147c-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f147c-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="f147c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f147c-102">SYNOPSIS</span></span>
<span data-ttu-id="f147c-103">Move um circuito ExpressRoute do modelo de implantação clássico para o modelo de implantação do Gerenciador de Recursos.</span><span class="sxs-lookup"><span data-stu-id="f147c-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="f147c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f147c-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f147c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f147c-105">DESCRIPTION</span></span>
<span data-ttu-id="f147c-106">O cmdlet **Move-AzExpressRouteCircuit** move um circuito ExpressRoute do modelo de implantação clássico para o modelo de implantação do Gerenciador de Recursos.</span><span class="sxs-lookup"><span data-stu-id="f147c-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="f147c-107">Após a movimentação, o circuito ExpressRoute se comporta e se comporta como qualquer outro circuito ExpressRoute criado no modelo de implantação do Gerenciador de Recursos.</span><span class="sxs-lookup"><span data-stu-id="f147c-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="f147c-108">Links de circuitos, redes virtuais e gateways VPN não são movidos por essa operação.</span><span class="sxs-lookup"><span data-stu-id="f147c-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="f147c-109">Esses recursos precisam ser reconfigurados após a movimentação.</span><span class="sxs-lookup"><span data-stu-id="f147c-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="f147c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f147c-110">EXAMPLES</span></span>

### <span data-ttu-id="f147c-111">Exemplo 1: mover um circuito ExpressRoute para o modelo de implantação do Gerenciador de Recursos</span><span class="sxs-lookup"><span data-stu-id="f147c-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="f147c-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f147c-112">PARAMETERS</span></span>

### <span data-ttu-id="f147c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f147c-113">-AsJob</span></span>
<span data-ttu-id="f147c-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f147c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f147c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f147c-115">-DefaultProfile</span></span>
<span data-ttu-id="f147c-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f147c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f147c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f147c-117">-Force</span></span>
<span data-ttu-id="f147c-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f147c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f147c-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f147c-119">-Location</span></span>
<span data-ttu-id="f147c-120">O nome do local do Azure onde o circuito ExpressRoute reside.</span><span class="sxs-lookup"><span data-stu-id="f147c-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="f147c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f147c-121">-Name</span></span>
<span data-ttu-id="f147c-122">O nome do circuito ExpressRoute a ser movido.</span><span class="sxs-lookup"><span data-stu-id="f147c-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="f147c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f147c-123">-ResourceGroupName</span></span>
<span data-ttu-id="f147c-124">O nome do grupo de recursos que conterá o circuito ExpressRoute sendo movido.</span><span class="sxs-lookup"><span data-stu-id="f147c-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="f147c-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="f147c-125">-ServiceKey</span></span>
<span data-ttu-id="f147c-126">A Chave de Serviço usada pelo circuito ExpressRoute no modelo de implantação clássico.</span><span class="sxs-lookup"><span data-stu-id="f147c-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="f147c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f147c-127">-Tag</span></span>
<span data-ttu-id="f147c-128">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f147c-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f147c-129">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f147c-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f147c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f147c-130">-Confirm</span></span>
<span data-ttu-id="f147c-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f147c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f147c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f147c-132">-WhatIf</span></span>
<span data-ttu-id="f147c-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f147c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f147c-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f147c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f147c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f147c-135">CommonParameters</span></span>
<span data-ttu-id="f147c-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f147c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f147c-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f147c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f147c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f147c-138">INPUTS</span></span>

### <span data-ttu-id="f147c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f147c-139">System.String</span></span>

### <span data-ttu-id="f147c-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f147c-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f147c-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f147c-141">OUTPUTS</span></span>

### <span data-ttu-id="f147c-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f147c-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f147c-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="f147c-143">NOTES</span></span>

## <span data-ttu-id="f147c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f147c-144">RELATED LINKS</span></span>

[<span data-ttu-id="f147c-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f147c-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f147c-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f147c-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="f147c-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f147c-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="f147c-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f147c-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
