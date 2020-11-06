---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609596"
---
# <span data-ttu-id="46e5b-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="46e5b-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="46e5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="46e5b-103">Reinicia um trabalho do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="46e5b-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46e5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46e5b-104">SYNTAX</span></span>

### <span data-ttu-id="46e5b-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="46e5b-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46e5b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="46e5b-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e5b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46e5b-107">DESCRIPTION</span></span>
<span data-ttu-id="46e5b-108">O cmdlet **Restart-AzureRmRecoveryServicesAsrJob** reinicia um trabalho de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="46e5b-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="46e5b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46e5b-109">EXAMPLES</span></span>

### <span data-ttu-id="46e5b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46e5b-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="46e5b-111">Reinicia o trabalho ASR especificado e retorna o objeto de trabalho ASR atualizado do trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="46e5b-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="46e5b-112">OS</span><span class="sxs-lookup"><span data-stu-id="46e5b-112">PARAMETERS</span></span>

### <span data-ttu-id="46e5b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46e5b-113">-InputObject</span></span>
<span data-ttu-id="46e5b-114">O objeto de entrada para o cmdlet: o objeto de trabalho ASR correspondente ao trabalho ASR a ser reiniciado</span><span class="sxs-lookup"><span data-stu-id="46e5b-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="46e5b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="46e5b-115">-Name</span></span>
<span data-ttu-id="46e5b-116">Especifique o trabalho por nome.</span><span class="sxs-lookup"><span data-stu-id="46e5b-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="46e5b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46e5b-117">-Confirm</span></span>
<span data-ttu-id="46e5b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46e5b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e5b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e5b-119">-WhatIf</span></span>
<span data-ttu-id="46e5b-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46e5b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46e5b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46e5b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e5b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e5b-122">CommonParameters</span></span>
<span data-ttu-id="46e5b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e5b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e5b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e5b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e5b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46e5b-125">INPUTS</span></span>

### <span data-ttu-id="46e5b-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="46e5b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="46e5b-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46e5b-127">OUTPUTS</span></span>

### <span data-ttu-id="46e5b-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="46e5b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="46e5b-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46e5b-129">NOTES</span></span>

## <span data-ttu-id="46e5b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46e5b-130">RELATED LINKS</span></span>

[<span data-ttu-id="46e5b-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="46e5b-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="46e5b-132">Currículo-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="46e5b-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="46e5b-133">Parar-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="46e5b-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
