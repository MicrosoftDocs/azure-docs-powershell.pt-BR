---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945657"
---
# <span data-ttu-id="93a53-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="93a53-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="93a53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93a53-102">SYNOPSIS</span></span>

<span data-ttu-id="93a53-103">Obtém um runbook.</span><span class="sxs-lookup"><span data-stu-id="93a53-103">Gets a runbook.</span></span>

## <span data-ttu-id="93a53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93a53-104">SYNTAX</span></span>

### <span data-ttu-id="93a53-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="93a53-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="93a53-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="93a53-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="93a53-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93a53-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="93a53-108">O cmdlet **Get-AzureAutomationRunbook** Obtém um ou mais Runbooks de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="93a53-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="93a53-109">Por padrão, todos os runbooks são retornados.</span><span class="sxs-lookup"><span data-stu-id="93a53-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="93a53-110">Para obter um runbook específico, especifique seu nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="93a53-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="93a53-111">Para obter todos os runbooks vinculados a um cronograma específico, especifique o nome do cronograma.</span><span class="sxs-lookup"><span data-stu-id="93a53-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="93a53-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93a53-112">EXAMPLES</span></span>

### <span data-ttu-id="93a53-113">Exemplo 1: obter todos os runbooks</span><span class="sxs-lookup"><span data-stu-id="93a53-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="93a53-114">Esse comando obtém todos os runbooks na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="93a53-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="93a53-115">OS</span><span class="sxs-lookup"><span data-stu-id="93a53-115">PARAMETERS</span></span>

### <span data-ttu-id="93a53-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="93a53-116">-AutomationAccountName</span></span>
<span data-ttu-id="93a53-117">Especifica o nome de uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="93a53-117">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="93a53-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="93a53-118">-Name</span></span>
<span data-ttu-id="93a53-119">Especifica o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="93a53-119">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a53-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="93a53-120">-Profile</span></span>
<span data-ttu-id="93a53-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="93a53-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93a53-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="93a53-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93a53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a53-123">CommonParameters</span></span>
<span data-ttu-id="93a53-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93a53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a53-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93a53-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a53-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93a53-126">INPUTS</span></span>

## <span data-ttu-id="93a53-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93a53-127">OUTPUTS</span></span>

### <span data-ttu-id="93a53-128">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="93a53-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="93a53-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93a53-129">NOTES</span></span>

## <span data-ttu-id="93a53-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93a53-130">RELATED LINKS</span></span>

[<span data-ttu-id="93a53-131">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="93a53-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="93a53-132">Publicar-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="93a53-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="93a53-133">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="93a53-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="93a53-134">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="93a53-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="93a53-135">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="93a53-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


