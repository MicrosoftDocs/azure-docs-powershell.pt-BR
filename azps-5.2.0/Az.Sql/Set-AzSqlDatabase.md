---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 15f9aee8e278a1b33330508a10487e3847820891
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259636"
---
# <span data-ttu-id="3ca22-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ca22-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="3ca22-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ca22-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca22-103">Define propriedades para um banco de dados ou move um banco de dados existente para um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="3ca22-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="3ca22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ca22-104">SYNTAX</span></span>

### <span data-ttu-id="3ca22-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="3ca22-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ca22-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="3ca22-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ca22-107">Rename</span><span class="sxs-lookup"><span data-stu-id="3ca22-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca22-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ca22-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca22-109">O cmdlet **set-AzSqlDatabase** define propriedades para um banco de dados no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca22-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="3ca22-110">Esse cmdlet pode modificar a camada de serviço (*edição*), o nível de desempenho (*RequestedServiceObjectiveName*) e o tamanho máximo de armazenamento (*MaxSizeBytes*) para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ca22-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="3ca22-111">Além disso, você pode especificar o parâmetro *ElasticPoolName* para mover um banco de dados para um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="3ca22-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="3ca22-112">Se um banco de dados já estiver em um pool elástico, você pode usar o parâmetro *RequestedServiceObjectiveName* para mover o banco de dados para fora de um pool elástico e para um nível de desempenho para bancos de dados individuais.</span><span class="sxs-lookup"><span data-stu-id="3ca22-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="3ca22-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ca22-113">EXAMPLES</span></span>

### <span data-ttu-id="3ca22-114">Exemplo 1: atualizar um banco de dados para um banco de dados S0 padrão</span><span class="sxs-lookup"><span data-stu-id="3ca22-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="3ca22-115">Esse comando atualiza um banco de dados denominado Database01 para um banco de dados S0 padrão em um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="3ca22-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="3ca22-116">Exemplo 2: adicionar um banco de dados a um pool elástico</span><span class="sxs-lookup"><span data-stu-id="3ca22-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="3ca22-117">Esse comando adiciona um banco de dados denominado Database01 ao pool elástico chamado ElasticPool01 hospedado no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="3ca22-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="3ca22-118">Exemplo 3: modificar o tamanho máximo de armazenamento de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="3ca22-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="3ca22-119">Esse comando atualiza um banco de dados chamado Database01 para definir seu tamanho máximo como 1 TB.</span><span class="sxs-lookup"><span data-stu-id="3ca22-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="3ca22-120">OS</span><span class="sxs-lookup"><span data-stu-id="3ca22-120">PARAMETERS</span></span>

### <span data-ttu-id="3ca22-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ca22-121">-AsJob</span></span>
<span data-ttu-id="3ca22-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3ca22-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ca22-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="3ca22-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="3ca22-124">O atraso de pausa automática em minutos para o banco de dados (somente sem servidor),-1 para recusar</span><span class="sxs-lookup"><span data-stu-id="3ca22-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="3ca22-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="3ca22-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="3ca22-126">A redundância do armazenamento de backup usada para armazenar backups para o banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="3ca22-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="3ca22-127">Opções são: local, região e geo.</span><span class="sxs-lookup"><span data-stu-id="3ca22-127">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="3ca22-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3ca22-128">-ComputeGeneration</span></span>
<span data-ttu-id="3ca22-129">A geração de computação a ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="3ca22-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="3ca22-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="3ca22-130">-ComputeModel</span></span>
<span data-ttu-id="3ca22-131">Modelo calculado do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca22-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="3ca22-132">Desprovisionada ou com servidor</span><span class="sxs-lookup"><span data-stu-id="3ca22-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="3ca22-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ca22-133">-DatabaseName</span></span>
<span data-ttu-id="3ca22-134">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ca22-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3ca22-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca22-135">-DefaultProfile</span></span>
<span data-ttu-id="3ca22-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3ca22-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ca22-137">-Edição</span><span class="sxs-lookup"><span data-stu-id="3ca22-137">-Edition</span></span>
<span data-ttu-id="3ca22-138">Especifica a edição para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ca22-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="3ca22-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3ca22-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ca22-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3ca22-140">None</span></span>
- <span data-ttu-id="3ca22-141">Basic</span><span class="sxs-lookup"><span data-stu-id="3ca22-141">Basic</span></span>
- <span data-ttu-id="3ca22-142">Oficial</span><span class="sxs-lookup"><span data-stu-id="3ca22-142">Standard</span></span>
- <span data-ttu-id="3ca22-143">Gratifica</span><span class="sxs-lookup"><span data-stu-id="3ca22-143">Premium</span></span>
- <span data-ttu-id="3ca22-144">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="3ca22-144">DataWarehouse</span></span>
- <span data-ttu-id="3ca22-145">Gratuito</span><span class="sxs-lookup"><span data-stu-id="3ca22-145">Free</span></span>
- <span data-ttu-id="3ca22-146">Automático</span><span class="sxs-lookup"><span data-stu-id="3ca22-146">Stretch</span></span>
- <span data-ttu-id="3ca22-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="3ca22-147">GeneralPurpose</span></span>
- <span data-ttu-id="3ca22-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="3ca22-148">BusinessCritical</span></span>

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

### <span data-ttu-id="3ca22-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3ca22-149">-ElasticPoolName</span></span>
<span data-ttu-id="3ca22-150">Especifica o nome do pool elástico no qual mover o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ca22-150">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="3ca22-151">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3ca22-151">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="3ca22-152">O número de réplicas secundárias ReadOnly associadas ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ca22-152">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="3ca22-153">Somente para a edição de hiperescalas.</span><span class="sxs-lookup"><span data-stu-id="3ca22-153">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="3ca22-154">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3ca22-154">-LicenseType</span></span>
<span data-ttu-id="3ca22-155">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca22-155">The license type for the Azure Sql database.</span></span> <span data-ttu-id="3ca22-156">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="3ca22-156">Possible values are:</span></span>
- <span data-ttu-id="3ca22-157">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3ca22-157">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3ca22-158">O preço do banco de dados será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3ca22-158">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3ca22-159">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3ca22-159">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3ca22-160">O preço do banco de dados incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3ca22-160">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3ca22-161">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="3ca22-161">-MaxSizeBytes</span></span>
<span data-ttu-id="3ca22-162">O tamanho máximo do banco de dados SQL do Azure em bytes.</span><span class="sxs-lookup"><span data-stu-id="3ca22-162">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="3ca22-163">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="3ca22-163">-MinimumCapacity</span></span>
<span data-ttu-id="3ca22-164">A capacidade mínima que o banco de dados sempre terá atribuído, se não pausar.</span><span class="sxs-lookup"><span data-stu-id="3ca22-164">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="3ca22-165">Somente para bancos de dados SQL do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3ca22-165">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="3ca22-166">-NewName</span><span class="sxs-lookup"><span data-stu-id="3ca22-166">-NewName</span></span>
<span data-ttu-id="3ca22-167">O novo nome para renomear o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ca22-167">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="3ca22-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="3ca22-168">-ReadScale</span></span>
<span data-ttu-id="3ca22-169">Se habilitada, as conexões que têm a intenção do aplicativo definida como ReadOnly na cadeia de conexão podem ser roteadas para uma réplica secundária somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3ca22-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="3ca22-170">Essa propriedade só é configurável para bancos de dados essenciais e comerciais essenciais.</span><span class="sxs-lookup"><span data-stu-id="3ca22-170">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="3ca22-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3ca22-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="3ca22-172">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ca22-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="3ca22-173">Para obter informações sobre os objetivos do serviço, consulte [níveis de desempenho e camadas do serviço de banco de dados SQL do Azure](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) na biblioteca do Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="3ca22-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="3ca22-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca22-174">-ResourceGroupName</span></span>
<span data-ttu-id="3ca22-175">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="3ca22-175">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3ca22-176">-Secondarytype</span><span class="sxs-lookup"><span data-stu-id="3ca22-176">-SecondaryType</span></span>
<span data-ttu-id="3ca22-177">O tipo secundário do banco de dados se for secundário.</span><span class="sxs-lookup"><span data-stu-id="3ca22-177">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="3ca22-178">Os valores válidos são geo e named.</span><span class="sxs-lookup"><span data-stu-id="3ca22-178">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="3ca22-179">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3ca22-179">-ServerName</span></span>
<span data-ttu-id="3ca22-180">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ca22-180">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3ca22-181">-Marcas</span><span class="sxs-lookup"><span data-stu-id="3ca22-181">-Tags</span></span>
<span data-ttu-id="3ca22-182">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3ca22-182">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3ca22-183">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3ca22-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3ca22-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="3ca22-184">-VCore</span></span>
<span data-ttu-id="3ca22-185">O número VCORE do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="3ca22-185">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="3ca22-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="3ca22-186">-ZoneRedundant</span></span>
<span data-ttu-id="3ca22-187">A redundância de zona para associar ao banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="3ca22-187">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="3ca22-188">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ca22-188">-Confirm</span></span>
<span data-ttu-id="3ca22-189">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca22-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca22-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca22-190">-WhatIf</span></span>
<span data-ttu-id="3ca22-191">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ca22-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca22-192">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ca22-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca22-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca22-193">CommonParameters</span></span>
<span data-ttu-id="3ca22-194">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca22-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca22-195">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ca22-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca22-196">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ca22-196">INPUTS</span></span>

### <span data-ttu-id="3ca22-197">System. String</span><span class="sxs-lookup"><span data-stu-id="3ca22-197">System.String</span></span>

## <span data-ttu-id="3ca22-198">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ca22-198">OUTPUTS</span></span>

### <span data-ttu-id="3ca22-199">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3ca22-199">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="3ca22-200">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ca22-200">NOTES</span></span>

## <span data-ttu-id="3ca22-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ca22-201">RELATED LINKS</span></span>

[<span data-ttu-id="3ca22-202">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ca22-202">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="3ca22-203">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ca22-203">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="3ca22-204">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ca22-204">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="3ca22-205">Currículo-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ca22-205">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="3ca22-206">Suspender-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ca22-206">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="3ca22-207">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3ca22-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
