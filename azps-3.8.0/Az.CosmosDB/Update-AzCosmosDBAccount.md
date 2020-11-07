---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940552"
---
# <span data-ttu-id="c109e-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="c109e-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="c109e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c109e-102">SYNOPSIS</span></span>
<span data-ttu-id="c109e-103">Atualize os atributos de uma conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c109e-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="c109e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c109e-104">SYNTAX</span></span>

### <span data-ttu-id="c109e-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c109e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c109e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c109e-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c109e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c109e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c109e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c109e-108">DESCRIPTION</span></span>
<span data-ttu-id="c109e-109">Atualizar as propriedades de uma conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c109e-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="c109e-110">Não é possível atualizar as regiões da conta simulataneously com outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="c109e-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="c109e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c109e-111">EXAMPLES</span></span>

### <span data-ttu-id="c109e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c109e-112">Example 1</span></span>
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

<span data-ttu-id="c109e-113">DefaultConsistencyLevel atualizado para "Strong", habilitado AutomaticFailover, habilitado MultipleWriteLocations e compatível com o VirtualNetwork para CosmosDB conta com nome accountName.</span><span class="sxs-lookup"><span data-stu-id="c109e-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="c109e-114">OS</span><span class="sxs-lookup"><span data-stu-id="c109e-114">PARAMETERS</span></span>

### <span data-ttu-id="c109e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c109e-115">-AsJob</span></span>
<span data-ttu-id="c109e-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c109e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c109e-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c109e-117">-Confirm</span></span>
<span data-ttu-id="c109e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c109e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c109e-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="c109e-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="c109e-120">Nível de consistência padrão da conta de banco de dados do banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="c109e-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="c109e-121">Valores aceitos: BoundedStaleness, ConsistentPrefix, eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="c109e-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="c109e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c109e-122">-DefaultProfile</span></span>
<span data-ttu-id="c109e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c109e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c109e-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="c109e-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="c109e-125">Desabilitar operações de gravação em recursos de metadados (bancos de dados, contêineres, produtividade) via chaves de conta</span><span class="sxs-lookup"><span data-stu-id="c109e-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="c109e-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="c109e-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="c109e-127">Habilita o failover automático da região de gravação no evento raro que a região não está disponível devido a uma interrupção.</span><span class="sxs-lookup"><span data-stu-id="c109e-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="c109e-128">O failover automático fará uma nova região de gravação para a conta e será escolhido com base nas prioridades de failover configuradas para a conta.</span><span class="sxs-lookup"><span data-stu-id="c109e-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="c109e-129">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="c109e-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="c109e-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="c109e-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="c109e-131">Habilite vários locais de gravação.</span><span class="sxs-lookup"><span data-stu-id="c109e-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="c109e-132">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="c109e-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="c109e-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c109e-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="c109e-134">Habilita a rede virtual na conta de banco de dados do cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c109e-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="c109e-135">Valores aceitos: falso, verdadeiro</span><span class="sxs-lookup"><span data-stu-id="c109e-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="c109e-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c109e-136">-InputObject</span></span>
<span data-ttu-id="c109e-137">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c109e-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c109e-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="c109e-138">-IpRangeFilter</span></span>
<span data-ttu-id="c109e-139">Suporte a firewall.</span><span class="sxs-lookup"><span data-stu-id="c109e-139">Firewall support.</span></span>
<span data-ttu-id="c109e-140">Especifica o conjunto de endereços IP ou intervalos de endereços IP no formato CIDR a ser incluído como a lista permitida de IPs de cliente para uma determinada conta de banco de dados</span><span class="sxs-lookup"><span data-stu-id="c109e-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="c109e-141">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c109e-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="c109e-142">Quando usado com consistência de ultrapassabilidade limitada, esse valor representa a quantidade de tempo de desvaloração (em TimeSpan) tolerada.</span><span class="sxs-lookup"><span data-stu-id="c109e-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="c109e-143">O intervalo aceito para esse valor é 5-86400.</span><span class="sxs-lookup"><span data-stu-id="c109e-143">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="c109e-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="c109e-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="c109e-145">Quando usado com consistência de ultrapassabilidade limitada, esse valor representa o número de solicitações obsoletas toleradas.</span><span class="sxs-lookup"><span data-stu-id="c109e-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="c109e-146">O intervalo aceito para esse valor é de 1 a 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="c109e-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="c109e-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="c109e-147">-Name</span></span>
<span data-ttu-id="c109e-148">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="c109e-148">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c109e-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c109e-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="c109e-150">Se o acesso de ponto de extremidade público ou não é permitido para este servidor.</span><span class="sxs-lookup"><span data-stu-id="c109e-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="c109e-151">Os valores possíveis incluem: ' Enabled ', ' disabled '</span><span class="sxs-lookup"><span data-stu-id="c109e-151">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="c109e-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c109e-152">-ResourceGroupName</span></span>
<span data-ttu-id="c109e-153">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c109e-153">Name of resource group.</span></span>

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

### <span data-ttu-id="c109e-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c109e-154">-ResourceId</span></span>
<span data-ttu-id="c109e-155">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="c109e-155">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="c109e-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="c109e-156">-Tag</span></span>
<span data-ttu-id="c109e-157">Hashtable de marcas como pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="c109e-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="c109e-158">Use uma cadeia de caracteres vazia para limpar a marca existente.</span><span class="sxs-lookup"><span data-stu-id="c109e-158">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="c109e-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c109e-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="c109e-160">Matriz de valores de cadeia de caracteres de ACL para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c109e-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="c109e-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="c109e-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="c109e-162">Matriz de PSVirtualNetworkRuleObjects para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c109e-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c109e-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c109e-163">-WhatIf</span></span>
<span data-ttu-id="c109e-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c109e-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c109e-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c109e-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c109e-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c109e-166">CommonParameters</span></span>
<span data-ttu-id="c109e-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c109e-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c109e-168">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c109e-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c109e-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c109e-169">INPUTS</span></span>

### <span data-ttu-id="c109e-170">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="c109e-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="c109e-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c109e-171">OUTPUTS</span></span>

### <span data-ttu-id="c109e-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c109e-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c109e-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c109e-173">NOTES</span></span>

## <span data-ttu-id="c109e-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c109e-174">RELATED LINKS</span></span>
