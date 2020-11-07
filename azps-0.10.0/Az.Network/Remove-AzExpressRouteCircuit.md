---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: 4dbddf7e78297acc3f12f69dd2a44f9698f7b891
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775306"
---
# <span data-ttu-id="88f93-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f93-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="88f93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88f93-102">SYNOPSIS</span></span>
<span data-ttu-id="88f93-103">Remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="88f93-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="88f93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88f93-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88f93-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88f93-105">DESCRIPTION</span></span>
<span data-ttu-id="88f93-106">O cmdlet **Remove-AzExpressRouteCircuit** remove um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="88f93-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="88f93-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88f93-107">EXAMPLES</span></span>

### <span data-ttu-id="88f93-108">Exemplo 1: excluir um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="88f93-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="88f93-109">Exemplo 2: excluir um circuito do ExpressRoute usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="88f93-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="88f93-110">OS</span><span class="sxs-lookup"><span data-stu-id="88f93-110">PARAMETERS</span></span>

### <span data-ttu-id="88f93-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88f93-111">-AsJob</span></span>
<span data-ttu-id="88f93-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="88f93-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88f93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f93-113">-DefaultProfile</span></span>
<span data-ttu-id="88f93-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88f93-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88f93-115">-Force</span><span class="sxs-lookup"><span data-stu-id="88f93-115">-Force</span></span>
<span data-ttu-id="88f93-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="88f93-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88f93-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="88f93-117">-Name</span></span>
<span data-ttu-id="88f93-118">O nome do circuito do ExpressRoute a ser removido.</span><span class="sxs-lookup"><span data-stu-id="88f93-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="88f93-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88f93-119">-PassThru</span></span>
<span data-ttu-id="88f93-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="88f93-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="88f93-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="88f93-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="88f93-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f93-122">-ResourceGroupName</span></span>
<span data-ttu-id="88f93-123">Especifica o nome do grupo de recursos ao qual este circuito do ExpressRoute pertence.</span><span class="sxs-lookup"><span data-stu-id="88f93-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="88f93-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88f93-124">-Confirm</span></span>
<span data-ttu-id="88f93-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88f93-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88f93-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f93-126">-WhatIf</span></span>
<span data-ttu-id="88f93-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88f93-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88f93-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88f93-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88f93-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f93-129">CommonParameters</span></span>
<span data-ttu-id="88f93-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88f93-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f93-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88f93-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f93-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88f93-132">INPUTS</span></span>

## <span data-ttu-id="88f93-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88f93-133">OUTPUTS</span></span>

## <span data-ttu-id="88f93-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88f93-134">NOTES</span></span>

## <span data-ttu-id="88f93-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88f93-135">RELATED LINKS</span></span>

[<span data-ttu-id="88f93-136">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f93-136">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="88f93-137">Mover-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f93-137">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="88f93-138">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f93-138">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="88f93-139">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f93-139">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
