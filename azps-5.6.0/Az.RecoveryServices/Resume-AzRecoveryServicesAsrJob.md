---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 5f76c9a1adabf69872b4d529df7e3289e4d6745b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891307"
---
# <span data-ttu-id="67acc-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="67acc-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="67acc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67acc-102">SYNOPSIS</span></span>
<span data-ttu-id="67acc-103">Retoma um trabalho suspenso de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="67acc-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="67acc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="67acc-104">SYNTAX</span></span>

### <span data-ttu-id="67acc-105">ByObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="67acc-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67acc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="67acc-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67acc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="67acc-107">DESCRIPTION</span></span>
<span data-ttu-id="67acc-108">O cmdlet **Resume-AzRecoveryServicesAsrJob** retoma um trabalho suspenso de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="67acc-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="67acc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67acc-109">EXAMPLES</span></span>

### <span data-ttu-id="67acc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67acc-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="67acc-111">Retome o trabalho especificado se ele estiver em um estado de espera ou suspenso e retorne o objeto de trabalho ASR atualizado correspondente ao trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="67acc-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="67acc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="67acc-112">PARAMETERS</span></span>

### <span data-ttu-id="67acc-113">-Comment</span><span class="sxs-lookup"><span data-stu-id="67acc-113">-Comment</span></span>
<span data-ttu-id="67acc-114">Comentários para o log de trabalho.</span><span class="sxs-lookup"><span data-stu-id="67acc-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="67acc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67acc-115">-DefaultProfile</span></span>
<span data-ttu-id="67acc-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67acc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="67acc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67acc-117">-InputObject</span></span>
<span data-ttu-id="67acc-118">O objeto de entrada para o cmdlet: o objeto Job ASR correspondente ao trabalho a ser retomado.</span><span class="sxs-lookup"><span data-stu-id="67acc-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="67acc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="67acc-119">-Name</span></span>
<span data-ttu-id="67acc-120">Especifique o trabalho ASR pelo nome.</span><span class="sxs-lookup"><span data-stu-id="67acc-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="67acc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67acc-121">-Confirm</span></span>
<span data-ttu-id="67acc-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67acc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67acc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67acc-123">-WhatIf</span></span>
<span data-ttu-id="67acc-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67acc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67acc-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67acc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67acc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67acc-126">CommonParameters</span></span>
<span data-ttu-id="67acc-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67acc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67acc-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67acc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67acc-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67acc-129">INPUTS</span></span>

### <span data-ttu-id="67acc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="67acc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="67acc-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="67acc-131">OUTPUTS</span></span>

### <span data-ttu-id="67acc-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="67acc-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="67acc-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="67acc-133">NOTES</span></span>

## <span data-ttu-id="67acc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67acc-134">RELATED LINKS</span></span>

[<span data-ttu-id="67acc-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="67acc-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="67acc-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="67acc-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="67acc-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="67acc-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
