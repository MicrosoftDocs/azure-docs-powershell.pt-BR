---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: 4c9311bfba05862b1c073be5ec5b07106d8b19a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889151"
---
# <span data-ttu-id="c8a71-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c8a71-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="c8a71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8a71-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a71-103">Obtém as configurações de auditoria de um servidor SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a71-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="c8a71-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c8a71-104">SYNTAX</span></span>

### <span data-ttu-id="c8a71-105">ServerParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c8a71-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8a71-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a71-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8a71-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c8a71-107">DESCRIPTION</span></span>
<span data-ttu-id="c8a71-108">O cmdlet **Get-AzSqlServerAudit** obtém as configurações de auditoria de um servidor SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a71-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="c8a71-109">*Especifique os parâmetros ResourceGroupName* *e ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="c8a71-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="c8a71-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8a71-110">EXAMPLES</span></span>

### <span data-ttu-id="c8a71-111">Exemplo 1: Obter as configurações de auditoria de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c8a71-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

### <span data-ttu-id="c8a71-112">Exemplo 2: Obter, por meio do pipeline, as configurações de auditoria de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c8a71-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAudit
ServerName                          : server01
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

### <span data-ttu-id="c8a71-113">Exemplo 3: Obter as configurações de auditoria de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c8a71-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

## <span data-ttu-id="c8a71-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c8a71-114">PARAMETERS</span></span>

### <span data-ttu-id="c8a71-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8a71-115">-AsJob</span></span>
<span data-ttu-id="c8a71-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8a71-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a71-117">-DefaultProfile</span></span>
<span data-ttu-id="c8a71-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a71-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a71-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8a71-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8a71-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a71-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8a71-121">-ServerName</span></span>
<span data-ttu-id="c8a71-122">SQL nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c8a71-122">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a71-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="c8a71-123">-ServerObject</span></span>
<span data-ttu-id="c8a71-124">O objeto server para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="c8a71-124">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a71-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a71-125">CommonParameters</span></span>
<span data-ttu-id="c8a71-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a71-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a71-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8a71-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a71-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8a71-128">INPUTS</span></span>

### <span data-ttu-id="c8a71-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c8a71-129">System.String</span></span>

### <span data-ttu-id="c8a71-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c8a71-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="c8a71-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c8a71-131">OUTPUTS</span></span>

### <span data-ttu-id="c8a71-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="c8a71-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="c8a71-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="c8a71-133">NOTES</span></span>

## <span data-ttu-id="c8a71-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8a71-134">RELATED LINKS</span></span>
