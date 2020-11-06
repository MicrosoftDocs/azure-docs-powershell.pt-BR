---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603219"
---
# <span data-ttu-id="f5644-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="f5644-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="f5644-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5644-102">SYNOPSIS</span></span>
<span data-ttu-id="f5644-103">Cria uma nova regra para uma determinada assinatura de tópico.</span><span class="sxs-lookup"><span data-stu-id="f5644-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5644-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5644-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5644-105">DESCRIPTION</span></span>
<span data-ttu-id="f5644-106">O cmdlet **New-AzureRmServiceBusRule** cria uma nova regra para a assinatura determinada.</span><span class="sxs-lookup"><span data-stu-id="f5644-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="f5644-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5644-107">EXAMPLES</span></span>

### <span data-ttu-id="f5644-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5644-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="f5644-109">O cmdlet New-AzureRmServiceBusRule cria uma nova regra para a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="f5644-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="f5644-110">OS</span><span class="sxs-lookup"><span data-stu-id="f5644-110">PARAMETERS</span></span>

### <span data-ttu-id="f5644-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5644-111">-DefaultProfile</span></span>
<span data-ttu-id="f5644-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5644-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5644-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5644-113">-Name</span></span>
<span data-ttu-id="f5644-114">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="f5644-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5644-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5644-115">-Namespace</span></span>
<span data-ttu-id="f5644-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="f5644-116">Namespace Name.</span></span>

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

### <span data-ttu-id="f5644-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5644-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5644-118">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f5644-118">The name of the resource group</span></span>

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

### <span data-ttu-id="f5644-119">-Sqlexpression</span><span class="sxs-lookup"><span data-stu-id="f5644-119">-SqlExpression</span></span>
<span data-ttu-id="f5644-120">Expressão filtrar SQL</span><span class="sxs-lookup"><span data-stu-id="f5644-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5644-121">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="f5644-121">-Subscription</span></span>
<span data-ttu-id="f5644-122">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="f5644-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5644-123">-Tópico</span><span class="sxs-lookup"><span data-stu-id="f5644-123">-Topic</span></span>
<span data-ttu-id="f5644-124">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="f5644-124">Topic Name.</span></span>

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

### <span data-ttu-id="f5644-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5644-125">-Confirm</span></span>
<span data-ttu-id="f5644-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5644-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5644-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5644-127">-WhatIf</span></span>
<span data-ttu-id="f5644-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5644-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5644-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5644-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5644-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5644-130">CommonParameters</span></span>
<span data-ttu-id="f5644-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5644-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5644-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5644-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5644-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5644-133">INPUTS</span></span>

### <span data-ttu-id="f5644-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f5644-134">System.String</span></span>

## <span data-ttu-id="f5644-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5644-135">OUTPUTS</span></span>

### <span data-ttu-id="f5644-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f5644-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="f5644-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5644-137">NOTES</span></span>

## <span data-ttu-id="f5644-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5644-138">RELATED LINKS</span></span>

