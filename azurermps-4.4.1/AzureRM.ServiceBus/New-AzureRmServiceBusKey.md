---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0483c60a1624374dc3e5b750439d905f19ceb2fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610172"
---
# <span data-ttu-id="424ad-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="424ad-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="424ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="424ad-102">SYNOPSIS</span></span>
<span data-ttu-id="424ad-103">Regenera a cadeia de caracteres de conexão primária ou secundária para o namespace ou a fila ou tópico do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="424ad-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="424ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="424ad-104">SYNTAX</span></span>

### <span data-ttu-id="424ad-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="424ad-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="424ad-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="424ad-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="424ad-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="424ad-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424ad-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="424ad-108">DESCRIPTION</span></span>
<span data-ttu-id="424ad-109">O cmdlet **New-AzureRmServiceBusKey** gera novas cadeias de conexão primárias ou secundárias para o namespace ou fila ou regra de autorização ou tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="424ad-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="424ad-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="424ad-110">EXAMPLES</span></span>

### <span data-ttu-id="424ad-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="424ad-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="424ad-112">Regenera as cadeias de conexão primária ou secundária para o namespace.</span><span class="sxs-lookup"><span data-stu-id="424ad-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="424ad-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="424ad-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="424ad-114">Regenera a cadeia de caracteres de conexão primária ou secundária para a fila.</span><span class="sxs-lookup"><span data-stu-id="424ad-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="424ad-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="424ad-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="424ad-116">Regenera as cadeias de conexão primária ou secundária para o tópico.</span><span class="sxs-lookup"><span data-stu-id="424ad-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="424ad-117">OS</span><span class="sxs-lookup"><span data-stu-id="424ad-117">PARAMETERS</span></span>

### <span data-ttu-id="424ad-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="424ad-118">-Confirm</span></span>
<span data-ttu-id="424ad-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424ad-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424ad-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="424ad-120">-Name</span></span>
<span data-ttu-id="424ad-121">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="424ad-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="424ad-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="424ad-122">-Namespace</span></span>
<span data-ttu-id="424ad-123">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="424ad-123">Namespace Name.</span></span>

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

### <span data-ttu-id="424ad-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="424ad-124">-Queue</span></span>
<span data-ttu-id="424ad-125">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="424ad-125">Queue Name.</span></span>

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

### <span data-ttu-id="424ad-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="424ad-126">-RegenerateKey</span></span>
<span data-ttu-id="424ad-127">Regenerar chaves-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="424ad-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424ad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424ad-128">-ResourceGroupName</span></span>
<span data-ttu-id="424ad-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="424ad-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="424ad-130">-Tópico</span><span class="sxs-lookup"><span data-stu-id="424ad-130">-Topic</span></span>
<span data-ttu-id="424ad-131">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="424ad-131">Topic Name.</span></span>

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

### <span data-ttu-id="424ad-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424ad-132">-WhatIf</span></span>
<span data-ttu-id="424ad-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="424ad-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="424ad-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="424ad-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424ad-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424ad-135">-DefaultProfile</span></span>
<span data-ttu-id="424ad-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="424ad-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="424ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424ad-137">CommonParameters</span></span>
<span data-ttu-id="424ad-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424ad-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424ad-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424ad-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="424ad-140">INPUTS</span></span>

### <span data-ttu-id="424ad-141">System. String</span><span class="sxs-lookup"><span data-stu-id="424ad-141">System.String</span></span>

## <span data-ttu-id="424ad-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="424ad-142">OUTPUTS</span></span>

### <span data-ttu-id="424ad-143">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="424ad-143">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="424ad-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="424ad-144">NOTES</span></span>

## <span data-ttu-id="424ad-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="424ad-145">RELATED LINKS</span></span>

