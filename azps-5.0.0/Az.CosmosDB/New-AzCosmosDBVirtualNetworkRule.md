---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281280"
---
# <span data-ttu-id="6683e-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6683e-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="6683e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6683e-102">SYNOPSIS</span></span>
<span data-ttu-id="6683e-103">Crie um novo objeto CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="6683e-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="6683e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6683e-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6683e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6683e-105">DESCRIPTION</span></span>
<span data-ttu-id="6683e-106">Crie um novo objeto CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="6683e-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="6683e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6683e-107">EXAMPLES</span></span>

### <span data-ttu-id="6683e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6683e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="6683e-109">OS</span><span class="sxs-lookup"><span data-stu-id="6683e-109">PARAMETERS</span></span>

### <span data-ttu-id="6683e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6683e-110">-DefaultProfile</span></span>
<span data-ttu-id="6683e-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6683e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6683e-112">-ID</span><span class="sxs-lookup"><span data-stu-id="6683e-112">-Id</span></span>
<span data-ttu-id="6683e-113">ID do recurso de uma sub-rede, por exemplo:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="6683e-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="6683e-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6683e-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="6683e-115">Booliano para indicar se criar uma regra de firewall antes da rede virtual ter ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="6683e-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="6683e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6683e-116">CommonParameters</span></span>
<span data-ttu-id="6683e-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6683e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6683e-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6683e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6683e-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6683e-119">INPUTS</span></span>

### <span data-ttu-id="6683e-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6683e-120">None</span></span>

## <span data-ttu-id="6683e-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6683e-121">OUTPUTS</span></span>

### <span data-ttu-id="6683e-122">Microsoft. Azure. Commands. CosmosDB. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6683e-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="6683e-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6683e-123">NOTES</span></span>

## <span data-ttu-id="6683e-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6683e-124">RELATED LINKS</span></span>
