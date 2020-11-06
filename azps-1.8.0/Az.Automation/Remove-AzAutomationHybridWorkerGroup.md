---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: b9f23105b6fa84781ef1b0f0ba4be0e52e06ee08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601530"
---
# <span data-ttu-id="98f85-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="98f85-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="98f85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98f85-102">SYNOPSIS</span></span>
<span data-ttu-id="98f85-103">Remove o grupo do Hybrid Worker da automação.</span><span class="sxs-lookup"><span data-stu-id="98f85-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="98f85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98f85-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98f85-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98f85-105">DESCRIPTION</span></span>
<span data-ttu-id="98f85-106">O cmdlet Remove-AzAutomationHybridWorkerGroup remove um grupo do Hybrid Worker da automação.</span><span class="sxs-lookup"><span data-stu-id="98f85-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="98f85-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98f85-107">EXAMPLES</span></span>

### <span data-ttu-id="98f85-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98f85-108">Example 1</span></span>
<span data-ttu-id="98f85-109">Esse comando Remove um trabalhador híbrido por nome.</span><span class="sxs-lookup"><span data-stu-id="98f85-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="98f85-110">OS</span><span class="sxs-lookup"><span data-stu-id="98f85-110">PARAMETERS</span></span>

### <span data-ttu-id="98f85-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="98f85-111">-AutomationAccountName</span></span>
<span data-ttu-id="98f85-112">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="98f85-112">The automation account name.</span></span>

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

### <span data-ttu-id="98f85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f85-113">-DefaultProfile</span></span>
<span data-ttu-id="98f85-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98f85-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f85-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="98f85-115">-Name</span></span>
<span data-ttu-id="98f85-116">O nome do grupo do Hybrid Worker.</span><span class="sxs-lookup"><span data-stu-id="98f85-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="98f85-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f85-117">-ResourceGroupName</span></span>
<span data-ttu-id="98f85-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="98f85-118">The resource group name.</span></span>

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

### <span data-ttu-id="98f85-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98f85-119">-Confirm</span></span>
<span data-ttu-id="98f85-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98f85-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f85-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f85-121">-WhatIf</span></span>
<span data-ttu-id="98f85-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98f85-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f85-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98f85-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f85-124">CommonParameters</span></span>
<span data-ttu-id="98f85-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f85-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f85-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98f85-127">INPUTS</span></span>

### <span data-ttu-id="98f85-128">System. String</span><span class="sxs-lookup"><span data-stu-id="98f85-128">System.String</span></span>

## <span data-ttu-id="98f85-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98f85-129">OUTPUTS</span></span>

### <span data-ttu-id="98f85-130">System. void</span><span class="sxs-lookup"><span data-stu-id="98f85-130">System.Void</span></span>

## <span data-ttu-id="98f85-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98f85-131">NOTES</span></span>

## <span data-ttu-id="98f85-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98f85-132">RELATED LINKS</span></span>
