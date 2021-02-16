---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117650"
---
# <span data-ttu-id="a0306-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="a0306-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="a0306-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0306-102">SYNOPSIS</span></span>
<span data-ttu-id="a0306-103">Criar objeto de substituição de regra gerenciado</span><span class="sxs-lookup"><span data-stu-id="a0306-103">Create managed rule override object</span></span>

## <span data-ttu-id="a0306-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0306-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0306-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0306-105">DESCRIPTION</span></span>
<span data-ttu-id="a0306-106">Crie o Objeto PSAzureManagedRuleOverride para a criação de objeto de substituição de grupo de regras WAF gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a0306-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="a0306-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a0306-107">EXAMPLES</span></span>

### <span data-ttu-id="a0306-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0306-108">Example 1</span></span>
<span data-ttu-id="a0306-109">Criar um objeto de substituição de regra gerenciado para a regra 942250 (que está no grupo SQLI).</span><span class="sxs-lookup"><span data-stu-id="a0306-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="a0306-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0306-110">PARAMETERS</span></span>

### <span data-ttu-id="a0306-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="a0306-111">-Action</span></span>
<span data-ttu-id="a0306-112">Substituir Ação</span><span class="sxs-lookup"><span data-stu-id="a0306-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0306-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0306-113">-DefaultProfile</span></span>
<span data-ttu-id="a0306-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0306-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0306-115">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="a0306-115">-Disabled</span></span>
<span data-ttu-id="a0306-116">Estado desabilitado</span><span class="sxs-lookup"><span data-stu-id="a0306-116">Disabled state</span></span>

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

### <span data-ttu-id="a0306-117">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="a0306-117">-Exclusion</span></span>
<span data-ttu-id="a0306-118">Exclusão</span><span class="sxs-lookup"><span data-stu-id="a0306-118">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0306-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="a0306-119">-RuleId</span></span>
<span data-ttu-id="a0306-120">ID da Regra</span><span class="sxs-lookup"><span data-stu-id="a0306-120">Rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0306-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0306-121">CommonParameters</span></span>
<span data-ttu-id="a0306-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0306-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0306-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0306-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0306-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="a0306-124">INPUTS</span></span>

### <span data-ttu-id="a0306-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a0306-125">None</span></span>

## <span data-ttu-id="a0306-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="a0306-126">OUTPUTS</span></span>

### <span data-ttu-id="a0306-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a0306-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="a0306-128">Notas</span><span class="sxs-lookup"><span data-stu-id="a0306-128">NOTES</span></span>

## <span data-ttu-id="a0306-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0306-129">RELATED LINKS</span></span>

[<span data-ttu-id="a0306-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="a0306-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)