---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 35ef4a5629726b33a8d9099da78134e6a0bac8b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892894"
---
# <span data-ttu-id="efcfd-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="efcfd-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="efcfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efcfd-102">SYNOPSIS</span></span>
<span data-ttu-id="efcfd-103">Remove o grupo de trabalho híbrido da Automação.</span><span class="sxs-lookup"><span data-stu-id="efcfd-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="efcfd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="efcfd-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efcfd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="efcfd-105">DESCRIPTION</span></span>
<span data-ttu-id="efcfd-106">O Remove-AzAutomationHybridWorkerGroup cmdlet remove um grupo de trabalho híbrido da Automação.</span><span class="sxs-lookup"><span data-stu-id="efcfd-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="efcfd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efcfd-107">EXAMPLES</span></span>

### <span data-ttu-id="efcfd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="efcfd-108">Example 1</span></span>
<span data-ttu-id="efcfd-109">Este comando remove um trabalhador híbrido pelo nome.</span><span class="sxs-lookup"><span data-stu-id="efcfd-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="efcfd-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="efcfd-110">PARAMETERS</span></span>

### <span data-ttu-id="efcfd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="efcfd-111">-AutomationAccountName</span></span>
<span data-ttu-id="efcfd-112">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="efcfd-112">The automation account name.</span></span>

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

### <span data-ttu-id="efcfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efcfd-113">-DefaultProfile</span></span>
<span data-ttu-id="efcfd-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="efcfd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efcfd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="efcfd-115">-Name</span></span>
<span data-ttu-id="efcfd-116">O nome do grupo de trabalho híbrido.</span><span class="sxs-lookup"><span data-stu-id="efcfd-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efcfd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efcfd-117">-ResourceGroupName</span></span>
<span data-ttu-id="efcfd-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="efcfd-118">The resource group name.</span></span>

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

### <span data-ttu-id="efcfd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efcfd-119">-Confirm</span></span>
<span data-ttu-id="efcfd-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efcfd-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efcfd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efcfd-121">-WhatIf</span></span>
<span data-ttu-id="efcfd-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="efcfd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efcfd-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="efcfd-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efcfd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efcfd-124">CommonParameters</span></span>
<span data-ttu-id="efcfd-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efcfd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efcfd-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efcfd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efcfd-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efcfd-127">INPUTS</span></span>

### <span data-ttu-id="efcfd-128">System.String</span><span class="sxs-lookup"><span data-stu-id="efcfd-128">System.String</span></span>

## <span data-ttu-id="efcfd-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="efcfd-129">OUTPUTS</span></span>

### <span data-ttu-id="efcfd-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="efcfd-130">System.Void</span></span>

## <span data-ttu-id="efcfd-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="efcfd-131">NOTES</span></span>

## <span data-ttu-id="efcfd-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efcfd-132">RELATED LINKS</span></span>
