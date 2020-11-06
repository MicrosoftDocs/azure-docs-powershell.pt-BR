---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: 459c217904ba44662d18c81c4c493a3b7f2033e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430527"
---
# <span data-ttu-id="317a7-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="317a7-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="317a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="317a7-102">SYNOPSIS</span></span>
<span data-ttu-id="317a7-103">Obtém runbooks de automação e cronogramas associados.</span><span class="sxs-lookup"><span data-stu-id="317a7-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="317a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="317a7-104">SYNTAX</span></span>

### <span data-ttu-id="317a7-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="317a7-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="317a7-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="317a7-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="317a7-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="317a7-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="317a7-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="317a7-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="317a7-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="317a7-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="317a7-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="317a7-110">DESCRIPTION</span></span>
<span data-ttu-id="317a7-111">O cmdlet **Get-AzureRmAutomationScheduledRunbook** Obtém um ou mais Runbooks de automação do Azure e cronogramas associados.</span><span class="sxs-lookup"><span data-stu-id="317a7-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="317a7-112">Por padrão, esse cmdlet obtém todos os runbooks programados.</span><span class="sxs-lookup"><span data-stu-id="317a7-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="317a7-113">Especifique o nome de um runbook ou um cronograma ou ambos para ver agendas de runbook específicas.</span><span class="sxs-lookup"><span data-stu-id="317a7-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="317a7-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="317a7-114">EXAMPLES</span></span>

### <span data-ttu-id="317a7-115">Exemplo 1: obter todos os runbooks agendados</span><span class="sxs-lookup"><span data-stu-id="317a7-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="317a7-116">Esse comando obtém todos os runbooks agendados na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="317a7-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="317a7-117">Exemplo 2: obter todos os cronogramas associados a um runbook</span><span class="sxs-lookup"><span data-stu-id="317a7-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="317a7-118">Esse comando obtém todos os runbooks agendados para o runbook Runbk01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="317a7-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="317a7-119">Exemplo 3: obter todos os runbooks associados a um cronograma</span><span class="sxs-lookup"><span data-stu-id="317a7-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="317a7-120">Esse comando obtém todos os runbooks agendados para o Schedule Schedule01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="317a7-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="317a7-121">OS</span><span class="sxs-lookup"><span data-stu-id="317a7-121">PARAMETERS</span></span>

### <span data-ttu-id="317a7-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="317a7-122">-AutomationAccountName</span></span>
<span data-ttu-id="317a7-123">Especifica uma conta de automação para o runbook no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="317a7-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317a7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317a7-124">-DefaultProfile</span></span>
<span data-ttu-id="317a7-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="317a7-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317a7-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="317a7-126">-JobScheduleId</span></span>
<span data-ttu-id="317a7-127">Especifica a ID de um trabalho agendado que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="317a7-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="317a7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="317a7-128">-ResourceGroupName</span></span>
<span data-ttu-id="317a7-129">Especifica o nome de um grupo de recursos para os runbooks agendados que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="317a7-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317a7-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="317a7-130">-RunbookName</span></span>
<span data-ttu-id="317a7-131">Especifica o nome de um runbook para o qual esse cmdlet obtém runbooks agendados.</span><span class="sxs-lookup"><span data-stu-id="317a7-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317a7-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="317a7-132">-ScheduleName</span></span>
<span data-ttu-id="317a7-133">Especifica o nome de um cronograma para o qual esse cmdlet obtém runbooks agendados.</span><span class="sxs-lookup"><span data-stu-id="317a7-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317a7-134">CommonParameters</span></span>
<span data-ttu-id="317a7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="317a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317a7-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="317a7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317a7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="317a7-137">INPUTS</span></span>

### <span data-ttu-id="317a7-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="317a7-138">None</span></span>
<span data-ttu-id="317a7-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="317a7-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="317a7-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="317a7-140">OUTPUTS</span></span>

### <span data-ttu-id="317a7-141">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="317a7-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="317a7-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="317a7-142">NOTES</span></span>

## <span data-ttu-id="317a7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="317a7-143">RELATED LINKS</span></span>

[<span data-ttu-id="317a7-144">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="317a7-144">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="317a7-145">Cancelar registro-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="317a7-145">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)

