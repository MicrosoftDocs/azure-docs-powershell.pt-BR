---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: d41d99993961906f88dc500603f74fc1a0d4fdf0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404914"
---
# <span data-ttu-id="f4bfa-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="f4bfa-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="f4bfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="f4bfa-103">Define as configurações de logs e métricas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="f4bfa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4bfa-104">SYNTAX</span></span>

### <span data-ttu-id="f4bfa-105">OldSetDiagnosticSetting (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f4bfa-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4bfa-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="f4bfa-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4bfa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4bfa-107">DESCRIPTION</span></span>
<span data-ttu-id="f4bfa-108">O cmdlet **Set-AzDiagnosticSetting** habilita ou desabilita cada categoria de granulação e log para o recurso específico.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="f4bfa-109">Os logs e as métricas são armazenados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="f4bfa-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f4bfa-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f4bfa-111">EXAMPLES</span></span>

### <span data-ttu-id="f4bfa-112">Exemplo 1: Habilitar todas as métricas e logs para um recurso</span><span class="sxs-lookup"><span data-stu-id="f4bfa-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="f4bfa-113">Esse comando habilita todas as métricas e logs disponíveis para Resource01.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="f4bfa-114">Exemplo 2: Desabilitar todas as métricas e logs</span><span class="sxs-lookup"><span data-stu-id="f4bfa-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="f4bfa-115">Esse comando desabilita todas as métricas e logs disponíveis para o recurso Resource01.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="f4bfa-116">Exemplo 3: Habilitar/desabilitar várias categorias de métricas</span><span class="sxs-lookup"><span data-stu-id="f4bfa-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
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

<span data-ttu-id="f4bfa-117">Esse comando desabilita as categorias de métricas chamadas Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="f4bfa-118">Todas as outras categorias permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="f4bfa-119">Exemplo 4: Habilitar/desabilitar várias categorias de log</span><span class="sxs-lookup"><span data-stu-id="f4bfa-119">Example 4: Enable/disable multiple log categories</span></span>
```
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

<span data-ttu-id="f4bfa-120">Esse comando habilita Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="f4bfa-121">Todas as outras categorias de logs e métricas permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="f4bfa-122">Exemplo 4: Habilitar uma hora e várias categorias</span><span class="sxs-lookup"><span data-stu-id="f4bfa-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="f4bfa-123">Esse comando habilita apenas Categoria1, Categoria2 e hora em PT1M.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="f4bfa-124">Todas as outras categorias e os outros tempos permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="f4bfa-125">Exemplo 5: usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="f4bfa-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting
```

<span data-ttu-id="f4bfa-126">Esse comando usa o pipeline do PowerShell para definir (não alterar feita) uma configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="f4bfa-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4bfa-127">PARAMETERS</span></span>

### <span data-ttu-id="f4bfa-128">-Categoria</span><span class="sxs-lookup"><span data-stu-id="f4bfa-128">-Category</span></span>
<span data-ttu-id="f4bfa-129">Especifica a lista de categorias de log para habilitar ou desabilitar, de acordo com o valor *de Enabled.*</span><span class="sxs-lookup"><span data-stu-id="f4bfa-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="f4bfa-130">Se nenhuma categoria for especificada, esse comando operará em todas as categorias com suporte.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-130">If no category is specified, this command operates on all supported categories.</span></span>

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

### <span data-ttu-id="f4bfa-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4bfa-131">-DefaultProfile</span></span>
<span data-ttu-id="f4bfa-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f4bfa-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4bfa-133">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="f4bfa-133">-Enabled</span></span>
<span data-ttu-id="f4bfa-134">Indica se você deve habilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="f4bfa-135">Especifique $True para habilitar o diagnóstico ou $False desabilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="f4bfa-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="f4bfa-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="f4bfa-137">A ID da regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="f4bfa-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="f4bfa-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="f4bfa-138">-EventHubName</span></span>
<span data-ttu-id="f4bfa-139">O nome do hub de evento</span><span class="sxs-lookup"><span data-stu-id="f4bfa-139">The event hub name</span></span>

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

### <span data-ttu-id="f4bfa-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4bfa-140">-InputObject</span></span>
<span data-ttu-id="f4bfa-141">O objeto de entrada (possível a partir do pipeline.) O nome e a IDdoprotetor serão extraídos deste objeto.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="f4bfa-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="f4bfa-142">-MetricCategory</span></span>
<span data-ttu-id="f4bfa-143">A lista de categorias métricas.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-143">The list of metric categories.</span></span>
<span data-ttu-id="f4bfa-144">Se nenhuma categoria for especificada, esse comando operará em todas as categorias com suporte.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-144">If no category is specified, this command operates on all supported categories.</span></span>

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

### <span data-ttu-id="f4bfa-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4bfa-145">-Name</span></span>
<span data-ttu-id="f4bfa-146">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="f4bfa-147">O valor padrão é **serviço.**</span><span class="sxs-lookup"><span data-stu-id="f4bfa-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="f4bfa-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4bfa-148">-ResourceId</span></span>
<span data-ttu-id="f4bfa-149">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="f4bfa-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="f4bfa-150">-RetentionEnabled</span></span>
<span data-ttu-id="f4bfa-151">Indica se a retenção de informações de diagnóstico está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="f4bfa-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f4bfa-152">-RetentionInDays</span></span>
<span data-ttu-id="f4bfa-153">Especifica a política de retenção em dias.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="f4bfa-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="f4bfa-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="f4bfa-155">A ID da Regra de BarraMento de Serviço.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="f4bfa-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f4bfa-156">-StorageAccountId</span></span>
<span data-ttu-id="f4bfa-157">Especifica a ID da conta de Armazenamento na qual os dados são armazenados.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="f4bfa-158">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="f4bfa-158">-Timegrain</span></span>
<span data-ttu-id="f4bfa-159">Especifica os tempos de tempo para habilitar ou desabilitar para métricas, de acordo com o valor *de Habilitado.*</span><span class="sxs-lookup"><span data-stu-id="f4bfa-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="f4bfa-160">Se você não especificar um tempo, esse comando operará em todos os tempos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="f4bfa-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="f4bfa-161">-WorkspaceId</span></span>
<span data-ttu-id="f4bfa-162">A ID do recurso do espaço de trabalho Do Log Analytics para enviar logs/métricas para</span><span class="sxs-lookup"><span data-stu-id="f4bfa-162">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="f4bfa-163">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f4bfa-163">-Confirm</span></span>
<span data-ttu-id="f4bfa-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4bfa-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4bfa-165">-WhatIf</span></span>
<span data-ttu-id="f4bfa-166">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4bfa-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4bfa-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4bfa-168">CommonParameters</span></span>
<span data-ttu-id="f4bfa-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4bfa-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4bfa-170">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4bfa-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4bfa-171">Entradas</span><span class="sxs-lookup"><span data-stu-id="f4bfa-171">INPUTS</span></span>

### <span data-ttu-id="f4bfa-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="f4bfa-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="f4bfa-173">System.String</span><span class="sxs-lookup"><span data-stu-id="f4bfa-173">System.String</span></span>

### <span data-ttu-id="f4bfa-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f4bfa-174">System.Boolean</span></span>

### <span data-ttu-id="f4bfa-175">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4bfa-175">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f4bfa-176">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4bfa-176">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f4bfa-177">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4bfa-177">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f4bfa-178">Saídas</span><span class="sxs-lookup"><span data-stu-id="f4bfa-178">OUTPUTS</span></span>

### <span data-ttu-id="f4bfa-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="f4bfa-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="f4bfa-180">Notas</span><span class="sxs-lookup"><span data-stu-id="f4bfa-180">NOTES</span></span>

## <span data-ttu-id="f4bfa-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4bfa-181">RELATED LINKS</span></span>

<span data-ttu-id="f4bfa-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="f4bfa-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
