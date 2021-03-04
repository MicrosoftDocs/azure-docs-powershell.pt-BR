---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: ee4193fff69e8b46362ac75019cc76178001c2e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887742"
---
# <span data-ttu-id="278ea-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="278ea-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="278ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="278ea-102">SYNOPSIS</span></span>
<span data-ttu-id="278ea-103">Criar objeto de substituição de regra gerenciada</span><span class="sxs-lookup"><span data-stu-id="278ea-103">Create managed rule override object</span></span>

## <span data-ttu-id="278ea-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="278ea-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="278ea-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="278ea-105">DESCRIPTION</span></span>
<span data-ttu-id="278ea-106">Crie Objeto PSAzureManagedRuleOverride para a criação de objeto de substituição de grupo de regras WAF gerenciado.</span><span class="sxs-lookup"><span data-stu-id="278ea-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="278ea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="278ea-107">EXAMPLES</span></span>

### <span data-ttu-id="278ea-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="278ea-108">Example 1</span></span>
<span data-ttu-id="278ea-109">Crie um objeto de substituição de regra gerenciada para a regra 942250 (que está no grupo SQLI).</span><span class="sxs-lookup"><span data-stu-id="278ea-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="278ea-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="278ea-110">PARAMETERS</span></span>

### <span data-ttu-id="278ea-111">-Action</span><span class="sxs-lookup"><span data-stu-id="278ea-111">-Action</span></span>
<span data-ttu-id="278ea-112">Ação Substituir</span><span class="sxs-lookup"><span data-stu-id="278ea-112">Override Action</span></span>

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

### <span data-ttu-id="278ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278ea-113">-DefaultProfile</span></span>
<span data-ttu-id="278ea-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="278ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="278ea-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="278ea-115">-Disabled</span></span>
<span data-ttu-id="278ea-116">Estado desabilitado</span><span class="sxs-lookup"><span data-stu-id="278ea-116">Disabled state</span></span>

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

### <span data-ttu-id="278ea-117">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="278ea-117">-Exclusion</span></span>
<span data-ttu-id="278ea-118">Exclusão</span><span class="sxs-lookup"><span data-stu-id="278ea-118">Exclusion</span></span>

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

### <span data-ttu-id="278ea-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="278ea-119">-RuleId</span></span>
<span data-ttu-id="278ea-120">ID da regra</span><span class="sxs-lookup"><span data-stu-id="278ea-120">Rule ID</span></span>

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

### <span data-ttu-id="278ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278ea-121">CommonParameters</span></span>
<span data-ttu-id="278ea-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="278ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278ea-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="278ea-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278ea-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="278ea-124">INPUTS</span></span>

### <span data-ttu-id="278ea-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="278ea-125">None</span></span>

## <span data-ttu-id="278ea-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="278ea-126">OUTPUTS</span></span>

### <span data-ttu-id="278ea-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="278ea-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="278ea-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="278ea-128">NOTES</span></span>

## <span data-ttu-id="278ea-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="278ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="278ea-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="278ea-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)