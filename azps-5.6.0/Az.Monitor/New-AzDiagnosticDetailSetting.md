---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: cccc773adf4b70f0dcef077ea436963c0af9f190
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889457"
---
# <span data-ttu-id="10ac6-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="10ac6-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="10ac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="10ac6-103">Criar objeto PSDiagnosticDetailSetting, tipo pode ser métrica ou log</span><span class="sxs-lookup"><span data-stu-id="10ac6-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="10ac6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="10ac6-104">SYNTAX</span></span>

### <span data-ttu-id="10ac6-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="10ac6-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10ac6-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="10ac6-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10ac6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="10ac6-107">DESCRIPTION</span></span>
<span data-ttu-id="10ac6-108">Crie objeto PSMetricSettings ou PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="10ac6-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="10ac6-109">Você pode obter categorias usando `Get-AzDiagnosticSettingCategory` .</span><span class="sxs-lookup"><span data-stu-id="10ac6-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="10ac6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10ac6-110">EXAMPLES</span></span>

### <span data-ttu-id="10ac6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10ac6-111">Example 1</span></span>
```powershell
PS C:\> $TimeGrain=New-TimeSpan -Days 90
PS C:\> New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics -Enabled -TimeGrain $TimeGrain
TimeGrain       : 90.00:00:00
Category        : AllMetrics
Enabled         : True
RetentionPolicy :
                  Enabled : True
                  Days    : 1
CategoryType    : Metrics
```

<span data-ttu-id="10ac6-112">Criar objeto PSMetricSettings.</span><span class="sxs-lookup"><span data-stu-id="10ac6-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="10ac6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="10ac6-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="10ac6-114">Criar objeto PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="10ac6-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="10ac6-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="10ac6-115">PARAMETERS</span></span>

### <span data-ttu-id="10ac6-116">-Category</span><span class="sxs-lookup"><span data-stu-id="10ac6-116">-Category</span></span>
<span data-ttu-id="10ac6-117">Categoria de configuração</span><span class="sxs-lookup"><span data-stu-id="10ac6-117">Category of setting</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ac6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ac6-118">-DefaultProfile</span></span>
<span data-ttu-id="10ac6-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10ac6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10ac6-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="10ac6-120">-Enabled</span></span>
<span data-ttu-id="10ac6-121">Habilitar a configuração</span><span class="sxs-lookup"><span data-stu-id="10ac6-121">Enable the setting</span></span>

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

### <span data-ttu-id="10ac6-122">-Log</span><span class="sxs-lookup"><span data-stu-id="10ac6-122">-Log</span></span>
<span data-ttu-id="10ac6-123">Para criar a configuração de log</span><span class="sxs-lookup"><span data-stu-id="10ac6-123">To create log setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ac6-124">-Metric</span><span class="sxs-lookup"><span data-stu-id="10ac6-124">-Metric</span></span>
<span data-ttu-id="10ac6-125">Para criar configuração métrica</span><span class="sxs-lookup"><span data-stu-id="10ac6-125">To create metric setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ac6-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="10ac6-126">-RetentionEnabled</span></span>
<span data-ttu-id="10ac6-127">Habilitar política de retenção</span><span class="sxs-lookup"><span data-stu-id="10ac6-127">Enable Retention policy</span></span>

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

### <span data-ttu-id="10ac6-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="10ac6-128">-RetentionInDays</span></span>
<span data-ttu-id="10ac6-129">Dias de retenção para política de retenção</span><span class="sxs-lookup"><span data-stu-id="10ac6-129">Retention days for retention policy</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ac6-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="10ac6-130">-TimeGrain</span></span>
<span data-ttu-id="10ac6-131">TimeGrain para configuração métrica</span><span class="sxs-lookup"><span data-stu-id="10ac6-131">TimeGrain for metric setting</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ac6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ac6-132">CommonParameters</span></span>
<span data-ttu-id="10ac6-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ac6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ac6-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10ac6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ac6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10ac6-135">INPUTS</span></span>

### <span data-ttu-id="10ac6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="10ac6-136">System.String</span></span>

## <span data-ttu-id="10ac6-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="10ac6-137">OUTPUTS</span></span>

### <span data-ttu-id="10ac6-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="10ac6-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="10ac6-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="10ac6-139">NOTES</span></span>

## <span data-ttu-id="10ac6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10ac6-140">RELATED LINKS</span></span>
