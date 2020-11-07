---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946407"
---
# <span data-ttu-id="2f4e9-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="2f4e9-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="2f4e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f4e9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4e9-103">Interrompe um trabalho de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="2f4e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f4e9-104">SYNTAX</span></span>

### <span data-ttu-id="2f4e9-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f4e9-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2f4e9-106">ById</span><span class="sxs-lookup"><span data-stu-id="2f4e9-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2f4e9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f4e9-107">DESCRIPTION</span></span>
<span data-ttu-id="2f4e9-108">O cmdlet **Stop-AzureSiteRecoveryJob** interrompe um trabalho de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="2f4e9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f4e9-109">EXAMPLES</span></span>

### <span data-ttu-id="2f4e9-110">Exemplo 1: interromper todos os trabalhos</span><span class="sxs-lookup"><span data-stu-id="2f4e9-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="2f4e9-111">O primeiro comando obtém os trabalhos do Azure site Recovery para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryJob** e, em seguida, armazena os resultados na variável $Jobs.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="2f4e9-112">O segundo comando interrompe os trabalhos especificados por $Jobs.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="2f4e9-113">OS</span><span class="sxs-lookup"><span data-stu-id="2f4e9-113">PARAMETERS</span></span>

### <span data-ttu-id="2f4e9-114">-ID</span><span class="sxs-lookup"><span data-stu-id="2f4e9-114">-Id</span></span>
<span data-ttu-id="2f4e9-115">Especifica a ID do trabalho a ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="2f4e9-116">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="2f4e9-116">-Job</span></span>
<span data-ttu-id="2f4e9-117">Especifica o trabalho para parar.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-117">Specifies the job to stop.</span></span>

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

### <span data-ttu-id="2f4e9-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2f4e9-118">-Profile</span></span>
<span data-ttu-id="2f4e9-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f4e9-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f4e9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4e9-121">CommonParameters</span></span>
<span data-ttu-id="2f4e9-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4e9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4e9-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4e9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4e9-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f4e9-124">INPUTS</span></span>

## <span data-ttu-id="2f4e9-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f4e9-125">OUTPUTS</span></span>

## <span data-ttu-id="2f4e9-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f4e9-126">NOTES</span></span>

## <span data-ttu-id="2f4e9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f4e9-127">RELATED LINKS</span></span>

[<span data-ttu-id="2f4e9-128">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="2f4e9-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="2f4e9-129">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="2f4e9-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="2f4e9-130">Currículo-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="2f4e9-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


