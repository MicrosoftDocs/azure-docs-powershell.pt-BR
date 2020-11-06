---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: ac3f3c843f13fd500156cf148b5c80436e2e2649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433037"
---
# <span data-ttu-id="de5cc-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="de5cc-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="de5cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="de5cc-103">Retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="de5cc-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de5cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de5cc-104">SYNTAX</span></span>

### <span data-ttu-id="de5cc-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="de5cc-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de5cc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="de5cc-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de5cc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de5cc-107">DESCRIPTION</span></span>
<span data-ttu-id="de5cc-108">O cmdlet **resume-AzureRmRecoveryServicesAsrJob** retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="de5cc-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="de5cc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de5cc-109">EXAMPLES</span></span>

### <span data-ttu-id="de5cc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de5cc-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="de5cc-111">Retome o trabalho especificado se ele estiver em um estado de espera ou suspenso e retornar o objeto de trabalho ASR atualizado correspondente ao trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="de5cc-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="de5cc-112">OS</span><span class="sxs-lookup"><span data-stu-id="de5cc-112">PARAMETERS</span></span>

### <span data-ttu-id="de5cc-113">-Comentário</span><span class="sxs-lookup"><span data-stu-id="de5cc-113">-Comment</span></span>
<span data-ttu-id="de5cc-114">Comentários do log de trabalho.</span><span class="sxs-lookup"><span data-stu-id="de5cc-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de5cc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de5cc-115">-InputObject</span></span>
<span data-ttu-id="de5cc-116">O objeto de entrada para o cmdlet: o objeto de trabalho ASR correspondente ao trabalho a ser retomado.</span><span class="sxs-lookup"><span data-stu-id="de5cc-116">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de5cc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="de5cc-117">-Name</span></span>
<span data-ttu-id="de5cc-118">Especifique o trabalho ASR por nome.</span><span class="sxs-lookup"><span data-stu-id="de5cc-118">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="de5cc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de5cc-119">-Confirm</span></span>
<span data-ttu-id="de5cc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de5cc-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de5cc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5cc-121">-WhatIf</span></span>
<span data-ttu-id="de5cc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de5cc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de5cc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de5cc-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de5cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5cc-124">CommonParameters</span></span>
<span data-ttu-id="de5cc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de5cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5cc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5cc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5cc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de5cc-127">INPUTS</span></span>

### <span data-ttu-id="de5cc-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="de5cc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="de5cc-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de5cc-129">OUTPUTS</span></span>

### <span data-ttu-id="de5cc-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="de5cc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="de5cc-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de5cc-131">NOTES</span></span>

## <span data-ttu-id="de5cc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de5cc-132">RELATED LINKS</span></span>

[<span data-ttu-id="de5cc-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="de5cc-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="de5cc-134">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="de5cc-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="de5cc-135">Parar-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="de5cc-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
