---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 32329ac1e36c74c08dcf25f8f8b4295e81633e90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940752"
---
# <span data-ttu-id="1d93e-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d93e-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="1d93e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d93e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d93e-103">Cria um banco de dados ou um banco de dados elástico.</span><span class="sxs-lookup"><span data-stu-id="1d93e-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="1d93e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d93e-104">SYNTAX</span></span>

### <span data-ttu-id="1d93e-105">DtuBasedDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="1d93e-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d93e-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="1d93e-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d93e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d93e-107">DESCRIPTION</span></span>
<span data-ttu-id="1d93e-108">O cmdlet **New-AzSqlDatabase** cria um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d93e-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="1d93e-109">Você também pode criar um banco de dados elástico definindo o parâmetro *ElasticPoolName* como um pool elástico existente.</span><span class="sxs-lookup"><span data-stu-id="1d93e-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="1d93e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d93e-110">EXAMPLES</span></span>

### <span data-ttu-id="1d93e-111">Exemplo 1: criar um banco de dados em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="1d93e-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="1d93e-112">Esse comando cria um banco de dados denominado Database01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="1d93e-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="1d93e-113">Exemplo 2: criar um banco de dados elástico em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="1d93e-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="1d93e-114">Esse comando cria um banco de dados denominado Database02 no pool elástico chamado ElasticPool01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="1d93e-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="1d93e-115">Exemplo 3: criar um banco de dados VCORE em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="1d93e-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="1d93e-116">Esse comando cria um banco de dados VCORE chamado Database03 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="1d93e-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="1d93e-117">Exemplo 4: criar um banco de dados com servidor no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="1d93e-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="1d93e-118">Esse comando cria um banco de dados com servidor chamado Database04 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="1d93e-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="1d93e-119">OS</span><span class="sxs-lookup"><span data-stu-id="1d93e-119">PARAMETERS</span></span>

### <span data-ttu-id="1d93e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d93e-120">-AsJob</span></span>
<span data-ttu-id="1d93e-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1d93e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d93e-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="1d93e-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="1d93e-123">O atraso de pausa automática em minutos para o banco de dados (somente sem servidor),-1 para recusar</span><span class="sxs-lookup"><span data-stu-id="1d93e-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="1d93e-124">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="1d93e-124">-CatalogCollation</span></span>
<span data-ttu-id="1d93e-125">Especifica o nome do agrupamento do catálogo do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="1d93e-125">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="1d93e-126">-CollationName</span><span class="sxs-lookup"><span data-stu-id="1d93e-126">-CollationName</span></span>
<span data-ttu-id="1d93e-127">Especifica o nome do agrupamento de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="1d93e-127">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="1d93e-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="1d93e-128">-ComputeGeneration</span></span>
<span data-ttu-id="1d93e-129">A geração de computação a ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="1d93e-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="1d93e-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="1d93e-130">-ComputeModel</span></span>
<span data-ttu-id="1d93e-131">O modelo de computação do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d93e-131">The compute model for Azure Sql database.</span></span> <span data-ttu-id="1d93e-132">Desprovisionada ou com servidor</span><span class="sxs-lookup"><span data-stu-id="1d93e-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="1d93e-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d93e-133">-DatabaseName</span></span>
<span data-ttu-id="1d93e-134">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1d93e-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1d93e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d93e-135">-DefaultProfile</span></span>
<span data-ttu-id="1d93e-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1d93e-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d93e-137">-Edição</span><span class="sxs-lookup"><span data-stu-id="1d93e-137">-Edition</span></span>
<span data-ttu-id="1d93e-138">Especifica a edição a ser atribuída ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1d93e-138">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="1d93e-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1d93e-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d93e-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1d93e-140">None</span></span>
- <span data-ttu-id="1d93e-141">Basic</span><span class="sxs-lookup"><span data-stu-id="1d93e-141">Basic</span></span>
- <span data-ttu-id="1d93e-142">Oficial</span><span class="sxs-lookup"><span data-stu-id="1d93e-142">Standard</span></span>
- <span data-ttu-id="1d93e-143">Gratifica</span><span class="sxs-lookup"><span data-stu-id="1d93e-143">Premium</span></span>
- <span data-ttu-id="1d93e-144">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="1d93e-144">DataWarehouse</span></span>
- <span data-ttu-id="1d93e-145">Gratuito</span><span class="sxs-lookup"><span data-stu-id="1d93e-145">Free</span></span>
- <span data-ttu-id="1d93e-146">Automático</span><span class="sxs-lookup"><span data-stu-id="1d93e-146">Stretch</span></span>
- <span data-ttu-id="1d93e-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="1d93e-147">GeneralPurpose</span></span>
- <span data-ttu-id="1d93e-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="1d93e-148">BusinessCritical</span></span>

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

### <span data-ttu-id="1d93e-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1d93e-149">-ElasticPoolName</span></span>
<span data-ttu-id="1d93e-150">Especifica o nome do pool elástico no qual colocar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1d93e-150">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="1d93e-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1d93e-151">-LicenseType</span></span>
<span data-ttu-id="1d93e-152">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d93e-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="1d93e-153">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="1d93e-153">Possible values are:</span></span>
- <span data-ttu-id="1d93e-154">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d93e-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="1d93e-155">O preço do banco de dados será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d93e-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="1d93e-156">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d93e-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="1d93e-157">O preço do banco de dados incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d93e-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="1d93e-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="1d93e-158">-MaxSizeBytes</span></span>
<span data-ttu-id="1d93e-159">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="1d93e-159">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="1d93e-160">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="1d93e-160">-MinimumCapacity</span></span>
<span data-ttu-id="1d93e-161">A capacidade mínima que o banco de dados sempre terá atribuído, se não pausar.</span><span class="sxs-lookup"><span data-stu-id="1d93e-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="1d93e-162">Somente para bancos de dados SQL do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d93e-162">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="1d93e-163">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="1d93e-163">-ReadReplicaCount</span></span>
<span data-ttu-id="1d93e-164">O número de réplicas secundárias ReadOnly associadas ao banco de dados para o qual as conexões do intuito do aplicativo ReadOnly podem ser roteadas.</span><span class="sxs-lookup"><span data-stu-id="1d93e-164">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="1d93e-165">Essa propriedade só é configurável para bancos de dados do Rescale Edition.</span><span class="sxs-lookup"><span data-stu-id="1d93e-165">This property is only settable for Hyperscale edition databases.</span></span>

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

### <span data-ttu-id="1d93e-166">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="1d93e-166">-ReadScale</span></span>
<span data-ttu-id="1d93e-167">Se habilitada, as conexões que têm a intenção do aplicativo definida como ReadOnly na cadeia de conexão podem ser roteadas para uma réplica secundária somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1d93e-167">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="1d93e-168">Essa propriedade só é configurável para bancos de dados essenciais e comerciais essenciais.</span><span class="sxs-lookup"><span data-stu-id="1d93e-168">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="1d93e-169">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="1d93e-169">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="1d93e-170">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1d93e-170">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="1d93e-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d93e-171">-ResourceGroupName</span></span>
<span data-ttu-id="1d93e-172">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="1d93e-172">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1d93e-173">-Samplename</span><span class="sxs-lookup"><span data-stu-id="1d93e-173">-SampleName</span></span>
<span data-ttu-id="1d93e-174">O nome do esquema de exemplo a ser aplicado ao criar este banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1d93e-174">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="1d93e-175">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1d93e-175">-ServerName</span></span>
<span data-ttu-id="1d93e-176">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1d93e-176">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1d93e-177">-Marcas</span><span class="sxs-lookup"><span data-stu-id="1d93e-177">-Tags</span></span>
<span data-ttu-id="1d93e-178">Especifica um dicionário de pares de chave-valor na forma de uma tabela de hash que este cmdlet associa ao novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1d93e-178">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="1d93e-179">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1d93e-179">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1d93e-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="1d93e-180">-VCore</span></span>
<span data-ttu-id="1d93e-181">O número VCORE do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1d93e-181">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="1d93e-182">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="1d93e-182">-ZoneRedundant</span></span>
<span data-ttu-id="1d93e-183">A redundância de zona para associar ao banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1d93e-183">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="1d93e-184">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1d93e-184">-Confirm</span></span>
<span data-ttu-id="1d93e-185">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d93e-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d93e-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d93e-186">-WhatIf</span></span>
<span data-ttu-id="1d93e-187">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d93e-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d93e-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d93e-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d93e-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d93e-189">CommonParameters</span></span>
<span data-ttu-id="1d93e-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d93e-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d93e-191">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d93e-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d93e-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d93e-192">INPUTS</span></span>

### <span data-ttu-id="1d93e-193">System. String</span><span class="sxs-lookup"><span data-stu-id="1d93e-193">System.String</span></span>

## <span data-ttu-id="1d93e-194">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d93e-194">OUTPUTS</span></span>

### <span data-ttu-id="1d93e-195">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1d93e-195">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1d93e-196">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d93e-196">NOTES</span></span>

## <span data-ttu-id="1d93e-197">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d93e-197">RELATED LINKS</span></span>

[<span data-ttu-id="1d93e-198">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d93e-198">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="1d93e-199">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1d93e-199">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="1d93e-200">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1d93e-200">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="1d93e-201">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d93e-201">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="1d93e-202">Currículo-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d93e-202">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="1d93e-203">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d93e-203">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="1d93e-204">Suspender-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d93e-204">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="1d93e-205">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="1d93e-205">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

