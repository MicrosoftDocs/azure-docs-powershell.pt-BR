---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262310"
---
# <span data-ttu-id="13d3a-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="13d3a-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="13d3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="13d3a-103">Criar uma regra de rede.</span><span class="sxs-lookup"><span data-stu-id="13d3a-103">Create a network rule.</span></span>

## <span data-ttu-id="13d3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13d3a-104">SYNTAX</span></span>

### <span data-ttu-id="13d3a-105">ByVirtualNetworkRule (padrão)</span><span class="sxs-lookup"><span data-stu-id="13d3a-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d3a-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="13d3a-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13d3a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13d3a-107">DESCRIPTION</span></span>
<span data-ttu-id="13d3a-108">Criar um objeto de regra de rede na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13d3a-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="13d3a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13d3a-109">EXAMPLES</span></span>

### <span data-ttu-id="13d3a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13d3a-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="13d3a-111">Criar conjunto de regras de VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="13d3a-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="13d3a-112">OS</span><span class="sxs-lookup"><span data-stu-id="13d3a-112">PARAMETERS</span></span>

### <span data-ttu-id="13d3a-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="13d3a-113">-Action</span></span>
<span data-ttu-id="13d3a-114">A ação da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="13d3a-114">The action of network rule.</span></span>

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

### <span data-ttu-id="13d3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d3a-115">-DefaultProfile</span></span>
<span data-ttu-id="13d3a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13d3a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d3a-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="13d3a-117">-IPAddressOrRange</span></span>
<span data-ttu-id="13d3a-118">Especifica o intervalo IP ou IP no formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="13d3a-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="13d3a-119">Somente o endereço IPV4 é permitido.</span><span class="sxs-lookup"><span data-stu-id="13d3a-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="13d3a-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="13d3a-120">-IPRule</span></span>
<span data-ttu-id="13d3a-121">Indique para criar IPRule.</span><span class="sxs-lookup"><span data-stu-id="13d3a-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="13d3a-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="13d3a-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="13d3a-123">ID do recurso de uma sub-rede, por exemplo:/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="13d3a-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="13d3a-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="13d3a-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="13d3a-125">Indique para criar VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="13d3a-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="13d3a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d3a-126">CommonParameters</span></span>
<span data-ttu-id="13d3a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13d3a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d3a-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13d3a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d3a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13d3a-129">INPUTS</span></span>

### <span data-ttu-id="13d3a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="13d3a-130">System.String</span></span>

## <span data-ttu-id="13d3a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13d3a-131">OUTPUTS</span></span>

### <span data-ttu-id="13d3a-132">Microsoft. Azure. Commands. ContainerRegistry. Models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="13d3a-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="13d3a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13d3a-133">NOTES</span></span>

## <span data-ttu-id="13d3a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13d3a-134">RELATED LINKS</span></span>
