---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 9f00ccfb01cd6e6b0d80b120364f8ac0c81daae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112749"
---
# <span data-ttu-id="bee35-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="bee35-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="bee35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bee35-102">SYNOPSIS</span></span>
<span data-ttu-id="bee35-103">Atualizar um Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="bee35-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="bee35-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bee35-104">SYNTAX</span></span>

### <span data-ttu-id="bee35-105">RouteServerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bee35-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bee35-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bee35-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bee35-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bee35-107">DESCRIPTION</span></span>
<span data-ttu-id="bee35-108">O cmdlet **Update-AzRouteServer** alterna o tráfego de ramificação para ramificação para um Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="bee35-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="bee35-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bee35-109">EXAMPLES</span></span>

### <span data-ttu-id="bee35-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bee35-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="bee35-111">Para habilitar o branch para ramificar o tráfego para o servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="bee35-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="bee35-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bee35-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="bee35-113">Para desabilitar a ramificação para o tráfego de ramificação para o servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="bee35-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="bee35-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bee35-114">PARAMETERS</span></span>

### <span data-ttu-id="bee35-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="bee35-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="bee35-116">Sinalizar para permitir a ramificação do tráfego para o servidor de roteamento.</span><span class="sxs-lookup"><span data-stu-id="bee35-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="bee35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee35-117">-DefaultProfile</span></span>
<span data-ttu-id="bee35-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bee35-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bee35-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee35-119">-ResourceGroupName</span></span>
<span data-ttu-id="bee35-120">O nome do grupo de recursos do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="bee35-120">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="bee35-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bee35-121">-ResourceId</span></span>
<span data-ttu-id="bee35-122">ResourceId do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="bee35-122">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="bee35-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="bee35-123">-RouteServerName</span></span>
<span data-ttu-id="bee35-124">O nome do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="bee35-124">The name of the route server.</span></span>

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

### <span data-ttu-id="bee35-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bee35-125">-Confirm</span></span>
<span data-ttu-id="bee35-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee35-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bee35-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee35-127">-WhatIf</span></span>
<span data-ttu-id="bee35-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bee35-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee35-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bee35-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bee35-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee35-130">CommonParameters</span></span>
<span data-ttu-id="bee35-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee35-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee35-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bee35-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee35-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="bee35-133">INPUTS</span></span>

### <span data-ttu-id="bee35-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bee35-134">System.String</span></span>

## <span data-ttu-id="bee35-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="bee35-135">OUTPUTS</span></span>

### <span data-ttu-id="bee35-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="bee35-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="bee35-137">Notas</span><span class="sxs-lookup"><span data-stu-id="bee35-137">NOTES</span></span>

## <span data-ttu-id="bee35-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bee35-138">RELATED LINKS</span></span>
