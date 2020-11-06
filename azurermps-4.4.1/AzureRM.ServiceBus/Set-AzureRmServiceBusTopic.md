---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 4b346d1ef4757d74ac9c663f5c72a134d5c48153
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430624"
---
# <span data-ttu-id="f0d46-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f0d46-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="f0d46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0d46-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d46-103">Atualiza a descrição de um tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="f0d46-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0d46-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0d46-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0d46-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d46-106">O cmdlet **set-AzureRmServiceBusTopic** atualiza um objeto Description para um tópico de barramento de serviço no namespace Bus Bus especificado.</span><span class="sxs-lookup"><span data-stu-id="f0d46-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f0d46-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0d46-107">EXAMPLES</span></span>

### <span data-ttu-id="f0d46-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0d46-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj
```

<span data-ttu-id="f0d46-109">Atualiza o tópico especificado com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="f0d46-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="f0d46-110">Este exemplo atualiza a propriedade **EnableExpress** para **true**.</span><span class="sxs-lookup"><span data-stu-id="f0d46-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="f0d46-111">OS</span><span class="sxs-lookup"><span data-stu-id="f0d46-111">PARAMETERS</span></span>

### <span data-ttu-id="f0d46-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f0d46-112">-Confirm</span></span>
<span data-ttu-id="f0d46-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d46-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d46-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d46-114">-WhatIf</span></span>
<span data-ttu-id="f0d46-115">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f0d46-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0d46-116">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0d46-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d46-117">-DefaultProfile</span></span>
<span data-ttu-id="f0d46-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d46-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d46-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0d46-119">-InputObject</span></span>
<span data-ttu-id="f0d46-120">Definição do tópico do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="f0d46-120">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d46-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0d46-121">-Name</span></span>
<span data-ttu-id="f0d46-122">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="f0d46-122">Topic Name.</span></span>

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

### <span data-ttu-id="f0d46-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f0d46-123">-Namespace</span></span>
<span data-ttu-id="f0d46-124">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="f0d46-124">Namespace Name.</span></span>

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

### <span data-ttu-id="f0d46-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d46-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0d46-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f0d46-126">The name of the resource group</span></span>

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

### <span data-ttu-id="f0d46-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d46-127">CommonParameters</span></span>
<span data-ttu-id="f0d46-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d46-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d46-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d46-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d46-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0d46-130">INPUTS</span></span>

### <span data-ttu-id="f0d46-131">-Resource</span><span class="sxs-lookup"><span data-stu-id="f0d46-131">-ResourceGroup</span></span>
 <span data-ttu-id="f0d46-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f0d46-132">System.String</span></span>

### <span data-ttu-id="f0d46-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f0d46-133">-NamespaceName</span></span>
 <span data-ttu-id="f0d46-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f0d46-134">System.String</span></span>

### <span data-ttu-id="f0d46-135">-Topicname</span><span class="sxs-lookup"><span data-stu-id="f0d46-135">-TopicName</span></span>
 <span data-ttu-id="f0d46-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f0d46-136">System.String</span></span>

### <span data-ttu-id="f0d46-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="f0d46-137">-TopicObj</span></span>
 <span data-ttu-id="f0d46-138">Microsoft. Azure. Commands. ServiceBus. Models. Topicattributes</span><span class="sxs-lookup"><span data-stu-id="f0d46-138">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>

## <span data-ttu-id="f0d46-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0d46-139">OUTPUTS</span></span>

### <span data-ttu-id="f0d46-140">Microsoft. Azure. Commands. ServiceBus. Models. Topicattributes</span><span class="sxs-lookup"><span data-stu-id="f0d46-140">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="f0d46-141">Nome: local do SB-Topic_exampl1: identificação do oeste dos EUA:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1 tipo: Microsoft. ServiceBus/tópico AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: true EnablePartitioning: true EnableSubscriptionPartitioning: FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false isexpress: false MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: false SizeInBytes: 0 status: active SubscriptionCount: 1 SupportOrdering: UpdatedAt: 1/20/2017 7:12:16 PM</span><span class="sxs-lookup"><span data-stu-id="f0d46-141">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB- Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : True EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 7:12:16 PM</span></span>

## <span data-ttu-id="f0d46-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0d46-142">NOTES</span></span>

## <span data-ttu-id="f0d46-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0d46-143">RELATED LINKS</span></span>

