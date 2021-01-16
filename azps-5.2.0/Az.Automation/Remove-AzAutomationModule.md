---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264518"
---
# <span data-ttu-id="4cfb3-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4cfb3-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="4cfb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cfb3-102">SYNOPSIS</span></span>
<span data-ttu-id="4cfb3-103">Remove um módulo da automação.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="4cfb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cfb3-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4cfb3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cfb3-105">DESCRIPTION</span></span>
<span data-ttu-id="4cfb3-106">O cmdlet **Remove-AzAutomationModule** remove um módulo de uma conta de automação na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="4cfb3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cfb3-107">EXAMPLES</span></span>

### <span data-ttu-id="4cfb3-108">Exemplo 1: remover um módulo</span><span class="sxs-lookup"><span data-stu-id="4cfb3-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4cfb3-109">Esse comando Remove um módulo chamado ContosoModule da conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4cfb3-110">OS</span><span class="sxs-lookup"><span data-stu-id="4cfb3-110">PARAMETERS</span></span>

### <span data-ttu-id="4cfb3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4cfb3-111">-AutomationAccountName</span></span>
<span data-ttu-id="4cfb3-112">Especifica o nome da conta de automação a partir da qual esse cmdlet Remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="4cfb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cfb3-113">-DefaultProfile</span></span>
<span data-ttu-id="4cfb3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4cfb3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cfb3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4cfb3-115">-Force</span></span>
<span data-ttu-id="4cfb3-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="4cfb3-116">ps_force</span></span>

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

### <span data-ttu-id="4cfb3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cfb3-117">-Name</span></span>
<span data-ttu-id="4cfb3-118">Especifica o nome do módulo que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4cfb3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cfb3-119">-ResourceGroupName</span></span>
<span data-ttu-id="4cfb3-120">Especifica o nome de um grupo de recursos em que esse cmdlet Remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="4cfb3-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4cfb3-121">-Confirm</span></span>
<span data-ttu-id="4cfb3-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cfb3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cfb3-123">-WhatIf</span></span>
<span data-ttu-id="4cfb3-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cfb3-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cfb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cfb3-126">CommonParameters</span></span>
<span data-ttu-id="4cfb3-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cfb3-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cfb3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cfb3-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cfb3-129">INPUTS</span></span>

### <span data-ttu-id="4cfb3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4cfb3-130">System.String</span></span>

## <span data-ttu-id="4cfb3-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cfb3-131">OUTPUTS</span></span>

### <span data-ttu-id="4cfb3-132">System. void</span><span class="sxs-lookup"><span data-stu-id="4cfb3-132">System.Void</span></span>

## <span data-ttu-id="4cfb3-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cfb3-133">NOTES</span></span>

## <span data-ttu-id="4cfb3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cfb3-134">RELATED LINKS</span></span>

[<span data-ttu-id="4cfb3-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4cfb3-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="4cfb3-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4cfb3-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="4cfb3-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4cfb3-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


