---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440576"
---
# <span data-ttu-id="d43c6-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d43c6-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="d43c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d43c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d43c6-103">Obtém os detalhes do trabalho ASR especificado ou a lista de trabalhos ASR recentes no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d43c6-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d43c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d43c6-104">SYNTAX</span></span>

### <span data-ttu-id="d43c6-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="d43c6-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### <span data-ttu-id="d43c6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d43c6-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="d43c6-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="d43c6-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## <span data-ttu-id="d43c6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d43c6-108">DESCRIPTION</span></span>
<span data-ttu-id="d43c6-109">O cmdlet **Get-AzureRmRecoveryServicesAsrJob** Obtém trabalhos do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d43c6-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="d43c6-110">Você pode usar esse cmdlet para exibir os trabalhos ASR no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d43c6-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="d43c6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d43c6-111">EXAMPLES</span></span>

### <span data-ttu-id="d43c6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d43c6-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="d43c6-113">Retorna todos os trabalhos em um objeto ASR específico (referenciar o objeto ASR, como um item replicado ou plano de recuperação por sua ID).</span><span class="sxs-lookup"><span data-stu-id="d43c6-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="d43c6-114">OS</span><span class="sxs-lookup"><span data-stu-id="d43c6-114">PARAMETERS</span></span>

### <span data-ttu-id="d43c6-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d43c6-115">-EndTime</span></span>
<span data-ttu-id="d43c6-116">Especifica a hora de término dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="d43c6-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="d43c6-117">Esse cmdlet obtém todos os trabalhos que começarem antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d43c6-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="d43c6-118">Para obter um objeto **DateTime** para esse parâmetro, use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="d43c6-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="d43c6-119">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d43c6-119">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43c6-120">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="d43c6-120">-Job</span></span>
<span data-ttu-id="d43c6-121">Especifica o objeto de trabalho ASR para o qual obter detalhes atualizados.</span><span class="sxs-lookup"><span data-stu-id="d43c6-121">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d43c6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d43c6-122">-Name</span></span>
<span data-ttu-id="d43c6-123">Especifique o trabalho ASR por nome.</span><span class="sxs-lookup"><span data-stu-id="d43c6-123">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43c6-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d43c6-124">-StartTime</span></span>
<span data-ttu-id="d43c6-125">Especifica a hora de início dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="d43c6-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="d43c6-126">Esse cmdlet obtém todos os trabalhos que iniciaram após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="d43c6-126">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43c6-127">-Estado</span><span class="sxs-lookup"><span data-stu-id="d43c6-127">-State</span></span>
<span data-ttu-id="d43c6-128">Especifica o estado para um trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="d43c6-128">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="d43c6-129">Esse cmdlet obtém todos os trabalhos que correspondem ao estado especificado.</span><span class="sxs-lookup"><span data-stu-id="d43c6-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="d43c6-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d43c6-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d43c6-131">Não iniciado</span><span class="sxs-lookup"><span data-stu-id="d43c6-131">NotStarted</span></span>
- <span data-ttu-id="d43c6-132">InProgress</span><span class="sxs-lookup"><span data-stu-id="d43c6-132">InProgress</span></span>
- <span data-ttu-id="d43c6-133">Foi</span><span class="sxs-lookup"><span data-stu-id="d43c6-133">Succeeded</span></span>
- <span data-ttu-id="d43c6-134">Demais</span><span class="sxs-lookup"><span data-stu-id="d43c6-134">Other</span></span>
- <span data-ttu-id="d43c6-135">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="d43c6-135">Failed</span></span>
- <span data-ttu-id="d43c6-136">Cela</span><span class="sxs-lookup"><span data-stu-id="d43c6-136">Cancelled</span></span>
- <span data-ttu-id="d43c6-137">Interrompido</span><span class="sxs-lookup"><span data-stu-id="d43c6-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43c6-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="d43c6-138">-TargetObjectId</span></span>
<span data-ttu-id="d43c6-139">Especifica a ID do objeto.</span><span class="sxs-lookup"><span data-stu-id="d43c6-139">Specifies the ID of the object.</span></span> <span data-ttu-id="d43c6-140">Usado para pesquisar trabalhos no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="d43c6-140">Used to search for jobs on the specified object.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43c6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43c6-141">CommonParameters</span></span>
<span data-ttu-id="d43c6-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d43c6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43c6-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d43c6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43c6-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d43c6-144">INPUTS</span></span>

### <span data-ttu-id="d43c6-145">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d43c6-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d43c6-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d43c6-146">OUTPUTS</span></span>

### <span data-ttu-id="d43c6-147">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d43c6-147">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d43c6-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d43c6-148">NOTES</span></span>

## <span data-ttu-id="d43c6-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d43c6-149">RELATED LINKS</span></span>

[<span data-ttu-id="d43c6-150">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d43c6-150">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="d43c6-151">Currículo-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d43c6-151">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="d43c6-152">Parar-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d43c6-152">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
