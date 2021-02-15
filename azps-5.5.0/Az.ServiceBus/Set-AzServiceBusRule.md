---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112591"
---
# <span data-ttu-id="6066d-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="6066d-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="6066d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6066d-102">SYNOPSIS</span></span>
<span data-ttu-id="6066d-103">Atualiza a descrição da regra especificada para a determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="6066d-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="6066d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6066d-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6066d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6066d-105">DESCRIPTION</span></span>
<span data-ttu-id="6066d-106">O cmdlet **Set-AzServiceBusRule** atualiza a descrição da regra especificada da determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="6066d-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="6066d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6066d-107">EXAMPLES</span></span>

### <span data-ttu-id="6066d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6066d-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="6066d-109">Atualiza a expressão sql **mysqlexpression='condition'** da `SBRule` regra da assinatura no `SBSubscription` Tópico `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="6066d-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="6066d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6066d-110">PARAMETERS</span></span>

### <span data-ttu-id="6066d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6066d-111">-DefaultProfile</span></span>
<span data-ttu-id="6066d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6066d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6066d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6066d-113">-InputObject</span></span>
<span data-ttu-id="6066d-114">Definição de Regras do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="6066d-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="6066d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6066d-115">-Name</span></span>
<span data-ttu-id="6066d-116">Nome da regra.</span><span class="sxs-lookup"><span data-stu-id="6066d-116">Rule Name.</span></span>

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

### <span data-ttu-id="6066d-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6066d-117">-Namespace</span></span>
<span data-ttu-id="6066d-118">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="6066d-118">Namespace Name.</span></span>

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

### <span data-ttu-id="6066d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6066d-119">-ResourceGroupName</span></span>
<span data-ttu-id="6066d-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6066d-120">The name of the resource group</span></span>

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

### <span data-ttu-id="6066d-121">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="6066d-121">-Subscription</span></span>
<span data-ttu-id="6066d-122">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6066d-122">Subscription Name.</span></span>

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

### <span data-ttu-id="6066d-123">-Tópico</span><span class="sxs-lookup"><span data-stu-id="6066d-123">-Topic</span></span>
<span data-ttu-id="6066d-124">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="6066d-124">Topic Name.</span></span>

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

### <span data-ttu-id="6066d-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6066d-125">-Confirm</span></span>
<span data-ttu-id="6066d-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6066d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6066d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6066d-127">-WhatIf</span></span>
<span data-ttu-id="6066d-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6066d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6066d-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6066d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6066d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6066d-130">CommonParameters</span></span>
<span data-ttu-id="6066d-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6066d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6066d-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6066d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6066d-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="6066d-133">INPUTS</span></span>

### <span data-ttu-id="6066d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6066d-134">System.String</span></span>

### <span data-ttu-id="6066d-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6066d-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="6066d-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="6066d-136">OUTPUTS</span></span>

### <span data-ttu-id="6066d-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6066d-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="6066d-138">Notas</span><span class="sxs-lookup"><span data-stu-id="6066d-138">NOTES</span></span>

## <span data-ttu-id="6066d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6066d-139">RELATED LINKS</span></span>
