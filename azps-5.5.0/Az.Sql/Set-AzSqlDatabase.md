---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 7971e93dfc36d5e7f61f0aaf44224b1b72ecd1fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117067"
---
# <span data-ttu-id="e1512-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1512-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="e1512-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1512-102">SYNOPSIS</span></span>
<span data-ttu-id="e1512-103">Define as propriedades de um banco de dados ou move um banco de dados existente para um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="e1512-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="e1512-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1512-104">SYNTAX</span></span>

### <span data-ttu-id="e1512-105">Atualização (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e1512-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1512-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="e1512-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1512-107">Renomear</span><span class="sxs-lookup"><span data-stu-id="e1512-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1512-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1512-108">DESCRIPTION</span></span>
<span data-ttu-id="e1512-109">O **cmdlet Set-AzSqlDatabase define** propriedades para um banco de dados no Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e1512-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="e1512-110">Este cmdlet pode modificar a camada de serviço *(Edição),* o nível de desempenho (*RequestedServiceObjectiveName)* e o tamanho máximo de armazenamento (*MaxSizeBytes)* para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1512-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="e1512-111">Além disso, você pode especificar o parâmetro *ElasticPoolName* para mover um banco de dados para um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="e1512-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="e1512-112">Se um banco de dados já estiver em um pool elástica, você poderá usar o parâmetro *RequestedServiceObjectiveName* para mover o banco de dados de um pool elástica e para um nível de desempenho para bancos de dados simples.</span><span class="sxs-lookup"><span data-stu-id="e1512-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="e1512-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e1512-113">EXAMPLES</span></span>

### <span data-ttu-id="e1512-114">Exemplo 1: Atualizar um banco de dados para um banco de dados S0 Padrão</span><span class="sxs-lookup"><span data-stu-id="e1512-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="e1512-115">Esse comando atualiza um banco de dados chamado Database01 para um banco de dados S0 Padrão em um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="e1512-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="e1512-116">Exemplo 2: Adicionar um banco de dados a um pool elástica</span><span class="sxs-lookup"><span data-stu-id="e1512-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="e1512-117">Esse comando adiciona um banco de dados chamado Banco de Dados01 ao pool elástica chamado ElasticPool01 hospedado no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="e1512-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="e1512-118">Exemplo 3: modificar o tamanho máximo de armazenamento de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="e1512-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="e1512-119">Esse comando atualiza um banco de dados chamado Database01 para definir seu tamanho máximo para 1 TB.</span><span class="sxs-lookup"><span data-stu-id="e1512-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="e1512-120">Exemplo 4: Atualizar um banco de dados de Finalidade Geral existente para o nível de serviço De hiper escala</span><span class="sxs-lookup"><span data-stu-id="e1512-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
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

<span data-ttu-id="e1512-121">Esse comando atualiza um banco de dados chamado Database01 da Finalidade Geral para o nível de serviço De Hiperscale.</span><span class="sxs-lookup"><span data-stu-id="e1512-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="e1512-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1512-122">PARAMETERS</span></span>

### <span data-ttu-id="e1512-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1512-123">-AsJob</span></span>
<span data-ttu-id="e1512-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e1512-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1512-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="e1512-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="e1512-126">O atraso de pausa automática em minutos para o banco de dados (somente sem servidor), -1 para sair</span><span class="sxs-lookup"><span data-stu-id="e1512-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="e1512-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="e1512-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="e1512-128">A redundância de armazenamento de backup usada para armazenar backups do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e1512-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="e1512-129">As opções são: Local, Zona e Geo.</span><span class="sxs-lookup"><span data-stu-id="e1512-129">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="e1512-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e1512-130">-ComputeGeneration</span></span>
<span data-ttu-id="e1512-131">A geração de computação a ser atribuir.</span><span class="sxs-lookup"><span data-stu-id="e1512-131">The compute generation to assign.</span></span>

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

### <span data-ttu-id="e1512-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="e1512-132">-ComputeModel</span></span>
<span data-ttu-id="e1512-133">Modelo calculado do banco de dados Sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="e1512-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="e1512-134">Sem servidor ou provisionado</span><span class="sxs-lookup"><span data-stu-id="e1512-134">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="e1512-135">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="e1512-135">-DatabaseName</span></span>
<span data-ttu-id="e1512-136">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1512-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e1512-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1512-137">-DefaultProfile</span></span>
<span data-ttu-id="e1512-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e1512-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1512-139">-Edição</span><span class="sxs-lookup"><span data-stu-id="e1512-139">-Edition</span></span>
<span data-ttu-id="e1512-140">Especifica a edição do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1512-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="e1512-141">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e1512-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1512-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e1512-142">None</span></span>
- <span data-ttu-id="e1512-143">Basic</span><span class="sxs-lookup"><span data-stu-id="e1512-143">Basic</span></span>
- <span data-ttu-id="e1512-144">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1512-144">Standard</span></span>
- <span data-ttu-id="e1512-145">Premium</span><span class="sxs-lookup"><span data-stu-id="e1512-145">Premium</span></span>
- <span data-ttu-id="e1512-146">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="e1512-146">DataWarehouse</span></span>
- <span data-ttu-id="e1512-147">Livre</span><span class="sxs-lookup"><span data-stu-id="e1512-147">Free</span></span>
- <span data-ttu-id="e1512-148">Esticar</span><span class="sxs-lookup"><span data-stu-id="e1512-148">Stretch</span></span>
- <span data-ttu-id="e1512-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="e1512-149">GeneralPurpose</span></span>
- <span data-ttu-id="e1512-150">Hyperscale</span><span class="sxs-lookup"><span data-stu-id="e1512-150">Hyperscale</span></span>
- <span data-ttu-id="e1512-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="e1512-151">BusinessCritical</span></span>

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

### <span data-ttu-id="e1512-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e1512-152">-ElasticPoolName</span></span>
<span data-ttu-id="e1512-153">Especifica o nome do pool elástica para mover o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1512-153">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="e1512-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="e1512-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="e1512-155">O número de réplicas secundárias lidas associadas ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1512-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="e1512-156">Somente para a edição Hyperscale.</span><span class="sxs-lookup"><span data-stu-id="e1512-156">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="e1512-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e1512-157">-LicenseType</span></span>
<span data-ttu-id="e1512-158">O tipo de licença do banco de dados Sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="e1512-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="e1512-159">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="e1512-159">Possible values are:</span></span>
- <span data-ttu-id="e1512-160">Preço BasePrice – O preço com desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças do SQL Server existentes é aplicado.</span><span class="sxs-lookup"><span data-stu-id="e1512-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="e1512-161">O preço do banco de dados será descontado para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e1512-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="e1512-162">LicenseInclt - O preço de desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças existentes do SQL Server não é aplicado.</span><span class="sxs-lookup"><span data-stu-id="e1512-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="e1512-163">O preço do banco de dados incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e1512-163">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="e1512-164">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e1512-164">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="e1512-165">A ID de configuração de manutenção do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e1512-165">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="e1512-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e1512-166">-MaxSizeBytes</span></span>
<span data-ttu-id="e1512-167">O tamanho máximo do Banco de Dados SQL do Azure em bytes.</span><span class="sxs-lookup"><span data-stu-id="e1512-167">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="e1512-168">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="e1512-168">-MinimumCapacity</span></span>
<span data-ttu-id="e1512-169">A capacidade mínima que o banco de dados sempre terá alocado, se não pausada.</span><span class="sxs-lookup"><span data-stu-id="e1512-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="e1512-170">Somente para bancos de dados do Azure Sql sem servidor.</span><span class="sxs-lookup"><span data-stu-id="e1512-170">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="e1512-171">-NovoNome</span><span class="sxs-lookup"><span data-stu-id="e1512-171">-NewName</span></span>
<span data-ttu-id="e1512-172">O novo nome para o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1512-172">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="e1512-173">-Escala de Leitura</span><span class="sxs-lookup"><span data-stu-id="e1512-173">-ReadScale</span></span>
<span data-ttu-id="e1512-174">Se habilitadas, as conexões que têm intenção de aplicativo definidas como somente leitura na cadeia de conexão podem ser roteadas para uma réplica secundária.</span><span class="sxs-lookup"><span data-stu-id="e1512-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="e1512-175">Esta propriedade só é definida para bancos de dados Premium e Crítico comercial.</span><span class="sxs-lookup"><span data-stu-id="e1512-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="e1512-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e1512-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="e1512-177">Especifica o nome do objetivo do serviço a ser atribuído ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1512-177">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="e1512-178">Para saber mais sobre os objetivos do serviço, confira as camadas de serviço do banco de dados SQL do [Azure](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) e os níveis de desempenho na Biblioteca de Rede do Desenvolvedor da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e1512-178">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="e1512-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1512-179">-ResourceGroupName</span></span>
<span data-ttu-id="e1512-180">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="e1512-180">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e1512-181">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="e1512-181">-SecondaryType</span></span>
<span data-ttu-id="e1512-182">O tipo secundário do banco de dados se for secundário.</span><span class="sxs-lookup"><span data-stu-id="e1512-182">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="e1512-183">Os valores válidos são Geo e Named.</span><span class="sxs-lookup"><span data-stu-id="e1512-183">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="e1512-184">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e1512-184">-ServerName</span></span>
<span data-ttu-id="e1512-185">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1512-185">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e1512-186">-Marcas</span><span class="sxs-lookup"><span data-stu-id="e1512-186">-Tags</span></span>
<span data-ttu-id="e1512-187">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="e1512-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e1512-188">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="e1512-188">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e1512-189">-VCore</span><span class="sxs-lookup"><span data-stu-id="e1512-189">-VCore</span></span>
<span data-ttu-id="e1512-190">O número do Vcore para o banco de dados Sql do Azure</span><span class="sxs-lookup"><span data-stu-id="e1512-190">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="e1512-191">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e1512-191">-ZoneRedundant</span></span>
<span data-ttu-id="e1512-192">A redundância de zona a ser associada ao Banco de Dados Sql do Azure</span><span class="sxs-lookup"><span data-stu-id="e1512-192">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="e1512-193">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e1512-193">-Confirm</span></span>
<span data-ttu-id="e1512-194">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1512-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1512-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1512-195">-WhatIf</span></span>
<span data-ttu-id="e1512-196">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e1512-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1512-197">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1512-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1512-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1512-198">CommonParameters</span></span>
<span data-ttu-id="e1512-199">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1512-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1512-200">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1512-200">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1512-201">Entradas</span><span class="sxs-lookup"><span data-stu-id="e1512-201">INPUTS</span></span>

### <span data-ttu-id="e1512-202">System.String</span><span class="sxs-lookup"><span data-stu-id="e1512-202">System.String</span></span>

## <span data-ttu-id="e1512-203">Saídas</span><span class="sxs-lookup"><span data-stu-id="e1512-203">OUTPUTS</span></span>

### <span data-ttu-id="e1512-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e1512-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e1512-205">Notas</span><span class="sxs-lookup"><span data-stu-id="e1512-205">NOTES</span></span>

## <span data-ttu-id="e1512-206">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1512-206">RELATED LINKS</span></span>

[<span data-ttu-id="e1512-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1512-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="e1512-208">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1512-208">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="e1512-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1512-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="e1512-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1512-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="e1512-211">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1512-211">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="e1512-212">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e1512-212">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
