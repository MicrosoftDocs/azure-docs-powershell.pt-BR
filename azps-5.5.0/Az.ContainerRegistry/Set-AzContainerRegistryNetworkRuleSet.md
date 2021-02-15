---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112080"
---
# <span data-ttu-id="73312-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73312-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="73312-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73312-102">SYNOPSIS</span></span>
<span data-ttu-id="73312-103">Criar ou atualizar um conjunto de regras de rede.</span><span class="sxs-lookup"><span data-stu-id="73312-103">Create or update a network rule set.</span></span> <span data-ttu-id="73312-104">O conjunto de regras só pode ser aplicado ao registro "Premium".</span><span class="sxs-lookup"><span data-stu-id="73312-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="73312-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73312-105">SYNTAX</span></span>

### <span data-ttu-id="73312-106">AddAddNetworkRuleWithoutInputObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="73312-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73312-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="73312-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73312-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="73312-108">DESCRIPTION</span></span>
<span data-ttu-id="73312-109">Criar ou atualizar um conjunto de regras de rede</span><span class="sxs-lookup"><span data-stu-id="73312-109">Create or update a network rule set</span></span>

## <span data-ttu-id="73312-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73312-110">EXAMPLES</span></span>

### <span data-ttu-id="73312-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73312-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="73312-112">Criar um novo conjunto de regras de rede.</span><span class="sxs-lookup"><span data-stu-id="73312-112">Create a new network rule set.</span></span>

## <span data-ttu-id="73312-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73312-113">PARAMETERS</span></span>

### <span data-ttu-id="73312-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="73312-114">-DefaultAction</span></span>
<span data-ttu-id="73312-115">Ação padrão, pode ser "Permitir" ou "Negar"</span><span class="sxs-lookup"><span data-stu-id="73312-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73312-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73312-116">-DefaultProfile</span></span>
<span data-ttu-id="73312-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73312-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73312-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73312-118">-InputObject</span></span>
<span data-ttu-id="73312-119">Entrada PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73312-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73312-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="73312-120">-NetworkRule</span></span>
<span data-ttu-id="73312-121">Lista de regras de rede</span><span class="sxs-lookup"><span data-stu-id="73312-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73312-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73312-122">CommonParameters</span></span>
<span data-ttu-id="73312-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73312-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73312-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73312-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73312-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="73312-125">INPUTS</span></span>

### <span data-ttu-id="73312-126">System.String</span><span class="sxs-lookup"><span data-stu-id="73312-126">System.String</span></span>

### <span data-ttu-id="73312-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="73312-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="73312-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="73312-128">OUTPUTS</span></span>

### <span data-ttu-id="73312-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73312-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="73312-130">Notas</span><span class="sxs-lookup"><span data-stu-id="73312-130">NOTES</span></span>

## <span data-ttu-id="73312-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73312-131">RELATED LINKS</span></span>
