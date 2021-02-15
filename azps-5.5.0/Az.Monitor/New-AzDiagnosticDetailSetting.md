---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117516"
---
# <span data-ttu-id="901ed-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="901ed-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="901ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="901ed-102">SYNOPSIS</span></span>
<span data-ttu-id="901ed-103">Criar objeto PSDiagnosticDetailSetting, o tipo pode ser métrico ou log</span><span class="sxs-lookup"><span data-stu-id="901ed-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="901ed-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="901ed-104">SYNTAX</span></span>

### <span data-ttu-id="901ed-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="901ed-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="901ed-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="901ed-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="901ed-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="901ed-107">DESCRIPTION</span></span>
<span data-ttu-id="901ed-108">Criar objeto PSMetricSettings ou PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="901ed-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="901ed-109">Você pode obter categorias usando `Get-AzDiagnosticSettingCategory` .</span><span class="sxs-lookup"><span data-stu-id="901ed-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="901ed-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="901ed-110">EXAMPLES</span></span>

### <span data-ttu-id="901ed-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="901ed-111">Example 1</span></span>
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

<span data-ttu-id="901ed-112">Criar objeto PSMetricSettings.</span><span class="sxs-lookup"><span data-stu-id="901ed-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="901ed-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="901ed-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="901ed-114">Criar objeto PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="901ed-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="901ed-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="901ed-115">PARAMETERS</span></span>

### <span data-ttu-id="901ed-116">-Categoria</span><span class="sxs-lookup"><span data-stu-id="901ed-116">-Category</span></span>
<span data-ttu-id="901ed-117">Categoria de configuração</span><span class="sxs-lookup"><span data-stu-id="901ed-117">Category of setting</span></span>

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

### <span data-ttu-id="901ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901ed-118">-DefaultProfile</span></span>
<span data-ttu-id="901ed-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="901ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="901ed-120">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="901ed-120">-Enabled</span></span>
<span data-ttu-id="901ed-121">Habilitar a configuração</span><span class="sxs-lookup"><span data-stu-id="901ed-121">Enable the setting</span></span>

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

### <span data-ttu-id="901ed-122">-Log</span><span class="sxs-lookup"><span data-stu-id="901ed-122">-Log</span></span>
<span data-ttu-id="901ed-123">Para criar configuração de log</span><span class="sxs-lookup"><span data-stu-id="901ed-123">To create log setting</span></span>

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

### <span data-ttu-id="901ed-124">-Métrica</span><span class="sxs-lookup"><span data-stu-id="901ed-124">-Metric</span></span>
<span data-ttu-id="901ed-125">Para criar configuração métrica</span><span class="sxs-lookup"><span data-stu-id="901ed-125">To create metric setting</span></span>

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

### <span data-ttu-id="901ed-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="901ed-126">-RetentionEnabled</span></span>
<span data-ttu-id="901ed-127">Habilitar política de retenção</span><span class="sxs-lookup"><span data-stu-id="901ed-127">Enable Retention policy</span></span>

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

### <span data-ttu-id="901ed-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="901ed-128">-RetentionInDays</span></span>
<span data-ttu-id="901ed-129">Dias de retenção para a política de retenção</span><span class="sxs-lookup"><span data-stu-id="901ed-129">Retention days for retention policy</span></span>

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

### <span data-ttu-id="901ed-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="901ed-130">-TimeGrain</span></span>
<span data-ttu-id="901ed-131">TimeGrain para configuração métrica</span><span class="sxs-lookup"><span data-stu-id="901ed-131">TimeGrain for metric setting</span></span>

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

### <span data-ttu-id="901ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901ed-132">CommonParameters</span></span>
<span data-ttu-id="901ed-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901ed-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="901ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901ed-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="901ed-135">INPUTS</span></span>

### <span data-ttu-id="901ed-136">System.String</span><span class="sxs-lookup"><span data-stu-id="901ed-136">System.String</span></span>

## <span data-ttu-id="901ed-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="901ed-137">OUTPUTS</span></span>

### <span data-ttu-id="901ed-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="901ed-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="901ed-139">Notas</span><span class="sxs-lookup"><span data-stu-id="901ed-139">NOTES</span></span>

## <span data-ttu-id="901ed-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="901ed-140">RELATED LINKS</span></span>
