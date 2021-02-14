---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: a420a7edf1d5fb7133087c5ecb9fcf605cbdddf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110906"
---
# <span data-ttu-id="b26f6-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b26f6-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="b26f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b26f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b26f6-103">Modifica as propriedades de um pool de banco de dados elástica no Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b26f6-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="b26f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b26f6-104">SYNTAX</span></span>

### <span data-ttu-id="b26f6-105">DtuBasedPool (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b26f6-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26f6-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="b26f6-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b26f6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b26f6-107">DESCRIPTION</span></span>
<span data-ttu-id="b26f6-108">O cmdlet **Set-AzSqlElasticPool** define propriedades para um pool elástica no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b26f6-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="b26f6-109">Esse cmdlet pode modificar os eDTUs por pool *(Dtu),* o tamanho máximo de armazenamento por pool *(StorageMB),* o máximo eDTUs por banco de dados (*DatabaseDtuMax)* e os eDTUs mínimos por banco de dados (*DatabaseDtuMin).*</span><span class="sxs-lookup"><span data-stu-id="b26f6-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="b26f6-110">Vários parâmetros (*-Dtu, -DatabaseDtuMin e -DatabaseDtuMax)* exigem que o valor que está sendo definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b26f6-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="b26f6-111">Por exemplo, -DatabaseDtuMax para um pool eDTU Padrão 100 só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="b26f6-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="b26f6-112">Para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticas.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b26f6-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="b26f6-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b26f6-113">EXAMPLES</span></span>

### <span data-ttu-id="b26f6-114">Exemplo 1: Modificar propriedades para um pool elástica</span><span class="sxs-lookup"><span data-stu-id="b26f6-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="b26f6-115">Esse comando modifica as propriedades de um pool elástica chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="b26f6-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="b26f6-116">O comando define o número de DTUs para o pool elástica como 1000 e define as DTUs mínima e máxima.</span><span class="sxs-lookup"><span data-stu-id="b26f6-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="b26f6-117">Exemplo 2: modificar o tamanho máximo de armazenamento de um pool elástica</span><span class="sxs-lookup"><span data-stu-id="b26f6-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="b26f6-118">Esse comando modifica as propriedades de um pool elástica chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="b26f6-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="b26f6-119">O comando define o armazenamento máximo de um pool elástica para 2 TB.</span><span class="sxs-lookup"><span data-stu-id="b26f6-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="b26f6-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b26f6-120">Example 3</span></span>

<span data-ttu-id="b26f6-121">Modifica as propriedades de um pool de banco de dados elástica no Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b26f6-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="b26f6-122">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="b26f6-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="b26f6-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b26f6-123">PARAMETERS</span></span>

### <span data-ttu-id="b26f6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b26f6-124">-AsJob</span></span>
<span data-ttu-id="b26f6-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b26f6-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b26f6-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b26f6-126">-ComputeGeneration</span></span>
<span data-ttu-id="b26f6-127">A geração de computação a ser atribuir.</span><span class="sxs-lookup"><span data-stu-id="b26f6-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="b26f6-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="b26f6-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="b26f6-129">Especifica o número máximo de DTUs que qualquer banco de dados único no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="b26f6-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="b26f6-130">Para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticas.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b26f6-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="b26f6-131">Os valores padrão para edições diferentes são os mesmos:</span><span class="sxs-lookup"><span data-stu-id="b26f6-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="b26f6-132">Basic.</span><span class="sxs-lookup"><span data-stu-id="b26f6-132">Basic.</span></span>  <span data-ttu-id="b26f6-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="b26f6-133">5 DTUs</span></span>
- <span data-ttu-id="b26f6-134">Padrão.</span><span class="sxs-lookup"><span data-stu-id="b26f6-134">Standard.</span></span> <span data-ttu-id="b26f6-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="b26f6-135">100 DTUs</span></span>
- <span data-ttu-id="b26f6-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="b26f6-136">Premium.</span></span> <span data-ttu-id="b26f6-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="b26f6-137">125 DTUs</span></span>

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

### <span data-ttu-id="b26f6-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="b26f6-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="b26f6-139">Especifica o número mínimo de DTUs que o pool elástica garante a todos os bancos de dados do pool.</span><span class="sxs-lookup"><span data-stu-id="b26f6-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="b26f6-140">Para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticas.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b26f6-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="b26f6-141">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="b26f6-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="b26f6-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="b26f6-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="b26f6-143">O número máximo de VCore que qualquer Banco de Dados do SqlAzure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="b26f6-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="b26f6-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="b26f6-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="b26f6-145">O número mínimo de VCore que qualquer Banco de Dados sqlAzure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="b26f6-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="b26f6-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26f6-146">-DefaultProfile</span></span>
<span data-ttu-id="b26f6-147">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b26f6-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b26f6-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="b26f6-148">-Dtu</span></span>
<span data-ttu-id="b26f6-149">Especifica o número total de DTUs compartilhadas para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="b26f6-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="b26f6-150">Para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticas.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b26f6-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="b26f6-151">Os valores padrão para edições diferentes são os mesmos:</span><span class="sxs-lookup"><span data-stu-id="b26f6-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="b26f6-152">Basic.</span><span class="sxs-lookup"><span data-stu-id="b26f6-152">Basic.</span></span> <span data-ttu-id="b26f6-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="b26f6-153">100 DTUs</span></span>
- <span data-ttu-id="b26f6-154">Padrão.</span><span class="sxs-lookup"><span data-stu-id="b26f6-154">Standard.</span></span> <span data-ttu-id="b26f6-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="b26f6-155">100 DTUs</span></span>
- <span data-ttu-id="b26f6-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="b26f6-156">Premium.</span></span> <span data-ttu-id="b26f6-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="b26f6-157">125 DTUs</span></span>

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

### <span data-ttu-id="b26f6-158">-Edição</span><span class="sxs-lookup"><span data-stu-id="b26f6-158">-Edition</span></span>
<span data-ttu-id="b26f6-159">Especifica a edição do Banco de Dados SQL do Azure para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="b26f6-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="b26f6-160">Não é possível alterar a edição.</span><span class="sxs-lookup"><span data-stu-id="b26f6-160">You cannot change the edition.</span></span> <span data-ttu-id="b26f6-161">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b26f6-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b26f6-162">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b26f6-162">None</span></span>
- <span data-ttu-id="b26f6-163">Basic</span><span class="sxs-lookup"><span data-stu-id="b26f6-163">Basic</span></span>
- <span data-ttu-id="b26f6-164">Padrão</span><span class="sxs-lookup"><span data-stu-id="b26f6-164">Standard</span></span>
- <span data-ttu-id="b26f6-165">Premium</span><span class="sxs-lookup"><span data-stu-id="b26f6-165">Premium</span></span>
- <span data-ttu-id="b26f6-166">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="b26f6-166">DataWarehouse</span></span>
- <span data-ttu-id="b26f6-167">Livre</span><span class="sxs-lookup"><span data-stu-id="b26f6-167">Free</span></span>
- <span data-ttu-id="b26f6-168">Esticar</span><span class="sxs-lookup"><span data-stu-id="b26f6-168">Stretch</span></span>
- <span data-ttu-id="b26f6-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="b26f6-169">GeneralPurpose</span></span>
- <span data-ttu-id="b26f6-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="b26f6-170">BusinessCritical</span></span>

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

### <span data-ttu-id="b26f6-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b26f6-171">-ElasticPoolName</span></span>
<span data-ttu-id="b26f6-172">Especifica o nome do pool elástica.</span><span class="sxs-lookup"><span data-stu-id="b26f6-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="b26f6-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b26f6-173">-LicenseType</span></span>
<span data-ttu-id="b26f6-174">O tipo de licença do banco de dados Sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="b26f6-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="b26f6-175">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b26f6-175">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="b26f6-176">A ID de configuração de manutenção do Pool Elástica SQL.</span><span class="sxs-lookup"><span data-stu-id="b26f6-176">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="b26f6-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26f6-177">-ResourceGroupName</span></span>
<span data-ttu-id="b26f6-178">Especifica o nome do grupo de recursos ao qual o pool elástica é atribuído.</span><span class="sxs-lookup"><span data-stu-id="b26f6-178">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="b26f6-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b26f6-179">-ServerName</span></span>
<span data-ttu-id="b26f6-180">Especifica o nome do servidor que hospeda o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="b26f6-180">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="b26f6-181">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="b26f6-181">-StorageMB</span></span>
<span data-ttu-id="b26f6-182">Especifica o limite de armazenamento, em megabytes, para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="b26f6-182">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="b26f6-183">Para obter mais informações, consulte o New-AzSqlElasticPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b26f6-183">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="b26f6-184">-Marcas</span><span class="sxs-lookup"><span data-stu-id="b26f6-184">-Tags</span></span>
<span data-ttu-id="b26f6-185">Especifica um dicionário de pares de valor-chave que este cmdlet associa ao pool elástica na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="b26f6-185">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="b26f6-186">Por exemplo: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="b26f6-186">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="b26f6-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="b26f6-187">-VCore</span></span>
<span data-ttu-id="b26f6-188">O número total compartilhado de Vcore para o Pool Elástica do Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="b26f6-188">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="b26f6-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b26f6-189">-ZoneRedundant</span></span>
<span data-ttu-id="b26f6-190">Redundância de zona a ser associada ao Pool Elástica sql do Azure</span><span class="sxs-lookup"><span data-stu-id="b26f6-190">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="b26f6-191">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b26f6-191">-Confirm</span></span>
<span data-ttu-id="b26f6-192">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b26f6-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b26f6-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b26f6-193">-WhatIf</span></span>
<span data-ttu-id="b26f6-194">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b26f6-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b26f6-195">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b26f6-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b26f6-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26f6-196">CommonParameters</span></span>
<span data-ttu-id="b26f6-197">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26f6-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26f6-198">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b26f6-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26f6-199">Entradas</span><span class="sxs-lookup"><span data-stu-id="b26f6-199">INPUTS</span></span>

### <span data-ttu-id="b26f6-200">System.String</span><span class="sxs-lookup"><span data-stu-id="b26f6-200">System.String</span></span>

## <span data-ttu-id="b26f6-201">Saídas</span><span class="sxs-lookup"><span data-stu-id="b26f6-201">OUTPUTS</span></span>

### <span data-ttu-id="b26f6-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="b26f6-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="b26f6-203">Notas</span><span class="sxs-lookup"><span data-stu-id="b26f6-203">NOTES</span></span>

## <span data-ttu-id="b26f6-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b26f6-204">RELATED LINKS</span></span>

[<span data-ttu-id="b26f6-205">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b26f6-205">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="b26f6-206">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="b26f6-206">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="b26f6-207">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="b26f6-207">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="b26f6-208">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b26f6-208">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="b26f6-209">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b26f6-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
