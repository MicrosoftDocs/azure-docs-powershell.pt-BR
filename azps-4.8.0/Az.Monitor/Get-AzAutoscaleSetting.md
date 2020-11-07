---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 989CE245-FD1D-4E1D-90A2-2D7DA3975D0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleSetting.md
ms.openlocfilehash: 9cc5fe5d6b65a45b74244971566009d7b3a069eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955870"
---
# <span data-ttu-id="5d8d4-101">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5d8d4-101">Get-AzAutoscaleSetting</span></span>

## <span data-ttu-id="5d8d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d8d4-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8d4-103">Obtém as configurações de autoescala.</span><span class="sxs-lookup"><span data-stu-id="5d8d4-103">Gets Autoscale settings.</span></span>

## <span data-ttu-id="5d8d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d8d4-104">SYNTAX</span></span>

```
Get-AzAutoscaleSetting -ResourceGroupName <String> [-Name <String>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d8d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d8d4-105">DESCRIPTION</span></span>
<span data-ttu-id="5d8d4-106">O cmdlet **Get-AzAutoscaleSetting** obtém todas as configurações de autoescala associadas a um grupo de recursos ou uma configuração de autoescala especificada.</span><span class="sxs-lookup"><span data-stu-id="5d8d4-106">The **Get-AzAutoscaleSetting** cmdlet gets all Autoscale settings associated with a resource group or a specified Autoscale setting.</span></span>

## <span data-ttu-id="5d8d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d8d4-107">EXAMPLES</span></span>

### <span data-ttu-id="5d8d4-108">Exemplo 1: obter configurações de autoescala</span><span class="sxs-lookup"><span data-stu-id="5d8d4-108">Example 1: Get Autoscale settings</span></span>
```
PS C:\>Get-AzAutoscaleSetting -ResourceGroup "Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction        : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction  : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1

MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
                                                TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
                                                Direction  : Increase
Type       : ChangeCount
Value      : 1
             TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="5d8d4-109">Este comando obtém as configurações de autoescala atribuídas ao grupo de recursos padrão-Web-Lesteus.</span><span class="sxs-lookup"><span data-stu-id="5d8d4-109">This command gets the Autoscale settings assigned to the resource group Default-Web-EastUS.</span></span>

### <span data-ttu-id="5d8d4-110">Exemplo 2: obter uma configuração de autoescala por nome</span><span class="sxs-lookup"><span data-stu-id="5d8d4-110">Example 2: Get an Autoscale setting by name</span></span>
```
PS C:\>Get-AzAutoscaleSetting -ResourceGroupName "Default-Web-EastUS" -Name "DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="5d8d4-111">Esse comando obtém a configuração de autoescala chamada DefaultServerFarm-Default-Web-Eastus.</span><span class="sxs-lookup"><span data-stu-id="5d8d4-111">This command gets the Autoscale setting named DefaultServerFarm-Default-Web-EastUS.</span></span>

## <span data-ttu-id="5d8d4-112">OS</span><span class="sxs-lookup"><span data-stu-id="5d8d4-112">PARAMETERS</span></span>

### <span data-ttu-id="5d8d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8d4-113">-DefaultProfile</span></span>
<span data-ttu-id="5d8d4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5d8d4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d8d4-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="5d8d4-115">-DetailedOutput</span></span>
<span data-ttu-id="5d8d4-116">Indica que essa operação exibe detalhes completos na saída.</span><span class="sxs-lookup"><span data-stu-id="5d8d4-116">Indicates that this operation displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d8d4-117">-Name</span></span>
<span data-ttu-id="5d8d4-118">Especifica o nome da configuração a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="5d8d4-118">Specifies the name of the setting to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d8d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d8d4-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d8d4-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8d4-121">CommonParameters</span></span>
<span data-ttu-id="5d8d4-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d8d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8d4-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d8d4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8d4-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d8d4-124">INPUTS</span></span>

### <span data-ttu-id="5d8d4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5d8d4-125">System.String</span></span>

### <span data-ttu-id="5d8d4-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5d8d4-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5d8d4-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d8d4-127">OUTPUTS</span></span>

### <span data-ttu-id="5d8d4-128">Microsoft. Azure. Commands. insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5d8d4-128">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

## <span data-ttu-id="5d8d4-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d8d4-129">NOTES</span></span>

## <span data-ttu-id="5d8d4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d8d4-130">RELATED LINKS</span></span>

[<span data-ttu-id="5d8d4-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5d8d4-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="5d8d4-132">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5d8d4-132">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


