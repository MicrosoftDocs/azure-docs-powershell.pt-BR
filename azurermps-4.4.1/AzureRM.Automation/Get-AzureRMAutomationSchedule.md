---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 1252864be8e55638ec5e982bd075aec647b68a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441422"
---
# <span data-ttu-id="4c945-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4c945-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="4c945-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c945-102">SYNOPSIS</span></span>
<span data-ttu-id="4c945-103">Obtém um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="4c945-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c945-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c945-104">SYNTAX</span></span>

### <span data-ttu-id="4c945-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="4c945-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c945-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4c945-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c945-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c945-107">DESCRIPTION</span></span>
<span data-ttu-id="4c945-108">O cmdlet **Get-AzureRmAutomationSchedule** Obtém um cronograma de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c945-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="4c945-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c945-109">EXAMPLES</span></span>

### <span data-ttu-id="4c945-110">Exemplo 1: obter um cronograma</span><span class="sxs-lookup"><span data-stu-id="4c945-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4c945-111">Este comando obtém o cronograma chamado DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="4c945-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="4c945-112">OS</span><span class="sxs-lookup"><span data-stu-id="4c945-112">PARAMETERS</span></span>

### <span data-ttu-id="4c945-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4c945-113">-AutomationAccountName</span></span>
<span data-ttu-id="4c945-114">Especifica o nome de uma conta de automação para a qual esse cmdlet tem um cronograma.</span><span class="sxs-lookup"><span data-stu-id="4c945-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="4c945-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c945-115">-Name</span></span>
<span data-ttu-id="4c945-116">Especifica o nome de uma agenda obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c945-116">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4c945-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c945-117">-ResourceGroupName</span></span>
<span data-ttu-id="4c945-118">Especifica o nome de um grupo de recursos para o qual esse cmdlet recebe um cronograma.</span><span class="sxs-lookup"><span data-stu-id="4c945-118">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="4c945-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c945-119">-DefaultProfile</span></span>
<span data-ttu-id="4c945-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c945-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c945-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c945-121">CommonParameters</span></span>
<span data-ttu-id="4c945-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c945-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c945-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c945-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c945-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c945-124">INPUTS</span></span>

## <span data-ttu-id="4c945-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c945-125">OUTPUTS</span></span>

### <span data-ttu-id="4c945-126">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="4c945-126">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="4c945-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c945-127">NOTES</span></span>

## <span data-ttu-id="4c945-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c945-128">RELATED LINKS</span></span>

[<span data-ttu-id="4c945-129">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4c945-129">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="4c945-130">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4c945-130">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="4c945-131">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4c945-131">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


