---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440947"
---
# <span data-ttu-id="4384a-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4384a-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="4384a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4384a-102">SYNOPSIS</span></span>
<span data-ttu-id="4384a-103">Obtém uma descrição da regra de autorização especificada para um determinado namespace ou fila ou tópico.</span><span class="sxs-lookup"><span data-stu-id="4384a-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4384a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4384a-104">SYNTAX</span></span>

### <span data-ttu-id="4384a-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4384a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4384a-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4384a-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4384a-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4384a-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4384a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4384a-108">DESCRIPTION</span></span>
<span data-ttu-id="4384a-109">O cmdlet **Get-AzureRmServiceBusAuthorizationRule** Obtém a descrição da regra de autorização especificada no namespace ou na fila ou tópico determinado.</span><span class="sxs-lookup"><span data-stu-id="4384a-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="4384a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4384a-110">EXAMPLES</span></span>

### <span data-ttu-id="4384a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4384a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="4384a-112">Retorna a descrição da regra de autorização especificada para um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="4384a-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="4384a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4384a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="4384a-114">Retorna a descrição da regra de autorização especificada para uma fila especificada.</span><span class="sxs-lookup"><span data-stu-id="4384a-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="4384a-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4384a-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="4384a-116">Retorna a descrição da regra de autorização especificada para um tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="4384a-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="4384a-117">OS</span><span class="sxs-lookup"><span data-stu-id="4384a-117">PARAMETERS</span></span>

### <span data-ttu-id="4384a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4384a-118">-Name</span></span>
<span data-ttu-id="4384a-119">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="4384a-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4384a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4384a-120">-Namespace</span></span>
<span data-ttu-id="4384a-121">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="4384a-121">Namespace Name.</span></span>

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

### <span data-ttu-id="4384a-122">-Queue</span><span class="sxs-lookup"><span data-stu-id="4384a-122">-Queue</span></span>
<span data-ttu-id="4384a-123">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="4384a-123">Queue Name.</span></span>

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

### <span data-ttu-id="4384a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4384a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4384a-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4384a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4384a-126">-Tópico</span><span class="sxs-lookup"><span data-stu-id="4384a-126">-Topic</span></span>
<span data-ttu-id="4384a-127">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="4384a-127">Topic Name.</span></span>

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

### <span data-ttu-id="4384a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4384a-128">-DefaultProfile</span></span>
<span data-ttu-id="4384a-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4384a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4384a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4384a-130">CommonParameters</span></span>
<span data-ttu-id="4384a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4384a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4384a-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4384a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4384a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4384a-133">INPUTS</span></span>

### <span data-ttu-id="4384a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4384a-134">System.String</span></span>

## <span data-ttu-id="4384a-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4384a-135">OUTPUTS</span></span>

### <span data-ttu-id="4384a-136">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4384a-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4384a-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4384a-137">NOTES</span></span>
## <span data-ttu-id="4384a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4384a-138">RELATED LINKS</span></span>

## <span data-ttu-id="4384a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4384a-139">RELATED LINKS</span></span>

