---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 13e221c0205f07be81d01fd5011fa2d937b020a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610456"
---
# <span data-ttu-id="21a0b-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="21a0b-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="21a0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="21a0b-103">Atualiza a descrição de uma assinatura para um tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="21a0b-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21a0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21a0b-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -InputObject <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21a0b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="21a0b-106">O cmdlet **set-AzureRmServiceBusSubscription** atualiza a descrição da assinatura para o tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="21a0b-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="21a0b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21a0b-107">EXAMPLES</span></span>

### <span data-ttu-id="21a0b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21a0b-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="21a0b-109">Atualiza a descrição da assinatura especificada para o tópico fornecido.</span><span class="sxs-lookup"><span data-stu-id="21a0b-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="21a0b-110">Este exemplo atualiza a propriedade **DeadLetteringOnMessageExpiration** para **true** e **MaxDeliveryCount** para 9.</span><span class="sxs-lookup"><span data-stu-id="21a0b-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="21a0b-111">OS</span><span class="sxs-lookup"><span data-stu-id="21a0b-111">PARAMETERS</span></span>

### <span data-ttu-id="21a0b-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21a0b-112">-Confirm</span></span>
<span data-ttu-id="21a0b-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21a0b-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a0b-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a0b-114">-WhatIf</span></span>
<span data-ttu-id="21a0b-115">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21a0b-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21a0b-116">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21a0b-116">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a0b-117">-DefaultProfile</span></span>
<span data-ttu-id="21a0b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21a0b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21a0b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21a0b-119">-InputObject</span></span>
<span data-ttu-id="21a0b-120">Definição da assinatura do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="21a0b-120">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21a0b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="21a0b-121">-Namespace</span></span>
<span data-ttu-id="21a0b-122">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="21a0b-122">Namespace Name.</span></span>

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

### <span data-ttu-id="21a0b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a0b-123">-ResourceGroupName</span></span>
<span data-ttu-id="21a0b-124">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="21a0b-124">The name of the resource group</span></span>

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

### <span data-ttu-id="21a0b-125">-Tópico</span><span class="sxs-lookup"><span data-stu-id="21a0b-125">-Topic</span></span>
<span data-ttu-id="21a0b-126">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="21a0b-126">Topic Name.</span></span>

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

### <span data-ttu-id="21a0b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a0b-127">CommonParameters</span></span>
<span data-ttu-id="21a0b-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a0b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a0b-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a0b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a0b-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21a0b-130">INPUTS</span></span>

### <span data-ttu-id="21a0b-131">-Resource</span><span class="sxs-lookup"><span data-stu-id="21a0b-131">-ResourceGroup</span></span>
 <span data-ttu-id="21a0b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="21a0b-132">System.String</span></span>

### <span data-ttu-id="21a0b-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="21a0b-133">-NamespaceName</span></span>
 <span data-ttu-id="21a0b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="21a0b-134">System.String</span></span>

### <span data-ttu-id="21a0b-135">-Topicname</span><span class="sxs-lookup"><span data-stu-id="21a0b-135">-TopicName</span></span>
 <span data-ttu-id="21a0b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="21a0b-136">System.String</span></span>

### <span data-ttu-id="21a0b-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="21a0b-137">-SubscriptionObj</span></span>
 <span data-ttu-id="21a0b-138">Microsoft. Azure. Commands. ServiceBus. Models. Subscriptionattributes</span><span class="sxs-lookup"><span data-stu-id="21a0b-138">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>

## <span data-ttu-id="21a0b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21a0b-139">OUTPUTS</span></span>

### <span data-ttu-id="21a0b-140">Microsoft. Azure. Commands. ServiceBus. Models. Subscriptionattributes</span><span class="sxs-lookup"><span data-stu-id="21a0b-140">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="21a0b-141">Nome: SB-TopicSubscription-example1 local: West US AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: CreatedAt: 1/20/2017 9:59:15 PM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: true EnableBatchedOperations: true EntityAvailabilityStatus: false status: LockDuration: 00:01:00 MaxDeliveryCount: 9 MessageCount: 0 RequiresSession: false status: active UpdatedAt: 1/20/2017 9:59:15 PM</span><span class="sxs-lookup"><span data-stu-id="21a0b-141">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : CreatedAt                                 : 1/20/2017 9:59:15 PM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : True EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 9 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 9:59:15 PM</span></span>

## <span data-ttu-id="21a0b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21a0b-142">NOTES</span></span>

## <span data-ttu-id="21a0b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21a0b-143">RELATED LINKS</span></span>

