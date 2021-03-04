---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 2609ed7483499445dbdd093d0059b76b7e781ef8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885524"
---
# <span data-ttu-id="fbfec-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="fbfec-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="fbfec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbfec-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfec-103">Reinicia um trabalho de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfec-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="fbfec-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fbfec-104">SYNTAX</span></span>

### <span data-ttu-id="fbfec-105">ByObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fbfec-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbfec-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fbfec-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbfec-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fbfec-107">DESCRIPTION</span></span>
<span data-ttu-id="fbfec-108">O cmdlet **Restart-AzRecoveryServicesAsrJob** reinicia um trabalho de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfec-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="fbfec-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbfec-109">EXAMPLES</span></span>

### <span data-ttu-id="fbfec-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fbfec-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="fbfec-111">Reinicia o trabalho ASR especificado e retorna o objeto de trabalho ASR atualizado do trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="fbfec-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="fbfec-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fbfec-112">PARAMETERS</span></span>

### <span data-ttu-id="fbfec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfec-113">-DefaultProfile</span></span>
<span data-ttu-id="fbfec-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fbfec-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbfec-115">-InputObject</span></span>
<span data-ttu-id="fbfec-116">O objeto de entrada para o cmdlet: o objeto de trabalho ASR correspondente ao trabalho ASR a ser reiniciado</span><span class="sxs-lookup"><span data-stu-id="fbfec-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="fbfec-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fbfec-117">-Name</span></span>
<span data-ttu-id="fbfec-118">Especifique o trabalho pelo nome.</span><span class="sxs-lookup"><span data-stu-id="fbfec-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="fbfec-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbfec-119">-Confirm</span></span>
<span data-ttu-id="fbfec-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbfec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbfec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbfec-121">-WhatIf</span></span>
<span data-ttu-id="fbfec-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fbfec-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbfec-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fbfec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbfec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfec-124">CommonParameters</span></span>
<span data-ttu-id="fbfec-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbfec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfec-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbfec-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfec-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbfec-127">INPUTS</span></span>

### <span data-ttu-id="fbfec-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="fbfec-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fbfec-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fbfec-129">OUTPUTS</span></span>

### <span data-ttu-id="fbfec-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="fbfec-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fbfec-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="fbfec-131">NOTES</span></span>

## <span data-ttu-id="fbfec-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbfec-132">RELATED LINKS</span></span>

[<span data-ttu-id="fbfec-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="fbfec-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="fbfec-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="fbfec-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="fbfec-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="fbfec-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
