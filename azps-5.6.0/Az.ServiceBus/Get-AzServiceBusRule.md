---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0dc9c54b3d2a080d7bb40c8560371b31f4ad3acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890720"
---
# <span data-ttu-id="bac04-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="bac04-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="bac04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac04-102">SYNOPSIS</span></span>
<span data-ttu-id="bac04-103">Recupera a definição de uma regra existente em uma determinada Assinatura de Tópico.</span><span class="sxs-lookup"><span data-stu-id="bac04-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="bac04-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bac04-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bac04-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bac04-105">DESCRIPTION</span></span>
<span data-ttu-id="bac04-106">O cmdlet **Get-AzServiceBusRule** obtém a descrição da regra especificada na determinada assinatura do tópico.</span><span class="sxs-lookup"><span data-stu-id="bac04-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="bac04-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bac04-107">EXAMPLES</span></span>

### <span data-ttu-id="bac04-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bac04-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="bac04-109">Retorna a descrição de regra especificada para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="bac04-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="bac04-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bac04-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="bac04-111">Retorna a lista de descrições de regra para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="bac04-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="bac04-112">Por padrão, a regra 100 será retornada, se mais de 100 regra for retornada, use -MaxCount Parameter.</span><span class="sxs-lookup"><span data-stu-id="bac04-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="bac04-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bac04-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="bac04-114">Retorna a lista das primeiras 150 descrições de regras para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="bac04-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="bac04-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bac04-115">PARAMETERS</span></span>

### <span data-ttu-id="bac04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac04-116">-DefaultProfile</span></span>
<span data-ttu-id="bac04-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bac04-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bac04-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bac04-118">-MaxCount</span></span>
<span data-ttu-id="bac04-119">Determine o número máximo de Regras a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="bac04-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac04-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bac04-120">-Name</span></span>
<span data-ttu-id="bac04-121">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="bac04-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac04-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bac04-122">-Namespace</span></span>
<span data-ttu-id="bac04-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="bac04-123">Namespace Name</span></span>

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

### <span data-ttu-id="bac04-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac04-124">-ResourceGroupName</span></span>
<span data-ttu-id="bac04-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bac04-125">The name of the resource group</span></span>

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

### <span data-ttu-id="bac04-126">-Subscription</span><span class="sxs-lookup"><span data-stu-id="bac04-126">-Subscription</span></span>
<span data-ttu-id="bac04-127">Nome da Assinatura</span><span class="sxs-lookup"><span data-stu-id="bac04-127">Subscription Name</span></span>

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

### <span data-ttu-id="bac04-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="bac04-128">-Topic</span></span>
<span data-ttu-id="bac04-129">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="bac04-129">Topic Name</span></span>

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

### <span data-ttu-id="bac04-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac04-130">CommonParameters</span></span>
<span data-ttu-id="bac04-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bac04-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac04-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac04-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac04-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bac04-133">INPUTS</span></span>

### <span data-ttu-id="bac04-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bac04-134">System.String</span></span>

## <span data-ttu-id="bac04-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bac04-135">OUTPUTS</span></span>

### <span data-ttu-id="bac04-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="bac04-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="bac04-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="bac04-137">NOTES</span></span>

## <span data-ttu-id="bac04-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bac04-138">RELATED LINKS</span></span>
