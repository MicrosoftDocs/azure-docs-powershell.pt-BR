---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112879"
---
# <span data-ttu-id="88ec7-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="88ec7-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="88ec7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="88ec7-103">Obter conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="88ec7-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="88ec7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88ec7-104">SYNTAX</span></span>

### <span data-ttu-id="88ec7-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="88ec7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88ec7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ec7-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88ec7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88ec7-107">DESCRIPTION</span></span>
<span data-ttu-id="88ec7-108">O cmdlet **Get-AzCosmosDBAccount** Obtém a lista de todas as contas existentes do CosmosDB para um determinado ResourceGroupName e obtém uma única conta do CosmosDB para um determinado ResourceGroupName e AccountName.</span><span class="sxs-lookup"><span data-stu-id="88ec7-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="88ec7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88ec7-109">EXAMPLES</span></span>

### <span data-ttu-id="88ec7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88ec7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
```

<span data-ttu-id="88ec7-111">Obtenha CosmosDB conta de banco de dados com o nome databaseAccountName no resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="88ec7-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="88ec7-112">OS</span><span class="sxs-lookup"><span data-stu-id="88ec7-112">PARAMETERS</span></span>

### <span data-ttu-id="88ec7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ec7-113">-DefaultProfile</span></span>
<span data-ttu-id="88ec7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88ec7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88ec7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="88ec7-115">-Name</span></span>
<span data-ttu-id="88ec7-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="88ec7-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ec7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ec7-117">-ResourceGroupName</span></span>
<span data-ttu-id="88ec7-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="88ec7-118">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ec7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88ec7-119">-ResourceId</span></span>
<span data-ttu-id="88ec7-120">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="88ec7-120">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ec7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ec7-121">CommonParameters</span></span>
<span data-ttu-id="88ec7-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ec7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ec7-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88ec7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ec7-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88ec7-124">INPUTS</span></span>

### <span data-ttu-id="88ec7-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="88ec7-125">None</span></span>

## <span data-ttu-id="88ec7-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88ec7-126">OUTPUTS</span></span>

### <span data-ttu-id="88ec7-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="88ec7-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="88ec7-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88ec7-128">NOTES</span></span>

## <span data-ttu-id="88ec7-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88ec7-129">RELATED LINKS</span></span>
