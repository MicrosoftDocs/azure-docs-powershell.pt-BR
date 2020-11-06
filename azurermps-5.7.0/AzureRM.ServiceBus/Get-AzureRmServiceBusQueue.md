---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 967bc5c3126a0976096b6c9d9b6b76af8f0ef43e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428763"
---
# <span data-ttu-id="5bda5-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="5bda5-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="5bda5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bda5-102">SYNOPSIS</span></span>
<span data-ttu-id="5bda5-103">Retorna uma descrição para a fila de barramento de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="5bda5-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bda5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bda5-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bda5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5bda5-105">DESCRIPTION</span></span>
<span data-ttu-id="5bda5-106">O cmdlet **Get-AzureRmServiceBusQueue** retorna uma descrição da fila de barramento de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="5bda5-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="5bda5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bda5-107">EXAMPLES</span></span>

### <span data-ttu-id="5bda5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5bda5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:35 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S
                                      B-Queue_example1
Name                                : SB-Queue_example1
Type                                : Microsoft.ServiceBus/Queues

```

<span data-ttu-id="5bda5-109">Retorna a descrição da fila.</span><span class="sxs-lookup"><span data-stu-id="5bda5-109">Returns the description of the queue.</span></span>

## <span data-ttu-id="5bda5-110">OS</span><span class="sxs-lookup"><span data-stu-id="5bda5-110">PARAMETERS</span></span>

### <span data-ttu-id="5bda5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bda5-111">-DefaultProfile</span></span>
<span data-ttu-id="5bda5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5bda5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bda5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bda5-113">-Name</span></span>
<span data-ttu-id="5bda5-114">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="5bda5-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bda5-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5bda5-115">-Namespace</span></span>
<span data-ttu-id="5bda5-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="5bda5-116">Namespace Name.</span></span>

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

### <span data-ttu-id="5bda5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bda5-117">-ResourceGroupName</span></span>
<span data-ttu-id="5bda5-118">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5bda5-118">The name of the resource group</span></span>

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

### <span data-ttu-id="5bda5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bda5-119">CommonParameters</span></span>
<span data-ttu-id="5bda5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bda5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bda5-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bda5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bda5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5bda5-122">INPUTS</span></span>

### <span data-ttu-id="5bda5-123">-Resource</span><span class="sxs-lookup"><span data-stu-id="5bda5-123">-ResourceGroup</span></span>
 <span data-ttu-id="5bda5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5bda5-124">System.String</span></span>
 

### <span data-ttu-id="5bda5-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5bda5-125">-NamespaceName</span></span>
 <span data-ttu-id="5bda5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5bda5-126">System.String</span></span>
 

### <span data-ttu-id="5bda5-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="5bda5-127">-QueueName</span></span>
 <span data-ttu-id="5bda5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5bda5-128">System.String</span></span> 

## <span data-ttu-id="5bda5-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5bda5-129">OUTPUTS</span></span>

### <span data-ttu-id="5bda5-130">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="5bda5-130">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="5bda5-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5bda5-131">NOTES</span></span>

## <span data-ttu-id="5bda5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bda5-132">RELATED LINKS</span></span>

