---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 3d688362932f61bdea9d685b98f2cba757288da2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264237"
---
# <span data-ttu-id="419b7-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="419b7-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="419b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="419b7-102">SYNOPSIS</span></span>
<span data-ttu-id="419b7-103">Retorna uma descrição para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="419b7-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="419b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="419b7-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="419b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="419b7-105">DESCRIPTION</span></span>
<span data-ttu-id="419b7-106">O cmdlet **Get-AzServiceBusTopic** retorna uma descrição de tópico para o namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="419b7-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="419b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="419b7-107">EXAMPLES</span></span>

### <span data-ttu-id="419b7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="419b7-108">Example 1</span></span>
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

<span data-ttu-id="419b7-109">Retorna a descrição do tópico especificado para o namespace de barramento de serviço fornecido.</span><span class="sxs-lookup"><span data-stu-id="419b7-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="419b7-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="419b7-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="419b7-111">Retorna a lista de tópicos de um namespace de barramento de serviço específico.</span><span class="sxs-lookup"><span data-stu-id="419b7-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="419b7-112">Por padrão, os tópicos do 100 serão retornados, se mais de 100 tópicos forem retornados, use o parâmetro-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="419b7-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="419b7-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="419b7-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="419b7-114">Retorna a lista de tópicos do primeiro 150 de um namespace de barramento de serviço específico.</span><span class="sxs-lookup"><span data-stu-id="419b7-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="419b7-115">OS</span><span class="sxs-lookup"><span data-stu-id="419b7-115">PARAMETERS</span></span>

### <span data-ttu-id="419b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="419b7-116">-DefaultProfile</span></span>
<span data-ttu-id="419b7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="419b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="419b7-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="419b7-118">-MaxCount</span></span>
<span data-ttu-id="419b7-119">Determine o número máximo de tópicos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="419b7-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="419b7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="419b7-120">-Name</span></span>
<span data-ttu-id="419b7-121">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="419b7-121">Topic Name</span></span>

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

### <span data-ttu-id="419b7-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="419b7-122">-Namespace</span></span>
<span data-ttu-id="419b7-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="419b7-123">Namespace Name</span></span>

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

### <span data-ttu-id="419b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="419b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="419b7-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="419b7-125">The name of the resource group</span></span>

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

### <span data-ttu-id="419b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="419b7-126">CommonParameters</span></span>
<span data-ttu-id="419b7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="419b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="419b7-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="419b7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="419b7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="419b7-129">INPUTS</span></span>

### <span data-ttu-id="419b7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="419b7-130">System.String</span></span>

## <span data-ttu-id="419b7-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="419b7-131">OUTPUTS</span></span>

### <span data-ttu-id="419b7-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="419b7-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="419b7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="419b7-133">NOTES</span></span>

## <span data-ttu-id="419b7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="419b7-134">RELATED LINKS</span></span>
