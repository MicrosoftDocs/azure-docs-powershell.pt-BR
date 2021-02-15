---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114928"
---
# <span data-ttu-id="98d54-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="98d54-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="98d54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98d54-102">SYNOPSIS</span></span>
<span data-ttu-id="98d54-103">Reinicia um trabalho de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="98d54-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="98d54-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98d54-104">SYNTAX</span></span>

### <span data-ttu-id="98d54-105">ByObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="98d54-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98d54-106">ByName</span><span class="sxs-lookup"><span data-stu-id="98d54-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98d54-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="98d54-107">DESCRIPTION</span></span>
<span data-ttu-id="98d54-108">O cmdlet **Restart-AzRecoveryServicesAsr Job** reinicia um trabalho de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="98d54-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="98d54-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="98d54-109">EXAMPLES</span></span>

### <span data-ttu-id="98d54-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98d54-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="98d54-111">Reinicia o trabalho ASR especificado e retorna o objeto de trabalho ASR atualizado do trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="98d54-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="98d54-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98d54-112">PARAMETERS</span></span>

### <span data-ttu-id="98d54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d54-113">-DefaultProfile</span></span>
<span data-ttu-id="98d54-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98d54-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="98d54-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98d54-115">-InputObject</span></span>
<span data-ttu-id="98d54-116">O objeto de entrada para o cmdlet: o objeto de trabalho ASR correspondente ao trabalho ASR a ser reiniciado</span><span class="sxs-lookup"><span data-stu-id="98d54-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="98d54-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="98d54-117">-Name</span></span>
<span data-ttu-id="98d54-118">Especifique o trabalho por nome.</span><span class="sxs-lookup"><span data-stu-id="98d54-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="98d54-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="98d54-119">-Confirm</span></span>
<span data-ttu-id="98d54-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98d54-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98d54-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98d54-121">-WhatIf</span></span>
<span data-ttu-id="98d54-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="98d54-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98d54-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98d54-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98d54-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d54-124">CommonParameters</span></span>
<span data-ttu-id="98d54-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d54-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d54-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98d54-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d54-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="98d54-127">INPUTS</span></span>

### <span data-ttu-id="98d54-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="98d54-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="98d54-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="98d54-129">OUTPUTS</span></span>

### <span data-ttu-id="98d54-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="98d54-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="98d54-131">Notas</span><span class="sxs-lookup"><span data-stu-id="98d54-131">NOTES</span></span>

## <span data-ttu-id="98d54-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98d54-132">RELATED LINKS</span></span>

[<span data-ttu-id="98d54-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="98d54-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="98d54-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="98d54-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="98d54-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="98d54-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
