---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117009"
---
# <span data-ttu-id="87628-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="87628-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="87628-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87628-102">SYNOPSIS</span></span>
<span data-ttu-id="87628-103">Obtém um cronograma de Automação.</span><span class="sxs-lookup"><span data-stu-id="87628-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="87628-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87628-104">SYNTAX</span></span>

### <span data-ttu-id="87628-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="87628-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87628-106">ByName</span><span class="sxs-lookup"><span data-stu-id="87628-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87628-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="87628-107">DESCRIPTION</span></span>
<span data-ttu-id="87628-108">O cmdlet **Get-AzAutomationSchedule** obtém um cronograma de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="87628-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="87628-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="87628-109">EXAMPLES</span></span>

### <span data-ttu-id="87628-110">Exemplo 1: Obter um cronograma</span><span class="sxs-lookup"><span data-stu-id="87628-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="87628-111">Esse comando obtém o cronograma chamado DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="87628-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="87628-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87628-112">PARAMETERS</span></span>

### <span data-ttu-id="87628-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="87628-113">-AutomationAccountName</span></span>
<span data-ttu-id="87628-114">Especifica o nome de uma conta de Automação para a qual este cmdlet obterá um cronograma.</span><span class="sxs-lookup"><span data-stu-id="87628-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="87628-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87628-115">-DefaultProfile</span></span>
<span data-ttu-id="87628-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="87628-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87628-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="87628-117">-Name</span></span>
<span data-ttu-id="87628-118">Especifica o nome de um cronograma que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="87628-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="87628-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87628-119">-ResourceGroupName</span></span>
<span data-ttu-id="87628-120">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém um cronograma.</span><span class="sxs-lookup"><span data-stu-id="87628-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="87628-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87628-121">CommonParameters</span></span>
<span data-ttu-id="87628-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87628-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87628-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87628-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87628-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="87628-124">INPUTS</span></span>

### <span data-ttu-id="87628-125">System.String</span><span class="sxs-lookup"><span data-stu-id="87628-125">System.String</span></span>

## <span data-ttu-id="87628-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="87628-126">OUTPUTS</span></span>

### <span data-ttu-id="87628-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="87628-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="87628-128">Notas</span><span class="sxs-lookup"><span data-stu-id="87628-128">NOTES</span></span>

## <span data-ttu-id="87628-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87628-129">RELATED LINKS</span></span>

[<span data-ttu-id="87628-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="87628-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="87628-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="87628-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="87628-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="87628-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


