---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: d0fb9fb0c6fb27ff683fcbb2b3ae537d736189cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430407"
---
# <span data-ttu-id="18fa0-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18fa0-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="18fa0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="18fa0-103">Move um circuito do ExpressRoute do modelo de implantação clássico para o modelo de implantação do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="18fa0-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18fa0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18fa0-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18fa0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="18fa0-106">O cmdlet **move-AzureRmExpressRouteCircuit** move um circuito do ExpressRoute do modelo de implantação clássico para o modelo de implantação do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="18fa0-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="18fa0-107">Após a movimentação, o circuito do ExpressRoute se comporta e é executado como qualquer outro circuito do ExpressRoute que é criado no modelo de implantação do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="18fa0-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="18fa0-108">Links de circuito, redes virtuais e gateways VPN não são movidos por essa operação.</span><span class="sxs-lookup"><span data-stu-id="18fa0-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="18fa0-109">Esses recursos precisam ser reconfigurados após a mudança.</span><span class="sxs-lookup"><span data-stu-id="18fa0-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="18fa0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18fa0-110">EXAMPLES</span></span>

### <span data-ttu-id="18fa0-111">Exemplo 1: mover um circuito do ExpressRoute para o modelo de implantação do Gerenciador de recursos</span><span class="sxs-lookup"><span data-stu-id="18fa0-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="18fa0-112">OS</span><span class="sxs-lookup"><span data-stu-id="18fa0-112">PARAMETERS</span></span>

### <span data-ttu-id="18fa0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18fa0-113">-AsJob</span></span>
<span data-ttu-id="18fa0-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="18fa0-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fa0-115">-DefaultProfile</span></span>
<span data-ttu-id="18fa0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18fa0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="18fa0-117">-Force</span></span>
<span data-ttu-id="18fa0-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="18fa0-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-119">-Local</span><span class="sxs-lookup"><span data-stu-id="18fa0-119">-Location</span></span>
<span data-ttu-id="18fa0-120">O nome do local do Azure em que o circuito do ExpressRoute reside.</span><span class="sxs-lookup"><span data-stu-id="18fa0-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="18fa0-121">-Name</span></span>
<span data-ttu-id="18fa0-122">O nome do circuito do ExpressRoute a ser movido.</span><span class="sxs-lookup"><span data-stu-id="18fa0-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fa0-123">-ResourceGroupName</span></span>
<span data-ttu-id="18fa0-124">O nome do grupo de recursos que conterá o circuito do ExpressRoute que está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="18fa0-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="18fa0-125">-ServiceKey</span></span>
<span data-ttu-id="18fa0-126">A chave de serviço usada pelo circuito do ExpressRoute no modelo de implantação clássico.</span><span class="sxs-lookup"><span data-stu-id="18fa0-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="18fa0-127">-Tag</span></span>
<span data-ttu-id="18fa0-128">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="18fa0-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18fa0-129">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="18fa0-129">For example:</span></span>

<span data-ttu-id="18fa0-130">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="18fa0-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18fa0-131">-Confirm</span></span>
<span data-ttu-id="18fa0-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18fa0-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18fa0-133">-WhatIf</span></span>
<span data-ttu-id="18fa0-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18fa0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18fa0-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18fa0-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fa0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fa0-136">CommonParameters</span></span>
<span data-ttu-id="18fa0-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18fa0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fa0-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18fa0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fa0-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18fa0-139">INPUTS</span></span>

### <span data-ttu-id="18fa0-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="18fa0-140">None</span></span>
<span data-ttu-id="18fa0-141">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="18fa0-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18fa0-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18fa0-142">OUTPUTS</span></span>

### <span data-ttu-id="18fa0-143">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18fa0-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="18fa0-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18fa0-144">NOTES</span></span>

## <span data-ttu-id="18fa0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18fa0-145">RELATED LINKS</span></span>

[<span data-ttu-id="18fa0-146">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18fa0-146">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="18fa0-147">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18fa0-147">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="18fa0-148">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18fa0-148">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="18fa0-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18fa0-149">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
