---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944926"
---
# <span data-ttu-id="bba35-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="bba35-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="bba35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bba35-102">SYNOPSIS</span></span>
<span data-ttu-id="bba35-103">Remove o grupo do Hybrid Worker da automação.</span><span class="sxs-lookup"><span data-stu-id="bba35-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="bba35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bba35-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bba35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bba35-105">DESCRIPTION</span></span>
<span data-ttu-id="bba35-106">O cmdlet Remove-AzAutomationHybridWorkerGroup remove um grupo do Hybrid Worker da automação.</span><span class="sxs-lookup"><span data-stu-id="bba35-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="bba35-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bba35-107">EXAMPLES</span></span>

### <span data-ttu-id="bba35-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bba35-108">Example 1</span></span>
<span data-ttu-id="bba35-109">Esse comando Remove um trabalhador híbrido por nome.</span><span class="sxs-lookup"><span data-stu-id="bba35-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="bba35-110">OS</span><span class="sxs-lookup"><span data-stu-id="bba35-110">PARAMETERS</span></span>

### <span data-ttu-id="bba35-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bba35-111">-AutomationAccountName</span></span>
<span data-ttu-id="bba35-112">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="bba35-112">The automation account name.</span></span>

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

### <span data-ttu-id="bba35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba35-113">-DefaultProfile</span></span>
<span data-ttu-id="bba35-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bba35-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bba35-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bba35-115">-Name</span></span>
<span data-ttu-id="bba35-116">O nome do grupo do Hybrid Worker.</span><span class="sxs-lookup"><span data-stu-id="bba35-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="bba35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba35-117">-ResourceGroupName</span></span>
<span data-ttu-id="bba35-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bba35-118">The resource group name.</span></span>

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

### <span data-ttu-id="bba35-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bba35-119">-Confirm</span></span>
<span data-ttu-id="bba35-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bba35-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bba35-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba35-121">-WhatIf</span></span>
<span data-ttu-id="bba35-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bba35-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba35-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bba35-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bba35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba35-124">CommonParameters</span></span>
<span data-ttu-id="bba35-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba35-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba35-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba35-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bba35-127">INPUTS</span></span>

### <span data-ttu-id="bba35-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bba35-128">System.String</span></span>

## <span data-ttu-id="bba35-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bba35-129">OUTPUTS</span></span>

### <span data-ttu-id="bba35-130">System. void</span><span class="sxs-lookup"><span data-stu-id="bba35-130">System.Void</span></span>

## <span data-ttu-id="bba35-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bba35-131">NOTES</span></span>

## <span data-ttu-id="bba35-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bba35-132">RELATED LINKS</span></span>
