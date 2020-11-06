---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: d05a8bb98910a478790581b21a0f4ee7be710ea1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599136"
---
# <span data-ttu-id="9f7ff-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="9f7ff-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="9f7ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9f7ff-103">Atualiza a descrição de uma assinatura para um tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9f7ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f7ff-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f7ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f7ff-105">DESCRIPTION</span></span>
<span data-ttu-id="9f7ff-106">O cmdlet **set-AzServiceBusSubscription** atualiza a descrição da assinatura para o tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9f7ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f7ff-107">EXAMPLES</span></span>

### <span data-ttu-id="9f7ff-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f7ff-108">Example 1</span></span>
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

<span data-ttu-id="9f7ff-109">Atualiza a descrição da assinatura especificada para o tópico fornecido.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="9f7ff-110">Este exemplo atualiza a propriedade **DeadLetteringOnMessageExpiration** para **true** e **MaxDeliveryCount** para 9.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="9f7ff-111">OS</span><span class="sxs-lookup"><span data-stu-id="9f7ff-111">PARAMETERS</span></span>

### <span data-ttu-id="9f7ff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f7ff-112">-DefaultProfile</span></span>
<span data-ttu-id="9f7ff-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f7ff-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f7ff-114">-InputObject</span></span>
<span data-ttu-id="9f7ff-115">Definição da assinatura do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="9f7ff-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9f7ff-116">-Namespace</span></span>
<span data-ttu-id="9f7ff-117">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-117">Namespace Name.</span></span>

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

### <span data-ttu-id="9f7ff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f7ff-118">-ResourceGroupName</span></span>
<span data-ttu-id="9f7ff-119">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9f7ff-119">The name of the resource group</span></span>

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

### <span data-ttu-id="9f7ff-120">-Tópico</span><span class="sxs-lookup"><span data-stu-id="9f7ff-120">-Topic</span></span>
<span data-ttu-id="9f7ff-121">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-121">Topic Name.</span></span>

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

### <span data-ttu-id="9f7ff-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9f7ff-122">-Confirm</span></span>
<span data-ttu-id="9f7ff-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f7ff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f7ff-124">-WhatIf</span></span>
<span data-ttu-id="9f7ff-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f7ff-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f7ff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f7ff-127">CommonParameters</span></span>
<span data-ttu-id="9f7ff-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f7ff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f7ff-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f7ff-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f7ff-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f7ff-130">INPUTS</span></span>

### <span data-ttu-id="9f7ff-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9f7ff-131">System.String</span></span>

### <span data-ttu-id="9f7ff-132">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="9f7ff-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="9f7ff-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f7ff-133">OUTPUTS</span></span>

### <span data-ttu-id="9f7ff-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="9f7ff-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="9f7ff-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f7ff-135">NOTES</span></span>

## <span data-ttu-id="9f7ff-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f7ff-136">RELATED LINKS</span></span>
