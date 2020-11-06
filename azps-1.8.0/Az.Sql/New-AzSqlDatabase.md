---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598908"
---
# <span data-ttu-id="e23c3-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e23c3-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="e23c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e23c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e23c3-103">Cria um banco de dados ou um banco de dados elástico.</span><span class="sxs-lookup"><span data-stu-id="e23c3-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="e23c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e23c3-104">SYNTAX</span></span>

### <span data-ttu-id="e23c3-105">DtuBasedDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="e23c3-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e23c3-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="e23c3-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e23c3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e23c3-107">DESCRIPTION</span></span>
<span data-ttu-id="e23c3-108">O cmdlet **New-AzSqlDatabase** cria um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e23c3-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="e23c3-109">Você também pode criar um banco de dados elástico definindo o parâmetro *ElasticPoolName* como um pool elástico existente.</span><span class="sxs-lookup"><span data-stu-id="e23c3-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="e23c3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e23c3-110">EXAMPLES</span></span>

### <span data-ttu-id="e23c3-111">Exemplo 1: criar um banco de dados em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="e23c3-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="e23c3-112">Esse comando cria um banco de dados denominado Database01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="e23c3-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="e23c3-113">Exemplo 2: criar um banco de dados elástico em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="e23c3-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="e23c3-114">Esse comando cria um banco de dados denominado Database02 no pool elástico chamado ElasticPool01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="e23c3-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="e23c3-115">Exemplo 3: criar um banco de dados VCORE em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="e23c3-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="e23c3-116">Esse comando cria um banco de dados VCORE chamado Database03 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="e23c3-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="e23c3-117">OS</span><span class="sxs-lookup"><span data-stu-id="e23c3-117">PARAMETERS</span></span>

### <span data-ttu-id="e23c3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e23c3-118">-AsJob</span></span>
<span data-ttu-id="e23c3-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e23c3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e23c3-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="e23c3-120">-CatalogCollation</span></span>
<span data-ttu-id="e23c3-121">Especifica o nome do agrupamento do catálogo do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e23c3-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="e23c3-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="e23c3-122">-CollationName</span></span>
<span data-ttu-id="e23c3-123">Especifica o nome do agrupamento de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e23c3-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="e23c3-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e23c3-124">-ComputeGeneration</span></span>
<span data-ttu-id="e23c3-125">A geração de computação a ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="e23c3-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="e23c3-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e23c3-126">-DatabaseName</span></span>
<span data-ttu-id="e23c3-127">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e23c3-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e23c3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23c3-128">-DefaultProfile</span></span>
<span data-ttu-id="e23c3-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e23c3-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e23c3-130">-Edição</span><span class="sxs-lookup"><span data-stu-id="e23c3-130">-Edition</span></span>
<span data-ttu-id="e23c3-131">Especifica a edição a ser atribuída ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e23c3-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="e23c3-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e23c3-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e23c3-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e23c3-133">None</span></span>
- <span data-ttu-id="e23c3-134">Basic</span><span class="sxs-lookup"><span data-stu-id="e23c3-134">Basic</span></span>
- <span data-ttu-id="e23c3-135">Oficial</span><span class="sxs-lookup"><span data-stu-id="e23c3-135">Standard</span></span>
- <span data-ttu-id="e23c3-136">Gratifica</span><span class="sxs-lookup"><span data-stu-id="e23c3-136">Premium</span></span>
- <span data-ttu-id="e23c3-137">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="e23c3-137">DataWarehouse</span></span>
- <span data-ttu-id="e23c3-138">Gratuito</span><span class="sxs-lookup"><span data-stu-id="e23c3-138">Free</span></span>
- <span data-ttu-id="e23c3-139">Automático</span><span class="sxs-lookup"><span data-stu-id="e23c3-139">Stretch</span></span>
- <span data-ttu-id="e23c3-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="e23c3-140">GeneralPurpose</span></span>
- <span data-ttu-id="e23c3-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="e23c3-141">BusinessCritical</span></span>

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

### <span data-ttu-id="e23c3-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e23c3-142">-ElasticPoolName</span></span>
<span data-ttu-id="e23c3-143">Especifica o nome do pool elástico no qual colocar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e23c3-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="e23c3-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e23c3-144">-LicenseType</span></span>
<span data-ttu-id="e23c3-145">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e23c3-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="e23c3-146">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="e23c3-146">Possible values are:</span></span>
- <span data-ttu-id="e23c3-147">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e23c3-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="e23c3-148">O preço do banco de dados será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e23c3-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="e23c3-149">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e23c3-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="e23c3-150">O preço do banco de dados incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e23c3-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="e23c3-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e23c3-151">-MaxSizeBytes</span></span>
<span data-ttu-id="e23c3-152">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="e23c3-152">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="e23c3-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="e23c3-153">-ReadScale</span></span>
<span data-ttu-id="e23c3-154">A opção de escala de leitura para atribuir ao banco de dados SQL do Azure. (Habilitado/desabilitado)</span><span class="sxs-lookup"><span data-stu-id="e23c3-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="e23c3-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e23c3-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="e23c3-156">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e23c3-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="e23c3-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e23c3-157">-ResourceGroupName</span></span>
<span data-ttu-id="e23c3-158">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="e23c3-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e23c3-159">-Samplename</span><span class="sxs-lookup"><span data-stu-id="e23c3-159">-SampleName</span></span>
<span data-ttu-id="e23c3-160">O nome do esquema de exemplo a ser aplicado ao criar este banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e23c3-160">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="e23c3-161">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e23c3-161">-ServerName</span></span>
<span data-ttu-id="e23c3-162">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e23c3-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e23c3-163">-Marcas</span><span class="sxs-lookup"><span data-stu-id="e23c3-163">-Tags</span></span>
<span data-ttu-id="e23c3-164">Especifica um dicionário de pares de chave-valor na forma de uma tabela de hash que este cmdlet associa ao novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e23c3-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="e23c3-165">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e23c3-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e23c3-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="e23c3-166">-VCore</span></span>
<span data-ttu-id="e23c3-167">O número VCORE do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e23c3-167">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23c3-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e23c3-168">-ZoneRedundant</span></span>
<span data-ttu-id="e23c3-169">A redundância de zona para associar ao banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e23c3-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="e23c3-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e23c3-170">-Confirm</span></span>
<span data-ttu-id="e23c3-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e23c3-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e23c3-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e23c3-172">-WhatIf</span></span>
<span data-ttu-id="e23c3-173">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e23c3-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e23c3-174">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e23c3-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e23c3-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23c3-175">CommonParameters</span></span>
<span data-ttu-id="e23c3-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e23c3-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23c3-177">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e23c3-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23c3-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e23c3-178">INPUTS</span></span>

### <span data-ttu-id="e23c3-179">System. String</span><span class="sxs-lookup"><span data-stu-id="e23c3-179">System.String</span></span>

## <span data-ttu-id="e23c3-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e23c3-180">OUTPUTS</span></span>

### <span data-ttu-id="e23c3-181">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e23c3-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e23c3-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e23c3-182">NOTES</span></span>

## <span data-ttu-id="e23c3-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e23c3-183">RELATED LINKS</span></span>

[<span data-ttu-id="e23c3-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e23c3-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="e23c3-185">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e23c3-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="e23c3-186">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e23c3-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="e23c3-187">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e23c3-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="e23c3-188">Currículo-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e23c3-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="e23c3-189">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e23c3-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="e23c3-190">Suspender-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e23c3-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="e23c3-191">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e23c3-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

