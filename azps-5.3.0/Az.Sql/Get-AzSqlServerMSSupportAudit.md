---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: c4f3687b2e520783c4b0392e1711dcea976e0c05
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426727"
---
# <span data-ttu-id="7532e-101">Get-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="7532e-101">Get-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="7532e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7532e-102">SYNOPSIS</span></span>
<span data-ttu-id="7532e-103">Obtém as configurações de auditoria de operações de suporte da Microsoft de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="7532e-103">Gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="7532e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7532e-104">SYNTAX</span></span>

### <span data-ttu-id="7532e-105">ServerParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7532e-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7532e-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7532e-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7532e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7532e-107">DESCRIPTION</span></span>
<span data-ttu-id="7532e-108">O cmdlet **Get-AzSqlServerMSSupportAudit** Obtém as configurações de auditoria de operações de suporte da Microsoft de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="7532e-108">The **Get-AzSqlServerMSSupportAudit** cmdlet gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="7532e-109">Especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="7532e-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="7532e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7532e-110">EXAMPLES</span></span>

### <span data-ttu-id="7532e-111">Exemplo 1: obter as configurações de auditoria de operações de suporte da Microsoft de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="7532e-111">Example 1: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7532e-112">Exemplo 2: obter, por meio de pipeline, as configurações de auditoria de operações de suporte da Microsoft de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="7532e-112">Example 2: Get, through pipeline, the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerMSSupportAudit
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7532e-113">Exemplo 3: obter as configurações de auditoria de operações de suporte da Microsoft de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="7532e-113">Example 3: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="7532e-114">OS</span><span class="sxs-lookup"><span data-stu-id="7532e-114">PARAMETERS</span></span>

### <span data-ttu-id="7532e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7532e-115">-AsJob</span></span>
<span data-ttu-id="7532e-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7532e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7532e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7532e-117">-DefaultProfile</span></span>
<span data-ttu-id="7532e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7532e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7532e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7532e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7532e-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7532e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7532e-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7532e-121">-ServerName</span></span>
<span data-ttu-id="7532e-122">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7532e-122">SQL server name.</span></span>

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

### <span data-ttu-id="7532e-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="7532e-123">-ServerObject</span></span>
<span data-ttu-id="7532e-124">O objeto do servidor para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7532e-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="7532e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7532e-125">CommonParameters</span></span>
<span data-ttu-id="7532e-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7532e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7532e-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7532e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7532e-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7532e-128">INPUTS</span></span>

### <span data-ttu-id="7532e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7532e-129">System.String</span></span>

### <span data-ttu-id="7532e-130">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="7532e-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="7532e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7532e-131">OUTPUTS</span></span>

### <span data-ttu-id="7532e-132">Microsoft. Azure. Commands. Sql. Auditing. Model. ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="7532e-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="7532e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7532e-133">NOTES</span></span>

## <span data-ttu-id="7532e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7532e-134">RELATED LINKS</span></span>
