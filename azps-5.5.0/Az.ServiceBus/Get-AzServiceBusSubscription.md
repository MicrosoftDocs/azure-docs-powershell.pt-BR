---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118673"
---
# <span data-ttu-id="dcae5-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="dcae5-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="dcae5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcae5-102">SYNOPSIS</span></span>
<span data-ttu-id="dcae5-103">Retorna uma descrição de assinatura para o tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="dcae5-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="dcae5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcae5-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcae5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcae5-105">DESCRIPTION</span></span>
<span data-ttu-id="dcae5-106">O cmdlet **Get-AzServiceBusSubscription** retorna uma descrição de assinatura para o tópico de Barra de Serviços especificado.</span><span class="sxs-lookup"><span data-stu-id="dcae5-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="dcae5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dcae5-107">EXAMPLES</span></span>

### <span data-ttu-id="dcae5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dcae5-108">Example 1</span></span>
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

<span data-ttu-id="dcae5-109">Retorna uma descrição de assinatura para o tópico especificado do Service Bus.</span><span class="sxs-lookup"><span data-stu-id="dcae5-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="dcae5-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dcae5-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="dcae5-111">Retorna a lista de assinaturas para o tópico especificado do Service Bus.</span><span class="sxs-lookup"><span data-stu-id="dcae5-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="dcae5-112">Por padrão, 100 assinaturas serão retornadas. Para o número de assinaturas, use -MaxCount Parameter</span><span class="sxs-lookup"><span data-stu-id="dcae5-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="dcae5-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dcae5-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="dcae5-114">Retorna a lista das primeiras 150 assinaturas para o tópico especificado do Service Bus.</span><span class="sxs-lookup"><span data-stu-id="dcae5-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="dcae5-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dcae5-115">PARAMETERS</span></span>

### <span data-ttu-id="dcae5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcae5-116">-DefaultProfile</span></span>
<span data-ttu-id="dcae5-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcae5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcae5-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="dcae5-118">-MaxCount</span></span>
<span data-ttu-id="dcae5-119">Determine o número máximo de assinaturas a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="dcae5-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="dcae5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcae5-120">-Name</span></span>
<span data-ttu-id="dcae5-121">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="dcae5-121">Subscription Name</span></span>

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

### <span data-ttu-id="dcae5-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dcae5-122">-Namespace</span></span>
<span data-ttu-id="dcae5-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="dcae5-123">Namespace Name</span></span>

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

### <span data-ttu-id="dcae5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcae5-124">-ResourceGroupName</span></span>
<span data-ttu-id="dcae5-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dcae5-125">The name of the resource group</span></span>

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

### <span data-ttu-id="dcae5-126">-Tópico</span><span class="sxs-lookup"><span data-stu-id="dcae5-126">-Topic</span></span>
<span data-ttu-id="dcae5-127">Nome do Tópico</span><span class="sxs-lookup"><span data-stu-id="dcae5-127">Topic Name</span></span>

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

### <span data-ttu-id="dcae5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcae5-128">CommonParameters</span></span>
<span data-ttu-id="dcae5-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcae5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcae5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcae5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcae5-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="dcae5-131">INPUTS</span></span>

### <span data-ttu-id="dcae5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="dcae5-132">System.String</span></span>

## <span data-ttu-id="dcae5-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="dcae5-133">OUTPUTS</span></span>

### <span data-ttu-id="dcae5-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="dcae5-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="dcae5-135">Notas</span><span class="sxs-lookup"><span data-stu-id="dcae5-135">NOTES</span></span>

## <span data-ttu-id="dcae5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcae5-136">RELATED LINKS</span></span>
