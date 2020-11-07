---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945885"
---
# <span data-ttu-id="311d9-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="311d9-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="311d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="311d9-102">SYNOPSIS</span></span>

<span data-ttu-id="311d9-103">Publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="311d9-103">Publishes a runbook.</span></span>

## <span data-ttu-id="311d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="311d9-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="311d9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="311d9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="311d9-106">O cmdlet **Publish-AzureAutomationRunbook** publica um runbook para uso no ambiente de produção da automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="311d9-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="311d9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="311d9-107">EXAMPLES</span></span>

### <span data-ttu-id="311d9-108">Exemplo 1: publicar um runbook</span><span class="sxs-lookup"><span data-stu-id="311d9-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="311d9-109">Esse comando publica o runbook chamado Runbk01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="311d9-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="311d9-110">OS</span><span class="sxs-lookup"><span data-stu-id="311d9-110">PARAMETERS</span></span>

### <span data-ttu-id="311d9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="311d9-111">-AutomationAccountName</span></span>
<span data-ttu-id="311d9-112">Especifica o nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="311d9-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="311d9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="311d9-113">-Name</span></span>
<span data-ttu-id="311d9-114">Especifica o nome do runbook.</span><span class="sxs-lookup"><span data-stu-id="311d9-114">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="311d9-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="311d9-115">-Profile</span></span>
<span data-ttu-id="311d9-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="311d9-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="311d9-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="311d9-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="311d9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311d9-118">CommonParameters</span></span>
<span data-ttu-id="311d9-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311d9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311d9-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="311d9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311d9-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="311d9-121">INPUTS</span></span>

## <span data-ttu-id="311d9-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="311d9-122">OUTPUTS</span></span>

## <span data-ttu-id="311d9-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="311d9-123">NOTES</span></span>

## <span data-ttu-id="311d9-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="311d9-124">RELATED LINKS</span></span>

[<span data-ttu-id="311d9-125">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="311d9-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="311d9-126">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="311d9-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="311d9-127">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="311d9-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="311d9-128">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="311d9-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="311d9-129">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="311d9-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


