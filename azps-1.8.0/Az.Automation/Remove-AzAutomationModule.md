---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 798e5f37fdeb53030d43f132eae59c94ea855fc1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601529"
---
# <span data-ttu-id="71793-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="71793-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="71793-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71793-102">SYNOPSIS</span></span>
<span data-ttu-id="71793-103">Remove um módulo da automação.</span><span class="sxs-lookup"><span data-stu-id="71793-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="71793-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71793-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71793-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71793-105">DESCRIPTION</span></span>
<span data-ttu-id="71793-106">O cmdlet **Remove-AzAutomationModule** remove um módulo de uma conta de automação na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="71793-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="71793-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71793-107">EXAMPLES</span></span>

### <span data-ttu-id="71793-108">Exemplo 1: remover um módulo</span><span class="sxs-lookup"><span data-stu-id="71793-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="71793-109">Esse comando Remove um módulo chamado ContosoModule da conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="71793-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="71793-110">OS</span><span class="sxs-lookup"><span data-stu-id="71793-110">PARAMETERS</span></span>

### <span data-ttu-id="71793-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="71793-111">-AutomationAccountName</span></span>
<span data-ttu-id="71793-112">Especifica o nome da conta de automação a partir da qual esse cmdlet Remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="71793-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="71793-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71793-113">-DefaultProfile</span></span>
<span data-ttu-id="71793-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="71793-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71793-115">-Force</span><span class="sxs-lookup"><span data-stu-id="71793-115">-Force</span></span>
<span data-ttu-id="71793-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="71793-116">ps_force</span></span>

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

### <span data-ttu-id="71793-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="71793-117">-Name</span></span>
<span data-ttu-id="71793-118">Especifica o nome do módulo que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="71793-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71793-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71793-119">-ResourceGroupName</span></span>
<span data-ttu-id="71793-120">Especifica o nome de um grupo de recursos em que esse cmdlet Remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="71793-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="71793-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71793-121">-Confirm</span></span>
<span data-ttu-id="71793-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71793-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71793-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71793-123">-WhatIf</span></span>
<span data-ttu-id="71793-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71793-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71793-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71793-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71793-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71793-126">CommonParameters</span></span>
<span data-ttu-id="71793-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71793-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71793-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71793-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71793-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71793-129">INPUTS</span></span>

### <span data-ttu-id="71793-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71793-130">System.String</span></span>

## <span data-ttu-id="71793-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71793-131">OUTPUTS</span></span>

### <span data-ttu-id="71793-132">System. void</span><span class="sxs-lookup"><span data-stu-id="71793-132">System.Void</span></span>

## <span data-ttu-id="71793-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71793-133">NOTES</span></span>

## <span data-ttu-id="71793-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71793-134">RELATED LINKS</span></span>

[<span data-ttu-id="71793-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="71793-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="71793-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="71793-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="71793-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="71793-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


