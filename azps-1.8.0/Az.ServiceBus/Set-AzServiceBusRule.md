---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b6682ae3c35bd16decc6e9e7b1b21de4a9ed42e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599139"
---
# <span data-ttu-id="aa57a-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="aa57a-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="aa57a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa57a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa57a-103">Atualiza a descrição da regra especificada para a assinatura fornecida.</span><span class="sxs-lookup"><span data-stu-id="aa57a-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="aa57a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa57a-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa57a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa57a-105">DESCRIPTION</span></span>
<span data-ttu-id="aa57a-106">O cmdlet **set-AzServiceBusRule** atualiza a descrição da regra especificada da assinatura determinada.</span><span class="sxs-lookup"><span data-stu-id="aa57a-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="aa57a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa57a-107">EXAMPLES</span></span>

### <span data-ttu-id="aa57a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa57a-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="aa57a-109">atualiza a **MySQL = ' Condition '** da regra `SBEule` da assinatura `SBSubscription` no tópico `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="aa57a-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="aa57a-110">OS</span><span class="sxs-lookup"><span data-stu-id="aa57a-110">PARAMETERS</span></span>

### <span data-ttu-id="aa57a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa57a-111">-DefaultProfile</span></span>
<span data-ttu-id="aa57a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa57a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa57a-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa57a-113">-InputObject</span></span>
<span data-ttu-id="aa57a-114">Definição de regras do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="aa57a-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="aa57a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa57a-115">-Name</span></span>
<span data-ttu-id="aa57a-116">Nome da regra.</span><span class="sxs-lookup"><span data-stu-id="aa57a-116">Rule Name.</span></span>

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

### <span data-ttu-id="aa57a-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aa57a-117">-Namespace</span></span>
<span data-ttu-id="aa57a-118">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="aa57a-118">Namespace Name.</span></span>

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

### <span data-ttu-id="aa57a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa57a-119">-ResourceGroupName</span></span>
<span data-ttu-id="aa57a-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="aa57a-120">The name of the resource group</span></span>

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

### <span data-ttu-id="aa57a-121">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="aa57a-121">-Subscription</span></span>
<span data-ttu-id="aa57a-122">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="aa57a-122">Subscription Name.</span></span>

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

### <span data-ttu-id="aa57a-123">-Tópico</span><span class="sxs-lookup"><span data-stu-id="aa57a-123">-Topic</span></span>
<span data-ttu-id="aa57a-124">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="aa57a-124">Topic Name.</span></span>

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

### <span data-ttu-id="aa57a-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aa57a-125">-Confirm</span></span>
<span data-ttu-id="aa57a-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa57a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa57a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa57a-127">-WhatIf</span></span>
<span data-ttu-id="aa57a-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa57a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa57a-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa57a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa57a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa57a-130">CommonParameters</span></span>
<span data-ttu-id="aa57a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa57a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa57a-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa57a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa57a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa57a-133">INPUTS</span></span>

### <span data-ttu-id="aa57a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aa57a-134">System.String</span></span>

### <span data-ttu-id="aa57a-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="aa57a-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="aa57a-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa57a-136">OUTPUTS</span></span>

### <span data-ttu-id="aa57a-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="aa57a-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="aa57a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa57a-138">NOTES</span></span>

## <span data-ttu-id="aa57a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa57a-139">RELATED LINKS</span></span>
