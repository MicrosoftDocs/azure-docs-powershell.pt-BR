---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: cf9bea67027e7a2c5e3928755f6d88b1dc124489
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773880"
---
# <span data-ttu-id="569cc-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="569cc-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="569cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="569cc-102">SYNOPSIS</span></span>
<span data-ttu-id="569cc-103">**Importante: esse cmdlet é preterido, [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) está substituindo-o.**</span><span class="sxs-lookup"><span data-stu-id="569cc-103">**Important: This cmdlet is deprecated, [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="569cc-104">Obtém as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="569cc-104">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="569cc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="569cc-105">SYNTAX</span></span>

### <span data-ttu-id="569cc-106">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="569cc-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569cc-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="569cc-107">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569cc-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="569cc-108">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569cc-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="569cc-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569cc-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="569cc-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569cc-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="569cc-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="569cc-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="569cc-112">DESCRIPTION</span></span>
<span data-ttu-id="569cc-113">O cmdlet **Get-AzSqlServerAuditing** Obtém as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="569cc-113">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="569cc-114">Especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="569cc-114">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="569cc-115">O destino dos logs de auditoria é determinado especificando um dos seguintes parâmetros de switch: BlobStorage, LogAnalytics ou EventHub (se nenhum for especificado, o padrão será BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="569cc-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="569cc-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="569cc-116">EXAMPLES</span></span>

### <span data-ttu-id="569cc-117">Exemplo 1: obter as configurações de auditoria de armazenamento blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="569cc-117">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="569cc-118">Exemplo 2: obter as configurações de auditoria de armazenamento blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="569cc-118">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="569cc-119">Exemplo 3: obter, por meio do pipeline, as configurações de auditoria de armazenamento de blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="569cc-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="569cc-120">Exemplo 4: obter as configurações de auditoria do hub de eventos de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="569cc-120">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="569cc-121">Exemplo 5: obter, por meio do pipeline, as configurações de auditoria do hub de eventos de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="569cc-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="569cc-122">Exemplo 6: obter as configurações de auditoria de análise de log de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="569cc-122">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="569cc-123">OS</span><span class="sxs-lookup"><span data-stu-id="569cc-123">PARAMETERS</span></span>

### <span data-ttu-id="569cc-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="569cc-124">-BlobStorage</span></span>
<span data-ttu-id="569cc-125">Especifica que o destino dos logs de auditoria é o armazenamento de BLOB</span><span class="sxs-lookup"><span data-stu-id="569cc-125">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="569cc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569cc-126">-DefaultProfile</span></span>
<span data-ttu-id="569cc-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="569cc-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="569cc-128">-EventHub</span><span class="sxs-lookup"><span data-stu-id="569cc-128">-EventHub</span></span>
<span data-ttu-id="569cc-129">Especifica que o destino dos logs de auditoria é o Hub de eventos</span><span class="sxs-lookup"><span data-stu-id="569cc-129">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="569cc-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="569cc-130">-InputObject</span></span>
<span data-ttu-id="569cc-131">O objeto do servidor para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="569cc-131">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="569cc-132">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="569cc-132">-LogAnalytics</span></span>
<span data-ttu-id="569cc-133">Especifica que o destino dos logs de auditoria é análise de logs</span><span class="sxs-lookup"><span data-stu-id="569cc-133">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="569cc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="569cc-134">-ResourceGroupName</span></span>
<span data-ttu-id="569cc-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="569cc-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="569cc-136">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="569cc-136">-ServerName</span></span>
<span data-ttu-id="569cc-137">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="569cc-137">SQL server name.</span></span>

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

### <span data-ttu-id="569cc-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="569cc-138">-Confirm</span></span>
<span data-ttu-id="569cc-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="569cc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="569cc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="569cc-140">-WhatIf</span></span>
<span data-ttu-id="569cc-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="569cc-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="569cc-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="569cc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="569cc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569cc-143">CommonParameters</span></span>
<span data-ttu-id="569cc-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="569cc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569cc-145">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="569cc-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569cc-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="569cc-146">INPUTS</span></span>

### <span data-ttu-id="569cc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="569cc-147">System.String</span></span>

### <span data-ttu-id="569cc-148">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="569cc-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="569cc-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="569cc-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="569cc-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="569cc-150">OUTPUTS</span></span>

### <span data-ttu-id="569cc-151">Microsoft. Azure. Commands. Sql. Auditing. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="569cc-151">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="569cc-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="569cc-152">NOTES</span></span>

## <span data-ttu-id="569cc-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="569cc-153">RELATED LINKS</span></span>
