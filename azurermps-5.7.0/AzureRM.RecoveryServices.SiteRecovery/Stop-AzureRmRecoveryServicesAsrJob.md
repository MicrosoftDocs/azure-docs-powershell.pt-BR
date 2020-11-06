---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c573cd8162961660dac57be3d3f5fe18cd055a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426641"
---
# <span data-ttu-id="8b02f-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8b02f-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="8b02f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b02f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b02f-103">Interrompe um trabalho de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b02f-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b02f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b02f-104">SYNTAX</span></span>

### <span data-ttu-id="8b02f-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b02f-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b02f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8b02f-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b02f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b02f-107">DESCRIPTION</span></span>
<span data-ttu-id="8b02f-108">O cmdlet **Stop-AzureRmRecoveryServicesAsrJob** interrompe o trabalho de recuperação de site do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="8b02f-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="8b02f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b02f-109">EXAMPLES</span></span>

### <span data-ttu-id="8b02f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8b02f-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="8b02f-111">Tenta interromper o trabalho especificado e retorna um objeto de trabalho ASR atualizado.</span><span class="sxs-lookup"><span data-stu-id="8b02f-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="8b02f-112">OS</span><span class="sxs-lookup"><span data-stu-id="8b02f-112">PARAMETERS</span></span>

### <span data-ttu-id="8b02f-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b02f-113">-Confirm</span></span>
<span data-ttu-id="8b02f-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b02f-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b02f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b02f-115">-DefaultProfile</span></span>
<span data-ttu-id="8b02f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b02f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="8b02f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b02f-117">-InputObject</span></span>
<span data-ttu-id="8b02f-118">Objeto de entrada: especifique o objeto de trabalho ASR correspondente ao trabalho ASR a ser interrompido</span><span class="sxs-lookup"><span data-stu-id="8b02f-118">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="8b02f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b02f-119">-Name</span></span>
<span data-ttu-id="8b02f-120">Especifique o trabalho ASR a ser interrompido pelo nome do trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="8b02f-120">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="8b02f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b02f-121">-WhatIf</span></span>
<span data-ttu-id="8b02f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b02f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b02f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b02f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b02f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b02f-124">CommonParameters</span></span>
<span data-ttu-id="8b02f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b02f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b02f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b02f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b02f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b02f-127">INPUTS</span></span>

### <span data-ttu-id="8b02f-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8b02f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8b02f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b02f-129">OUTPUTS</span></span>

### <span data-ttu-id="8b02f-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8b02f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8b02f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b02f-131">NOTES</span></span>

## <span data-ttu-id="8b02f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b02f-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b02f-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8b02f-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8b02f-134">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8b02f-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8b02f-135">Currículo-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8b02f-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
