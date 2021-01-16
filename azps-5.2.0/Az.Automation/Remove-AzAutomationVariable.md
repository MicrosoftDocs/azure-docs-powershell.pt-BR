---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264508"
---
# <span data-ttu-id="3e6de-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3e6de-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="3e6de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e6de-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6de-103">Remove uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="3e6de-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="3e6de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e6de-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e6de-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e6de-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6de-106">O cmdlet **Remove-AzAutomationVariable** remove uma variável da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e6de-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="3e6de-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e6de-107">EXAMPLES</span></span>

### <span data-ttu-id="3e6de-108">Exemplo 1: remover uma variável</span><span class="sxs-lookup"><span data-stu-id="3e6de-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3e6de-109">Esse comando Remove uma variável chamada StringVariable22 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3e6de-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="3e6de-110">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="3e6de-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3e6de-111">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="3e6de-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3e6de-112">OS</span><span class="sxs-lookup"><span data-stu-id="3e6de-112">PARAMETERS</span></span>

### <span data-ttu-id="3e6de-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3e6de-113">-AutomationAccountName</span></span>
<span data-ttu-id="3e6de-114">Especifica o nome da conta de automação que contém a variável que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="3e6de-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="3e6de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6de-115">-DefaultProfile</span></span>
<span data-ttu-id="3e6de-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3e6de-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e6de-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e6de-117">-Name</span></span>
<span data-ttu-id="3e6de-118">Especifica o nome da variável que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="3e6de-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="3e6de-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e6de-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e6de-120">Especifica o grupo de recursos para o qual esse cmdlet exclui uma variável.</span><span class="sxs-lookup"><span data-stu-id="3e6de-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="3e6de-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e6de-121">-Confirm</span></span>
<span data-ttu-id="3e6de-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e6de-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e6de-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e6de-123">-WhatIf</span></span>
<span data-ttu-id="3e6de-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e6de-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e6de-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e6de-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e6de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6de-126">CommonParameters</span></span>
<span data-ttu-id="3e6de-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6de-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e6de-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6de-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e6de-129">INPUTS</span></span>

### <span data-ttu-id="3e6de-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3e6de-130">System.String</span></span>

## <span data-ttu-id="3e6de-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e6de-131">OUTPUTS</span></span>

### <span data-ttu-id="3e6de-132">System. void</span><span class="sxs-lookup"><span data-stu-id="3e6de-132">System.Void</span></span>

## <span data-ttu-id="3e6de-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e6de-133">NOTES</span></span>

## <span data-ttu-id="3e6de-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e6de-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e6de-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3e6de-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="3e6de-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3e6de-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="3e6de-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3e6de-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


