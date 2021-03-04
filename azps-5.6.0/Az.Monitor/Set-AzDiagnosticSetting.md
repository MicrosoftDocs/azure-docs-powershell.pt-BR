---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 148986d5ab16e4791a4c886f5ba4557b6dc90fba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886441"
---
# <span data-ttu-id="29926-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="29926-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="29926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29926-102">SYNOPSIS</span></span>
<span data-ttu-id="29926-103">Define as configurações de logs e métricas do recurso.</span><span class="sxs-lookup"><span data-stu-id="29926-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="29926-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="29926-104">SYNTAX</span></span>

### <span data-ttu-id="29926-105">OldSetDiagnosticSetting (Padrão)</span><span class="sxs-lookup"><span data-stu-id="29926-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-ExportToResourceSpecific] [-EnableLog <Boolean>]
 [-EnableMetrics <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29926-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="29926-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29926-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="29926-107">DESCRIPTION</span></span>
<span data-ttu-id="29926-108">O cmdlet **Set-AzDiagnosticSetting** habilita ou desabilita cada categoria de granulação e log para o recurso específico.</span><span class="sxs-lookup"><span data-stu-id="29926-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="29926-109">Os logs e as métricas são armazenados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="29926-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="29926-110">Este cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="29926-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="29926-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29926-111">EXAMPLES</span></span>

### <span data-ttu-id="29926-112">Exemplo 1: Habilitar todas as métricas e logs para um recurso</span><span class="sxs-lookup"><span data-stu-id="29926-112">Example 1: Enable all metrics and logs for a resource</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="29926-113">Esse comando habilita todas as métricas e logs disponíveis para Resource01.</span><span class="sxs-lookup"><span data-stu-id="29926-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="29926-114">Exemplo 2: Desabilitar todas as métricas e logs</span><span class="sxs-lookup"><span data-stu-id="29926-114">Example 2: Disable all metrics and logs</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="29926-115">Este comando desabilita todas as métricas e logs disponíveis para o recurso Resource01.</span><span class="sxs-lookup"><span data-stu-id="29926-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="29926-116">Exemplo 3: Habilitar/desabilitar várias categorias de métricas</span><span class="sxs-lookup"><span data-stu-id="29926-116">Example 3: Enable/disable multiple metrics categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="29926-117">Este comando desabilita as categorias de métricas chamadas Category1 e Category2.</span><span class="sxs-lookup"><span data-stu-id="29926-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="29926-118">Todas as outras categorias permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="29926-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="29926-119">Exemplo 4: Habilitar/desabilitar várias categorias de log</span><span class="sxs-lookup"><span data-stu-id="29926-119">Example 4: Enable/disable multiple log categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="29926-120">Este comando habilita Category1 e Category2.</span><span class="sxs-lookup"><span data-stu-id="29926-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="29926-121">Todas as outras categorias de métricas e logs permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="29926-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="29926-122">Exemplo 5: Habilitar um grain de tempo e várias categorias</span><span class="sxs-lookup"><span data-stu-id="29926-122">Example 5: Enable a time grain and multiple categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="29926-123">Este comando habilita apenas Category1, Category2 e time grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="29926-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="29926-124">Todas as outras categorias e grãos de tempo não são alterados.</span><span class="sxs-lookup"><span data-stu-id="29926-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="29926-125">Exemplo 6: Usando pipeline</span><span class="sxs-lookup"><span data-stu-id="29926-125">Example 6: Using pipeline</span></span>
```powershell
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="29926-126">Este comando usa o pipeline do PowerShell para definir (nenhuma alteração feita) uma configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="29926-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="29926-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="29926-127">PARAMETERS</span></span>

### <span data-ttu-id="29926-128">-Category</span><span class="sxs-lookup"><span data-stu-id="29926-128">-Category</span></span>
<span data-ttu-id="29926-129">Especifica a lista de categorias de log para habilitar ou desabilitar, de acordo com o valor *de Enabled*.</span><span class="sxs-lookup"><span data-stu-id="29926-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="29926-130">Se nenhuma categoria for especificada, esse comando operará em todas as categorias suportadas.</span><span class="sxs-lookup"><span data-stu-id="29926-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29926-131">-DefaultProfile</span></span>
<span data-ttu-id="29926-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="29926-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29926-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="29926-133">-Enabled</span></span>
<span data-ttu-id="29926-134">Indica se é possível habilitar diagnósticos.</span><span class="sxs-lookup"><span data-stu-id="29926-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="29926-135">Especifique $True para habilitar diagnósticos ou $False desabilitar diagnósticos.</span><span class="sxs-lookup"><span data-stu-id="29926-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-136">-EnableLog</span><span class="sxs-lookup"><span data-stu-id="29926-136">-EnableLog</span></span>
<span data-ttu-id="29926-137">O valor que indica se os logs de diagnóstico devem ser habilitados ou desabilitados</span><span class="sxs-lookup"><span data-stu-id="29926-137">The value indicating whether the diagnostic logs should be enabled or disabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-138">-EnableMetrics</span><span class="sxs-lookup"><span data-stu-id="29926-138">-EnableMetrics</span></span>
<span data-ttu-id="29926-139">O valor que indica se as métricas de diagnóstico devem ser habilitadas ou desabilitadas</span><span class="sxs-lookup"><span data-stu-id="29926-139">The value indicating whether the diagnostic metrics should be enabled or disabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-140">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="29926-140">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="29926-141">A ID da regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="29926-141">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-142">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="29926-142">-EventHubName</span></span>
<span data-ttu-id="29926-143">O nome do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="29926-143">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-144">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="29926-144">-ExportToResourceSpecific</span></span>
<span data-ttu-id="29926-145">Sinalizador indicando que a exportação para LA deve ser feita para uma tabela específica do recurso, a.k.a.</span><span class="sxs-lookup"><span data-stu-id="29926-145">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="29926-146">tabela de esquema dedicada ou fixa, em vez da **tabela** de esquema dinâmica padrão chamada **AzureDiagnostics**.</span><span class="sxs-lookup"><span data-stu-id="29926-146">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="29926-147">Esse argumento só é eficaz quando o argumento **-workspaceId** também é dado.</span><span class="sxs-lookup"><span data-stu-id="29926-147">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29926-148">-InputObject</span></span>
<span data-ttu-id="29926-149">O objeto de entrada (possível a partir do pipeline.) O nome e resourceId serão extraídos deste objeto.</span><span class="sxs-lookup"><span data-stu-id="29926-149">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-150">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="29926-150">-MetricCategory</span></span>
<span data-ttu-id="29926-151">A lista de categorias métricas.</span><span class="sxs-lookup"><span data-stu-id="29926-151">The list of metric categories.</span></span> <span data-ttu-id="29926-152">Se nenhuma categoria for especificada, esse comando operará em todas as categorias suportadas.</span><span class="sxs-lookup"><span data-stu-id="29926-152">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-153">-Name</span><span class="sxs-lookup"><span data-stu-id="29926-153">-Name</span></span>
<span data-ttu-id="29926-154">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="29926-154">The name of the diagnostic setting.</span></span> <span data-ttu-id="29926-155">O valor padrão é **serviço**.</span><span class="sxs-lookup"><span data-stu-id="29926-155">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-156">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29926-156">-ResourceId</span></span>
<span data-ttu-id="29926-157">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="29926-157">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-158">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="29926-158">-RetentionEnabled</span></span>
<span data-ttu-id="29926-159">Indica se a retenção de informações de diagnóstico está habilitada.</span><span class="sxs-lookup"><span data-stu-id="29926-159">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-160">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="29926-160">-RetentionInDays</span></span>
<span data-ttu-id="29926-161">Especifica a política de retenção, em dias.</span><span class="sxs-lookup"><span data-stu-id="29926-161">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-162">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="29926-162">-ServiceBusRuleId</span></span>
<span data-ttu-id="29926-163">A ID da Regra de Barramento de Serviço.</span><span class="sxs-lookup"><span data-stu-id="29926-163">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-164">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="29926-164">-StorageAccountId</span></span>
<span data-ttu-id="29926-165">Especifica a ID da conta de armazenamento na qual os dados serão salvo.</span><span class="sxs-lookup"><span data-stu-id="29926-165">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-166">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="29926-166">-Timegrain</span></span>
<span data-ttu-id="29926-167">Especifica os grãos de tempo para habilitar ou desabilitar métricas, de acordo com o valor *de Enabled*.</span><span class="sxs-lookup"><span data-stu-id="29926-167">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="29926-168">Se você não especificar um grain de hora, este comando operará em todos os grãos de tempo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="29926-168">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-169">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="29926-169">-WorkspaceId</span></span>
<span data-ttu-id="29926-170">A ID de recurso do espaço de trabalho do Log Analytics para enviar logs/métricas para</span><span class="sxs-lookup"><span data-stu-id="29926-170">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29926-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29926-171">-Confirm</span></span>
<span data-ttu-id="29926-172">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29926-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29926-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29926-173">-WhatIf</span></span>
<span data-ttu-id="29926-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29926-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29926-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29926-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29926-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29926-176">CommonParameters</span></span>
<span data-ttu-id="29926-177">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29926-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29926-178">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29926-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29926-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29926-179">INPUTS</span></span>

### <span data-ttu-id="29926-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="29926-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="29926-181">System.String</span><span class="sxs-lookup"><span data-stu-id="29926-181">System.String</span></span>

### <span data-ttu-id="29926-182">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29926-182">System.Boolean</span></span>

### <span data-ttu-id="29926-183">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="29926-183">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="29926-184">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="29926-184">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="29926-185">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="29926-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="29926-186">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="29926-186">OUTPUTS</span></span>

### <span data-ttu-id="29926-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="29926-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="29926-188">NOTES</span><span class="sxs-lookup"><span data-stu-id="29926-188">NOTES</span></span>

## <span data-ttu-id="29926-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29926-189">RELATED LINKS</span></span>

<span data-ttu-id="29926-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="29926-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
