---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 479b91f222852ebfc356d320cf880eb2ae99db6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428362"
---
# <span data-ttu-id="8c960-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c960-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="8c960-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c960-102">SYNOPSIS</span></span>
<span data-ttu-id="8c960-103">Cria uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8c960-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c960-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c960-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c960-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c960-105">DESCRIPTION</span></span>
<span data-ttu-id="8c960-106">O cmdlet **New-AzureRmSchedulerJobCollection** cria uma coleção de trabalhos no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c960-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="8c960-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c960-107">EXAMPLES</span></span>

## <span data-ttu-id="8c960-108">OS</span><span class="sxs-lookup"><span data-stu-id="8c960-108">PARAMETERS</span></span>

### <span data-ttu-id="8c960-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c960-109">-DefaultProfile</span></span>
<span data-ttu-id="8c960-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c960-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c960-111">-Frequency</span><span class="sxs-lookup"><span data-stu-id="8c960-111">-Frequency</span></span>
<span data-ttu-id="8c960-112">Especifica a frequência máxima que você pode especificar em qualquer trabalho da coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8c960-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="8c960-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8c960-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8c960-114">Minuto</span><span class="sxs-lookup"><span data-stu-id="8c960-114">Minute</span></span> 
- <span data-ttu-id="8c960-115">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="8c960-115">Hour</span></span> 
- <span data-ttu-id="8c960-116">Contas</span><span class="sxs-lookup"><span data-stu-id="8c960-116">Day</span></span> 
- <span data-ttu-id="8c960-117">Emana</span><span class="sxs-lookup"><span data-stu-id="8c960-117">Week</span></span> 
- <span data-ttu-id="8c960-118">Mensais</span><span class="sxs-lookup"><span data-stu-id="8c960-118">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c960-119">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="8c960-119">-Interval</span></span>
<span data-ttu-id="8c960-120">Especifica um intervalo de recorrência.</span><span class="sxs-lookup"><span data-stu-id="8c960-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c960-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8c960-121">-JobCollectionName</span></span>
<span data-ttu-id="8c960-122">Especifica um nome para a coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8c960-122">Specifies a name for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c960-123">-Local</span><span class="sxs-lookup"><span data-stu-id="8c960-123">-Location</span></span>
<span data-ttu-id="8c960-124">Especifica a região do Azure na qual esse cmdlet cria a coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8c960-124">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c960-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="8c960-125">-MaxJobCount</span></span>
<span data-ttu-id="8c960-126">Especifica o número máximo de trabalhos que você pode criar na coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8c960-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="8c960-127">O máximo depende do plano que o parâmetro de *plano* especifica.</span><span class="sxs-lookup"><span data-stu-id="8c960-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c960-128">-Plano</span><span class="sxs-lookup"><span data-stu-id="8c960-128">-Plan</span></span>
<span data-ttu-id="8c960-129">Especifica o plano de coleta de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8c960-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="8c960-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8c960-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8c960-131">Gratuito</span><span class="sxs-lookup"><span data-stu-id="8c960-131">Free</span></span> 
- <span data-ttu-id="8c960-132">Oficial</span><span class="sxs-lookup"><span data-stu-id="8c960-132">Standard</span></span> 
- <span data-ttu-id="8c960-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="8c960-133">P10Premium</span></span> 
- <span data-ttu-id="8c960-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="8c960-134">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c960-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c960-135">-ResourceGroupName</span></span>
<span data-ttu-id="8c960-136">Especifica o grupo de recursos para a coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8c960-136">Specifies the resource group for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c960-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c960-137">-Confirm</span></span>
<span data-ttu-id="8c960-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c960-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c960-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c960-139">-WhatIf</span></span>
<span data-ttu-id="8c960-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c960-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c960-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c960-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c960-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c960-142">CommonParameters</span></span>
<span data-ttu-id="8c960-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c960-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c960-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c960-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c960-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c960-145">INPUTS</span></span>

### <span data-ttu-id="8c960-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8c960-146">System.String</span></span>

## <span data-ttu-id="8c960-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c960-147">OUTPUTS</span></span>

### <span data-ttu-id="8c960-148">Microsoft. Azure. Commands. scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="8c960-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="8c960-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c960-149">NOTES</span></span>

## <span data-ttu-id="8c960-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c960-150">RELATED LINKS</span></span>

[<span data-ttu-id="8c960-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c960-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c960-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c960-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c960-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c960-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c960-154">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c960-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c960-155">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c960-155">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


