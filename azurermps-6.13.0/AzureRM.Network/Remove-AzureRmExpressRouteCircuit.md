---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e38cdc9a7f0b34fa5e7769192fa5fcb0ad342de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432286"
---
# <span data-ttu-id="8d51d-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8d51d-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="8d51d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d51d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d51d-103">Remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8d51d-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d51d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d51d-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d51d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d51d-105">DESCRIPTION</span></span>
<span data-ttu-id="8d51d-106">O cmdlet **Remove-AzureRmExpressRouteCircuit** remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8d51d-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="8d51d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d51d-107">EXAMPLES</span></span>

### <span data-ttu-id="8d51d-108">Exemplo 1: excluir um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="8d51d-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="8d51d-109">Exemplo 2: excluir um circuito do ExpressRoute usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="8d51d-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="8d51d-110">OS</span><span class="sxs-lookup"><span data-stu-id="8d51d-110">PARAMETERS</span></span>

### <span data-ttu-id="8d51d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d51d-111">-AsJob</span></span>
<span data-ttu-id="8d51d-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8d51d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d51d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d51d-113">-DefaultProfile</span></span>
<span data-ttu-id="8d51d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d51d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d51d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8d51d-115">-Force</span></span>
<span data-ttu-id="8d51d-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d51d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d51d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d51d-117">-Name</span></span>
<span data-ttu-id="8d51d-118">O nome do circuito do ExpressRoute a ser removido.</span><span class="sxs-lookup"><span data-stu-id="8d51d-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="8d51d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d51d-119">-PassThru</span></span>
<span data-ttu-id="8d51d-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8d51d-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8d51d-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8d51d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8d51d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d51d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8d51d-123">Especifica o nome do grupo de recursos ao qual este circuito do ExpressRoute pertence.</span><span class="sxs-lookup"><span data-stu-id="8d51d-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="8d51d-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d51d-124">-Confirm</span></span>
<span data-ttu-id="8d51d-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d51d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d51d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d51d-126">-WhatIf</span></span>
<span data-ttu-id="8d51d-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d51d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d51d-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d51d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d51d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d51d-129">CommonParameters</span></span>
<span data-ttu-id="8d51d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d51d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d51d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d51d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d51d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d51d-132">INPUTS</span></span>

### <span data-ttu-id="8d51d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8d51d-133">System.String</span></span>

## <span data-ttu-id="8d51d-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d51d-134">OUTPUTS</span></span>

### <span data-ttu-id="8d51d-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d51d-135">System.Boolean</span></span>

## <span data-ttu-id="8d51d-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d51d-136">NOTES</span></span>

## <span data-ttu-id="8d51d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d51d-137">RELATED LINKS</span></span>

[<span data-ttu-id="8d51d-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8d51d-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8d51d-139">Mover-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8d51d-139">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8d51d-140">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8d51d-140">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8d51d-141">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8d51d-141">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
