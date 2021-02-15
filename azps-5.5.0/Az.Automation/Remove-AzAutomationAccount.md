---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118019"
---
# <span data-ttu-id="0ff0c-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0ff0c-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="0ff0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ff0c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff0c-103">Remove uma conta de Automação.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-103">Removes an Automation account.</span></span>

## <span data-ttu-id="0ff0c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ff0c-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff0c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ff0c-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff0c-106">O **cmdlet Remove-AzAutomationAccount** remove uma conta de Automação do Azure de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="0ff0c-107">Para obter mais informações sobre contas de automação, consulte New-AzAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="0ff0c-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ff0c-108">EXAMPLES</span></span>

### <span data-ttu-id="0ff0c-109">Exemplo 1: Remover uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="0ff0c-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0ff0c-110">Esse comando remove uma conta de automação chamada ContosoAutomationAccount sem solicitar a validação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="0ff0c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ff0c-111">PARAMETERS</span></span>

### <span data-ttu-id="0ff0c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff0c-112">-DefaultProfile</span></span>
<span data-ttu-id="0ff0c-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0ff0c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ff0c-114">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0ff0c-114">-Force</span></span>
<span data-ttu-id="0ff0c-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="0ff0c-115">ps_force</span></span>

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

### <span data-ttu-id="0ff0c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ff0c-116">-Name</span></span>
<span data-ttu-id="0ff0c-117">Especifica o nome da conta automação que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff0c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff0c-118">-ResourceGroupName</span></span>
<span data-ttu-id="0ff0c-119">Especifica o nome do grupo de recursos do qual este cmdlet remove uma conta de Automação.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="0ff0c-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0ff0c-120">-Confirm</span></span>
<span data-ttu-id="0ff0c-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff0c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff0c-122">-WhatIf</span></span>
<span data-ttu-id="0ff0c-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ff0c-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff0c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff0c-125">CommonParameters</span></span>
<span data-ttu-id="0ff0c-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff0c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff0c-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff0c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff0c-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="0ff0c-128">INPUTS</span></span>

### <span data-ttu-id="0ff0c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="0ff0c-129">System.String</span></span>

## <span data-ttu-id="0ff0c-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="0ff0c-130">OUTPUTS</span></span>

### <span data-ttu-id="0ff0c-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0ff0c-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="0ff0c-132">Notas</span><span class="sxs-lookup"><span data-stu-id="0ff0c-132">NOTES</span></span>

## <span data-ttu-id="0ff0c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ff0c-133">RELATED LINKS</span></span>

[<span data-ttu-id="0ff0c-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0ff0c-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="0ff0c-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0ff0c-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="0ff0c-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="0ff0c-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


