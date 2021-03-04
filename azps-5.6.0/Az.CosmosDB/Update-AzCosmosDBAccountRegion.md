---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: 643cdbf8aa0aed98dba7497fa0107d8d81583bba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886240"
---
# <span data-ttu-id="707a3-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="707a3-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="707a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="707a3-102">SYNOPSIS</span></span>
<span data-ttu-id="707a3-103">Atualizar regiões de uma conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="707a3-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="707a3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="707a3-104">SYNTAX</span></span>

### <span data-ttu-id="707a3-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="707a3-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="707a3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="707a3-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="707a3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="707a3-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="707a3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="707a3-108">DESCRIPTION</span></span>
<span data-ttu-id="707a3-109">Atualizar regiões de uma conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="707a3-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="707a3-110">O local pode ser fornecido como um objeto do tipo PSLocation ou como cadeias de caracteres de Nome de Local ordenadas por prioridade de failover.</span><span class="sxs-lookup"><span data-stu-id="707a3-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="707a3-111">O parâmetro LocationObject espera que a lista de locais atuais (priorizações de failover incluídas) acrescentada pelos novos LocationObjects correspondentes a novos locais sejam adicionados.</span><span class="sxs-lookup"><span data-stu-id="707a3-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="707a3-112">O parâmetro Location espera a lista de localização atual (ordenada por prioridade de failover) e os novos locais.</span><span class="sxs-lookup"><span data-stu-id="707a3-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="707a3-113">Observe que só suportamos a adição de regiões.</span><span class="sxs-lookup"><span data-stu-id="707a3-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="707a3-114">Forneça Location ou LocationObject.</span><span class="sxs-lookup"><span data-stu-id="707a3-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="707a3-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="707a3-115">EXAMPLES</span></span>

### <span data-ttu-id="707a3-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="707a3-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="707a3-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="707a3-117">PARAMETERS</span></span>

### <span data-ttu-id="707a3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="707a3-118">-AsJob</span></span>
<span data-ttu-id="707a3-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="707a3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="707a3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="707a3-120">-Confirm</span></span>
<span data-ttu-id="707a3-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="707a3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="707a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707a3-122">-DefaultProfile</span></span>
<span data-ttu-id="707a3-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="707a3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="707a3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="707a3-124">-InputObject</span></span>
<span data-ttu-id="707a3-125">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="707a3-125">ResourceId of the resource.</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="707a3-126">-Location</span><span class="sxs-lookup"><span data-stu-id="707a3-126">-Location</span></span>
<span data-ttu-id="707a3-127">Nome do local a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="707a3-127">Name of the location to be added.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707a3-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="707a3-128">-LocationObject</span></span>
<span data-ttu-id="707a3-129">Adicione um local à conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="707a3-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="707a3-130">Matriz de objetos PSLocation.</span><span class="sxs-lookup"><span data-stu-id="707a3-130">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707a3-131">-Name</span><span class="sxs-lookup"><span data-stu-id="707a3-131">-Name</span></span>
<span data-ttu-id="707a3-132">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="707a3-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="707a3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="707a3-133">-ResourceGroupName</span></span>
<span data-ttu-id="707a3-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="707a3-134">Name of resource group.</span></span>

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

### <span data-ttu-id="707a3-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="707a3-135">-ResourceId</span></span>
<span data-ttu-id="707a3-136">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="707a3-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="707a3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="707a3-137">-WhatIf</span></span>
<span data-ttu-id="707a3-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="707a3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="707a3-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="707a3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="707a3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707a3-140">CommonParameters</span></span>
<span data-ttu-id="707a3-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="707a3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707a3-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="707a3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707a3-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="707a3-143">INPUTS</span></span>

### <span data-ttu-id="707a3-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="707a3-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="707a3-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="707a3-145">OUTPUTS</span></span>

### <span data-ttu-id="707a3-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="707a3-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="707a3-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="707a3-147">NOTES</span></span>

## <span data-ttu-id="707a3-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="707a3-148">RELATED LINKS</span></span>
