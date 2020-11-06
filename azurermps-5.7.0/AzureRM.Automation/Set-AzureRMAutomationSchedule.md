---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: b311554fa5aeeae67829055506b85766fd6f9670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431745"
---
# <span data-ttu-id="e2050-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e2050-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="e2050-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2050-102">SYNOPSIS</span></span>
<span data-ttu-id="e2050-103">Modifica um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="e2050-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2050-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2050-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2050-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2050-105">DESCRIPTION</span></span>
<span data-ttu-id="e2050-106">O cmdlet **set-AzureRmAutomationSchedule** modifica um cronograma na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2050-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="e2050-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2050-107">EXAMPLES</span></span>

### <span data-ttu-id="e2050-108">Exemplo 1: modificar um cronograma</span><span class="sxs-lookup"><span data-stu-id="e2050-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e2050-109">Esse comando modifica a descrição do cronograma chamado Schedule01.</span><span class="sxs-lookup"><span data-stu-id="e2050-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="e2050-110">OS</span><span class="sxs-lookup"><span data-stu-id="e2050-110">PARAMETERS</span></span>

### <span data-ttu-id="e2050-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e2050-111">-AutomationAccountName</span></span>
<span data-ttu-id="e2050-112">Especifica o nome de uma conta de automação para a qual esse cmdlet modifica um cronograma.</span><span class="sxs-lookup"><span data-stu-id="e2050-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="e2050-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2050-113">-DefaultProfile</span></span>
<span data-ttu-id="e2050-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e2050-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2050-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e2050-115">-Description</span></span>
<span data-ttu-id="e2050-116">Especifica uma descrição para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="e2050-116">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2050-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e2050-117">-IsEnabled</span></span>
<span data-ttu-id="e2050-118">Especifica se esse cmdlet habilita o cronograma.</span><span class="sxs-lookup"><span data-stu-id="e2050-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2050-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2050-119">-Name</span></span>
<span data-ttu-id="e2050-120">Especifica o nome do agendamento que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e2050-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2050-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2050-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2050-122">Especifica o nome de um grupo de recursos para o qual esse cmdlet modifica um cronograma.</span><span class="sxs-lookup"><span data-stu-id="e2050-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="e2050-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2050-123">CommonParameters</span></span>
<span data-ttu-id="e2050-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2050-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2050-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2050-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2050-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2050-126">INPUTS</span></span>

### <span data-ttu-id="e2050-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e2050-127">None</span></span>
<span data-ttu-id="e2050-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e2050-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2050-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2050-129">OUTPUTS</span></span>

### <span data-ttu-id="e2050-130">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="e2050-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="e2050-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2050-131">NOTES</span></span>

## <span data-ttu-id="e2050-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2050-132">RELATED LINKS</span></span>

[<span data-ttu-id="e2050-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e2050-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="e2050-134">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e2050-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="e2050-135">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e2050-135">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


