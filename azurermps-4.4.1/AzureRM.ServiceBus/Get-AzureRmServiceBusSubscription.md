---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 0e0f6a824571ab529daa576e5f3f9a4cbff08264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427791"
---
# <span data-ttu-id="8df2d-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="8df2d-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="8df2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8df2d-102">SYNOPSIS</span></span>
<span data-ttu-id="8df2d-103">Retorna uma descrição de assinatura para o tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="8df2d-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8df2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8df2d-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8df2d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8df2d-105">DESCRIPTION</span></span>
<span data-ttu-id="8df2d-106">O cmdlet **Get-AzureRmServiceBusSubscription** retorna uma descrição de assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="8df2d-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="8df2d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8df2d-107">EXAMPLES</span></span>

### <span data-ttu-id="8df2d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8df2d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="8df2d-109">Retorna uma descrição de assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="8df2d-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="8df2d-110">OS</span><span class="sxs-lookup"><span data-stu-id="8df2d-110">PARAMETERS</span></span>

### <span data-ttu-id="8df2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df2d-111">-DefaultProfile</span></span>
<span data-ttu-id="8df2d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8df2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8df2d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8df2d-113">-Name</span></span>
<span data-ttu-id="8df2d-114">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="8df2d-114">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df2d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8df2d-115">-Namespace</span></span>
<span data-ttu-id="8df2d-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="8df2d-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8df2d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df2d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8df2d-118">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8df2d-118">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8df2d-119">-Tópico</span><span class="sxs-lookup"><span data-stu-id="8df2d-119">-Topic</span></span>
<span data-ttu-id="8df2d-120">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="8df2d-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8df2d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df2d-121">CommonParameters</span></span>
<span data-ttu-id="8df2d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8df2d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df2d-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8df2d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df2d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8df2d-124">INPUTS</span></span>

### <span data-ttu-id="8df2d-125">-Resource</span><span class="sxs-lookup"><span data-stu-id="8df2d-125">-ResourceGroup</span></span>
 <span data-ttu-id="8df2d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8df2d-126">System.String</span></span>
 

### <span data-ttu-id="8df2d-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8df2d-127">-NamespaceName</span></span>
 <span data-ttu-id="8df2d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8df2d-128">System.String</span></span>
 

### <span data-ttu-id="8df2d-129">-Topicname</span><span class="sxs-lookup"><span data-stu-id="8df2d-129">-TopicName</span></span>
 <span data-ttu-id="8df2d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8df2d-130">System.String</span></span>
 

### <span data-ttu-id="8df2d-131">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="8df2d-131">-SubscriptionName</span></span>
 <span data-ttu-id="8df2d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8df2d-132">System.String</span></span>
 

## <span data-ttu-id="8df2d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8df2d-133">OUTPUTS</span></span>

### <span data-ttu-id="8df2d-134">Microsoft. Azure. Commands. ServiceBus. Models. Subscriptionattributes</span><span class="sxs-lookup"><span data-stu-id="8df2d-134">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="8df2d-135">Nome: SB-TopicSubscription-example1 local: West US AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: 10 EnableBatchedOperations: 0 EntityAvailabilityStatus: false status: LockDuration: 00:01:00 MaxDeliveryCount: 10 MessageCount: 0 RequiresSession: false status: de UpdatedAt: 1/20/2017 3:18:54</span><span class="sxs-lookup"><span data-stu-id="8df2d-135">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="8df2d-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8df2d-136">NOTES</span></span>

## <span data-ttu-id="8df2d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8df2d-137">RELATED LINKS</span></span>

