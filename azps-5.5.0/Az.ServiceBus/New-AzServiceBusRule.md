---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117130"
---
# <span data-ttu-id="366ec-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="366ec-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="366ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="366ec-102">SYNOPSIS</span></span>
<span data-ttu-id="366ec-103">Cria uma nova regra para uma determinada Assinatura de Tópico.</span><span class="sxs-lookup"><span data-stu-id="366ec-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="366ec-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="366ec-104">SYNTAX</span></span>

### <span data-ttu-id="366ec-105">RulePropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="366ec-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="366ec-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="366ec-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="366ec-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="366ec-107">DESCRIPTION</span></span>
<span data-ttu-id="366ec-108">O **cmdlet New-AzServiceBusRule** cria uma nova regra para determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="366ec-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="366ec-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="366ec-109">EXAMPLES</span></span>

### <span data-ttu-id="366ec-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="366ec-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="366ec-111">O New-AzServiceBusRule cmdlet cria uma nova regra para a Assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="366ec-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="366ec-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="366ec-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="366ec-113">O New-AzServiceBusRule cmdlet cria uma nova regra para a assinatura especificada com o ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="366ec-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="366ec-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="366ec-114">PARAMETERS</span></span>

### <span data-ttu-id="366ec-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="366ec-115">-ActionSqlExpression</span></span>
<span data-ttu-id="366ec-116">Action SqlFilter Expression</span><span class="sxs-lookup"><span data-stu-id="366ec-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="366ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366ec-117">-DefaultProfile</span></span>
<span data-ttu-id="366ec-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="366ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="366ec-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="366ec-119">-Name</span></span>
<span data-ttu-id="366ec-120">Nome da Regra</span><span class="sxs-lookup"><span data-stu-id="366ec-120">Rule Name</span></span>

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

### <span data-ttu-id="366ec-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="366ec-121">-Namespace</span></span>
<span data-ttu-id="366ec-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="366ec-122">Namespace Name</span></span>

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

### <span data-ttu-id="366ec-123">- RequerPreprocessamento</span><span class="sxs-lookup"><span data-stu-id="366ec-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="366ec-124">Ação requer pré-processamento</span><span class="sxs-lookup"><span data-stu-id="366ec-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="366ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="366ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="366ec-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="366ec-126">The name of the resource group</span></span>

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

### <span data-ttu-id="366ec-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="366ec-127">-SqlExpression</span></span>
<span data-ttu-id="366ec-128">Sql Filter Expression</span><span class="sxs-lookup"><span data-stu-id="366ec-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="366ec-129">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="366ec-129">-Subscription</span></span>
<span data-ttu-id="366ec-130">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="366ec-130">Subscription Name</span></span>

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

### <span data-ttu-id="366ec-131">-Tópico</span><span class="sxs-lookup"><span data-stu-id="366ec-131">-Topic</span></span>
<span data-ttu-id="366ec-132">Nome do Tópico</span><span class="sxs-lookup"><span data-stu-id="366ec-132">Topic Name</span></span>

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

### <span data-ttu-id="366ec-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="366ec-133">-Confirm</span></span>
<span data-ttu-id="366ec-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="366ec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="366ec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="366ec-135">-WhatIf</span></span>
<span data-ttu-id="366ec-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="366ec-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="366ec-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="366ec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="366ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366ec-138">CommonParameters</span></span>
<span data-ttu-id="366ec-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="366ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366ec-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="366ec-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366ec-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="366ec-141">INPUTS</span></span>

### <span data-ttu-id="366ec-142">System.String</span><span class="sxs-lookup"><span data-stu-id="366ec-142">System.String</span></span>

## <span data-ttu-id="366ec-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="366ec-143">OUTPUTS</span></span>

### <span data-ttu-id="366ec-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="366ec-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="366ec-145">Notas</span><span class="sxs-lookup"><span data-stu-id="366ec-145">NOTES</span></span>

## <span data-ttu-id="366ec-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="366ec-146">RELATED LINKS</span></span>
