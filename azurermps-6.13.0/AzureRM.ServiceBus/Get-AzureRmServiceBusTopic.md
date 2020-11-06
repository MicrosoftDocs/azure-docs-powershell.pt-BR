---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: ddccdb907dac89466a81be62e104202a3e59a672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432732"
---
# <span data-ttu-id="10071-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="10071-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="10071-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10071-102">SYNOPSIS</span></span>
<span data-ttu-id="10071-103">Retorna uma descrição para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="10071-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10071-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10071-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10071-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10071-105">DESCRIPTION</span></span>
<span data-ttu-id="10071-106">O cmdlet **Get-AzureRmServiceBusTopic** retorna uma descrição de tópico para o namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="10071-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="10071-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10071-107">EXAMPLES</span></span>

### <span data-ttu-id="10071-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10071-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

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

<span data-ttu-id="10071-109">Retorna a descrição do tópico especificado para o namespace de barramento de serviço fornecido.</span><span class="sxs-lookup"><span data-stu-id="10071-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="10071-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="10071-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="10071-111">Retorna a lista de tópicos de um namespace de barramento de serviço específico.</span><span class="sxs-lookup"><span data-stu-id="10071-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="10071-112">Por padrão, os tópicos do 100 serão retornados, se mais de 100 tópicos forem retornados, use o parâmetro-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="10071-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="10071-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="10071-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="10071-114">Retorna a lista de tópicos do primeiro 150 de um namespace de barramento de serviço específico.</span><span class="sxs-lookup"><span data-stu-id="10071-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="10071-115">OS</span><span class="sxs-lookup"><span data-stu-id="10071-115">PARAMETERS</span></span>

### <span data-ttu-id="10071-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10071-116">-DefaultProfile</span></span>
<span data-ttu-id="10071-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10071-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10071-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="10071-118">-MaxCount</span></span>
<span data-ttu-id="10071-119">Determine o número máximo de tópicos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="10071-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="10071-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="10071-120">-Name</span></span>
<span data-ttu-id="10071-121">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="10071-121">Topic Name</span></span>

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

### <span data-ttu-id="10071-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="10071-122">-Namespace</span></span>
<span data-ttu-id="10071-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="10071-123">Namespace Name</span></span>

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

### <span data-ttu-id="10071-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10071-124">-ResourceGroupName</span></span>
<span data-ttu-id="10071-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="10071-125">The name of the resource group</span></span>

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

### <span data-ttu-id="10071-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10071-126">CommonParameters</span></span>
<span data-ttu-id="10071-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10071-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10071-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10071-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10071-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10071-129">INPUTS</span></span>

### <span data-ttu-id="10071-130">System. String</span><span class="sxs-lookup"><span data-stu-id="10071-130">System.String</span></span>

## <span data-ttu-id="10071-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10071-131">OUTPUTS</span></span>

### <span data-ttu-id="10071-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="10071-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="10071-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10071-133">NOTES</span></span>

## <span data-ttu-id="10071-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10071-134">RELATED LINKS</span></span>
