---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: e09e4f19a63eef1cd4b87760239d4456afee70fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427790"
---
# <span data-ttu-id="81fac-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="81fac-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="81fac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81fac-102">SYNOPSIS</span></span>
<span data-ttu-id="81fac-103">Obtém uma descrição da regra especificada para uma determinada assinatura de tópico.</span><span class="sxs-lookup"><span data-stu-id="81fac-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81fac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81fac-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81fac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81fac-105">DESCRIPTION</span></span>
<span data-ttu-id="81fac-106">O cmdlet **Get-AzureRmServiceBusRule** Obtém a descrição da regra especificada na assinatura determinada do tópico.</span><span class="sxs-lookup"><span data-stu-id="81fac-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="81fac-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81fac-107">EXAMPLES</span></span>

### <span data-ttu-id="81fac-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81fac-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="81fac-109">Retorna a descrição da regra especificada para uma assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="81fac-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="81fac-110">OS</span><span class="sxs-lookup"><span data-stu-id="81fac-110">PARAMETERS</span></span>

### <span data-ttu-id="81fac-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="81fac-111">-Name</span></span>
<span data-ttu-id="81fac-112">Nome da regra.</span><span class="sxs-lookup"><span data-stu-id="81fac-112">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81fac-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="81fac-113">-Namespace</span></span>
<span data-ttu-id="81fac-114">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="81fac-114">Namespace Name.</span></span>

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

### <span data-ttu-id="81fac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81fac-115">-ResourceGroupName</span></span>
<span data-ttu-id="81fac-116">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="81fac-116">The name of the resource group</span></span>

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

### <span data-ttu-id="81fac-117">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="81fac-117">-Subscription</span></span>
<span data-ttu-id="81fac-118">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="81fac-118">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81fac-119">-Tópico</span><span class="sxs-lookup"><span data-stu-id="81fac-119">-Topic</span></span>
<span data-ttu-id="81fac-120">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="81fac-120">Topic Name.</span></span>

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

### <span data-ttu-id="81fac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81fac-121">-DefaultProfile</span></span>
<span data-ttu-id="81fac-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81fac-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81fac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81fac-123">CommonParameters</span></span>
<span data-ttu-id="81fac-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81fac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81fac-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81fac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81fac-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81fac-126">INPUTS</span></span>

### <span data-ttu-id="81fac-127">System. String</span><span class="sxs-lookup"><span data-stu-id="81fac-127">System.String</span></span>

## <span data-ttu-id="81fac-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81fac-128">OUTPUTS</span></span>

### <span data-ttu-id="81fac-129">Microsoft. Azure. Commands. ServiceBus. Models. Rules</span><span class="sxs-lookup"><span data-stu-id="81fac-129">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="81fac-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81fac-130">NOTES</span></span>

## <span data-ttu-id="81fac-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81fac-131">RELATED LINKS</span></span>

