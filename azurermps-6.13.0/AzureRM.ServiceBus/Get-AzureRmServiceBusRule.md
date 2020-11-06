---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 2d249d8935b79c310e4ca0aa1270ee67bf33ece3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602899"
---
# <span data-ttu-id="f25ff-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="f25ff-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="f25ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f25ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f25ff-103">Cria uma nova regra para uma determinada assinatura de tópico.</span><span class="sxs-lookup"><span data-stu-id="f25ff-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f25ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f25ff-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f25ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f25ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f25ff-106">O cmdlet **Get-AzureRmServiceBusRule** Obtém a descrição da regra especificada na assinatura determinada do tópico.</span><span class="sxs-lookup"><span data-stu-id="f25ff-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="f25ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f25ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f25ff-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f25ff-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="f25ff-109">Retorna a descrição da regra especificada para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="f25ff-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="f25ff-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f25ff-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="f25ff-111">Retorna uma lista de descrições de regra para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="f25ff-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="f25ff-112">Por padrão, a regra 100 será retornada, se mais de 100 regras a serem retornadas, use o parâmetro-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="f25ff-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="f25ff-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f25ff-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="f25ff-114">Retorna a lista das primeiras descrições de regras de 150 para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="f25ff-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="f25ff-115">OS</span><span class="sxs-lookup"><span data-stu-id="f25ff-115">PARAMETERS</span></span>

### <span data-ttu-id="f25ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25ff-116">-DefaultProfile</span></span>
<span data-ttu-id="f25ff-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f25ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f25ff-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f25ff-118">-MaxCount</span></span>
<span data-ttu-id="f25ff-119">Determine o número máximo de regras a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="f25ff-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="f25ff-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f25ff-120">-Name</span></span>
<span data-ttu-id="f25ff-121">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="f25ff-121">Rule Name</span></span>

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

### <span data-ttu-id="f25ff-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f25ff-122">-Namespace</span></span>
<span data-ttu-id="f25ff-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="f25ff-123">Namespace Name</span></span>

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

### <span data-ttu-id="f25ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f25ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="f25ff-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f25ff-125">The name of the resource group</span></span>

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

### <span data-ttu-id="f25ff-126">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="f25ff-126">-Subscription</span></span>
<span data-ttu-id="f25ff-127">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="f25ff-127">Subscription Name</span></span>

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

### <span data-ttu-id="f25ff-128">-Tópico</span><span class="sxs-lookup"><span data-stu-id="f25ff-128">-Topic</span></span>
<span data-ttu-id="f25ff-129">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="f25ff-129">Topic Name</span></span>

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

### <span data-ttu-id="f25ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25ff-130">CommonParameters</span></span>
<span data-ttu-id="f25ff-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f25ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25ff-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f25ff-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25ff-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f25ff-133">INPUTS</span></span>

### <span data-ttu-id="f25ff-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f25ff-134">System.String</span></span>

## <span data-ttu-id="f25ff-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f25ff-135">OUTPUTS</span></span>

### <span data-ttu-id="f25ff-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f25ff-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="f25ff-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f25ff-137">NOTES</span></span>

## <span data-ttu-id="f25ff-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f25ff-138">RELATED LINKS</span></span>
