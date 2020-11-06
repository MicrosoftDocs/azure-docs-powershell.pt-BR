---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e6c384f56e7af9bacad40dfbc1fbf87d26dd8320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429725"
---
# <span data-ttu-id="4918f-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4918f-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="4918f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4918f-102">SYNOPSIS</span></span>
<span data-ttu-id="4918f-103">Retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4918f-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4918f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4918f-104">SYNTAX</span></span>

### <span data-ttu-id="4918f-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="4918f-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4918f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4918f-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4918f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4918f-107">DESCRIPTION</span></span>
<span data-ttu-id="4918f-108">O cmdlet **resume-AzureRmRecoveryServicesAsrJob** retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4918f-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="4918f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4918f-109">EXAMPLES</span></span>

### <span data-ttu-id="4918f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4918f-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="4918f-111">Retome o trabalho especificado se ele estiver em um estado de espera ou suspenso e retornar o objeto de trabalho ASR atualizado correspondente ao trabalho ASR.</span><span class="sxs-lookup"><span data-stu-id="4918f-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="4918f-112">OS</span><span class="sxs-lookup"><span data-stu-id="4918f-112">PARAMETERS</span></span>

### <span data-ttu-id="4918f-113">-Comentário</span><span class="sxs-lookup"><span data-stu-id="4918f-113">-Comment</span></span>
<span data-ttu-id="4918f-114">Comentários do log de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4918f-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4918f-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4918f-115">-Confirm</span></span>
<span data-ttu-id="4918f-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4918f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4918f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4918f-117">-DefaultProfile</span></span>
<span data-ttu-id="4918f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4918f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="4918f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4918f-119">-InputObject</span></span>
<span data-ttu-id="4918f-120">O objeto de entrada para o cmdlet: o objeto de trabalho ASR correspondente ao trabalho a ser retomado.</span><span class="sxs-lookup"><span data-stu-id="4918f-120">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="4918f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4918f-121">-Name</span></span>
<span data-ttu-id="4918f-122">Especifique o trabalho ASR por nome.</span><span class="sxs-lookup"><span data-stu-id="4918f-122">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="4918f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4918f-123">-WhatIf</span></span>
<span data-ttu-id="4918f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4918f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4918f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4918f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4918f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4918f-126">CommonParameters</span></span>
<span data-ttu-id="4918f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4918f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4918f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4918f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4918f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4918f-129">INPUTS</span></span>

### <span data-ttu-id="4918f-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4918f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4918f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4918f-131">OUTPUTS</span></span>

### <span data-ttu-id="4918f-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4918f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4918f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4918f-133">NOTES</span></span>

## <span data-ttu-id="4918f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4918f-134">RELATED LINKS</span></span>

[<span data-ttu-id="4918f-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4918f-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="4918f-136">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4918f-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="4918f-137">Parar-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4918f-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
