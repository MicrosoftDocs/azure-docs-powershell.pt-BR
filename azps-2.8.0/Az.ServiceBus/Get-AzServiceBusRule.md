---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0c23f4a46782e4ff30b48cde57706680c532e8f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773238"
---
# <span data-ttu-id="35dd8-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="35dd8-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="35dd8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="35dd8-103">Cria uma nova regra para uma determinada assinatura de tópico.</span><span class="sxs-lookup"><span data-stu-id="35dd8-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="35dd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35dd8-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35dd8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35dd8-105">DESCRIPTION</span></span>
<span data-ttu-id="35dd8-106">O cmdlet **Get-AzServiceBusRule** Obtém a descrição da regra especificada na assinatura determinada do tópico.</span><span class="sxs-lookup"><span data-stu-id="35dd8-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="35dd8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35dd8-107">EXAMPLES</span></span>

### <span data-ttu-id="35dd8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35dd8-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="35dd8-109">Retorna a descrição da regra especificada para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="35dd8-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="35dd8-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="35dd8-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="35dd8-111">Retorna uma lista de descrições de regra para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="35dd8-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="35dd8-112">Por padrão, a regra 100 será retornada, se mais de 100 regras a serem retornadas, use o parâmetro-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="35dd8-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="35dd8-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="35dd8-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="35dd8-114">Retorna a lista das primeiras descrições de regras de 150 para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="35dd8-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="35dd8-115">OS</span><span class="sxs-lookup"><span data-stu-id="35dd8-115">PARAMETERS</span></span>

### <span data-ttu-id="35dd8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35dd8-116">-DefaultProfile</span></span>
<span data-ttu-id="35dd8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35dd8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35dd8-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="35dd8-118">-MaxCount</span></span>
<span data-ttu-id="35dd8-119">Determine o número máximo de regras a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="35dd8-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="35dd8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="35dd8-120">-Name</span></span>
<span data-ttu-id="35dd8-121">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="35dd8-121">Rule Name</span></span>

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

### <span data-ttu-id="35dd8-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="35dd8-122">-Namespace</span></span>
<span data-ttu-id="35dd8-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="35dd8-123">Namespace Name</span></span>

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

### <span data-ttu-id="35dd8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35dd8-124">-ResourceGroupName</span></span>
<span data-ttu-id="35dd8-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="35dd8-125">The name of the resource group</span></span>

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

### <span data-ttu-id="35dd8-126">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="35dd8-126">-Subscription</span></span>
<span data-ttu-id="35dd8-127">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="35dd8-127">Subscription Name</span></span>

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

### <span data-ttu-id="35dd8-128">-Tópico</span><span class="sxs-lookup"><span data-stu-id="35dd8-128">-Topic</span></span>
<span data-ttu-id="35dd8-129">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="35dd8-129">Topic Name</span></span>

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

### <span data-ttu-id="35dd8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35dd8-130">CommonParameters</span></span>
<span data-ttu-id="35dd8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35dd8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35dd8-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35dd8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35dd8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35dd8-133">INPUTS</span></span>

### <span data-ttu-id="35dd8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="35dd8-134">System.String</span></span>

## <span data-ttu-id="35dd8-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35dd8-135">OUTPUTS</span></span>

### <span data-ttu-id="35dd8-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="35dd8-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="35dd8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35dd8-137">NOTES</span></span>

## <span data-ttu-id="35dd8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35dd8-138">RELATED LINKS</span></span>