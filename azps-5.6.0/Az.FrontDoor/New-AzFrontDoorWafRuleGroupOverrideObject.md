---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 5d8e872ea2ca47169c727a29c1847a83b5a6542b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901486"
---
# <span data-ttu-id="de8f4-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="de8f4-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="de8f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="de8f4-103">Criar objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="de8f4-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="de8f4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="de8f4-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de8f4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="de8f4-105">DESCRIPTION</span></span>
<span data-ttu-id="de8f4-106">Criar objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="de8f4-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="de8f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de8f4-107">EXAMPLES</span></span>

### <span data-ttu-id="de8f4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de8f4-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="de8f4-109">Criar um objeto RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="de8f4-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="de8f4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="de8f4-110">PARAMETERS</span></span>

### <span data-ttu-id="de8f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8f4-111">-DefaultProfile</span></span>
<span data-ttu-id="de8f4-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de8f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de8f4-113">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="de8f4-113">-Exclusion</span></span>
<span data-ttu-id="de8f4-114">Exclusão</span><span class="sxs-lookup"><span data-stu-id="de8f4-114">Exclusion</span></span>

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

### <span data-ttu-id="de8f4-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="de8f4-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="de8f4-116">Lista de substituição de regras</span><span class="sxs-lookup"><span data-stu-id="de8f4-116">Rule override list</span></span>

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

### <span data-ttu-id="de8f4-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="de8f4-117">-RuleGroupName</span></span>
<span data-ttu-id="de8f4-118">Nome do Grupo de Regras para o qual essas substituições se aplicam</span><span class="sxs-lookup"><span data-stu-id="de8f4-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="de8f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8f4-119">CommonParameters</span></span>
<span data-ttu-id="de8f4-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8f4-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de8f4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8f4-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de8f4-122">INPUTS</span></span>

### <span data-ttu-id="de8f4-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="de8f4-123">None</span></span>

## <span data-ttu-id="de8f4-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="de8f4-124">OUTPUTS</span></span>

### <span data-ttu-id="de8f4-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="de8f4-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="de8f4-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="de8f4-126">NOTES</span></span>

## <span data-ttu-id="de8f4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de8f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="de8f4-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="de8f4-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
