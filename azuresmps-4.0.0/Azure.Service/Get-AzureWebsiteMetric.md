---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946271"
---
# <span data-ttu-id="83d86-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="83d86-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="83d86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83d86-102">SYNOPSIS</span></span>
<span data-ttu-id="83d86-103">Obtém métricas para o site do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="83d86-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="83d86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83d86-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="83d86-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83d86-105">DESCRIPTION</span></span>
<span data-ttu-id="83d86-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="83d86-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="83d86-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="83d86-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="83d86-108">O cmdlet **Get-AzureWebsiteMetric** Obtém métricas para o site do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="83d86-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="83d86-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83d86-109">EXAMPLES</span></span>

### <span data-ttu-id="83d86-110">Exemplo 1: obter métricas para as últimas três horas em um nível por instância para um site</span><span class="sxs-lookup"><span data-stu-id="83d86-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="83d86-111">Esse comando obtém métricas para as últimas três horas em um nível por instância de um site.</span><span class="sxs-lookup"><span data-stu-id="83d86-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="83d86-112">OS</span><span class="sxs-lookup"><span data-stu-id="83d86-112">PARAMETERS</span></span>

### <span data-ttu-id="83d86-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="83d86-113">-EndDate</span></span>
<span data-ttu-id="83d86-114">Especifica o tempo, como um objeto **DateTime** , para parar de obter métricas.</span><span class="sxs-lookup"><span data-stu-id="83d86-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="83d86-115">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="83d86-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="83d86-116">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="83d86-116">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="83d86-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="83d86-117">-InstanceDetails</span></span>
<span data-ttu-id="83d86-118">Indica que esse cmdlet inclui detalhes em nível por instância.</span><span class="sxs-lookup"><span data-stu-id="83d86-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="83d86-119">Se o plano de hospedagem na Web for executado em dois ou mais computadores, esse cmdlet retornará métricas para cada computador.</span><span class="sxs-lookup"><span data-stu-id="83d86-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

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

### <span data-ttu-id="83d86-120">-Metricnames</span><span class="sxs-lookup"><span data-stu-id="83d86-120">-MetricNames</span></span>
<span data-ttu-id="83d86-121">Especifica uma matriz de métricas a serem obtidas.</span><span class="sxs-lookup"><span data-stu-id="83d86-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="83d86-122">Se você não especificar esse parâmetro, o cmdlet obtém todas as métricas.</span><span class="sxs-lookup"><span data-stu-id="83d86-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

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

### <span data-ttu-id="83d86-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="83d86-123">-Name</span></span>
<span data-ttu-id="83d86-124">Especifica o nome de um site na assinatura.</span><span class="sxs-lookup"><span data-stu-id="83d86-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="83d86-125">Esse parâmetro não oferece suporte a caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="83d86-125">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="83d86-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="83d86-126">-Profile</span></span>
<span data-ttu-id="83d86-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="83d86-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83d86-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="83d86-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83d86-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="83d86-129">-Slot</span></span>
<span data-ttu-id="83d86-130">Especifica o ambiente de uma implantação de serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="83d86-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="83d86-131">Os valores válidos são: produção e preparação.</span><span class="sxs-lookup"><span data-stu-id="83d86-131">Valid values are: Production and Staging.</span></span>

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

### <span data-ttu-id="83d86-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="83d86-132">-SlotView</span></span>
<span data-ttu-id="83d86-133">Indica que esse cmdlet obtém métricas para os nomes de host que recebem tráfego no slot atual.</span><span class="sxs-lookup"><span data-stu-id="83d86-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="83d86-134">Se ocorrer uma troca durante o período de tempo, as métricas serão mescladas.</span><span class="sxs-lookup"><span data-stu-id="83d86-134">If a swap occurs during the time period, the metrics are merged.</span></span>

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

### <span data-ttu-id="83d86-135">-StartDate</span><span class="sxs-lookup"><span data-stu-id="83d86-135">-StartDate</span></span>
<span data-ttu-id="83d86-136">Especifica o tempo, como um objeto **DateTime** , para começar a obter métricas.</span><span class="sxs-lookup"><span data-stu-id="83d86-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

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

### <span data-ttu-id="83d86-137">-Timegranular</span><span class="sxs-lookup"><span data-stu-id="83d86-137">-TimeGrain</span></span>
<span data-ttu-id="83d86-138">Especifica a unidade de tempo para métricas.</span><span class="sxs-lookup"><span data-stu-id="83d86-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="83d86-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="83d86-139">Valid values are:</span></span> 

- <span data-ttu-id="83d86-140">PT1M (minuto)</span><span class="sxs-lookup"><span data-stu-id="83d86-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="83d86-141">PT1H (hora)</span><span class="sxs-lookup"><span data-stu-id="83d86-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="83d86-142">P1D (dia)</span><span class="sxs-lookup"><span data-stu-id="83d86-142">P1D (Day)</span></span>

<span data-ttu-id="83d86-143">O valor padrão é PT1H.</span><span class="sxs-lookup"><span data-stu-id="83d86-143">The default value is PT1H.</span></span>

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

### <span data-ttu-id="83d86-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d86-144">CommonParameters</span></span>
<span data-ttu-id="83d86-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d86-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d86-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d86-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d86-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83d86-147">INPUTS</span></span>

###  
<span data-ttu-id="83d86-148">Você pode passar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="83d86-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="83d86-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83d86-149">OUTPUTS</span></span>

### <span data-ttu-id="83d86-150">Microsoft. WindowsAzure. Commands. Utilities. sites. Services. webentities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="83d86-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="83d86-151">Por padrão, **Get-AzureWebsiteMetric** retorna uma matriz de objetos **MetricResponse** .</span><span class="sxs-lookup"><span data-stu-id="83d86-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="83d86-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83d86-152">NOTES</span></span>

## <span data-ttu-id="83d86-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83d86-153">RELATED LINKS</span></span>

[<span data-ttu-id="83d86-154">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="83d86-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


