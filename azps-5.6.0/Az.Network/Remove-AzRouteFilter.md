---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 0b75cdb63d2a8bb3c01a93a90ee01db096cf7fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888463"
---
# <span data-ttu-id="3a18c-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3a18c-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="3a18c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a18c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a18c-103">Remove um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="3a18c-103">Removes a route filter.</span></span>

## <span data-ttu-id="3a18c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3a18c-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a18c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3a18c-105">DESCRIPTION</span></span>
<span data-ttu-id="3a18c-106">O cmdlet **Remove-AzRouteFilter** remove um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="3a18c-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="3a18c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a18c-107">EXAMPLES</span></span>

### <span data-ttu-id="3a18c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a18c-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3a18c-109">O comando remove o filtro de rota chamado RouteFilter01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3a18c-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3a18c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3a18c-110">PARAMETERS</span></span>

### <span data-ttu-id="3a18c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a18c-111">-DefaultProfile</span></span>
<span data-ttu-id="3a18c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3a18c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a18c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3a18c-113">-Force</span></span>
<span data-ttu-id="3a18c-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3a18c-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3a18c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3a18c-115">-Name</span></span>
<span data-ttu-id="3a18c-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3a18c-116">The resource name.</span></span>

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

### <span data-ttu-id="3a18c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a18c-117">-PassThru</span></span>
<span data-ttu-id="3a18c-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3a18c-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="3a18c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a18c-119">-ResourceGroupName</span></span>
<span data-ttu-id="3a18c-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a18c-120">The resource group name.</span></span>

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

### <span data-ttu-id="3a18c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a18c-121">-Confirm</span></span>
<span data-ttu-id="3a18c-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a18c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a18c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a18c-123">-WhatIf</span></span>
<span data-ttu-id="3a18c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a18c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a18c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a18c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a18c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a18c-126">CommonParameters</span></span>
<span data-ttu-id="3a18c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a18c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a18c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a18c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a18c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a18c-129">INPUTS</span></span>

### <span data-ttu-id="3a18c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3a18c-130">System.String</span></span>

## <span data-ttu-id="3a18c-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3a18c-131">OUTPUTS</span></span>

### <span data-ttu-id="3a18c-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a18c-132">System.Boolean</span></span>

## <span data-ttu-id="3a18c-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="3a18c-133">NOTES</span></span>

## <span data-ttu-id="3a18c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a18c-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a18c-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3a18c-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="3a18c-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3a18c-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="3a18c-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3a18c-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="3a18c-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a18c-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3a18c-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a18c-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3a18c-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a18c-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3a18c-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a18c-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3a18c-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a18c-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
