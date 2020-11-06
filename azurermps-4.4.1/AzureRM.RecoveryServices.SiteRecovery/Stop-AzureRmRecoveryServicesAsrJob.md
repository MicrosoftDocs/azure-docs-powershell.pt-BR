---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609592"
---
# <span data-ttu-id="31b00-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="31b00-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="31b00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31b00-102">SYNOPSIS</span></span>
<span data-ttu-id="31b00-103">Interrompe um trabalho de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="31b00-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31b00-104">SYNTAX</span></span>

### <span data-ttu-id="31b00-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="31b00-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b00-106">ByName</span><span class="sxs-lookup"><span data-stu-id="31b00-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b00-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31b00-107">DESCRIPTION</span></span>
<span data-ttu-id="31b00-108">O cmdlet **Stop-AzureRmRecoveryServicesAsrJob** interrompe o trabalho de recuperação de site do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="31b00-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="31b00-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31b00-109">EXAMPLES</span></span>

### <span data-ttu-id="31b00-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="31b00-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="31b00-111">Tenta interromper o trabalho especificado e retorna um objeto de trabalho ASR atualizado.</span><span class="sxs-lookup"><span data-stu-id="31b00-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="31b00-112">OS</span><span class="sxs-lookup"><span data-stu-id="31b00-112">PARAMETERS</span></span>

### <span data-ttu-id="31b00-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31b00-113">-InputObject</span></span>
<span data-ttu-id="31b00-114">Objeto de entrada: especifique o objeto de trabalho ASR correspondente ao trabalho ASR a ser interrompido</span><span class="sxs-lookup"><span data-stu-id="31b00-114">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="31b00-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="31b00-115">-Name</span></span>
<span data-ttu-id="31b00-116">Especifique o trabalho ASR a ser interrompido pelo nome do trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="31b00-116">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="31b00-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="31b00-117">-Confirm</span></span>
<span data-ttu-id="31b00-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31b00-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b00-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b00-119">-WhatIf</span></span>
<span data-ttu-id="31b00-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31b00-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31b00-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31b00-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b00-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b00-122">CommonParameters</span></span>
<span data-ttu-id="31b00-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b00-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b00-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b00-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b00-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31b00-125">INPUTS</span></span>

### <span data-ttu-id="31b00-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="31b00-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="31b00-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31b00-127">OUTPUTS</span></span>

### <span data-ttu-id="31b00-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="31b00-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="31b00-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31b00-129">NOTES</span></span>

## <span data-ttu-id="31b00-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31b00-130">RELATED LINKS</span></span>

[<span data-ttu-id="31b00-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="31b00-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="31b00-132">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="31b00-132">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="31b00-133">Currículo-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="31b00-133">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
