---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 57af759caa940686d69118157973eb01c9a6928e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115745"
---
# <span data-ttu-id="0814a-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0814a-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="0814a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0814a-102">SYNOPSIS</span></span>
<span data-ttu-id="0814a-103">Cria um banco de dados ou um banco de dados elástica.</span><span class="sxs-lookup"><span data-stu-id="0814a-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="0814a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0814a-104">SYNTAX</span></span>

### <span data-ttu-id="0814a-105">DtuBasedDatabase (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0814a-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0814a-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="0814a-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0814a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0814a-107">DESCRIPTION</span></span>
<span data-ttu-id="0814a-108">O **cmdlet New-AzSqlDatabase** cria um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0814a-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="0814a-109">Você também pode criar um banco de dados elástica definindo o parâmetro *ElasticPoolName* para um pool elástica existente.</span><span class="sxs-lookup"><span data-stu-id="0814a-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="0814a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0814a-110">EXAMPLES</span></span>

### <span data-ttu-id="0814a-111">Exemplo 1: Criar um banco de dados em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="0814a-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="0814a-112">Esse comando cria um banco de dados chamado Database01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="0814a-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="0814a-113">Exemplo 2: Criar um banco de dados elástica em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="0814a-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="0814a-114">Esse comando cria um banco de dados chamado Database02 no pool elástica chamado ElasticPool01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="0814a-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="0814a-115">Exemplo 3: Criar um banco de dados de Vcore em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="0814a-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="0814a-116">Esse comando cria um banco de dados Vcore chamado Database03 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="0814a-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="0814a-117">Exemplo 4: Criar um banco de dados Serverless no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="0814a-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="0814a-118">Esse comando cria um banco de dados Serverless chamado Database04 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="0814a-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="0814a-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0814a-119">PARAMETERS</span></span>

### <span data-ttu-id="0814a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0814a-120">-AsJob</span></span>
<span data-ttu-id="0814a-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0814a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0814a-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="0814a-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="0814a-123">O atraso de pausa automática em minutos para o banco de dados(somente sem servidor), -1 para optar por não</span><span class="sxs-lookup"><span data-stu-id="0814a-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="0814a-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="0814a-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="0814a-125">A redundância de armazenamento de backup usada para armazenar backups do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0814a-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="0814a-126">As opções são: Local, Zona e Geo.</span><span class="sxs-lookup"><span data-stu-id="0814a-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="0814a-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="0814a-127">-CatalogCollation</span></span>
<span data-ttu-id="0814a-128">Especifica o nome do colagem de catálogo de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0814a-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="0814a-129">-Nomeda Collation</span><span class="sxs-lookup"><span data-stu-id="0814a-129">-CollationName</span></span>
<span data-ttu-id="0814a-130">Especifica o nome do colagem de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0814a-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="0814a-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0814a-131">-ComputeGeneration</span></span>
<span data-ttu-id="0814a-132">A geração de computação a ser atribuir.</span><span class="sxs-lookup"><span data-stu-id="0814a-132">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="0814a-133">-ComputeModel</span></span>
<span data-ttu-id="0814a-134">O modelo de computação do banco de dados Sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="0814a-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="0814a-135">Sem servidor ou provisionado</span><span class="sxs-lookup"><span data-stu-id="0814a-135">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-136">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="0814a-136">-DatabaseName</span></span>
<span data-ttu-id="0814a-137">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0814a-137">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0814a-138">-DefaultProfile</span></span>
<span data-ttu-id="0814a-139">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0814a-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0814a-140">-Edição</span><span class="sxs-lookup"><span data-stu-id="0814a-140">-Edition</span></span>
<span data-ttu-id="0814a-141">Especifica a edição a ser atribuir ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0814a-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="0814a-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0814a-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0814a-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0814a-143">None</span></span>
- <span data-ttu-id="0814a-144">Basic</span><span class="sxs-lookup"><span data-stu-id="0814a-144">Basic</span></span>
- <span data-ttu-id="0814a-145">Padrão</span><span class="sxs-lookup"><span data-stu-id="0814a-145">Standard</span></span>
- <span data-ttu-id="0814a-146">Premium</span><span class="sxs-lookup"><span data-stu-id="0814a-146">Premium</span></span>
- <span data-ttu-id="0814a-147">Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="0814a-147">DataWarehouse</span></span>
- <span data-ttu-id="0814a-148">Livre</span><span class="sxs-lookup"><span data-stu-id="0814a-148">Free</span></span>
- <span data-ttu-id="0814a-149">Esticar</span><span class="sxs-lookup"><span data-stu-id="0814a-149">Stretch</span></span>
- <span data-ttu-id="0814a-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0814a-150">GeneralPurpose</span></span>
- <span data-ttu-id="0814a-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0814a-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0814a-152">-ElasticPoolName</span></span>
<span data-ttu-id="0814a-153">Especifica o nome do pool elástica no qual o banco de dados deve ser colocado.</span><span class="sxs-lookup"><span data-stu-id="0814a-153">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-154">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0814a-154">-Force</span></span>
<span data-ttu-id="0814a-155">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="0814a-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0814a-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="0814a-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="0814a-157">O número de réplicas readonly secundárias associadas ao banco de dados para o qual as conexões de intenção de aplicativos podem ser roteadas.</span><span class="sxs-lookup"><span data-stu-id="0814a-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="0814a-158">Esta propriedade só é definida para bancos de dados de edição Hyperscale.</span><span class="sxs-lookup"><span data-stu-id="0814a-158">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0814a-159">-LicenseType</span></span>
<span data-ttu-id="0814a-160">O tipo de licença do banco de dados Sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="0814a-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="0814a-161">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="0814a-161">Possible values are:</span></span>
- <span data-ttu-id="0814a-162">Preço BasePrice – O preço com desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças do SQL Server existentes é aplicado.</span><span class="sxs-lookup"><span data-stu-id="0814a-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="0814a-163">O preço do banco de dados será descontado para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0814a-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="0814a-164">LicenseInclt - O preço de desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças existentes do SQL Server não é aplicado.</span><span class="sxs-lookup"><span data-stu-id="0814a-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="0814a-165">O preço do banco de dados incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0814a-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="0814a-166">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0814a-166">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="0814a-167">A ID de configuração de manutenção do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0814a-167">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="0814a-168">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="0814a-168">-MaxSizeBytes</span></span>
<span data-ttu-id="0814a-169">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="0814a-169">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-170">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="0814a-170">-MinimumCapacity</span></span>
<span data-ttu-id="0814a-171">A capacidade mínima que o banco de dados sempre terá alocado, se não pausada.</span><span class="sxs-lookup"><span data-stu-id="0814a-171">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="0814a-172">Somente para bancos de dados do Azure Sql sem servidor.</span><span class="sxs-lookup"><span data-stu-id="0814a-172">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-173">-Escala de Leitura</span><span class="sxs-lookup"><span data-stu-id="0814a-173">-ReadScale</span></span>
<span data-ttu-id="0814a-174">Se habilitadas, as conexões que têm intenção de aplicativo definidas como somente leitura na cadeia de conexão podem ser roteadas para uma réplica secundária.</span><span class="sxs-lookup"><span data-stu-id="0814a-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="0814a-175">Esta propriedade só é definida para bancos de dados Premium e Crítico comercial.</span><span class="sxs-lookup"><span data-stu-id="0814a-175">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="0814a-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="0814a-177">Especifica o nome do objetivo do serviço a ser atribuído ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0814a-177">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0814a-178">-ResourceGroupName</span></span>
<span data-ttu-id="0814a-179">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="0814a-179">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0814a-180">-Nomedo Exemplo</span><span class="sxs-lookup"><span data-stu-id="0814a-180">-SampleName</span></span>
<span data-ttu-id="0814a-181">O nome do esquema de exemplo a ser aplicado ao criar esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0814a-181">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-182">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="0814a-182">-SecondaryType</span></span>
<span data-ttu-id="0814a-183">O tipo secundário do banco de dados se for secundário.</span><span class="sxs-lookup"><span data-stu-id="0814a-183">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="0814a-184">Os valores válidos são Geo e Named.</span><span class="sxs-lookup"><span data-stu-id="0814a-184">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="0814a-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0814a-185">-ServerName</span></span>
<span data-ttu-id="0814a-186">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0814a-186">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0814a-187">-Marcas</span><span class="sxs-lookup"><span data-stu-id="0814a-187">-Tags</span></span>
<span data-ttu-id="0814a-188">Especifica um dicionário de pares de valor-chave na forma de uma tabela hash que este cmdlet associa ao novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0814a-188">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="0814a-189">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0814a-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0814a-190">-VCore</span><span class="sxs-lookup"><span data-stu-id="0814a-190">-VCore</span></span>
<span data-ttu-id="0814a-191">O número do Vcore para o banco de dados Sql do Azure</span><span class="sxs-lookup"><span data-stu-id="0814a-191">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0814a-192">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0814a-192">-ZoneRedundant</span></span>
<span data-ttu-id="0814a-193">A redundância de zona a ser associada ao Banco de Dados Sql do Azure</span><span class="sxs-lookup"><span data-stu-id="0814a-193">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="0814a-194">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0814a-194">-Confirm</span></span>
<span data-ttu-id="0814a-195">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0814a-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0814a-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0814a-196">-WhatIf</span></span>
<span data-ttu-id="0814a-197">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0814a-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0814a-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0814a-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0814a-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0814a-199">CommonParameters</span></span>
<span data-ttu-id="0814a-200">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0814a-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0814a-201">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0814a-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0814a-202">Entradas</span><span class="sxs-lookup"><span data-stu-id="0814a-202">INPUTS</span></span>

### <span data-ttu-id="0814a-203">System.String</span><span class="sxs-lookup"><span data-stu-id="0814a-203">System.String</span></span>

## <span data-ttu-id="0814a-204">Saídas</span><span class="sxs-lookup"><span data-stu-id="0814a-204">OUTPUTS</span></span>

### <span data-ttu-id="0814a-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0814a-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0814a-206">Notas</span><span class="sxs-lookup"><span data-stu-id="0814a-206">NOTES</span></span>

## <span data-ttu-id="0814a-207">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0814a-207">RELATED LINKS</span></span>

[<span data-ttu-id="0814a-208">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0814a-208">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0814a-209">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0814a-209">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="0814a-210">Novo-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="0814a-210">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="0814a-211">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0814a-211">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="0814a-212">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0814a-212">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="0814a-213">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0814a-213">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="0814a-214">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0814a-214">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="0814a-215">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0814a-215">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

