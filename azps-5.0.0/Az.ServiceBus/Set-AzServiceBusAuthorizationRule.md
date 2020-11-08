---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: da981d38f0833adc276a114c42def5d19322e0d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116725"
---
# <span data-ttu-id="cfcbc-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cfcbc-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="cfcbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfcbc-102">SYNOPSIS</span></span>
<span data-ttu-id="cfcbc-103">Atualiza a descrição da regra de autorização especificada para o namespace ou a fila ou o tópico específico do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="cfcbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfcbc-104">SYNTAX</span></span>

### <span data-ttu-id="cfcbc-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfcbc-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfcbc-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfcbc-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfcbc-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfcbc-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cfcbc-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfcbc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfcbc-109">DESCRIPTION</span></span>
<span data-ttu-id="cfcbc-110">O cmdlet **set-AzServiceBusAuthorizationRule** atualiza a descrição da regra de autorização especificada no namespace ou na fila ou no tópico específico do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="cfcbc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfcbc-111">EXAMPLES</span></span>

### <span data-ttu-id="cfcbc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cfcbc-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="cfcbc-113">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` no namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="cfcbc-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="cfcbc-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cfcbc-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="cfcbc-115">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` na fila `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="cfcbc-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="cfcbc-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cfcbc-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="cfcbc-117">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` no tópico `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="cfcbc-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="cfcbc-118">OS</span><span class="sxs-lookup"><span data-stu-id="cfcbc-118">PARAMETERS</span></span>

### <span data-ttu-id="cfcbc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfcbc-119">-DefaultProfile</span></span>
<span data-ttu-id="cfcbc-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfcbc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfcbc-121">-InputObject</span></span>
<span data-ttu-id="cfcbc-122">Objeto AuthorizationRule do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfcbc-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="cfcbc-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfcbc-123">-Name</span></span>
<span data-ttu-id="cfcbc-124">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cfcbc-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="cfcbc-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cfcbc-125">-Namespace</span></span>
<span data-ttu-id="cfcbc-126">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="cfcbc-126">Namespace Name</span></span>

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

### <span data-ttu-id="cfcbc-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="cfcbc-127">-Queue</span></span>
<span data-ttu-id="cfcbc-128">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="cfcbc-128">Queue Name</span></span>

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

### <span data-ttu-id="cfcbc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfcbc-129">-ResourceGroupName</span></span>
<span data-ttu-id="cfcbc-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cfcbc-130">Resource Group Name</span></span>

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

### <span data-ttu-id="cfcbc-131">-Direitos</span><span class="sxs-lookup"><span data-stu-id="cfcbc-131">-Rights</span></span>
<span data-ttu-id="cfcbc-132">Direitos, por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="cfcbc-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="cfcbc-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="cfcbc-133">-Topic</span></span>
<span data-ttu-id="cfcbc-134">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="cfcbc-134">Topic Name</span></span>

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

### <span data-ttu-id="cfcbc-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cfcbc-135">-Confirm</span></span>
<span data-ttu-id="cfcbc-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfcbc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfcbc-137">-WhatIf</span></span>
<span data-ttu-id="cfcbc-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfcbc-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfcbc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfcbc-140">CommonParameters</span></span>
<span data-ttu-id="cfcbc-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfcbc-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfcbc-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfcbc-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfcbc-143">INPUTS</span></span>

### <span data-ttu-id="cfcbc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cfcbc-144">System.String</span></span>

### <span data-ttu-id="cfcbc-145">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cfcbc-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="cfcbc-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="cfcbc-146">System.String[]</span></span>

## <span data-ttu-id="cfcbc-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfcbc-147">OUTPUTS</span></span>

### <span data-ttu-id="cfcbc-148">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cfcbc-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cfcbc-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfcbc-149">NOTES</span></span>

## <span data-ttu-id="cfcbc-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfcbc-150">RELATED LINKS</span></span>
