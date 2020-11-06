---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 869bfdaa7ff772980b7acf1caee6c7d6a8784d37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599180"
---
# <span data-ttu-id="e8992-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="e8992-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="e8992-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8992-102">SYNOPSIS</span></span>
<span data-ttu-id="e8992-103">Cria uma nova regra para uma determinada assinatura de tópico.</span><span class="sxs-lookup"><span data-stu-id="e8992-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="e8992-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8992-104">SYNTAX</span></span>

### <span data-ttu-id="e8992-105">RulePropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8992-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8992-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e8992-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8992-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8992-107">DESCRIPTION</span></span>
<span data-ttu-id="e8992-108">O cmdlet **New-AzServiceBusRule** cria uma nova regra para a assinatura determinada.</span><span class="sxs-lookup"><span data-stu-id="e8992-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="e8992-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8992-109">EXAMPLES</span></span>

### <span data-ttu-id="e8992-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8992-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="e8992-111">O cmdlet New-AzServiceBusRule cria uma nova regra para a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="e8992-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="e8992-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e8992-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="e8992-113">O cmdlet New-AzServiceBusRule cria uma nova regra para a assinatura especificada com o ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="e8992-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="e8992-114">OS</span><span class="sxs-lookup"><span data-stu-id="e8992-114">PARAMETERS</span></span>

### <span data-ttu-id="e8992-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="e8992-115">-ActionSqlExpression</span></span>
<span data-ttu-id="e8992-116">Expressão SqlFillter de ação</span><span class="sxs-lookup"><span data-stu-id="e8992-116">Action SqlFillter Expression</span></span>

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

### <span data-ttu-id="e8992-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8992-117">-DefaultProfile</span></span>
<span data-ttu-id="e8992-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8992-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8992-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8992-119">-Name</span></span>
<span data-ttu-id="e8992-120">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="e8992-120">Rule Name</span></span>

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

### <span data-ttu-id="e8992-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e8992-121">-Namespace</span></span>
<span data-ttu-id="e8992-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="e8992-122">Namespace Name</span></span>

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

### <span data-ttu-id="e8992-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="e8992-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="e8992-124">A ação requer pré-processamento</span><span class="sxs-lookup"><span data-stu-id="e8992-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="e8992-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8992-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8992-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e8992-126">The name of the resource group</span></span>

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

### <span data-ttu-id="e8992-127">-Sqlexpression</span><span class="sxs-lookup"><span data-stu-id="e8992-127">-SqlExpression</span></span>
<span data-ttu-id="e8992-128">Expressão filtrar SQL</span><span class="sxs-lookup"><span data-stu-id="e8992-128">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="e8992-129">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="e8992-129">-Subscription</span></span>
<span data-ttu-id="e8992-130">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="e8992-130">Subscription Name</span></span>

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

### <span data-ttu-id="e8992-131">-Tópico</span><span class="sxs-lookup"><span data-stu-id="e8992-131">-Topic</span></span>
<span data-ttu-id="e8992-132">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="e8992-132">Topic Name</span></span>

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

### <span data-ttu-id="e8992-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e8992-133">-Confirm</span></span>
<span data-ttu-id="e8992-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8992-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8992-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8992-135">-WhatIf</span></span>
<span data-ttu-id="e8992-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8992-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8992-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8992-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8992-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8992-138">CommonParameters</span></span>
<span data-ttu-id="e8992-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8992-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8992-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8992-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8992-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8992-141">INPUTS</span></span>

### <span data-ttu-id="e8992-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e8992-142">System.String</span></span>

## <span data-ttu-id="e8992-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8992-143">OUTPUTS</span></span>

### <span data-ttu-id="e8992-144">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="e8992-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="e8992-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8992-145">NOTES</span></span>

## <span data-ttu-id="e8992-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8992-146">RELATED LINKS</span></span>
