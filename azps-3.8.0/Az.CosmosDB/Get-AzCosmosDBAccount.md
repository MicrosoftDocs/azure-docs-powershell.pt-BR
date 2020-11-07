---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777548"
---
# <span data-ttu-id="de8ea-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="de8ea-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="de8ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="de8ea-103">Obter conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="de8ea-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="de8ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de8ea-104">SYNTAX</span></span>

### <span data-ttu-id="de8ea-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="de8ea-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de8ea-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de8ea-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de8ea-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de8ea-107">DESCRIPTION</span></span>
<span data-ttu-id="de8ea-108">O cmdlet **Get-AzCosmosDBAccount** Obtém a lista de todas as contas existentes do CosmosDB para um determinado ResourceGroupName e obtém uma única conta do CosmosDB para um determinado ResourceGroupName e AccountName.</span><span class="sxs-lookup"><span data-stu-id="de8ea-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="de8ea-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de8ea-109">EXAMPLES</span></span>

### <span data-ttu-id="de8ea-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de8ea-110">Example 1</span></span>
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

<span data-ttu-id="de8ea-111">Obtenha CosmosDB conta de banco de dados com o nome databaseAccountName no resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="de8ea-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="de8ea-112">OS</span><span class="sxs-lookup"><span data-stu-id="de8ea-112">PARAMETERS</span></span>

### <span data-ttu-id="de8ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8ea-113">-DefaultProfile</span></span>
<span data-ttu-id="de8ea-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de8ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de8ea-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="de8ea-115">-Name</span></span>
<span data-ttu-id="de8ea-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="de8ea-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="de8ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de8ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="de8ea-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de8ea-118">Name of resource group.</span></span>

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

### <span data-ttu-id="de8ea-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de8ea-119">-ResourceId</span></span>
<span data-ttu-id="de8ea-120">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="de8ea-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="de8ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8ea-121">CommonParameters</span></span>
<span data-ttu-id="de8ea-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8ea-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de8ea-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8ea-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de8ea-124">INPUTS</span></span>

### <span data-ttu-id="de8ea-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="de8ea-125">None</span></span>

## <span data-ttu-id="de8ea-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de8ea-126">OUTPUTS</span></span>

### <span data-ttu-id="de8ea-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="de8ea-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="de8ea-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de8ea-128">NOTES</span></span>

## <span data-ttu-id="de8ea-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de8ea-129">RELATED LINKS</span></span>
