---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 8a8c60f486980fef6005cb4f4070af31689fae92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428762"
---
# <span data-ttu-id="f4e50-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="f4e50-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="f4e50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4e50-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e50-103">Atualiza a descrição da regra especificada para a assinatura fornecida.</span><span class="sxs-lookup"><span data-stu-id="f4e50-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4e50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4e50-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4e50-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4e50-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e50-106">O cmdlet **set-AzureRmServiceBusRule** atualiza a descrição da regra especificada da assinatura determinada.</span><span class="sxs-lookup"><span data-stu-id="f4e50-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="f4e50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4e50-107">EXAMPLES</span></span>

### <span data-ttu-id="f4e50-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4e50-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="f4e50-109">atualiza a **MySQL = ' Condition '** da regra `SBEule` da assinatura `SBSubscription` no tópico `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="f4e50-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="f4e50-110">OS</span><span class="sxs-lookup"><span data-stu-id="f4e50-110">PARAMETERS</span></span>

### <span data-ttu-id="f4e50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e50-111">-DefaultProfile</span></span>
<span data-ttu-id="f4e50-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e50-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e50-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4e50-113">-InputObject</span></span>
<span data-ttu-id="f4e50-114">Definição de regras do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="f4e50-114">ServiceBus Rules definition.</span></span>

```yaml
Type: PSRulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e50-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4e50-115">-Name</span></span>
<span data-ttu-id="f4e50-116">Nome da regra.</span><span class="sxs-lookup"><span data-stu-id="f4e50-116">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e50-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f4e50-117">-Namespace</span></span>
<span data-ttu-id="f4e50-118">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="f4e50-118">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e50-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e50-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4e50-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f4e50-120">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e50-121">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="f4e50-121">-Subscription</span></span>
<span data-ttu-id="f4e50-122">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f4e50-122">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e50-123">-Tópico</span><span class="sxs-lookup"><span data-stu-id="f4e50-123">-Topic</span></span>
<span data-ttu-id="f4e50-124">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="f4e50-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e50-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4e50-125">-Confirm</span></span>
<span data-ttu-id="f4e50-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4e50-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e50-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e50-127">-WhatIf</span></span>
<span data-ttu-id="f4e50-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4e50-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4e50-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4e50-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e50-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e50-130">CommonParameters</span></span>
<span data-ttu-id="f4e50-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e50-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e50-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e50-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e50-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4e50-133">INPUTS</span></span>

### <span data-ttu-id="f4e50-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f4e50-134">System.String</span></span>
<span data-ttu-id="f4e50-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f4e50-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="f4e50-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4e50-136">OUTPUTS</span></span>

### <span data-ttu-id="f4e50-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f4e50-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="f4e50-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4e50-138">NOTES</span></span>

## <span data-ttu-id="f4e50-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4e50-139">RELATED LINKS</span></span>

