---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 67ce9249134365aa182024dff6e5913f68e11738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773211"
---
# <span data-ttu-id="408be-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="408be-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="408be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="408be-102">SYNOPSIS</span></span>
<span data-ttu-id="408be-103">Atualiza a descrição de um tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="408be-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="408be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="408be-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="408be-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="408be-105">DESCRIPTION</span></span>
<span data-ttu-id="408be-106">O cmdlet **set-AzServiceBusTopic** atualiza um objeto Description para um tópico de barramento de serviço no namespace Bus Bus especificado.</span><span class="sxs-lookup"><span data-stu-id="408be-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="408be-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="408be-107">EXAMPLES</span></span>

### <span data-ttu-id="408be-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="408be-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

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

<span data-ttu-id="408be-109">Atualiza o tópico especificado com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="408be-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="408be-110">Este exemplo atualiza a propriedade **EnableExpress** para **true**.</span><span class="sxs-lookup"><span data-stu-id="408be-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="408be-111">OS</span><span class="sxs-lookup"><span data-stu-id="408be-111">PARAMETERS</span></span>

### <span data-ttu-id="408be-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408be-112">-DefaultProfile</span></span>
<span data-ttu-id="408be-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="408be-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="408be-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="408be-114">-InputObject</span></span>
<span data-ttu-id="408be-115">Definição do tópico do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="408be-115">ServiceBus Topic definition.</span></span>

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

### <span data-ttu-id="408be-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="408be-116">-Name</span></span>
<span data-ttu-id="408be-117">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="408be-117">Topic Name.</span></span>

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

### <span data-ttu-id="408be-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="408be-118">-Namespace</span></span>
<span data-ttu-id="408be-119">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="408be-119">Namespace Name.</span></span>

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

### <span data-ttu-id="408be-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="408be-120">-ResourceGroupName</span></span>
<span data-ttu-id="408be-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="408be-121">The name of the resource group</span></span>

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

### <span data-ttu-id="408be-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="408be-122">-Confirm</span></span>
<span data-ttu-id="408be-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="408be-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="408be-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="408be-124">-WhatIf</span></span>
<span data-ttu-id="408be-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="408be-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="408be-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="408be-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="408be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408be-127">CommonParameters</span></span>
<span data-ttu-id="408be-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408be-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408be-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408be-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="408be-130">INPUTS</span></span>

### <span data-ttu-id="408be-131">System. String</span><span class="sxs-lookup"><span data-stu-id="408be-131">System.String</span></span>

### <span data-ttu-id="408be-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="408be-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="408be-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="408be-133">OUTPUTS</span></span>

### <span data-ttu-id="408be-134">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="408be-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="408be-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="408be-135">NOTES</span></span>

## <span data-ttu-id="408be-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="408be-136">RELATED LINKS</span></span>