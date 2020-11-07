---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 6175b99f5da139344c351189db5fbc5a13a137c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770847"
---
# <span data-ttu-id="d80bc-101">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="d80bc-101">New-AzFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="d80bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d80bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d80bc-103">Criar objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="d80bc-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="d80bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d80bc-104">SYNTAX</span></span>

```
New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d80bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d80bc-105">DESCRIPTION</span></span>
<span data-ttu-id="d80bc-106">Criar objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="d80bc-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="d80bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d80bc-107">EXAMPLES</span></span>

### <span data-ttu-id="d80bc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d80bc-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="d80bc-109">Criar um objeto RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d80bc-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="d80bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="d80bc-110">PARAMETERS</span></span>

### <span data-ttu-id="d80bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80bc-111">-DefaultProfile</span></span>
<span data-ttu-id="d80bc-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d80bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d80bc-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d80bc-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="d80bc-114">Lista substituir regra</span><span class="sxs-lookup"><span data-stu-id="d80bc-114">Rule override list</span></span>

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

### <span data-ttu-id="d80bc-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="d80bc-115">-RuleGroupName</span></span>
<span data-ttu-id="d80bc-116">Nome do grupo de regras para o qual essas substituições se aplicam</span><span class="sxs-lookup"><span data-stu-id="d80bc-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="d80bc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80bc-117">CommonParameters</span></span>
<span data-ttu-id="d80bc-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d80bc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80bc-119">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d80bc-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80bc-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d80bc-120">INPUTS</span></span>

### <span data-ttu-id="d80bc-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d80bc-121">None</span></span>

## <span data-ttu-id="d80bc-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d80bc-122">OUTPUTS</span></span>

### <span data-ttu-id="d80bc-123">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d80bc-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="d80bc-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d80bc-124">NOTES</span></span>

## <span data-ttu-id="d80bc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d80bc-125">RELATED LINKS</span></span>

[<span data-ttu-id="d80bc-126">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d80bc-126">New-AzFrontDoorManagedRuleObject</span></span>](./New-AzFrontDoorManagedRuleObject.md)
