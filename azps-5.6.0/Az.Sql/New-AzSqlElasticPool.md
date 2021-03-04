---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: d625e28b0007a9dc99434f0257a910ea804e3644
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887662"
---
# <span data-ttu-id="c1827-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c1827-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="c1827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1827-102">SYNOPSIS</span></span>
<span data-ttu-id="c1827-103">Cria um pool de banco de dados elástica para um banco de dados SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="c1827-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="c1827-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c1827-104">SYNTAX</span></span>

### <span data-ttu-id="c1827-105">DtuBasedPool (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c1827-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1827-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="c1827-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1827-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c1827-107">DESCRIPTION</span></span>
<span data-ttu-id="c1827-108">O cmdlet **New-AzSqlElasticPool** cria um pool de banco de dados elástica para um banco de dados do Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c1827-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="c1827-109">Vários parâmetros (*-Dtu, -DatabaseDtuMin e -DatabaseDtuMax*) exigem que o valor que está sendo definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c1827-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="c1827-110">Por exemplo, -DatabaseDtuMax para um pool EDTU Standard 100 só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="c1827-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="c1827-111">Para obter detalhes sobre quais valores são válidos, consulte a tabela para seu pool de tamanho específico em [pools elásticas](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="c1827-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="c1827-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1827-112">EXAMPLES</span></span>

### <span data-ttu-id="c1827-113">Exemplo 1: Criar um pool elástica de DTU</span><span class="sxs-lookup"><span data-stu-id="c1827-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="c1827-114">Este comando cria um pool elástica na camada de serviço Standard chamada ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="c1827-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="c1827-115">O servidor chamado server01, atribuído a um grupo de recursos do Azure chamado ResourceGroup01, hospeda o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="c1827-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="c1827-116">O comando especifica valores de propriedade DTU para o pool e os bancos de dados no pool.</span><span class="sxs-lookup"><span data-stu-id="c1827-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="c1827-117">Exemplo 2: Criar um pool elástica vCore</span><span class="sxs-lookup"><span data-stu-id="c1827-117">Example 2: Create a vCore elastic pool</span></span>

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

<span data-ttu-id="c1827-118">Este comando cria um pool elástica na camada de serviço GengeralPurpose chamada ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="c1827-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="c1827-119">O servidor chamado server01, atribuído a um grupo de recursos do Azure chamado ResourceGroup01, hospeda o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="c1827-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="c1827-120">O comando especifica os valores da propriedade vCore para o pool e os bancos de dados no pool.</span><span class="sxs-lookup"><span data-stu-id="c1827-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="c1827-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c1827-121">Example 3</span></span>

<span data-ttu-id="c1827-122">Cria um pool de banco de dados elástica para um banco de dados SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="c1827-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="c1827-123">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="c1827-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="c1827-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c1827-124">PARAMETERS</span></span>

### <span data-ttu-id="c1827-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1827-125">-AsJob</span></span>
<span data-ttu-id="c1827-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c1827-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1827-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c1827-127">-ComputeGeneration</span></span>
<span data-ttu-id="c1827-128">A geração de computação a ser atribuida.</span><span class="sxs-lookup"><span data-stu-id="c1827-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="c1827-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="c1827-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="c1827-130">Especifica o número máximo de DTUs (Unidades de Transferência de Banco de Dados) que qualquer banco de dados único no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="c1827-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="c1827-131">Os valores padrão para as diferentes edições são os seguinte:</span><span class="sxs-lookup"><span data-stu-id="c1827-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="c1827-132">Básico.</span><span class="sxs-lookup"><span data-stu-id="c1827-132">Basic.</span></span> <span data-ttu-id="c1827-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="c1827-133">5 DTUs</span></span>
- <span data-ttu-id="c1827-134">Padrão.</span><span class="sxs-lookup"><span data-stu-id="c1827-134">Standard.</span></span> <span data-ttu-id="c1827-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="c1827-135">100 DTUs</span></span>
- <span data-ttu-id="c1827-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="c1827-136">Premium.</span></span> <span data-ttu-id="c1827-137">125 DTUs Para obter detalhes sobre quais valores são válidos, consulte a tabela para o pool de tamanho específico em [pools elásticas](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="c1827-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="c1827-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="c1827-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="c1827-139">Especifica o número mínimo de DTUs que o pool elástica garante a todos os bancos de dados no pool.</span><span class="sxs-lookup"><span data-stu-id="c1827-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="c1827-140">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="c1827-140">The default value is zero (0).</span></span>
<span data-ttu-id="c1827-141">Para obter detalhes sobre quais valores são válidos, consulte a tabela para seu pool de tamanho específico em [pools elásticas](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="c1827-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="c1827-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="c1827-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="c1827-143">O número máximo de VCore que qualquer Banco de Dados sqlAzure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="c1827-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="c1827-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="c1827-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="c1827-145">O número mínimo de VCore que qualquer Banco de Dados sqlAzure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="c1827-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="c1827-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1827-146">-DefaultProfile</span></span>
<span data-ttu-id="c1827-147">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c1827-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1827-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="c1827-148">-Dtu</span></span>
<span data-ttu-id="c1827-149">Especifica o número total de DTUs compartilhados para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="c1827-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="c1827-150">Os valores padrão para as diferentes edições são os seguinte:</span><span class="sxs-lookup"><span data-stu-id="c1827-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="c1827-151">Básico.</span><span class="sxs-lookup"><span data-stu-id="c1827-151">Basic.</span></span>
<span data-ttu-id="c1827-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="c1827-152">100 DTUs</span></span>
- <span data-ttu-id="c1827-153">Padrão.</span><span class="sxs-lookup"><span data-stu-id="c1827-153">Standard.</span></span>
<span data-ttu-id="c1827-154">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="c1827-154">100 DTUs</span></span>
- <span data-ttu-id="c1827-155">Premium.</span><span class="sxs-lookup"><span data-stu-id="c1827-155">Premium.</span></span>
<span data-ttu-id="c1827-156">125 DTUs Para obter detalhes sobre quais valores são válidos, consulte a tabela para seu pool de tamanho específico em [pools elásticas](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="c1827-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="c1827-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="c1827-157">-Edition</span></span>
<span data-ttu-id="c1827-158">Especifica a edição do banco de dados do Azure SQL usado para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="c1827-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="c1827-159">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c1827-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c1827-160">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1827-160">None</span></span>
- <span data-ttu-id="c1827-161">Básico</span><span class="sxs-lookup"><span data-stu-id="c1827-161">Basic</span></span>
- <span data-ttu-id="c1827-162">Standard</span><span class="sxs-lookup"><span data-stu-id="c1827-162">Standard</span></span>
- <span data-ttu-id="c1827-163">Premium</span><span class="sxs-lookup"><span data-stu-id="c1827-163">Premium</span></span>
- <span data-ttu-id="c1827-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="c1827-164">DataWarehouse</span></span>
- <span data-ttu-id="c1827-165">Gratuito</span><span class="sxs-lookup"><span data-stu-id="c1827-165">Free</span></span>
- <span data-ttu-id="c1827-166">Stretch</span><span class="sxs-lookup"><span data-stu-id="c1827-166">Stretch</span></span>
- <span data-ttu-id="c1827-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="c1827-167">GeneralPurpose</span></span>
- <span data-ttu-id="c1827-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="c1827-168">BusinessCritical</span></span>

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

### <span data-ttu-id="c1827-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c1827-169">-ElasticPoolName</span></span>
<span data-ttu-id="c1827-170">Especifica o nome do pool elástica que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c1827-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c1827-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c1827-171">-LicenseType</span></span>
<span data-ttu-id="c1827-172">O tipo de licença para o banco de dados do Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="c1827-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="c1827-173">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c1827-173">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="c1827-174">A ID de configuração de manutenção do pool SQL Elastic.</span><span class="sxs-lookup"><span data-stu-id="c1827-174">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="c1827-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1827-175">-ResourceGroupName</span></span>
<span data-ttu-id="c1827-176">Especifica o nome do grupo de recursos ao qual este cmdlet atribui o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="c1827-176">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="c1827-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c1827-177">-ServerName</span></span>
<span data-ttu-id="c1827-178">Especifica o nome do servidor que hospeda o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="c1827-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="c1827-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="c1827-179">-StorageMB</span></span>
<span data-ttu-id="c1827-180">Especifica o limite de armazenamento, em megabytes, para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="c1827-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="c1827-181">Se você não especificar esse parâmetro, esse cmdlet calculará um valor que depende do valor do parâmetro *Dtu.*</span><span class="sxs-lookup"><span data-stu-id="c1827-181">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="c1827-182">Consulte [eDTU e limites de armazenamento para](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) ver os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="c1827-182">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="c1827-183">-Tags</span><span class="sxs-lookup"><span data-stu-id="c1827-183">-Tags</span></span>
<span data-ttu-id="c1827-184">Especifica um dicionário de pares de valores-chave na forma de uma tabela de hash que esse cmdlet associa ao pool elástica.</span><span class="sxs-lookup"><span data-stu-id="c1827-184">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="c1827-185">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c1827-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c1827-186">-VCore</span><span class="sxs-lookup"><span data-stu-id="c1827-186">-VCore</span></span>
<span data-ttu-id="c1827-187">O número total compartilhado de Vcores para o Pool Elástica do Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="c1827-187">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="c1827-188">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="c1827-188">-ZoneRedundant</span></span>
<span data-ttu-id="c1827-189">A redundância de zona a ser associada ao Pool Elástica do Azure Sql</span><span class="sxs-lookup"><span data-stu-id="c1827-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="c1827-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1827-190">-Confirm</span></span>
<span data-ttu-id="c1827-191">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1827-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1827-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1827-192">-WhatIf</span></span>
<span data-ttu-id="c1827-193">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1827-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1827-194">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1827-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1827-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1827-195">CommonParameters</span></span>
<span data-ttu-id="c1827-196">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1827-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1827-197">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1827-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1827-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1827-198">INPUTS</span></span>

### <span data-ttu-id="c1827-199">System.String</span><span class="sxs-lookup"><span data-stu-id="c1827-199">System.String</span></span>

## <span data-ttu-id="c1827-200">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c1827-200">OUTPUTS</span></span>

### <span data-ttu-id="c1827-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="c1827-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="c1827-202">NOTES</span><span class="sxs-lookup"><span data-stu-id="c1827-202">NOTES</span></span>

## <span data-ttu-id="c1827-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1827-203">RELATED LINKS</span></span>

[<span data-ttu-id="c1827-204">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c1827-204">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="c1827-205">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c1827-205">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="c1827-206">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="c1827-206">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="c1827-207">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c1827-207">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="c1827-208">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c1827-208">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="c1827-209">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="c1827-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
