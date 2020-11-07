---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946076"
---
# <span data-ttu-id="e82a7-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e82a7-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="e82a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e82a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e82a7-103">Reinicia um trabalho de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="e82a7-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="e82a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e82a7-104">SYNTAX</span></span>

### <span data-ttu-id="e82a7-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="e82a7-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e82a7-106">ById</span><span class="sxs-lookup"><span data-stu-id="e82a7-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e82a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e82a7-107">DESCRIPTION</span></span>
<span data-ttu-id="e82a7-108">O cmdlet **Restart-AzureSiteRecoveryJob** reinicia um trabalho de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e82a7-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="e82a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e82a7-109">EXAMPLES</span></span>

### <span data-ttu-id="e82a7-110">Exemplo 1: reiniciar um trabalho</span><span class="sxs-lookup"><span data-stu-id="e82a7-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="e82a7-111">Esse comando reinicia o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="e82a7-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="e82a7-112">OS</span><span class="sxs-lookup"><span data-stu-id="e82a7-112">PARAMETERS</span></span>

### <span data-ttu-id="e82a7-113">-ID</span><span class="sxs-lookup"><span data-stu-id="e82a7-113">-Id</span></span>
<span data-ttu-id="e82a7-114">Especifica a ID do trabalho a ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e82a7-114">Specifies the ID of the job to restart.</span></span>

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

### <span data-ttu-id="e82a7-115">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="e82a7-115">-Job</span></span>
<span data-ttu-id="e82a7-116">Especifica o trabalho a ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e82a7-116">Specifies the job to restart.</span></span>

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

### <span data-ttu-id="e82a7-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e82a7-117">-Profile</span></span>
<span data-ttu-id="e82a7-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e82a7-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e82a7-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e82a7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e82a7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82a7-120">CommonParameters</span></span>
<span data-ttu-id="e82a7-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e82a7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82a7-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e82a7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82a7-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e82a7-123">INPUTS</span></span>

## <span data-ttu-id="e82a7-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e82a7-124">OUTPUTS</span></span>

## <span data-ttu-id="e82a7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e82a7-125">NOTES</span></span>

## <span data-ttu-id="e82a7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e82a7-126">RELATED LINKS</span></span>

[<span data-ttu-id="e82a7-127">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e82a7-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e82a7-128">Currículo-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e82a7-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e82a7-129">Parar-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e82a7-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


