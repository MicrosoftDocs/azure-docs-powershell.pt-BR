---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 3fb795f614e6ccd7c4e97470d89c6c8923fa9165
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892895"
---
# <span data-ttu-id="194c5-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="194c5-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="194c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="194c5-102">SYNOPSIS</span></span>
<span data-ttu-id="194c5-103">Remove uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="194c5-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="194c5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="194c5-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="194c5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="194c5-105">DESCRIPTION</span></span>
<span data-ttu-id="194c5-106">O cmdlet **Remove-AzAutomationCredential** remove uma credencial da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="194c5-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="194c5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="194c5-107">EXAMPLES</span></span>

### <span data-ttu-id="194c5-108">Exemplo 1: Remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="194c5-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="194c5-109">Este comando remove uma credencial chamada ContosoCredential na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="194c5-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="194c5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="194c5-110">PARAMETERS</span></span>

### <span data-ttu-id="194c5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="194c5-111">-AutomationAccountName</span></span>
<span data-ttu-id="194c5-112">Especifica o nome da conta automação da qual este cmdlet remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="194c5-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="194c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="194c5-113">-DefaultProfile</span></span>
<span data-ttu-id="194c5-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="194c5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="194c5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="194c5-115">-Name</span></span>
<span data-ttu-id="194c5-116">Especifica o nome da credencial que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="194c5-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="194c5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="194c5-117">-ResourceGroupName</span></span>
<span data-ttu-id="194c5-118">Especifica o nome do grupo de recursos para o qual este cmdlet remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="194c5-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="194c5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="194c5-119">-Confirm</span></span>
<span data-ttu-id="194c5-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="194c5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="194c5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="194c5-121">-WhatIf</span></span>
<span data-ttu-id="194c5-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="194c5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="194c5-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="194c5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="194c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="194c5-124">CommonParameters</span></span>
<span data-ttu-id="194c5-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="194c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="194c5-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="194c5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="194c5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="194c5-127">INPUTS</span></span>

### <span data-ttu-id="194c5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="194c5-128">System.String</span></span>

## <span data-ttu-id="194c5-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="194c5-129">OUTPUTS</span></span>

### <span data-ttu-id="194c5-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="194c5-130">System.Void</span></span>

## <span data-ttu-id="194c5-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="194c5-131">NOTES</span></span>

## <span data-ttu-id="194c5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="194c5-132">RELATED LINKS</span></span>

[<span data-ttu-id="194c5-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="194c5-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="194c5-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="194c5-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="194c5-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="194c5-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


