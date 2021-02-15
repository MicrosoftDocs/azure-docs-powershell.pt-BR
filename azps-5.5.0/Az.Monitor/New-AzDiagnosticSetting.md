---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111754"
---
# <span data-ttu-id="0cda3-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0cda3-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="0cda3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cda3-102">SYNOPSIS</span></span>
<span data-ttu-id="0cda3-103">Criar objeto PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="0cda3-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="0cda3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cda3-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cda3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cda3-105">DESCRIPTION</span></span>
<span data-ttu-id="0cda3-106">Criar objeto PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="0cda3-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="0cda3-107">Isso pode ser usado como parâmetro `-InputObject` para `Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="0cda3-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="0cda3-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0cda3-108">EXAMPLES</span></span>

### <span data-ttu-id="0cda3-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0cda3-109">Example 1</span></span>
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

<span data-ttu-id="0cda3-110">Criar objeto PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="0cda3-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="0cda3-111">E crie uma configuração de diagnóstico para o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="0cda3-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="0cda3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cda3-112">PARAMETERS</span></span>

### <span data-ttu-id="0cda3-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="0cda3-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="0cda3-114">O valor que indica se você deve exportar (para ODS) para recursos específicos (se presentes) ou para a AzureDiagnostics (padrão, não apresentar)</span><span class="sxs-lookup"><span data-stu-id="0cda3-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cda3-115">-DefaultProfile</span></span>
<span data-ttu-id="0cda3-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0cda3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="0cda3-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="0cda3-118">A ID da regra do hub de evento</span><span class="sxs-lookup"><span data-stu-id="0cda3-118">The event hub rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="0cda3-119">-EventHubName</span></span>
<span data-ttu-id="0cda3-120">A ID da regra de barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="0cda3-120">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0cda3-121">-Name</span></span>
<span data-ttu-id="0cda3-122">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0cda3-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="0cda3-123">Padrões de "serviço"</span><span class="sxs-lookup"><span data-stu-id="0cda3-123">Defaults to 'service'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="0cda3-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="0cda3-125">A ID da regra de barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="0cda3-125">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-126">-Configuração</span><span class="sxs-lookup"><span data-stu-id="0cda3-126">-Setting</span></span>
<span data-ttu-id="0cda3-127">Configurações métricas ou configurações de Log</span><span class="sxs-lookup"><span data-stu-id="0cda3-127">Metric settings or Log settings</span></span>

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0cda3-128">-StorageAccountId</span></span>
<span data-ttu-id="0cda3-129">A ID da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0cda3-129">The storage account id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0cda3-130">-TargetResourceId</span></span>
<span data-ttu-id="0cda3-131">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="0cda3-131">The resource id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="0cda3-132">-WorkspaceId</span></span>
<span data-ttu-id="0cda3-133">A ID do recurso do espaço de trabalho Do Log Analytics para enviar logs/métricas para</span><span class="sxs-lookup"><span data-stu-id="0cda3-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cda3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cda3-134">CommonParameters</span></span>
<span data-ttu-id="0cda3-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cda3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cda3-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cda3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cda3-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="0cda3-137">INPUTS</span></span>

### <span data-ttu-id="0cda3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0cda3-138">System.String</span></span>

### <span data-ttu-id="0cda3-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0cda3-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0cda3-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span><span class="sxs-lookup"><span data-stu-id="0cda3-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="0cda3-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="0cda3-141">OUTPUTS</span></span>

### <span data-ttu-id="0cda3-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="0cda3-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="0cda3-143">Notas</span><span class="sxs-lookup"><span data-stu-id="0cda3-143">NOTES</span></span>

## <span data-ttu-id="0cda3-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cda3-144">RELATED LINKS</span></span>
