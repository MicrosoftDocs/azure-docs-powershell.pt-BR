---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 17e6c492828f877ebf53c634a7670e8d60c9ccba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890955"
---
# <span data-ttu-id="4753f-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4753f-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="4753f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4753f-102">SYNOPSIS</span></span>
<span data-ttu-id="4753f-103">Define propriedades para um banco de dados ou move um banco de dados existente para um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="4753f-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="4753f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4753f-104">SYNTAX</span></span>

### <span data-ttu-id="4753f-105">Atualização (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4753f-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4753f-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="4753f-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4753f-107">Renomear</span><span class="sxs-lookup"><span data-stu-id="4753f-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4753f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4753f-108">DESCRIPTION</span></span>
<span data-ttu-id="4753f-109">O cmdlet **Set-AzSqlDatabase** define propriedades para um banco de dados no Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="4753f-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="4753f-110">Este cmdlet pode modificar a camada de serviço (*Edition*), o nível de desempenho (*RequestedServiceObjectiveName*) e o tamanho máximo de armazenamento (*MaxSizeBytes*) para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4753f-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="4753f-111">Além disso, você pode especificar o parâmetro *ElasticPoolName* para mover um banco de dados para um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="4753f-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="4753f-112">Se um banco de dados já estiver em um pool elástica, você poderá usar o parâmetro *RequestedServiceObjectiveName* para mover o banco de dados de um pool elástica e para um nível de desempenho para bancos de dados individuais.</span><span class="sxs-lookup"><span data-stu-id="4753f-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="4753f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4753f-113">EXAMPLES</span></span>

### <span data-ttu-id="4753f-114">Exemplo 1: atualizar um banco de dados para um banco de dados S0 Padrão</span><span class="sxs-lookup"><span data-stu-id="4753f-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="4753f-115">Este comando atualiza um banco de dados chamado Database01 para um banco de dados S0 Padrão em um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="4753f-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="4753f-116">Exemplo 2: Adicionar um banco de dados a um pool elástica</span><span class="sxs-lookup"><span data-stu-id="4753f-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="4753f-117">Este comando adiciona um banco de dados chamado Database01 ao pool elástica chamado ElasticPool01 hospedado no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="4753f-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="4753f-118">Exemplo 3: Modificar o tamanho máximo de armazenamento de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="4753f-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="4753f-119">Este comando atualiza um banco de dados chamado Database01 para definir seu tamanho máximo como 1 TB.</span><span class="sxs-lookup"><span data-stu-id="4753f-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="4753f-120">Exemplo 4: Atualizar um banco de dados de finalidade geral existente para a camada de serviço Hyperscale</span><span class="sxs-lookup"><span data-stu-id="4753f-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Hyperscale" -RequestedServiceObjectiveName "HS_Gen5_2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : 56246136-839f-4171-80af-4c28142463b1
Edition                       : Hyperscale
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : -1
Status                        : Online
CreationDate                  : 12/6/2020 5:34:16 PM
CurrentServiceObjectiveId     : 00000000-0000-0000-0000-000000000000
CurrentServiceObjectiveName   : HS_Gen5_2
RequestedServiceObjectiveName : HS_Gen5_2
RequestedServiceObjectiveId   :
ElasticPoolName               :
EarliestRestoreDate           : 12/6/2020 5:34:16 PM
Tags                          : {}
ResourceId                    : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/Server01/databases/Database01
CreateMode                    :
ReadScale                     : Enabled
ZoneRedundant                 :
Capacity                      : 2
Family                        : Gen5
SkuName                       : HS_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       :
MinimumCapacity               :
ReadReplicaCount              : 1
BackupStorageRedundancy       : Geo
```

<span data-ttu-id="4753f-121">Este comando atualiza um banco de dados chamado Database01 da camada de serviço De Finalidade Geral para Hyperscale.</span><span class="sxs-lookup"><span data-stu-id="4753f-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="4753f-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4753f-122">PARAMETERS</span></span>

### <span data-ttu-id="4753f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4753f-123">-AsJob</span></span>
<span data-ttu-id="4753f-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4753f-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4753f-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="4753f-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="4753f-126">O atraso de pausa automática em minutos para o banco de dados (somente sem servidor), -1 para não</span><span class="sxs-lookup"><span data-stu-id="4753f-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="4753f-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="4753f-128">A redundância de armazenamento de backup usada para armazenar backups para o banco de dados SQL Backup.</span><span class="sxs-lookup"><span data-stu-id="4753f-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="4753f-129">As opções são: Local, Zona e Geo.</span><span class="sxs-lookup"><span data-stu-id="4753f-129">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4753f-130">-ComputeGeneration</span></span>
<span data-ttu-id="4753f-131">A geração de computação a ser atribuida.</span><span class="sxs-lookup"><span data-stu-id="4753f-131">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="4753f-132">-ComputeModel</span></span>
<span data-ttu-id="4753f-133">Modelo calculado do banco de dados do Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="4753f-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="4753f-134">Sem servidor ou provisionado</span><span class="sxs-lookup"><span data-stu-id="4753f-134">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4753f-135">-DatabaseName</span></span>
<span data-ttu-id="4753f-136">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4753f-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="4753f-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4753f-137">-DefaultProfile</span></span>
<span data-ttu-id="4753f-138">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4753f-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4753f-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="4753f-139">-Edition</span></span>
<span data-ttu-id="4753f-140">Especifica a edição do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4753f-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="4753f-141">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4753f-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4753f-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4753f-142">None</span></span>
- <span data-ttu-id="4753f-143">Básico</span><span class="sxs-lookup"><span data-stu-id="4753f-143">Basic</span></span>
- <span data-ttu-id="4753f-144">Standard</span><span class="sxs-lookup"><span data-stu-id="4753f-144">Standard</span></span>
- <span data-ttu-id="4753f-145">Premium</span><span class="sxs-lookup"><span data-stu-id="4753f-145">Premium</span></span>
- <span data-ttu-id="4753f-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="4753f-146">DataWarehouse</span></span>
- <span data-ttu-id="4753f-147">Gratuito</span><span class="sxs-lookup"><span data-stu-id="4753f-147">Free</span></span>
- <span data-ttu-id="4753f-148">Stretch</span><span class="sxs-lookup"><span data-stu-id="4753f-148">Stretch</span></span>
- <span data-ttu-id="4753f-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="4753f-149">GeneralPurpose</span></span>
- <span data-ttu-id="4753f-150">Hyperscale</span><span class="sxs-lookup"><span data-stu-id="4753f-150">Hyperscale</span></span>
- <span data-ttu-id="4753f-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="4753f-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4753f-152">-ElasticPoolName</span></span>
<span data-ttu-id="4753f-153">Especifica o nome do pool elástica no qual mover o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4753f-153">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="4753f-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="4753f-155">O número de réplicas readon secondary associadas ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4753f-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="4753f-156">Somente para a edição Hyperscale.</span><span class="sxs-lookup"><span data-stu-id="4753f-156">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4753f-157">-LicenseType</span></span>
<span data-ttu-id="4753f-158">O tipo de licença para o banco de dados do Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="4753f-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="4753f-159">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="4753f-159">Possible values are:</span></span>
- <span data-ttu-id="4753f-160">BasePrice - Os preços com desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças SQL Server existentes são aplicados.</span><span class="sxs-lookup"><span data-stu-id="4753f-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="4753f-161">O preço do banco de dados será descontado para os proprietários SQL Server licenças existentes.</span><span class="sxs-lookup"><span data-stu-id="4753f-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="4753f-162">LicenseIncluded - O preço de desconto do Benefício Híbrido do Azure (AHB) para proprietários SQL Server licenças existentes não é aplicado.</span><span class="sxs-lookup"><span data-stu-id="4753f-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="4753f-163">O preço do banco de dados incluirá um novo SQL Server de licença.</span><span class="sxs-lookup"><span data-stu-id="4753f-163">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-164">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4753f-164">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="4753f-165">A ID de configuração de manutenção para o banco de dados SQL de dados.</span><span class="sxs-lookup"><span data-stu-id="4753f-165">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="4753f-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="4753f-166">-MaxSizeBytes</span></span>
<span data-ttu-id="4753f-167">O tamanho máximo do banco de dados do Azure SQL em bytes.</span><span class="sxs-lookup"><span data-stu-id="4753f-167">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-168">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="4753f-168">-MinimumCapacity</span></span>
<span data-ttu-id="4753f-169">A capacidade mínima que o banco de dados sempre alocará, se não pausada.</span><span class="sxs-lookup"><span data-stu-id="4753f-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="4753f-170">Somente para bancos de dados do Azure Sql sem servidor.</span><span class="sxs-lookup"><span data-stu-id="4753f-170">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-171">-NewName</span><span class="sxs-lookup"><span data-stu-id="4753f-171">-NewName</span></span>
<span data-ttu-id="4753f-172">O novo nome para o que renomear o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4753f-172">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="4753f-173">-ReadScale</span></span>
<span data-ttu-id="4753f-174">Se habilitada, as conexões com intenção de aplicativo definidas como somente leitura em sua cadeia de caracteres de conexão podem ser roteadas para uma réplica somente leitura secundária.</span><span class="sxs-lookup"><span data-stu-id="4753f-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="4753f-175">Essa propriedade só é settable para bancos de dados Premium e Business Critical.</span><span class="sxs-lookup"><span data-stu-id="4753f-175">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="4753f-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="4753f-177">Especifica o nome do objetivo do serviço a ser atribuído ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4753f-177">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="4753f-178">Para obter informações sobre os objetivos do serviço, consulte [Azure SQL Níveis](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) de Serviço de Banco de Dados e Níveis de Desempenho na Biblioteca de Rede de Desenvolvedores da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4753f-178">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4753f-179">-ResourceGroupName</span></span>
<span data-ttu-id="4753f-180">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="4753f-180">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4753f-181">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="4753f-181">-SecondaryType</span></span>
<span data-ttu-id="4753f-182">O tipo secundário do banco de dados se for secundário.</span><span class="sxs-lookup"><span data-stu-id="4753f-182">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="4753f-183">Os valores válidos são Geo e Named.</span><span class="sxs-lookup"><span data-stu-id="4753f-183">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-184">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4753f-184">-ServerName</span></span>
<span data-ttu-id="4753f-185">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4753f-185">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4753f-186">-Tags</span><span class="sxs-lookup"><span data-stu-id="4753f-186">-Tags</span></span>
<span data-ttu-id="4753f-187">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4753f-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4753f-188">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="4753f-188">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-189">-VCore</span><span class="sxs-lookup"><span data-stu-id="4753f-189">-VCore</span></span>
<span data-ttu-id="4753f-190">O número do Vcore para o banco de dados do Azure Sql</span><span class="sxs-lookup"><span data-stu-id="4753f-190">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-191">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="4753f-191">-ZoneRedundant</span></span>
<span data-ttu-id="4753f-192">A redundância de zona a ser associada ao Banco de Dados sql do Azure</span><span class="sxs-lookup"><span data-stu-id="4753f-192">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4753f-193">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4753f-193">-Confirm</span></span>
<span data-ttu-id="4753f-194">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4753f-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4753f-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4753f-195">-WhatIf</span></span>
<span data-ttu-id="4753f-196">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4753f-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4753f-197">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4753f-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4753f-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4753f-198">CommonParameters</span></span>
<span data-ttu-id="4753f-199">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4753f-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4753f-200">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4753f-200">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4753f-201">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4753f-201">INPUTS</span></span>

### <span data-ttu-id="4753f-202">System.String</span><span class="sxs-lookup"><span data-stu-id="4753f-202">System.String</span></span>

## <span data-ttu-id="4753f-203">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4753f-203">OUTPUTS</span></span>

### <span data-ttu-id="4753f-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4753f-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4753f-205">NOTES</span><span class="sxs-lookup"><span data-stu-id="4753f-205">NOTES</span></span>

## <span data-ttu-id="4753f-206">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4753f-206">RELATED LINKS</span></span>

[<span data-ttu-id="4753f-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4753f-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="4753f-208">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4753f-208">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="4753f-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4753f-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="4753f-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4753f-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="4753f-211">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4753f-211">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="4753f-212">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="4753f-212">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
