---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 2b4ddf625e5565de0d345a5477d3ba368dcb186b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609743"
---
# <span data-ttu-id="8033c-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8033c-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="8033c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8033c-102">SYNOPSIS</span></span>
<span data-ttu-id="8033c-103">Atualiza a descrição da regra de autorização especificada para o namespace ou a fila ou o tópico específico do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="8033c-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8033c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8033c-104">SYNTAX</span></span>

### <span data-ttu-id="8033c-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8033c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8033c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8033c-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8033c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8033c-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8033c-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8033c-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8033c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8033c-109">DESCRIPTION</span></span>
<span data-ttu-id="8033c-110">O cmdlet **set-AzureRmServiceBusAuthorizationRule** atualiza a descrição da regra de autorização especificada no namespace ou na fila ou no tópico específico do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="8033c-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="8033c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8033c-111">EXAMPLES</span></span>

### <span data-ttu-id="8033c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8033c-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="8033c-113">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` no namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="8033c-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="8033c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8033c-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="8033c-115">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` na fila `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="8033c-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="8033c-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8033c-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="8033c-117">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` no tópico `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="8033c-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="8033c-118">OS</span><span class="sxs-lookup"><span data-stu-id="8033c-118">PARAMETERS</span></span>

### <span data-ttu-id="8033c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8033c-119">-DefaultProfile</span></span>
<span data-ttu-id="8033c-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8033c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8033c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8033c-121">-InputObject</span></span>
<span data-ttu-id="8033c-122">Objeto AuthorizationRule do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8033c-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8033c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8033c-123">-Name</span></span>
<span data-ttu-id="8033c-124">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8033c-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="8033c-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8033c-125">-Namespace</span></span>
<span data-ttu-id="8033c-126">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="8033c-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8033c-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="8033c-127">-Queue</span></span>
<span data-ttu-id="8033c-128">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="8033c-128">Queue Name</span></span>

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

### <span data-ttu-id="8033c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8033c-129">-ResourceGroupName</span></span>
<span data-ttu-id="8033c-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8033c-130">Resource Group Name</span></span>

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

### <span data-ttu-id="8033c-131">-Direitos</span><span class="sxs-lookup"><span data-stu-id="8033c-131">-Rights</span></span>
<span data-ttu-id="8033c-132">Direitos, por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="8033c-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8033c-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="8033c-133">-Topic</span></span>
<span data-ttu-id="8033c-134">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="8033c-134">Topic Name</span></span>

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

### <span data-ttu-id="8033c-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8033c-135">-Confirm</span></span>
<span data-ttu-id="8033c-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8033c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8033c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8033c-137">-WhatIf</span></span>
<span data-ttu-id="8033c-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8033c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8033c-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8033c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8033c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8033c-140">CommonParameters</span></span>
<span data-ttu-id="8033c-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8033c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8033c-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8033c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8033c-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8033c-143">INPUTS</span></span>

### <span data-ttu-id="8033c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8033c-144">System.String</span></span>

### <span data-ttu-id="8033c-145">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8033c-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="8033c-146">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8033c-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8033c-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="8033c-147">System.String[]</span></span>

## <span data-ttu-id="8033c-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8033c-148">OUTPUTS</span></span>

### <span data-ttu-id="8033c-149">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8033c-149">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8033c-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8033c-150">NOTES</span></span>

## <span data-ttu-id="8033c-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8033c-151">RELATED LINKS</span></span>
