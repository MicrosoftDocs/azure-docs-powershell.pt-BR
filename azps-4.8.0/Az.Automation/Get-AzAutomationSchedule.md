---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956029"
---
# <span data-ttu-id="3af5d-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3af5d-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="3af5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3af5d-102">SYNOPSIS</span></span>
<span data-ttu-id="3af5d-103">Obtém um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="3af5d-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="3af5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3af5d-104">SYNTAX</span></span>

### <span data-ttu-id="3af5d-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="3af5d-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3af5d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3af5d-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3af5d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3af5d-107">DESCRIPTION</span></span>
<span data-ttu-id="3af5d-108">O cmdlet **Get-AzAutomationSchedule** Obtém um cronograma de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3af5d-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="3af5d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3af5d-109">EXAMPLES</span></span>

### <span data-ttu-id="3af5d-110">Exemplo 1: obter um cronograma</span><span class="sxs-lookup"><span data-stu-id="3af5d-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3af5d-111">Este comando obtém o cronograma chamado DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="3af5d-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="3af5d-112">OS</span><span class="sxs-lookup"><span data-stu-id="3af5d-112">PARAMETERS</span></span>

### <span data-ttu-id="3af5d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3af5d-113">-AutomationAccountName</span></span>
<span data-ttu-id="3af5d-114">Especifica o nome de uma conta de automação para a qual esse cmdlet tem um cronograma.</span><span class="sxs-lookup"><span data-stu-id="3af5d-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="3af5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af5d-115">-DefaultProfile</span></span>
<span data-ttu-id="3af5d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3af5d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3af5d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3af5d-117">-Name</span></span>
<span data-ttu-id="3af5d-118">Especifica o nome de uma agenda obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af5d-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3af5d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af5d-119">-ResourceGroupName</span></span>
<span data-ttu-id="3af5d-120">Especifica o nome de um grupo de recursos para o qual esse cmdlet recebe um cronograma.</span><span class="sxs-lookup"><span data-stu-id="3af5d-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="3af5d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af5d-121">CommonParameters</span></span>
<span data-ttu-id="3af5d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af5d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af5d-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af5d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af5d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3af5d-124">INPUTS</span></span>

### <span data-ttu-id="3af5d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3af5d-125">System.String</span></span>

## <span data-ttu-id="3af5d-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3af5d-126">OUTPUTS</span></span>

### <span data-ttu-id="3af5d-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="3af5d-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="3af5d-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3af5d-128">NOTES</span></span>

## <span data-ttu-id="3af5d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3af5d-129">RELATED LINKS</span></span>

[<span data-ttu-id="3af5d-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3af5d-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="3af5d-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3af5d-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="3af5d-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3af5d-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


