---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945873"
---
# <span data-ttu-id="ce841-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="ce841-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="ce841-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce841-102">SYNOPSIS</span></span>

<span data-ttu-id="ce841-103">Associa um runbook a um cronograma.</span><span class="sxs-lookup"><span data-stu-id="ce841-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="ce841-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce841-104">SYNTAX</span></span>

### <span data-ttu-id="ce841-105">ByRunbookName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce841-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce841-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="ce841-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ce841-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce841-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ce841-108">O cmdlet **Register-AzureAutomationScheduledRunbook** associa um runbook a um cronograma.</span><span class="sxs-lookup"><span data-stu-id="ce841-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="ce841-109">O runbook começará com base no agendamento especificado usando o parâmetro *Scheduler* .</span><span class="sxs-lookup"><span data-stu-id="ce841-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="ce841-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce841-110">EXAMPLES</span></span>

### <span data-ttu-id="ce841-111">Exemplo 1: associar um runbook a um cronograma</span><span class="sxs-lookup"><span data-stu-id="ce841-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="ce841-112">Esse comando associa o runbook chamado Runbk01 com o cronograma chamado Sched01 na conta de automação do Azure chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ce841-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ce841-113">OS</span><span class="sxs-lookup"><span data-stu-id="ce841-113">PARAMETERS</span></span>

### <span data-ttu-id="ce841-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ce841-114">-AutomationAccountName</span></span>
<span data-ttu-id="ce841-115">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ce841-115">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="ce841-116">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce841-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce841-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ce841-117">-Profile</span></span>
<span data-ttu-id="ce841-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ce841-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce841-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ce841-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce841-120">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="ce841-120">-RunbookName</span></span>
<span data-ttu-id="ce841-121">Especifica o nome do runbook.</span><span class="sxs-lookup"><span data-stu-id="ce841-121">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="ce841-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="ce841-122">-ScheduleName</span></span>
<span data-ttu-id="ce841-123">Especifica o nome do cronograma.</span><span class="sxs-lookup"><span data-stu-id="ce841-123">Specifies the name of the schedule.</span></span>

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

### <span data-ttu-id="ce841-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce841-124">CommonParameters</span></span>
<span data-ttu-id="ce841-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce841-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce841-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce841-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce841-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce841-127">INPUTS</span></span>

## <span data-ttu-id="ce841-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce841-128">OUTPUTS</span></span>

### <span data-ttu-id="ce841-129">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="ce841-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="ce841-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce841-130">NOTES</span></span>

## <span data-ttu-id="ce841-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce841-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce841-132">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ce841-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="ce841-133">Cancelar registro-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="ce841-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


