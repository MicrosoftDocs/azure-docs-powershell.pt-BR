---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: f082f9390dd5a00fa5984aa2e0df26e8c3b63636
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281345"
---
# <span data-ttu-id="b71a6-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b71a6-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b71a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b71a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b71a6-103">Crie uma nova conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b71a6-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="b71a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b71a6-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b71a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b71a6-105">DESCRIPTION</span></span>
<span data-ttu-id="b71a6-106">Crie uma nova conta do CosmosDB em um determinado.</span><span class="sxs-lookup"><span data-stu-id="b71a6-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="b71a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b71a6-107">EXAMPLES</span></span>

### <span data-ttu-id="b71a6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b71a6-108">Example 1</span></span>
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

<span data-ttu-id="b71a6-109">Uma nova conta do CosmosDB com o nome databaseAccountName é criada no resourceGroupName do.</span><span class="sxs-lookup"><span data-stu-id="b71a6-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="b71a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="b71a6-110">PARAMETERS</span></span>

### <span data-ttu-id="b71a6-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="b71a6-111">-ApiKind</span></span>
<span data-ttu-id="b71a6-112">O tipo de conta de banco de dados de banco de dados do cosmos a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b71a6-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="b71a6-113">Valores aceitos: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="b71a6-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="b71a6-114">Valor padrão: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="b71a6-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="b71a6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b71a6-115">-AsJob</span></span>
<span data-ttu-id="b71a6-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b71a6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b71a6-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b71a6-117">-Confirm</span></span>
<span data-ttu-id="b71a6-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b71a6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b71a6-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="b71a6-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="b71a6-120">Nível de consistência padrão da conta de banco de dados do banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="b71a6-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="b71a6-121">Valores aceitos: BoundedStaleness, ConsistentPrefix, eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="b71a6-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="b71a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71a6-122">-DefaultProfile</span></span>
<span data-ttu-id="b71a6-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b71a6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b71a6-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="b71a6-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="b71a6-125">Desabilitar operações de gravação em recursos de metadados (bancos de dados, contêineres, produtividade) via chaves de conta</span><span class="sxs-lookup"><span data-stu-id="b71a6-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="b71a6-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="b71a6-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="b71a6-127">Bool para indicar se o AnalyticalStorage está habilitado na conta.</span><span class="sxs-lookup"><span data-stu-id="b71a6-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="b71a6-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="b71a6-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="b71a6-129">Habilita o failover automático da região de gravação no evento raro que a região não está disponível devido a uma interrupção.</span><span class="sxs-lookup"><span data-stu-id="b71a6-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="b71a6-130">O failover automático fará uma nova região de gravação para a conta e será escolhido com base nas prioridades de failover configuradas para a conta.</span><span class="sxs-lookup"><span data-stu-id="b71a6-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="b71a6-131">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="b71a6-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b71a6-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="b71a6-132">-EnableFreeTier</span></span>
<span data-ttu-id="b71a6-133">Bool para indicar se o FreeTier está habilitado na conta.</span><span class="sxs-lookup"><span data-stu-id="b71a6-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="b71a6-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="b71a6-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="b71a6-135">Habilite vários locais de gravação.</span><span class="sxs-lookup"><span data-stu-id="b71a6-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="b71a6-136">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="b71a6-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b71a6-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b71a6-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="b71a6-138">Habilita a rede virtual na conta de banco de dados do cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b71a6-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="b71a6-139">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="b71a6-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b71a6-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="b71a6-140">-IpRule</span></span>
<span data-ttu-id="b71a6-141">Suporte a firewall.</span><span class="sxs-lookup"><span data-stu-id="b71a6-141">Firewall support.</span></span> <span data-ttu-id="b71a6-142">Especifica o conjunto de endereços IP ou intervalos de endereços IP no formato CIDR a ser incluído como a lista permitida de IPs de cliente para uma determinada conta de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b71a6-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="b71a6-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="b71a6-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="b71a6-144">URI do cofre</span><span class="sxs-lookup"><span data-stu-id="b71a6-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="b71a6-145">-Local</span><span class="sxs-lookup"><span data-stu-id="b71a6-145">-Location</span></span>
<span data-ttu-id="b71a6-146">Adicione um local para a conta de banco de dados do cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b71a6-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="b71a6-147">Matriz de cadeia de caracteres, ordenada pela prioridade de failover.</span><span class="sxs-lookup"><span data-stu-id="b71a6-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="b71a6-148">-Locationobject</span><span class="sxs-lookup"><span data-stu-id="b71a6-148">-LocationObject</span></span>
<span data-ttu-id="b71a6-149">Adicione um local para a conta de banco de dados do cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b71a6-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="b71a6-150">Matriz de objetos PSLocation.</span><span class="sxs-lookup"><span data-stu-id="b71a6-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="b71a6-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b71a6-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="b71a6-152">Quando usado com consistência de ultrapassabilidade limitada, esse valor representa a quantidade de tempo de desvaloração (em TimeSpan) tolerada.</span><span class="sxs-lookup"><span data-stu-id="b71a6-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="b71a6-153">O intervalo aceito para esse valor é 5-86400.</span><span class="sxs-lookup"><span data-stu-id="b71a6-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="b71a6-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="b71a6-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="b71a6-155">Quando usado com consistência de ultrapassabilidade limitada, esse valor representa o número de solicitações obsoletas toleradas.</span><span class="sxs-lookup"><span data-stu-id="b71a6-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="b71a6-156">O intervalo aceito para esse valor é de 1 a 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="b71a6-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="b71a6-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="b71a6-157">-Name</span></span>
<span data-ttu-id="b71a6-158">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="b71a6-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b71a6-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b71a6-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="b71a6-160">Se o acesso de ponto de extremidade público ou não é permitido para este servidor.</span><span class="sxs-lookup"><span data-stu-id="b71a6-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="b71a6-161">Os valores possíveis incluem: ' Enabled ', ' disabled '</span><span class="sxs-lookup"><span data-stu-id="b71a6-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="b71a6-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71a6-162">-ResourceGroupName</span></span>
<span data-ttu-id="b71a6-163">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b71a6-163">Name of resource group.</span></span>

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

### <span data-ttu-id="b71a6-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b71a6-164">-ServerVersion</span></span>
<span data-ttu-id="b71a6-165">ServerVersion, válido somente em caso de contas do MongoDB.</span><span class="sxs-lookup"><span data-stu-id="b71a6-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="b71a6-166">-Marca</span><span class="sxs-lookup"><span data-stu-id="b71a6-166">-Tag</span></span>
<span data-ttu-id="b71a6-167">Hashtable de marcas como pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="b71a6-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="b71a6-168">Use uma cadeia de caracteres vazia para limpar a marca existente.</span><span class="sxs-lookup"><span data-stu-id="b71a6-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="b71a6-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b71a6-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="b71a6-170">Matriz de valores de cadeia de caracteres de ACL para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b71a6-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="b71a6-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="b71a6-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="b71a6-172">Matriz de PSVirtualNetworkRuleObjects para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b71a6-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="b71a6-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b71a6-173">-WhatIf</span></span>
<span data-ttu-id="b71a6-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b71a6-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b71a6-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b71a6-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b71a6-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71a6-176">CommonParameters</span></span>
<span data-ttu-id="b71a6-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b71a6-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71a6-178">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b71a6-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71a6-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b71a6-179">INPUTS</span></span>

### <span data-ttu-id="b71a6-180">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="b71a6-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="b71a6-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b71a6-181">OUTPUTS</span></span>

### <span data-ttu-id="b71a6-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b71a6-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b71a6-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b71a6-183">NOTES</span></span>

## <span data-ttu-id="b71a6-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b71a6-184">RELATED LINKS</span></span>
