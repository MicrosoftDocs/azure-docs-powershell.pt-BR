---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111023"
---
# <span data-ttu-id="c537e-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="c537e-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="c537e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c537e-102">SYNOPSIS</span></span>
<span data-ttu-id="c537e-103">Atualizar Regiões de uma Conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c537e-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="c537e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c537e-104">SYNTAX</span></span>

### <span data-ttu-id="c537e-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c537e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c537e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c537e-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c537e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c537e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c537e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c537e-108">DESCRIPTION</span></span>
<span data-ttu-id="c537e-109">Atualizar Regiões de uma Conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c537e-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="c537e-110">O local pode ser fornecido como um objeto do tipo PSLocation ou como cadeias de caracteres de Nome de Local ordenadas por prioridade de failover.</span><span class="sxs-lookup"><span data-stu-id="c537e-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="c537e-111">O parâmetro LocationObject espera que a lista de locais atuais (priorícios de failover incluídos) acrescentada pelos novos LocationObjects correspondentes a novos locais sejam adicionados.</span><span class="sxs-lookup"><span data-stu-id="c537e-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="c537e-112">O parâmetro de localização espera a lista de localização atual (ordenada por prioridade de failover) e os novos locais.</span><span class="sxs-lookup"><span data-stu-id="c537e-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="c537e-113">Observe que só damos suporte à Adição de Regiões.</span><span class="sxs-lookup"><span data-stu-id="c537e-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="c537e-114">Forneça Local ou LocalObject.</span><span class="sxs-lookup"><span data-stu-id="c537e-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="c537e-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c537e-115">EXAMPLES</span></span>

### <span data-ttu-id="c537e-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c537e-116">Example 1</span></span>
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

## <span data-ttu-id="c537e-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c537e-117">PARAMETERS</span></span>

### <span data-ttu-id="c537e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c537e-118">-AsJob</span></span>
<span data-ttu-id="c537e-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c537e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c537e-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c537e-120">-Confirm</span></span>
<span data-ttu-id="c537e-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c537e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c537e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c537e-122">-DefaultProfile</span></span>
<span data-ttu-id="c537e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c537e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c537e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c537e-124">-InputObject</span></span>
<span data-ttu-id="c537e-125">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="c537e-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="c537e-126">-Local</span><span class="sxs-lookup"><span data-stu-id="c537e-126">-Location</span></span>
<span data-ttu-id="c537e-127">Nome do local a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="c537e-127">Name of the location to be added.</span></span>

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

### <span data-ttu-id="c537e-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="c537e-128">-LocationObject</span></span>
<span data-ttu-id="c537e-129">Adicione um local à conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="c537e-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="c537e-130">Matriz de objetos PSLocation.</span><span class="sxs-lookup"><span data-stu-id="c537e-130">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="c537e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="c537e-131">-Name</span></span>
<span data-ttu-id="c537e-132">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="c537e-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c537e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c537e-133">-ResourceGroupName</span></span>
<span data-ttu-id="c537e-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c537e-134">Name of resource group.</span></span>

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

### <span data-ttu-id="c537e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c537e-135">-ResourceId</span></span>
<span data-ttu-id="c537e-136">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="c537e-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="c537e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c537e-137">-WhatIf</span></span>
<span data-ttu-id="c537e-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c537e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c537e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c537e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c537e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c537e-140">CommonParameters</span></span>
<span data-ttu-id="c537e-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c537e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c537e-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c537e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c537e-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="c537e-143">INPUTS</span></span>

### <span data-ttu-id="c537e-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c537e-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c537e-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="c537e-145">OUTPUTS</span></span>

### <span data-ttu-id="c537e-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c537e-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c537e-147">Notas</span><span class="sxs-lookup"><span data-stu-id="c537e-147">NOTES</span></span>

## <span data-ttu-id="c537e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c537e-148">RELATED LINKS</span></span>
