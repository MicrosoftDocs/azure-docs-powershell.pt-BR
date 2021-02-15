---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: da981d38f0833adc276a114c42def5d19322e0d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116180"
---
# <span data-ttu-id="27dbb-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="27dbb-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="27dbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="27dbb-103">Atualiza a descrição da regra de autorização especificada para o namespace ou fila ou tópico do Service Bus.</span><span class="sxs-lookup"><span data-stu-id="27dbb-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="27dbb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27dbb-104">SYNTAX</span></span>

### <span data-ttu-id="27dbb-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="27dbb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dbb-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="27dbb-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dbb-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="27dbb-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dbb-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27dbb-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27dbb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="27dbb-109">DESCRIPTION</span></span>
<span data-ttu-id="27dbb-110">O cmdlet **Set-AzServiceBusAuthorizationRule** atualiza a descrição da regra de autorização especificada no namespace ou fila ou tópico do Service Bus.</span><span class="sxs-lookup"><span data-stu-id="27dbb-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="27dbb-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="27dbb-111">EXAMPLES</span></span>

### <span data-ttu-id="27dbb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="27dbb-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="27dbb-113">Remove Gerenciar **dos** direitos de acesso da regra de autorização `AuthoRule1` no `SB-Example1` namespace.</span><span class="sxs-lookup"><span data-stu-id="27dbb-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="27dbb-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="27dbb-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="27dbb-115">Remove Gerenciar **dos** direitos de acesso da regra de autorização `AuthoRule1` na `SBQueue` fila.</span><span class="sxs-lookup"><span data-stu-id="27dbb-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="27dbb-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="27dbb-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="27dbb-117">Remove Gerenciar **dos** direitos de acesso da regra de autorização `AuthoRule1` no `SBTopic` tópico.</span><span class="sxs-lookup"><span data-stu-id="27dbb-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="27dbb-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27dbb-118">PARAMETERS</span></span>

### <span data-ttu-id="27dbb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27dbb-119">-DefaultProfile</span></span>
<span data-ttu-id="27dbb-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27dbb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27dbb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27dbb-121">-InputObject</span></span>
<span data-ttu-id="27dbb-122">Objeto ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="27dbb-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="27dbb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="27dbb-123">-Name</span></span>
<span data-ttu-id="27dbb-124">Nome de AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="27dbb-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="27dbb-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="27dbb-125">-Namespace</span></span>
<span data-ttu-id="27dbb-126">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="27dbb-126">Namespace Name</span></span>

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

### <span data-ttu-id="27dbb-127">-Fila</span><span class="sxs-lookup"><span data-stu-id="27dbb-127">-Queue</span></span>
<span data-ttu-id="27dbb-128">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="27dbb-128">Queue Name</span></span>

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

### <span data-ttu-id="27dbb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27dbb-129">-ResourceGroupName</span></span>
<span data-ttu-id="27dbb-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="27dbb-130">Resource Group Name</span></span>

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

### <span data-ttu-id="27dbb-131">-Direitos</span><span class="sxs-lookup"><span data-stu-id="27dbb-131">-Rights</span></span>
<span data-ttu-id="27dbb-132">Direitos, por exemplo, @("Ouvir";"Enviar";"Gerenciar")</span><span class="sxs-lookup"><span data-stu-id="27dbb-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="27dbb-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="27dbb-133">-Topic</span></span>
<span data-ttu-id="27dbb-134">Nome do Tópico</span><span class="sxs-lookup"><span data-stu-id="27dbb-134">Topic Name</span></span>

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

### <span data-ttu-id="27dbb-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="27dbb-135">-Confirm</span></span>
<span data-ttu-id="27dbb-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27dbb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27dbb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27dbb-137">-WhatIf</span></span>
<span data-ttu-id="27dbb-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="27dbb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27dbb-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27dbb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27dbb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27dbb-140">CommonParameters</span></span>
<span data-ttu-id="27dbb-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27dbb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27dbb-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27dbb-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27dbb-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="27dbb-143">INPUTS</span></span>

### <span data-ttu-id="27dbb-144">System.String</span><span class="sxs-lookup"><span data-stu-id="27dbb-144">System.String</span></span>

### <span data-ttu-id="27dbb-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="27dbb-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="27dbb-146">System.String[]</span><span class="sxs-lookup"><span data-stu-id="27dbb-146">System.String[]</span></span>

## <span data-ttu-id="27dbb-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="27dbb-147">OUTPUTS</span></span>

### <span data-ttu-id="27dbb-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="27dbb-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="27dbb-149">Notas</span><span class="sxs-lookup"><span data-stu-id="27dbb-149">NOTES</span></span>

## <span data-ttu-id="27dbb-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27dbb-150">RELATED LINKS</span></span>
