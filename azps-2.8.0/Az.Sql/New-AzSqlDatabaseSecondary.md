---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 1ed31d2fedc44900d08a4108ea53220a29228a7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773841"
---
# <span data-ttu-id="e07c6-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e07c6-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="e07c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e07c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e07c6-103">Cria um banco de dados secundário para um banco de dados existente e inicia a replicação de dados.</span><span class="sxs-lookup"><span data-stu-id="e07c6-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="e07c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e07c6-104">SYNTAX</span></span>

### <span data-ttu-id="e07c6-105">DtuBasedDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="e07c6-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07c6-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="e07c6-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e07c6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e07c6-107">DESCRIPTION</span></span>
<span data-ttu-id="e07c6-108">O cmdlet **New-AzSqlDatabaseSecondary** substitui o cmdlet Start-AzSqlDatabaseCopy quando usado para configurar a replicação geográfica para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e07c6-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="e07c6-109">Ele retorna o objeto de link de replicação geográfica do banco de dados primário para o secundário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="e07c6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e07c6-110">EXAMPLES</span></span>

### <span data-ttu-id="e07c6-111">1: estabelecer Geo-Replication ativas</span><span class="sxs-lookup"><span data-stu-id="e07c6-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="e07c6-112">OS</span><span class="sxs-lookup"><span data-stu-id="e07c6-112">PARAMETERS</span></span>

### <span data-ttu-id="e07c6-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="e07c6-113">-AllowConnections</span></span>
<span data-ttu-id="e07c6-114">Especifica a intenção de leitura do banco de dados SQL secundário do Azure.</span><span class="sxs-lookup"><span data-stu-id="e07c6-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="e07c6-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e07c6-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e07c6-116">Não</span><span class="sxs-lookup"><span data-stu-id="e07c6-116">No</span></span>
- <span data-ttu-id="e07c6-117">Todo</span><span class="sxs-lookup"><span data-stu-id="e07c6-117">All</span></span>

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

### <span data-ttu-id="e07c6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e07c6-118">-AsJob</span></span>
<span data-ttu-id="e07c6-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e07c6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e07c6-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e07c6-120">-DatabaseName</span></span>
<span data-ttu-id="e07c6-121">Especifica o nome do banco de dados para atuar como primário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="e07c6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07c6-122">-DefaultProfile</span></span>
<span data-ttu-id="e07c6-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e07c6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e07c6-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e07c6-124">-LicenseType</span></span>
<span data-ttu-id="e07c6-125">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e07c6-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="e07c6-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07c6-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="e07c6-127">Especifica o nome do grupo de recursos do Azure ao qual esse cmdlet atribui o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="e07c6-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="e07c6-128">-PartnerServerName</span></span>
<span data-ttu-id="e07c6-129">Especifica o nome do servidor de banco de dados SQL do Azure atuar como secundário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="e07c6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07c6-130">-ResourceGroupName</span></span>
<span data-ttu-id="e07c6-131">Especifica o nome do grupo de recursos do Azure ao qual esse cmdlet atribui o banco de dados primário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="e07c6-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e07c6-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="e07c6-133">A geração de computação do banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-133">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="e07c6-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e07c6-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="e07c6-135">Especifica o nome do pool elástico no qual colocar o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="e07c6-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e07c6-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="e07c6-137">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="e07c6-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="e07c6-138">-SecondaryVCore</span></span>
<span data-ttu-id="e07c6-139">Os números Vcores do banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="e07c6-140">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e07c6-140">-ServerName</span></span>
<span data-ttu-id="e07c6-141">Especifica o nome do SQL Server do banco de dados SQL primário.</span><span class="sxs-lookup"><span data-stu-id="e07c6-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="e07c6-142">-Marcas</span><span class="sxs-lookup"><span data-stu-id="e07c6-142">-Tags</span></span>
<span data-ttu-id="e07c6-143">Especifica os pares de valores chave na forma de uma tabela de hash a serem associados ao link de replicação do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e07c6-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="e07c6-144">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e07c6-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e07c6-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e07c6-145">-Confirm</span></span>
<span data-ttu-id="e07c6-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07c6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07c6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07c6-147">-WhatIf</span></span>
<span data-ttu-id="e07c6-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e07c6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07c6-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e07c6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07c6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07c6-150">CommonParameters</span></span>
<span data-ttu-id="e07c6-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e07c6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07c6-152">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e07c6-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07c6-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e07c6-153">INPUTS</span></span>

### <span data-ttu-id="e07c6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e07c6-154">System.String</span></span>

## <span data-ttu-id="e07c6-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e07c6-155">OUTPUTS</span></span>

### <span data-ttu-id="e07c6-156">Microsoft. Azure. Commands. Sql. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="e07c6-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="e07c6-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e07c6-157">NOTES</span></span>

## <span data-ttu-id="e07c6-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e07c6-158">RELATED LINKS</span></span>

[<span data-ttu-id="e07c6-159">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e07c6-159">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="e07c6-160">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e07c6-160">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="e07c6-161">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e07c6-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
