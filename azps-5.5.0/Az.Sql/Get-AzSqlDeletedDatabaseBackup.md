---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118610"
---
# <span data-ttu-id="3106a-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="3106a-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="3106a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3106a-102">SYNOPSIS</span></span>
<span data-ttu-id="3106a-103">Obtém um banco de dados excluído que você pode restaurar.</span><span class="sxs-lookup"><span data-stu-id="3106a-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="3106a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3106a-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3106a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3106a-105">DESCRIPTION</span></span>
<span data-ttu-id="3106a-106">O cmdlet **Get-AzSqlDeletedDatabaseBackup** obtém um backup de banco de dados SQL excluído especificado que você pode restaurar ou todos os backups excluídos que você pode restaurar.</span><span class="sxs-lookup"><span data-stu-id="3106a-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="3106a-107">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="3106a-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3106a-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3106a-108">EXAMPLES</span></span>

### <span data-ttu-id="3106a-109">Exemplo 1: Obter todos os backups de banco de dados excluídos em um servidor</span><span class="sxs-lookup"><span data-stu-id="3106a-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="3106a-110">Esse comando obtém todos os backups de banco de dados excluídos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="3106a-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="3106a-111">Exemplo 2: Obter um backup de banco de dados excluído especificado</span><span class="sxs-lookup"><span data-stu-id="3106a-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="3106a-112">Esse comando obtém o backup de banco de dados excluído da ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="3106a-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="3106a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3106a-113">PARAMETERS</span></span>

### <span data-ttu-id="3106a-114">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="3106a-114">-DatabaseName</span></span>
<span data-ttu-id="3106a-115">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3106a-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3106a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3106a-116">-DefaultProfile</span></span>
<span data-ttu-id="3106a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3106a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3106a-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="3106a-118">-DeletionDate</span></span>
<span data-ttu-id="3106a-119">Especifica a data, como um objeto **DateTime,** de que o banco de dados foi excluído.</span><span class="sxs-lookup"><span data-stu-id="3106a-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="3106a-120">Para obter um **objeto DateTime,** use o cmdlet Get-Date dados.</span><span class="sxs-lookup"><span data-stu-id="3106a-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="3106a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3106a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3106a-122">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="3106a-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3106a-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3106a-123">-ServerName</span></span>
<span data-ttu-id="3106a-124">Especifica o nome do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3106a-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="3106a-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3106a-125">-Confirm</span></span>
<span data-ttu-id="3106a-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3106a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3106a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3106a-127">-WhatIf</span></span>
<span data-ttu-id="3106a-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3106a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3106a-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3106a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3106a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3106a-130">CommonParameters</span></span>
<span data-ttu-id="3106a-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3106a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3106a-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3106a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3106a-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="3106a-133">INPUTS</span></span>

### <span data-ttu-id="3106a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3106a-134">System.String</span></span>

### <span data-ttu-id="3106a-135">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3106a-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3106a-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="3106a-136">OUTPUTS</span></span>

### <span data-ttu-id="3106a-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="3106a-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="3106a-138">Notas</span><span class="sxs-lookup"><span data-stu-id="3106a-138">NOTES</span></span>

## <span data-ttu-id="3106a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3106a-139">RELATED LINKS</span></span>

[<span data-ttu-id="3106a-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3106a-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="3106a-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3106a-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
