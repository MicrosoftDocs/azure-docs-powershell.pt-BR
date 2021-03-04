---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
ms.openlocfilehash: 24e53b7f7bfd0f09e93184b2862deed4608af544
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886160"
---
# <span data-ttu-id="595f0-101">New-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="595f0-101">New-AzRouteServer</span></span>

## <span data-ttu-id="595f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="595f0-102">SYNOPSIS</span></span>
<span data-ttu-id="595f0-103">Cria um RouteServer do Azure.</span><span class="sxs-lookup"><span data-stu-id="595f0-103">Creates an Azure RouteServer.</span></span>

## <span data-ttu-id="595f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="595f0-104">SYNTAX</span></span>

```
New-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> -HostedSubnet <String>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="595f0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="595f0-105">DESCRIPTION</span></span>
<span data-ttu-id="595f0-106">O cmdlet **New-AzRouteServer** cria um RouteServer do Azure</span><span class="sxs-lookup"><span data-stu-id="595f0-106">The **New-AzRouteServer** cmdlet creates an Azure RouteServer</span></span>

## <span data-ttu-id="595f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="595f0-107">EXAMPLES</span></span>

### <span data-ttu-id="595f0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="595f0-108">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzRouteServer -RouteServerName $routeServerName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="595f0-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="595f0-109">PARAMETERS</span></span>

### <span data-ttu-id="595f0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="595f0-110">-AsJob</span></span>
<span data-ttu-id="595f0-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="595f0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="595f0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595f0-112">-DefaultProfile</span></span>
<span data-ttu-id="595f0-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="595f0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="595f0-114">-Force</span><span class="sxs-lookup"><span data-stu-id="595f0-114">-Force</span></span>
<span data-ttu-id="595f0-115">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="595f0-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="595f0-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="595f0-116">-HostedSubnet</span></span>
<span data-ttu-id="595f0-117">A sub-rede onde o servidor de rota está hospedado.</span><span class="sxs-lookup"><span data-stu-id="595f0-117">The subnet where the route server is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595f0-118">-Location</span><span class="sxs-lookup"><span data-stu-id="595f0-118">-Location</span></span>
<span data-ttu-id="595f0-119">O local.</span><span class="sxs-lookup"><span data-stu-id="595f0-119">The location.</span></span>

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

### <span data-ttu-id="595f0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595f0-120">-ResourceGroupName</span></span>
<span data-ttu-id="595f0-121">O nome do grupo de recursos do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="595f0-121">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="595f0-122">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="595f0-122">-RouteServerName</span></span>
<span data-ttu-id="595f0-123">O nome do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="595f0-123">The name of the route server.</span></span>

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

### <span data-ttu-id="595f0-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="595f0-124">-Tag</span></span>
<span data-ttu-id="595f0-125">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="595f0-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595f0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="595f0-126">-Confirm</span></span>
<span data-ttu-id="595f0-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="595f0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="595f0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="595f0-128">-WhatIf</span></span>
<span data-ttu-id="595f0-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="595f0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="595f0-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="595f0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="595f0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595f0-131">CommonParameters</span></span>
<span data-ttu-id="595f0-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="595f0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595f0-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="595f0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595f0-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="595f0-134">INPUTS</span></span>

### <span data-ttu-id="595f0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="595f0-135">System.String</span></span>

### <span data-ttu-id="595f0-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="595f0-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="595f0-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="595f0-137">OUTPUTS</span></span>

### <span data-ttu-id="595f0-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="595f0-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="595f0-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="595f0-139">NOTES</span></span>

## <span data-ttu-id="595f0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="595f0-140">RELATED LINKS</span></span>
