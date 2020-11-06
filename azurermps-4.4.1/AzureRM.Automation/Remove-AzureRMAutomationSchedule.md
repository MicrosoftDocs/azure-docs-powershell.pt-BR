---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 562b5b5986d544f5fa8d91e0f39cb34ef9dababd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431816"
---
# <span data-ttu-id="8bf23-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="8bf23-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="8bf23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bf23-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf23-103">Exclui um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="8bf23-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bf23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bf23-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bf23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bf23-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf23-106">O cmdlet **Remove-AzureRmAutomationSchedule** exclui um cronograma da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf23-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="8bf23-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bf23-107">EXAMPLES</span></span>

### <span data-ttu-id="8bf23-108">Exemplo 1: remover um cronograma</span><span class="sxs-lookup"><span data-stu-id="8bf23-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8bf23-109">Esse comando modifica a descrição do cronograma chamado Schedule01.</span><span class="sxs-lookup"><span data-stu-id="8bf23-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="8bf23-110">OS</span><span class="sxs-lookup"><span data-stu-id="8bf23-110">PARAMETERS</span></span>

### <span data-ttu-id="8bf23-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8bf23-111">-AutomationAccountName</span></span>
<span data-ttu-id="8bf23-112">Especifica o nome de uma conta de automação para a qual esse cmdlet modifica um cronograma.</span><span class="sxs-lookup"><span data-stu-id="8bf23-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="8bf23-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8bf23-113">-Force</span></span>
<span data-ttu-id="8bf23-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="8bf23-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf23-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bf23-115">-Name</span></span>
<span data-ttu-id="8bf23-116">Especifica o nome do agendamento que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8bf23-116">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8bf23-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf23-117">-ResourceGroupName</span></span>
<span data-ttu-id="8bf23-118">Especifica o nome de um grupo de recursos para o qual esse cmdlet Remove um cronograma.</span><span class="sxs-lookup"><span data-stu-id="8bf23-118">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="8bf23-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bf23-119">-Confirm</span></span>
<span data-ttu-id="8bf23-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bf23-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf23-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf23-121">-WhatIf</span></span>
<span data-ttu-id="8bf23-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bf23-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf23-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bf23-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf23-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf23-124">-DefaultProfile</span></span>
<span data-ttu-id="8bf23-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf23-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bf23-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf23-126">CommonParameters</span></span>
<span data-ttu-id="8bf23-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf23-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf23-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bf23-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf23-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bf23-129">INPUTS</span></span>

## <span data-ttu-id="8bf23-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bf23-130">OUTPUTS</span></span>

## <span data-ttu-id="8bf23-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bf23-131">NOTES</span></span>

## <span data-ttu-id="8bf23-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bf23-132">RELATED LINKS</span></span>

[<span data-ttu-id="8bf23-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="8bf23-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="8bf23-134">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="8bf23-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="8bf23-135">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="8bf23-135">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


