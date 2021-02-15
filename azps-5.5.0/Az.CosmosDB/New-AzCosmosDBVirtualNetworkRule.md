---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112042"
---
# <span data-ttu-id="51a86-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="51a86-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="51a86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51a86-102">SYNOPSIS</span></span>
<span data-ttu-id="51a86-103">Crie um novo Objeto Do Portal VirtualNetworkRule(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="51a86-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="51a86-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51a86-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51a86-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="51a86-105">DESCRIPTION</span></span>
<span data-ttu-id="51a86-106">Crie um novo Objeto Do Portal VirtualNetworkRule(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="51a86-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="51a86-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="51a86-107">EXAMPLES</span></span>

### <span data-ttu-id="51a86-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51a86-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="51a86-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51a86-109">PARAMETERS</span></span>

### <span data-ttu-id="51a86-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a86-110">-DefaultProfile</span></span>
<span data-ttu-id="51a86-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51a86-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51a86-112">-ID</span><span class="sxs-lookup"><span data-stu-id="51a86-112">-Id</span></span>
<span data-ttu-id="51a86-113">ID de recurso de uma sub-rede, por exemplo: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="51a86-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="51a86-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="51a86-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="51a86-115">Booliano para indicar se você deve criar uma regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço VNET habilitado.</span><span class="sxs-lookup"><span data-stu-id="51a86-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="51a86-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a86-116">CommonParameters</span></span>
<span data-ttu-id="51a86-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a86-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a86-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51a86-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a86-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="51a86-119">INPUTS</span></span>

### <span data-ttu-id="51a86-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="51a86-120">None</span></span>

## <span data-ttu-id="51a86-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="51a86-121">OUTPUTS</span></span>

### <span data-ttu-id="51a86-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="51a86-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="51a86-123">Notas</span><span class="sxs-lookup"><span data-stu-id="51a86-123">NOTES</span></span>

## <span data-ttu-id="51a86-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51a86-124">RELATED LINKS</span></span>
