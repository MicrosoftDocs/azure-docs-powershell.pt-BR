---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: fc2375e66dbc47ccadf11d0f7dd9dd66e42470de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609485"
---
# <span data-ttu-id="20340-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="20340-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="20340-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20340-102">SYNOPSIS</span></span>
<span data-ttu-id="20340-103">Modifica uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="20340-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20340-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20340-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20340-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20340-105">DESCRIPTION</span></span>
<span data-ttu-id="20340-106">O cmdlet **set-AzureRmSchedulerJobCollection** modifica uma coleção de trabalhos no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="20340-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="20340-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20340-107">EXAMPLES</span></span>

## <span data-ttu-id="20340-108">OS</span><span class="sxs-lookup"><span data-stu-id="20340-108">PARAMETERS</span></span>

### <span data-ttu-id="20340-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20340-109">-DefaultProfile</span></span>
<span data-ttu-id="20340-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20340-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20340-111">-Frequency</span><span class="sxs-lookup"><span data-stu-id="20340-111">-Frequency</span></span>
<span data-ttu-id="20340-112">Especifica a frequência máxima que você pode especificar em qualquer trabalho da coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="20340-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="20340-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="20340-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20340-114">Minuto</span><span class="sxs-lookup"><span data-stu-id="20340-114">Minute</span></span> 
- <span data-ttu-id="20340-115">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="20340-115">Hour</span></span> 
- <span data-ttu-id="20340-116">Contas</span><span class="sxs-lookup"><span data-stu-id="20340-116">Day</span></span> 
- <span data-ttu-id="20340-117">Emana</span><span class="sxs-lookup"><span data-stu-id="20340-117">Week</span></span> 
- <span data-ttu-id="20340-118">Mensais</span><span class="sxs-lookup"><span data-stu-id="20340-118">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20340-119">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="20340-119">-Interval</span></span>
<span data-ttu-id="20340-120">Especifica um intervalo de recorrência.</span><span class="sxs-lookup"><span data-stu-id="20340-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20340-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="20340-121">-JobCollectionName</span></span>
<span data-ttu-id="20340-122">Especifica o nome de uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="20340-122">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20340-123">-Local</span><span class="sxs-lookup"><span data-stu-id="20340-123">-Location</span></span>
<span data-ttu-id="20340-124">Especifica a região do Azure na qual existe a coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="20340-124">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="20340-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="20340-125">-MaxJobCount</span></span>
<span data-ttu-id="20340-126">Especifica o número máximo de trabalhos que você pode criar na coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="20340-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="20340-127">O máximo depende do plano que o parâmetro de *plano* especifica.</span><span class="sxs-lookup"><span data-stu-id="20340-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20340-128">-Plano</span><span class="sxs-lookup"><span data-stu-id="20340-128">-Plan</span></span>
<span data-ttu-id="20340-129">Especifica o plano de coleta de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="20340-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="20340-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="20340-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20340-131">Gratuito</span><span class="sxs-lookup"><span data-stu-id="20340-131">Free</span></span> 
- <span data-ttu-id="20340-132">Oficial</span><span class="sxs-lookup"><span data-stu-id="20340-132">Standard</span></span> 
- <span data-ttu-id="20340-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="20340-133">P10Premium</span></span> 
- <span data-ttu-id="20340-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="20340-134">P20Premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20340-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20340-135">-ResourceGroupName</span></span>
<span data-ttu-id="20340-136">Especifica o grupo de recursos da coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="20340-136">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="20340-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20340-137">-Confirm</span></span>
<span data-ttu-id="20340-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20340-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20340-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20340-139">-WhatIf</span></span>
<span data-ttu-id="20340-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20340-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20340-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20340-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20340-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20340-142">CommonParameters</span></span>
<span data-ttu-id="20340-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20340-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20340-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20340-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20340-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20340-145">INPUTS</span></span>

### <span data-ttu-id="20340-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="20340-146">None</span></span>
<span data-ttu-id="20340-147">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="20340-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20340-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20340-148">OUTPUTS</span></span>

### <span data-ttu-id="20340-149">Microsoft. Azure. Commands. scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="20340-149">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="20340-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20340-150">NOTES</span></span>

## <span data-ttu-id="20340-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20340-151">RELATED LINKS</span></span>

[<span data-ttu-id="20340-152">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="20340-152">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="20340-153">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="20340-153">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="20340-154">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="20340-154">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="20340-155">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="20340-155">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="20340-156">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="20340-156">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


