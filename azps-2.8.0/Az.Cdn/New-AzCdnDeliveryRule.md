---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: 981447b1988dd750534a69529989d5d3480bc006
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597591"
---
# <span data-ttu-id="8f234-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="8f234-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="8f234-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f234-102">SYNOPSIS</span></span>
<span data-ttu-id="8f234-103">Cria uma regra de entrega.</span><span class="sxs-lookup"><span data-stu-id="8f234-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="8f234-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f234-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f234-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f234-105">DESCRIPTION</span></span>
<span data-ttu-id="8f234-106">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para criação de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="8f234-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="8f234-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f234-107">EXAMPLES</span></span>

### <span data-ttu-id="8f234-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f234-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="8f234-109">Crie uma regra simples.</span><span class="sxs-lookup"><span data-stu-id="8f234-109">Create a simple rule.</span></span>

## <span data-ttu-id="8f234-110">OS</span><span class="sxs-lookup"><span data-stu-id="8f234-110">PARAMETERS</span></span>

### <span data-ttu-id="8f234-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="8f234-111">-Action</span></span>
<span data-ttu-id="8f234-112">Uma lista de ações executadas quando todas as condições de uma regra são satisfeitas.</span><span class="sxs-lookup"><span data-stu-id="8f234-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="8f234-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="8f234-113">-Condition</span></span>
<span data-ttu-id="8f234-114">Uma lista de condições que devem ser atendidas para que as ações sejam executadas.</span><span class="sxs-lookup"><span data-stu-id="8f234-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="8f234-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f234-115">-DefaultProfile</span></span>
<span data-ttu-id="8f234-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f234-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f234-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f234-117">-Name</span></span>
<span data-ttu-id="8f234-118">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="8f234-118">Name of the rule</span></span>

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

### <span data-ttu-id="8f234-119">-Pedido</span><span class="sxs-lookup"><span data-stu-id="8f234-119">-Order</span></span>
<span data-ttu-id="8f234-120">Ordem da regra</span><span class="sxs-lookup"><span data-stu-id="8f234-120">Order of the rule</span></span>

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

### <span data-ttu-id="8f234-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f234-121">CommonParameters</span></span>
<span data-ttu-id="8f234-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f234-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f234-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f234-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f234-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f234-124">INPUTS</span></span>

### <span data-ttu-id="8f234-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8f234-125">None</span></span>

## <span data-ttu-id="8f234-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f234-126">OUTPUTS</span></span>

### <span data-ttu-id="8f234-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="8f234-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="8f234-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f234-128">NOTES</span></span>

## <span data-ttu-id="8f234-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f234-129">RELATED LINKS</span></span>
