---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
ms.openlocfilehash: 772fe33dab13c4c92a0e17fc09a6bf1d5aa04624
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785237"
---
# <span data-ttu-id="47bf6-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="47bf6-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="47bf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="47bf6-103">Define as configurações de logs e métricas do recurso.</span><span class="sxs-lookup"><span data-stu-id="47bf6-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47bf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47bf6-104">SYNTAX</span></span>

### <span data-ttu-id="47bf6-105">OldSetDiagnosticSetting (padrão)</span><span class="sxs-lookup"><span data-stu-id="47bf6-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bf6-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="47bf6-106">NewSetDiagnosticSetting</span></span>
```
Set-AzureRmDiagnosticSetting -InputObject <PSServiceDiagnosticSettings>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47bf6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47bf6-107">DESCRIPTION</span></span>
<span data-ttu-id="47bf6-108">O cmdlet **set-AzureRmDiagnosticSetting** habilita ou desabilita cada intervalo de tempo e categoria de log para o recurso específico.</span><span class="sxs-lookup"><span data-stu-id="47bf6-108">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="47bf6-109">Os logs e as métricas são armazenados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="47bf6-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="47bf6-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="47bf6-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="47bf6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47bf6-111">EXAMPLES</span></span>

### <span data-ttu-id="47bf6-112">Exemplo 1: habilitar todas as métricas e registros para um recurso</span><span class="sxs-lookup"><span data-stu-id="47bf6-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="47bf6-113">Esse comando habilita todas as métricas e logs disponíveis para o Resource01.</span><span class="sxs-lookup"><span data-stu-id="47bf6-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="47bf6-114">Exemplo 2: desabilitar todas as métricas e registros</span><span class="sxs-lookup"><span data-stu-id="47bf6-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="47bf6-115">Esse comando desabilita todas as métricas e logs disponíveis para o recurso Resource01.</span><span class="sxs-lookup"><span data-stu-id="47bf6-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="47bf6-116">Exemplo 3: habilitar/desabilitar várias categorias de métricas</span><span class="sxs-lookup"><span data-stu-id="47bf6-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
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

<span data-ttu-id="47bf6-117">Esse comando habilita o cateories de métricas chamado Category1 e Category2.</span><span class="sxs-lookup"><span data-stu-id="47bf6-117">This command enables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="47bf6-118">Todas as outras categorias permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="47bf6-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="47bf6-119">Exemplo 4: habilitar/desabilitar várias categorias de log</span><span class="sxs-lookup"><span data-stu-id="47bf6-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
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

<span data-ttu-id="47bf6-120">Esse comando habilita Category1 e Category2.</span><span class="sxs-lookup"><span data-stu-id="47bf6-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="47bf6-121">Todas as outras categorias de métricas e registros permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="47bf6-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="47bf6-122">Exemplo 4: habilitar um intervalo de tempo e várias categorias</span><span class="sxs-lookup"><span data-stu-id="47bf6-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="47bf6-123">Esse comando habilita somente o Category1, o Category2 e o intervalo de tempo PT1M.</span><span class="sxs-lookup"><span data-stu-id="47bf6-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="47bf6-124">Todas as outras granularidades de tempo e categorias não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="47bf6-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="47bf6-125">Exemplo 5: usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="47bf6-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "Resource01" | Set-AzureRmDiagnosticSetting
```

<span data-ttu-id="47bf6-126">Esse comando usa o pipeline do PowerShell para definir (não alterações feitas) uma configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="47bf6-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="47bf6-127">OS</span><span class="sxs-lookup"><span data-stu-id="47bf6-127">PARAMETERS</span></span>

### <span data-ttu-id="47bf6-128">-Categorias</span><span class="sxs-lookup"><span data-stu-id="47bf6-128">-Categories</span></span>
<span data-ttu-id="47bf6-129">Especifica a lista de categorias de log para habilitar ou desabilitar, de acordo com o valor de *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="47bf6-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="47bf6-130">Se nenhuma categoria for especificada, esse comando funcionará em todas as categorias com suporte.</span><span class="sxs-lookup"><span data-stu-id="47bf6-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Category

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47bf6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47bf6-131">-DefaultProfile</span></span>
<span data-ttu-id="47bf6-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="47bf6-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47bf6-133">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="47bf6-133">-Enabled</span></span>
<span data-ttu-id="47bf6-134">Indica se os diagnósticos devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="47bf6-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="47bf6-135">Especifique $True para habilitar o diagnóstico ou $False para desabilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="47bf6-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="47bf6-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="47bf6-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="47bf6-137">A ID da regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="47bf6-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="47bf6-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="47bf6-138">-EventHubName</span></span>
<span data-ttu-id="47bf6-139">O nome do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="47bf6-139">The event hub name</span></span>

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

### <span data-ttu-id="47bf6-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47bf6-140">-InputObject</span></span>
<span data-ttu-id="47bf6-141">O objeto de entrada (possível no pipeline) O nome e o ResourceId serão extraídos deste objeto.</span><span class="sxs-lookup"><span data-stu-id="47bf6-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="47bf6-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="47bf6-142">-MetricCategory</span></span>
<span data-ttu-id="47bf6-143">A lista de categorias métricas.</span><span class="sxs-lookup"><span data-stu-id="47bf6-143">The list of metric categories.</span></span> <span data-ttu-id="47bf6-144">Se nenhuma categoria for especificada, esse comando funcionará em todas as categorias com suporte.</span><span class="sxs-lookup"><span data-stu-id="47bf6-144">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="47bf6-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="47bf6-145">-Name</span></span>
<span data-ttu-id="47bf6-146">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="47bf6-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="47bf6-147">O valor padrão é **serviço**.</span><span class="sxs-lookup"><span data-stu-id="47bf6-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="47bf6-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47bf6-148">-ResourceId</span></span>
<span data-ttu-id="47bf6-149">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="47bf6-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="47bf6-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="47bf6-150">-RetentionEnabled</span></span>
<span data-ttu-id="47bf6-151">Indica se a retenção de informações de diagnóstico está habilitada.</span><span class="sxs-lookup"><span data-stu-id="47bf6-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="47bf6-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="47bf6-152">-RetentionInDays</span></span>
<span data-ttu-id="47bf6-153">Especifica a política de retenção, em dias.</span><span class="sxs-lookup"><span data-stu-id="47bf6-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="47bf6-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="47bf6-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="47bf6-155">A ID da regra de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="47bf6-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="47bf6-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="47bf6-156">-StorageAccountId</span></span>
<span data-ttu-id="47bf6-157">Especifica a ID da conta de armazenamento na qual os dados são salvos.</span><span class="sxs-lookup"><span data-stu-id="47bf6-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="47bf6-158">-Refinamentos</span><span class="sxs-lookup"><span data-stu-id="47bf6-158">-Timegrains</span></span>
<span data-ttu-id="47bf6-159">Especifica o intervalo de tempo para habilitar ou desabilitar as métricas, de acordo com o valor de *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="47bf6-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="47bf6-160">Se você não especificar um intervalo de tempo, esse comando funcionará em todos os refinamentos de tempo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="47bf6-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Timegrain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47bf6-161">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="47bf6-161">-WorkspaceId</span></span>
<span data-ttu-id="47bf6-162">A ID do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="47bf6-162">The Id of the workspace</span></span>

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

### <span data-ttu-id="47bf6-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47bf6-163">-Confirm</span></span>
<span data-ttu-id="47bf6-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47bf6-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47bf6-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47bf6-165">-WhatIf</span></span>
<span data-ttu-id="47bf6-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47bf6-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47bf6-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47bf6-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47bf6-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47bf6-168">CommonParameters</span></span>
<span data-ttu-id="47bf6-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47bf6-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47bf6-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47bf6-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47bf6-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47bf6-171">INPUTS</span></span>

### <span data-ttu-id="47bf6-172">Microsoft. Azure. Commands. insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="47bf6-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>
<span data-ttu-id="47bf6-173">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="47bf6-173">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="47bf6-174">System. String</span><span class="sxs-lookup"><span data-stu-id="47bf6-174">System.String</span></span>

### <span data-ttu-id="47bf6-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47bf6-175">System.Boolean</span></span>

### <span data-ttu-id="47bf6-176">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="47bf6-176">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="47bf6-177">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="47bf6-177">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="47bf6-178">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="47bf6-178">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="47bf6-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47bf6-179">OUTPUTS</span></span>

### <span data-ttu-id="47bf6-180">Microsoft. Azure. Commands. insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="47bf6-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="47bf6-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47bf6-181">NOTES</span></span>

## <span data-ttu-id="47bf6-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47bf6-182">RELATED LINKS</span></span>

<span data-ttu-id="47bf6-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="47bf6-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
