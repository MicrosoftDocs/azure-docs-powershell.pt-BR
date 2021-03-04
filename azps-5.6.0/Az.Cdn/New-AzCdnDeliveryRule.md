---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: a2143e0363d08a06ac72ee7c5207ef93f5c3a509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891881"
---
# <span data-ttu-id="353a5-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="353a5-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="353a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="353a5-102">SYNOPSIS</span></span>
<span data-ttu-id="353a5-103">Cria uma regra de entrega.</span><span class="sxs-lookup"><span data-stu-id="353a5-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="353a5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="353a5-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="353a5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="353a5-105">DESCRIPTION</span></span>
<span data-ttu-id="353a5-106">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para a criação do ponto de extremidade cdn.</span><span class="sxs-lookup"><span data-stu-id="353a5-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="353a5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="353a5-107">EXAMPLES</span></span>

### <span data-ttu-id="353a5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="353a5-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="353a5-109">Crie uma regra simples.</span><span class="sxs-lookup"><span data-stu-id="353a5-109">Create a simple rule.</span></span>

## <span data-ttu-id="353a5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="353a5-110">PARAMETERS</span></span>

### <span data-ttu-id="353a5-111">-Action</span><span class="sxs-lookup"><span data-stu-id="353a5-111">-Action</span></span>
<span data-ttu-id="353a5-112">Uma lista de ações executadas quando todas as condições de uma regra são atendidas.</span><span class="sxs-lookup"><span data-stu-id="353a5-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353a5-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="353a5-113">-Condition</span></span>
<span data-ttu-id="353a5-114">Uma lista de condições que devem ser corresponder às ações a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="353a5-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353a5-115">-DefaultProfile</span></span>
<span data-ttu-id="353a5-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="353a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="353a5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="353a5-117">-Name</span></span>
<span data-ttu-id="353a5-118">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="353a5-118">Name of the rule</span></span>

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

### <span data-ttu-id="353a5-119">-Order</span><span class="sxs-lookup"><span data-stu-id="353a5-119">-Order</span></span>
<span data-ttu-id="353a5-120">Ordem da regra</span><span class="sxs-lookup"><span data-stu-id="353a5-120">Order of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353a5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353a5-121">CommonParameters</span></span>
<span data-ttu-id="353a5-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353a5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353a5-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="353a5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353a5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="353a5-124">INPUTS</span></span>

### <span data-ttu-id="353a5-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="353a5-125">None</span></span>

## <span data-ttu-id="353a5-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="353a5-126">OUTPUTS</span></span>

### <span data-ttu-id="353a5-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="353a5-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="353a5-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="353a5-128">NOTES</span></span>

## <span data-ttu-id="353a5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="353a5-129">RELATED LINKS</span></span>
