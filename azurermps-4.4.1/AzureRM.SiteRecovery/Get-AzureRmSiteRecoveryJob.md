---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602401"
---
# <span data-ttu-id="a7d79-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a7d79-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="a7d79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7d79-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d79-103">Obtém as informações de operação do cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="a7d79-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7d79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7d79-104">SYNTAX</span></span>

### <span data-ttu-id="a7d79-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7d79-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d79-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a7d79-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d79-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="a7d79-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d79-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7d79-108">DESCRIPTION</span></span>
<span data-ttu-id="a7d79-109">O cmdlet **Get-AzureRmSiteRecoveryJob** Obtém trabalhos do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a7d79-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="a7d79-110">Você pode usar esse cmdlet para exibir as informações de operação do cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="a7d79-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="a7d79-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7d79-111">EXAMPLES</span></span>

## <span data-ttu-id="a7d79-112">OS</span><span class="sxs-lookup"><span data-stu-id="a7d79-112">PARAMETERS</span></span>

### <span data-ttu-id="a7d79-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a7d79-113">-EndTime</span></span>
<span data-ttu-id="a7d79-114">Especifica a hora de término dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="a7d79-114">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="a7d79-115">Esse cmdlet obtém todos os trabalhos que começarem antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="a7d79-115">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="a7d79-116">Para obter um objeto **DateTime** para esse parâmetro, use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="a7d79-116">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="a7d79-117">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a7d79-117">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="a7d79-118">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="a7d79-118">-Job</span></span>
<span data-ttu-id="a7d79-119">Especifica o trabalho de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="a7d79-119">Specifies the Site Recovery job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d79-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7d79-120">-Name</span></span>
<span data-ttu-id="a7d79-121">Especifica um nome exclusivo que identifica o trabalho.</span><span class="sxs-lookup"><span data-stu-id="a7d79-121">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="a7d79-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a7d79-122">-StartTime</span></span>
<span data-ttu-id="a7d79-123">Especifica a hora de início dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="a7d79-123">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="a7d79-124">Esse cmdlet obtém todos os trabalhos que iniciaram após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="a7d79-124">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="a7d79-125">-Estado</span><span class="sxs-lookup"><span data-stu-id="a7d79-125">-State</span></span>
<span data-ttu-id="a7d79-126">Especifica o estado de entrada para um trabalho de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="a7d79-126">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="a7d79-127">Esse cmdlet obtém todos os trabalhos que correspondem ao estado especificado.</span><span class="sxs-lookup"><span data-stu-id="a7d79-127">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="a7d79-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a7d79-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7d79-129">Não iniciado</span><span class="sxs-lookup"><span data-stu-id="a7d79-129">NotStarted</span></span>
- <span data-ttu-id="a7d79-130">InProgress</span><span class="sxs-lookup"><span data-stu-id="a7d79-130">InProgress</span></span>
- <span data-ttu-id="a7d79-131">Foi</span><span class="sxs-lookup"><span data-stu-id="a7d79-131">Succeeded</span></span>
- <span data-ttu-id="a7d79-132">Demais</span><span class="sxs-lookup"><span data-stu-id="a7d79-132">Other</span></span>
- <span data-ttu-id="a7d79-133">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="a7d79-133">Failed</span></span>
- <span data-ttu-id="a7d79-134">Cela</span><span class="sxs-lookup"><span data-stu-id="a7d79-134">Cancelled</span></span>
- <span data-ttu-id="a7d79-135">Interrompido</span><span class="sxs-lookup"><span data-stu-id="a7d79-135">Suspended</span></span>

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

### <span data-ttu-id="a7d79-136">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="a7d79-136">-TargetObjectId</span></span>
<span data-ttu-id="a7d79-137">Especifica a ID do objeto de destino do trabalho.</span><span class="sxs-lookup"><span data-stu-id="a7d79-137">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="a7d79-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d79-138">-DefaultProfile</span></span>
<span data-ttu-id="a7d79-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d79-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7d79-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d79-140">CommonParameters</span></span>
<span data-ttu-id="a7d79-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d79-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d79-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d79-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d79-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7d79-143">INPUTS</span></span>

### <span data-ttu-id="a7d79-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="a7d79-144">ASRJob</span></span>
<span data-ttu-id="a7d79-145">O parâmetro ' Job ' aceita o valor do tipo ' ASRJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a7d79-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="a7d79-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7d79-146">OUTPUTS</span></span>

### <span data-ttu-id="a7d79-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="a7d79-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="a7d79-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7d79-148">NOTES</span></span>

## <span data-ttu-id="a7d79-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7d79-149">RELATED LINKS</span></span>

[<span data-ttu-id="a7d79-150">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a7d79-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="a7d79-151">Currículo-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a7d79-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="a7d79-152">Parar-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a7d79-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
