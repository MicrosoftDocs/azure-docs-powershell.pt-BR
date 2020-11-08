---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115446"
---
# <span data-ttu-id="f665d-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="f665d-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="f665d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f665d-102">SYNOPSIS</span></span>
<span data-ttu-id="f665d-103">Criar objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="f665d-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="f665d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f665d-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f665d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f665d-105">DESCRIPTION</span></span>
<span data-ttu-id="f665d-106">Criar objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="f665d-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="f665d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f665d-107">EXAMPLES</span></span>

### <span data-ttu-id="f665d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f665d-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="f665d-109">Criar um objeto RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f665d-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="f665d-110">OS</span><span class="sxs-lookup"><span data-stu-id="f665d-110">PARAMETERS</span></span>

### <span data-ttu-id="f665d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f665d-111">-DefaultProfile</span></span>
<span data-ttu-id="f665d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f665d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f665d-113">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="f665d-113">-Exclusion</span></span>
<span data-ttu-id="f665d-114">Excluídos</span><span class="sxs-lookup"><span data-stu-id="f665d-114">Exclusion</span></span>

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

### <span data-ttu-id="f665d-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f665d-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="f665d-116">Lista substituir regra</span><span class="sxs-lookup"><span data-stu-id="f665d-116">Rule override list</span></span>

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

### <span data-ttu-id="f665d-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="f665d-117">-RuleGroupName</span></span>
<span data-ttu-id="f665d-118">Nome do grupo de regras para o qual essas substituições se aplicam</span><span class="sxs-lookup"><span data-stu-id="f665d-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="f665d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f665d-119">CommonParameters</span></span>
<span data-ttu-id="f665d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f665d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f665d-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f665d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f665d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f665d-122">INPUTS</span></span>

### <span data-ttu-id="f665d-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f665d-123">None</span></span>

## <span data-ttu-id="f665d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f665d-124">OUTPUTS</span></span>

### <span data-ttu-id="f665d-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f665d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="f665d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f665d-126">NOTES</span></span>

## <span data-ttu-id="f665d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f665d-127">RELATED LINKS</span></span>

[<span data-ttu-id="f665d-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f665d-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
