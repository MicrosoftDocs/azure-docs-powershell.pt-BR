---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a32b86ce308f18537ec1acda62c2694e7b621d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901353"
---
# <span data-ttu-id="f26e4-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f26e4-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="f26e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f26e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f26e4-103">Obtém um agendamento de automação.</span><span class="sxs-lookup"><span data-stu-id="f26e4-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="f26e4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f26e4-104">SYNTAX</span></span>

### <span data-ttu-id="f26e4-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f26e4-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f26e4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f26e4-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f26e4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f26e4-107">DESCRIPTION</span></span>
<span data-ttu-id="f26e4-108">O cmdlet **Get-AzAutomationSchedule** obtém um cronograma de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="f26e4-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="f26e4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f26e4-109">EXAMPLES</span></span>

### <span data-ttu-id="f26e4-110">Exemplo 1: Obter um cronograma</span><span class="sxs-lookup"><span data-stu-id="f26e4-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f26e4-111">Este comando obtém a agenda chamada DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="f26e4-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="f26e4-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f26e4-112">PARAMETERS</span></span>

### <span data-ttu-id="f26e4-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f26e4-113">-AutomationAccountName</span></span>
<span data-ttu-id="f26e4-114">Especifica o nome de uma conta de automação para a qual este cmdlet obterá uma agenda.</span><span class="sxs-lookup"><span data-stu-id="f26e4-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="f26e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f26e4-115">-DefaultProfile</span></span>
<span data-ttu-id="f26e4-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f26e4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26e4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f26e4-117">-Name</span></span>
<span data-ttu-id="f26e4-118">Especifica o nome de um cronograma que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f26e4-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f26e4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f26e4-119">-ResourceGroupName</span></span>
<span data-ttu-id="f26e4-120">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém um cronograma.</span><span class="sxs-lookup"><span data-stu-id="f26e4-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="f26e4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f26e4-121">CommonParameters</span></span>
<span data-ttu-id="f26e4-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f26e4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f26e4-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f26e4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f26e4-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f26e4-124">INPUTS</span></span>

### <span data-ttu-id="f26e4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f26e4-125">System.String</span></span>

## <span data-ttu-id="f26e4-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f26e4-126">OUTPUTS</span></span>

### <span data-ttu-id="f26e4-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="f26e4-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="f26e4-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="f26e4-128">NOTES</span></span>

## <span data-ttu-id="f26e4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f26e4-129">RELATED LINKS</span></span>

[<span data-ttu-id="f26e4-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f26e4-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="f26e4-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f26e4-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="f26e4-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f26e4-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


