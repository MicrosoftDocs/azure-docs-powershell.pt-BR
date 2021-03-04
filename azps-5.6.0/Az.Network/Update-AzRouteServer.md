---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 3cb1fe0fb72182e22c4f7653de26f356ecd823ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885338"
---
# <span data-ttu-id="d2759-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="d2759-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="d2759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2759-102">SYNOPSIS</span></span>
<span data-ttu-id="d2759-103">Atualize um RouteServer do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2759-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="d2759-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2759-104">SYNTAX</span></span>

### <span data-ttu-id="d2759-105">RouteServerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2759-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2759-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2759-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2759-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2759-107">DESCRIPTION</span></span>
<span data-ttu-id="d2759-108">O cmdlet **Update-AzRouteServer** alterna o tráfego de filial para filial para um RouteServer do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2759-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="d2759-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2759-109">EXAMPLES</span></span>

### <span data-ttu-id="d2759-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2759-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="d2759-111">Para habilitar o branch para ramificar o tráfego para o servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="d2759-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="d2759-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2759-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="d2759-113">Para desabilitar o branch para o tráfego de filial para o servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="d2759-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="d2759-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2759-114">PARAMETERS</span></span>

### <span data-ttu-id="d2759-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="d2759-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="d2759-116">Sinalizador para permitir que o branch ramifica o tráfego para o servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="d2759-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="d2759-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2759-117">-DefaultProfile</span></span>
<span data-ttu-id="d2759-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2759-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2759-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2759-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2759-120">O nome do grupo de recursos do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="d2759-120">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2759-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2759-121">-ResourceId</span></span>
<span data-ttu-id="d2759-122">ResourceId do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="d2759-122">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2759-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="d2759-123">-RouteServerName</span></span>
<span data-ttu-id="d2759-124">O nome do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="d2759-124">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2759-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2759-125">-Confirm</span></span>
<span data-ttu-id="d2759-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2759-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2759-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2759-127">-WhatIf</span></span>
<span data-ttu-id="d2759-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2759-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2759-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2759-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2759-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2759-130">CommonParameters</span></span>
<span data-ttu-id="d2759-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2759-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2759-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2759-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2759-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2759-133">INPUTS</span></span>

### <span data-ttu-id="d2759-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d2759-134">System.String</span></span>

## <span data-ttu-id="d2759-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2759-135">OUTPUTS</span></span>

### <span data-ttu-id="d2759-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="d2759-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="d2759-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2759-137">NOTES</span></span>

## <span data-ttu-id="d2759-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2759-138">RELATED LINKS</span></span>
