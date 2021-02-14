---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 810888885c53381c274f85dc79ea2dd7bd4492c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116464"
---
# <span data-ttu-id="b422e-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b422e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b422e-102">SYNOPSIS</span></span>
<span data-ttu-id="b422e-103">Criar uma nova Conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b422e-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="b422e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b422e-104">SYNTAX</span></span>

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

## <span data-ttu-id="b422e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b422e-105">DESCRIPTION</span></span>
<span data-ttu-id="b422e-106">Crie uma nova Conta do CosmosDB no Determinado Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="b422e-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="b422e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b422e-107">EXAMPLES</span></span>

### <span data-ttu-id="b422e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b422e-108">Example 1</span></span>
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

<span data-ttu-id="b422e-109">Uma nova Conta do CosmosDB com nome de banco de dadosAccountName é criada no ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="b422e-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="b422e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b422e-110">PARAMETERS</span></span>

### <span data-ttu-id="b422e-111">-Api Ltda</span><span class="sxs-lookup"><span data-stu-id="b422e-111">-ApiKind</span></span>
<span data-ttu-id="b422e-112">O tipo de conta de banco de dados Do Db para criar.</span><span class="sxs-lookup"><span data-stu-id="b422e-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="b422e-113">Valores aceitos: Sql, MongoDB, Gremlin, Table, Ltda.</span><span class="sxs-lookup"><span data-stu-id="b422e-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="b422e-114">Valor padrão: Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-114">Default value: Sql</span></span>

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

### <span data-ttu-id="b422e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b422e-115">-AsJob</span></span>
<span data-ttu-id="b422e-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b422e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b422e-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b422e-117">-Confirm</span></span>
<span data-ttu-id="b422e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b422e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b422e-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="b422e-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="b422e-120">Nível de consistência padrão da conta do banco de dados Db Db.</span><span class="sxs-lookup"><span data-stu-id="b422e-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="b422e-121">Valores aceitos: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="b422e-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="b422e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b422e-122">-DefaultProfile</span></span>
<span data-ttu-id="b422e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b422e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b422e-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="b422e-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="b422e-125">Desabilitar operações de gravação em recursos de metadados (bancos de dados, contêineres, produtividade) por meio de chaves de conta</span><span class="sxs-lookup"><span data-stu-id="b422e-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="b422e-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="b422e-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="b422e-127">Bool para indicar se a AnalyticalStorage está habilitada na conta.</span><span class="sxs-lookup"><span data-stu-id="b422e-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="b422e-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="b422e-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="b422e-129">Habilita o failover automático da região de gravação no evento raro em que a região não está disponível devido a uma falha.</span><span class="sxs-lookup"><span data-stu-id="b422e-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="b422e-130">O failover automático resultará em uma nova região de gravação para a conta e será escolhido com base nas prioridades de failover configuradas para a conta.</span><span class="sxs-lookup"><span data-stu-id="b422e-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="b422e-131">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="b422e-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b422e-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="b422e-132">-EnableFreeTier</span></span>
<span data-ttu-id="b422e-133">Bool para indicar se o FreeTier está habilitado na conta.</span><span class="sxs-lookup"><span data-stu-id="b422e-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="b422e-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="b422e-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="b422e-135">Habilitar vários locais de gravação.</span><span class="sxs-lookup"><span data-stu-id="b422e-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="b422e-136">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="b422e-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b422e-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b422e-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="b422e-138">Habilita a rede virtual na conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="b422e-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="b422e-139">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="b422e-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="b422e-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="b422e-140">-IpRule</span></span>
<span data-ttu-id="b422e-141">Suporte para firewall.</span><span class="sxs-lookup"><span data-stu-id="b422e-141">Firewall support.</span></span> <span data-ttu-id="b422e-142">Especifica o conjunto de endereços IP ou intervalos de endereços IP no formulário CIDR a ser incluído como a lista de IPs de cliente permitidos para uma determinada conta de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b422e-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="b422e-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="b422e-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="b422e-144">URI do KeyVault</span><span class="sxs-lookup"><span data-stu-id="b422e-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="b422e-145">-Local</span><span class="sxs-lookup"><span data-stu-id="b422e-145">-Location</span></span>
<span data-ttu-id="b422e-146">Adicione um local à conta de banco de dados do Db Db.</span><span class="sxs-lookup"><span data-stu-id="b422e-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="b422e-147">Matriz de cadeias de caracteres, ordenada por prioridade de failover.</span><span class="sxs-lookup"><span data-stu-id="b422e-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="b422e-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="b422e-148">-LocationObject</span></span>
<span data-ttu-id="b422e-149">Adicione um local à conta de banco de dados do Db Db.</span><span class="sxs-lookup"><span data-stu-id="b422e-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="b422e-150">Matriz de objetos PSLocation.</span><span class="sxs-lookup"><span data-stu-id="b422e-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="b422e-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b422e-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="b422e-152">Quando usado com a consistência de Estaleçamento Limitado, esse valor representa a quantidade de tempo de atraso (em tempo) indevida.</span><span class="sxs-lookup"><span data-stu-id="b422e-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="b422e-153">O intervalo aceito para esse valor é 5-86400.</span><span class="sxs-lookup"><span data-stu-id="b422e-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="b422e-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="b422e-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="b422e-155">Quando usado com a consistência de Estaleçamento Limitado, esse valor representa o número de solicitações desajustadas.</span><span class="sxs-lookup"><span data-stu-id="b422e-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="b422e-156">O intervalo aceito para esse valor é 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="b422e-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="b422e-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="b422e-157">-Name</span></span>
<span data-ttu-id="b422e-158">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="b422e-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b422e-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b422e-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="b422e-160">Se o acesso ao ponto de extremidade público é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="b422e-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="b422e-161">Os valores possíveis incluem: 'Habilitado', 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="b422e-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="b422e-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b422e-162">-ResourceGroupName</span></span>
<span data-ttu-id="b422e-163">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b422e-163">Name of resource group.</span></span>

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

### <span data-ttu-id="b422e-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b422e-164">-ServerVersion</span></span>
<span data-ttu-id="b422e-165">ServerVersion, válido somente no caso de Contas MongoDB.</span><span class="sxs-lookup"><span data-stu-id="b422e-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="b422e-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="b422e-166">-Tag</span></span>
<span data-ttu-id="b422e-167">Hashtable of tags as key-value pairs.</span><span class="sxs-lookup"><span data-stu-id="b422e-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="b422e-168">Use uma cadeia de caracteres vazia para limpar a marca existente.</span><span class="sxs-lookup"><span data-stu-id="b422e-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="b422e-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b422e-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="b422e-170">Matriz de valores de cadeia de caracteres de ACL para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b422e-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="b422e-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="b422e-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="b422e-172">Matriz de PSVirtualNetworkRuleObjects para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b422e-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="b422e-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b422e-173">-WhatIf</span></span>
<span data-ttu-id="b422e-174">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b422e-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b422e-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b422e-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b422e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b422e-176">CommonParameters</span></span>
<span data-ttu-id="b422e-177">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b422e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b422e-178">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b422e-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b422e-179">Entradas</span><span class="sxs-lookup"><span data-stu-id="b422e-179">INPUTS</span></span>

### <span data-ttu-id="b422e-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="b422e-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="b422e-181">Saídas</span><span class="sxs-lookup"><span data-stu-id="b422e-181">OUTPUTS</span></span>

### <span data-ttu-id="b422e-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b422e-183">Notas</span><span class="sxs-lookup"><span data-stu-id="b422e-183">NOTES</span></span>

## <span data-ttu-id="b422e-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b422e-184">RELATED LINKS</span></span>
