---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: EA7C1449-E11F-4AE8-A513-59BDCA38875D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e432edd2469fa25519c12f0cd1f2dadb1d0dca2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946587"
---
# <span data-ttu-id="de20d-101">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="de20d-101">Unregister-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="de20d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de20d-102">SYNOPSIS</span></span>

<span data-ttu-id="de20d-103">Remove uma associação entre um runbook e um cronograma.</span><span class="sxs-lookup"><span data-stu-id="de20d-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="de20d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de20d-104">SYNTAX</span></span>

### <span data-ttu-id="de20d-105">ByJobScheduleId (padrão)</span><span class="sxs-lookup"><span data-stu-id="de20d-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="de20d-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="de20d-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="de20d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de20d-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="de20d-108">O cmdlet **Unregister-AzureAutomationScheduledRunbook** remove a associação entre um runbook de automação do Microsoft Azure e um cronograma, o que interrompe o início do runbook quando o cronograma é acionado.</span><span class="sxs-lookup"><span data-stu-id="de20d-108">The **Unregister-AzureAutomationScheduledRunbook** cmdlet removes the association between a Microsoft Azure Automation runbook and a schedule, which stops the runbook from starting when the schedule fires.</span></span>

## <span data-ttu-id="de20d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de20d-109">EXAMPLES</span></span>

### <span data-ttu-id="de20d-110">Exemplo 1: remover a associação entre um runbook e um cronograma</span><span class="sxs-lookup"><span data-stu-id="de20d-110">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\> Unregister-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="de20d-111">Esse comando Remove a associação entre o runbook chamado Runbk01 e o agendamento chamado Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="de20d-111">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="de20d-112">OS</span><span class="sxs-lookup"><span data-stu-id="de20d-112">PARAMETERS</span></span>

### <span data-ttu-id="de20d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="de20d-113">-AutomationAccountName</span></span>
<span data-ttu-id="de20d-114">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="de20d-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="de20d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="de20d-115">-Force</span></span>
<span data-ttu-id="de20d-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="de20d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de20d-117">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="de20d-117">-JobScheduleId</span></span>
<span data-ttu-id="de20d-118">Especifica a ID de um runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="de20d-118">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de20d-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="de20d-119">-Profile</span></span>
<span data-ttu-id="de20d-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="de20d-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="de20d-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="de20d-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="de20d-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="de20d-122">-RunbookName</span></span>
<span data-ttu-id="de20d-123">Especifica o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="de20d-123">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de20d-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="de20d-124">-ScheduleName</span></span>
<span data-ttu-id="de20d-125">Especifica o nome de um cronograma.</span><span class="sxs-lookup"><span data-stu-id="de20d-125">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de20d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de20d-126">CommonParameters</span></span>
<span data-ttu-id="de20d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de20d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de20d-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de20d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de20d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de20d-129">INPUTS</span></span>

## <span data-ttu-id="de20d-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de20d-130">OUTPUTS</span></span>

## <span data-ttu-id="de20d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de20d-131">NOTES</span></span>

## <span data-ttu-id="de20d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de20d-132">RELATED LINKS</span></span>

[<span data-ttu-id="de20d-133">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="de20d-133">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)


