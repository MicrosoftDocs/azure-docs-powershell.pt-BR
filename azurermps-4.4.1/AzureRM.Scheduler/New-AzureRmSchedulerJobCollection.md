---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433012"
---
# <span data-ttu-id="7974d-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7974d-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="7974d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7974d-102">SYNOPSIS</span></span>
<span data-ttu-id="7974d-103">Cria uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="7974d-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7974d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7974d-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7974d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7974d-105">DESCRIPTION</span></span>
<span data-ttu-id="7974d-106">O cmdlet **New-AzureRmSchedulerJobCollection** cria uma coleção de trabalhos no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="7974d-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="7974d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7974d-107">EXAMPLES</span></span>

## <span data-ttu-id="7974d-108">OS</span><span class="sxs-lookup"><span data-stu-id="7974d-108">PARAMETERS</span></span>

### <span data-ttu-id="7974d-109">-Frequency</span><span class="sxs-lookup"><span data-stu-id="7974d-109">-Frequency</span></span>
<span data-ttu-id="7974d-110">Especifica a frequência máxima que você pode especificar em qualquer trabalho da coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="7974d-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="7974d-111">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7974d-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7974d-112">Minuto</span><span class="sxs-lookup"><span data-stu-id="7974d-112">Minute</span></span> 
- <span data-ttu-id="7974d-113">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="7974d-113">Hour</span></span> 
- <span data-ttu-id="7974d-114">Contas</span><span class="sxs-lookup"><span data-stu-id="7974d-114">Day</span></span> 
- <span data-ttu-id="7974d-115">Emana</span><span class="sxs-lookup"><span data-stu-id="7974d-115">Week</span></span> 
- <span data-ttu-id="7974d-116">Mensais</span><span class="sxs-lookup"><span data-stu-id="7974d-116">Month</span></span>

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

### <span data-ttu-id="7974d-117">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="7974d-117">-Interval</span></span>
<span data-ttu-id="7974d-118">Especifica um intervalo de recorrência.</span><span class="sxs-lookup"><span data-stu-id="7974d-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="7974d-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7974d-119">-JobCollectionName</span></span>
<span data-ttu-id="7974d-120">Especifica um nome para a coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="7974d-120">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="7974d-121">-Local</span><span class="sxs-lookup"><span data-stu-id="7974d-121">-Location</span></span>
<span data-ttu-id="7974d-122">Especifica a região do Azure na qual esse cmdlet cria a coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="7974d-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="7974d-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="7974d-123">-MaxJobCount</span></span>
<span data-ttu-id="7974d-124">Especifica o número máximo de trabalhos que você pode criar na coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="7974d-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="7974d-125">O máximo depende do plano que o parâmetro de *plano* especifica.</span><span class="sxs-lookup"><span data-stu-id="7974d-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="7974d-126">-Plano</span><span class="sxs-lookup"><span data-stu-id="7974d-126">-Plan</span></span>
<span data-ttu-id="7974d-127">Especifica o plano de coleta de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="7974d-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="7974d-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7974d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7974d-129">Gratuito</span><span class="sxs-lookup"><span data-stu-id="7974d-129">Free</span></span> 
- <span data-ttu-id="7974d-130">Oficial</span><span class="sxs-lookup"><span data-stu-id="7974d-130">Standard</span></span> 
- <span data-ttu-id="7974d-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="7974d-131">P10Premium</span></span> 
- <span data-ttu-id="7974d-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="7974d-132">P20Premium</span></span>

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

### <span data-ttu-id="7974d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7974d-133">-ResourceGroupName</span></span>
<span data-ttu-id="7974d-134">Especifica o grupo de recursos para a coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="7974d-134">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="7974d-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7974d-135">-Confirm</span></span>
<span data-ttu-id="7974d-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7974d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7974d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7974d-137">-WhatIf</span></span>
<span data-ttu-id="7974d-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7974d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7974d-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7974d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7974d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7974d-140">-DefaultProfile</span></span>
<span data-ttu-id="7974d-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7974d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7974d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7974d-142">CommonParameters</span></span>
<span data-ttu-id="7974d-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7974d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7974d-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7974d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7974d-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7974d-145">INPUTS</span></span>

## <span data-ttu-id="7974d-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7974d-146">OUTPUTS</span></span>

### <span data-ttu-id="7974d-147">Microsoft. Azure. Commands. scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="7974d-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="7974d-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7974d-148">NOTES</span></span>

## <span data-ttu-id="7974d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7974d-149">RELATED LINKS</span></span>

[<span data-ttu-id="7974d-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7974d-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7974d-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7974d-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7974d-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7974d-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7974d-153">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7974d-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7974d-154">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7974d-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


