---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c5efb6b9aa7d78ef5f8d50ef80c5155c7e731f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440039"
---
# <span data-ttu-id="60efa-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="60efa-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="60efa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60efa-102">SYNOPSIS</span></span>
<span data-ttu-id="60efa-103">Retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="60efa-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60efa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60efa-104">SYNTAX</span></span>

### <span data-ttu-id="60efa-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="60efa-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60efa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="60efa-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60efa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60efa-107">DESCRIPTION</span></span>
<span data-ttu-id="60efa-108">O cmdlet **resume-AzureRmRecoveryServicesAsrJob** retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="60efa-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="60efa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60efa-109">EXAMPLES</span></span>

### <span data-ttu-id="60efa-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60efa-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="60efa-111">Retome o trabalho especificado se ele estiver em um estado de espera ou suspenso e retornar o objeto de trabalho ASR atualizado correspondente ao trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="60efa-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="60efa-112">OS</span><span class="sxs-lookup"><span data-stu-id="60efa-112">PARAMETERS</span></span>

### <span data-ttu-id="60efa-113">-Comentário</span><span class="sxs-lookup"><span data-stu-id="60efa-113">-Comment</span></span>
<span data-ttu-id="60efa-114">Comentários do log de trabalho.</span><span class="sxs-lookup"><span data-stu-id="60efa-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="60efa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60efa-115">-DefaultProfile</span></span>
<span data-ttu-id="60efa-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60efa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60efa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60efa-117">-InputObject</span></span>
<span data-ttu-id="60efa-118">O objeto de entrada para o cmdlet: o objeto de trabalho ASR correspondente ao trabalho a ser retomado.</span><span class="sxs-lookup"><span data-stu-id="60efa-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="60efa-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="60efa-119">-Name</span></span>
<span data-ttu-id="60efa-120">Especifique o trabalho ASR por nome.</span><span class="sxs-lookup"><span data-stu-id="60efa-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="60efa-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60efa-121">-Confirm</span></span>
<span data-ttu-id="60efa-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60efa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60efa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60efa-123">-WhatIf</span></span>
<span data-ttu-id="60efa-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60efa-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60efa-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60efa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60efa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60efa-126">CommonParameters</span></span>
<span data-ttu-id="60efa-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60efa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60efa-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60efa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60efa-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60efa-129">INPUTS</span></span>

### <span data-ttu-id="60efa-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="60efa-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="60efa-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60efa-131">OUTPUTS</span></span>

### <span data-ttu-id="60efa-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="60efa-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="60efa-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60efa-133">NOTES</span></span>

## <span data-ttu-id="60efa-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60efa-134">RELATED LINKS</span></span>

[<span data-ttu-id="60efa-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="60efa-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="60efa-136">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="60efa-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="60efa-137">Parar-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="60efa-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
