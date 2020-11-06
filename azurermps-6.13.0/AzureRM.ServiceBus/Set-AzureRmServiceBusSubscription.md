---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: dbc3acdf65f97e5fa46d9359f1f7af43c2c137d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430861"
---
# <span data-ttu-id="fac02-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="fac02-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="fac02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fac02-102">SYNOPSIS</span></span>
<span data-ttu-id="fac02-103">Atualiza a descrição de uma assinatura para um tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="fac02-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fac02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fac02-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fac02-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fac02-105">DESCRIPTION</span></span>
<span data-ttu-id="fac02-106">O cmdlet **set-AzureRmServiceBusSubscription** atualiza a descrição da assinatura para o tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="fac02-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fac02-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fac02-107">EXAMPLES</span></span>

### <span data-ttu-id="fac02-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fac02-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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
PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="fac02-109">Atualiza a descrição da assinatura especificada para o tópico fornecido.</span><span class="sxs-lookup"><span data-stu-id="fac02-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="fac02-110">Este exemplo atualiza a propriedade **DeadLetteringOnMessageExpiration** para **true** e **MaxDeliveryCount** para 9.</span><span class="sxs-lookup"><span data-stu-id="fac02-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="fac02-111">OS</span><span class="sxs-lookup"><span data-stu-id="fac02-111">PARAMETERS</span></span>

### <span data-ttu-id="fac02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac02-112">-DefaultProfile</span></span>
<span data-ttu-id="fac02-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fac02-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fac02-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fac02-114">-InputObject</span></span>
<span data-ttu-id="fac02-115">Definição da assinatura do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="fac02-115">ServiceBus Subscription definition.</span></span>

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

### <span data-ttu-id="fac02-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fac02-116">-Namespace</span></span>
<span data-ttu-id="fac02-117">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="fac02-117">Namespace Name.</span></span>

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

### <span data-ttu-id="fac02-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fac02-118">-ResourceGroupName</span></span>
<span data-ttu-id="fac02-119">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fac02-119">The name of the resource group</span></span>

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

### <span data-ttu-id="fac02-120">-Tópico</span><span class="sxs-lookup"><span data-stu-id="fac02-120">-Topic</span></span>
<span data-ttu-id="fac02-121">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="fac02-121">Topic Name.</span></span>

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

### <span data-ttu-id="fac02-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fac02-122">-Confirm</span></span>
<span data-ttu-id="fac02-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fac02-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fac02-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fac02-124">-WhatIf</span></span>
<span data-ttu-id="fac02-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fac02-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fac02-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fac02-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fac02-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac02-127">CommonParameters</span></span>
<span data-ttu-id="fac02-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fac02-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac02-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fac02-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac02-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fac02-130">INPUTS</span></span>

### <span data-ttu-id="fac02-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fac02-131">System.String</span></span>

### <span data-ttu-id="fac02-132">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="fac02-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>
<span data-ttu-id="fac02-133">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fac02-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fac02-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fac02-134">OUTPUTS</span></span>

### <span data-ttu-id="fac02-135">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="fac02-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="fac02-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fac02-136">NOTES</span></span>

## <span data-ttu-id="fac02-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fac02-137">RELATED LINKS</span></span>
