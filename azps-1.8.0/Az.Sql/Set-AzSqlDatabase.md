---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 62823ec87758142b34490f24d3e1b24e0c434f85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598807"
---
# <span data-ttu-id="e9cc1-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9cc1-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="e9cc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="e9cc1-103">Define propriedades para um banco de dados ou move um banco de dados existente para um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="e9cc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9cc1-104">SYNTAX</span></span>

### <span data-ttu-id="e9cc1-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="e9cc1-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9cc1-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="e9cc1-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9cc1-107">Rename</span><span class="sxs-lookup"><span data-stu-id="e9cc1-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9cc1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9cc1-108">DESCRIPTION</span></span>
<span data-ttu-id="e9cc1-109">O cmdlet **set-AzSqlDatabase** define propriedades para um banco de dados no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="e9cc1-110">Esse cmdlet pode modificar a camada de serviço ( *edição* ), o nível de desempenho ( *RequestedServiceObjectiveName* ) e o tamanho máximo de armazenamento ( *MaxSizeBytes* ) para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="e9cc1-111">Além disso, você pode especificar o parâmetro *ElasticPoolName* para mover um banco de dados para um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="e9cc1-112">Se um banco de dados já estiver em um pool elástico, você pode usar o parâmetro *RequestedServiceObjectiveName* para mover o banco de dados para fora de um pool elástico e para um nível de desempenho para bancos de dados individuais.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="e9cc1-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9cc1-113">EXAMPLES</span></span>

### <span data-ttu-id="e9cc1-114">Exemplo 1: atualizar um banco de dados para um banco de dados S0 padrão</span><span class="sxs-lookup"><span data-stu-id="e9cc1-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="e9cc1-115">Esse comando atualiza um banco de dados denominado Database01 para um banco de dados S0 padrão em um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="e9cc1-116">Exemplo 2: adicionar um banco de dados a um pool elástico</span><span class="sxs-lookup"><span data-stu-id="e9cc1-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="e9cc1-117">Esse comando adiciona um banco de dados denominado Database01 ao pool elástico chamado ElasticPool01 hospedado no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="e9cc1-118">Exemplo 3: modificar o tamanho máximo de armazenamento de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="e9cc1-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="e9cc1-119">Esse comando atualiza um banco de dados chamado Database01 para definir seu tamanho máximo como 1 TB.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="e9cc1-120">OS</span><span class="sxs-lookup"><span data-stu-id="e9cc1-120">PARAMETERS</span></span>

### <span data-ttu-id="e9cc1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9cc1-121">-AsJob</span></span>
<span data-ttu-id="e9cc1-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e9cc1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9cc1-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e9cc1-123">-ComputeGeneration</span></span>
<span data-ttu-id="e9cc1-124">A geração de computação a ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="e9cc1-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9cc1-125">-DatabaseName</span></span>
<span data-ttu-id="e9cc1-126">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-126">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e9cc1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9cc1-127">-DefaultProfile</span></span>
<span data-ttu-id="e9cc1-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e9cc1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9cc1-129">-Edição</span><span class="sxs-lookup"><span data-stu-id="e9cc1-129">-Edition</span></span>
<span data-ttu-id="e9cc1-130">Especifica a edição para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-130">Specifies the edition for the database.</span></span>
<span data-ttu-id="e9cc1-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e9cc1-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e9cc1-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e9cc1-132">None</span></span>
- <span data-ttu-id="e9cc1-133">Basic</span><span class="sxs-lookup"><span data-stu-id="e9cc1-133">Basic</span></span>
- <span data-ttu-id="e9cc1-134">Oficial</span><span class="sxs-lookup"><span data-stu-id="e9cc1-134">Standard</span></span>
- <span data-ttu-id="e9cc1-135">Gratifica</span><span class="sxs-lookup"><span data-stu-id="e9cc1-135">Premium</span></span>
- <span data-ttu-id="e9cc1-136">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="e9cc1-136">DataWarehouse</span></span>
- <span data-ttu-id="e9cc1-137">Gratuito</span><span class="sxs-lookup"><span data-stu-id="e9cc1-137">Free</span></span>
- <span data-ttu-id="e9cc1-138">Automático</span><span class="sxs-lookup"><span data-stu-id="e9cc1-138">Stretch</span></span>
- <span data-ttu-id="e9cc1-139">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="e9cc1-139">GeneralPurpose</span></span>
- <span data-ttu-id="e9cc1-140">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="e9cc1-140">BusinessCritical</span></span>

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

### <span data-ttu-id="e9cc1-141">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e9cc1-141">-ElasticPoolName</span></span>
<span data-ttu-id="e9cc1-142">Especifica o nome do pool elástico no qual mover o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-142">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="e9cc1-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e9cc1-143">-LicenseType</span></span>
<span data-ttu-id="e9cc1-144">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-144">The license type for the Azure Sql database.</span></span> <span data-ttu-id="e9cc1-145">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="e9cc1-145">Possible values are:</span></span>
- <span data-ttu-id="e9cc1-146">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-146">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="e9cc1-147">O preço do banco de dados será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-147">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="e9cc1-148">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-148">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="e9cc1-149">O preço do banco de dados incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-149">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="e9cc1-150">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e9cc1-150">-MaxSizeBytes</span></span>
<span data-ttu-id="e9cc1-151">O tamanho máximo do banco de dados SQL do Azure em bytes.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-151">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="e9cc1-152">-NewName</span><span class="sxs-lookup"><span data-stu-id="e9cc1-152">-NewName</span></span>
<span data-ttu-id="e9cc1-153">O novo nome para renomear o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-153">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="e9cc1-154">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="e9cc1-154">-ReadScale</span></span>
<span data-ttu-id="e9cc1-155">A opção de escala de leitura para atribuir ao banco de dados SQL do Azure. (Habilitado/desabilitado)</span><span class="sxs-lookup"><span data-stu-id="e9cc1-155">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="e9cc1-156">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e9cc1-156">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="e9cc1-157">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-157">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="e9cc1-158">Para obter informações sobre os objetivos do serviço, consulte [níveis de desempenho e camadas do serviço de banco de dados SQL do Azure](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) na biblioteca do Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-158">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="e9cc1-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9cc1-159">-ResourceGroupName</span></span>
<span data-ttu-id="e9cc1-160">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-160">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e9cc1-161">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e9cc1-161">-ServerName</span></span>
<span data-ttu-id="e9cc1-162">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e9cc1-163">-Marcas</span><span class="sxs-lookup"><span data-stu-id="e9cc1-163">-Tags</span></span>
<span data-ttu-id="e9cc1-164">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e9cc1-165">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e9cc1-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e9cc1-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="e9cc1-166">-VCore</span></span>
<span data-ttu-id="e9cc1-167">O número VCORE do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e9cc1-167">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9cc1-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e9cc1-168">-ZoneRedundant</span></span>
<span data-ttu-id="e9cc1-169">A redundância de zona para associar ao banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e9cc1-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="e9cc1-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9cc1-170">-Confirm</span></span>
<span data-ttu-id="e9cc1-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9cc1-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9cc1-172">-WhatIf</span></span>
<span data-ttu-id="e9cc1-173">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9cc1-174">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9cc1-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9cc1-175">CommonParameters</span></span>
<span data-ttu-id="e9cc1-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9cc1-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9cc1-177">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9cc1-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9cc1-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9cc1-178">INPUTS</span></span>

### <span data-ttu-id="e9cc1-179">System. String</span><span class="sxs-lookup"><span data-stu-id="e9cc1-179">System.String</span></span>

## <span data-ttu-id="e9cc1-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9cc1-180">OUTPUTS</span></span>

### <span data-ttu-id="e9cc1-181">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e9cc1-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e9cc1-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9cc1-182">NOTES</span></span>

## <span data-ttu-id="e9cc1-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9cc1-183">RELATED LINKS</span></span>

[<span data-ttu-id="e9cc1-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9cc1-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="e9cc1-185">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9cc1-185">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="e9cc1-186">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9cc1-186">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="e9cc1-187">Currículo-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9cc1-187">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="e9cc1-188">Suspender-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9cc1-188">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="e9cc1-189">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e9cc1-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
