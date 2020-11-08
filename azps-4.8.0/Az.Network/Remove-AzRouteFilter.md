---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111538"
---
# <span data-ttu-id="52b87-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="52b87-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="52b87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52b87-102">SYNOPSIS</span></span>
<span data-ttu-id="52b87-103">Remove um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="52b87-103">Removes a route filter.</span></span>

## <span data-ttu-id="52b87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52b87-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52b87-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52b87-105">DESCRIPTION</span></span>
<span data-ttu-id="52b87-106">O cmdlet **Remove-AzRouteFilter** remove um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="52b87-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="52b87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52b87-107">EXAMPLES</span></span>

### <span data-ttu-id="52b87-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52b87-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="52b87-109">O comando Remove o filtro de rota chamado RouteFilter01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="52b87-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="52b87-110">OS</span><span class="sxs-lookup"><span data-stu-id="52b87-110">PARAMETERS</span></span>

### <span data-ttu-id="52b87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b87-111">-DefaultProfile</span></span>
<span data-ttu-id="52b87-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52b87-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52b87-113">-Force</span><span class="sxs-lookup"><span data-stu-id="52b87-113">-Force</span></span>
<span data-ttu-id="52b87-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="52b87-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="52b87-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="52b87-115">-Name</span></span>
<span data-ttu-id="52b87-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="52b87-116">The resource name.</span></span>

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

### <span data-ttu-id="52b87-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52b87-117">-PassThru</span></span>
<span data-ttu-id="52b87-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="52b87-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="52b87-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b87-119">-ResourceGroupName</span></span>
<span data-ttu-id="52b87-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52b87-120">The resource group name.</span></span>

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

### <span data-ttu-id="52b87-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52b87-121">-Confirm</span></span>
<span data-ttu-id="52b87-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b87-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52b87-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52b87-123">-WhatIf</span></span>
<span data-ttu-id="52b87-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52b87-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b87-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52b87-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52b87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b87-126">CommonParameters</span></span>
<span data-ttu-id="52b87-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b87-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b87-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b87-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52b87-129">INPUTS</span></span>

### <span data-ttu-id="52b87-130">System. String</span><span class="sxs-lookup"><span data-stu-id="52b87-130">System.String</span></span>

## <span data-ttu-id="52b87-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52b87-131">OUTPUTS</span></span>

### <span data-ttu-id="52b87-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52b87-132">System.Boolean</span></span>

## <span data-ttu-id="52b87-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52b87-133">NOTES</span></span>

## <span data-ttu-id="52b87-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52b87-134">RELATED LINKS</span></span>

[<span data-ttu-id="52b87-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="52b87-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="52b87-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="52b87-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="52b87-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="52b87-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="52b87-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="52b87-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="52b87-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="52b87-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="52b87-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="52b87-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="52b87-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="52b87-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="52b87-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="52b87-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
