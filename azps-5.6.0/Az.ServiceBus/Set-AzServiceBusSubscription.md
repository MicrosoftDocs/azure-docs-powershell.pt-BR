---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: e19906f4a26f39929c62ffba89bd54092b4c961c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890070"
---
# <span data-ttu-id="92a61-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="92a61-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="92a61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92a61-102">SYNOPSIS</span></span>
<span data-ttu-id="92a61-103">Atualiza uma descrição de assinatura para um tópico de Barramento de Serviço no namespace de Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="92a61-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="92a61-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="92a61-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92a61-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="92a61-105">DESCRIPTION</span></span>
<span data-ttu-id="92a61-106">O cmdlet **Set-AzServiceBusSubscription** atualiza a descrição da assinatura do tópico Barramento de Serviço no namespace de Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="92a61-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="92a61-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92a61-107">EXAMPLES</span></span>

### <span data-ttu-id="92a61-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92a61-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="92a61-109">Atualiza a descrição da assinatura especificada para o tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="92a61-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="92a61-110">Este exemplo atualiza a **propriedade DeadLetteringOnMessageExpiration** como **true** e **MaxDeliveryCount** como 9.</span><span class="sxs-lookup"><span data-stu-id="92a61-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="92a61-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="92a61-111">PARAMETERS</span></span>

### <span data-ttu-id="92a61-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a61-112">-DefaultProfile</span></span>
<span data-ttu-id="92a61-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="92a61-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92a61-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92a61-114">-InputObject</span></span>
<span data-ttu-id="92a61-115">Definição de assinatura serviceBus.</span><span class="sxs-lookup"><span data-stu-id="92a61-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92a61-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="92a61-116">-Namespace</span></span>
<span data-ttu-id="92a61-117">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="92a61-117">Namespace Name.</span></span>

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

### <span data-ttu-id="92a61-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a61-118">-ResourceGroupName</span></span>
<span data-ttu-id="92a61-119">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="92a61-119">The name of the resource group</span></span>

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

### <span data-ttu-id="92a61-120">-Topic</span><span class="sxs-lookup"><span data-stu-id="92a61-120">-Topic</span></span>
<span data-ttu-id="92a61-121">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="92a61-121">Topic Name.</span></span>

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

### <span data-ttu-id="92a61-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92a61-122">-Confirm</span></span>
<span data-ttu-id="92a61-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a61-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a61-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a61-124">-WhatIf</span></span>
<span data-ttu-id="92a61-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92a61-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92a61-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92a61-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a61-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a61-127">CommonParameters</span></span>
<span data-ttu-id="92a61-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a61-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a61-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a61-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a61-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92a61-130">INPUTS</span></span>

### <span data-ttu-id="92a61-131">System.String</span><span class="sxs-lookup"><span data-stu-id="92a61-131">System.String</span></span>

### <span data-ttu-id="92a61-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="92a61-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="92a61-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="92a61-133">OUTPUTS</span></span>

### <span data-ttu-id="92a61-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="92a61-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="92a61-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="92a61-135">NOTES</span></span>

## <span data-ttu-id="92a61-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92a61-136">RELATED LINKS</span></span>
