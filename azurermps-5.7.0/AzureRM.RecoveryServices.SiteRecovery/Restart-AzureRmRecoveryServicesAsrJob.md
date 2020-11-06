---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 0ac09a527aff78648d3af14413baa33da137d59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429729"
---
# <span data-ttu-id="37d67-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="37d67-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="37d67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37d67-102">SYNOPSIS</span></span>
<span data-ttu-id="37d67-103">Reinicia um trabalho do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="37d67-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37d67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37d67-104">SYNTAX</span></span>

### <span data-ttu-id="37d67-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="37d67-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d67-106">ByName</span><span class="sxs-lookup"><span data-stu-id="37d67-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37d67-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37d67-107">DESCRIPTION</span></span>
<span data-ttu-id="37d67-108">O cmdlet **Restart-AzureRmRecoveryServicesAsrJob** reinicia um trabalho de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="37d67-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="37d67-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37d67-109">EXAMPLES</span></span>

### <span data-ttu-id="37d67-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37d67-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="37d67-111">Reinicia o trabalho ASR especificado e retorna o objeto de trabalho ASR atualizado do trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="37d67-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="37d67-112">OS</span><span class="sxs-lookup"><span data-stu-id="37d67-112">PARAMETERS</span></span>

### <span data-ttu-id="37d67-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="37d67-113">-Confirm</span></span>
<span data-ttu-id="37d67-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37d67-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37d67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d67-115">-DefaultProfile</span></span>
<span data-ttu-id="37d67-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37d67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="37d67-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37d67-117">-InputObject</span></span>
<span data-ttu-id="37d67-118">O objeto de entrada para o cmdlet: o objeto de trabalho ASR correspondente ao trabalho ASR a ser reiniciado</span><span class="sxs-lookup"><span data-stu-id="37d67-118">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="37d67-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="37d67-119">-Name</span></span>
<span data-ttu-id="37d67-120">Especifique o trabalho por nome.</span><span class="sxs-lookup"><span data-stu-id="37d67-120">Specify the job by name.</span></span>

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

### <span data-ttu-id="37d67-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d67-121">-WhatIf</span></span>
<span data-ttu-id="37d67-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37d67-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37d67-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37d67-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37d67-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d67-124">CommonParameters</span></span>
<span data-ttu-id="37d67-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d67-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d67-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37d67-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d67-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37d67-127">INPUTS</span></span>

### <span data-ttu-id="37d67-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="37d67-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="37d67-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37d67-129">OUTPUTS</span></span>

### <span data-ttu-id="37d67-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="37d67-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="37d67-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37d67-131">NOTES</span></span>

## <span data-ttu-id="37d67-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37d67-132">RELATED LINKS</span></span>

[<span data-ttu-id="37d67-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="37d67-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="37d67-134">Currículo-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="37d67-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="37d67-135">Parar-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="37d67-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
