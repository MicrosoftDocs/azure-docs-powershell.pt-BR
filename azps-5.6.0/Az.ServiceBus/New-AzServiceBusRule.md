---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 12064269e3a8c2e424bbd0e15888968c679784e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886593"
---
# <span data-ttu-id="7c39a-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="7c39a-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="7c39a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c39a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c39a-103">Cria uma nova regra para uma determinada Assinatura de Tópico.</span><span class="sxs-lookup"><span data-stu-id="7c39a-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="7c39a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7c39a-104">SYNTAX</span></span>

### <span data-ttu-id="7c39a-105">RulePropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7c39a-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c39a-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="7c39a-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c39a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7c39a-107">DESCRIPTION</span></span>
<span data-ttu-id="7c39a-108">O cmdlet **New-AzServiceBusRule** cria uma nova regra para determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="7c39a-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="7c39a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c39a-109">EXAMPLES</span></span>

### <span data-ttu-id="7c39a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c39a-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="7c39a-111">O New-AzServiceBusRule cmdlet cria uma nova regra para a Assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="7c39a-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="7c39a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7c39a-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="7c39a-113">O New-AzServiceBusRule cmdlet cria uma nova regra para a Assinatura especificada com ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="7c39a-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="7c39a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7c39a-114">PARAMETERS</span></span>

### <span data-ttu-id="7c39a-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="7c39a-115">-ActionSqlExpression</span></span>
<span data-ttu-id="7c39a-116">Action SqlFilter Expression</span><span class="sxs-lookup"><span data-stu-id="7c39a-116">Action SqlFilter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c39a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c39a-117">-DefaultProfile</span></span>
<span data-ttu-id="7c39a-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c39a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c39a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7c39a-119">-Name</span></span>
<span data-ttu-id="7c39a-120">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="7c39a-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c39a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7c39a-121">-Namespace</span></span>
<span data-ttu-id="7c39a-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="7c39a-122">Namespace Name</span></span>

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

### <span data-ttu-id="7c39a-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="7c39a-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="7c39a-124">Ação requer pré-processamento</span><span class="sxs-lookup"><span data-stu-id="7c39a-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c39a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c39a-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c39a-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7c39a-126">The name of the resource group</span></span>

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

### <span data-ttu-id="7c39a-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="7c39a-127">-SqlExpression</span></span>
<span data-ttu-id="7c39a-128">Expressão do Filtro Sql</span><span class="sxs-lookup"><span data-stu-id="7c39a-128">Sql Filter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c39a-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="7c39a-129">-Subscription</span></span>
<span data-ttu-id="7c39a-130">Nome da Assinatura</span><span class="sxs-lookup"><span data-stu-id="7c39a-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c39a-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="7c39a-131">-Topic</span></span>
<span data-ttu-id="7c39a-132">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="7c39a-132">Topic Name</span></span>

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

### <span data-ttu-id="7c39a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c39a-133">-Confirm</span></span>
<span data-ttu-id="7c39a-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c39a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c39a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c39a-135">-WhatIf</span></span>
<span data-ttu-id="7c39a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c39a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c39a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c39a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c39a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c39a-138">CommonParameters</span></span>
<span data-ttu-id="7c39a-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c39a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c39a-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c39a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c39a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c39a-141">INPUTS</span></span>

### <span data-ttu-id="7c39a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7c39a-142">System.String</span></span>

## <span data-ttu-id="7c39a-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7c39a-143">OUTPUTS</span></span>

### <span data-ttu-id="7c39a-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="7c39a-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="7c39a-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="7c39a-145">NOTES</span></span>

## <span data-ttu-id="7c39a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c39a-146">RELATED LINKS</span></span>
