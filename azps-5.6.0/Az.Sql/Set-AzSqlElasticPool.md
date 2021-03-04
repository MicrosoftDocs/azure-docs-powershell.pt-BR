---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: 564bd475b8574f30f8d00cc1a374bc11b4a93ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886836"
---
# <span data-ttu-id="79f1a-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="79f1a-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="79f1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="79f1a-103">Modifica as propriedades de um pool de banco de dados elástica no Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79f1a-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="79f1a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="79f1a-104">SYNTAX</span></span>

### <span data-ttu-id="79f1a-105">DtuBasedPool (Padrão)</span><span class="sxs-lookup"><span data-stu-id="79f1a-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79f1a-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="79f1a-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79f1a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="79f1a-107">DESCRIPTION</span></span>
<span data-ttu-id="79f1a-108">O cmdlet **Set-AzSqlElasticPool** define propriedades para um pool elástica no Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79f1a-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="79f1a-109">Este cmdlet pode modificar os eDTUs por pool (*Dtu*), tamanho máximo de armazenamento por pool (*StorageMB*), máximo eDTUs por banco de dados (*DatabaseDtuMax*) e eDTUs mínimo por banco de dados (*DatabaseDtuMin*).</span><span class="sxs-lookup"><span data-stu-id="79f1a-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="79f1a-110">Vários parâmetros (*-Dtu, -DatabaseDtuMin e -DatabaseDtuMax*) exigem que o valor que está sendo definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="79f1a-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="79f1a-111">Por exemplo, -DatabaseDtuMax para um pool EDTU Standard 100 só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="79f1a-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="79f1a-112">Para obter detalhes sobre quais valores são válidos, consulte a tabela para seu pool de tamanho específico em [pools elásticas](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="79f1a-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="79f1a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79f1a-113">EXAMPLES</span></span>

### <span data-ttu-id="79f1a-114">Exemplo 1: Modificar propriedades para um pool elástica</span><span class="sxs-lookup"><span data-stu-id="79f1a-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="79f1a-115">Este comando modifica propriedades para um pool elástica chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="79f1a-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="79f1a-116">O comando define o número de DTUs para o pool elástica como 1000 e define as DTUs mínimas e máximas.</span><span class="sxs-lookup"><span data-stu-id="79f1a-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="79f1a-117">Exemplo 2: Modificar o tamanho máximo de armazenamento de um pool elástica</span><span class="sxs-lookup"><span data-stu-id="79f1a-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="79f1a-118">Este comando modifica propriedades para um pool elástica chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="79f1a-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="79f1a-119">O comando define o armazenamento máximo de um pool elástica como 2 TB.</span><span class="sxs-lookup"><span data-stu-id="79f1a-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="79f1a-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="79f1a-120">Example 3</span></span>

<span data-ttu-id="79f1a-121">Modifica as propriedades de um pool de banco de dados elástica no Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79f1a-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="79f1a-122">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="79f1a-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="79f1a-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="79f1a-123">PARAMETERS</span></span>

### <span data-ttu-id="79f1a-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79f1a-124">-AsJob</span></span>
<span data-ttu-id="79f1a-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="79f1a-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79f1a-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="79f1a-126">-ComputeGeneration</span></span>
<span data-ttu-id="79f1a-127">A geração de computação a ser atribuida.</span><span class="sxs-lookup"><span data-stu-id="79f1a-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="79f1a-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="79f1a-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="79f1a-129">Especifica o número máximo de DTUs que qualquer banco de dados único no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="79f1a-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="79f1a-130">Para obter detalhes sobre quais valores são válidos, consulte a tabela para seu pool de tamanho específico em [pools elásticas](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="79f1a-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="79f1a-131">Os valores padrão para edições diferentes são os seguinte:</span><span class="sxs-lookup"><span data-stu-id="79f1a-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="79f1a-132">Básico.</span><span class="sxs-lookup"><span data-stu-id="79f1a-132">Basic.</span></span>  <span data-ttu-id="79f1a-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="79f1a-133">5 DTUs</span></span>
- <span data-ttu-id="79f1a-134">Padrão.</span><span class="sxs-lookup"><span data-stu-id="79f1a-134">Standard.</span></span> <span data-ttu-id="79f1a-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="79f1a-135">100 DTUs</span></span>
- <span data-ttu-id="79f1a-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="79f1a-136">Premium.</span></span> <span data-ttu-id="79f1a-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="79f1a-137">125 DTUs</span></span>

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

### <span data-ttu-id="79f1a-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="79f1a-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="79f1a-139">Especifica o número mínimo de DTUs que o pool elástica garante a todos os bancos de dados no pool.</span><span class="sxs-lookup"><span data-stu-id="79f1a-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="79f1a-140">Para obter detalhes sobre quais valores são válidos, consulte a tabela para seu pool de tamanho específico em [pools elásticas](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="79f1a-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="79f1a-141">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="79f1a-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="79f1a-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="79f1a-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="79f1a-143">O número máximo de VCore que qualquer Banco de Dados sqlAzure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="79f1a-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="79f1a-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="79f1a-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="79f1a-145">O número mínimo de VCore que qualquer Banco de Dados sqlAzure pode consumir no pool.</span><span class="sxs-lookup"><span data-stu-id="79f1a-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="79f1a-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f1a-146">-DefaultProfile</span></span>
<span data-ttu-id="79f1a-147">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="79f1a-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79f1a-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="79f1a-148">-Dtu</span></span>
<span data-ttu-id="79f1a-149">Especifica o número total de DTUs compartilhados para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="79f1a-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="79f1a-150">Para obter detalhes sobre quais valores são válidos, consulte a tabela para seu pool de tamanho específico em [pools elásticas](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="79f1a-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="79f1a-151">Os valores padrão para edições diferentes são os seguinte:</span><span class="sxs-lookup"><span data-stu-id="79f1a-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="79f1a-152">Básico.</span><span class="sxs-lookup"><span data-stu-id="79f1a-152">Basic.</span></span> <span data-ttu-id="79f1a-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="79f1a-153">100 DTUs</span></span>
- <span data-ttu-id="79f1a-154">Padrão.</span><span class="sxs-lookup"><span data-stu-id="79f1a-154">Standard.</span></span> <span data-ttu-id="79f1a-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="79f1a-155">100 DTUs</span></span>
- <span data-ttu-id="79f1a-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="79f1a-156">Premium.</span></span> <span data-ttu-id="79f1a-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="79f1a-157">125 DTUs</span></span>

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

### <span data-ttu-id="79f1a-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="79f1a-158">-Edition</span></span>
<span data-ttu-id="79f1a-159">Especifica a edição do banco de dados do Azure SQL para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="79f1a-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="79f1a-160">Não é possível alterar a edição.</span><span class="sxs-lookup"><span data-stu-id="79f1a-160">You cannot change the edition.</span></span> <span data-ttu-id="79f1a-161">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="79f1a-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79f1a-162">Nenhum</span><span class="sxs-lookup"><span data-stu-id="79f1a-162">None</span></span>
- <span data-ttu-id="79f1a-163">Básico</span><span class="sxs-lookup"><span data-stu-id="79f1a-163">Basic</span></span>
- <span data-ttu-id="79f1a-164">Standard</span><span class="sxs-lookup"><span data-stu-id="79f1a-164">Standard</span></span>
- <span data-ttu-id="79f1a-165">Premium</span><span class="sxs-lookup"><span data-stu-id="79f1a-165">Premium</span></span>
- <span data-ttu-id="79f1a-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="79f1a-166">DataWarehouse</span></span>
- <span data-ttu-id="79f1a-167">Gratuito</span><span class="sxs-lookup"><span data-stu-id="79f1a-167">Free</span></span>
- <span data-ttu-id="79f1a-168">Stretch</span><span class="sxs-lookup"><span data-stu-id="79f1a-168">Stretch</span></span>
- <span data-ttu-id="79f1a-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="79f1a-169">GeneralPurpose</span></span>
- <span data-ttu-id="79f1a-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="79f1a-170">BusinessCritical</span></span>

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

### <span data-ttu-id="79f1a-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="79f1a-171">-ElasticPoolName</span></span>
<span data-ttu-id="79f1a-172">Especifica o nome do pool elástica.</span><span class="sxs-lookup"><span data-stu-id="79f1a-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="79f1a-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="79f1a-173">-LicenseType</span></span>
<span data-ttu-id="79f1a-174">O tipo de licença para o banco de dados do Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="79f1a-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="79f1a-175">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="79f1a-175">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="79f1a-176">A ID de configuração de manutenção do pool SQL Elastic.</span><span class="sxs-lookup"><span data-stu-id="79f1a-176">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="79f1a-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f1a-177">-ResourceGroupName</span></span>
<span data-ttu-id="79f1a-178">Especifica o nome do grupo de recursos ao qual o pool elástica é atribuído.</span><span class="sxs-lookup"><span data-stu-id="79f1a-178">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="79f1a-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79f1a-179">-ServerName</span></span>
<span data-ttu-id="79f1a-180">Especifica o nome do servidor que hospeda o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="79f1a-180">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="79f1a-181">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="79f1a-181">-StorageMB</span></span>
<span data-ttu-id="79f1a-182">Especifica o limite de armazenamento, em megabytes, para o pool elástica.</span><span class="sxs-lookup"><span data-stu-id="79f1a-182">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="79f1a-183">Para obter mais informações, consulte o New-AzSqlElasticPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79f1a-183">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="79f1a-184">-Tags</span><span class="sxs-lookup"><span data-stu-id="79f1a-184">-Tags</span></span>
<span data-ttu-id="79f1a-185">Especifica um dicionário de pares de valores-chave que esse cmdlet associa ao pool elástica na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="79f1a-185">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="79f1a-186">Por exemplo: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="79f1a-186">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="79f1a-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="79f1a-187">-VCore</span></span>
<span data-ttu-id="79f1a-188">O número total compartilhado de Vcore para o Pool Elástica do Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="79f1a-188">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="79f1a-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="79f1a-189">-ZoneRedundant</span></span>
<span data-ttu-id="79f1a-190">A redundância de zona a ser associada ao Pool Elástica do Azure Sql</span><span class="sxs-lookup"><span data-stu-id="79f1a-190">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="79f1a-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79f1a-191">-Confirm</span></span>
<span data-ttu-id="79f1a-192">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79f1a-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79f1a-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79f1a-193">-WhatIf</span></span>
<span data-ttu-id="79f1a-194">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79f1a-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79f1a-195">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79f1a-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79f1a-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f1a-196">CommonParameters</span></span>
<span data-ttu-id="79f1a-197">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f1a-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f1a-198">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79f1a-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f1a-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79f1a-199">INPUTS</span></span>

### <span data-ttu-id="79f1a-200">System.String</span><span class="sxs-lookup"><span data-stu-id="79f1a-200">System.String</span></span>

## <span data-ttu-id="79f1a-201">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="79f1a-201">OUTPUTS</span></span>

### <span data-ttu-id="79f1a-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="79f1a-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="79f1a-203">NOTES</span><span class="sxs-lookup"><span data-stu-id="79f1a-203">NOTES</span></span>

## <span data-ttu-id="79f1a-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79f1a-204">RELATED LINKS</span></span>

[<span data-ttu-id="79f1a-205">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="79f1a-205">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="79f1a-206">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="79f1a-206">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="79f1a-207">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="79f1a-207">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="79f1a-208">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="79f1a-208">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="79f1a-209">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="79f1a-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
