---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945462"
---
# <span data-ttu-id="4ddd7-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4ddd7-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="4ddd7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ddd7-102">SYNOPSIS</span></span>

<span data-ttu-id="4ddd7-103">Retoma um trabalho de automação suspenso.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="4ddd7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ddd7-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ddd7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ddd7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4ddd7-106">O cmdlet **resume-AzureAutomationJob** retoma um trabalho suspenso do Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="4ddd7-107">Use o parâmetro *ID* para especificar o trabalho suspenso.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="4ddd7-108">Para suspender um trabalho, use o cmdlet Suspend-AzureAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="4ddd7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ddd7-109">EXAMPLES</span></span>

### <span data-ttu-id="4ddd7-110">Exemplo 1: retomar um trabalho suspenso</span><span class="sxs-lookup"><span data-stu-id="4ddd7-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="4ddd7-111">Esse comando retoma o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="4ddd7-112">OS</span><span class="sxs-lookup"><span data-stu-id="4ddd7-112">PARAMETERS</span></span>

### <span data-ttu-id="4ddd7-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4ddd7-113">-AutomationAccountName</span></span>
<span data-ttu-id="4ddd7-114">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="4ddd7-115">-ID</span><span class="sxs-lookup"><span data-stu-id="4ddd7-115">-Id</span></span>
<span data-ttu-id="4ddd7-116">Especifica a ID de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="4ddd7-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4ddd7-117">-Profile</span></span>
<span data-ttu-id="4ddd7-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4ddd7-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4ddd7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ddd7-120">CommonParameters</span></span>
<span data-ttu-id="4ddd7-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ddd7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ddd7-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ddd7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ddd7-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ddd7-123">INPUTS</span></span>

## <span data-ttu-id="4ddd7-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ddd7-124">OUTPUTS</span></span>

## <span data-ttu-id="4ddd7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ddd7-125">NOTES</span></span>

## <span data-ttu-id="4ddd7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ddd7-126">RELATED LINKS</span></span>

[<span data-ttu-id="4ddd7-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4ddd7-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="4ddd7-128">Parar-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4ddd7-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="4ddd7-129">Suspender-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4ddd7-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


