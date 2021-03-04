---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: 7bfe287b6e2a60ed169a7ffab24a410ede33913b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887328"
---
# <span data-ttu-id="482e8-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="482e8-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="482e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="482e8-102">SYNOPSIS</span></span>
<span data-ttu-id="482e8-103">Obtém as configurações de auditoria de um banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="482e8-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="482e8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="482e8-104">SYNTAX</span></span>

### <span data-ttu-id="482e8-105">DatabaseParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="482e8-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="482e8-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="482e8-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="482e8-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="482e8-107">DESCRIPTION</span></span>
<span data-ttu-id="482e8-108">O cmdlet **Get-AzSqlDatabaseAudit** obtém as configurações de auditoria de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="482e8-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="482e8-109">Para usar o cmdlet, use os *parâmetros ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="482e8-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="482e8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="482e8-110">EXAMPLES</span></span>

### <span data-ttu-id="482e8-111">Exemplo 1: Obter as configurações de auditoria de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="482e8-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="482e8-112">Exemplo 2: Obter, por meio do pipeline, as configurações de auditoria de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="482e8-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="482e8-113">Exemplo 3: Obter as configurações de auditoria de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="482e8-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="482e8-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="482e8-114">PARAMETERS</span></span>

### <span data-ttu-id="482e8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="482e8-115">-DatabaseName</span></span>
<span data-ttu-id="482e8-116">SQL Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="482e8-116">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482e8-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="482e8-117">-DatabaseObject</span></span>
<span data-ttu-id="482e8-118">O objeto database para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="482e8-118">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="482e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482e8-119">-DefaultProfile</span></span>
<span data-ttu-id="482e8-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="482e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="482e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="482e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="482e8-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="482e8-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482e8-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="482e8-123">-ServerName</span></span>
<span data-ttu-id="482e8-124">SQL nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="482e8-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482e8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482e8-125">CommonParameters</span></span>
<span data-ttu-id="482e8-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="482e8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482e8-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="482e8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482e8-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="482e8-128">INPUTS</span></span>

### <span data-ttu-id="482e8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="482e8-129">System.String</span></span>

### <span data-ttu-id="482e8-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="482e8-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="482e8-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="482e8-131">OUTPUTS</span></span>

### <span data-ttu-id="482e8-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="482e8-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="482e8-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="482e8-133">NOTES</span></span>

## <span data-ttu-id="482e8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="482e8-134">RELATED LINKS</span></span>
