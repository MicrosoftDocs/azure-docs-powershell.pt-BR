---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 6ef5b99f916724dcdb746d67a6f9373e4bbfc9ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602893"
---
# <span data-ttu-id="321c7-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="321c7-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="321c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="321c7-102">SYNOPSIS</span></span>
<span data-ttu-id="321c7-103">Cria uma nova regra para uma determinada assinatura de tópico.</span><span class="sxs-lookup"><span data-stu-id="321c7-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="321c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="321c7-104">SYNTAX</span></span>

### <span data-ttu-id="321c7-105">RulePropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="321c7-105">RulePropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="321c7-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="321c7-106">RuleActionPropertiesSet</span></span>
```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="321c7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="321c7-107">DESCRIPTION</span></span>
<span data-ttu-id="321c7-108">O cmdlet **New-AzureRmServiceBusRule** cria uma nova regra para a assinatura determinada.</span><span class="sxs-lookup"><span data-stu-id="321c7-108">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="321c7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="321c7-109">EXAMPLES</span></span>

### <span data-ttu-id="321c7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="321c7-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="321c7-111">O cmdlet New-AzureRmServiceBusRule cria uma nova regra para a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="321c7-111">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>


### <span data-ttu-id="321c7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="321c7-112">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="321c7-113">O cmdlet New-AzureRmServiceBusRule cria uma nova regra para a assinatura especificada com o ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="321c7-113">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="321c7-114">OS</span><span class="sxs-lookup"><span data-stu-id="321c7-114">PARAMETERS</span></span>

### <span data-ttu-id="321c7-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="321c7-115">-ActionSqlExpression</span></span>
<span data-ttu-id="321c7-116">Expressão SqlFillter de ação</span><span class="sxs-lookup"><span data-stu-id="321c7-116">Action SqlFillter Expression</span></span>

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

### <span data-ttu-id="321c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="321c7-117">-DefaultProfile</span></span>
<span data-ttu-id="321c7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="321c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="321c7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="321c7-119">-Name</span></span>
<span data-ttu-id="321c7-120">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="321c7-120">Rule Name</span></span>

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

### <span data-ttu-id="321c7-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="321c7-121">-Namespace</span></span>
<span data-ttu-id="321c7-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="321c7-122">Namespace Name</span></span>

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

### <span data-ttu-id="321c7-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="321c7-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="321c7-124">A ação requer pré-processamento</span><span class="sxs-lookup"><span data-stu-id="321c7-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="321c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="321c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="321c7-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="321c7-126">The name of the resource group</span></span>

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

### <span data-ttu-id="321c7-127">-Sqlexpression</span><span class="sxs-lookup"><span data-stu-id="321c7-127">-SqlExpression</span></span>
<span data-ttu-id="321c7-128">Expressão filtrar SQL</span><span class="sxs-lookup"><span data-stu-id="321c7-128">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="321c7-129">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="321c7-129">-Subscription</span></span>
<span data-ttu-id="321c7-130">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="321c7-130">Subscription Name</span></span>

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

### <span data-ttu-id="321c7-131">-Tópico</span><span class="sxs-lookup"><span data-stu-id="321c7-131">-Topic</span></span>
<span data-ttu-id="321c7-132">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="321c7-132">Topic Name</span></span>

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

### <span data-ttu-id="321c7-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="321c7-133">-Confirm</span></span>
<span data-ttu-id="321c7-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="321c7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="321c7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="321c7-135">-WhatIf</span></span>
<span data-ttu-id="321c7-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="321c7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="321c7-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="321c7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="321c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321c7-138">CommonParameters</span></span>
<span data-ttu-id="321c7-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="321c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="321c7-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="321c7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321c7-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="321c7-141">INPUTS</span></span>

### <span data-ttu-id="321c7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="321c7-142">System.String</span></span>


## <span data-ttu-id="321c7-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="321c7-143">OUTPUTS</span></span>

### <span data-ttu-id="321c7-144">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="321c7-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>


## <span data-ttu-id="321c7-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="321c7-145">NOTES</span></span>

## <span data-ttu-id="321c7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="321c7-146">RELATED LINKS</span></span>
