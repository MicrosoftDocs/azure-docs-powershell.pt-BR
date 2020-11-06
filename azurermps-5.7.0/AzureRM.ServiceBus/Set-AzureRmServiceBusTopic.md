---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 92c26b2b92257de7cdd3bbbb0d602d45d8ea1d1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428759"
---
# <span data-ttu-id="b2e64-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="b2e64-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="b2e64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2e64-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e64-103">Atualiza a descrição de um tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="b2e64-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2e64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2e64-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2e64-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2e64-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e64-106">O cmdlet **set-AzureRmServiceBusTopic** atualiza um objeto Description para um tópico de barramento de serviço no namespace Bus Bus especificado.</span><span class="sxs-lookup"><span data-stu-id="b2e64-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b2e64-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2e64-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e64-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2e64-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-
                                      Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : True
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 7:12:16 PM
```
<span data-ttu-id="b2e64-109">Atualiza o tópico especificado com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="b2e64-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="b2e64-110">Este exemplo atualiza a propriedade **EnableExpress** para **true**.</span><span class="sxs-lookup"><span data-stu-id="b2e64-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="b2e64-111">OS</span><span class="sxs-lookup"><span data-stu-id="b2e64-111">PARAMETERS</span></span>

### <span data-ttu-id="b2e64-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e64-112">-DefaultProfile</span></span>
<span data-ttu-id="b2e64-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e64-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e64-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2e64-114">-InputObject</span></span>
<span data-ttu-id="b2e64-115">Definição do tópico do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="b2e64-115">ServiceBus Topic definition.</span></span>

```yaml
Type: PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e64-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2e64-116">-Name</span></span>
<span data-ttu-id="b2e64-117">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="b2e64-117">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e64-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b2e64-118">-Namespace</span></span>
<span data-ttu-id="b2e64-119">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="b2e64-119">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e64-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e64-120">-ResourceGroupName</span></span>
<span data-ttu-id="b2e64-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b2e64-121">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e64-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2e64-122">-Confirm</span></span>
<span data-ttu-id="b2e64-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e64-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e64-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e64-124">-WhatIf</span></span>
<span data-ttu-id="b2e64-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2e64-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e64-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2e64-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e64-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e64-127">CommonParameters</span></span>
<span data-ttu-id="b2e64-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e64-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e64-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e64-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e64-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2e64-130">INPUTS</span></span>

### <span data-ttu-id="b2e64-131">-Resource</span><span class="sxs-lookup"><span data-stu-id="b2e64-131">-ResourceGroup</span></span>
 <span data-ttu-id="b2e64-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e64-132">System.String</span></span>

### <span data-ttu-id="b2e64-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b2e64-133">-NamespaceName</span></span>
 <span data-ttu-id="b2e64-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e64-134">System.String</span></span>

### <span data-ttu-id="b2e64-135">-Topicname</span><span class="sxs-lookup"><span data-stu-id="b2e64-135">-TopicName</span></span>
 <span data-ttu-id="b2e64-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e64-136">System.String</span></span>

### <span data-ttu-id="b2e64-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="b2e64-137">-TopicObj</span></span>
 <span data-ttu-id="b2e64-138">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="b2e64-138">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="b2e64-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2e64-139">OUTPUTS</span></span>

### <span data-ttu-id="b2e64-140">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="b2e64-140">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="b2e64-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2e64-141">NOTES</span></span>

## <span data-ttu-id="b2e64-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2e64-142">RELATED LINKS</span></span>

