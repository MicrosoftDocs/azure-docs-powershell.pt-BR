---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115666"
---
# <span data-ttu-id="04f75-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="04f75-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="04f75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04f75-102">SYNOPSIS</span></span>
<span data-ttu-id="04f75-103">Obtém um banco de dados excluído que você pode restaurar.</span><span class="sxs-lookup"><span data-stu-id="04f75-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="04f75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04f75-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04f75-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04f75-105">DESCRIPTION</span></span>
<span data-ttu-id="04f75-106">O cmdlet **Get-AzSqlDeletedDatabaseBackup** Obtém um backup de banco de dados SQL excluído que você pode restaurar ou todos os backups excluídos que podem ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="04f75-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="04f75-107">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="04f75-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="04f75-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04f75-108">EXAMPLES</span></span>

### <span data-ttu-id="04f75-109">Exemplo 1: obter todos os backups de banco de dados excluídos em um servidor</span><span class="sxs-lookup"><span data-stu-id="04f75-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="04f75-110">Esse comando obtém todos os backups de banco de dados excluídos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="04f75-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="04f75-111">Exemplo 2: obter um backup de banco de dados excluído especificado</span><span class="sxs-lookup"><span data-stu-id="04f75-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="04f75-112">Esse comando obtém o backup do banco de dados excluído para ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="04f75-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="04f75-113">OS</span><span class="sxs-lookup"><span data-stu-id="04f75-113">PARAMETERS</span></span>

### <span data-ttu-id="04f75-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="04f75-114">-DatabaseName</span></span>
<span data-ttu-id="04f75-115">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="04f75-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="04f75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f75-116">-DefaultProfile</span></span>
<span data-ttu-id="04f75-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="04f75-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04f75-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="04f75-118">-DeletionDate</span></span>
<span data-ttu-id="04f75-119">Especifica a data, como um objeto **DateTime** , que o banco de dados foi excluído.</span><span class="sxs-lookup"><span data-stu-id="04f75-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="04f75-120">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="04f75-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="04f75-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04f75-121">-ResourceGroupName</span></span>
<span data-ttu-id="04f75-122">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="04f75-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="04f75-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="04f75-123">-ServerName</span></span>
<span data-ttu-id="04f75-124">Especifica o nome do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="04f75-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="04f75-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04f75-125">-Confirm</span></span>
<span data-ttu-id="04f75-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04f75-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04f75-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f75-127">-WhatIf</span></span>
<span data-ttu-id="04f75-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04f75-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04f75-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04f75-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04f75-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f75-130">CommonParameters</span></span>
<span data-ttu-id="04f75-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04f75-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f75-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04f75-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f75-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04f75-133">INPUTS</span></span>

### <span data-ttu-id="04f75-134">System. String</span><span class="sxs-lookup"><span data-stu-id="04f75-134">System.String</span></span>

### <span data-ttu-id="04f75-135">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04f75-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="04f75-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04f75-136">OUTPUTS</span></span>

### <span data-ttu-id="04f75-137">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="04f75-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="04f75-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04f75-138">NOTES</span></span>

## <span data-ttu-id="04f75-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04f75-139">RELATED LINKS</span></span>

[<span data-ttu-id="04f75-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="04f75-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="04f75-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="04f75-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
