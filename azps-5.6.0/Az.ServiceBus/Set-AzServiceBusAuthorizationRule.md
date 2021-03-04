---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 4e28f829a9daa17d5d6f44af10f21e8dc3b1f929
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901562"
---
# <span data-ttu-id="d2015-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d2015-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="d2015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2015-102">SYNOPSIS</span></span>
<span data-ttu-id="d2015-103">Atualiza a descrição da regra de autorização especificada para o namespace ou fila ou tópico do Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="d2015-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="d2015-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2015-104">SYNTAX</span></span>

### <span data-ttu-id="d2015-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2015-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2015-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2015-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2015-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2015-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2015-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d2015-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2015-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2015-109">DESCRIPTION</span></span>
<span data-ttu-id="d2015-110">O cmdlet **Set-AzServiceBusAuthorizationRule** atualiza a descrição da regra de autorização especificada no namespace ou fila ou tópico do Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="d2015-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="d2015-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2015-111">EXAMPLES</span></span>

### <span data-ttu-id="d2015-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2015-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="d2015-113">Remove Gerenciar **dos** direitos de acesso da regra de autorização `AuthoRule1` no namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="d2015-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="d2015-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d2015-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="d2015-115">Remove Gerenciar **dos** direitos de acesso da regra de autorização `AuthoRule1` na fila `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="d2015-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="d2015-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d2015-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="d2015-117">Remove **Gerenciar dos** direitos de acesso da regra de autorização `AuthoRule1` no tópico `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="d2015-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="d2015-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2015-118">PARAMETERS</span></span>

### <span data-ttu-id="d2015-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2015-119">-DefaultProfile</span></span>
<span data-ttu-id="d2015-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2015-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2015-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2015-121">-InputObject</span></span>
<span data-ttu-id="d2015-122">Objeto ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d2015-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="d2015-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d2015-123">-Name</span></span>
<span data-ttu-id="d2015-124">Nome authorizationRule</span><span class="sxs-lookup"><span data-stu-id="d2015-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="d2015-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d2015-125">-Namespace</span></span>
<span data-ttu-id="d2015-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d2015-126">Namespace Name</span></span>

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

### <span data-ttu-id="d2015-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="d2015-127">-Queue</span></span>
<span data-ttu-id="d2015-128">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="d2015-128">Queue Name</span></span>

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

### <span data-ttu-id="d2015-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2015-129">-ResourceGroupName</span></span>
<span data-ttu-id="d2015-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d2015-130">Resource Group Name</span></span>

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

### <span data-ttu-id="d2015-131">-Rights</span><span class="sxs-lookup"><span data-stu-id="d2015-131">-Rights</span></span>
<span data-ttu-id="d2015-132">Direitos, por exemplo, @("Listen","Send","Manage")</span><span class="sxs-lookup"><span data-stu-id="d2015-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="d2015-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="d2015-133">-Topic</span></span>
<span data-ttu-id="d2015-134">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="d2015-134">Topic Name</span></span>

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

### <span data-ttu-id="d2015-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2015-135">-Confirm</span></span>
<span data-ttu-id="d2015-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2015-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2015-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2015-137">-WhatIf</span></span>
<span data-ttu-id="d2015-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2015-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2015-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2015-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2015-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2015-140">CommonParameters</span></span>
<span data-ttu-id="d2015-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2015-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2015-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2015-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2015-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2015-143">INPUTS</span></span>

### <span data-ttu-id="d2015-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d2015-144">System.String</span></span>

### <span data-ttu-id="d2015-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d2015-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="d2015-146">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d2015-146">System.String[]</span></span>

## <span data-ttu-id="d2015-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2015-147">OUTPUTS</span></span>

### <span data-ttu-id="d2015-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d2015-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d2015-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2015-149">NOTES</span></span>

## <span data-ttu-id="d2015-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2015-150">RELATED LINKS</span></span>
