---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 623f52f1de9370c679f6df09b6cf05c50f38ca6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118928"
---
# <span data-ttu-id="e598d-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="e598d-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="e598d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e598d-102">SYNOPSIS</span></span>
<span data-ttu-id="e598d-103">Altera as configurações de auditoria de operações de suporte da Microsoft de um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e598d-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="e598d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e598d-104">SYNTAX</span></span>

### <span data-ttu-id="e598d-105">ServerParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e598d-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e598d-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e598d-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e598d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e598d-107">DESCRIPTION</span></span>
<span data-ttu-id="e598d-108">O cmdlet **Set-AzSqlServerMSSupportAudit** altera as configurações de auditoria de operações de suporte da Microsoft de um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e598d-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="e598d-109">Para usar o cmdlet, use os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="e598d-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="e598d-110">Quando o armazenamento de blob é um destino para logs de auditoria, especifique o parâmetro *StorageAccountResourceId* para determinar a conta de armazenamento dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="e598d-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="e598d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e598d-111">EXAMPLES</span></span>

### <span data-ttu-id="e598d-112">Exemplo 1: Habilitar a política de auditoria de operações de suporte de armazenamento de blob de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e598d-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="e598d-113">Exemplo 2: Desabilitar a política de auditoria de operações de suporte de armazenamento de blob de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e598d-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="e598d-114">Exemplo 3: Habilitar a política de auditoria de operações de suporte do hub de eventos da Microsoft de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e598d-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="e598d-115">Exemplo 4: desabilitar a política de auditoria de operações de suporte do hub de eventos da Microsoft de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e598d-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="e598d-116">Exemplo 5: Habilitar a política de auditoria de operações de suporte da Microsoft de análise de log de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e598d-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="e598d-117">Exemplo 6: desabilitar a política de auditoria de operações de suporte da Microsoft de análise de log de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e598d-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="e598d-118">Exemplo 7: Desabilitar, por meio do pipeline, a política de auditoria de operações de suporte de análise de log da Microsoft de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e598d-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="e598d-119">Exemplo 8: desabilitar o envio de registros de auditoria de operações de suporte da Microsoft de um servidor SQL do Azure para blob armazenamento e habilitar o envio para análise de log.</span><span class="sxs-lookup"><span data-stu-id="e598d-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="e598d-120">Exemplo 9: Habilitar o envio de registros de auditoria de operações de suporte da Microsoft de um servidor SQL do Azure para blob armazenamento, hub de eventos e análise de log.</span><span class="sxs-lookup"><span data-stu-id="e598d-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="e598d-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e598d-121">PARAMETERS</span></span>

### <span data-ttu-id="e598d-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e598d-122">-AsJob</span></span>
<span data-ttu-id="e598d-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e598d-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e598d-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="e598d-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="e598d-125">Indica se o armazenamento de blob é um destino para registros de auditoria de operações de suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e598d-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e598d-126">-DefaultProfile</span></span>
<span data-ttu-id="e598d-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e598d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e598d-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="e598d-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="e598d-129">A ID do recurso para a regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="e598d-129">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598d-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="e598d-130">-EventHubName</span></span>
<span data-ttu-id="e598d-131">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="e598d-131">The name of the event hub.</span></span> <span data-ttu-id="e598d-132">Se nenhum for especificado ao fornecer EventHubAuthorizationRuleResourceId, o hub de eventos padrão será selecionado.</span><span class="sxs-lookup"><span data-stu-id="e598d-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598d-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="e598d-133">-EventHubTargetState</span></span>
<span data-ttu-id="e598d-134">Indica se o hub de eventos é um destino para registros de auditoria de operações de suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e598d-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598d-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="e598d-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="e598d-136">Indica se a análise de log é um destino para registros de auditoria de operações de suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e598d-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598d-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e598d-137">-PassThru</span></span>
<span data-ttu-id="e598d-138">Especifica se a política de auditoria de operações de suporte da Microsoft será saída no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="e598d-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="e598d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e598d-139">-ResourceGroupName</span></span>
<span data-ttu-id="e598d-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e598d-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="e598d-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e598d-141">-ServerName</span></span>
<span data-ttu-id="e598d-142">Nome do servidor SQL.</span><span class="sxs-lookup"><span data-stu-id="e598d-142">SQL server name.</span></span>

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

### <span data-ttu-id="e598d-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="e598d-143">-ServerObject</span></span>
<span data-ttu-id="e598d-144">O objeto do servidor para gerenciar sua política de auditoria de operações de suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e598d-144">The server object to manage its Microsoft support operations audit policy.</span></span>

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

### <span data-ttu-id="e598d-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e598d-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="e598d-146">A ID de recurso da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e598d-146">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598d-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="e598d-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="e598d-148">A ID do espaço de trabalho (ID de recurso de um espaço de trabalho do Log Analytics) de um espaço de trabalho do Log Analytics para o qual você gostaria de enviar Logs de Auditoria das operações de suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e598d-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="e598d-149">Exemplo: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="e598d-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e598d-150">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e598d-150">-Confirm</span></span>
<span data-ttu-id="e598d-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e598d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e598d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e598d-152">-WhatIf</span></span>
<span data-ttu-id="e598d-153">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e598d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e598d-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e598d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e598d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e598d-155">CommonParameters</span></span>
<span data-ttu-id="e598d-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e598d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e598d-157">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e598d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e598d-158">Entradas</span><span class="sxs-lookup"><span data-stu-id="e598d-158">INPUTS</span></span>

### <span data-ttu-id="e598d-159">System.String</span><span class="sxs-lookup"><span data-stu-id="e598d-159">System.String</span></span>

### <span data-ttu-id="e598d-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="e598d-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="e598d-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e598d-161">System.Guid</span></span>

### <span data-ttu-id="e598d-162">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e598d-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e598d-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="e598d-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="e598d-164">Saídas</span><span class="sxs-lookup"><span data-stu-id="e598d-164">OUTPUTS</span></span>

### <span data-ttu-id="e598d-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e598d-165">System.Boolean</span></span>

## <span data-ttu-id="e598d-166">Notas</span><span class="sxs-lookup"><span data-stu-id="e598d-166">NOTES</span></span>

## <span data-ttu-id="e598d-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e598d-167">RELATED LINKS</span></span>
