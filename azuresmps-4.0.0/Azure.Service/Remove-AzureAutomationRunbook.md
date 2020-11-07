---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946171"
---
# <span data-ttu-id="17a03-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="17a03-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="17a03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17a03-102">SYNOPSIS</span></span>

<span data-ttu-id="17a03-103">Remove um runbook.</span><span class="sxs-lookup"><span data-stu-id="17a03-103">Removes a runbook.</span></span>

## <span data-ttu-id="17a03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17a03-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17a03-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17a03-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="17a03-106">O cmdlet **Remove-AzureAutomationRunbook** remove um runbook da automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="17a03-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="17a03-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17a03-107">EXAMPLES</span></span>

### <span data-ttu-id="17a03-108">Exemplo 1: remover um runbook</span><span class="sxs-lookup"><span data-stu-id="17a03-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="17a03-109">Esse comando Remove o runbook chamado MyRunbook na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="17a03-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="17a03-110">OS</span><span class="sxs-lookup"><span data-stu-id="17a03-110">PARAMETERS</span></span>

### <span data-ttu-id="17a03-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17a03-111">-AutomationAccountName</span></span>
<span data-ttu-id="17a03-112">Especifica o nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="17a03-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="17a03-113">-Force</span><span class="sxs-lookup"><span data-stu-id="17a03-113">-Force</span></span>
<span data-ttu-id="17a03-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="17a03-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a03-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="17a03-115">-Name</span></span>
<span data-ttu-id="17a03-116">Especifica o nome do runbook a ser removido.</span><span class="sxs-lookup"><span data-stu-id="17a03-116">Specifies the name of the runbook to remove.</span></span>

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

### <span data-ttu-id="17a03-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="17a03-117">-Profile</span></span>
<span data-ttu-id="17a03-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="17a03-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17a03-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="17a03-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17a03-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17a03-120">-Confirm</span></span>
<span data-ttu-id="17a03-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17a03-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a03-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17a03-122">-WhatIf</span></span>
<span data-ttu-id="17a03-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17a03-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17a03-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17a03-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a03-125">CommonParameters</span></span>
<span data-ttu-id="17a03-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17a03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a03-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17a03-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a03-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17a03-128">INPUTS</span></span>

## <span data-ttu-id="17a03-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17a03-129">OUTPUTS</span></span>

## <span data-ttu-id="17a03-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17a03-130">NOTES</span></span>

## <span data-ttu-id="17a03-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17a03-131">RELATED LINKS</span></span>

[<span data-ttu-id="17a03-132">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="17a03-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="17a03-133">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="17a03-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="17a03-134">Publicar-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="17a03-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="17a03-135">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="17a03-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="17a03-136">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="17a03-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


