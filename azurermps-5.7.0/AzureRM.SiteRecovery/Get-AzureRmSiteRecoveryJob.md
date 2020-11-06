---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431590"
---
# <span data-ttu-id="f65e0-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f65e0-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="f65e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f65e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f65e0-103">Obtém as informações de operação do cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="f65e0-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f65e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f65e0-104">SYNTAX</span></span>

### <span data-ttu-id="f65e0-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="f65e0-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f65e0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f65e0-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f65e0-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="f65e0-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f65e0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f65e0-108">DESCRIPTION</span></span>
<span data-ttu-id="f65e0-109">O cmdlet **Get-AzureRmSiteRecoveryJob** Obtém trabalhos do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f65e0-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="f65e0-110">Você pode usar esse cmdlet para exibir as informações de operação do cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="f65e0-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="f65e0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f65e0-111">EXAMPLES</span></span>

## <span data-ttu-id="f65e0-112">OS</span><span class="sxs-lookup"><span data-stu-id="f65e0-112">PARAMETERS</span></span>

### <span data-ttu-id="f65e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65e0-113">-DefaultProfile</span></span>
<span data-ttu-id="f65e0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f65e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f65e0-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f65e0-115">-EndTime</span></span>
<span data-ttu-id="f65e0-116">Especifica a hora de término dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="f65e0-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="f65e0-117">Esse cmdlet obtém todos os trabalhos que começarem antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="f65e0-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="f65e0-118">Para obter um objeto **DateTime** para esse parâmetro, use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="f65e0-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="f65e0-119">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f65e0-119">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="f65e0-120">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="f65e0-120">-Job</span></span>
<span data-ttu-id="f65e0-121">Especifica o trabalho de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="f65e0-121">Specifies the Site Recovery job.</span></span>

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

### <span data-ttu-id="f65e0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f65e0-122">-Name</span></span>
<span data-ttu-id="f65e0-123">Especifica um nome exclusivo que identifica o trabalho.</span><span class="sxs-lookup"><span data-stu-id="f65e0-123">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="f65e0-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f65e0-124">-StartTime</span></span>
<span data-ttu-id="f65e0-125">Especifica a hora de início dos trabalhos.</span><span class="sxs-lookup"><span data-stu-id="f65e0-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="f65e0-126">Esse cmdlet obtém todos os trabalhos que iniciaram após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="f65e0-126">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="f65e0-127">-Estado</span><span class="sxs-lookup"><span data-stu-id="f65e0-127">-State</span></span>
<span data-ttu-id="f65e0-128">Especifica o estado de entrada para um trabalho de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="f65e0-128">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="f65e0-129">Esse cmdlet obtém todos os trabalhos que correspondem ao estado especificado.</span><span class="sxs-lookup"><span data-stu-id="f65e0-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="f65e0-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f65e0-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f65e0-131">Não iniciado</span><span class="sxs-lookup"><span data-stu-id="f65e0-131">NotStarted</span></span>
- <span data-ttu-id="f65e0-132">InProgress</span><span class="sxs-lookup"><span data-stu-id="f65e0-132">InProgress</span></span>
- <span data-ttu-id="f65e0-133">Foi</span><span class="sxs-lookup"><span data-stu-id="f65e0-133">Succeeded</span></span>
- <span data-ttu-id="f65e0-134">Demais</span><span class="sxs-lookup"><span data-stu-id="f65e0-134">Other</span></span>
- <span data-ttu-id="f65e0-135">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="f65e0-135">Failed</span></span>
- <span data-ttu-id="f65e0-136">Cela</span><span class="sxs-lookup"><span data-stu-id="f65e0-136">Cancelled</span></span>
- <span data-ttu-id="f65e0-137">Interrompido</span><span class="sxs-lookup"><span data-stu-id="f65e0-137">Suspended</span></span>

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

### <span data-ttu-id="f65e0-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="f65e0-138">-TargetObjectId</span></span>
<span data-ttu-id="f65e0-139">Especifica a ID do objeto de destino do trabalho.</span><span class="sxs-lookup"><span data-stu-id="f65e0-139">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="f65e0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65e0-140">CommonParameters</span></span>
<span data-ttu-id="f65e0-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f65e0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65e0-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f65e0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65e0-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f65e0-143">INPUTS</span></span>

### <span data-ttu-id="f65e0-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="f65e0-144">ASRJob</span></span>
<span data-ttu-id="f65e0-145">O parâmetro ' Job ' aceita o valor do tipo ' ASRJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="f65e0-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="f65e0-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f65e0-146">OUTPUTS</span></span>

### <span data-ttu-id="f65e0-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="f65e0-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="f65e0-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f65e0-148">NOTES</span></span>

## <span data-ttu-id="f65e0-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f65e0-149">RELATED LINKS</span></span>

[<span data-ttu-id="f65e0-150">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f65e0-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="f65e0-151">Currículo-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f65e0-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="f65e0-152">Parar-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f65e0-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
