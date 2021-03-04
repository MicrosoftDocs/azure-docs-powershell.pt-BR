---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: cbee0ef9ce750dbb72af5be484106ccabec79321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892994"
---
# <span data-ttu-id="65750-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="65750-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="65750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65750-102">SYNOPSIS</span></span>
<span data-ttu-id="65750-103">Atualizar atributos de conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="65750-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="65750-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65750-104">SYNTAX</span></span>

### <span data-ttu-id="65750-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65750-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65750-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65750-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65750-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65750-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65750-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65750-108">DESCRIPTION</span></span>
<span data-ttu-id="65750-109">Atualize as propriedades de uma conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="65750-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="65750-110">Não é possível atualizar as Regiões de Conta de forma simulada com outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="65750-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="65750-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65750-111">EXAMPLES</span></span>

### <span data-ttu-id="65750-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65750-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="65750-113">Atualizado DefaultConsistencyLevel para "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations e Enabled VirtualNetwork for CosmosDB Account with name accountName.</span><span class="sxs-lookup"><span data-stu-id="65750-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="65750-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65750-114">PARAMETERS</span></span>

### <span data-ttu-id="65750-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65750-115">-AsJob</span></span>
<span data-ttu-id="65750-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="65750-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65750-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="65750-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="65750-118">O intervalo(em minutos) com o qual o backup é feito (somente para contas com backups de modo periódico)</span><span class="sxs-lookup"><span data-stu-id="65750-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="65750-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="65750-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="65750-120">O tempo(em horas) para o qual cada backup é mantido (somente para contas com backups de modo periódico)</span><span class="sxs-lookup"><span data-stu-id="65750-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="65750-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65750-121">-Confirm</span></span>
<span data-ttu-id="65750-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65750-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65750-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="65750-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="65750-124">Nível de consistência padrão da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="65750-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="65750-125">Valores aceitos: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="65750-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="65750-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65750-126">-DefaultProfile</span></span>
<span data-ttu-id="65750-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65750-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65750-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="65750-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="65750-129">Desabilitar operações de gravação em recursos de metadados (bancos de dados, contêineres, transferência) por meio de chaves de conta</span><span class="sxs-lookup"><span data-stu-id="65750-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="65750-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="65750-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="65750-131">Bool para indicar se AnalyticalStorage está habilitado na conta.</span><span class="sxs-lookup"><span data-stu-id="65750-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="65750-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="65750-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="65750-133">Habilita o failover automático da região de gravação no evento raro em que a região está indisponível devido a uma paralisação.</span><span class="sxs-lookup"><span data-stu-id="65750-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="65750-134">O failover automático resultará em uma nova região de gravação para a conta e será escolhido com base nas prioridades de failover configuradas para a conta.</span><span class="sxs-lookup"><span data-stu-id="65750-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="65750-135">Valores aceitos: false, true</span><span class="sxs-lookup"><span data-stu-id="65750-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="65750-136">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="65750-136">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="65750-137">Habilitar vários locais de gravação.</span><span class="sxs-lookup"><span data-stu-id="65750-137">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="65750-138">Valores aceitos: false, true</span><span class="sxs-lookup"><span data-stu-id="65750-138">Accepted values: false, true</span></span>

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

### <span data-ttu-id="65750-139">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="65750-139">-EnableVirtualNetwork</span></span>
<span data-ttu-id="65750-140">Habilita a rede virtual na conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="65750-140">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="65750-141">Valores aceitos: false, true</span><span class="sxs-lookup"><span data-stu-id="65750-141">Accepted values: false, true</span></span>

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

### <span data-ttu-id="65750-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65750-142">-InputObject</span></span>
<span data-ttu-id="65750-143">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="65750-143">CosmosDB Account object</span></span>

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

### <span data-ttu-id="65750-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="65750-144">-IpRule</span></span>
<span data-ttu-id="65750-145">Suporte ao firewall.</span><span class="sxs-lookup"><span data-stu-id="65750-145">Firewall support.</span></span> <span data-ttu-id="65750-146">Especifica o conjunto de endereços IP ou intervalos de endereços IP no formulário CIDR a ser incluído como a lista de IPs de cliente permitidos para uma determinada conta de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="65750-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="65750-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="65750-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="65750-148">URI do KeyVault</span><span class="sxs-lookup"><span data-stu-id="65750-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="65750-149">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="65750-149">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="65750-150">Quando usado com consistência de Estaleza Limitada, esse valor representa a quantidade de tempo de atraso (em tempo limite) tolerada.</span><span class="sxs-lookup"><span data-stu-id="65750-150">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="65750-151">O intervalo aceito para esse valor é 5-86400.</span><span class="sxs-lookup"><span data-stu-id="65750-151">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="65750-152">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="65750-152">-MaxStalenessPrefix</span></span>
<span data-ttu-id="65750-153">Quando usado com consistência de Estaleosidade Limitada, esse valor representa o número de solicitações de atraso toleradas.</span><span class="sxs-lookup"><span data-stu-id="65750-153">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="65750-154">O intervalo aceito para esse valor é 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="65750-154">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="65750-155">-Name</span><span class="sxs-lookup"><span data-stu-id="65750-155">-Name</span></span>
<span data-ttu-id="65750-156">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="65750-156">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="65750-157">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="65750-157">-NetworkAclBypass</span></span>
<span data-ttu-id="65750-158">Se o Bypass de Rede Acl está habilitado ou não para essa conta para o Link Synapse.</span><span class="sxs-lookup"><span data-stu-id="65750-158">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="65750-159">Os valores possíveis incluem: 'None', 'AzureServices'.</span><span class="sxs-lookup"><span data-stu-id="65750-159">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="65750-160">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="65750-160">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="65750-161">Lista de IDs de Recursos para permitir Bypass de Rede Acl para Link Synapse.</span><span class="sxs-lookup"><span data-stu-id="65750-161">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="65750-162">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="65750-162">-PublicNetworkAccess</span></span>
<span data-ttu-id="65750-163">Se o acesso ao ponto de extremidade público é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="65750-163">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="65750-164">Os valores possíveis incluem: 'Habilitado', 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="65750-164">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="65750-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65750-165">-ResourceGroupName</span></span>
<span data-ttu-id="65750-166">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65750-166">Name of resource group.</span></span>

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

### <span data-ttu-id="65750-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65750-167">-ResourceId</span></span>
<span data-ttu-id="65750-168">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="65750-168">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="65750-169">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="65750-169">-ServerVersion</span></span>
<span data-ttu-id="65750-170">ServerVersion, válido somente no caso de Contas MongoDB.</span><span class="sxs-lookup"><span data-stu-id="65750-170">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="65750-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="65750-171">-Tag</span></span>
<span data-ttu-id="65750-172">Hashtable de marcas como pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="65750-172">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="65750-173">Use a cadeia de caracteres vazia para limpar a marca existente.</span><span class="sxs-lookup"><span data-stu-id="65750-173">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="65750-174">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="65750-174">-VirtualNetworkRule</span></span>
<span data-ttu-id="65750-175">Matriz de valores de cadeia de caracteres de ACL para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="65750-175">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="65750-176">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="65750-176">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="65750-177">Matriz de PSVirtualNetworkRuleObjects para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="65750-177">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="65750-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65750-178">-WhatIf</span></span>
<span data-ttu-id="65750-179">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65750-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65750-180">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65750-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65750-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65750-181">CommonParameters</span></span>
<span data-ttu-id="65750-182">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65750-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65750-183">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65750-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65750-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65750-184">INPUTS</span></span>

### <span data-ttu-id="65750-185">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="65750-185">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="65750-186">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65750-186">OUTPUTS</span></span>

### <span data-ttu-id="65750-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="65750-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="65750-188">NOTES</span><span class="sxs-lookup"><span data-stu-id="65750-188">NOTES</span></span>

## <span data-ttu-id="65750-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65750-189">RELATED LINKS</span></span>
