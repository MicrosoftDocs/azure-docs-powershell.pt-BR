---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602408"
---
# <span data-ttu-id="65da4-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="65da4-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="65da4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65da4-102">SYNOPSIS</span></span>
<span data-ttu-id="65da4-103">Remove a regra de autorização de um namespace ou uma fila ou tópico de barramento do serviço do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="65da4-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65da4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65da4-104">SYNTAX</span></span>

### <span data-ttu-id="65da4-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="65da4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="65da4-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="65da4-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="65da4-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="65da4-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="65da4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65da4-108">DESCRIPTION</span></span>
<span data-ttu-id="65da4-109">O cmdlet **Remove-AzureRmServiceBusAuthorizationRule** remove a regra de autorização de um namespace ou uma fila ou tópico de barramento do serviço para o grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="65da4-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="65da4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65da4-110">EXAMPLES</span></span>

### <span data-ttu-id="65da4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65da4-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="65da4-112">Remove a regra `SBAuthoRule1` de autorização do namespace `SB-Example1` do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="65da4-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="65da4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="65da4-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="65da4-114">Remove a regra `SBAuthoRule1` de autorização da fila `SBQueue` do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="65da4-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="65da4-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="65da4-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="65da4-116">Remove a regra `SBAuthoRule1` de autorização do tópico `SBTopic` do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="65da4-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="65da4-117">OS</span><span class="sxs-lookup"><span data-stu-id="65da4-117">PARAMETERS</span></span>

### <span data-ttu-id="65da4-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65da4-118">-Confirm</span></span>
<span data-ttu-id="65da4-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65da4-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65da4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="65da4-120">-Force</span></span>
<span data-ttu-id="65da4-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="65da4-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65da4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="65da4-122">-Name</span></span>
<span data-ttu-id="65da4-123">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="65da4-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65da4-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65da4-124">-Namespace</span></span>
<span data-ttu-id="65da4-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="65da4-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65da4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65da4-126">-PassThru</span></span>
<span data-ttu-id="65da4-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="65da4-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65da4-128">-Queue</span><span class="sxs-lookup"><span data-stu-id="65da4-128">-Queue</span></span>
<span data-ttu-id="65da4-129">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="65da4-129">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65da4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65da4-130">-ResourceGroupName</span></span>
<span data-ttu-id="65da4-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65da4-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65da4-132">-Tópico</span><span class="sxs-lookup"><span data-stu-id="65da4-132">-Topic</span></span>
<span data-ttu-id="65da4-133">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="65da4-133">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65da4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65da4-134">-WhatIf</span></span>
<span data-ttu-id="65da4-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65da4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65da4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65da4-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="65da4-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65da4-137">INPUTS</span></span>

### <span data-ttu-id="65da4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="65da4-138">System.String</span></span>


## <span data-ttu-id="65da4-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65da4-139">OUTPUTS</span></span>

### <span data-ttu-id="65da4-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65da4-140">System.Boolean</span></span>


## <span data-ttu-id="65da4-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65da4-141">NOTES</span></span>

## <span data-ttu-id="65da4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65da4-142">RELATED LINKS</span></span>

