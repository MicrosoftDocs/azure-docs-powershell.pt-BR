---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2373a076e6edd97314e08c9170f9584a904ad902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429316"
---
# <span data-ttu-id="6b802-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="6b802-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="6b802-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b802-102">SYNOPSIS</span></span>
<span data-ttu-id="6b802-103">Obtém um banco de dados excluído que você pode restaurar.</span><span class="sxs-lookup"><span data-stu-id="6b802-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b802-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b802-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b802-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b802-105">DESCRIPTION</span></span>
<span data-ttu-id="6b802-106">O cmdlet **Get-AzureRMSqlDeletedDatabaseBackup** Obtém um backup de banco de dados SQL excluído que você pode restaurar ou todos os backups excluídos que podem ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="6b802-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="6b802-107">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="6b802-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6b802-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b802-108">EXAMPLES</span></span>

### <span data-ttu-id="6b802-109">Exemplo 1: obter todos os backups de banco de dados excluídos em um servidor</span><span class="sxs-lookup"><span data-stu-id="6b802-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="6b802-110">Esse comando obtém todos os backups de banco de dados excluídos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="6b802-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="6b802-111">Exemplo 2: obter um backup de banco de dados excluído especificado</span><span class="sxs-lookup"><span data-stu-id="6b802-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="6b802-112">Esse comando obtém o backup do banco de dados excluído para ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="6b802-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="6b802-113">OS</span><span class="sxs-lookup"><span data-stu-id="6b802-113">PARAMETERS</span></span>

### <span data-ttu-id="6b802-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6b802-114">-DatabaseName</span></span>
<span data-ttu-id="6b802-115">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b802-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="6b802-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b802-116">-DefaultProfile</span></span>
<span data-ttu-id="6b802-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6b802-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b802-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="6b802-118">-DeletionDate</span></span>
<span data-ttu-id="6b802-119">Especifica a data, como um objeto **DateTime** , que o banco de dados foi excluído.</span><span class="sxs-lookup"><span data-stu-id="6b802-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="6b802-120">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="6b802-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="6b802-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b802-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b802-122">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="6b802-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6b802-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="6b802-123">-ServerName</span></span>
<span data-ttu-id="6b802-124">Especifica o nome do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b802-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="6b802-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b802-125">-Confirm</span></span>
<span data-ttu-id="6b802-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b802-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b802-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b802-127">-WhatIf</span></span>
<span data-ttu-id="6b802-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b802-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b802-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b802-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b802-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b802-130">CommonParameters</span></span>
<span data-ttu-id="6b802-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b802-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b802-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b802-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b802-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b802-133">INPUTS</span></span>

### <span data-ttu-id="6b802-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6b802-134">System.String</span></span>

### <span data-ttu-id="6b802-135">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6b802-135">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6b802-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b802-136">OUTPUTS</span></span>

### <span data-ttu-id="6b802-137">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="6b802-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="6b802-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b802-138">NOTES</span></span>

## <span data-ttu-id="6b802-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b802-139">RELATED LINKS</span></span>

[<span data-ttu-id="6b802-140">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6b802-140">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="6b802-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="6b802-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
