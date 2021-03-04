---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 9f8e7ee089972768053fd2873be22ed31dab206c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890717"
---
# <span data-ttu-id="a95fe-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a95fe-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="a95fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a95fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a95fe-103">Retorna uma descrição para o tópico Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="a95fe-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="a95fe-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a95fe-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a95fe-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a95fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a95fe-106">O cmdlet **Get-AzServiceBusTopic** retorna uma descrição de tópico para o namespace de Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="a95fe-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a95fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a95fe-107">EXAMPLES</span></span>

### <span data-ttu-id="a95fe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a95fe-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="a95fe-109">Retorna a descrição do tópico especificado para o namespace de Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="a95fe-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="a95fe-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a95fe-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="a95fe-111">Retorna a lista de tópicos para determinado namespace de Barramento de Serviço.</span><span class="sxs-lookup"><span data-stu-id="a95fe-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="a95fe-112">Por padrão, 100 tópicos serão retornados, se mais de 100 tópicos a serem retornados, use -MaxCount Parameter.</span><span class="sxs-lookup"><span data-stu-id="a95fe-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="a95fe-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a95fe-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="a95fe-114">Retorna a lista dos primeiros 150 tópicos para determinado namespace de Barramento de Serviço.</span><span class="sxs-lookup"><span data-stu-id="a95fe-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="a95fe-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a95fe-115">PARAMETERS</span></span>

### <span data-ttu-id="a95fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95fe-116">-DefaultProfile</span></span>
<span data-ttu-id="a95fe-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a95fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95fe-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a95fe-118">-MaxCount</span></span>
<span data-ttu-id="a95fe-119">Determine o número máximo de Tópicos a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="a95fe-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="a95fe-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a95fe-120">-Name</span></span>
<span data-ttu-id="a95fe-121">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="a95fe-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95fe-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a95fe-122">-Namespace</span></span>
<span data-ttu-id="a95fe-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a95fe-123">Namespace Name</span></span>

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

### <span data-ttu-id="a95fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="a95fe-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a95fe-125">The name of the resource group</span></span>

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

### <span data-ttu-id="a95fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95fe-126">CommonParameters</span></span>
<span data-ttu-id="a95fe-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a95fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95fe-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a95fe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95fe-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a95fe-129">INPUTS</span></span>

### <span data-ttu-id="a95fe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a95fe-130">System.String</span></span>

## <span data-ttu-id="a95fe-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a95fe-131">OUTPUTS</span></span>

### <span data-ttu-id="a95fe-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="a95fe-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="a95fe-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="a95fe-133">NOTES</span></span>

## <span data-ttu-id="a95fe-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a95fe-134">RELATED LINKS</span></span>
