---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: abc97b0473353a0bc71aae59386bc5b5770b730b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888985"
---
# <span data-ttu-id="658aa-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="658aa-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="658aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="658aa-102">SYNOPSIS</span></span>
<span data-ttu-id="658aa-103">Crie um novo objeto VirtualNetworkRule do CosmosDB(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="658aa-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="658aa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="658aa-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="658aa-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="658aa-105">DESCRIPTION</span></span>
<span data-ttu-id="658aa-106">Crie um novo objeto VirtualNetworkRule do CosmosDB(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="658aa-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="658aa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="658aa-107">EXAMPLES</span></span>

### <span data-ttu-id="658aa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="658aa-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="658aa-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="658aa-109">PARAMETERS</span></span>

### <span data-ttu-id="658aa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658aa-110">-DefaultProfile</span></span>
<span data-ttu-id="658aa-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="658aa-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="658aa-112">-Id</span><span class="sxs-lookup"><span data-stu-id="658aa-112">-Id</span></span>
<span data-ttu-id="658aa-113">ID de recurso de uma sub-rede, por exemplo: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="658aa-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658aa-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="658aa-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="658aa-115">Boolean para indicar se é necessário criar uma regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="658aa-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658aa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658aa-116">CommonParameters</span></span>
<span data-ttu-id="658aa-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="658aa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658aa-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="658aa-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658aa-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="658aa-119">INPUTS</span></span>

### <span data-ttu-id="658aa-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="658aa-120">None</span></span>

## <span data-ttu-id="658aa-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="658aa-121">OUTPUTS</span></span>

### <span data-ttu-id="658aa-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="658aa-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="658aa-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="658aa-123">NOTES</span></span>

## <span data-ttu-id="658aa-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="658aa-124">RELATED LINKS</span></span>
