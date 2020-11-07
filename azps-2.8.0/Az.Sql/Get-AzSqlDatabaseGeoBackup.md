---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 07f6e9b01e3def2dfe7cc88602b9643344ff3c4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773675"
---
# <span data-ttu-id="0f6c2-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="0f6c2-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="0f6c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f6c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6c2-103">Obtém um backup de um banco de dados com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="0f6c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f6c2-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f6c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f6c2-105">DESCRIPTION</span></span>
<span data-ttu-id="0f6c2-106">O cmdlet **Get-AzSqlDatabaseGeoBackup** Obtém um backup de redundância geográfica especificado de um banco de dados SQL ou todos os backups com redundância geográfica disponíveis em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="0f6c2-107">Um backup com redundância geográfica é um recurso recuperável que usa arquivos de dados de uma localização geográfica separada.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="0f6c2-108">Você pode usar Geo-Restore para restaurar um backup com redundância geográfica em caso de falha regional para recuperar seu banco de dados em uma nova região.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="0f6c2-109">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0f6c2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f6c2-110">EXAMPLES</span></span>

### <span data-ttu-id="0f6c2-111">Exemplo 1: obter todos os backups com redundância geográfica em um servidor</span><span class="sxs-lookup"><span data-stu-id="0f6c2-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="0f6c2-112">Esse comando obtém todos os backups com redundância geográfica disponíveis em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="0f6c2-113">Exemplo 2: obter um backup de redundância geográfica especificado</span><span class="sxs-lookup"><span data-stu-id="0f6c2-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="0f6c2-114">Esse comando obtém o backup com redundância geográfica de banco de dados chamado ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="0f6c2-115">Exemplo 3: obter todos os backups com redundância geográfica em um servidor usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="0f6c2-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="0f6c2-116">Esse comando obtém todos os backups com redundância geográfica disponíveis em um servidor especificado que comece com "contoso".</span><span class="sxs-lookup"><span data-stu-id="0f6c2-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="0f6c2-117">OS</span><span class="sxs-lookup"><span data-stu-id="0f6c2-117">PARAMETERS</span></span>

### <span data-ttu-id="0f6c2-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f6c2-118">-DatabaseName</span></span>
<span data-ttu-id="0f6c2-119">Especifica o nome do banco de dados a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0f6c2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6c2-120">-DefaultProfile</span></span>
<span data-ttu-id="0f6c2-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0f6c2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f6c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f6c2-123">Especifica o nome do grupo de recursos ao qual o servidor de banco de dados SQL está atribuído.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="0f6c2-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0f6c2-124">-ServerName</span></span>
<span data-ttu-id="0f6c2-125">Especifica o nome do servidor que hospeda o backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="0f6c2-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f6c2-126">-Confirm</span></span>
<span data-ttu-id="0f6c2-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f6c2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6c2-128">-WhatIf</span></span>
<span data-ttu-id="0f6c2-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f6c2-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f6c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6c2-131">CommonParameters</span></span>
<span data-ttu-id="0f6c2-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f6c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6c2-133">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f6c2-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6c2-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f6c2-134">INPUTS</span></span>

### <span data-ttu-id="0f6c2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0f6c2-135">System.String</span></span>

## <span data-ttu-id="0f6c2-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f6c2-136">OUTPUTS</span></span>

### <span data-ttu-id="0f6c2-137">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="0f6c2-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="0f6c2-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f6c2-138">NOTES</span></span>

## <span data-ttu-id="0f6c2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f6c2-139">RELATED LINKS</span></span>

[<span data-ttu-id="0f6c2-140">Visão geral: continuidade de negócios em nuvem e recuperação de desastres do banco de dados com SQL</span><span class="sxs-lookup"><span data-stu-id="0f6c2-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="0f6c2-141">Recuperar um banco de dados SQL do Azure de uma interrupção</span><span class="sxs-lookup"><span data-stu-id="0f6c2-141">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="0f6c2-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0f6c2-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="0f6c2-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0f6c2-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)