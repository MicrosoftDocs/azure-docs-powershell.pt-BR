---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946170"
---
# <span data-ttu-id="6b1a6-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6b1a6-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="6b1a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b1a6-102">SYNOPSIS</span></span>

<span data-ttu-id="6b1a6-103">Exclui um cronograma de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="6b1a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b1a6-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b1a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b1a6-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6b1a6-106">O cmdlet **Remove-AzureAutomationSchedule** exclui um cronograma da automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="6b1a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b1a6-107">EXAMPLES</span></span>

### <span data-ttu-id="6b1a6-108">Exemplo 1: remover um cronograma</span><span class="sxs-lookup"><span data-stu-id="6b1a6-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="6b1a6-109">Esse comando Remove o cronograma chamado MySchedule.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="6b1a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="6b1a6-110">PARAMETERS</span></span>

### <span data-ttu-id="6b1a6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6b1a6-111">-AutomationAccountName</span></span>
<span data-ttu-id="6b1a6-112">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="6b1a6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6b1a6-113">-Force</span></span>
<span data-ttu-id="6b1a6-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b1a6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b1a6-115">-Name</span></span>
<span data-ttu-id="6b1a6-116">Especifica o nome do cronograma a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-116">Specifies the name of the schedule to remove.</span></span>

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

### <span data-ttu-id="6b1a6-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6b1a6-117">-Profile</span></span>
<span data-ttu-id="6b1a6-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6b1a6-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6b1a6-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b1a6-120">-Confirm</span></span>
<span data-ttu-id="6b1a6-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b1a6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b1a6-122">-WhatIf</span></span>
<span data-ttu-id="6b1a6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b1a6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b1a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1a6-125">CommonParameters</span></span>
<span data-ttu-id="6b1a6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1a6-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b1a6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1a6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b1a6-128">INPUTS</span></span>

## <span data-ttu-id="6b1a6-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b1a6-129">OUTPUTS</span></span>

## <span data-ttu-id="6b1a6-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b1a6-130">NOTES</span></span>

## <span data-ttu-id="6b1a6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b1a6-131">RELATED LINKS</span></span>

[<span data-ttu-id="6b1a6-132">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6b1a6-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="6b1a6-133">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6b1a6-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="6b1a6-134">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6b1a6-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


