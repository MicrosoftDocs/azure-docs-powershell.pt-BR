---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943628"
---
# <span data-ttu-id="2fb1f-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2fb1f-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="2fb1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2fb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb1f-103">Crie um novo objeto CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="2fb1f-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="2fb1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fb1f-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fb1f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2fb1f-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb1f-106">Crie um novo objeto CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="2fb1f-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="2fb1f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fb1f-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb1f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2fb1f-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="2fb1f-109">OS</span><span class="sxs-lookup"><span data-stu-id="2fb1f-109">PARAMETERS</span></span>

### <span data-ttu-id="2fb1f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb1f-110">-DefaultProfile</span></span>
<span data-ttu-id="2fb1f-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2fb1f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fb1f-112">-ID</span><span class="sxs-lookup"><span data-stu-id="2fb1f-112">-Id</span></span>
<span data-ttu-id="2fb1f-113">ID do recurso de uma sub-rede, por exemplo:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="2fb1f-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="2fb1f-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2fb1f-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="2fb1f-115">Booliano para indicar se criar uma regra de firewall antes da rede virtual ter ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="2fb1f-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="2fb1f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb1f-116">CommonParameters</span></span>
<span data-ttu-id="2fb1f-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb1f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb1f-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fb1f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb1f-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2fb1f-119">INPUTS</span></span>

### <span data-ttu-id="2fb1f-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2fb1f-120">None</span></span>

## <span data-ttu-id="2fb1f-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2fb1f-121">OUTPUTS</span></span>

### <span data-ttu-id="2fb1f-122">Microsoft. Azure. Commands. CosmosDB. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2fb1f-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="2fb1f-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2fb1f-123">NOTES</span></span>

## <span data-ttu-id="2fb1f-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fb1f-124">RELATED LINKS</span></span>
