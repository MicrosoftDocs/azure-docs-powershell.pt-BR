---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945595"
---
# <span data-ttu-id="bcfe9-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="bcfe9-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="bcfe9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcfe9-102">SYNOPSIS</span></span>
<span data-ttu-id="bcfe9-103">Obtém as informações de operação para um cofre de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="bcfe9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcfe9-104">SYNTAX</span></span>

### <span data-ttu-id="bcfe9-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="bcfe9-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bcfe9-106">ById</span><span class="sxs-lookup"><span data-stu-id="bcfe9-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bcfe9-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="bcfe9-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bcfe9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcfe9-108">DESCRIPTION</span></span>
<span data-ttu-id="bcfe9-109">O cmdlet **Get-AzureSiteRecoveryJob** Obtém trabalhos do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="bcfe9-110">Você pode usar esse cmdlet para exibir as informações de operação do cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="bcfe9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcfe9-111">EXAMPLES</span></span>

### <span data-ttu-id="bcfe9-112">Exemplo 1: obter um trabalho especificando uma ID</span><span class="sxs-lookup"><span data-stu-id="bcfe9-112">Example 1: Get a job by specifying an ID</span></span>
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

<span data-ttu-id="bcfe9-113">Este comando obtém o trabalho de recuperação do site do Azure com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="bcfe9-114">Exemplo 2: Obtém um trabalho com base no tempo</span><span class="sxs-lookup"><span data-stu-id="bcfe9-114">Example 2: Gets a job based on time</span></span>
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

<span data-ttu-id="bcfe9-115">Esse comando obtém trabalhos de recuperação de site que estão entre a hora de início e a hora de término especificadas.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="bcfe9-116">OS</span><span class="sxs-lookup"><span data-stu-id="bcfe9-116">PARAMETERS</span></span>

### <span data-ttu-id="bcfe9-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="bcfe9-117">-EndTime</span></span>
<span data-ttu-id="bcfe9-118">Especifica a hora de término dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="bcfe9-119">Esse cmdlet obtém todos os trabalhos que começarem antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="bcfe9-120">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="bcfe9-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="bcfe9-121">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="bcfe9-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="bcfe9-122">-ID</span><span class="sxs-lookup"><span data-stu-id="bcfe9-122">-Id</span></span>
<span data-ttu-id="bcfe9-123">Especifica a ID de um trabalho a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-123">Specifies the ID of a job to get.</span></span>

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

### <span data-ttu-id="bcfe9-124">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="bcfe9-124">-Job</span></span>
<span data-ttu-id="bcfe9-125">Especifica um trabalho a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="bcfe9-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bcfe9-126">-Profile</span></span>
<span data-ttu-id="bcfe9-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bcfe9-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bcfe9-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bcfe9-129">-StartTime</span></span>
<span data-ttu-id="bcfe9-130">Especifica a hora de início dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="bcfe9-131">Esse cmdlet obtém todos os trabalhos que iniciaram após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="bcfe9-132">-Estado</span><span class="sxs-lookup"><span data-stu-id="bcfe9-132">-State</span></span>
<span data-ttu-id="bcfe9-133">Especifica o estado de entrada para um trabalho de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="bcfe9-134">Esse cmdlet obtém todos os trabalhos que correspondem ao estado especificado.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="bcfe9-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bcfe9-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bcfe9-136">Não iniciado</span><span class="sxs-lookup"><span data-stu-id="bcfe9-136">NotStarted</span></span>
- <span data-ttu-id="bcfe9-137">InProgress</span><span class="sxs-lookup"><span data-stu-id="bcfe9-137">InProgress</span></span>
- <span data-ttu-id="bcfe9-138">Foi</span><span class="sxs-lookup"><span data-stu-id="bcfe9-138">Succeeded</span></span>
- <span data-ttu-id="bcfe9-139">Demais</span><span class="sxs-lookup"><span data-stu-id="bcfe9-139">Other</span></span>
- <span data-ttu-id="bcfe9-140">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="bcfe9-140">Failed</span></span>
- <span data-ttu-id="bcfe9-141">Cela</span><span class="sxs-lookup"><span data-stu-id="bcfe9-141">Cancelled</span></span>
- <span data-ttu-id="bcfe9-142">Interrompido</span><span class="sxs-lookup"><span data-stu-id="bcfe9-142">Suspended</span></span>

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

### <span data-ttu-id="bcfe9-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="bcfe9-143">-TargetObjectId</span></span>
<span data-ttu-id="bcfe9-144">Especifica a ID do objeto de destino do trabalho.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="bcfe9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcfe9-145">CommonParameters</span></span>
<span data-ttu-id="bcfe9-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcfe9-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcfe9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcfe9-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcfe9-148">INPUTS</span></span>

## <span data-ttu-id="bcfe9-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcfe9-149">OUTPUTS</span></span>

## <span data-ttu-id="bcfe9-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcfe9-150">NOTES</span></span>

## <span data-ttu-id="bcfe9-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcfe9-151">RELATED LINKS</span></span>

[<span data-ttu-id="bcfe9-152">Cmdlets de serviços de recuperação do site do Azure</span><span class="sxs-lookup"><span data-stu-id="bcfe9-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="bcfe9-153">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="bcfe9-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="bcfe9-154">Currículo-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="bcfe9-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="bcfe9-155">Parar-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="bcfe9-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


