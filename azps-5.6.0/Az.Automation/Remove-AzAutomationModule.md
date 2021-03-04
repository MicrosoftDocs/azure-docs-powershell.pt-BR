---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 9fa84ffed6352dfb566ad02aa2393a7cba7f393b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892889"
---
# <span data-ttu-id="ead86-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ead86-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="ead86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ead86-102">SYNOPSIS</span></span>
<span data-ttu-id="ead86-103">Remove um módulo da Automação.</span><span class="sxs-lookup"><span data-stu-id="ead86-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="ead86-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ead86-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ead86-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ead86-105">DESCRIPTION</span></span>
<span data-ttu-id="ead86-106">O cmdlet **Remove-AzAutomationModule** remove um módulo de uma conta de automação no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ead86-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="ead86-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ead86-107">EXAMPLES</span></span>

### <span data-ttu-id="ead86-108">Exemplo 1: Remover um módulo</span><span class="sxs-lookup"><span data-stu-id="ead86-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ead86-109">Este comando remove um módulo chamado ContosoModule da conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ead86-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ead86-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ead86-110">PARAMETERS</span></span>

### <span data-ttu-id="ead86-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ead86-111">-AutomationAccountName</span></span>
<span data-ttu-id="ead86-112">Especifica o nome da conta de automação da qual este cmdlet remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="ead86-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="ead86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead86-113">-DefaultProfile</span></span>
<span data-ttu-id="ead86-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ead86-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ead86-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ead86-115">-Force</span></span>
<span data-ttu-id="ead86-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="ead86-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead86-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ead86-117">-Name</span></span>
<span data-ttu-id="ead86-118">Especifica o nome do módulo que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="ead86-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ead86-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead86-119">-ResourceGroupName</span></span>
<span data-ttu-id="ead86-120">Especifica o nome de um grupo de recursos no qual este cmdlet remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="ead86-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="ead86-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ead86-121">-Confirm</span></span>
<span data-ttu-id="ead86-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ead86-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead86-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead86-123">-WhatIf</span></span>
<span data-ttu-id="ead86-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ead86-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead86-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ead86-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead86-126">CommonParameters</span></span>
<span data-ttu-id="ead86-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead86-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ead86-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead86-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ead86-129">INPUTS</span></span>

### <span data-ttu-id="ead86-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ead86-130">System.String</span></span>

## <span data-ttu-id="ead86-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ead86-131">OUTPUTS</span></span>

### <span data-ttu-id="ead86-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="ead86-132">System.Void</span></span>

## <span data-ttu-id="ead86-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="ead86-133">NOTES</span></span>

## <span data-ttu-id="ead86-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ead86-134">RELATED LINKS</span></span>

[<span data-ttu-id="ead86-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ead86-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="ead86-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ead86-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="ead86-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ead86-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


