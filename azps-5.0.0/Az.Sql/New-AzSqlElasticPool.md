---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fed3f32f5ff0a9920b87438b75cb25cee7c9217
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116673"
---
# <span data-ttu-id="2683b-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2683b-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="2683b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2683b-102">SYNOPSIS</span></span>
<span data-ttu-id="2683b-103">Cria um pool de banco de dados elástico para um banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="2683b-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="2683b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2683b-104">SYNTAX</span></span>

### <span data-ttu-id="2683b-105">DtuBasedPool (padrão)</span><span class="sxs-lookup"><span data-stu-id="2683b-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2683b-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="2683b-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2683b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2683b-107">DESCRIPTION</span></span>
<span data-ttu-id="2683b-108">O cmdlet **New-AzSqlElasticPool** cria um pool de banco de dados elástico para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2683b-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="2683b-109">Vários parâmetros ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) exigem que o valor definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2683b-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="2683b-110">Por exemplo,-DatabaseDtuMax para um pool de eDTU de 100 padrão só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="2683b-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="2683b-111">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="2683b-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="2683b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2683b-112">EXAMPLES</span></span>

### <span data-ttu-id="2683b-113">Exemplo 1: criar um pool elástico de DTU</span><span class="sxs-lookup"><span data-stu-id="2683b-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
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

<span data-ttu-id="2683b-114">Esse comando cria um pool elástico na camada de serviço padrão chamada ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="2683b-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="2683b-115">O servidor chamado Server01, atribuído a um grupo de recursos do Azure chamado ResourceGroup01, hospeda o pool elástico no.</span><span class="sxs-lookup"><span data-stu-id="2683b-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="2683b-116">O comando especifica os valores da propriedade DTU para o pool e os bancos de dados no pool.</span><span class="sxs-lookup"><span data-stu-id="2683b-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="2683b-117">Exemplo 2: criar um pool elástico vCore</span><span class="sxs-lookup"><span data-stu-id="2683b-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                :
```

<span data-ttu-id="2683b-118">Esse comando cria um pool elástico na camada de serviço GengeralPurpose chamada ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="2683b-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="2683b-119">O servidor chamado Server01, atribuído a um grupo de recursos do Azure chamado ResourceGroup01, hospeda o pool elástico no.</span><span class="sxs-lookup"><span data-stu-id="2683b-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="2683b-120">O comando especifica os valores de propriedade vCore para o pool e os bancos de dados no pool.</span><span class="sxs-lookup"><span data-stu-id="2683b-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="2683b-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2683b-121">Example 3</span></span>

<span data-ttu-id="2683b-122">Cria um pool de banco de dados elástico para um banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="2683b-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="2683b-123">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="2683b-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="2683b-124">OS</span><span class="sxs-lookup"><span data-stu-id="2683b-124">PARAMETERS</span></span>

### <span data-ttu-id="2683b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2683b-125">-AsJob</span></span>
<span data-ttu-id="2683b-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2683b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2683b-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2683b-127">-ComputeGeneration</span></span>
<span data-ttu-id="2683b-128">A geração de computação a ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="2683b-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="2683b-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="2683b-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="2683b-130">Especifica o número máximo de unidades de produtividade do banco de dados (DTUs) que qualquer único banco de dados no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="2683b-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="2683b-131">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="2683b-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="2683b-132">Basic.</span><span class="sxs-lookup"><span data-stu-id="2683b-132">Basic.</span></span> <span data-ttu-id="2683b-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="2683b-133">5 DTUs</span></span>
- <span data-ttu-id="2683b-134">Oficial.</span><span class="sxs-lookup"><span data-stu-id="2683b-134">Standard.</span></span> <span data-ttu-id="2683b-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="2683b-135">100 DTUs</span></span>
- <span data-ttu-id="2683b-136">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="2683b-136">Premium.</span></span> <span data-ttu-id="2683b-137">125 DTUs para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="2683b-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="2683b-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="2683b-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="2683b-139">Especifica o número mínimo de DTUs que o pool elástico garante para todos os bancos de dados do pool.</span><span class="sxs-lookup"><span data-stu-id="2683b-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="2683b-140">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="2683b-140">The default value is zero (0).</span></span>
<span data-ttu-id="2683b-141">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="2683b-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="2683b-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="2683b-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="2683b-143">O número máximo de VCore que qualquer banco de dados sqlazure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="2683b-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="2683b-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="2683b-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="2683b-145">O número mínimo de VCore que qualquer banco de dados sqlazure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="2683b-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="2683b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2683b-146">-DefaultProfile</span></span>
<span data-ttu-id="2683b-147">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2683b-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2683b-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="2683b-148">-Dtu</span></span>
<span data-ttu-id="2683b-149">Especifica o número total de DTUs compartilhadas para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="2683b-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="2683b-150">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="2683b-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="2683b-151">Basic.</span><span class="sxs-lookup"><span data-stu-id="2683b-151">Basic.</span></span>
<span data-ttu-id="2683b-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="2683b-152">100 DTUs</span></span>
- <span data-ttu-id="2683b-153">Oficial.</span><span class="sxs-lookup"><span data-stu-id="2683b-153">Standard.</span></span>
<span data-ttu-id="2683b-154">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="2683b-154">100 DTUs</span></span>
- <span data-ttu-id="2683b-155">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="2683b-155">Premium.</span></span>
<span data-ttu-id="2683b-156">125 DTUs para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="2683b-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="2683b-157">-Edição</span><span class="sxs-lookup"><span data-stu-id="2683b-157">-Edition</span></span>
<span data-ttu-id="2683b-158">Especifica a edição do banco de dados SQL do Azure usado para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="2683b-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="2683b-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2683b-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2683b-160">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2683b-160">None</span></span>
- <span data-ttu-id="2683b-161">Basic</span><span class="sxs-lookup"><span data-stu-id="2683b-161">Basic</span></span>
- <span data-ttu-id="2683b-162">Oficial</span><span class="sxs-lookup"><span data-stu-id="2683b-162">Standard</span></span>
- <span data-ttu-id="2683b-163">Gratifica</span><span class="sxs-lookup"><span data-stu-id="2683b-163">Premium</span></span>
- <span data-ttu-id="2683b-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="2683b-164">DataWarehouse</span></span>
- <span data-ttu-id="2683b-165">Gratuito</span><span class="sxs-lookup"><span data-stu-id="2683b-165">Free</span></span>
- <span data-ttu-id="2683b-166">Automático</span><span class="sxs-lookup"><span data-stu-id="2683b-166">Stretch</span></span>
- <span data-ttu-id="2683b-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="2683b-167">GeneralPurpose</span></span>
- <span data-ttu-id="2683b-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="2683b-168">BusinessCritical</span></span>

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

### <span data-ttu-id="2683b-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2683b-169">-ElasticPoolName</span></span>
<span data-ttu-id="2683b-170">Especifica o nome do pool elástico que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="2683b-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2683b-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2683b-171">-LicenseType</span></span>
<span data-ttu-id="2683b-172">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2683b-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="2683b-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2683b-173">-ResourceGroupName</span></span>
<span data-ttu-id="2683b-174">Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="2683b-174">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="2683b-175">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2683b-175">-ServerName</span></span>
<span data-ttu-id="2683b-176">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="2683b-176">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="2683b-177">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="2683b-177">-StorageMB</span></span>
<span data-ttu-id="2683b-178">Especifica o limite de armazenamento, em megabytes, para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="2683b-178">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="2683b-179">Se você não especificar esse parâmetro, esse cmdlet calculará um valor que depende do valor do parâmetro *DTU* .</span><span class="sxs-lookup"><span data-stu-id="2683b-179">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="2683b-180">Veja [os limites de eDTU e armazenamento](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) para os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="2683b-180">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="2683b-181">-Marcas</span><span class="sxs-lookup"><span data-stu-id="2683b-181">-Tags</span></span>
<span data-ttu-id="2683b-182">Especifica um dicionário de pares de chave-valor na forma de uma tabela de hash que este cmdlet associa ao pool elástico.</span><span class="sxs-lookup"><span data-stu-id="2683b-182">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="2683b-183">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2683b-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2683b-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="2683b-184">-VCore</span></span>
<span data-ttu-id="2683b-185">O número total compartilhado de Vcores para o pool elástico do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2683b-185">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="2683b-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="2683b-186">-ZoneRedundant</span></span>
<span data-ttu-id="2683b-187">A redundância de zona para associar ao pool elástico do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="2683b-187">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="2683b-188">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2683b-188">-Confirm</span></span>
<span data-ttu-id="2683b-189">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2683b-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2683b-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2683b-190">-WhatIf</span></span>
<span data-ttu-id="2683b-191">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2683b-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2683b-192">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2683b-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2683b-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2683b-193">CommonParameters</span></span>
<span data-ttu-id="2683b-194">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2683b-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2683b-195">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2683b-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2683b-196">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2683b-196">INPUTS</span></span>

### <span data-ttu-id="2683b-197">System. String</span><span class="sxs-lookup"><span data-stu-id="2683b-197">System.String</span></span>

## <span data-ttu-id="2683b-198">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2683b-198">OUTPUTS</span></span>

### <span data-ttu-id="2683b-199">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="2683b-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="2683b-200">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2683b-200">NOTES</span></span>

## <span data-ttu-id="2683b-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2683b-201">RELATED LINKS</span></span>

[<span data-ttu-id="2683b-202">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2683b-202">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="2683b-203">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2683b-203">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="2683b-204">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2683b-204">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="2683b-205">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2683b-205">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="2683b-206">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2683b-206">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="2683b-207">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="2683b-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
