---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124738"
---
# <span data-ttu-id="7178a-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7178a-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="7178a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7178a-102">SYNOPSIS</span></span>
<span data-ttu-id="7178a-103">Modifica as propriedades de um pool de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7178a-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="7178a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7178a-104">SYNTAX</span></span>

### <span data-ttu-id="7178a-105">DtuBasedPool (padrão)</span><span class="sxs-lookup"><span data-stu-id="7178a-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7178a-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="7178a-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7178a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7178a-107">DESCRIPTION</span></span>
<span data-ttu-id="7178a-108">O cmdlet **set-AzSqlElasticPool** define propriedades para um pool elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7178a-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="7178a-109">Esse cmdlet pode modificar o eDTUs por pool ( *DTU* ), o tamanho máximo de armazenamento por pool ( *StorageMB* ), o máximo eDTUs por banco de dados ( *DatabaseDtuMax* ) e o mínimo de EDTUs por banco de dados ( *DatabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="7178a-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="7178a-110">Vários parâmetros ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) exigem que o valor definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7178a-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="7178a-111">Por exemplo,-DatabaseDtuMax para um pool de eDTU de 100 padrão só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="7178a-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="7178a-112">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="7178a-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="7178a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7178a-113">EXAMPLES</span></span>

### <span data-ttu-id="7178a-114">Exemplo 1: modificar as propriedades de um pool elástico</span><span class="sxs-lookup"><span data-stu-id="7178a-114">Example 1: Modify properties for an elastic pool</span></span>
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="7178a-115">Esse comando modifica as propriedades de um pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="7178a-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="7178a-116">O comando define o número de DTUs para o pool elástico para 1000 e define as DTUs mínima e máxima.</span><span class="sxs-lookup"><span data-stu-id="7178a-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="7178a-117">Exemplo 2: modificar o tamanho máximo de armazenamento de um pool elástico</span><span class="sxs-lookup"><span data-stu-id="7178a-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="7178a-118">Esse comando modifica as propriedades de um pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="7178a-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="7178a-119">O comando define o armazenamento máximo para um pool elástico para 2 TB.</span><span class="sxs-lookup"><span data-stu-id="7178a-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="7178a-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7178a-120">Example 3</span></span>

<span data-ttu-id="7178a-121">Modifica as propriedades de um pool de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7178a-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="7178a-122">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="7178a-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="7178a-123">OS</span><span class="sxs-lookup"><span data-stu-id="7178a-123">PARAMETERS</span></span>

### <span data-ttu-id="7178a-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7178a-124">-AsJob</span></span>
<span data-ttu-id="7178a-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7178a-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7178a-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="7178a-126">-ComputeGeneration</span></span>
<span data-ttu-id="7178a-127">A geração de computação a ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="7178a-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="7178a-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="7178a-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="7178a-129">Especifica o número máximo de DTUs que qualquer único banco de dados no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="7178a-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="7178a-130">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="7178a-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="7178a-131">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7178a-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="7178a-132">Basic.</span><span class="sxs-lookup"><span data-stu-id="7178a-132">Basic.</span></span>  <span data-ttu-id="7178a-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="7178a-133">5 DTUs</span></span>
- <span data-ttu-id="7178a-134">Oficial.</span><span class="sxs-lookup"><span data-stu-id="7178a-134">Standard.</span></span> <span data-ttu-id="7178a-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="7178a-135">100 DTUs</span></span>
- <span data-ttu-id="7178a-136">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="7178a-136">Premium.</span></span> <span data-ttu-id="7178a-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="7178a-137">125 DTUs</span></span>

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

### <span data-ttu-id="7178a-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="7178a-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="7178a-139">Especifica o número mínimo de DTUs que o pool elástico garante para todos os bancos de dados do pool.</span><span class="sxs-lookup"><span data-stu-id="7178a-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="7178a-140">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="7178a-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="7178a-141">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="7178a-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="7178a-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="7178a-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="7178a-143">O número máximo de VCore que qualquer banco de dados sqlazure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="7178a-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="7178a-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="7178a-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="7178a-145">O número mínimo de VCore que qualquer banco de dados sqlazure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="7178a-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="7178a-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7178a-146">-DefaultProfile</span></span>
<span data-ttu-id="7178a-147">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7178a-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7178a-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="7178a-148">-Dtu</span></span>
<span data-ttu-id="7178a-149">Especifica o número total de DTUs compartilhadas para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="7178a-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="7178a-150">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="7178a-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="7178a-151">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7178a-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="7178a-152">Basic.</span><span class="sxs-lookup"><span data-stu-id="7178a-152">Basic.</span></span> <span data-ttu-id="7178a-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="7178a-153">100 DTUs</span></span>
- <span data-ttu-id="7178a-154">Oficial.</span><span class="sxs-lookup"><span data-stu-id="7178a-154">Standard.</span></span> <span data-ttu-id="7178a-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="7178a-155">100 DTUs</span></span>
- <span data-ttu-id="7178a-156">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="7178a-156">Premium.</span></span> <span data-ttu-id="7178a-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="7178a-157">125 DTUs</span></span>

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

### <span data-ttu-id="7178a-158">-Edição</span><span class="sxs-lookup"><span data-stu-id="7178a-158">-Edition</span></span>
<span data-ttu-id="7178a-159">Especifica a edição do banco de dados SQL do Azure para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="7178a-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="7178a-160">Não é possível alterar a edição.</span><span class="sxs-lookup"><span data-stu-id="7178a-160">You cannot change the edition.</span></span> <span data-ttu-id="7178a-161">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7178a-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7178a-162">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7178a-162">None</span></span>
- <span data-ttu-id="7178a-163">Basic</span><span class="sxs-lookup"><span data-stu-id="7178a-163">Basic</span></span>
- <span data-ttu-id="7178a-164">Oficial</span><span class="sxs-lookup"><span data-stu-id="7178a-164">Standard</span></span>
- <span data-ttu-id="7178a-165">Gratifica</span><span class="sxs-lookup"><span data-stu-id="7178a-165">Premium</span></span>
- <span data-ttu-id="7178a-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="7178a-166">DataWarehouse</span></span>
- <span data-ttu-id="7178a-167">Gratuito</span><span class="sxs-lookup"><span data-stu-id="7178a-167">Free</span></span>
- <span data-ttu-id="7178a-168">Automático</span><span class="sxs-lookup"><span data-stu-id="7178a-168">Stretch</span></span>
- <span data-ttu-id="7178a-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="7178a-169">GeneralPurpose</span></span>
- <span data-ttu-id="7178a-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="7178a-170">BusinessCritical</span></span>

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

### <span data-ttu-id="7178a-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7178a-171">-ElasticPoolName</span></span>
<span data-ttu-id="7178a-172">Especifica o nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="7178a-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="7178a-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7178a-173">-LicenseType</span></span>
<span data-ttu-id="7178a-174">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7178a-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="7178a-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7178a-175">-ResourceGroupName</span></span>
<span data-ttu-id="7178a-176">Especifica o nome do grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7178a-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="7178a-177">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7178a-177">-ServerName</span></span>
<span data-ttu-id="7178a-178">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="7178a-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="7178a-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="7178a-179">-StorageMB</span></span>
<span data-ttu-id="7178a-180">Especifica o limite de armazenamento, em megabytes, para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="7178a-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="7178a-181">Para obter mais informações, consulte o cmdlet New-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="7178a-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="7178a-182">-Marcas</span><span class="sxs-lookup"><span data-stu-id="7178a-182">-Tags</span></span>
<span data-ttu-id="7178a-183">Especifica um dicionário de pares de chave-valor que esse cmdlet associa ao pool elástico na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7178a-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="7178a-184">Por exemplo: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="7178a-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="7178a-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="7178a-185">-VCore</span></span>
<span data-ttu-id="7178a-186">O número total de partilhas de VCORE do pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7178a-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="7178a-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7178a-187">-ZoneRedundant</span></span>
<span data-ttu-id="7178a-188">A redundância de zona para associar ao pool elástico do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="7178a-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="7178a-189">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7178a-189">-Confirm</span></span>
<span data-ttu-id="7178a-190">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7178a-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7178a-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7178a-191">-WhatIf</span></span>
<span data-ttu-id="7178a-192">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7178a-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7178a-193">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7178a-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7178a-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7178a-194">CommonParameters</span></span>
<span data-ttu-id="7178a-195">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7178a-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7178a-196">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7178a-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7178a-197">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7178a-197">INPUTS</span></span>

### <span data-ttu-id="7178a-198">System. String</span><span class="sxs-lookup"><span data-stu-id="7178a-198">System.String</span></span>

## <span data-ttu-id="7178a-199">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7178a-199">OUTPUTS</span></span>

### <span data-ttu-id="7178a-200">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="7178a-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="7178a-201">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7178a-201">NOTES</span></span>

## <span data-ttu-id="7178a-202">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7178a-202">RELATED LINKS</span></span>

[<span data-ttu-id="7178a-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7178a-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="7178a-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7178a-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="7178a-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="7178a-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="7178a-206">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7178a-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="7178a-207">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7178a-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
