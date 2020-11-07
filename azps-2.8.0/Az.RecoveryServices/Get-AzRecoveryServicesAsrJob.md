---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 85479392a34e81395d3f00e3ef3891772a2dcbec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773047"
---
# <span data-ttu-id="c8d40-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c8d40-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="c8d40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8d40-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d40-103">Obtém os detalhes do trabalho ASR especificado ou a lista de trabalhos ASR recentes no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c8d40-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="c8d40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8d40-104">SYNTAX</span></span>

### <span data-ttu-id="c8d40-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8d40-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8d40-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c8d40-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8d40-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="c8d40-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8d40-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8d40-108">DESCRIPTION</span></span>
<span data-ttu-id="c8d40-109">O cmdlet **Get-AzRecoveryServicesAsrJob** Obtém trabalhos do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c8d40-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="c8d40-110">Você pode usar esse cmdlet para exibir os trabalhos ASR no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c8d40-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="c8d40-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8d40-111">EXAMPLES</span></span>

### <span data-ttu-id="c8d40-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8d40-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="c8d40-113">Retorna todos os trabalhos em um objeto ASR específico (referenciar o objeto ASR, como um item replicado ou plano de recuperação por sua ID).</span><span class="sxs-lookup"><span data-stu-id="c8d40-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="c8d40-114">OS</span><span class="sxs-lookup"><span data-stu-id="c8d40-114">PARAMETERS</span></span>

### <span data-ttu-id="c8d40-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d40-115">-DefaultProfile</span></span>
<span data-ttu-id="c8d40-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d40-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c8d40-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c8d40-117">-EndTime</span></span>
<span data-ttu-id="c8d40-118">Especifica a hora de término dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="c8d40-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="c8d40-119">Esse cmdlet obtém todos os trabalhos que começarem antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="c8d40-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="c8d40-120">Para obter um objeto **DateTime** para esse parâmetro, use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="c8d40-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="c8d40-121">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c8d40-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d40-122">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="c8d40-122">-Job</span></span>
<span data-ttu-id="c8d40-123">Especifica o objeto de trabalho ASR para o qual obter detalhes atualizados.</span><span class="sxs-lookup"><span data-stu-id="c8d40-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d40-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8d40-124">-Name</span></span>
<span data-ttu-id="c8d40-125">Especifique o trabalho ASR por nome.</span><span class="sxs-lookup"><span data-stu-id="c8d40-125">Specify the ASR job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d40-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c8d40-126">-StartTime</span></span>
<span data-ttu-id="c8d40-127">Especifica a hora de início dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="c8d40-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="c8d40-128">Esse cmdlet obtém todos os trabalhos que iniciaram após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="c8d40-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d40-129">-Estado</span><span class="sxs-lookup"><span data-stu-id="c8d40-129">-State</span></span>
<span data-ttu-id="c8d40-130">Especifica o estado para um trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="c8d40-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="c8d40-131">Esse cmdlet obtém todos os trabalhos que correspondem ao estado especificado.</span><span class="sxs-lookup"><span data-stu-id="c8d40-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="c8d40-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c8d40-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8d40-133">Não iniciado</span><span class="sxs-lookup"><span data-stu-id="c8d40-133">NotStarted</span></span>
- <span data-ttu-id="c8d40-134">InProgress</span><span class="sxs-lookup"><span data-stu-id="c8d40-134">InProgress</span></span>
- <span data-ttu-id="c8d40-135">Foi</span><span class="sxs-lookup"><span data-stu-id="c8d40-135">Succeeded</span></span>
- <span data-ttu-id="c8d40-136">Demais</span><span class="sxs-lookup"><span data-stu-id="c8d40-136">Other</span></span>
- <span data-ttu-id="c8d40-137">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="c8d40-137">Failed</span></span>
- <span data-ttu-id="c8d40-138">Cela</span><span class="sxs-lookup"><span data-stu-id="c8d40-138">Cancelled</span></span>
- <span data-ttu-id="c8d40-139">Interrompido</span><span class="sxs-lookup"><span data-stu-id="c8d40-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d40-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="c8d40-140">-TargetObjectId</span></span>
<span data-ttu-id="c8d40-141">Especifica a ID do objeto.</span><span class="sxs-lookup"><span data-stu-id="c8d40-141">Specifies the ID of the object.</span></span> <span data-ttu-id="c8d40-142">Usado para pesquisar trabalhos no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c8d40-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d40-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d40-143">CommonParameters</span></span>
<span data-ttu-id="c8d40-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d40-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d40-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d40-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d40-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8d40-146">INPUTS</span></span>

### <span data-ttu-id="c8d40-147">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c8d40-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c8d40-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8d40-148">OUTPUTS</span></span>

### <span data-ttu-id="c8d40-149">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c8d40-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c8d40-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8d40-150">NOTES</span></span>

## <span data-ttu-id="c8d40-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8d40-151">RELATED LINKS</span></span>

[<span data-ttu-id="c8d40-152">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c8d40-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="c8d40-153">Currículo-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c8d40-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="c8d40-154">Parar-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c8d40-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
