---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944940"
---
# <span data-ttu-id="27bd5-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="27bd5-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="27bd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="27bd5-103">Remove uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="27bd5-103">Removes an Automation account.</span></span>

## <span data-ttu-id="27bd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27bd5-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27bd5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="27bd5-106">O cmdlet **Remove-AzAutomationAccount** remove uma conta de automação do Azure de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27bd5-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="27bd5-107">Para obter mais informações sobre contas de automação, consulte o cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="27bd5-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="27bd5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27bd5-108">EXAMPLES</span></span>

### <span data-ttu-id="27bd5-109">Exemplo 1: remover uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="27bd5-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="27bd5-110">Esse comando Remove uma conta de automação chamada ContosoAutomationAccount sem solicitar a validação do usuário.</span><span class="sxs-lookup"><span data-stu-id="27bd5-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="27bd5-111">OS</span><span class="sxs-lookup"><span data-stu-id="27bd5-111">PARAMETERS</span></span>

### <span data-ttu-id="27bd5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27bd5-112">-DefaultProfile</span></span>
<span data-ttu-id="27bd5-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="27bd5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27bd5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="27bd5-114">-Force</span></span>
<span data-ttu-id="27bd5-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="27bd5-115">ps_force</span></span>

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

### <span data-ttu-id="27bd5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="27bd5-116">-Name</span></span>
<span data-ttu-id="27bd5-117">Especifica o nome da conta de automação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="27bd5-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="27bd5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27bd5-118">-ResourceGroupName</span></span>
<span data-ttu-id="27bd5-119">Especifica o nome do grupo de recursos do qual esse cmdlet Remove uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="27bd5-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="27bd5-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27bd5-120">-Confirm</span></span>
<span data-ttu-id="27bd5-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27bd5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27bd5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27bd5-122">-WhatIf</span></span>
<span data-ttu-id="27bd5-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27bd5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27bd5-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27bd5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27bd5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27bd5-125">CommonParameters</span></span>
<span data-ttu-id="27bd5-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27bd5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27bd5-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27bd5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27bd5-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27bd5-128">INPUTS</span></span>

### <span data-ttu-id="27bd5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="27bd5-129">System.String</span></span>

## <span data-ttu-id="27bd5-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27bd5-130">OUTPUTS</span></span>

### <span data-ttu-id="27bd5-131">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="27bd5-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="27bd5-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27bd5-132">NOTES</span></span>

## <span data-ttu-id="27bd5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27bd5-133">RELATED LINKS</span></span>

[<span data-ttu-id="27bd5-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="27bd5-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="27bd5-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="27bd5-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="27bd5-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="27bd5-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


