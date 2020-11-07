---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946440"
---
# <span data-ttu-id="38b3e-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="38b3e-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="38b3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="38b3e-103">Retoma um trabalho suspenso de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="38b3e-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="38b3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38b3e-104">SYNTAX</span></span>

### <span data-ttu-id="38b3e-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="38b3e-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="38b3e-106">ById</span><span class="sxs-lookup"><span data-stu-id="38b3e-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="38b3e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38b3e-107">DESCRIPTION</span></span>
<span data-ttu-id="38b3e-108">O cmdlet **resume-AzureSiteRecoveryJob** retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="38b3e-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="38b3e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38b3e-109">EXAMPLES</span></span>

### <span data-ttu-id="38b3e-110">Exemplo 1: retomar todos os trabalhos</span><span class="sxs-lookup"><span data-stu-id="38b3e-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="38b3e-111">O primeiro comando obtém todos os trabalhos do Azure site Recovery para o cofre de recuperação do site atual usando o cmdlet **Get-AzureSiteRecoveryJob** e armazena os resultados na variável $Jobs.</span><span class="sxs-lookup"><span data-stu-id="38b3e-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="38b3e-112">O segundo comando retoma o trabalho especificado por $Jobs.</span><span class="sxs-lookup"><span data-stu-id="38b3e-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="38b3e-113">OS</span><span class="sxs-lookup"><span data-stu-id="38b3e-113">PARAMETERS</span></span>

### <span data-ttu-id="38b3e-114">-Comentários</span><span class="sxs-lookup"><span data-stu-id="38b3e-114">-Comments</span></span>
<span data-ttu-id="38b3e-115">Especifica os comentários para o log de trabalho.</span><span class="sxs-lookup"><span data-stu-id="38b3e-115">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b3e-116">-ID</span><span class="sxs-lookup"><span data-stu-id="38b3e-116">-Id</span></span>
<span data-ttu-id="38b3e-117">Especifica a ID de um trabalho a ser retomada.</span><span class="sxs-lookup"><span data-stu-id="38b3e-117">Specifies the ID of a job to resume.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b3e-118">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="38b3e-118">-Job</span></span>
<span data-ttu-id="38b3e-119">Especifica o trabalho a ser retomado.</span><span class="sxs-lookup"><span data-stu-id="38b3e-119">Specifies the job to resume.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38b3e-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="38b3e-120">-Profile</span></span>
<span data-ttu-id="38b3e-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="38b3e-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38b3e-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="38b3e-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b3e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b3e-123">CommonParameters</span></span>
<span data-ttu-id="38b3e-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b3e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b3e-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b3e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b3e-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38b3e-126">INPUTS</span></span>

## <span data-ttu-id="38b3e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38b3e-127">OUTPUTS</span></span>

## <span data-ttu-id="38b3e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38b3e-128">NOTES</span></span>

## <span data-ttu-id="38b3e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38b3e-129">RELATED LINKS</span></span>

[<span data-ttu-id="38b3e-130">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="38b3e-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="38b3e-131">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="38b3e-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="38b3e-132">Parar-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="38b3e-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


