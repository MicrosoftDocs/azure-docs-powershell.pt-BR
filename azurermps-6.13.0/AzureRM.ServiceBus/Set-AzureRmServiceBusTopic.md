---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: b08b4d9bd201f8a29ef878a4aaa73c926eb47151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430860"
---
# <span data-ttu-id="a5f95-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a5f95-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="a5f95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5f95-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f95-103">Atualiza a descrição de um tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="a5f95-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5f95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5f95-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5f95-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5f95-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f95-106">O cmdlet **set-AzureRmServiceBusTopic** atualiza um objeto Description para um tópico de barramento de serviço no namespace Bus Bus especificado.</span><span class="sxs-lookup"><span data-stu-id="a5f95-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a5f95-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5f95-107">EXAMPLES</span></span>

### <span data-ttu-id="a5f95-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5f95-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="a5f95-109">Atualiza o tópico especificado com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="a5f95-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="a5f95-110">Este exemplo atualiza a propriedade **EnableExpress** para **true**.</span><span class="sxs-lookup"><span data-stu-id="a5f95-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="a5f95-111">OS</span><span class="sxs-lookup"><span data-stu-id="a5f95-111">PARAMETERS</span></span>

### <span data-ttu-id="a5f95-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f95-112">-DefaultProfile</span></span>
<span data-ttu-id="a5f95-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5f95-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5f95-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5f95-114">-InputObject</span></span>
<span data-ttu-id="a5f95-115">Definição do tópico do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="a5f95-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f95-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5f95-116">-Name</span></span>
<span data-ttu-id="a5f95-117">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="a5f95-117">Topic Name.</span></span>

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

### <span data-ttu-id="a5f95-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a5f95-118">-Namespace</span></span>
<span data-ttu-id="a5f95-119">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="a5f95-119">Namespace Name.</span></span>

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

### <span data-ttu-id="a5f95-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5f95-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5f95-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a5f95-121">The name of the resource group</span></span>

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

### <span data-ttu-id="a5f95-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5f95-122">-Confirm</span></span>
<span data-ttu-id="a5f95-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5f95-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5f95-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f95-124">-WhatIf</span></span>
<span data-ttu-id="a5f95-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5f95-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f95-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5f95-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5f95-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f95-127">CommonParameters</span></span>
<span data-ttu-id="a5f95-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5f95-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f95-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5f95-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f95-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5f95-130">INPUTS</span></span>

### <span data-ttu-id="a5f95-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a5f95-131">System.String</span></span>

### <span data-ttu-id="a5f95-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="a5f95-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="a5f95-133">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5f95-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a5f95-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5f95-134">OUTPUTS</span></span>

### <span data-ttu-id="a5f95-135">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="a5f95-135">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="a5f95-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5f95-136">NOTES</span></span>

## <span data-ttu-id="a5f95-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5f95-137">RELATED LINKS</span></span>
