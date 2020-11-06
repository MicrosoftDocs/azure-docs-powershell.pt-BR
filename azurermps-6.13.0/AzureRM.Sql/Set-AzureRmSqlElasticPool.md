---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 6b059905cdc1e9474ce455f78fac88f282b5ce10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430812"
---
# <span data-ttu-id="ca964-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ca964-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="ca964-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca964-102">SYNOPSIS</span></span>
<span data-ttu-id="ca964-103">Modifica as propriedades de um pool de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca964-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca964-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca964-104">SYNTAX</span></span>

### <span data-ttu-id="ca964-105">DtuBasedPool (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca964-105">DtuBasedPool (Default)</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca964-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="ca964-106">VcoreBasedPool</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca964-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca964-107">DESCRIPTION</span></span>
<span data-ttu-id="ca964-108">O cmdlet **set-AzureRmSqlElasticPool** define propriedades para um pool elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca964-108">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="ca964-109">Esse cmdlet pode modificar o eDTUs por pool ( *DTU* ), o tamanho máximo de armazenamento por pool ( *StorageMB* ), o máximo eDTUs por banco de dados ( *DatabaseDtuMax* ) e o mínimo de EDTUs por banco de dados ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="ca964-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>
<span data-ttu-id="ca964-110">Vários parâmetros ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) exigem que o valor definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ca964-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="ca964-111">Por exemplo,-DatabaseDtuMax para um pool de eDTU de 100 padrão só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="ca964-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="ca964-112">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ca964-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="ca964-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca964-113">EXAMPLES</span></span>

### <span data-ttu-id="ca964-114">Exemplo 1: modificar as propriedades de um pool elástico</span><span class="sxs-lookup"><span data-stu-id="ca964-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="ca964-115">Esse comando modifica as propriedades de um pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="ca964-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="ca964-116">O comando define o número de DTUs para o pool elástico para 1000 e define as DTUs mínima e máxima.</span><span class="sxs-lookup"><span data-stu-id="ca964-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="ca964-117">Exemplo 2: modificar o tamanho máximo de armazenamento de um pool elástico</span><span class="sxs-lookup"><span data-stu-id="ca964-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="ca964-118">Esse comando modifica as propriedades de um pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="ca964-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="ca964-119">O comando define o armazenamento máximo para um pool elástico para 2 TB.</span><span class="sxs-lookup"><span data-stu-id="ca964-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="ca964-120">OS</span><span class="sxs-lookup"><span data-stu-id="ca964-120">PARAMETERS</span></span>

### <span data-ttu-id="ca964-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca964-121">-AsJob</span></span>
<span data-ttu-id="ca964-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ca964-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca964-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ca964-123">-ComputeGeneration</span></span>
<span data-ttu-id="ca964-124">A geração de computação a ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="ca964-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca964-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="ca964-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="ca964-126">Especifica o número máximo de DTUs que qualquer único banco de dados no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="ca964-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="ca964-127">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ca964-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="ca964-128">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="ca964-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="ca964-129">Basic.</span><span class="sxs-lookup"><span data-stu-id="ca964-129">Basic.</span></span>  <span data-ttu-id="ca964-130">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca964-130">5 DTUs</span></span>
- <span data-ttu-id="ca964-131">Oficial.</span><span class="sxs-lookup"><span data-stu-id="ca964-131">Standard.</span></span> <span data-ttu-id="ca964-132">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca964-132">100 DTUs</span></span>
- <span data-ttu-id="ca964-133">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="ca964-133">Premium.</span></span> <span data-ttu-id="ca964-134">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca964-134">125 DTUs</span></span>

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

### <span data-ttu-id="ca964-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="ca964-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="ca964-136">Especifica o número mínimo de DTUs que o pool elástico garante para todos os bancos de dados do pool.</span><span class="sxs-lookup"><span data-stu-id="ca964-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="ca964-137">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ca964-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="ca964-138">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="ca964-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="ca964-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="ca964-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="ca964-140">O número VCore da Maxmium qualquer banco de dados sqlazure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="ca964-140">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="ca964-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="ca964-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="ca964-142">O número mínimo de VCore que qualquer banco de dados sqlazure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="ca964-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="ca964-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca964-143">-DefaultProfile</span></span>
<span data-ttu-id="ca964-144">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ca964-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca964-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="ca964-145">-Dtu</span></span>
<span data-ttu-id="ca964-146">Especifica o número total de DTUs compartilhadas para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="ca964-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="ca964-147">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="ca964-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="ca964-148">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="ca964-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="ca964-149">Basic.</span><span class="sxs-lookup"><span data-stu-id="ca964-149">Basic.</span></span> <span data-ttu-id="ca964-150">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca964-150">100 DTUs</span></span>
- <span data-ttu-id="ca964-151">Oficial.</span><span class="sxs-lookup"><span data-stu-id="ca964-151">Standard.</span></span> <span data-ttu-id="ca964-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca964-152">100 DTUs</span></span>
- <span data-ttu-id="ca964-153">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="ca964-153">Premium.</span></span> <span data-ttu-id="ca964-154">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="ca964-154">125 DTUs</span></span>

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

### <span data-ttu-id="ca964-155">-Edição</span><span class="sxs-lookup"><span data-stu-id="ca964-155">-Edition</span></span>
<span data-ttu-id="ca964-156">Especifica a edição do banco de dados SQL do Azure para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="ca964-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="ca964-157">Não é possível alterar a edição.</span><span class="sxs-lookup"><span data-stu-id="ca964-157">You cannot change the edition.</span></span> <span data-ttu-id="ca964-158">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ca964-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca964-159">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ca964-159">None</span></span>
- <span data-ttu-id="ca964-160">Basic</span><span class="sxs-lookup"><span data-stu-id="ca964-160">Basic</span></span>
- <span data-ttu-id="ca964-161">Oficial</span><span class="sxs-lookup"><span data-stu-id="ca964-161">Standard</span></span>
- <span data-ttu-id="ca964-162">Gratifica</span><span class="sxs-lookup"><span data-stu-id="ca964-162">Premium</span></span>
- <span data-ttu-id="ca964-163">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="ca964-163">DataWarehouse</span></span>
- <span data-ttu-id="ca964-164">Gratuito</span><span class="sxs-lookup"><span data-stu-id="ca964-164">Free</span></span>
- <span data-ttu-id="ca964-165">Automático</span><span class="sxs-lookup"><span data-stu-id="ca964-165">Stretch</span></span>
- <span data-ttu-id="ca964-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="ca964-166">GeneralPurpose</span></span>
- <span data-ttu-id="ca964-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="ca964-167">BusinessCritical</span></span>

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

### <span data-ttu-id="ca964-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ca964-168">-ElasticPoolName</span></span>
<span data-ttu-id="ca964-169">Especifica o nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="ca964-169">Specifies the name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca964-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ca964-170">-LicenseType</span></span>
<span data-ttu-id="ca964-171">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca964-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="ca964-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca964-172">-ResourceGroupName</span></span>
<span data-ttu-id="ca964-173">Especifica o nome do grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="ca964-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="ca964-174">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ca964-174">-ServerName</span></span>
<span data-ttu-id="ca964-175">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="ca964-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="ca964-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="ca964-176">-StorageMB</span></span>
<span data-ttu-id="ca964-177">Especifica o limite de armazenamento, em megabytes, para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="ca964-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="ca964-178">Para obter mais informações, consulte o cmdlet New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="ca964-178">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="ca964-179">-Marcas</span><span class="sxs-lookup"><span data-stu-id="ca964-179">-Tags</span></span>
<span data-ttu-id="ca964-180">Especifica um dicionário de pares de chave-valor que esse cmdlet associa ao pool elástico na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ca964-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="ca964-181">Por exemplo: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="ca964-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="ca964-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="ca964-182">-VCore</span></span>
<span data-ttu-id="ca964-183">O número total de partilhas de VCORE do pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ca964-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca964-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ca964-184">-ZoneRedundant</span></span>
<span data-ttu-id="ca964-185">A redundância de zona para associar ao pool elástico do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ca964-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="ca964-186">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca964-186">-Confirm</span></span>
<span data-ttu-id="ca964-187">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca964-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca964-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca964-188">-WhatIf</span></span>
<span data-ttu-id="ca964-189">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca964-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca964-190">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca964-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca964-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca964-191">CommonParameters</span></span>
<span data-ttu-id="ca964-192">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca964-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca964-193">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca964-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca964-194">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca964-194">INPUTS</span></span>

### <span data-ttu-id="ca964-195">System. String</span><span class="sxs-lookup"><span data-stu-id="ca964-195">System.String</span></span>

## <span data-ttu-id="ca964-196">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca964-196">OUTPUTS</span></span>

### <span data-ttu-id="ca964-197">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="ca964-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="ca964-198">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca964-198">NOTES</span></span>

## <span data-ttu-id="ca964-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca964-199">RELATED LINKS</span></span>

[<span data-ttu-id="ca964-200">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ca964-200">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ca964-201">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ca964-201">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="ca964-202">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ca964-202">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="ca964-203">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ca964-203">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ca964-204">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ca964-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
