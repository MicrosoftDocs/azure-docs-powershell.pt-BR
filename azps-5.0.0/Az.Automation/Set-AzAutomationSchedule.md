---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117659"
---
# <span data-ttu-id="f4303-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f4303-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="f4303-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4303-102">SYNOPSIS</span></span>
<span data-ttu-id="f4303-103">Modifica um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="f4303-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="f4303-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4303-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4303-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4303-105">DESCRIPTION</span></span>
<span data-ttu-id="f4303-106">O cmdlet **set-AzAutomationSchedule** modifica um cronograma na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4303-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="f4303-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4303-107">EXAMPLES</span></span>

### <span data-ttu-id="f4303-108">Exemplo 1: modificar um cronograma</span><span class="sxs-lookup"><span data-stu-id="f4303-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f4303-109">Esse comando modifica a descrição do cronograma chamado Schedule01.</span><span class="sxs-lookup"><span data-stu-id="f4303-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="f4303-110">OS</span><span class="sxs-lookup"><span data-stu-id="f4303-110">PARAMETERS</span></span>

### <span data-ttu-id="f4303-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f4303-111">-AutomationAccountName</span></span>
<span data-ttu-id="f4303-112">Especifica o nome de uma conta de automação para a qual esse cmdlet modifica um cronograma.</span><span class="sxs-lookup"><span data-stu-id="f4303-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="f4303-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4303-113">-DefaultProfile</span></span>
<span data-ttu-id="f4303-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f4303-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4303-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f4303-115">-Description</span></span>
<span data-ttu-id="f4303-116">Especifica uma descrição para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="f4303-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4303-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="f4303-117">-IsEnabled</span></span>
<span data-ttu-id="f4303-118">Especifica se esse cmdlet habilita o cronograma.</span><span class="sxs-lookup"><span data-stu-id="f4303-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4303-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4303-119">-Name</span></span>
<span data-ttu-id="f4303-120">Especifica o nome do agendamento que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f4303-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4303-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4303-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4303-122">Especifica o nome de um grupo de recursos para o qual esse cmdlet modifica um cronograma.</span><span class="sxs-lookup"><span data-stu-id="f4303-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="f4303-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4303-123">CommonParameters</span></span>
<span data-ttu-id="f4303-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4303-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4303-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4303-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4303-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4303-126">INPUTS</span></span>

### <span data-ttu-id="f4303-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f4303-127">System.String</span></span>

### <span data-ttu-id="f4303-128">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4303-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f4303-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4303-129">OUTPUTS</span></span>

### <span data-ttu-id="f4303-130">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="f4303-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="f4303-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4303-131">NOTES</span></span>

## <span data-ttu-id="f4303-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4303-132">RELATED LINKS</span></span>

[<span data-ttu-id="f4303-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f4303-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="f4303-134">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f4303-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="f4303-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f4303-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


