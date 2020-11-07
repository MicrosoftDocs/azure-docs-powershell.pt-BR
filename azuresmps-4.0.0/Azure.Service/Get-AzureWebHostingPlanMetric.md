---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946510"
---
# <span data-ttu-id="e2e96-101">Get-AzureWebHostingPlanMetric</span><span class="sxs-lookup"><span data-stu-id="e2e96-101">Get-AzureWebHostingPlanMetric</span></span>

## <span data-ttu-id="e2e96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2e96-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e96-103">Obtém métricas para planos de Hospedagem de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e96-103">Gets metrics for Azure website hosting plans.</span></span>

## <span data-ttu-id="e2e96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2e96-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2e96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2e96-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e96-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2e96-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e2e96-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e2e96-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e2e96-108">O cmdlet **Get-AzureWebHostingPlanMetric** Obtém métricas para os planos de hospedagem da Web do Azure em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2e96-108">The **Get-AzureWebHostingPlanMetric** cmdlet gets metrics for Azure web hosting plans in a subscription.</span></span>

## <span data-ttu-id="e2e96-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2e96-109">EXAMPLES</span></span>

### <span data-ttu-id="e2e96-110">Exemplo 1: obter métricas para as últimas três horas em um nível por instância</span><span class="sxs-lookup"><span data-stu-id="e2e96-110">Example 1: Get metrics for the last three hours at a per-instance level</span></span>
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

<span data-ttu-id="e2e96-111">Este comando obtém as métricas do plano de hospedagem na Web para as últimas três horas em nível por instância.</span><span class="sxs-lookup"><span data-stu-id="e2e96-111">This command gets web hosting plan metrics for last three hours on per-instance level.</span></span>

## <span data-ttu-id="e2e96-112">OS</span><span class="sxs-lookup"><span data-stu-id="e2e96-112">PARAMETERS</span></span>

### <span data-ttu-id="e2e96-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e2e96-113">-EndDate</span></span>
<span data-ttu-id="e2e96-114">Especifica a hora de término, como um objeto **DateTime** , do qual as métricas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="e2e96-114">Specifies the end time, as a **DateTime** object, from which to return metrics.</span></span>
<span data-ttu-id="e2e96-115">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="e2e96-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="e2e96-116">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e2e96-116">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e96-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="e2e96-117">-InstanceDetails</span></span>
<span data-ttu-id="e2e96-118">Indica que esse cmdlet inclui detalhes em nível por instância.</span><span class="sxs-lookup"><span data-stu-id="e2e96-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="e2e96-119">Se o plano de hospedagem do site for executado em duas ou mais máquinas, esse cmdlet retornará as métricas detalhadas para cada máquina.</span><span class="sxs-lookup"><span data-stu-id="e2e96-119">If the website hosting plan runs on two or more machines, this cmdlet returns details metrics for each machine.</span></span>

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

### <span data-ttu-id="e2e96-120">-Metricnames</span><span class="sxs-lookup"><span data-stu-id="e2e96-120">-MetricNames</span></span>
<span data-ttu-id="e2e96-121">Especifica uma matriz de métricas a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="e2e96-121">Species an array of metrics to get.</span></span>
<span data-ttu-id="e2e96-122">Se você não especificar um valor para esse parâmetro, esse cmdlet obterá todas as métricas.</span><span class="sxs-lookup"><span data-stu-id="e2e96-122">If you do not specify a value for this parameter, this cmdlet gets all metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e96-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2e96-123">-Name</span></span>
<span data-ttu-id="e2e96-124">Especifica o nome de um plano na assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2e96-124">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="e2e96-125">Por padrão, **Get-AzureWebHostingPlanMetric** Obtém todos os sites na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e2e96-125">By default, **Get-AzureWebHostingPlanMetric** gets all websites in the current subscription.</span></span>
<span data-ttu-id="e2e96-126">Esse parâmetro não oferece suporte a caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="e2e96-126">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="e2e96-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e2e96-127">-Profile</span></span>
<span data-ttu-id="e2e96-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e2e96-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2e96-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e2e96-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e96-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e2e96-130">-StartDate</span></span>
<span data-ttu-id="e2e96-131">Especifica a hora de início, como um objeto **DateTime** , para o qual obter métricas.</span><span class="sxs-lookup"><span data-stu-id="e2e96-131">Specifies the start time, as a **DateTime** object, for which to get metrics.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e96-132">-Timegranular</span><span class="sxs-lookup"><span data-stu-id="e2e96-132">-TimeGrain</span></span>
<span data-ttu-id="e2e96-133">Especifica a unidade de tempo para a qual obter métricas.</span><span class="sxs-lookup"><span data-stu-id="e2e96-133">Specifies the time unit for which to get metrics.</span></span>
<span data-ttu-id="e2e96-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="e2e96-134">Valid values are:</span></span> 

- <span data-ttu-id="e2e96-135">PT1M (minuto)</span><span class="sxs-lookup"><span data-stu-id="e2e96-135">PT1M (Minute)</span></span> 
- <span data-ttu-id="e2e96-136">PT1H (hora)</span><span class="sxs-lookup"><span data-stu-id="e2e96-136">PT1H (Hour)</span></span> 
- <span data-ttu-id="e2e96-137">P1D (dia)</span><span class="sxs-lookup"><span data-stu-id="e2e96-137">P1D (Day)</span></span>

<span data-ttu-id="e2e96-138">O valor padrão é PT1H.</span><span class="sxs-lookup"><span data-stu-id="e2e96-138">The default value is PT1H.</span></span>

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

### <span data-ttu-id="e2e96-139">-Webspacename</span><span class="sxs-lookup"><span data-stu-id="e2e96-139">-WebSpaceName</span></span>
<span data-ttu-id="e2e96-140">Especifica o nome de um espaço da Web na assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2e96-140">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="e2e96-141">Por padrão, **Get-AzureWebHostingPlanMetric** Obtém todos os planos na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e2e96-141">By default, **Get-AzureWebHostingPlanMetric** gets all plans in the current subscription.</span></span>
<span data-ttu-id="e2e96-142">Esse parâmetro não oferece suporte a caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="e2e96-142">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e96-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e96-143">CommonParameters</span></span>
<span data-ttu-id="e2e96-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e96-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e96-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e96-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e96-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2e96-146">INPUTS</span></span>

###  
<span data-ttu-id="e2e96-147">Você pode passar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="e2e96-147">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="e2e96-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2e96-148">OUTPUTS</span></span>

###  
<span data-ttu-id="e2e96-149">Microsoft. WindowsAzure. Commands. Utilities. sites. Services. webentities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="e2e96-149">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>

<span data-ttu-id="e2e96-150">Por padrão, **Get-AzureWebHostingPlanMetric** retorna uma matriz de objetos **MetricResponse** .</span><span class="sxs-lookup"><span data-stu-id="e2e96-150">By default, **Get-AzureWebHostingPlanMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="e2e96-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2e96-151">NOTES</span></span>

## <span data-ttu-id="e2e96-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2e96-152">RELATED LINKS</span></span>

[<span data-ttu-id="e2e96-153">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="e2e96-153">Get-AzureWebHostingPlan</span></span>](./Get-AzureWebHostingPlan.md)


