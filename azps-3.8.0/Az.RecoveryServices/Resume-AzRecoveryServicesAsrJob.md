---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943534"
---
# <span data-ttu-id="117c8-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="117c8-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="117c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="117c8-102">SYNOPSIS</span></span>
<span data-ttu-id="117c8-103">Retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="117c8-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="117c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="117c8-104">SYNTAX</span></span>

### <span data-ttu-id="117c8-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="117c8-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="117c8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="117c8-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="117c8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="117c8-107">DESCRIPTION</span></span>
<span data-ttu-id="117c8-108">O cmdlet **resume-AzRecoveryServicesAsrJob** retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="117c8-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="117c8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="117c8-109">EXAMPLES</span></span>

### <span data-ttu-id="117c8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="117c8-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="117c8-111">Retome o trabalho especificado se ele estiver em um estado de espera ou suspenso e retornar o objeto de trabalho ASR atualizado correspondente ao trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="117c8-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="117c8-112">OS</span><span class="sxs-lookup"><span data-stu-id="117c8-112">PARAMETERS</span></span>

### <span data-ttu-id="117c8-113">-Comentário</span><span class="sxs-lookup"><span data-stu-id="117c8-113">-Comment</span></span>
<span data-ttu-id="117c8-114">Comentários do log de trabalho.</span><span class="sxs-lookup"><span data-stu-id="117c8-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117c8-115">-DefaultProfile</span></span>
<span data-ttu-id="117c8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="117c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="117c8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="117c8-117">-InputObject</span></span>
<span data-ttu-id="117c8-118">O objeto de entrada para o cmdlet: o objeto de trabalho ASR correspondente ao trabalho a ser retomado.</span><span class="sxs-lookup"><span data-stu-id="117c8-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="117c8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="117c8-119">-Name</span></span>
<span data-ttu-id="117c8-120">Especifique o trabalho ASR por nome.</span><span class="sxs-lookup"><span data-stu-id="117c8-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="117c8-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="117c8-121">-Confirm</span></span>
<span data-ttu-id="117c8-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="117c8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="117c8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="117c8-123">-WhatIf</span></span>
<span data-ttu-id="117c8-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="117c8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="117c8-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="117c8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="117c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117c8-126">CommonParameters</span></span>
<span data-ttu-id="117c8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="117c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117c8-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="117c8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117c8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="117c8-129">INPUTS</span></span>

### <span data-ttu-id="117c8-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="117c8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="117c8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="117c8-131">OUTPUTS</span></span>

### <span data-ttu-id="117c8-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="117c8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="117c8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="117c8-133">NOTES</span></span>

## <span data-ttu-id="117c8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="117c8-134">RELATED LINKS</span></span>

[<span data-ttu-id="117c8-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="117c8-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="117c8-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="117c8-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="117c8-137">Parar-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="117c8-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
