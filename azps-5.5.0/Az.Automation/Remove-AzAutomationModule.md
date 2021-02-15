---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118004"
---
# <span data-ttu-id="84f09-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="84f09-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="84f09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84f09-102">SYNOPSIS</span></span>
<span data-ttu-id="84f09-103">Remove um módulo da Automação.</span><span class="sxs-lookup"><span data-stu-id="84f09-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="84f09-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84f09-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84f09-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="84f09-105">DESCRIPTION</span></span>
<span data-ttu-id="84f09-106">O cmdlet **Remove-AzAutomationModule** remove um módulo de uma conta de Automação no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="84f09-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="84f09-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84f09-107">EXAMPLES</span></span>

### <span data-ttu-id="84f09-108">Exemplo 1: Remover um módulo</span><span class="sxs-lookup"><span data-stu-id="84f09-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="84f09-109">Esse comando remove um módulo chamado ContosoModule da conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="84f09-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="84f09-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84f09-110">PARAMETERS</span></span>

### <span data-ttu-id="84f09-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="84f09-111">-AutomationAccountName</span></span>
<span data-ttu-id="84f09-112">Especifica o nome da conta automação da qual este cmdlet remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="84f09-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="84f09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f09-113">-DefaultProfile</span></span>
<span data-ttu-id="84f09-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="84f09-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84f09-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="84f09-115">-Force</span></span>
<span data-ttu-id="84f09-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="84f09-116">ps_force</span></span>

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

### <span data-ttu-id="84f09-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="84f09-117">-Name</span></span>
<span data-ttu-id="84f09-118">Especifica o nome do módulo que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="84f09-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="84f09-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84f09-119">-ResourceGroupName</span></span>
<span data-ttu-id="84f09-120">Especifica o nome de um grupo de recursos no qual este cmdlet remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="84f09-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="84f09-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="84f09-121">-Confirm</span></span>
<span data-ttu-id="84f09-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84f09-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84f09-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84f09-123">-WhatIf</span></span>
<span data-ttu-id="84f09-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="84f09-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84f09-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84f09-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84f09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f09-126">CommonParameters</span></span>
<span data-ttu-id="84f09-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84f09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f09-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84f09-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f09-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="84f09-129">INPUTS</span></span>

### <span data-ttu-id="84f09-130">System.String</span><span class="sxs-lookup"><span data-stu-id="84f09-130">System.String</span></span>

## <span data-ttu-id="84f09-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="84f09-131">OUTPUTS</span></span>

### <span data-ttu-id="84f09-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="84f09-132">System.Void</span></span>

## <span data-ttu-id="84f09-133">Notas</span><span class="sxs-lookup"><span data-stu-id="84f09-133">NOTES</span></span>

## <span data-ttu-id="84f09-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84f09-134">RELATED LINKS</span></span>

[<span data-ttu-id="84f09-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="84f09-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="84f09-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="84f09-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="84f09-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="84f09-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


