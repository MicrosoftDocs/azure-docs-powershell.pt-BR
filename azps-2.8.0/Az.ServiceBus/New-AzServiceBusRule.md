---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: f3d9c9029b1c87e6d58dde21eac9d41857f53ab8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772473"
---
# <span data-ttu-id="07a1b-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="07a1b-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="07a1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="07a1b-103">Cria uma nova regra para uma determinada assinatura de tópico.</span><span class="sxs-lookup"><span data-stu-id="07a1b-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="07a1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07a1b-104">SYNTAX</span></span>

### <span data-ttu-id="07a1b-105">RulePropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="07a1b-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a1b-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="07a1b-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a1b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07a1b-107">DESCRIPTION</span></span>
<span data-ttu-id="07a1b-108">O cmdlet **New-AzServiceBusRule** cria uma nova regra para a assinatura determinada.</span><span class="sxs-lookup"><span data-stu-id="07a1b-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="07a1b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07a1b-109">EXAMPLES</span></span>

### <span data-ttu-id="07a1b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07a1b-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="07a1b-111">O cmdlet New-AzServiceBusRule cria uma nova regra para a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="07a1b-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="07a1b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="07a1b-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="07a1b-113">O cmdlet New-AzServiceBusRule cria uma nova regra para a assinatura especificada com o ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="07a1b-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="07a1b-114">OS</span><span class="sxs-lookup"><span data-stu-id="07a1b-114">PARAMETERS</span></span>

### <span data-ttu-id="07a1b-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="07a1b-115">-ActionSqlExpression</span></span>
<span data-ttu-id="07a1b-116">Expressão sqlfilter da ação</span><span class="sxs-lookup"><span data-stu-id="07a1b-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="07a1b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a1b-117">-DefaultProfile</span></span>
<span data-ttu-id="07a1b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07a1b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07a1b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="07a1b-119">-Name</span></span>
<span data-ttu-id="07a1b-120">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="07a1b-120">Rule Name</span></span>

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

### <span data-ttu-id="07a1b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07a1b-121">-Namespace</span></span>
<span data-ttu-id="07a1b-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="07a1b-122">Namespace Name</span></span>

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

### <span data-ttu-id="07a1b-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="07a1b-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="07a1b-124">A ação requer pré-processamento</span><span class="sxs-lookup"><span data-stu-id="07a1b-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="07a1b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a1b-125">-ResourceGroupName</span></span>
<span data-ttu-id="07a1b-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="07a1b-126">The name of the resource group</span></span>

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

### <span data-ttu-id="07a1b-127">-Sqlexpression</span><span class="sxs-lookup"><span data-stu-id="07a1b-127">-SqlExpression</span></span>
<span data-ttu-id="07a1b-128">Expressão de filtro SQL</span><span class="sxs-lookup"><span data-stu-id="07a1b-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="07a1b-129">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="07a1b-129">-Subscription</span></span>
<span data-ttu-id="07a1b-130">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="07a1b-130">Subscription Name</span></span>

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

### <span data-ttu-id="07a1b-131">-Tópico</span><span class="sxs-lookup"><span data-stu-id="07a1b-131">-Topic</span></span>
<span data-ttu-id="07a1b-132">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="07a1b-132">Topic Name</span></span>

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

### <span data-ttu-id="07a1b-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07a1b-133">-Confirm</span></span>
<span data-ttu-id="07a1b-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07a1b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a1b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a1b-135">-WhatIf</span></span>
<span data-ttu-id="07a1b-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07a1b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07a1b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07a1b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a1b-138">CommonParameters</span></span>
<span data-ttu-id="07a1b-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07a1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a1b-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a1b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a1b-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07a1b-141">INPUTS</span></span>

### <span data-ttu-id="07a1b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="07a1b-142">System.String</span></span>

## <span data-ttu-id="07a1b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07a1b-143">OUTPUTS</span></span>

### <span data-ttu-id="07a1b-144">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="07a1b-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="07a1b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07a1b-145">NOTES</span></span>

## <span data-ttu-id="07a1b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07a1b-146">RELATED LINKS</span></span>
