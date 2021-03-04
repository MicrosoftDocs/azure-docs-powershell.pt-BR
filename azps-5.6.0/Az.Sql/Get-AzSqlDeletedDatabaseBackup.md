---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: f64f7f7e16f18c9213c77df2903c17d8e7ea4ae1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891613"
---
# <span data-ttu-id="57e79-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="57e79-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="57e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57e79-102">SYNOPSIS</span></span>
<span data-ttu-id="57e79-103">Obtém um banco de dados excluído que você pode restaurar.</span><span class="sxs-lookup"><span data-stu-id="57e79-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="57e79-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57e79-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57e79-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57e79-105">DESCRIPTION</span></span>
<span data-ttu-id="57e79-106">O cmdlet **Get-AzSqlDeletedDatabaseBackup** obtém um backup de banco de dados excluído especificado SQL que você pode restaurar ou todos os backups excluídos que você pode restaurar.</span><span class="sxs-lookup"><span data-stu-id="57e79-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="57e79-107">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="57e79-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="57e79-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57e79-108">EXAMPLES</span></span>

### <span data-ttu-id="57e79-109">Exemplo 1: Obter todos os backups de banco de dados excluídos em um servidor</span><span class="sxs-lookup"><span data-stu-id="57e79-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="57e79-110">Esse comando obtém todos os backups de banco de dados excluídos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="57e79-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="57e79-111">Exemplo 2: Obter um backup de banco de dados excluído especificado</span><span class="sxs-lookup"><span data-stu-id="57e79-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="57e79-112">Este comando obtém o backup de banco de dados excluído para ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="57e79-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="57e79-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57e79-113">PARAMETERS</span></span>

### <span data-ttu-id="57e79-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="57e79-114">-DatabaseName</span></span>
<span data-ttu-id="57e79-115">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="57e79-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e79-116">-DefaultProfile</span></span>
<span data-ttu-id="57e79-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="57e79-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57e79-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="57e79-118">-DeletionDate</span></span>
<span data-ttu-id="57e79-119">Especifica a data, como um **objeto DateTime,** que o banco de dados foi excluído.</span><span class="sxs-lookup"><span data-stu-id="57e79-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="57e79-120">Para obter um **objeto DateTime,** use o Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57e79-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e79-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e79-121">-ResourceGroupName</span></span>
<span data-ttu-id="57e79-122">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="57e79-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="57e79-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57e79-123">-ServerName</span></span>
<span data-ttu-id="57e79-124">Especifica o nome do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="57e79-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="57e79-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57e79-125">-Confirm</span></span>
<span data-ttu-id="57e79-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57e79-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57e79-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57e79-127">-WhatIf</span></span>
<span data-ttu-id="57e79-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57e79-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57e79-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57e79-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57e79-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e79-130">CommonParameters</span></span>
<span data-ttu-id="57e79-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e79-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e79-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57e79-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e79-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57e79-133">INPUTS</span></span>

### <span data-ttu-id="57e79-134">System.String</span><span class="sxs-lookup"><span data-stu-id="57e79-134">System.String</span></span>

### <span data-ttu-id="57e79-135">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="57e79-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="57e79-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57e79-136">OUTPUTS</span></span>

### <span data-ttu-id="57e79-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="57e79-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="57e79-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="57e79-138">NOTES</span></span>

## <span data-ttu-id="57e79-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57e79-139">RELATED LINKS</span></span>

[<span data-ttu-id="57e79-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="57e79-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="57e79-141">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="57e79-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
