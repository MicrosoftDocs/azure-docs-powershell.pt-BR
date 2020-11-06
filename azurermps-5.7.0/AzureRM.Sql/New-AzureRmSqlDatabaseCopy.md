---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 4e9d33691cfd09681bb115c89d0eaf351ef14f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426551"
---
# <span data-ttu-id="5e4f7-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5e4f7-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="5e4f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4f7-103">Cria uma cópia de um banco de dados SQL que usa o instantâneo no momento atual.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e4f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e4f7-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e4f7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="5e4f7-106">O cmdlet **New-AzureRmSqlDatabaseCopy** cria uma cópia de um banco de dados SQL do Azure que usa o instantâneo dos dados no momento atual.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="5e4f7-107">Use esse cmdlet em vez do cmdlet Start-AzureSqlDatabaseCopy para criar uma cópia do banco de dados única.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="5e4f7-108">Esse cmdlet retorna o objeto **Database** da cópia.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="5e4f7-109">Observação: Use o cmdlet New-AzureRmSqlDatabaseSecondary para configurar a replicação geográfica para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="5e4f7-110">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5e4f7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e4f7-111">EXAMPLES</span></span>

## <span data-ttu-id="5e4f7-112">OS</span><span class="sxs-lookup"><span data-stu-id="5e4f7-112">PARAMETERS</span></span>

### <span data-ttu-id="5e4f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e4f7-113">-AsJob</span></span>
<span data-ttu-id="5e4f7-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5e4f7-114">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="5e4f7-115">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e4f7-115">-CopyDatabaseName</span></span>
<span data-ttu-id="5e4f7-116">Especifica o nome da cópia do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-116">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4f7-117">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e4f7-117">-CopyResourceGroupName</span></span>
<span data-ttu-id="5e4f7-118">Especifica o nome do grupo de recursos do Azure no qual atribuir a cópia.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-118">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="5e4f7-119">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="5e4f7-119">-CopyServerName</span></span>
<span data-ttu-id="5e4f7-120">Especifica o nome do SQL Server que hospeda a cópia.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-120">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="5e4f7-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e4f7-121">-DatabaseName</span></span>
<span data-ttu-id="5e4f7-122">Especifica o nome do banco de dados SQL a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-122">Specifies the name of the SQL Database to copy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e4f7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4f7-123">-DefaultProfile</span></span>
<span data-ttu-id="5e4f7-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5e4f7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e4f7-125">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5e4f7-125">-ElasticPoolName</span></span>
<span data-ttu-id="5e4f7-126">Especifica o nome do pool elástico no qual atribuir a cópia.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-126">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="5e4f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e4f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="5e4f7-128">Especifica o nome do grupo de recursos que contém o banco de dados a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-128">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="5e4f7-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5e4f7-129">-ServerName</span></span>
<span data-ttu-id="5e4f7-130">Especifica o nome do SQL Server que contém o banco de dados a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-130">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="5e4f7-131">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="5e4f7-131">-ServiceObjectiveName</span></span>
<span data-ttu-id="5e4f7-132">Especifica o nome do objetivo de serviço a ser atribuído à cópia.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-132">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="5e4f7-133">-Marcas</span><span class="sxs-lookup"><span data-stu-id="5e4f7-133">-Tags</span></span>
<span data-ttu-id="5e4f7-134">Especifica os pares de valor chave na forma de uma tabela de hash para associar a cópia do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-134">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="5e4f7-135">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5e4f7-135">For example:</span></span>

<span data-ttu-id="5e4f7-136">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5e4f7-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5e4f7-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e4f7-137">-Confirm</span></span>
<span data-ttu-id="5e4f7-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e4f7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e4f7-139">-WhatIf</span></span>
<span data-ttu-id="5e4f7-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e4f7-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e4f7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4f7-142">CommonParameters</span></span>
<span data-ttu-id="5e4f7-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4f7-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e4f7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4f7-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e4f7-145">INPUTS</span></span>

### <span data-ttu-id="5e4f7-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5e4f7-146">None</span></span>
<span data-ttu-id="5e4f7-147">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e4f7-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e4f7-148">OUTPUTS</span></span>

### <span data-ttu-id="5e4f7-149">Microsoft. Azure. Commands. Sql. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="5e4f7-149">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="5e4f7-150">Esse cmdlet retorna um objeto de **banco de dados** que representa o banco de dados copiado.</span><span class="sxs-lookup"><span data-stu-id="5e4f7-150">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="5e4f7-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e4f7-151">NOTES</span></span>

## <span data-ttu-id="5e4f7-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e4f7-152">RELATED LINKS</span></span>

[<span data-ttu-id="5e4f7-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5e4f7-153">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="5e4f7-154">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5e4f7-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
