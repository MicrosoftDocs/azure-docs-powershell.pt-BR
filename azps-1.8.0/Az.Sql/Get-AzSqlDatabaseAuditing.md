---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: ac1057159de6f3028bd599183dc5c411155f14e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599044"
---
# <span data-ttu-id="aa23f-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="aa23f-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="aa23f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa23f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa23f-103">Obtém as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa23f-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="aa23f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa23f-104">SYNTAX</span></span>

### <span data-ttu-id="aa23f-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="aa23f-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa23f-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="aa23f-106">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa23f-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="aa23f-107">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa23f-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="aa23f-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa23f-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="aa23f-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa23f-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="aa23f-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa23f-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa23f-111">DESCRIPTION</span></span>
<span data-ttu-id="aa23f-112">O cmdlet **Get-AzSqlDatabaseAuditing** Obtém as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa23f-112">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="aa23f-113">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="aa23f-113">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="aa23f-114">O destino dos logs de auditoria é determinado especificando um dos seguintes parâmetros de switch: BlobStorage, LogAnalytics ou EventHub (se nenhum for especificado, o padrão será BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="aa23f-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="aa23f-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa23f-115">EXAMPLES</span></span>

### <span data-ttu-id="aa23f-116">Exemplo 1: obter as configurações de auditoria de armazenamento blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="aa23f-116">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="aa23f-117">Exemplo 2: obter as configurações de auditoria de armazenamento blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="aa23f-117">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="aa23f-118">Exemplo 3: obter, por meio do pipeline, as configurações de auditoria de armazenamento de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="aa23f-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="aa23f-119">Exemplo 4: obter as configurações de auditoria do hub de eventos de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="aa23f-119">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="aa23f-120">Exemplo 5: obter, por meio de pipeline, as configurações de auditoria de Hub de eventos de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="aa23f-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="aa23f-121">Exemplo 6: obter as configurações de auditoria de análise de log de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="aa23f-121">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="aa23f-122">OS</span><span class="sxs-lookup"><span data-stu-id="aa23f-122">PARAMETERS</span></span>

### <span data-ttu-id="aa23f-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="aa23f-123">-BlobStorage</span></span>
<span data-ttu-id="aa23f-124">Especifica que o destino dos logs de auditoria é o armazenamento de BLOB</span><span class="sxs-lookup"><span data-stu-id="aa23f-124">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa23f-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa23f-125">-DatabaseName</span></span>
<span data-ttu-id="aa23f-126">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="aa23f-126">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa23f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa23f-127">-DefaultProfile</span></span>
<span data-ttu-id="aa23f-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa23f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa23f-129">-EventHub</span><span class="sxs-lookup"><span data-stu-id="aa23f-129">-EventHub</span></span>
<span data-ttu-id="aa23f-130">Especifica que o destino dos logs de auditoria é o Hub de eventos</span><span class="sxs-lookup"><span data-stu-id="aa23f-130">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa23f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa23f-131">-InputObject</span></span>
<span data-ttu-id="aa23f-132">O objeto de banco de dados para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="aa23f-132">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa23f-133">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="aa23f-133">-LogAnalytics</span></span>
<span data-ttu-id="aa23f-134">Especifica que o destino dos logs de auditoria é análise de logs</span><span class="sxs-lookup"><span data-stu-id="aa23f-134">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa23f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa23f-135">-ResourceGroupName</span></span>
<span data-ttu-id="aa23f-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa23f-136">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa23f-137">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="aa23f-137">-ServerName</span></span>
<span data-ttu-id="aa23f-138">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="aa23f-138">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa23f-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aa23f-139">-Confirm</span></span>
<span data-ttu-id="aa23f-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa23f-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa23f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa23f-141">-WhatIf</span></span>
<span data-ttu-id="aa23f-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa23f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa23f-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa23f-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa23f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa23f-144">CommonParameters</span></span>
<span data-ttu-id="aa23f-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa23f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa23f-146">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa23f-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa23f-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa23f-147">INPUTS</span></span>

### <span data-ttu-id="aa23f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="aa23f-148">System.String</span></span>

### <span data-ttu-id="aa23f-149">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="aa23f-149">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="aa23f-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aa23f-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa23f-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa23f-151">OUTPUTS</span></span>

### <span data-ttu-id="aa23f-152">Microsoft. Azure. Commands. Sql. Auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="aa23f-152">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="aa23f-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa23f-153">NOTES</span></span>

## <span data-ttu-id="aa23f-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa23f-154">RELATED LINKS</span></span>
