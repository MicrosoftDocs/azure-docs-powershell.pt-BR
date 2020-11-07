---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941614"
---
# <span data-ttu-id="699cf-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="699cf-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="699cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="699cf-102">SYNOPSIS</span></span>
<span data-ttu-id="699cf-103">Interrompe um trabalho de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="699cf-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="699cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="699cf-104">SYNTAX</span></span>

### <span data-ttu-id="699cf-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="699cf-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="699cf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="699cf-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="699cf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="699cf-107">DESCRIPTION</span></span>
<span data-ttu-id="699cf-108">O cmdlet **Stop-AzRecoveryServicesAsrJob** interrompe o trabalho de recuperação de site do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="699cf-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="699cf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="699cf-109">EXAMPLES</span></span>

### <span data-ttu-id="699cf-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="699cf-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="699cf-111">Tenta interromper o trabalho especificado e retorna um objeto de trabalho ASR atualizado.</span><span class="sxs-lookup"><span data-stu-id="699cf-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="699cf-112">OS</span><span class="sxs-lookup"><span data-stu-id="699cf-112">PARAMETERS</span></span>

### <span data-ttu-id="699cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699cf-113">-DefaultProfile</span></span>
<span data-ttu-id="699cf-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="699cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699cf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="699cf-115">-InputObject</span></span>
<span data-ttu-id="699cf-116">Objeto de entrada: especifique o objeto de trabalho ASR correspondente ao trabalho ASR a ser interrompido</span><span class="sxs-lookup"><span data-stu-id="699cf-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="699cf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="699cf-117">-Name</span></span>
<span data-ttu-id="699cf-118">Especifique o trabalho ASR a ser interrompido pelo nome do trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="699cf-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="699cf-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="699cf-119">-Confirm</span></span>
<span data-ttu-id="699cf-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="699cf-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="699cf-121">-WhatIf</span></span>
<span data-ttu-id="699cf-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="699cf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="699cf-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="699cf-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699cf-124">CommonParameters</span></span>
<span data-ttu-id="699cf-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699cf-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="699cf-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699cf-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="699cf-127">INPUTS</span></span>

### <span data-ttu-id="699cf-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="699cf-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="699cf-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="699cf-129">OUTPUTS</span></span>

### <span data-ttu-id="699cf-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="699cf-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="699cf-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="699cf-131">NOTES</span></span>

## <span data-ttu-id="699cf-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="699cf-132">RELATED LINKS</span></span>

[<span data-ttu-id="699cf-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="699cf-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="699cf-134">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="699cf-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="699cf-135">Currículo-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="699cf-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
