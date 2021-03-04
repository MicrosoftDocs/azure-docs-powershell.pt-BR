---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 75085bed9c1f9b0cd0c0328b9a166c6dc08a60b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890640"
---
# <span data-ttu-id="dd8f6-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="dd8f6-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="dd8f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8f6-103">Crie uma nova conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="dd8f6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dd8f6-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>] [-Location <String[]>]
 [-LocationObject <PSLocation[]>] -ResourceGroupName <String> -Name <String>
 [-DefaultConsistencyLevel <String>] [-IpRule <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-PublicNetworkAccess <String>]
 [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob] [-NetworkAclBypass <String>]
 [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>] [-BackupIntervalInMinutes <Int32>]
 [-BackupRetentionIntervalInHours <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd8f6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dd8f6-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8f6-106">Crie uma nova Conta do CosmosDB no ResourceGroup determinado.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="dd8f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd8f6-107">EXAMPLES</span></span>

### <span data-ttu-id="dd8f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd8f6-108">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="dd8f6-109">Uma nova Conta do CosmosDB com nome databaseAccountName é criada no resourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="dd8f6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dd8f6-110">PARAMETERS</span></span>

### <span data-ttu-id="dd8f6-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="dd8f6-111">-ApiKind</span></span>
<span data-ttu-id="dd8f6-112">O tipo de conta de banco de dados db do Cosmos a ser criado.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="dd8f6-113">Valores aceitos: Sql, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="dd8f6-114">Valor padrão: Sql</span><span class="sxs-lookup"><span data-stu-id="dd8f6-114">Default value: Sql</span></span>

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

### <span data-ttu-id="dd8f6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd8f6-115">-AsJob</span></span>
<span data-ttu-id="dd8f6-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dd8f6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd8f6-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="dd8f6-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="dd8f6-118">O intervalo(em minutos) com o qual o backup é feito (somente para contas com backups de modo periódico)</span><span class="sxs-lookup"><span data-stu-id="dd8f6-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="dd8f6-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="dd8f6-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="dd8f6-120">O tempo(em horas) para o qual cada backup é mantido (somente para contas com backups de modo periódico)</span><span class="sxs-lookup"><span data-stu-id="dd8f6-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="dd8f6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd8f6-121">-Confirm</span></span>
<span data-ttu-id="dd8f6-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd8f6-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="dd8f6-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="dd8f6-124">Nível de consistência padrão da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="dd8f6-125">Valores aceitos: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="dd8f6-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="dd8f6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8f6-126">-DefaultProfile</span></span>
<span data-ttu-id="dd8f6-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd8f6-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="dd8f6-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="dd8f6-129">Desabilitar operações de gravação em recursos de metadados (bancos de dados, contêineres, transferência) por meio de chaves de conta</span><span class="sxs-lookup"><span data-stu-id="dd8f6-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="dd8f6-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="dd8f6-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="dd8f6-131">Bool para indicar se AnalyticalStorage está habilitado na conta.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="dd8f6-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="dd8f6-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="dd8f6-133">Habilita o failover automático da região de gravação no evento raro em que a região está indisponível devido a uma paralisação.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="dd8f6-134">O failover automático resultará em uma nova região de gravação para a conta e será escolhido com base nas prioridades de failover configuradas para a conta.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="dd8f6-135">Valores aceitos: false, true</span><span class="sxs-lookup"><span data-stu-id="dd8f6-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="dd8f6-136">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="dd8f6-136">-EnableFreeTier</span></span>
<span data-ttu-id="dd8f6-137">Bool para indicar se FreeTier está habilitado na conta.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-137">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="dd8f6-138">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="dd8f6-138">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="dd8f6-139">Habilitar vários locais de gravação.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-139">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="dd8f6-140">Valores aceitos: false, true</span><span class="sxs-lookup"><span data-stu-id="dd8f6-140">Accepted values: false, true</span></span>

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

### <span data-ttu-id="dd8f6-141">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dd8f6-141">-EnableVirtualNetwork</span></span>
<span data-ttu-id="dd8f6-142">Habilita a rede virtual na conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-142">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="dd8f6-143">Valores aceitos: false, true</span><span class="sxs-lookup"><span data-stu-id="dd8f6-143">Accepted values: false, true</span></span>

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

### <span data-ttu-id="dd8f6-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="dd8f6-144">-IpRule</span></span>
<span data-ttu-id="dd8f6-145">Suporte ao firewall.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-145">Firewall support.</span></span> <span data-ttu-id="dd8f6-146">Especifica o conjunto de endereços IP ou intervalos de endereços IP no formulário CIDR a ser incluído como a lista de IPs de cliente permitidos para uma determinada conta de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="dd8f6-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="dd8f6-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="dd8f6-148">URI do KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd8f6-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="dd8f6-149">-Location</span><span class="sxs-lookup"><span data-stu-id="dd8f6-149">-Location</span></span>
<span data-ttu-id="dd8f6-150">Adicione um local à conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-150">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="dd8f6-151">Matriz de cadeias de caracteres, ordenada por prioridade de failover.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-151">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="dd8f6-152">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="dd8f6-152">-LocationObject</span></span>
<span data-ttu-id="dd8f6-153">Adicione um local à conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-153">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="dd8f6-154">Matriz de objetos PSLocation.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-154">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="dd8f6-155">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="dd8f6-155">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="dd8f6-156">Quando usado com consistência de Estaleza Limitada, esse valor representa a quantidade de tempo de atraso (em tempo limite) tolerada.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-156">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="dd8f6-157">O intervalo aceito para esse valor é 5-86400.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-157">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="dd8f6-158">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="dd8f6-158">-MaxStalenessPrefix</span></span>
<span data-ttu-id="dd8f6-159">Quando usado com consistência de Estaleosidade Limitada, esse valor representa o número de solicitações de atraso toleradas.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-159">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="dd8f6-160">O intervalo aceito para esse valor é 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-160">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="dd8f6-161">-Name</span><span class="sxs-lookup"><span data-stu-id="dd8f6-161">-Name</span></span>
<span data-ttu-id="dd8f6-162">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-162">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dd8f6-163">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="dd8f6-163">-NetworkAclBypass</span></span>
<span data-ttu-id="dd8f6-164">Se o Bypass de Rede Acl está habilitado ou não para essa conta para o Link Synapse.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-164">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="dd8f6-165">Os valores possíveis incluem: 'None', 'AzureServices'.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-165">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="dd8f6-166">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="dd8f6-166">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="dd8f6-167">Lista de IDs de Recursos para permitir Bypass de Rede Acl para Link Synapse.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-167">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="dd8f6-168">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="dd8f6-168">-PublicNetworkAccess</span></span>
<span data-ttu-id="dd8f6-169">Se o acesso ao ponto de extremidade público é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-169">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="dd8f6-170">Os valores possíveis incluem: 'Habilitado', 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="dd8f6-170">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="dd8f6-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8f6-171">-ResourceGroupName</span></span>
<span data-ttu-id="dd8f6-172">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-172">Name of resource group.</span></span>

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

### <span data-ttu-id="dd8f6-173">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="dd8f6-173">-ServerVersion</span></span>
<span data-ttu-id="dd8f6-174">ServerVersion, válido somente no caso de Contas MongoDB.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-174">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="dd8f6-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd8f6-175">-Tag</span></span>
<span data-ttu-id="dd8f6-176">Hashtable de marcas como pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-176">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="dd8f6-177">Use a cadeia de caracteres vazia para limpar a marca existente.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-177">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="dd8f6-178">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dd8f6-178">-VirtualNetworkRule</span></span>
<span data-ttu-id="dd8f6-179">Matriz de valores de cadeia de caracteres de ACL para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-179">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="dd8f6-180">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="dd8f6-180">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="dd8f6-181">Matriz de PSVirtualNetworkRuleObjects para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-181">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="dd8f6-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8f6-182">-WhatIf</span></span>
<span data-ttu-id="dd8f6-183">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8f6-184">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd8f6-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8f6-185">CommonParameters</span></span>
<span data-ttu-id="dd8f6-186">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8f6-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8f6-187">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd8f6-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8f6-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd8f6-188">INPUTS</span></span>

### <span data-ttu-id="dd8f6-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="dd8f6-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="dd8f6-190">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dd8f6-190">OUTPUTS</span></span>

### <span data-ttu-id="dd8f6-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="dd8f6-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="dd8f6-192">NOTES</span><span class="sxs-lookup"><span data-stu-id="dd8f6-192">NOTES</span></span>

## <span data-ttu-id="dd8f6-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd8f6-193">RELATED LINKS</span></span>
