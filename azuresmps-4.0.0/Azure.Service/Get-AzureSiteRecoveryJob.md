---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a7c99e2ce307d700e43094ffa9be47e5449acc0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411646"
---
# <span data-ttu-id="e2471-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e2471-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="e2471-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2471-102">SYNOPSIS</span></span>
<span data-ttu-id="e2471-103">Obtém as informações de operação de um cofre de Recuperação de Site.</span><span class="sxs-lookup"><span data-stu-id="e2471-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="e2471-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2471-104">SYNTAX</span></span>

### <span data-ttu-id="e2471-105">ByParam (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e2471-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e2471-106">ById</span><span class="sxs-lookup"><span data-stu-id="e2471-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e2471-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="e2471-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2471-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2471-108">DESCRIPTION</span></span>
<span data-ttu-id="e2471-109">O **cmdlet Get-AzureSiteRecoveryJob** obtém trabalhos de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2471-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="e2471-110">Você pode usar esse cmdlet para exibir as informações de operação do cofre de Recuperação de Site atual.</span><span class="sxs-lookup"><span data-stu-id="e2471-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="e2471-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e2471-111">EXAMPLES</span></span>

### <span data-ttu-id="e2471-112">Exemplo 1: Obter um trabalho especificando uma ID</span><span class="sxs-lookup"><span data-stu-id="e2471-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="e2471-113">Esse comando obtém o trabalho de Recuperação de Site do Azure com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="e2471-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="e2471-114">Exemplo 2: Obtém um trabalho com base no tempo</span><span class="sxs-lookup"><span data-stu-id="e2471-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="e2471-115">Esse comando obtém trabalhos de Recuperação de Site que estão entre a hora de início e a hora de término especificadas.</span><span class="sxs-lookup"><span data-stu-id="e2471-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="e2471-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2471-116">PARAMETERS</span></span>

### <span data-ttu-id="e2471-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e2471-117">-EndTime</span></span>
<span data-ttu-id="e2471-118">Especifica a hora de término dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="e2471-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="e2471-119">Esse cmdlet obtém todos os trabalhos que começaram antes do horário especificado.</span><span class="sxs-lookup"><span data-stu-id="e2471-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="e2471-120">Para obter um **objeto DateTime,** use o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="e2471-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="e2471-121">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e2471-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="e2471-122">-ID</span><span class="sxs-lookup"><span data-stu-id="e2471-122">-Id</span></span>
<span data-ttu-id="e2471-123">Especifica a ID de um trabalho a ser feito.</span><span class="sxs-lookup"><span data-stu-id="e2471-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2471-124">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="e2471-124">-Job</span></span>
<span data-ttu-id="e2471-125">Especifica um trabalho a ser feito.</span><span class="sxs-lookup"><span data-stu-id="e2471-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="e2471-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e2471-126">-Profile</span></span>
<span data-ttu-id="e2471-127">Especifica o perfil do Azure a partir do qual este cmdlet é lido.</span><span class="sxs-lookup"><span data-stu-id="e2471-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2471-128">Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e2471-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2471-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e2471-129">-StartTime</span></span>
<span data-ttu-id="e2471-130">Especifica a hora de início dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="e2471-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="e2471-131">Esse cmdlet obtém todos os trabalhos que começaram após o tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="e2471-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="e2471-132">-Estado</span><span class="sxs-lookup"><span data-stu-id="e2471-132">-State</span></span>
<span data-ttu-id="e2471-133">Especifica o estado de entrada para um trabalho de Recuperação de Site.</span><span class="sxs-lookup"><span data-stu-id="e2471-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="e2471-134">Este cmdlet obtém todos os trabalhos que corresponderem ao estado especificado.</span><span class="sxs-lookup"><span data-stu-id="e2471-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="e2471-135">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e2471-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2471-136">Notstarted</span><span class="sxs-lookup"><span data-stu-id="e2471-136">NotStarted</span></span>
- <span data-ttu-id="e2471-137">Inprogress</span><span class="sxs-lookup"><span data-stu-id="e2471-137">InProgress</span></span>
- <span data-ttu-id="e2471-138">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="e2471-138">Succeeded</span></span>
- <span data-ttu-id="e2471-139">Outros</span><span class="sxs-lookup"><span data-stu-id="e2471-139">Other</span></span>
- <span data-ttu-id="e2471-140">Falhou</span><span class="sxs-lookup"><span data-stu-id="e2471-140">Failed</span></span>
- <span data-ttu-id="e2471-141">Cancelado</span><span class="sxs-lookup"><span data-stu-id="e2471-141">Cancelled</span></span>
- <span data-ttu-id="e2471-142">Suspenso</span><span class="sxs-lookup"><span data-stu-id="e2471-142">Suspended</span></span>

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

### <span data-ttu-id="e2471-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="e2471-143">-TargetObjectId</span></span>
<span data-ttu-id="e2471-144">Especifica a ID do objeto direcionado pelo trabalho.</span><span class="sxs-lookup"><span data-stu-id="e2471-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="e2471-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2471-145">CommonParameters</span></span>
<span data-ttu-id="e2471-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2471-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2471-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2471-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2471-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="e2471-148">INPUTS</span></span>

## <span data-ttu-id="e2471-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="e2471-149">OUTPUTS</span></span>

## <span data-ttu-id="e2471-150">Notas</span><span class="sxs-lookup"><span data-stu-id="e2471-150">NOTES</span></span>

## <span data-ttu-id="e2471-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2471-151">RELATED LINKS</span></span>



[<span data-ttu-id="e2471-152">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e2471-152">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e2471-153">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e2471-153">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e2471-154">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e2471-154">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


