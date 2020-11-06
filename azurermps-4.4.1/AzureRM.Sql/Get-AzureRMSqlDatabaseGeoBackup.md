---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: ad46883722f0c9d4c4d8bf5a5f5f568bb267bba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610706"
---
# <span data-ttu-id="3a951-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="3a951-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="3a951-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a951-102">SYNOPSIS</span></span>
<span data-ttu-id="3a951-103">Obtém um backup de um banco de dados com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="3a951-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a951-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a951-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a951-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a951-105">DESCRIPTION</span></span>
<span data-ttu-id="3a951-106">O cmdlet **Get-AzureRMSqlDatabaseGeoBackup** Obtém um backup de redundância geográfica especificado de um banco de dados SQL ou todos os backups com redundância geográfica disponíveis em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="3a951-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>

<span data-ttu-id="3a951-107">Um backup com redundância geográfica é um recurso recuperável que usa arquivos de dados de uma localização geográfica separada.</span><span class="sxs-lookup"><span data-stu-id="3a951-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="3a951-108">Você pode usar Geo-Restore para restaurar um backup com redundância geográfica em caso de falha regional para recuperar seu banco de dados em uma nova região.</span><span class="sxs-lookup"><span data-stu-id="3a951-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>

<span data-ttu-id="3a951-109">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="3a951-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3a951-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a951-110">EXAMPLES</span></span>

### <span data-ttu-id="3a951-111">Exemplo 1: obter todos os backups com redundância geográfica em um servidor</span><span class="sxs-lookup"><span data-stu-id="3a951-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="3a951-112">Esse comando obtém todos os backups com redundância geográfica disponíveis em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="3a951-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="3a951-113">Exemplo 2: obter um backup de redundância geográfica especificado</span><span class="sxs-lookup"><span data-stu-id="3a951-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="3a951-114">Esse comando obtém o backup com redundância geográfica de banco de dados chamado ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="3a951-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="3a951-115">OS</span><span class="sxs-lookup"><span data-stu-id="3a951-115">PARAMETERS</span></span>

### <span data-ttu-id="3a951-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a951-116">-DatabaseName</span></span>
<span data-ttu-id="3a951-117">Especifica o nome do banco de dados a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="3a951-117">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="3a951-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a951-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a951-119">Especifica o nome do grupo de recursos ao qual o servidor de banco de dados SQL está atribuído.</span><span class="sxs-lookup"><span data-stu-id="3a951-119">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="3a951-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3a951-120">-ServerName</span></span>
<span data-ttu-id="3a951-121">Especifica o nome do servidor que hospeda o backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="3a951-121">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="3a951-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a951-122">-Confirm</span></span>
<span data-ttu-id="3a951-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a951-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a951-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a951-124">-WhatIf</span></span>
<span data-ttu-id="3a951-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a951-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a951-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a951-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a951-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a951-127">-DefaultProfile</span></span>
<span data-ttu-id="3a951-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a951-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a951-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a951-129">CommonParameters</span></span>
<span data-ttu-id="3a951-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a951-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a951-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a951-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a951-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a951-132">INPUTS</span></span>

## <span data-ttu-id="3a951-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a951-133">OUTPUTS</span></span>

### <span data-ttu-id="3a951-134">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="3a951-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="3a951-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a951-135">NOTES</span></span>

## <span data-ttu-id="3a951-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a951-136">RELATED LINKS</span></span>

[<span data-ttu-id="3a951-137">Visão geral: continuidade de negócios em nuvem e recuperação de desastres do banco de dados com SQL</span><span class="sxs-lookup"><span data-stu-id="3a951-137">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="3a951-138">Recuperar um banco de dados SQL do Azure de uma interrupção</span><span class="sxs-lookup"><span data-stu-id="3a951-138">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="3a951-139">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a951-139">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="3a951-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3a951-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
