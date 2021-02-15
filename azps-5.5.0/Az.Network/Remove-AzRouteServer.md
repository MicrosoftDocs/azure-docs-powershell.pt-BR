---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 2b50d49c108408e1639b5f5f490c2aaafc7bbd82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114647"
---
# <span data-ttu-id="d7f80-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="d7f80-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="d7f80-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7f80-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f80-103">Exclui um Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="d7f80-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="d7f80-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7f80-104">SYNTAX</span></span>

### <span data-ttu-id="d7f80-105">RouteServerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7f80-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7f80-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7f80-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7f80-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7f80-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7f80-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7f80-108">DESCRIPTION</span></span>
<span data-ttu-id="d7f80-109">O **cmdlet Remove-AzRouteServer** exclui um Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="d7f80-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="d7f80-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7f80-110">EXAMPLES</span></span>

### <span data-ttu-id="d7f80-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7f80-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="d7f80-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d7f80-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="d7f80-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d7f80-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="d7f80-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7f80-114">PARAMETERS</span></span>

### <span data-ttu-id="d7f80-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7f80-115">-AsJob</span></span>
<span data-ttu-id="d7f80-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d7f80-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7f80-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f80-117">-DefaultProfile</span></span>
<span data-ttu-id="d7f80-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f80-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7f80-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="d7f80-119">-Force</span></span>
<span data-ttu-id="d7f80-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="d7f80-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d7f80-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7f80-121">-InputObject</span></span>
<span data-ttu-id="d7f80-122">O objeto de entrada do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="d7f80-122">The route server input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServer
Parameter Sets: RouteServerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f80-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7f80-123">-PassThru</span></span>
<span data-ttu-id="d7f80-124">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="d7f80-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="d7f80-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7f80-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7f80-126">O nome do grupo de recursos do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="d7f80-126">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="d7f80-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7f80-127">-ResourceId</span></span>
<span data-ttu-id="d7f80-128">A ID de recurso do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="d7f80-128">The route server resource Id.</span></span>

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

### <span data-ttu-id="d7f80-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="d7f80-129">-RouteServerName</span></span>
<span data-ttu-id="d7f80-130">O nome do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="d7f80-130">The name of the route server.</span></span>

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

### <span data-ttu-id="d7f80-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d7f80-131">-Confirm</span></span>
<span data-ttu-id="d7f80-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7f80-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7f80-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7f80-133">-WhatIf</span></span>
<span data-ttu-id="d7f80-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d7f80-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7f80-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7f80-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7f80-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f80-136">CommonParameters</span></span>
<span data-ttu-id="d7f80-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f80-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f80-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7f80-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f80-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="d7f80-139">INPUTS</span></span>

### <span data-ttu-id="d7f80-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d7f80-140">System.String</span></span>

### <span data-ttu-id="d7f80-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="d7f80-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="d7f80-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="d7f80-142">OUTPUTS</span></span>

### <span data-ttu-id="d7f80-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7f80-143">System.Boolean</span></span>

## <span data-ttu-id="d7f80-144">Notas</span><span class="sxs-lookup"><span data-stu-id="d7f80-144">NOTES</span></span>

## <span data-ttu-id="d7f80-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7f80-145">RELATED LINKS</span></span>
