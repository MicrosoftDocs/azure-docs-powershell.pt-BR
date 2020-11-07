---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: e9a93b66f62f6a42ba400dd84b6890cdf9f81cec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785169"
---
# <span data-ttu-id="e2ff0-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2ff0-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="e2ff0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ff0-103">Remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2ff0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2ff0-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2ff0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2ff0-105">DESCRIPTION</span></span>
<span data-ttu-id="e2ff0-106">O cmdlet **Remove-AzureRmExpressRouteCircuit** remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e2ff0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2ff0-107">EXAMPLES</span></span>

### <span data-ttu-id="e2ff0-108">Exemplo 1: excluir um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e2ff0-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="e2ff0-109">Exemplo 2: excluir um circuito do ExpressRoute usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="e2ff0-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="e2ff0-110">OS</span><span class="sxs-lookup"><span data-stu-id="e2ff0-110">PARAMETERS</span></span>

### <span data-ttu-id="e2ff0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2ff0-111">-AsJob</span></span>
<span data-ttu-id="e2ff0-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e2ff0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2ff0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ff0-113">-DefaultProfile</span></span>
<span data-ttu-id="e2ff0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2ff0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e2ff0-115">-Force</span></span>
<span data-ttu-id="e2ff0-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2ff0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2ff0-117">-Name</span></span>
<span data-ttu-id="e2ff0-118">O nome do circuito do ExpressRoute a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="e2ff0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2ff0-119">-PassThru</span></span>
<span data-ttu-id="e2ff0-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e2ff0-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e2ff0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ff0-122">-ResourceGroupName</span></span>
<span data-ttu-id="e2ff0-123">Especifica o nome do grupo de recursos ao qual este circuito do ExpressRoute pertence.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="e2ff0-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2ff0-124">-Confirm</span></span>
<span data-ttu-id="e2ff0-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ff0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ff0-126">-WhatIf</span></span>
<span data-ttu-id="e2ff0-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ff0-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ff0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ff0-129">CommonParameters</span></span>
<span data-ttu-id="e2ff0-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ff0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ff0-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2ff0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ff0-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2ff0-132">INPUTS</span></span>

## <span data-ttu-id="e2ff0-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2ff0-133">OUTPUTS</span></span>

## <span data-ttu-id="e2ff0-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2ff0-134">NOTES</span></span>

## <span data-ttu-id="e2ff0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2ff0-135">RELATED LINKS</span></span>

[<span data-ttu-id="e2ff0-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2ff0-136">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e2ff0-137">Mover-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2ff0-137">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e2ff0-138">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2ff0-138">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e2ff0-139">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2ff0-139">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
