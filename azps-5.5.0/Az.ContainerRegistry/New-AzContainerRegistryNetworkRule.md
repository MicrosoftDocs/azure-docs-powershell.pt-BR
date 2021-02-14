---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115942"
---
# <span data-ttu-id="e3e45-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3e45-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="e3e45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3e45-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e45-103">Criar uma regra de rede.</span><span class="sxs-lookup"><span data-stu-id="e3e45-103">Create a network rule.</span></span>

## <span data-ttu-id="e3e45-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3e45-104">SYNTAX</span></span>

### <span data-ttu-id="e3e45-105">ByVirtualNetworkRule (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e3e45-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3e45-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="e3e45-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3e45-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3e45-107">DESCRIPTION</span></span>
<span data-ttu-id="e3e45-108">Criar um objeto de regra de rede na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e3e45-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="e3e45-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3e45-109">EXAMPLES</span></span>

### <span data-ttu-id="e3e45-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3e45-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="e3e45-111">Criar conjunto de regras de virtualnetwork.</span><span class="sxs-lookup"><span data-stu-id="e3e45-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="e3e45-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3e45-112">PARAMETERS</span></span>

### <span data-ttu-id="e3e45-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="e3e45-113">-Action</span></span>
<span data-ttu-id="e3e45-114">A ação da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="e3e45-114">The action of network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e45-115">-DefaultProfile</span></span>
<span data-ttu-id="e3e45-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3e45-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3e45-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e3e45-117">-IPAddressOrRange</span></span>
<span data-ttu-id="e3e45-118">Especifica o intervalo IP ou IP no formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="e3e45-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="e3e45-119">Somente endereço IPV4 é permitido.</span><span class="sxs-lookup"><span data-stu-id="e3e45-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e45-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="e3e45-120">-IPRule</span></span>
<span data-ttu-id="e3e45-121">Indicar para criar IPRule.</span><span class="sxs-lookup"><span data-stu-id="e3e45-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e45-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e45-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e3e45-123">ID de recurso de uma sub-rede, por exemplo: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="e3e45-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e45-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3e45-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="e3e45-125">Indique para criar o VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="e3e45-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e45-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e45-126">CommonParameters</span></span>
<span data-ttu-id="e3e45-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3e45-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e45-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3e45-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e45-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="e3e45-129">INPUTS</span></span>

### <span data-ttu-id="e3e45-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e3e45-130">System.String</span></span>

## <span data-ttu-id="e3e45-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="e3e45-131">OUTPUTS</span></span>

### <span data-ttu-id="e3e45-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3e45-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="e3e45-133">Notas</span><span class="sxs-lookup"><span data-stu-id="e3e45-133">NOTES</span></span>

## <span data-ttu-id="e3e45-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3e45-134">RELATED LINKS</span></span>
