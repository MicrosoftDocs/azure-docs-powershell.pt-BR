---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946071"
---
# <span data-ttu-id="304e0-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="304e0-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="304e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="304e0-102">SYNOPSIS</span></span>

<span data-ttu-id="304e0-103">Modifica um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="304e0-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="304e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="304e0-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="304e0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="304e0-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="304e0-106">O cmdlet **set-AzureAutomationSchedule** modifica um cronograma na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="304e0-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="304e0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="304e0-107">EXAMPLES</span></span>

### <span data-ttu-id="304e0-108">Exemplo 1: modificar um cronograma</span><span class="sxs-lookup"><span data-stu-id="304e0-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="304e0-109">Esse comando modifica a descrição do cronograma chamado Schedule01.</span><span class="sxs-lookup"><span data-stu-id="304e0-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="304e0-110">OS</span><span class="sxs-lookup"><span data-stu-id="304e0-110">PARAMETERS</span></span>

### <span data-ttu-id="304e0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="304e0-111">-AutomationAccountName</span></span>
<span data-ttu-id="304e0-112">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="304e0-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="304e0-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="304e0-113">-Description</span></span>
<span data-ttu-id="304e0-114">Especifica uma descrição para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="304e0-114">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="304e0-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="304e0-115">-IsEnabled</span></span>
<span data-ttu-id="304e0-116">Indica se o cronograma está habilitado.</span><span class="sxs-lookup"><span data-stu-id="304e0-116">Indicates whether the schedule is enabled.</span></span>

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

### <span data-ttu-id="304e0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="304e0-117">-Name</span></span>
<span data-ttu-id="304e0-118">Especifica um nome para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="304e0-118">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="304e0-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="304e0-119">-Profile</span></span>
<span data-ttu-id="304e0-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="304e0-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="304e0-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="304e0-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="304e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304e0-122">CommonParameters</span></span>
<span data-ttu-id="304e0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="304e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304e0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="304e0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304e0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="304e0-125">INPUTS</span></span>

## <span data-ttu-id="304e0-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="304e0-126">OUTPUTS</span></span>

### <span data-ttu-id="304e0-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="304e0-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="304e0-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="304e0-128">NOTES</span></span>

## <span data-ttu-id="304e0-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="304e0-129">RELATED LINKS</span></span>

[<span data-ttu-id="304e0-130">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="304e0-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="304e0-131">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="304e0-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="304e0-132">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="304e0-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


