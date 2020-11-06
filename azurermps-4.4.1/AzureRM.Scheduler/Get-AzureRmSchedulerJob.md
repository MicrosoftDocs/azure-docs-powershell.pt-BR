---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 3357eb154f21bc57de6ef60b243571e05bc0c22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609566"
---
# <span data-ttu-id="b0d3b-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="b0d3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d3b-103">Obtém trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="b0d3b-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0d3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0d3b-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d3b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d3b-106">O cmdlet **Get-AzureRmSchedulerJob** Obtém trabalhos do Agendador do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d3b-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="b0d3b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0d3b-107">EXAMPLES</span></span>

## <span data-ttu-id="b0d3b-108">OS</span><span class="sxs-lookup"><span data-stu-id="b0d3b-108">PARAMETERS</span></span>

### <span data-ttu-id="b0d3b-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b0d3b-109">-JobCollectionName</span></span>
<span data-ttu-id="b0d3b-110">Especifica o nome de uma coleção de trabalho que contém trabalhos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="b0d3b-110">Specifies the name of a job collection that contains jobs to get.</span></span>

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

### <span data-ttu-id="b0d3b-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="b0d3b-111">-JobName</span></span>
<span data-ttu-id="b0d3b-112">Especifica o nome de um trabalho a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="b0d3b-112">Specifies the name of a job to get.</span></span>

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

### <span data-ttu-id="b0d3b-113">-JobState</span><span class="sxs-lookup"><span data-stu-id="b0d3b-113">-JobState</span></span>
<span data-ttu-id="b0d3b-114">Especifica um estado de trabalho para obter tarefas.</span><span class="sxs-lookup"><span data-stu-id="b0d3b-114">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="b0d3b-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b0d3b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b0d3b-116">Possibilita</span><span class="sxs-lookup"><span data-stu-id="b0d3b-116">Enabled</span></span> 
- <span data-ttu-id="b0d3b-117">Ativo</span><span class="sxs-lookup"><span data-stu-id="b0d3b-117">Disabled</span></span> 
- <span data-ttu-id="b0d3b-118">Com defeito</span><span class="sxs-lookup"><span data-stu-id="b0d3b-118">Faulted</span></span> 
- <span data-ttu-id="b0d3b-119">Feito</span><span class="sxs-lookup"><span data-stu-id="b0d3b-119">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d3b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d3b-120">-ResourceGroupName</span></span>
<span data-ttu-id="b0d3b-121">Especifica o grupo de recursos dos trabalhos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="b0d3b-121">Specifies the resource group of the jobs to get.</span></span>

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

### <span data-ttu-id="b0d3b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d3b-122">-DefaultProfile</span></span>
<span data-ttu-id="b0d3b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d3b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0d3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d3b-124">CommonParameters</span></span>
<span data-ttu-id="b0d3b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d3b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d3b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d3b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0d3b-127">INPUTS</span></span>

## <span data-ttu-id="b0d3b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0d3b-128">OUTPUTS</span></span>

### <span data-ttu-id="b0d3b-129">Microsoft. Azure. Commands. scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b0d3b-129">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="b0d3b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0d3b-130">NOTES</span></span>

## <span data-ttu-id="b0d3b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0d3b-131">RELATED LINKS</span></span>

[<span data-ttu-id="b0d3b-132">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-132">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="b0d3b-133">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b0d3b-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b0d3b-134">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-134">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="b0d3b-135">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-135">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="b0d3b-136">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-136">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="b0d3b-137">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-137">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="b0d3b-138">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-138">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="b0d3b-139">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-139">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="b0d3b-140">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-140">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="b0d3b-141">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="b0d3b-141">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


