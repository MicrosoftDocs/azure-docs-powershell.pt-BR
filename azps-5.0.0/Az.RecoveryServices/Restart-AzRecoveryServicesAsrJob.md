---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118021"
---
# <span data-ttu-id="7dbfb-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7dbfb-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="7dbfb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7dbfb-102">SYNOPSIS</span></span>
<span data-ttu-id="7dbfb-103">Reinicia um trabalho do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7dbfb-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="7dbfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7dbfb-104">SYNTAX</span></span>

### <span data-ttu-id="7dbfb-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="7dbfb-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbfb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7dbfb-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7dbfb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7dbfb-107">DESCRIPTION</span></span>
<span data-ttu-id="7dbfb-108">O cmdlet **Restart-AzRecoveryServicesAsrJob** reinicia um trabalho de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="7dbfb-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="7dbfb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7dbfb-109">EXAMPLES</span></span>

### <span data-ttu-id="7dbfb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7dbfb-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="7dbfb-111">Reinicia o trabalho ASR especificado e retorna o objeto de trabalho ASR atualizado do trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="7dbfb-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="7dbfb-112">OS</span><span class="sxs-lookup"><span data-stu-id="7dbfb-112">PARAMETERS</span></span>

### <span data-ttu-id="7dbfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dbfb-113">-DefaultProfile</span></span>
<span data-ttu-id="7dbfb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7dbfb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7dbfb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dbfb-115">-InputObject</span></span>
<span data-ttu-id="7dbfb-116">O objeto de entrada para o cmdlet: o objeto de trabalho ASR correspondente ao trabalho ASR a ser reiniciado</span><span class="sxs-lookup"><span data-stu-id="7dbfb-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="7dbfb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7dbfb-117">-Name</span></span>
<span data-ttu-id="7dbfb-118">Especifique o trabalho por nome.</span><span class="sxs-lookup"><span data-stu-id="7dbfb-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="7dbfb-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7dbfb-119">-Confirm</span></span>
<span data-ttu-id="7dbfb-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dbfb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dbfb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dbfb-121">-WhatIf</span></span>
<span data-ttu-id="7dbfb-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7dbfb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7dbfb-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7dbfb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dbfb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dbfb-124">CommonParameters</span></span>
<span data-ttu-id="7dbfb-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dbfb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dbfb-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dbfb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dbfb-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7dbfb-127">INPUTS</span></span>

### <span data-ttu-id="7dbfb-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7dbfb-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7dbfb-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7dbfb-129">OUTPUTS</span></span>

### <span data-ttu-id="7dbfb-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7dbfb-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7dbfb-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7dbfb-131">NOTES</span></span>

## <span data-ttu-id="7dbfb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dbfb-132">RELATED LINKS</span></span>

[<span data-ttu-id="7dbfb-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7dbfb-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="7dbfb-134">Currículo-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7dbfb-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="7dbfb-135">Parar-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7dbfb-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
