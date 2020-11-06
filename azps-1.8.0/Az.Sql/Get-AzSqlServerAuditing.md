---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: ba225571780d4d09dfd5ecc1b47132462468b734
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598951"
---
# <span data-ttu-id="9b53b-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="9b53b-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="9b53b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b53b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b53b-103">Obtém as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="9b53b-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="9b53b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b53b-104">SYNTAX</span></span>

### <span data-ttu-id="9b53b-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b53b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b53b-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="9b53b-106">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b53b-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="9b53b-107">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b53b-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="9b53b-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b53b-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="9b53b-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b53b-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="9b53b-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b53b-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b53b-111">DESCRIPTION</span></span>
<span data-ttu-id="9b53b-112">O cmdlet **Get-AzSqlServerAuditing** Obtém as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="9b53b-112">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="9b53b-113">Especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="9b53b-113">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="9b53b-114">O destino dos logs de auditoria é determinado especificando um dos seguintes parâmetros de switch: BlobStorage, LogAnalytics ou EventHub (se nenhum for especificado, o padrão será BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="9b53b-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="9b53b-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b53b-115">EXAMPLES</span></span>

### <span data-ttu-id="9b53b-116">Exemplo 1: obter as configurações de auditoria de armazenamento blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="9b53b-116">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="9b53b-117">Exemplo 2: obter as configurações de auditoria de armazenamento blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="9b53b-117">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
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

### <span data-ttu-id="9b53b-118">Exemplo 3: obter, por meio do pipeline, as configurações de auditoria de armazenamento de blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="9b53b-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
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

### <span data-ttu-id="9b53b-119">Exemplo 4: obter as configurações de auditoria do hub de eventos de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="9b53b-119">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="9b53b-120">Exemplo 5: obter, por meio do pipeline, as configurações de auditoria do hub de eventos de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="9b53b-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="9b53b-121">Exemplo 6: obter as configurações de auditoria de análise de log de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="9b53b-121">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="9b53b-122">OS</span><span class="sxs-lookup"><span data-stu-id="9b53b-122">PARAMETERS</span></span>

### <span data-ttu-id="9b53b-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="9b53b-123">-BlobStorage</span></span>
<span data-ttu-id="9b53b-124">Especifica que o destino dos logs de auditoria é o armazenamento de BLOB</span><span class="sxs-lookup"><span data-stu-id="9b53b-124">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="9b53b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b53b-125">-DefaultProfile</span></span>
<span data-ttu-id="9b53b-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b53b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b53b-127">-EventHub</span><span class="sxs-lookup"><span data-stu-id="9b53b-127">-EventHub</span></span>
<span data-ttu-id="9b53b-128">Especifica que o destino dos logs de auditoria é o Hub de eventos</span><span class="sxs-lookup"><span data-stu-id="9b53b-128">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="9b53b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b53b-129">-InputObject</span></span>
<span data-ttu-id="9b53b-130">O objeto do servidor para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="9b53b-130">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b53b-131">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="9b53b-131">-LogAnalytics</span></span>
<span data-ttu-id="9b53b-132">Especifica que o destino dos logs de auditoria é análise de logs</span><span class="sxs-lookup"><span data-stu-id="9b53b-132">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="9b53b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b53b-133">-ResourceGroupName</span></span>
<span data-ttu-id="9b53b-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b53b-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b53b-135">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="9b53b-135">-ServerName</span></span>
<span data-ttu-id="9b53b-136">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9b53b-136">SQL server name.</span></span>

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

### <span data-ttu-id="9b53b-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b53b-137">-Confirm</span></span>
<span data-ttu-id="9b53b-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b53b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b53b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b53b-139">-WhatIf</span></span>
<span data-ttu-id="9b53b-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b53b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b53b-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b53b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b53b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b53b-142">CommonParameters</span></span>
<span data-ttu-id="9b53b-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b53b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b53b-144">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b53b-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b53b-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b53b-145">INPUTS</span></span>

### <span data-ttu-id="9b53b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9b53b-146">System.String</span></span>

### <span data-ttu-id="9b53b-147">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="9b53b-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="9b53b-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9b53b-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9b53b-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b53b-149">OUTPUTS</span></span>

### <span data-ttu-id="9b53b-150">Microsoft. Azure. Commands. Sql. Auditing. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="9b53b-150">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="9b53b-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b53b-151">NOTES</span></span>

## <span data-ttu-id="9b53b-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b53b-152">RELATED LINKS</span></span>
