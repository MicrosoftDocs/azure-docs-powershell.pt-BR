---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427787"
---
# <span data-ttu-id="cc465-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="cc465-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="cc465-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc465-102">SYNOPSIS</span></span>
<span data-ttu-id="cc465-103">Retorna uma descrição para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="cc465-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc465-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc465-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc465-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc465-105">DESCRIPTION</span></span>
<span data-ttu-id="cc465-106">O cmdlet **Get-AzureRmServiceBusTopic** retorna uma descrição de tópico para o namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="cc465-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="cc465-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc465-107">EXAMPLES</span></span>

### <span data-ttu-id="cc465-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc465-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="cc465-109">Retorna a descrição do tópico especificado para o namespace de barramento de serviço fornecido.</span><span class="sxs-lookup"><span data-stu-id="cc465-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="cc465-110">OS</span><span class="sxs-lookup"><span data-stu-id="cc465-110">PARAMETERS</span></span>

### <span data-ttu-id="cc465-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc465-111">-DefaultProfile</span></span>
<span data-ttu-id="cc465-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc465-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc465-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc465-113">-Name</span></span>
<span data-ttu-id="cc465-114">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="cc465-114">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc465-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc465-115">-Namespace</span></span>
<span data-ttu-id="cc465-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="cc465-116">Namespace Name.</span></span>

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

### <span data-ttu-id="cc465-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc465-117">-ResourceGroupName</span></span>
<span data-ttu-id="cc465-118">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cc465-118">The name of the resource group</span></span>

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

### <span data-ttu-id="cc465-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc465-119">CommonParameters</span></span>
<span data-ttu-id="cc465-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc465-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc465-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc465-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc465-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc465-122">INPUTS</span></span>

### <span data-ttu-id="cc465-123">-Resource</span><span class="sxs-lookup"><span data-stu-id="cc465-123">-ResourceGroup</span></span>
 <span data-ttu-id="cc465-124">System. String</span><span class="sxs-lookup"><span data-stu-id="cc465-124">System.String</span></span>
 

### <span data-ttu-id="cc465-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="cc465-125">-NamespaceName</span></span>
 <span data-ttu-id="cc465-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cc465-126">System.String</span></span>
 

### <span data-ttu-id="cc465-127">-Topicname</span><span class="sxs-lookup"><span data-stu-id="cc465-127">-TopicName</span></span>
 <span data-ttu-id="cc465-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cc465-128">System.String</span></span>

## <span data-ttu-id="cc465-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc465-129">OUTPUTS</span></span>

### <span data-ttu-id="cc465-130">Microsoft. Azure. Commands. ServiceBus. Models. Topicattributes</span><span class="sxs-lookup"><span data-stu-id="cc465-130">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="cc465-131">Nome: local do SB-Topic_exampl1: identificação do oeste dos EUA:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 tipo: Microsoft. ServiceBus/tópico AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: FilteringMessagesBeforePublishing IsAnonymousAccessible: false MaxSizeInMegabytes: false Isexpress: false RequiresDuplicateDetection: sizeInBytes: false SubscriptionCount: 0 status: active SupportOrdering: 1 UpdatedAt:: 1/20/2017 3:16:43 AM 16384</span><span class="sxs-lookup"><span data-stu-id="cc465-131">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="cc465-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc465-132">NOTES</span></span>

## <span data-ttu-id="cc465-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc465-133">RELATED LINKS</span></span>

