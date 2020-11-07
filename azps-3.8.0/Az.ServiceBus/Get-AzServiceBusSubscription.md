---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943736"
---
# <span data-ttu-id="bf3ef-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="bf3ef-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="bf3ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="bf3ef-103">Retorna uma descrição de assinatura para o tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="bf3ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf3ef-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf3ef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf3ef-105">DESCRIPTION</span></span>
<span data-ttu-id="bf3ef-106">O cmdlet **Get-AzServiceBusSubscription** retorna uma descrição de assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="bf3ef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf3ef-107">EXAMPLES</span></span>

### <span data-ttu-id="bf3ef-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf3ef-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="bf3ef-109">Retorna uma descrição de assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="bf3ef-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bf3ef-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="bf3ef-111">Retorna a lista de assinaturas do tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="bf3ef-112">Por padrão, as assinaturas do 100 serão retornadas, para o número de assinaturas, use o parâmetro-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bf3ef-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="bf3ef-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bf3ef-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="bf3ef-114">Retorna a lista das primeiras assinaturas do 150 para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="bf3ef-115">OS</span><span class="sxs-lookup"><span data-stu-id="bf3ef-115">PARAMETERS</span></span>

### <span data-ttu-id="bf3ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf3ef-116">-DefaultProfile</span></span>
<span data-ttu-id="bf3ef-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf3ef-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bf3ef-118">-MaxCount</span></span>
<span data-ttu-id="bf3ef-119">Determine o número máximo de assinaturas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="bf3ef-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf3ef-120">-Name</span></span>
<span data-ttu-id="bf3ef-121">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="bf3ef-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3ef-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bf3ef-122">-Namespace</span></span>
<span data-ttu-id="bf3ef-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="bf3ef-123">Namespace Name</span></span>

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

### <span data-ttu-id="bf3ef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf3ef-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf3ef-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bf3ef-125">The name of the resource group</span></span>

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

### <span data-ttu-id="bf3ef-126">-Tópico</span><span class="sxs-lookup"><span data-stu-id="bf3ef-126">-Topic</span></span>
<span data-ttu-id="bf3ef-127">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="bf3ef-127">Topic Name</span></span>

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

### <span data-ttu-id="bf3ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf3ef-128">CommonParameters</span></span>
<span data-ttu-id="bf3ef-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf3ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf3ef-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf3ef-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf3ef-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf3ef-131">INPUTS</span></span>

### <span data-ttu-id="bf3ef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bf3ef-132">System.String</span></span>

## <span data-ttu-id="bf3ef-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf3ef-133">OUTPUTS</span></span>

### <span data-ttu-id="bf3ef-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bf3ef-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bf3ef-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf3ef-135">NOTES</span></span>

## <span data-ttu-id="bf3ef-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf3ef-136">RELATED LINKS</span></span>
