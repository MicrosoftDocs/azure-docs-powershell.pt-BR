---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427792"
---
# <span data-ttu-id="95d6e-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="95d6e-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="95d6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="95d6e-103">Obtém as cadeias de conexão primária e secundária para o namespace ou a fila ou tópico determinado.</span><span class="sxs-lookup"><span data-stu-id="95d6e-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95d6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95d6e-104">SYNTAX</span></span>

### <span data-ttu-id="95d6e-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="95d6e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95d6e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="95d6e-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95d6e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="95d6e-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95d6e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95d6e-108">DESCRIPTION</span></span>
<span data-ttu-id="95d6e-109">O cmdlet **Get-AzureRmServiceBusKey** retorna as cadeias de conexão primária e secundária para o namespace ou a fila ou tópico determinado.</span><span class="sxs-lookup"><span data-stu-id="95d6e-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="95d6e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95d6e-110">EXAMPLES</span></span>

### <span data-ttu-id="95d6e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95d6e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="95d6e-112">Cadeia de conexão primária e secundária para o namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="95d6e-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="95d6e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="95d6e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="95d6e-114">Cadeia de conexão primária e secundária para a fila especificada.</span><span class="sxs-lookup"><span data-stu-id="95d6e-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="95d6e-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="95d6e-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="95d6e-116">Cadeia de conexão primária e secundária para o tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="95d6e-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="95d6e-117">OS</span><span class="sxs-lookup"><span data-stu-id="95d6e-117">PARAMETERS</span></span>

### <span data-ttu-id="95d6e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="95d6e-118">-Name</span></span>
<span data-ttu-id="95d6e-119">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="95d6e-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d6e-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="95d6e-120">-Namespace</span></span>
<span data-ttu-id="95d6e-121">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="95d6e-121">Namespace Name.</span></span>

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

### <span data-ttu-id="95d6e-122">-Queue</span><span class="sxs-lookup"><span data-stu-id="95d6e-122">-Queue</span></span>
<span data-ttu-id="95d6e-123">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="95d6e-123">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d6e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d6e-124">-ResourceGroupName</span></span>
<span data-ttu-id="95d6e-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="95d6e-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d6e-126">-Tópico</span><span class="sxs-lookup"><span data-stu-id="95d6e-126">-Topic</span></span>
<span data-ttu-id="95d6e-127">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="95d6e-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d6e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d6e-128">-DefaultProfile</span></span>
<span data-ttu-id="95d6e-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95d6e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95d6e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d6e-130">CommonParameters</span></span>
<span data-ttu-id="95d6e-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d6e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d6e-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d6e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d6e-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95d6e-133">INPUTS</span></span>

### <span data-ttu-id="95d6e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="95d6e-134">System.String</span></span>

## <span data-ttu-id="95d6e-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95d6e-135">OUTPUTS</span></span>

### <span data-ttu-id="95d6e-136">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="95d6e-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="95d6e-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95d6e-137">NOTES</span></span>

## <span data-ttu-id="95d6e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95d6e-138">RELATED LINKS</span></span>

