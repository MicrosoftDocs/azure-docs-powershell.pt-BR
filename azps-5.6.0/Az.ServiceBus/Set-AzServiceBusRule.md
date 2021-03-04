---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: 2caf2ccfe0d3428515812aa2dfeafc1237f820f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889085"
---
# <span data-ttu-id="d376a-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="d376a-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="d376a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d376a-102">SYNOPSIS</span></span>
<span data-ttu-id="d376a-103">Atualiza a descrição de regra especificada para a assinatura determinada.</span><span class="sxs-lookup"><span data-stu-id="d376a-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="d376a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d376a-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d376a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d376a-105">DESCRIPTION</span></span>
<span data-ttu-id="d376a-106">O cmdlet **Set-AzServiceBusRule** atualiza a descrição da regra especificada da assinatura determinada.</span><span class="sxs-lookup"><span data-stu-id="d376a-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="d376a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d376a-107">EXAMPLES</span></span>

### <span data-ttu-id="d376a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d376a-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="d376a-109">Atualiza a expressão sql **mysqlexpression='condition'** da regra `SBRule` da assinatura em `SBSubscription` Tópico `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="d376a-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="d376a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d376a-110">PARAMETERS</span></span>

### <span data-ttu-id="d376a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d376a-111">-DefaultProfile</span></span>
<span data-ttu-id="d376a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d376a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d376a-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d376a-113">-InputObject</span></span>
<span data-ttu-id="d376a-114">Definição de Regras de ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="d376a-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d376a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d376a-115">-Name</span></span>
<span data-ttu-id="d376a-116">Nome da regra.</span><span class="sxs-lookup"><span data-stu-id="d376a-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d376a-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d376a-117">-Namespace</span></span>
<span data-ttu-id="d376a-118">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="d376a-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d376a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d376a-119">-ResourceGroupName</span></span>
<span data-ttu-id="d376a-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d376a-120">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d376a-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="d376a-121">-Subscription</span></span>
<span data-ttu-id="d376a-122">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d376a-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d376a-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="d376a-123">-Topic</span></span>
<span data-ttu-id="d376a-124">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="d376a-124">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d376a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d376a-125">-Confirm</span></span>
<span data-ttu-id="d376a-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d376a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d376a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d376a-127">-WhatIf</span></span>
<span data-ttu-id="d376a-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d376a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d376a-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d376a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d376a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d376a-130">CommonParameters</span></span>
<span data-ttu-id="d376a-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d376a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d376a-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d376a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d376a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d376a-133">INPUTS</span></span>

### <span data-ttu-id="d376a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d376a-134">System.String</span></span>

### <span data-ttu-id="d376a-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="d376a-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="d376a-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d376a-136">OUTPUTS</span></span>

### <span data-ttu-id="d376a-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="d376a-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="d376a-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="d376a-138">NOTES</span></span>

## <span data-ttu-id="d376a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d376a-139">RELATED LINKS</span></span>
