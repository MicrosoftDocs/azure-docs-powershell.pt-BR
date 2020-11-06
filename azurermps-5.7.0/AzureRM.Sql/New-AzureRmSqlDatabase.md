---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: f5fc78f3e06150f3283e35c23bf80edce4f47650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432384"
---
# <span data-ttu-id="378e5-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378e5-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="378e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="378e5-102">SYNOPSIS</span></span>
<span data-ttu-id="378e5-103">Cria um banco de dados ou um banco de dados elástico.</span><span class="sxs-lookup"><span data-stu-id="378e5-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="378e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="378e5-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="378e5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="378e5-105">DESCRIPTION</span></span>
<span data-ttu-id="378e5-106">O cmdlet **New-AzureRmSqlDatabase** cria um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="378e5-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="378e5-107">Você também pode criar um banco de dados elástico definindo o parâmetro *ElasticPoolName* como um pool elástico existente.</span><span class="sxs-lookup"><span data-stu-id="378e5-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="378e5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="378e5-108">EXAMPLES</span></span>

### <span data-ttu-id="378e5-109">Exemplo 1: criar um banco de dados em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="378e5-109">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
Tags                          :
```

<span data-ttu-id="378e5-110">Esse comando cria um banco de dados denominado Database01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="378e5-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="378e5-111">Exemplo 2: criar um banco de dados elástico em um servidor especificado</span><span class="sxs-lookup"><span data-stu-id="378e5-111">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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
Tags                          :
```

<span data-ttu-id="378e5-112">Esse comando cria um banco de dados denominado Database01 no pool elástico chamado ElasticPool01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="378e5-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="378e5-113">OS</span><span class="sxs-lookup"><span data-stu-id="378e5-113">PARAMETERS</span></span>

### <span data-ttu-id="378e5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="378e5-114">-AsJob</span></span>
<span data-ttu-id="378e5-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="378e5-115">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-116">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="378e5-116">-CatalogCollation</span></span>
<span data-ttu-id="378e5-117">Especifica o nome do agrupamento do catálogo do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="378e5-117">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-118">-CollationName</span><span class="sxs-lookup"><span data-stu-id="378e5-118">-CollationName</span></span>
<span data-ttu-id="378e5-119">Especifica o nome do agrupamento de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="378e5-119">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="378e5-120">-DatabaseName</span></span>
<span data-ttu-id="378e5-121">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="378e5-121">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378e5-122">-DefaultProfile</span></span>
<span data-ttu-id="378e5-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="378e5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-124">-Edição</span><span class="sxs-lookup"><span data-stu-id="378e5-124">-Edition</span></span>
<span data-ttu-id="378e5-125">Especifica a edição a ser atribuída ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="378e5-125">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="378e5-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="378e5-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="378e5-127">Assume</span><span class="sxs-lookup"><span data-stu-id="378e5-127">Default</span></span>
- <span data-ttu-id="378e5-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="378e5-128">None</span></span>
- <span data-ttu-id="378e5-129">Gratifica</span><span class="sxs-lookup"><span data-stu-id="378e5-129">Premium</span></span>
- <span data-ttu-id="378e5-130">Basic</span><span class="sxs-lookup"><span data-stu-id="378e5-130">Basic</span></span>
- <span data-ttu-id="378e5-131">Oficial</span><span class="sxs-lookup"><span data-stu-id="378e5-131">Standard</span></span>
- <span data-ttu-id="378e5-132">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="378e5-132">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-133">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="378e5-133">-ElasticPoolName</span></span>
<span data-ttu-id="378e5-134">Especifica o nome do pool elástico no qual colocar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="378e5-134">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-135">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="378e5-135">-MaxSizeBytes</span></span>
<span data-ttu-id="378e5-136">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="378e5-136">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-137">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="378e5-137">-ReadScale</span></span>
<span data-ttu-id="378e5-138">A opção de escala de leitura para atribuir ao banco de dados SQL do Azure. (Habilitado/desabilitado)</span><span class="sxs-lookup"><span data-stu-id="378e5-138">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-139">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="378e5-139">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="378e5-140">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="378e5-140">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="378e5-141">-ResourceGroupName</span></span>
<span data-ttu-id="378e5-142">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="378e5-142">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-143">-Samplename</span><span class="sxs-lookup"><span data-stu-id="378e5-143">-SampleName</span></span>
<span data-ttu-id="378e5-144">O nome do esquema de exemplo a ser aplicado ao criar este banco de dados.</span><span class="sxs-lookup"><span data-stu-id="378e5-144">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-145">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="378e5-145">-ServerName</span></span>
<span data-ttu-id="378e5-146">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="378e5-146">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-147">-Marcas</span><span class="sxs-lookup"><span data-stu-id="378e5-147">-Tags</span></span>
<span data-ttu-id="378e5-148">Especifica um dicionário de pares de chave-valor na forma de uma tabela de hash que este cmdlet associa ao novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="378e5-148">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="378e5-149">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="378e5-149">For example:</span></span>

<span data-ttu-id="378e5-150">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="378e5-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-151">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="378e5-151">-ZoneRedundant</span></span>
<span data-ttu-id="378e5-152">A redundância de zona para associar ao banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="378e5-152">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="378e5-153">-Confirm</span></span>
<span data-ttu-id="378e5-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="378e5-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="378e5-155">-WhatIf</span></span>
<span data-ttu-id="378e5-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="378e5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="378e5-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="378e5-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378e5-158">CommonParameters</span></span>
<span data-ttu-id="378e5-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="378e5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378e5-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="378e5-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378e5-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="378e5-161">INPUTS</span></span>

### <span data-ttu-id="378e5-162">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="378e5-162">None</span></span>
<span data-ttu-id="378e5-163">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="378e5-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="378e5-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="378e5-164">OUTPUTS</span></span>

### <span data-ttu-id="378e5-165">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="378e5-165">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="378e5-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="378e5-166">NOTES</span></span>

## <span data-ttu-id="378e5-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="378e5-167">RELATED LINKS</span></span>

[<span data-ttu-id="378e5-168">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378e5-168">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="378e5-169">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="378e5-169">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="378e5-170">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="378e5-170">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="378e5-171">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378e5-171">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="378e5-172">Currículo-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378e5-172">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="378e5-173">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378e5-173">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="378e5-174">Suspender-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="378e5-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="378e5-175">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="378e5-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
