---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: f7dbffffe9a51d35ced8861894373322898fd0f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942468"
---
# <span data-ttu-id="c134b-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c134b-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="c134b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c134b-102">SYNOPSIS</span></span>
<span data-ttu-id="c134b-103">Cria um banco de dados secundário para um banco de dados existente e inicia a replicação de dados.</span><span class="sxs-lookup"><span data-stu-id="c134b-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="c134b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c134b-104">SYNTAX</span></span>

### <span data-ttu-id="c134b-105">DtuBasedDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="c134b-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c134b-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="c134b-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c134b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c134b-107">DESCRIPTION</span></span>
<span data-ttu-id="c134b-108">O cmdlet **New-AzSqlDatabaseSecondary** substitui o cmdlet Start-AzSqlDatabaseCopy quando usado para configurar a replicação geográfica para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c134b-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="c134b-109">Ele retorna o objeto de link de replicação geográfica do banco de dados primário para o secundário.</span><span class="sxs-lookup"><span data-stu-id="c134b-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="c134b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c134b-110">EXAMPLES</span></span>

### <span data-ttu-id="c134b-111">1: estabelecer Geo-Replication ativas</span><span class="sxs-lookup"><span data-stu-id="c134b-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="c134b-112">2: estabeleça o Geo-Replication ativo e especifique o nome do banco de dados do parceiro para ser diferente do nome do banco de dados de origem</span><span class="sxs-lookup"><span data-stu-id="c134b-112">2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="c134b-113">OS</span><span class="sxs-lookup"><span data-stu-id="c134b-113">PARAMETERS</span></span>

### <span data-ttu-id="c134b-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="c134b-114">-AllowConnections</span></span>
<span data-ttu-id="c134b-115">Especifica a intenção de leitura do banco de dados SQL secundário do Azure.</span><span class="sxs-lookup"><span data-stu-id="c134b-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="c134b-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c134b-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c134b-117">Não</span><span class="sxs-lookup"><span data-stu-id="c134b-117">No</span></span>
- <span data-ttu-id="c134b-118">Todo</span><span class="sxs-lookup"><span data-stu-id="c134b-118">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c134b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c134b-119">-AsJob</span></span>
<span data-ttu-id="c134b-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c134b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c134b-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c134b-121">-DatabaseName</span></span>
<span data-ttu-id="c134b-122">Especifica o nome do banco de dados para atuar como primário.</span><span class="sxs-lookup"><span data-stu-id="c134b-122">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c134b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c134b-123">-DefaultProfile</span></span>
<span data-ttu-id="c134b-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c134b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c134b-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c134b-125">-LicenseType</span></span>
<span data-ttu-id="c134b-126">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c134b-126">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="c134b-127">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c134b-127">-PartnerDatabaseName</span></span>
<span data-ttu-id="c134b-128">O nome do banco de dados secundário a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c134b-128">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="c134b-129">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c134b-129">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c134b-130">Especifica o nome do grupo de recursos do Azure ao qual esse cmdlet atribui o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="c134b-130">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c134b-131">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c134b-131">-PartnerServerName</span></span>
<span data-ttu-id="c134b-132">Especifica o nome do servidor de banco de dados SQL do Azure atuar como secundário.</span><span class="sxs-lookup"><span data-stu-id="c134b-132">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c134b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c134b-133">-ResourceGroupName</span></span>
<span data-ttu-id="c134b-134">Especifica o nome do grupo de recursos do Azure ao qual esse cmdlet atribui o banco de dados primário.</span><span class="sxs-lookup"><span data-stu-id="c134b-134">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="c134b-135">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c134b-135">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="c134b-136">A geração de computação do banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="c134b-136">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="c134b-137">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c134b-137">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="c134b-138">Especifica o nome do pool elástico no qual colocar o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="c134b-138">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="c134b-139">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="c134b-139">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="c134b-140">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="c134b-140">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="c134b-141">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="c134b-141">-SecondaryVCore</span></span>
<span data-ttu-id="c134b-142">Os números Vcores do banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="c134b-142">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="c134b-143">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c134b-143">-ServerName</span></span>
<span data-ttu-id="c134b-144">Especifica o nome do SQL Server do banco de dados SQL primário.</span><span class="sxs-lookup"><span data-stu-id="c134b-144">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="c134b-145">-Marcas</span><span class="sxs-lookup"><span data-stu-id="c134b-145">-Tags</span></span>
<span data-ttu-id="c134b-146">Especifica os pares de valores chave na forma de uma tabela de hash a serem associados ao link de replicação do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="c134b-146">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="c134b-147">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c134b-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c134b-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c134b-148">-Confirm</span></span>
<span data-ttu-id="c134b-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c134b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c134b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c134b-150">-WhatIf</span></span>
<span data-ttu-id="c134b-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c134b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c134b-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c134b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c134b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c134b-153">CommonParameters</span></span>
<span data-ttu-id="c134b-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c134b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c134b-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c134b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c134b-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c134b-156">INPUTS</span></span>

### <span data-ttu-id="c134b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c134b-157">System.String</span></span>

## <span data-ttu-id="c134b-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c134b-158">OUTPUTS</span></span>

### <span data-ttu-id="c134b-159">Microsoft. Azure. Commands. Sql. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="c134b-159">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="c134b-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c134b-160">NOTES</span></span>

## <span data-ttu-id="c134b-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c134b-161">RELATED LINKS</span></span>

[<span data-ttu-id="c134b-162">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c134b-162">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c134b-163">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c134b-163">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c134b-164">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="c134b-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
