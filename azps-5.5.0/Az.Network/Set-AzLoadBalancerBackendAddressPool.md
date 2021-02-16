---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113434"
---
# <span data-ttu-id="b7c66-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b7c66-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="b7c66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7c66-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c66-103">Atualiza o pool de back-end em um loadbalancer</span><span class="sxs-lookup"><span data-stu-id="b7c66-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="b7c66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7c66-104">SYNTAX</span></span>

### <span data-ttu-id="b7c66-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7c66-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c66-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7c66-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c66-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7c66-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c66-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7c66-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7c66-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7c66-109">DESCRIPTION</span></span>
<span data-ttu-id="b7c66-110">Atualiza o pool de back-end em um loadbalancer</span><span class="sxs-lookup"><span data-stu-id="b7c66-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="b7c66-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b7c66-111">EXAMPLES</span></span>

### <span data-ttu-id="b7c66-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7c66-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="b7c66-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b7c66-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="b7c66-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b7c66-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="b7c66-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7c66-115">PARAMETERS</span></span>

### <span data-ttu-id="b7c66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c66-116">-DefaultProfile</span></span>
<span data-ttu-id="b7c66-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b7c66-118">-Force</span></span>
<span data-ttu-id="b7c66-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b7c66-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b7c66-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7c66-120">-InputObject</span></span>
<span data-ttu-id="b7c66-121">O pool de endereços back-end para definir</span><span class="sxs-lookup"><span data-stu-id="b7c66-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7c66-122">-LoadBalancer</span></span>
<span data-ttu-id="b7c66-123">O recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b7c66-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="b7c66-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="b7c66-125">Os endereços de back-end.</span><span class="sxs-lookup"><span data-stu-id="b7c66-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="b7c66-126">-LoadBalancerName</span></span>
<span data-ttu-id="b7c66-127">O nome do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b7c66-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7c66-128">-Name</span></span>
<span data-ttu-id="b7c66-129">O nome do pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="b7c66-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7c66-130">-PassThru</span></span>
<span data-ttu-id="b7c66-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b7c66-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b7c66-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c66-132">-ResourceGroupName</span></span>
<span data-ttu-id="b7c66-133">O nome do grupo de recursos do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b7c66-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c66-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b7c66-135">-Confirm</span></span>
<span data-ttu-id="b7c66-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7c66-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c66-137">-WhatIf</span></span>
<span data-ttu-id="b7c66-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b7c66-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c66-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7c66-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c66-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c66-140">CommonParameters</span></span>
<span data-ttu-id="b7c66-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c66-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c66-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7c66-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c66-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="b7c66-143">INPUTS</span></span>

### <span data-ttu-id="b7c66-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7c66-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b7c66-145">System.String</span><span class="sxs-lookup"><span data-stu-id="b7c66-145">System.String</span></span>

## <span data-ttu-id="b7c66-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="b7c66-146">OUTPUTS</span></span>

### <span data-ttu-id="b7c66-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b7c66-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b7c66-148">Notas</span><span class="sxs-lookup"><span data-stu-id="b7c66-148">NOTES</span></span>

## <span data-ttu-id="b7c66-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7c66-149">RELATED LINKS</span></span>
