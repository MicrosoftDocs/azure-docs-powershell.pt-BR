---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CE04DEE6-28AE-43A3-A8DE-98AC0A57E575
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1c2d9a3aa53cb8efd2924f24aa80db2c7fd07fea
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945759"
---
# <span data-ttu-id="465b2-101">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="465b2-101">Suspend-AzureAutomationJob</span></span>

## <span data-ttu-id="465b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="465b2-102">SYNOPSIS</span></span>

<span data-ttu-id="465b2-103">Suspende um trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="465b2-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="465b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="465b2-104">SYNTAX</span></span>

```
Suspend-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="465b2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="465b2-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="465b2-106">O cmdlet **Suspend-AzureAutomationJob** suspende um trabalho de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="465b2-106">The **Suspend-AzureAutomationJob** cmdlet suspends a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="465b2-107">Especifique um trabalho de automação em execução.</span><span class="sxs-lookup"><span data-stu-id="465b2-107">Specify a running Automation job.</span></span>

<span data-ttu-id="465b2-108">Para retomar um trabalho suspenso, use o cmdlet **resume-AzureAutomationJob** .</span><span class="sxs-lookup"><span data-stu-id="465b2-108">To resume a suspended job, use the **Resume-AzureAutomationJob** cmdlet.</span></span>

## <span data-ttu-id="465b2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="465b2-109">EXAMPLES</span></span>

### <span data-ttu-id="465b2-110">Exemplo 1: suspender um trabalho</span><span class="sxs-lookup"><span data-stu-id="465b2-110">Example 1: Suspend a job</span></span>
```
PS C:\> Suspend-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="465b2-111">Esse comando suspende o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="465b2-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="465b2-112">OS</span><span class="sxs-lookup"><span data-stu-id="465b2-112">PARAMETERS</span></span>

### <span data-ttu-id="465b2-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="465b2-113">-AutomationAccountName</span></span>
<span data-ttu-id="465b2-114">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="465b2-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="465b2-115">-ID</span><span class="sxs-lookup"><span data-stu-id="465b2-115">-Id</span></span>
<span data-ttu-id="465b2-116">Especifica a ID de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="465b2-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="465b2-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="465b2-117">-Profile</span></span>
<span data-ttu-id="465b2-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="465b2-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="465b2-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="465b2-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="465b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="465b2-120">CommonParameters</span></span>
<span data-ttu-id="465b2-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="465b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="465b2-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="465b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="465b2-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="465b2-123">INPUTS</span></span>

## <span data-ttu-id="465b2-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="465b2-124">OUTPUTS</span></span>

## <span data-ttu-id="465b2-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="465b2-125">NOTES</span></span>

## <span data-ttu-id="465b2-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="465b2-126">RELATED LINKS</span></span>

[<span data-ttu-id="465b2-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="465b2-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="465b2-128">Currículo-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="465b2-128">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="465b2-129">Parar-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="465b2-129">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)


