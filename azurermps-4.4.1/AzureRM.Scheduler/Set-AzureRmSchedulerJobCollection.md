---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 141a91272e805cc30f290d544a9a33c7c81484e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609561"
---
# <span data-ttu-id="1a268-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1a268-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="1a268-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a268-102">SYNOPSIS</span></span>
<span data-ttu-id="1a268-103">Modifica uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1a268-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a268-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a268-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a268-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a268-105">DESCRIPTION</span></span>
<span data-ttu-id="1a268-106">O cmdlet **set-AzureRmSchedulerJobCollection** modifica uma coleção de trabalhos no Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a268-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="1a268-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a268-107">EXAMPLES</span></span>

## <span data-ttu-id="1a268-108">OS</span><span class="sxs-lookup"><span data-stu-id="1a268-108">PARAMETERS</span></span>

### <span data-ttu-id="1a268-109">-Frequency</span><span class="sxs-lookup"><span data-stu-id="1a268-109">-Frequency</span></span>
<span data-ttu-id="1a268-110">Especifica a frequência máxima que você pode especificar em qualquer trabalho da coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1a268-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="1a268-111">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a268-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a268-112">Minuto</span><span class="sxs-lookup"><span data-stu-id="1a268-112">Minute</span></span> 
- <span data-ttu-id="1a268-113">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="1a268-113">Hour</span></span> 
- <span data-ttu-id="1a268-114">Contas</span><span class="sxs-lookup"><span data-stu-id="1a268-114">Day</span></span> 
- <span data-ttu-id="1a268-115">Emana</span><span class="sxs-lookup"><span data-stu-id="1a268-115">Week</span></span> 
- <span data-ttu-id="1a268-116">Mensais</span><span class="sxs-lookup"><span data-stu-id="1a268-116">Month</span></span>

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

### <span data-ttu-id="1a268-117">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="1a268-117">-Interval</span></span>
<span data-ttu-id="1a268-118">Especifica um intervalo de recorrência.</span><span class="sxs-lookup"><span data-stu-id="1a268-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="1a268-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="1a268-119">-JobCollectionName</span></span>
<span data-ttu-id="1a268-120">Especifica o nome de uma coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1a268-120">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="1a268-121">-Local</span><span class="sxs-lookup"><span data-stu-id="1a268-121">-Location</span></span>
<span data-ttu-id="1a268-122">Especifica a região do Azure na qual existe a coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1a268-122">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="1a268-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="1a268-123">-MaxJobCount</span></span>
<span data-ttu-id="1a268-124">Especifica o número máximo de trabalhos que você pode criar na coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1a268-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="1a268-125">O máximo depende do plano que o parâmetro de *plano* especifica.</span><span class="sxs-lookup"><span data-stu-id="1a268-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="1a268-126">-Plano</span><span class="sxs-lookup"><span data-stu-id="1a268-126">-Plan</span></span>
<span data-ttu-id="1a268-127">Especifica o plano de coleta de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1a268-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="1a268-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1a268-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a268-129">Gratuito</span><span class="sxs-lookup"><span data-stu-id="1a268-129">Free</span></span> 
- <span data-ttu-id="1a268-130">Oficial</span><span class="sxs-lookup"><span data-stu-id="1a268-130">Standard</span></span> 
- <span data-ttu-id="1a268-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="1a268-131">P10Premium</span></span> 
- <span data-ttu-id="1a268-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="1a268-132">P20Premium</span></span>

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

### <span data-ttu-id="1a268-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a268-133">-ResourceGroupName</span></span>
<span data-ttu-id="1a268-134">Especifica o grupo de recursos da coleção de trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1a268-134">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="1a268-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a268-135">-Confirm</span></span>
<span data-ttu-id="1a268-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a268-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a268-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a268-137">-WhatIf</span></span>
<span data-ttu-id="1a268-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a268-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a268-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a268-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a268-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a268-140">-DefaultProfile</span></span>
<span data-ttu-id="1a268-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a268-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a268-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a268-142">CommonParameters</span></span>
<span data-ttu-id="1a268-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a268-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a268-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a268-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a268-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a268-145">INPUTS</span></span>

## <span data-ttu-id="1a268-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a268-146">OUTPUTS</span></span>

### <span data-ttu-id="1a268-147">Microsoft. Azure. Commands. scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="1a268-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="1a268-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a268-148">NOTES</span></span>

## <span data-ttu-id="1a268-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a268-149">RELATED LINKS</span></span>

[<span data-ttu-id="1a268-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1a268-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1a268-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1a268-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1a268-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1a268-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1a268-153">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1a268-153">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1a268-154">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1a268-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


