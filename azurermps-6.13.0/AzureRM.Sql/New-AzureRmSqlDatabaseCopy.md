---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 7019fc7345b4296d9c35f11c6acec5bf5a42d966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440016"
---
# <span data-ttu-id="2bc0f-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2bc0f-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="2bc0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bc0f-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc0f-103">Cria uma cópia de um banco de dados SQL que usa o instantâneo no momento atual.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bc0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bc0f-104">SYNTAX</span></span>

### <span data-ttu-id="2bc0f-105">DtuBasedDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="2bc0f-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bc0f-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="2bc0f-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bc0f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bc0f-107">DESCRIPTION</span></span>
<span data-ttu-id="2bc0f-108">O cmdlet **New-AzureRmSqlDatabaseCopy** cria uma cópia de um banco de dados SQL do Azure que usa o instantâneo dos dados no momento atual.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-108">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="2bc0f-109">Use esse cmdlet em vez do cmdlet Start-AzureSqlDatabaseCopy para criar uma cópia do banco de dados única.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-109">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="2bc0f-110">Esse cmdlet retorna o objeto **Database** da cópia.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="2bc0f-111">Observação: Use o cmdlet New-AzureRmSqlDatabaseSecondary para configurar a replicação geográfica para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-111">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="2bc0f-112">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2bc0f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bc0f-113">EXAMPLES</span></span>

## <span data-ttu-id="2bc0f-114">OS</span><span class="sxs-lookup"><span data-stu-id="2bc0f-114">PARAMETERS</span></span>

### <span data-ttu-id="2bc0f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bc0f-115">-AsJob</span></span>
<span data-ttu-id="2bc0f-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2bc0f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bc0f-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2bc0f-117">-ComputeGeneration</span></span>
<span data-ttu-id="2bc0f-118">A geração de computação a ser atribuída à nova cópia.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-118">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="2bc0f-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2bc0f-119">-CopyDatabaseName</span></span>
<span data-ttu-id="2bc0f-120">Especifica o nome da cópia do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="2bc0f-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc0f-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="2bc0f-122">Especifica o nome do grupo de recursos do Azure no qual atribuir a cópia.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="2bc0f-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="2bc0f-123">-CopyServerName</span></span>
<span data-ttu-id="2bc0f-124">Especifica o nome do SQL Server que hospeda a cópia.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="2bc0f-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2bc0f-125">-DatabaseName</span></span>
<span data-ttu-id="2bc0f-126">Especifica o nome do banco de dados SQL a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="2bc0f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc0f-127">-DefaultProfile</span></span>
<span data-ttu-id="2bc0f-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2bc0f-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc0f-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2bc0f-129">-ElasticPoolName</span></span>
<span data-ttu-id="2bc0f-130">Especifica o nome do pool elástico no qual atribuir a cópia.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="2bc0f-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2bc0f-131">-LicenseType</span></span>
<span data-ttu-id="2bc0f-132">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="2bc0f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc0f-133">-ResourceGroupName</span></span>
<span data-ttu-id="2bc0f-134">Especifica o nome do grupo de recursos que contém o banco de dados a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="2bc0f-135">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2bc0f-135">-ServerName</span></span>
<span data-ttu-id="2bc0f-136">Especifica o nome do SQL Server que contém o banco de dados a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="2bc0f-137">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="2bc0f-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="2bc0f-138">Especifica o nome do objetivo de serviço a ser atribuído à cópia.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-138">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="2bc0f-139">-Marcas</span><span class="sxs-lookup"><span data-stu-id="2bc0f-139">-Tags</span></span>
<span data-ttu-id="2bc0f-140">Especifica os pares de valor chave na forma de uma tabela de hash para associar a cópia do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="2bc0f-141">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2bc0f-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2bc0f-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="2bc0f-142">-VCore</span></span>
<span data-ttu-id="2bc0f-143">Os números Vcores da cópia do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

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

### <span data-ttu-id="2bc0f-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2bc0f-144">-Confirm</span></span>
<span data-ttu-id="2bc0f-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bc0f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bc0f-146">-WhatIf</span></span>
<span data-ttu-id="2bc0f-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bc0f-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bc0f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc0f-149">CommonParameters</span></span>
<span data-ttu-id="2bc0f-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc0f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc0f-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc0f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc0f-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bc0f-152">INPUTS</span></span>

### <span data-ttu-id="2bc0f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc0f-153">System.String</span></span>

## <span data-ttu-id="2bc0f-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bc0f-154">OUTPUTS</span></span>

### <span data-ttu-id="2bc0f-155">Microsoft. Azure. Commands. Sql. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="2bc0f-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="2bc0f-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bc0f-156">NOTES</span></span>

## <span data-ttu-id="2bc0f-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bc0f-157">RELATED LINKS</span></span>

[<span data-ttu-id="2bc0f-158">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2bc0f-158">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="2bc0f-159">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="2bc0f-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
