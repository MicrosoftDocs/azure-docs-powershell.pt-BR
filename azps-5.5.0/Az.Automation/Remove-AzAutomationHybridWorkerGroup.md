---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118006"
---
# <span data-ttu-id="bba96-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="bba96-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="bba96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bba96-102">SYNOPSIS</span></span>
<span data-ttu-id="bba96-103">Remove o grupo de trabalhadores híbridos da Automação.</span><span class="sxs-lookup"><span data-stu-id="bba96-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="bba96-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bba96-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bba96-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bba96-105">DESCRIPTION</span></span>
<span data-ttu-id="bba96-106">O Remove-AzAutomationHybridWorkerGroup cmdlet remove um grupo de trabalhadores híbridos da Automação.</span><span class="sxs-lookup"><span data-stu-id="bba96-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="bba96-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bba96-107">EXAMPLES</span></span>

### <span data-ttu-id="bba96-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bba96-108">Example 1</span></span>
<span data-ttu-id="bba96-109">Esse comando remove um trabalhador híbrido por nome.</span><span class="sxs-lookup"><span data-stu-id="bba96-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="bba96-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bba96-110">PARAMETERS</span></span>

### <span data-ttu-id="bba96-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bba96-111">-AutomationAccountName</span></span>
<span data-ttu-id="bba96-112">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="bba96-112">The automation account name.</span></span>

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

### <span data-ttu-id="bba96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba96-113">-DefaultProfile</span></span>
<span data-ttu-id="bba96-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bba96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bba96-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bba96-115">-Name</span></span>
<span data-ttu-id="bba96-116">O nome do grupo de trabalhadores híbridos.</span><span class="sxs-lookup"><span data-stu-id="bba96-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="bba96-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba96-117">-ResourceGroupName</span></span>
<span data-ttu-id="bba96-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bba96-118">The resource group name.</span></span>

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

### <span data-ttu-id="bba96-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bba96-119">-Confirm</span></span>
<span data-ttu-id="bba96-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bba96-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bba96-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba96-121">-WhatIf</span></span>
<span data-ttu-id="bba96-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bba96-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba96-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bba96-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bba96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba96-124">CommonParameters</span></span>
<span data-ttu-id="bba96-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba96-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba96-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba96-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="bba96-127">INPUTS</span></span>

### <span data-ttu-id="bba96-128">System.String</span><span class="sxs-lookup"><span data-stu-id="bba96-128">System.String</span></span>

## <span data-ttu-id="bba96-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="bba96-129">OUTPUTS</span></span>

### <span data-ttu-id="bba96-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="bba96-130">System.Void</span></span>

## <span data-ttu-id="bba96-131">Notas</span><span class="sxs-lookup"><span data-stu-id="bba96-131">NOTES</span></span>

## <span data-ttu-id="bba96-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bba96-132">RELATED LINKS</span></span>
