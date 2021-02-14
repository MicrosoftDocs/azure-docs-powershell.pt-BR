---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117343"
---
# <span data-ttu-id="3d2b4-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d2b4-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="3d2b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3d2b4-103">Remove um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-103">Removes a route filter.</span></span>

## <span data-ttu-id="3d2b4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d2b4-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d2b4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d2b4-105">DESCRIPTION</span></span>
<span data-ttu-id="3d2b4-106">O **cmdlet Remove-AzRouteFilter** remove um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="3d2b4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3d2b4-107">EXAMPLES</span></span>

### <span data-ttu-id="3d2b4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d2b4-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3d2b4-109">O comando remove o filtro de rota chamado RouteFilter01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3d2b4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d2b4-110">PARAMETERS</span></span>

### <span data-ttu-id="3d2b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d2b4-111">-DefaultProfile</span></span>
<span data-ttu-id="3d2b4-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d2b4-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3d2b4-113">-Force</span></span>
<span data-ttu-id="3d2b4-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3d2b4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d2b4-115">-Name</span></span>
<span data-ttu-id="3d2b4-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-116">The resource name.</span></span>

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

### <span data-ttu-id="3d2b4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d2b4-117">-PassThru</span></span>
<span data-ttu-id="3d2b4-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="3d2b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d2b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="3d2b4-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-120">The resource group name.</span></span>

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

### <span data-ttu-id="3d2b4-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3d2b4-121">-Confirm</span></span>
<span data-ttu-id="3d2b4-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d2b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d2b4-123">-WhatIf</span></span>
<span data-ttu-id="3d2b4-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d2b4-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d2b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d2b4-126">CommonParameters</span></span>
<span data-ttu-id="3d2b4-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d2b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d2b4-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d2b4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d2b4-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="3d2b4-129">INPUTS</span></span>

### <span data-ttu-id="3d2b4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3d2b4-130">System.String</span></span>

## <span data-ttu-id="3d2b4-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="3d2b4-131">OUTPUTS</span></span>

### <span data-ttu-id="3d2b4-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d2b4-132">System.Boolean</span></span>

## <span data-ttu-id="3d2b4-133">Notas</span><span class="sxs-lookup"><span data-stu-id="3d2b4-133">NOTES</span></span>

## <span data-ttu-id="3d2b4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d2b4-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d2b4-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d2b4-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="3d2b4-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d2b4-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="3d2b4-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d2b4-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="3d2b4-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d2b4-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3d2b4-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d2b4-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3d2b4-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d2b4-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3d2b4-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d2b4-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3d2b4-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d2b4-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
