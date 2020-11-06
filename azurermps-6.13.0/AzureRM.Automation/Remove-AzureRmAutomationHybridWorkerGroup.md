---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
ms.openlocfilehash: b6f15bc55c2e9f9a05e60e7e6f2c139ddbb70454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602324"
---
# <span data-ttu-id="ed6bc-101">Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="ed6bc-101">Remove-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="ed6bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6bc-103">Remove o grupo do Hybrid Worker da automação.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-103">Removes hybrid worker group from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed6bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed6bc-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed6bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed6bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ed6bc-106">O cmdlet Remove-AzureRmAutomationHybridWorkerGroup remove um grupo do Hybrid Worker da automação.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-106">The Remove-AzureRmAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="ed6bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed6bc-107">EXAMPLES</span></span>

### <span data-ttu-id="ed6bc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed6bc-108">Example 1</span></span>
<span data-ttu-id="ed6bc-109">Esse comando Remove um trabalhador híbrido por nome.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="ed6bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="ed6bc-110">PARAMETERS</span></span>

### <span data-ttu-id="ed6bc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed6bc-111">-AutomationAccountName</span></span>
<span data-ttu-id="ed6bc-112">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-112">The automation account name.</span></span>

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

### <span data-ttu-id="ed6bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6bc-113">-DefaultProfile</span></span>
<span data-ttu-id="ed6bc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6bc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed6bc-115">-Name</span></span>
<span data-ttu-id="ed6bc-116">O nome do grupo do Hybrid Worker.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="ed6bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed6bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="ed6bc-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-118">The resource group name.</span></span>

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

### <span data-ttu-id="ed6bc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ed6bc-119">-Confirm</span></span>
<span data-ttu-id="ed6bc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed6bc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed6bc-121">-WhatIf</span></span>
<span data-ttu-id="ed6bc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed6bc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed6bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6bc-124">CommonParameters</span></span>
<span data-ttu-id="ed6bc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed6bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6bc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed6bc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6bc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed6bc-127">INPUTS</span></span>

### <span data-ttu-id="ed6bc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ed6bc-128">System.String</span></span>

## <span data-ttu-id="ed6bc-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed6bc-129">OUTPUTS</span></span>

### <span data-ttu-id="ed6bc-130">System. void</span><span class="sxs-lookup"><span data-stu-id="ed6bc-130">System.Void</span></span>

## <span data-ttu-id="ed6bc-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed6bc-131">NOTES</span></span>

## <span data-ttu-id="ed6bc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed6bc-132">RELATED LINKS</span></span>
