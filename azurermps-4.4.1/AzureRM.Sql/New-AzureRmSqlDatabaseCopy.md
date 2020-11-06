---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610699"
---
# <span data-ttu-id="b5063-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b5063-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="b5063-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5063-102">SYNOPSIS</span></span>
<span data-ttu-id="b5063-103">Cria uma cópia de um banco de dados SQL que usa o instantâneo no momento atual.</span><span class="sxs-lookup"><span data-stu-id="b5063-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5063-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5063-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5063-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5063-105">DESCRIPTION</span></span>
<span data-ttu-id="b5063-106">O cmdlet **New-AzureRmSqlDatabaseCopy** cria uma cópia de um banco de dados SQL do Azure que usa o instantâneo dos dados no momento atual.</span><span class="sxs-lookup"><span data-stu-id="b5063-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="b5063-107">Use esse cmdlet em vez do cmdlet Start-AzureSqlDatabaseCopy para criar uma cópia do banco de dados única.</span><span class="sxs-lookup"><span data-stu-id="b5063-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="b5063-108">Esse cmdlet retorna o objeto **Database** da cópia.</span><span class="sxs-lookup"><span data-stu-id="b5063-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="b5063-109">Observação: Use o cmdlet New-AzureRmSqlDatabaseSecondary para configurar a replicação geográfica para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b5063-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="b5063-110">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="b5063-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b5063-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5063-111">EXAMPLES</span></span>

## <span data-ttu-id="b5063-112">OS</span><span class="sxs-lookup"><span data-stu-id="b5063-112">PARAMETERS</span></span>

### <span data-ttu-id="b5063-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5063-113">-CopyDatabaseName</span></span>
<span data-ttu-id="b5063-114">Especifica o nome da cópia do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="b5063-114">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="b5063-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5063-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="b5063-116">Especifica o nome do grupo de recursos do Azure no qual atribuir a cópia.</span><span class="sxs-lookup"><span data-stu-id="b5063-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="b5063-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="b5063-117">-CopyServerName</span></span>
<span data-ttu-id="b5063-118">Especifica o nome do SQL Server que hospeda a cópia.</span><span class="sxs-lookup"><span data-stu-id="b5063-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="b5063-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5063-119">-DatabaseName</span></span>
<span data-ttu-id="b5063-120">Especifica o nome do banco de dados SQL a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="b5063-120">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="b5063-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b5063-121">-ElasticPoolName</span></span>
<span data-ttu-id="b5063-122">Especifica o nome do pool elástico no qual atribuir a cópia.</span><span class="sxs-lookup"><span data-stu-id="b5063-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="b5063-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5063-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5063-124">Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o banco de dados copiado.</span><span class="sxs-lookup"><span data-stu-id="b5063-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

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

### <span data-ttu-id="b5063-125">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b5063-125">-ServerName</span></span>
<span data-ttu-id="b5063-126">Especifica o nome do SQL Server que contém o banco de dados a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="b5063-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="b5063-127">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="b5063-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="b5063-128">Especifica o nome do objetivo de serviço a ser atribuído à cópia.</span><span class="sxs-lookup"><span data-stu-id="b5063-128">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="b5063-129">-Marcas</span><span class="sxs-lookup"><span data-stu-id="b5063-129">-Tags</span></span>
<span data-ttu-id="b5063-130">Especifica os pares de valor chave na forma de uma tabela de hash para associar a cópia do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b5063-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="b5063-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b5063-131">For example:</span></span>

<span data-ttu-id="b5063-132">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b5063-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b5063-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b5063-133">-Confirm</span></span>
<span data-ttu-id="b5063-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5063-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5063-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5063-135">-WhatIf</span></span>
<span data-ttu-id="b5063-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b5063-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5063-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5063-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5063-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5063-138">-DefaultProfile</span></span>
<span data-ttu-id="b5063-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5063-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5063-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5063-140">CommonParameters</span></span>
<span data-ttu-id="b5063-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5063-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5063-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5063-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5063-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5063-143">INPUTS</span></span>

## <span data-ttu-id="b5063-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5063-144">OUTPUTS</span></span>

### <span data-ttu-id="b5063-145">Microsoft. Azure. Commands. Sql. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="b5063-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="b5063-146">Esse cmdlet retorna um objeto de **banco de dados** que representa o banco de dados copiado.</span><span class="sxs-lookup"><span data-stu-id="b5063-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="b5063-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5063-147">NOTES</span></span>

## <span data-ttu-id="b5063-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5063-148">RELATED LINKS</span></span>

[<span data-ttu-id="b5063-149">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b5063-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b5063-150">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b5063-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
