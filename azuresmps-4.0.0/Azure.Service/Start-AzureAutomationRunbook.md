---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946032"
---
# <span data-ttu-id="ceb61-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ceb61-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="ceb61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ceb61-102">SYNOPSIS</span></span>

<span data-ttu-id="ceb61-103">Inicia um trabalho de runbook.</span><span class="sxs-lookup"><span data-stu-id="ceb61-103">Starts a runbook job.</span></span>

## <span data-ttu-id="ceb61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ceb61-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ceb61-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ceb61-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ceb61-106">O cmdlet **Start-AzureAutomationRunbook** inicia um trabalho de runbook de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ceb61-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="ceb61-107">Especifique a ID ou o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="ceb61-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="ceb61-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ceb61-108">EXAMPLES</span></span>

### <span data-ttu-id="ceb61-109">Exemplo 1: iniciar um trabalho de runbook</span><span class="sxs-lookup"><span data-stu-id="ceb61-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="ceb61-110">Esse comando inicia um trabalho de runbook para o runbook chamado Runbk01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ceb61-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ceb61-111">OS</span><span class="sxs-lookup"><span data-stu-id="ceb61-111">PARAMETERS</span></span>

### <span data-ttu-id="ceb61-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ceb61-112">-AutomationAccountName</span></span>
<span data-ttu-id="ceb61-113">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ceb61-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="ceb61-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ceb61-114">-Name</span></span>
<span data-ttu-id="ceb61-115">Especifica o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="ceb61-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb61-116">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ceb61-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb61-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ceb61-117">-Profile</span></span>
<span data-ttu-id="ceb61-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ceb61-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ceb61-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ceb61-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ceb61-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="ceb61-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb61-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb61-121">CommonParameters</span></span>
<span data-ttu-id="ceb61-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb61-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb61-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb61-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb61-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ceb61-124">INPUTS</span></span>

## <span data-ttu-id="ceb61-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ceb61-125">OUTPUTS</span></span>

### <span data-ttu-id="ceb61-126">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="ceb61-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="ceb61-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ceb61-127">NOTES</span></span>

## <span data-ttu-id="ceb61-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ceb61-128">RELATED LINKS</span></span>

[<span data-ttu-id="ceb61-129">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ceb61-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="ceb61-130">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ceb61-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="ceb61-131">Publicar-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ceb61-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="ceb61-132">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ceb61-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="ceb61-133">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ceb61-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


