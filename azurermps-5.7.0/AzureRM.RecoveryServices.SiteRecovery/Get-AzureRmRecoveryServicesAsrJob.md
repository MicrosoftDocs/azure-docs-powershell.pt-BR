---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 233a6a7c7fd7b2bfe96ed9cc0df6a88bdb9d8747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427470"
---
# <span data-ttu-id="8f366-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8f366-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="8f366-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f366-102">SYNOPSIS</span></span>
<span data-ttu-id="8f366-103">Obtém os detalhes do trabalho ASR especificado ou a lista de trabalhos ASR recentes no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8f366-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f366-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f366-104">SYNTAX</span></span>

### <span data-ttu-id="8f366-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="8f366-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f366-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8f366-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f366-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="8f366-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f366-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f366-108">DESCRIPTION</span></span>
<span data-ttu-id="8f366-109">O cmdlet **Get-AzureRmRecoveryServicesAsrJob** Obtém trabalhos do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8f366-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="8f366-110">Você pode usar esse cmdlet para exibir os trabalhos ASR no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8f366-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="8f366-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f366-111">EXAMPLES</span></span>

### <span data-ttu-id="8f366-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f366-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="8f366-113">Retorna todos os trabalhos em um objeto ASR específico (referenciar o objeto ASR, como um item replicado ou plano de recuperação por sua ID).</span><span class="sxs-lookup"><span data-stu-id="8f366-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="8f366-114">OS</span><span class="sxs-lookup"><span data-stu-id="8f366-114">PARAMETERS</span></span>

### <span data-ttu-id="8f366-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f366-115">-DefaultProfile</span></span>
<span data-ttu-id="8f366-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f366-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="8f366-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8f366-117">-EndTime</span></span>
<span data-ttu-id="8f366-118">Especifica a hora de término dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8f366-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="8f366-119">Esse cmdlet obtém todos os trabalhos que começarem antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="8f366-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="8f366-120">Para obter um objeto **DateTime** para esse parâmetro, use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="8f366-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="8f366-121">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8f366-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="8f366-122">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="8f366-122">-Job</span></span>
<span data-ttu-id="8f366-123">Especifica o objeto de trabalho ASR para o qual obter detalhes atualizados.</span><span class="sxs-lookup"><span data-stu-id="8f366-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="8f366-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f366-124">-Name</span></span>
<span data-ttu-id="8f366-125">Especifique o trabalho ASR por nome.</span><span class="sxs-lookup"><span data-stu-id="8f366-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="8f366-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8f366-126">-StartTime</span></span>
<span data-ttu-id="8f366-127">Especifica a hora de início dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8f366-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="8f366-128">Esse cmdlet obtém todos os trabalhos que iniciaram após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="8f366-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="8f366-129">-Estado</span><span class="sxs-lookup"><span data-stu-id="8f366-129">-State</span></span>
<span data-ttu-id="8f366-130">Especifica o estado para um trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="8f366-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="8f366-131">Esse cmdlet obtém todos os trabalhos que correspondem ao estado especificado.</span><span class="sxs-lookup"><span data-stu-id="8f366-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="8f366-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8f366-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f366-133">Não iniciado</span><span class="sxs-lookup"><span data-stu-id="8f366-133">NotStarted</span></span>
- <span data-ttu-id="8f366-134">InProgress</span><span class="sxs-lookup"><span data-stu-id="8f366-134">InProgress</span></span>
- <span data-ttu-id="8f366-135">Foi</span><span class="sxs-lookup"><span data-stu-id="8f366-135">Succeeded</span></span>
- <span data-ttu-id="8f366-136">Demais</span><span class="sxs-lookup"><span data-stu-id="8f366-136">Other</span></span>
- <span data-ttu-id="8f366-137">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="8f366-137">Failed</span></span>
- <span data-ttu-id="8f366-138">Cela</span><span class="sxs-lookup"><span data-stu-id="8f366-138">Cancelled</span></span>
- <span data-ttu-id="8f366-139">Interrompido</span><span class="sxs-lookup"><span data-stu-id="8f366-139">Suspended</span></span>

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

### <span data-ttu-id="8f366-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="8f366-140">-TargetObjectId</span></span>
<span data-ttu-id="8f366-141">Especifica a ID do objeto.</span><span class="sxs-lookup"><span data-stu-id="8f366-141">Specifies the ID of the object.</span></span> <span data-ttu-id="8f366-142">Usado para pesquisar trabalhos no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f366-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="8f366-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f366-143">CommonParameters</span></span>
<span data-ttu-id="8f366-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f366-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f366-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f366-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f366-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f366-146">INPUTS</span></span>

### <span data-ttu-id="8f366-147">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8f366-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8f366-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f366-148">OUTPUTS</span></span>

### <span data-ttu-id="8f366-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8f366-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8f366-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f366-150">NOTES</span></span>

## <span data-ttu-id="8f366-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f366-151">RELATED LINKS</span></span>

[<span data-ttu-id="8f366-152">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8f366-152">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8f366-153">Currículo-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8f366-153">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8f366-154">Parar-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8f366-154">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
