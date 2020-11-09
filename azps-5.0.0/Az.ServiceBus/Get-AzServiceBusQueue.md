---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 367d5b9184e98b9559d0f2f09696c2cf9905a854
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280469"
---
# <span data-ttu-id="c309b-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c309b-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="c309b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c309b-102">SYNOPSIS</span></span>
<span data-ttu-id="c309b-103">Retorna uma descrição para a fila de barramento de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="c309b-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="c309b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c309b-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c309b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c309b-105">DESCRIPTION</span></span>
<span data-ttu-id="c309b-106">Retorna uma descrição para a fila de barramento de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="c309b-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="c309b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c309b-107">EXAMPLES</span></span>

### <span data-ttu-id="c309b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c309b-108">Example 1</span></span>
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

<span data-ttu-id="c309b-109">Retorna a descrição da fila.</span><span class="sxs-lookup"><span data-stu-id="c309b-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="c309b-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c309b-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="c309b-111">Retorna a lista de filas para determinado namespace, por padrão, as filas do 100 serão retornadas, se mais de 100 filas forem retornadas, use o parâmetro-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="c309b-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="c309b-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c309b-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="c309b-113">Retorna a lista de primeiras filas do 150 para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="c309b-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="c309b-114">OS</span><span class="sxs-lookup"><span data-stu-id="c309b-114">PARAMETERS</span></span>

### <span data-ttu-id="c309b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c309b-115">-DefaultProfile</span></span>
<span data-ttu-id="c309b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c309b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c309b-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c309b-117">-MaxCount</span></span>
<span data-ttu-id="c309b-118">Determine o número máximo de filas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="c309b-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="c309b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c309b-119">-Name</span></span>
<span data-ttu-id="c309b-120">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="c309b-120">Queue Name</span></span>

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

### <span data-ttu-id="c309b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c309b-121">-Namespace</span></span>
<span data-ttu-id="c309b-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="c309b-122">Namespace Name</span></span>

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

### <span data-ttu-id="c309b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c309b-123">-ResourceGroupName</span></span>
<span data-ttu-id="c309b-124">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c309b-124">The name of the resource group</span></span>

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

### <span data-ttu-id="c309b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c309b-125">CommonParameters</span></span>
<span data-ttu-id="c309b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c309b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c309b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c309b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c309b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c309b-128">INPUTS</span></span>

### <span data-ttu-id="c309b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c309b-129">System.String</span></span>

## <span data-ttu-id="c309b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c309b-130">OUTPUTS</span></span>

### <span data-ttu-id="c309b-131">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="c309b-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="c309b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c309b-132">NOTES</span></span>

## <span data-ttu-id="c309b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c309b-133">RELATED LINKS</span></span>
