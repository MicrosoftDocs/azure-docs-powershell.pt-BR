---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: fe8d7b4407aa5afc3454d80e4cf45c102d9006bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441419"
---
# <span data-ttu-id="3ee5b-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3ee5b-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="3ee5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ee5b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee5b-103">Obtém runbooks de automação e cronogramas associados.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ee5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ee5b-104">SYNTAX</span></span>

### <span data-ttu-id="3ee5b-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="3ee5b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ee5b-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="3ee5b-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ee5b-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="3ee5b-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ee5b-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="3ee5b-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ee5b-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="3ee5b-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ee5b-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ee5b-110">DESCRIPTION</span></span>
<span data-ttu-id="3ee5b-111">O cmdlet **Get-AzureRmAutomationScheduledRunbook** Obtém um ou mais Runbooks de automação do Azure e cronogramas associados.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="3ee5b-112">Por padrão, esse cmdlet obtém todos os runbooks programados.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="3ee5b-113">Especifique o nome de um runbook ou um cronograma ou ambos para ver agendas de runbook específicas.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="3ee5b-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ee5b-114">EXAMPLES</span></span>

### <span data-ttu-id="3ee5b-115">Exemplo 1: obter todos os runbooks agendados</span><span class="sxs-lookup"><span data-stu-id="3ee5b-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3ee5b-116">Esse comando obtém todos os runbooks agendados na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="3ee5b-117">Exemplo 2: obter todos os cronogramas associados a um runbook</span><span class="sxs-lookup"><span data-stu-id="3ee5b-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="3ee5b-118">Esse comando obtém todos os runbooks agendados para o runbook Runbk01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="3ee5b-119">Exemplo 3: obter todos os runbooks associados a um cronograma</span><span class="sxs-lookup"><span data-stu-id="3ee5b-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="3ee5b-120">Esse comando obtém todos os runbooks agendados para o Schedule Schedule01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3ee5b-121">OS</span><span class="sxs-lookup"><span data-stu-id="3ee5b-121">PARAMETERS</span></span>

### <span data-ttu-id="3ee5b-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ee5b-122">-AutomationAccountName</span></span>
<span data-ttu-id="3ee5b-123">Especifica uma conta de automação para o runbook no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee5b-124">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="3ee5b-124">-JobScheduleId</span></span>
<span data-ttu-id="3ee5b-125">Especifica a ID de um trabalho agendado que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-125">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee5b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee5b-126">-ResourceGroupName</span></span>
<span data-ttu-id="3ee5b-127">Especifica o nome de um grupo de recursos para os runbooks agendados que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-127">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee5b-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="3ee5b-128">-RunbookName</span></span>
<span data-ttu-id="3ee5b-129">Especifica o nome de um runbook para o qual esse cmdlet obtém runbooks agendados.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-129">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee5b-130">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="3ee5b-130">-ScheduleName</span></span>
<span data-ttu-id="3ee5b-131">Especifica o nome de um cronograma para o qual esse cmdlet obtém runbooks agendados.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-131">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee5b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee5b-132">-DefaultProfile</span></span>
<span data-ttu-id="3ee5b-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee5b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee5b-134">CommonParameters</span></span>
<span data-ttu-id="3ee5b-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee5b-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee5b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee5b-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ee5b-137">INPUTS</span></span>

## <span data-ttu-id="3ee5b-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ee5b-138">OUTPUTS</span></span>

### <span data-ttu-id="3ee5b-139">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ee5b-139">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="3ee5b-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ee5b-140">NOTES</span></span>

## <span data-ttu-id="3ee5b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ee5b-141">RELATED LINKS</span></span>

[<span data-ttu-id="3ee5b-142">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3ee5b-142">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="3ee5b-143">Cancelar registro-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3ee5b-143">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


