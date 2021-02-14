---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111025"
---
# <span data-ttu-id="5eabc-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="5eabc-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="5eabc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5eabc-102">SYNOPSIS</span></span>
<span data-ttu-id="5eabc-103">Atualize os atributos de uma conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5eabc-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="5eabc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5eabc-104">SYNTAX</span></span>

### <span data-ttu-id="5eabc-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5eabc-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eabc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5eabc-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eabc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5eabc-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eabc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5eabc-108">DESCRIPTION</span></span>
<span data-ttu-id="5eabc-109">Atualize as propriedades de uma conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5eabc-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="5eabc-110">Não é possível atualizar as Regiões de Conta de forma simulada com outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="5eabc-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="5eabc-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5eabc-111">EXAMPLES</span></span>

### <span data-ttu-id="5eabc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5eabc-112">Example 1</span></span>
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
```

<span data-ttu-id="5eabc-113">DefaultConsistencyLevel atualizado como "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations e Enabled VirtualNetwork for CosmosDB Account with name accountName.</span><span class="sxs-lookup"><span data-stu-id="5eabc-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="5eabc-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5eabc-114">PARAMETERS</span></span>

### <span data-ttu-id="5eabc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5eabc-115">-AsJob</span></span>
<span data-ttu-id="5eabc-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5eabc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5eabc-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5eabc-117">-Confirm</span></span>
<span data-ttu-id="5eabc-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eabc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eabc-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="5eabc-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="5eabc-120">Nível de consistência padrão da conta do banco de dados Db Db.</span><span class="sxs-lookup"><span data-stu-id="5eabc-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="5eabc-121">Valores aceitos: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="5eabc-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="5eabc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eabc-122">-DefaultProfile</span></span>
<span data-ttu-id="5eabc-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5eabc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eabc-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="5eabc-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="5eabc-125">Desabilitar operações de gravação em recursos de metadados (bancos de dados, contêineres, produtividade) por meio de chaves de conta</span><span class="sxs-lookup"><span data-stu-id="5eabc-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="5eabc-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="5eabc-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="5eabc-127">Bool para indicar se a AnalyticalStorage está habilitada na conta.</span><span class="sxs-lookup"><span data-stu-id="5eabc-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="5eabc-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="5eabc-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="5eabc-129">Habilita o failover automático da região de gravação no evento raro em que a região não está disponível devido a uma falha.</span><span class="sxs-lookup"><span data-stu-id="5eabc-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="5eabc-130">O failover automático resultará em uma nova região de gravação para a conta e será escolhido com base nas prioridades de failover configuradas para a conta.</span><span class="sxs-lookup"><span data-stu-id="5eabc-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="5eabc-131">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="5eabc-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="5eabc-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="5eabc-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="5eabc-133">Habilitar vários locais de gravação.</span><span class="sxs-lookup"><span data-stu-id="5eabc-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="5eabc-134">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="5eabc-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="5eabc-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5eabc-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="5eabc-136">Habilita a rede virtual na conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="5eabc-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="5eabc-137">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="5eabc-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="5eabc-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eabc-138">-InputObject</span></span>
<span data-ttu-id="5eabc-139">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="5eabc-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5eabc-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="5eabc-140">-IpRule</span></span>
<span data-ttu-id="5eabc-141">Suporte para firewall.</span><span class="sxs-lookup"><span data-stu-id="5eabc-141">Firewall support.</span></span> <span data-ttu-id="5eabc-142">Especifica o conjunto de endereços IP ou intervalos de endereços IP no formulário CIDR a ser incluído como a lista de IPs de cliente permitidos para uma determinada conta de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5eabc-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="5eabc-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="5eabc-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="5eabc-144">URI do KeyVault</span><span class="sxs-lookup"><span data-stu-id="5eabc-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="5eabc-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5eabc-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="5eabc-146">Quando usado com a consistência de Estaleçamento Limitado, esse valor representa a quantidade de tempo de atraso (em tempo) indevida.</span><span class="sxs-lookup"><span data-stu-id="5eabc-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="5eabc-147">O intervalo aceito para esse valor é 5-86400.</span><span class="sxs-lookup"><span data-stu-id="5eabc-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="5eabc-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="5eabc-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="5eabc-149">Quando usado com a consistência de Estaleçamento Limitado, esse valor representa o número de solicitações desajustadas.</span><span class="sxs-lookup"><span data-stu-id="5eabc-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="5eabc-150">O intervalo aceito para esse valor é 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="5eabc-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="5eabc-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="5eabc-151">-Name</span></span>
<span data-ttu-id="5eabc-152">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="5eabc-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5eabc-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5eabc-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="5eabc-154">Se o acesso ao ponto de extremidade público é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="5eabc-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="5eabc-155">Os valores possíveis incluem: 'Habilitado', 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="5eabc-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="5eabc-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eabc-156">-ResourceGroupName</span></span>
<span data-ttu-id="5eabc-157">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5eabc-157">Name of resource group.</span></span>

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

### <span data-ttu-id="5eabc-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5eabc-158">-ResourceId</span></span>
<span data-ttu-id="5eabc-159">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="5eabc-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="5eabc-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="5eabc-160">-Tag</span></span>
<span data-ttu-id="5eabc-161">Hashtable of tags as key-value pairs.</span><span class="sxs-lookup"><span data-stu-id="5eabc-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="5eabc-162">Use uma cadeia de caracteres vazia para limpar a marca existente.</span><span class="sxs-lookup"><span data-stu-id="5eabc-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="5eabc-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5eabc-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="5eabc-164">Matriz de valores de cadeia de caracteres de ACL para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5eabc-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="5eabc-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5eabc-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="5eabc-166">Matriz de PSVirtualNetworkRuleObjects para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5eabc-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="5eabc-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eabc-167">-WhatIf</span></span>
<span data-ttu-id="5eabc-168">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5eabc-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eabc-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5eabc-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eabc-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eabc-170">CommonParameters</span></span>
<span data-ttu-id="5eabc-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eabc-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eabc-172">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5eabc-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eabc-173">Entradas</span><span class="sxs-lookup"><span data-stu-id="5eabc-173">INPUTS</span></span>

### <span data-ttu-id="5eabc-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="5eabc-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="5eabc-175">Saídas</span><span class="sxs-lookup"><span data-stu-id="5eabc-175">OUTPUTS</span></span>

### <span data-ttu-id="5eabc-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5eabc-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5eabc-177">Notas</span><span class="sxs-lookup"><span data-stu-id="5eabc-177">NOTES</span></span>

## <span data-ttu-id="5eabc-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eabc-178">RELATED LINKS</span></span>
