---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110962"
---
# <span data-ttu-id="f1a54-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="f1a54-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="f1a54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1a54-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a54-103">Obtém um backup geo-redundante de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f1a54-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="f1a54-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1a54-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a54-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1a54-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a54-106">O cmdlet **Get-AzSqlDatabaseGeoBackup** obtém um backup especificado de redundância geográfica de um banco de dados SQL ou todos os backups disponíveis de redundância geográfica em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="f1a54-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="f1a54-107">Um backup redundante geográfico é um recurso restaurável usando arquivos de dados de uma localização geográfica separada.</span><span class="sxs-lookup"><span data-stu-id="f1a54-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="f1a54-108">Você pode usar Geo-Restore para restaurar um backup geo redundante em caso de uma paralisação regional para recuperar seu banco de dados em uma nova região.</span><span class="sxs-lookup"><span data-stu-id="f1a54-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="f1a54-109">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="f1a54-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f1a54-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f1a54-110">EXAMPLES</span></span>

### <span data-ttu-id="f1a54-111">Exemplo 1: Obter todos os backups geo redundantes em um servidor</span><span class="sxs-lookup"><span data-stu-id="f1a54-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="f1a54-112">Esse comando obtém todos os backups geo redundantes disponíveis em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="f1a54-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="f1a54-113">Exemplo 2: Obter um backup geo redundante especificado</span><span class="sxs-lookup"><span data-stu-id="f1a54-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="f1a54-114">Esse comando obtém o backup geo redundante do banco de dados chamado ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="f1a54-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="f1a54-115">Exemplo 3: Obter todos os backups geo redundantes em um servidor usando filtragem</span><span class="sxs-lookup"><span data-stu-id="f1a54-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="f1a54-116">Esse comando obtém todos os backups geo redundantes disponíveis em um servidor especificado que começa com "Contoso".</span><span class="sxs-lookup"><span data-stu-id="f1a54-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="f1a54-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1a54-117">PARAMETERS</span></span>

### <span data-ttu-id="f1a54-118">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="f1a54-118">-DatabaseName</span></span>
<span data-ttu-id="f1a54-119">Especifica o nome do banco de dados a ser obter.</span><span class="sxs-lookup"><span data-stu-id="f1a54-119">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="f1a54-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a54-120">-DefaultProfile</span></span>
<span data-ttu-id="f1a54-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f1a54-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1a54-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a54-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1a54-123">Especifica o nome do grupo de recursos ao qual o servidor de banco de dados SQL está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f1a54-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="f1a54-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1a54-124">-ServerName</span></span>
<span data-ttu-id="f1a54-125">Especifica o nome do servidor que hospeda o backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="f1a54-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="f1a54-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f1a54-126">-Confirm</span></span>
<span data-ttu-id="f1a54-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1a54-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a54-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a54-128">-WhatIf</span></span>
<span data-ttu-id="f1a54-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f1a54-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a54-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1a54-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a54-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a54-131">CommonParameters</span></span>
<span data-ttu-id="f1a54-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a54-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a54-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1a54-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a54-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="f1a54-134">INPUTS</span></span>

### <span data-ttu-id="f1a54-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f1a54-135">System.String</span></span>

## <span data-ttu-id="f1a54-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="f1a54-136">OUTPUTS</span></span>

### <span data-ttu-id="f1a54-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="f1a54-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="f1a54-138">Notas</span><span class="sxs-lookup"><span data-stu-id="f1a54-138">NOTES</span></span>

## <span data-ttu-id="f1a54-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1a54-139">RELATED LINKS</span></span>

[<span data-ttu-id="f1a54-140">Visão geral: continuidade de negócios na nuvem e recuperação de desastres de banco de dados com o banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f1a54-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="f1a54-141">Recuperar um banco de dados SQL do Azure de uma paralisação</span><span class="sxs-lookup"><span data-stu-id="f1a54-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="f1a54-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f1a54-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="f1a54-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f1a54-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
