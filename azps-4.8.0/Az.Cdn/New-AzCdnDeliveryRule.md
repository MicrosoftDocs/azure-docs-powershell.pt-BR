---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947888"
---
# <span data-ttu-id="a84ec-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="a84ec-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="a84ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a84ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a84ec-103">Cria uma regra de entrega.</span><span class="sxs-lookup"><span data-stu-id="a84ec-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="a84ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a84ec-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a84ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a84ec-105">DESCRIPTION</span></span>
<span data-ttu-id="a84ec-106">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para criação de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="a84ec-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="a84ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a84ec-107">EXAMPLES</span></span>

### <span data-ttu-id="a84ec-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a84ec-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="a84ec-109">Crie uma regra simples.</span><span class="sxs-lookup"><span data-stu-id="a84ec-109">Create a simple rule.</span></span>

## <span data-ttu-id="a84ec-110">OS</span><span class="sxs-lookup"><span data-stu-id="a84ec-110">PARAMETERS</span></span>

### <span data-ttu-id="a84ec-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="a84ec-111">-Action</span></span>
<span data-ttu-id="a84ec-112">Uma lista de ações executadas quando todas as condições de uma regra são satisfeitas.</span><span class="sxs-lookup"><span data-stu-id="a84ec-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="a84ec-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="a84ec-113">-Condition</span></span>
<span data-ttu-id="a84ec-114">Uma lista de condições que devem ser atendidas para que as ações sejam executadas.</span><span class="sxs-lookup"><span data-stu-id="a84ec-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="a84ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84ec-115">-DefaultProfile</span></span>
<span data-ttu-id="a84ec-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a84ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a84ec-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a84ec-117">-Name</span></span>
<span data-ttu-id="a84ec-118">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="a84ec-118">Name of the rule</span></span>

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

### <span data-ttu-id="a84ec-119">-Pedido</span><span class="sxs-lookup"><span data-stu-id="a84ec-119">-Order</span></span>
<span data-ttu-id="a84ec-120">Ordem da regra</span><span class="sxs-lookup"><span data-stu-id="a84ec-120">Order of the rule</span></span>

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

### <span data-ttu-id="a84ec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84ec-121">CommonParameters</span></span>
<span data-ttu-id="a84ec-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84ec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84ec-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a84ec-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84ec-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a84ec-124">INPUTS</span></span>

### <span data-ttu-id="a84ec-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a84ec-125">None</span></span>

## <span data-ttu-id="a84ec-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a84ec-126">OUTPUTS</span></span>

### <span data-ttu-id="a84ec-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="a84ec-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="a84ec-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a84ec-128">NOTES</span></span>

## <span data-ttu-id="a84ec-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a84ec-129">RELATED LINKS</span></span>
