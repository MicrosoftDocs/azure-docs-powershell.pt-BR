---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115792"
---
# <span data-ttu-id="10fd0-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="10fd0-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="10fd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="10fd0-103">Criar Objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="10fd0-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="10fd0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10fd0-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10fd0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="10fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="10fd0-106">Criar Objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="10fd0-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="10fd0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10fd0-107">EXAMPLES</span></span>

### <span data-ttu-id="10fd0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10fd0-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="10fd0-109">Criar um Objeto RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="10fd0-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="10fd0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10fd0-110">PARAMETERS</span></span>

### <span data-ttu-id="10fd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10fd0-111">-DefaultProfile</span></span>
<span data-ttu-id="10fd0-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10fd0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10fd0-113">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="10fd0-113">-Exclusion</span></span>
<span data-ttu-id="10fd0-114">Exclusão</span><span class="sxs-lookup"><span data-stu-id="10fd0-114">Exclusion</span></span>

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

### <span data-ttu-id="10fd0-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="10fd0-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="10fd0-116">Lista de substituição de regras</span><span class="sxs-lookup"><span data-stu-id="10fd0-116">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10fd0-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="10fd0-117">-RuleGroupName</span></span>
<span data-ttu-id="10fd0-118">Nome do Grupo de Regras para o qual essas substituições se aplicam</span><span class="sxs-lookup"><span data-stu-id="10fd0-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="10fd0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10fd0-119">CommonParameters</span></span>
<span data-ttu-id="10fd0-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10fd0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10fd0-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10fd0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10fd0-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="10fd0-122">INPUTS</span></span>

### <span data-ttu-id="10fd0-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="10fd0-123">None</span></span>

## <span data-ttu-id="10fd0-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="10fd0-124">OUTPUTS</span></span>

### <span data-ttu-id="10fd0-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="10fd0-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="10fd0-126">Notas</span><span class="sxs-lookup"><span data-stu-id="10fd0-126">NOTES</span></span>

## <span data-ttu-id="10fd0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10fd0-127">RELATED LINKS</span></span>

[<span data-ttu-id="10fd0-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="10fd0-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
