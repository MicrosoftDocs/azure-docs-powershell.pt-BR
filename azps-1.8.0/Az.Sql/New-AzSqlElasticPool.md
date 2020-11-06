---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fbc0d1e1ac32906c081c5a9714c8420e0f1292e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598892"
---
# <span data-ttu-id="8ad93-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8ad93-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="8ad93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ad93-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad93-103">Cria um pool de banco de dados elástico para um banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="8ad93-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="8ad93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ad93-104">SYNTAX</span></span>

### <span data-ttu-id="8ad93-105">DtuBasedPool (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ad93-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad93-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="8ad93-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ad93-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ad93-107">DESCRIPTION</span></span>
<span data-ttu-id="8ad93-108">O cmdlet **New-AzSqlElasticPool** cria um pool de banco de dados elástico para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad93-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="8ad93-109">Vários parâmetros ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) exigem que o valor definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8ad93-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="8ad93-110">Por exemplo,-DatabaseDtuMax para um pool de eDTU de 100 padrão só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="8ad93-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="8ad93-111">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="8ad93-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="8ad93-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ad93-112">EXAMPLES</span></span>

### <span data-ttu-id="8ad93-113">Exemplo 1: criar um pool elástico</span><span class="sxs-lookup"><span data-stu-id="8ad93-113">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="8ad93-114">Esse comando cria um pool elástico na camada de serviço padrão chamada ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="8ad93-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="8ad93-115">O servidor chamado Server01, atribuído a um grupo de recursos do Azure chamado ResourceGroup01, hospeda o pool elástico no.</span><span class="sxs-lookup"><span data-stu-id="8ad93-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="8ad93-116">O comando especifica os valores da propriedade DTU para o pool e os bancos de dados no pool.</span><span class="sxs-lookup"><span data-stu-id="8ad93-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="8ad93-117">OS</span><span class="sxs-lookup"><span data-stu-id="8ad93-117">PARAMETERS</span></span>

### <span data-ttu-id="8ad93-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ad93-118">-AsJob</span></span>
<span data-ttu-id="8ad93-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8ad93-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="8ad93-120">-ComputeGeneration</span></span>
<span data-ttu-id="8ad93-121">A geração de computação a ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="8ad93-121">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="8ad93-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="8ad93-123">Especifica o número máximo de unidades de produtividade do banco de dados (DTUs) que qualquer único banco de dados no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="8ad93-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="8ad93-124">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="8ad93-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="8ad93-125">Basic.</span><span class="sxs-lookup"><span data-stu-id="8ad93-125">Basic.</span></span> <span data-ttu-id="8ad93-126">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="8ad93-126">5 DTUs</span></span>
- <span data-ttu-id="8ad93-127">Oficial.</span><span class="sxs-lookup"><span data-stu-id="8ad93-127">Standard.</span></span> <span data-ttu-id="8ad93-128">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="8ad93-128">100 DTUs</span></span>
- <span data-ttu-id="8ad93-129">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="8ad93-129">Premium.</span></span> <span data-ttu-id="8ad93-130">125 DTUs para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="8ad93-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="8ad93-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="8ad93-132">Especifica o número mínimo de DTUs que o pool elástico garante para todos os bancos de dados do pool.</span><span class="sxs-lookup"><span data-stu-id="8ad93-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="8ad93-133">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="8ad93-133">The default value is zero (0).</span></span>
<span data-ttu-id="8ad93-134">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="8ad93-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="8ad93-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="8ad93-136">O número VCore da Maxmium qualquer banco de dados sqlazure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="8ad93-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="8ad93-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="8ad93-138">O número mínimo de VCore que qualquer banco de dados sqlazure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="8ad93-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad93-139">-DefaultProfile</span></span>
<span data-ttu-id="8ad93-140">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8ad93-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-141">-DTU</span><span class="sxs-lookup"><span data-stu-id="8ad93-141">-Dtu</span></span>
<span data-ttu-id="8ad93-142">Especifica o número total de DTUs compartilhadas para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="8ad93-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="8ad93-143">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="8ad93-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="8ad93-144">Basic.</span><span class="sxs-lookup"><span data-stu-id="8ad93-144">Basic.</span></span>
<span data-ttu-id="8ad93-145">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="8ad93-145">100 DTUs</span></span>
- <span data-ttu-id="8ad93-146">Oficial.</span><span class="sxs-lookup"><span data-stu-id="8ad93-146">Standard.</span></span>
<span data-ttu-id="8ad93-147">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="8ad93-147">100 DTUs</span></span>
- <span data-ttu-id="8ad93-148">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="8ad93-148">Premium.</span></span>
<span data-ttu-id="8ad93-149">125 DTUs para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="8ad93-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-150">-Edição</span><span class="sxs-lookup"><span data-stu-id="8ad93-150">-Edition</span></span>
<span data-ttu-id="8ad93-151">Especifica a edição do banco de dados SQL do Azure usado para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="8ad93-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="8ad93-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8ad93-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ad93-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8ad93-153">None</span></span>
- <span data-ttu-id="8ad93-154">Basic</span><span class="sxs-lookup"><span data-stu-id="8ad93-154">Basic</span></span>
- <span data-ttu-id="8ad93-155">Oficial</span><span class="sxs-lookup"><span data-stu-id="8ad93-155">Standard</span></span>
- <span data-ttu-id="8ad93-156">Gratifica</span><span class="sxs-lookup"><span data-stu-id="8ad93-156">Premium</span></span>
- <span data-ttu-id="8ad93-157">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="8ad93-157">DataWarehouse</span></span>
- <span data-ttu-id="8ad93-158">Gratuito</span><span class="sxs-lookup"><span data-stu-id="8ad93-158">Free</span></span>
- <span data-ttu-id="8ad93-159">Automático</span><span class="sxs-lookup"><span data-stu-id="8ad93-159">Stretch</span></span>
- <span data-ttu-id="8ad93-160">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="8ad93-160">GeneralPurpose</span></span>
- <span data-ttu-id="8ad93-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="8ad93-161">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8ad93-162">-ElasticPoolName</span></span>
<span data-ttu-id="8ad93-163">Especifica o nome do pool elástico que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="8ad93-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8ad93-164">-LicenseType</span></span>
<span data-ttu-id="8ad93-165">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad93-165">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad93-166">-ResourceGroupName</span></span>
<span data-ttu-id="8ad93-167">Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="8ad93-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-168">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="8ad93-168">-ServerName</span></span>
<span data-ttu-id="8ad93-169">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="8ad93-169">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="8ad93-170">-StorageMB</span></span>
<span data-ttu-id="8ad93-171">Especifica o limite de armazenamento, em megabytes, para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="8ad93-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="8ad93-172">Se você não especificar esse parâmetro, esse cmdlet calculará um valor que depende do valor do parâmetro *DTU* .</span><span class="sxs-lookup"><span data-stu-id="8ad93-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="8ad93-173">Veja [os limites de eDTU e armazenamento](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) para os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="8ad93-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-174">-Marcas</span><span class="sxs-lookup"><span data-stu-id="8ad93-174">-Tags</span></span>
<span data-ttu-id="8ad93-175">Especifica um dicionário de pares de chave-valor na forma de uma tabela de hash que este cmdlet associa ao pool elástico.</span><span class="sxs-lookup"><span data-stu-id="8ad93-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="8ad93-176">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8ad93-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="8ad93-177">-VCore</span></span>
<span data-ttu-id="8ad93-178">O número total compartilhado de Vcores para o pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad93-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="8ad93-179">-ZoneRedundant</span></span>
<span data-ttu-id="8ad93-180">A redundância de zona para associar ao pool elástico do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="8ad93-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-181">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ad93-181">-Confirm</span></span>
<span data-ttu-id="8ad93-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ad93-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ad93-183">-WhatIf</span></span>
<span data-ttu-id="8ad93-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ad93-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ad93-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ad93-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad93-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad93-186">CommonParameters</span></span>
<span data-ttu-id="8ad93-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ad93-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad93-188">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ad93-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad93-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ad93-189">INPUTS</span></span>

### <span data-ttu-id="8ad93-190">System. String</span><span class="sxs-lookup"><span data-stu-id="8ad93-190">System.String</span></span>

## <span data-ttu-id="8ad93-191">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ad93-191">OUTPUTS</span></span>

### <span data-ttu-id="8ad93-192">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="8ad93-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="8ad93-193">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ad93-193">NOTES</span></span>

## <span data-ttu-id="8ad93-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ad93-194">RELATED LINKS</span></span>

[<span data-ttu-id="8ad93-195">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8ad93-195">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="8ad93-196">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="8ad93-196">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="8ad93-197">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="8ad93-197">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="8ad93-198">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8ad93-198">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="8ad93-199">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8ad93-199">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="8ad93-200">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="8ad93-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
