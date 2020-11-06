---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 099e86e8ed085169823c40d51de376085f768753
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599197"
---
# <span data-ttu-id="b78fa-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="b78fa-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="b78fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b78fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b78fa-103">Retorna uma descrição para a fila de barramento de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="b78fa-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="b78fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b78fa-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b78fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b78fa-105">DESCRIPTION</span></span>
<span data-ttu-id="b78fa-106">Retorna uma descrição para a fila de barramento de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="b78fa-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="b78fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b78fa-107">EXAMPLES</span></span>

### <span data-ttu-id="b78fa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b78fa-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="b78fa-109">Retorna a descrição da fila.</span><span class="sxs-lookup"><span data-stu-id="b78fa-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="b78fa-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b78fa-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="b78fa-111">Retorna a lista de filas para determinado namespace, por padrão, as filas do 100 serão retornadas, se mais de 100 filas forem retornadas, use o parâmetro-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="b78fa-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="b78fa-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b78fa-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="b78fa-113">Retorna a lista de primeiras filas do 150 para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="b78fa-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="b78fa-114">OS</span><span class="sxs-lookup"><span data-stu-id="b78fa-114">PARAMETERS</span></span>

### <span data-ttu-id="b78fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b78fa-115">-DefaultProfile</span></span>
<span data-ttu-id="b78fa-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b78fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b78fa-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b78fa-117">-MaxCount</span></span>
<span data-ttu-id="b78fa-118">Determine o número máximo de filas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="b78fa-118">Determine the maximum number of Queues to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b78fa-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b78fa-119">-Name</span></span>
<span data-ttu-id="b78fa-120">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="b78fa-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b78fa-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b78fa-121">-Namespace</span></span>
<span data-ttu-id="b78fa-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b78fa-122">Namespace Name</span></span>

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

### <span data-ttu-id="b78fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b78fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="b78fa-124">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b78fa-124">The name of the resource group</span></span>

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

### <span data-ttu-id="b78fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b78fa-125">CommonParameters</span></span>
<span data-ttu-id="b78fa-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b78fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b78fa-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b78fa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b78fa-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b78fa-128">INPUTS</span></span>

### <span data-ttu-id="b78fa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b78fa-129">System.String</span></span>

## <span data-ttu-id="b78fa-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b78fa-130">OUTPUTS</span></span>

### <span data-ttu-id="b78fa-131">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="b78fa-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="b78fa-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b78fa-132">NOTES</span></span>

## <span data-ttu-id="b78fa-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b78fa-133">RELATED LINKS</span></span>
