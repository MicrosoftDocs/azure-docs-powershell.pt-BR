---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 76df37703882e799eb42542cd08d105f62787419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942565"
---
# <span data-ttu-id="66fd0-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="66fd0-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="66fd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="66fd0-103">Crie uma nova conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="66fd0-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="66fd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66fd0-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork] [-IpRangeFilter <String[]>]
 [-Location <String[]>] [-LocationObject <PSLocation[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-ApiKind <String>] [-PublicNetworkAccess <String>]
 [-DisableKeyBasedMetadataWriteAccess] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66fd0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="66fd0-106">Crie uma nova conta do CosmosDB em um determinado.</span><span class="sxs-lookup"><span data-stu-id="66fd0-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="66fd0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66fd0-107">EXAMPLES</span></span>

### <span data-ttu-id="66fd0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66fd0-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="66fd0-109">Uma nova conta do CosmosDB com o nome databaseAccountName é criada no resourceGroupName do.</span><span class="sxs-lookup"><span data-stu-id="66fd0-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="66fd0-110">OS</span><span class="sxs-lookup"><span data-stu-id="66fd0-110">PARAMETERS</span></span>

### <span data-ttu-id="66fd0-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="66fd0-111">-ApiKind</span></span>
<span data-ttu-id="66fd0-112">O tipo de conta de banco de dados de banco de dados do cosmos a ser criado.</span><span class="sxs-lookup"><span data-stu-id="66fd0-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="66fd0-113">Valores aceitos: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="66fd0-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="66fd0-114">Valor padrão: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="66fd0-114">Default value: GlobalDocumentDB</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fd0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66fd0-115">-AsJob</span></span>
<span data-ttu-id="66fd0-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="66fd0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66fd0-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66fd0-117">-Confirm</span></span>
<span data-ttu-id="66fd0-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66fd0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66fd0-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="66fd0-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="66fd0-120">Nível de consistência padrão da conta de banco de dados do banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="66fd0-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="66fd0-121">Valores aceitos: BoundedStaleness, ConsistentPrefix, eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="66fd0-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fd0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fd0-122">-DefaultProfile</span></span>
<span data-ttu-id="66fd0-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66fd0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66fd0-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="66fd0-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="66fd0-125">Desabilitar operações de gravação em recursos de metadados (bancos de dados, contêineres, produtividade) via chaves de conta</span><span class="sxs-lookup"><span data-stu-id="66fd0-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="66fd0-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="66fd0-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="66fd0-127">Habilita o failover automático da região de gravação no evento raro que a região não está disponível devido a uma interrupção.</span><span class="sxs-lookup"><span data-stu-id="66fd0-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="66fd0-128">O failover automático fará uma nova região de gravação para a conta e será escolhido com base nas prioridades de failover configuradas para a conta.</span><span class="sxs-lookup"><span data-stu-id="66fd0-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="66fd0-129">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="66fd0-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="66fd0-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="66fd0-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="66fd0-131">Habilite vários locais de gravação.</span><span class="sxs-lookup"><span data-stu-id="66fd0-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="66fd0-132">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="66fd0-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="66fd0-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="66fd0-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="66fd0-134">Habilita a rede virtual na conta de banco de dados do cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="66fd0-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="66fd0-135">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="66fd0-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="66fd0-136">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="66fd0-136">-IpRangeFilter</span></span>
<span data-ttu-id="66fd0-137">Suporte a firewall.</span><span class="sxs-lookup"><span data-stu-id="66fd0-137">Firewall support.</span></span>
<span data-ttu-id="66fd0-138">Especifica o conjunto de endereços IP ou intervalos de endereços IP no formato CIDR a ser incluído como a lista permitida de IPs de cliente para uma determinada conta de banco de dados</span><span class="sxs-lookup"><span data-stu-id="66fd0-138">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="66fd0-139">-Local</span><span class="sxs-lookup"><span data-stu-id="66fd0-139">-Location</span></span>
<span data-ttu-id="66fd0-140">Adicione um local para a conta de banco de dados do cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="66fd0-140">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="66fd0-141">Matriz de cadeia de caracteres, ordenada pela prioridade de failover.</span><span class="sxs-lookup"><span data-stu-id="66fd0-141">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="66fd0-142">-Locationobject</span><span class="sxs-lookup"><span data-stu-id="66fd0-142">-LocationObject</span></span>
<span data-ttu-id="66fd0-143">Adicione um local para a conta de banco de dados do cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="66fd0-143">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="66fd0-144">Matriz de objetos PSLocation.</span><span class="sxs-lookup"><span data-stu-id="66fd0-144">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="66fd0-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="66fd0-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="66fd0-146">Quando usado com consistência de ultrapassabilidade limitada, esse valor representa a quantidade de tempo de desvaloração (em TimeSpan) tolerada.</span><span class="sxs-lookup"><span data-stu-id="66fd0-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="66fd0-147">O intervalo aceito para esse valor é 5-86400.</span><span class="sxs-lookup"><span data-stu-id="66fd0-147">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fd0-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="66fd0-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="66fd0-149">Quando usado com consistência de ultrapassabilidade limitada, esse valor representa o número de solicitações obsoletas toleradas.</span><span class="sxs-lookup"><span data-stu-id="66fd0-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="66fd0-150">O intervalo aceito para esse valor é de 1 a 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="66fd0-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fd0-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="66fd0-151">-Name</span></span>
<span data-ttu-id="66fd0-152">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="66fd0-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="66fd0-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="66fd0-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="66fd0-154">Se o acesso de ponto de extremidade público ou não é permitido para este servidor.</span><span class="sxs-lookup"><span data-stu-id="66fd0-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="66fd0-155">Os valores possíveis incluem: ' Enabled ', ' disabled '</span><span class="sxs-lookup"><span data-stu-id="66fd0-155">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fd0-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66fd0-156">-ResourceGroupName</span></span>
<span data-ttu-id="66fd0-157">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66fd0-157">Name of resource group.</span></span>

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

### <span data-ttu-id="66fd0-158">-Marca</span><span class="sxs-lookup"><span data-stu-id="66fd0-158">-Tag</span></span>
<span data-ttu-id="66fd0-159">Hashtable de marcas como pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="66fd0-159">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="66fd0-160">Use uma cadeia de caracteres vazia para limpar a marca existente.</span><span class="sxs-lookup"><span data-stu-id="66fd0-160">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fd0-161">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="66fd0-161">-VirtualNetworkRule</span></span>
<span data-ttu-id="66fd0-162">Matriz de valores de cadeia de caracteres de ACL para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="66fd0-162">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="66fd0-163">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="66fd0-163">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="66fd0-164">Matriz de PSVirtualNetworkRuleObjects para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="66fd0-164">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fd0-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66fd0-165">-WhatIf</span></span>
<span data-ttu-id="66fd0-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66fd0-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66fd0-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66fd0-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66fd0-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fd0-168">CommonParameters</span></span>
<span data-ttu-id="66fd0-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fd0-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fd0-170">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66fd0-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fd0-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66fd0-171">INPUTS</span></span>

### <span data-ttu-id="66fd0-172">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="66fd0-172">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="66fd0-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66fd0-173">OUTPUTS</span></span>

### <span data-ttu-id="66fd0-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="66fd0-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="66fd0-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66fd0-175">NOTES</span></span>

## <span data-ttu-id="66fd0-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66fd0-176">RELATED LINKS</span></span>
