---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945655"
---
# <span data-ttu-id="caa67-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="caa67-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="caa67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="caa67-102">SYNOPSIS</span></span>

<span data-ttu-id="caa67-103">Obtém um cronograma de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="caa67-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="caa67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="caa67-104">SYNTAX</span></span>

### <span data-ttu-id="caa67-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="caa67-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="caa67-106">ByName</span><span class="sxs-lookup"><span data-stu-id="caa67-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="caa67-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="caa67-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="caa67-108">O cmdlet **Get-AzureAutomationSchedule** Obtém um cronograma de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="caa67-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="caa67-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="caa67-109">EXAMPLES</span></span>

### <span data-ttu-id="caa67-110">Exemplo 1: obter um cronograma</span><span class="sxs-lookup"><span data-stu-id="caa67-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="caa67-111">Este comando obtém o cronograma chamado DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="caa67-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="caa67-112">OS</span><span class="sxs-lookup"><span data-stu-id="caa67-112">PARAMETERS</span></span>

### <span data-ttu-id="caa67-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="caa67-113">-AutomationAccountName</span></span>
<span data-ttu-id="caa67-114">Especifica o nome de uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="caa67-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="caa67-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="caa67-115">-Name</span></span>
<span data-ttu-id="caa67-116">Especifica o nome de um cronograma.</span><span class="sxs-lookup"><span data-stu-id="caa67-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caa67-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="caa67-117">-Profile</span></span>
<span data-ttu-id="caa67-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="caa67-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="caa67-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="caa67-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="caa67-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa67-120">CommonParameters</span></span>
<span data-ttu-id="caa67-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caa67-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa67-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa67-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa67-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="caa67-123">INPUTS</span></span>

## <span data-ttu-id="caa67-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="caa67-124">OUTPUTS</span></span>

### <span data-ttu-id="caa67-125">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="caa67-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="caa67-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="caa67-126">NOTES</span></span>

## <span data-ttu-id="caa67-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="caa67-127">RELATED LINKS</span></span>

[<span data-ttu-id="caa67-128">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="caa67-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="caa67-129">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="caa67-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="caa67-130">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="caa67-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


