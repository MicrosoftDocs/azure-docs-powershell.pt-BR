---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116621"
---
# <span data-ttu-id="f78c7-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f78c7-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="f78c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f78c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f78c7-103">Remove uma variável automação.</span><span class="sxs-lookup"><span data-stu-id="f78c7-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="f78c7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f78c7-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f78c7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f78c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f78c7-106">O **cmdlet Remove-AzAutomationVariable** remove uma variável da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="f78c7-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="f78c7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f78c7-107">EXAMPLES</span></span>

### <span data-ttu-id="f78c7-108">Exemplo 1: Remover uma variável</span><span class="sxs-lookup"><span data-stu-id="f78c7-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f78c7-109">Esse comando remove uma variável chamada StringVariable22 na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f78c7-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f78c7-110">Esse comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="f78c7-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f78c7-111">Portanto, ele não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="f78c7-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f78c7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f78c7-112">PARAMETERS</span></span>

### <span data-ttu-id="f78c7-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f78c7-113">-AutomationAccountName</span></span>
<span data-ttu-id="f78c7-114">Especifica o nome da conta automação que contém a variável que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="f78c7-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f78c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78c7-115">-DefaultProfile</span></span>
<span data-ttu-id="f78c7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f78c7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f78c7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f78c7-117">-Name</span></span>
<span data-ttu-id="f78c7-118">Especifica o nome da variável que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="f78c7-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f78c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f78c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="f78c7-120">Especifica o grupo de recursos para o qual este cmdlet exclui uma variável.</span><span class="sxs-lookup"><span data-stu-id="f78c7-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="f78c7-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f78c7-121">-Confirm</span></span>
<span data-ttu-id="f78c7-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f78c7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f78c7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f78c7-123">-WhatIf</span></span>
<span data-ttu-id="f78c7-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f78c7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f78c7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f78c7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f78c7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78c7-126">CommonParameters</span></span>
<span data-ttu-id="f78c7-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78c7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78c7-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f78c7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78c7-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="f78c7-129">INPUTS</span></span>

### <span data-ttu-id="f78c7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f78c7-130">System.String</span></span>

## <span data-ttu-id="f78c7-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="f78c7-131">OUTPUTS</span></span>

### <span data-ttu-id="f78c7-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="f78c7-132">System.Void</span></span>

## <span data-ttu-id="f78c7-133">Notas</span><span class="sxs-lookup"><span data-stu-id="f78c7-133">NOTES</span></span>

## <span data-ttu-id="f78c7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f78c7-134">RELATED LINKS</span></span>

[<span data-ttu-id="f78c7-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f78c7-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="f78c7-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f78c7-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="f78c7-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f78c7-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


