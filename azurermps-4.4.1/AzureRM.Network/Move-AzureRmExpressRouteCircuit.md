---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432180"
---
# <span data-ttu-id="15a53-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15a53-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="15a53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15a53-102">SYNOPSIS</span></span>
<span data-ttu-id="15a53-103">Move um circuito do ExpressRoute do modelo de implantação clássico para o modelo de implantação do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="15a53-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15a53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15a53-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a53-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15a53-105">DESCRIPTION</span></span>
<span data-ttu-id="15a53-106">O cmdlet **move-AzureRmExpressRouteCircuit** move um circuito do ExpressRoute do modelo de implantação clássico para o modelo de implantação do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="15a53-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="15a53-107">Após a movimentação, o circuito do ExpressRoute se comporta e é executado como qualquer outro circuito do ExpressRoute que é criado no modelo de implantação do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="15a53-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="15a53-108">Links de circuito, redes virtuais e gateways VPN não são movidos por essa operação.</span><span class="sxs-lookup"><span data-stu-id="15a53-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="15a53-109">Esses recursos precisam ser reconfigurados após a mudança.</span><span class="sxs-lookup"><span data-stu-id="15a53-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="15a53-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15a53-110">EXAMPLES</span></span>

### <span data-ttu-id="15a53-111">Exemplo 1: mover um circuito do ExpressRoute para o modelo de implantação do Gerenciador de recursos</span><span class="sxs-lookup"><span data-stu-id="15a53-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="15a53-112">OS</span><span class="sxs-lookup"><span data-stu-id="15a53-112">PARAMETERS</span></span>

### <span data-ttu-id="15a53-113">-Force</span><span class="sxs-lookup"><span data-stu-id="15a53-113">-Force</span></span>
<span data-ttu-id="15a53-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="15a53-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15a53-115">-Local</span><span class="sxs-lookup"><span data-stu-id="15a53-115">-Location</span></span>
<span data-ttu-id="15a53-116">O nome do local do Azure em que o circuito do ExpressRoute reside.</span><span class="sxs-lookup"><span data-stu-id="15a53-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="15a53-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="15a53-117">-Name</span></span>
<span data-ttu-id="15a53-118">O nome do circuito do ExpressRoute a ser movido.</span><span class="sxs-lookup"><span data-stu-id="15a53-118">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="15a53-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a53-119">-ResourceGroupName</span></span>
<span data-ttu-id="15a53-120">O nome do grupo de recursos que conterá o circuito do ExpressRoute que está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="15a53-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="15a53-121">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="15a53-121">-ServiceKey</span></span>
<span data-ttu-id="15a53-122">A chave de serviço usada pelo circuito do ExpressRoute no modelo de implantação clássico.</span><span class="sxs-lookup"><span data-stu-id="15a53-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="15a53-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="15a53-123">-Tag</span></span>
<span data-ttu-id="15a53-124">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="15a53-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="15a53-125">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="15a53-125">For example:</span></span>

<span data-ttu-id="15a53-126">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="15a53-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="15a53-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15a53-127">-Confirm</span></span>
<span data-ttu-id="15a53-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15a53-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a53-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a53-129">-WhatIf</span></span>
<span data-ttu-id="15a53-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15a53-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a53-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15a53-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a53-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a53-132">-DefaultProfile</span></span>
<span data-ttu-id="15a53-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15a53-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a53-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a53-134">CommonParameters</span></span>
<span data-ttu-id="15a53-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a53-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a53-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a53-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a53-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15a53-137">INPUTS</span></span>

## <span data-ttu-id="15a53-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15a53-138">OUTPUTS</span></span>

### <span data-ttu-id="15a53-139">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15a53-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="15a53-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15a53-140">NOTES</span></span>

## <span data-ttu-id="15a53-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15a53-141">RELATED LINKS</span></span>

[<span data-ttu-id="15a53-142">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15a53-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="15a53-143">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15a53-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="15a53-144">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15a53-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="15a53-145">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="15a53-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
