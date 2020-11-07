---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945658"
---
# <span data-ttu-id="18e52-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="18e52-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="18e52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18e52-102">SYNOPSIS</span></span>

<span data-ttu-id="18e52-103">Obtém a saída de um trabalho de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="18e52-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="18e52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18e52-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="18e52-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18e52-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="18e52-106">O cmdlet **Get-AzureAutomationJobOutput** Obtém a saída de um trabalho de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18e52-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="18e52-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18e52-107">EXAMPLES</span></span>

### <span data-ttu-id="18e52-108">Exemplo 1: obter a saída de um trabalho de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="18e52-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="18e52-109">Esse comando obtém toda a saída do trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="18e52-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="18e52-110">OS</span><span class="sxs-lookup"><span data-stu-id="18e52-110">PARAMETERS</span></span>

### <span data-ttu-id="18e52-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="18e52-111">-AutomationAccountName</span></span>
<span data-ttu-id="18e52-112">Especifica o nome de uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="18e52-112">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e52-113">-ID</span><span class="sxs-lookup"><span data-stu-id="18e52-113">-Id</span></span>
<span data-ttu-id="18e52-114">Especifica a ID de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="18e52-114">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e52-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="18e52-115">-Profile</span></span>
<span data-ttu-id="18e52-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="18e52-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="18e52-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="18e52-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="18e52-118">-StartTime</span><span class="sxs-lookup"><span data-stu-id="18e52-118">-StartTime</span></span>
<span data-ttu-id="18e52-119">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="18e52-119">Specifies a start time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e52-120">-Stream</span><span class="sxs-lookup"><span data-stu-id="18e52-120">-Stream</span></span>
<span data-ttu-id="18e52-121">Especifica o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="18e52-121">Specifies the type of output.</span></span>
<span data-ttu-id="18e52-122">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="18e52-122">Valid values are:</span></span> 

- <span data-ttu-id="18e52-123">Qualquer</span><span class="sxs-lookup"><span data-stu-id="18e52-123">Any</span></span>
- <span data-ttu-id="18e52-124">Depurá</span><span class="sxs-lookup"><span data-stu-id="18e52-124">Debug</span></span>
- <span data-ttu-id="18e52-125">Erros</span><span class="sxs-lookup"><span data-stu-id="18e52-125">Error</span></span>
- <span data-ttu-id="18e52-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="18e52-126">Output</span></span>
- <span data-ttu-id="18e52-127">Progresso</span><span class="sxs-lookup"><span data-stu-id="18e52-127">Progress</span></span>
- <span data-ttu-id="18e52-128">Detalha</span><span class="sxs-lookup"><span data-stu-id="18e52-128">Verbose</span></span>
- <span data-ttu-id="18e52-129">Avisa</span><span class="sxs-lookup"><span data-stu-id="18e52-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e52-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e52-130">CommonParameters</span></span>
<span data-ttu-id="18e52-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e52-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e52-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e52-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e52-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18e52-133">INPUTS</span></span>

## <span data-ttu-id="18e52-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18e52-134">OUTPUTS</span></span>

## <span data-ttu-id="18e52-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18e52-135">NOTES</span></span>

## <span data-ttu-id="18e52-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18e52-136">RELATED LINKS</span></span>

[<span data-ttu-id="18e52-137">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="18e52-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="18e52-138">Currículo-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="18e52-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="18e52-139">Parar-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="18e52-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="18e52-140">Suspender-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="18e52-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


