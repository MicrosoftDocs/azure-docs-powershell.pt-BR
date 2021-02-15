---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 4ca8156e80a827c9916def7ef749cfa9abb9389a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112654"
---
# <span data-ttu-id="b3b3f-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b3b3f-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="b3b3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b3f-103">Atualiza a descrição da regra de autorização especificada para as entidades de Retransmissão determinadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b3b3f-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b3b3f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3b3f-104">SYNTAX</span></span>

### <span data-ttu-id="b3b3f-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b3b3f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b3f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3b3f-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b3f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3b3f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b3f-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b3b3f-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3b3f-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b3b3f-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3b3f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3b3f-110">DESCRIPTION</span></span>
<span data-ttu-id="b3b3f-111">O cmdlet **Set-AzRelayAuthorizationRule** atualiza a descrição da regra de autorização especificada das entidades de Relay determinadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b3b3f-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b3b3f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b3b3f-112">EXAMPLES</span></span>

### <span data-ttu-id="b3b3f-113">Exemplo 1.1 - Namespace com InputObject</span><span class="sxs-lookup"><span data-stu-id="b3b3f-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="b3b3f-114">Adiciona **Enviar** a partir dos direitos de acesso da regra de autorização `AuthoRule1` no `TestNameSpace-Relay1` namespace.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="b3b3f-115">Exemplo 1.2 - Namespace with Rights parameter</span><span class="sxs-lookup"><span data-stu-id="b3b3f-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="b3b3f-116">Adiciona **Enviar** a partir dos direitos de acesso da regra de autorização `AuthoRule1` no `TestNameSpace-Relay1` namespace.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="b3b3f-117">Exemplo 2.1 - WcfRelay com InputObject</span><span class="sxs-lookup"><span data-stu-id="b3b3f-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="b3b3f-118">Adiciona **Enviar** aos direitos de acesso da regra de `AuthoRule1` autorização do WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="b3b3f-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="b3b3f-119">Exemplo 2.2 - Parâmetro WcfRelay com Direitos</span><span class="sxs-lookup"><span data-stu-id="b3b3f-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="b3b3f-120">Adiciona **Enviar** aos direitos de acesso da regra de `AuthoRule1` autorização do WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="b3b3f-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="b3b3f-121">Exemplo 3.1 - HybridConnection com InputObject</span><span class="sxs-lookup"><span data-stu-id="b3b3f-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="b3b3f-122">Adiciona **Enviar** aos direitos de acesso da regra de `AuthoRule1` autorização da HybridConnection. `TestHybridConnection`</span><span class="sxs-lookup"><span data-stu-id="b3b3f-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="b3b3f-123">Exemplo 3.2 - Parâmetro HybridConnection with Rights</span><span class="sxs-lookup"><span data-stu-id="b3b3f-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="b3b3f-124">Adiciona **Enviar** aos direitos de acesso da regra de `AuthoRule1` autorização da HybridConnection. `TestHybridConnection`</span><span class="sxs-lookup"><span data-stu-id="b3b3f-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="b3b3f-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3b3f-125">PARAMETERS</span></span>

### <span data-ttu-id="b3b3f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b3f-126">-DefaultProfile</span></span>
<span data-ttu-id="b3b3f-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3b3f-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b3b3f-128">-HybridConnection</span></span>
<span data-ttu-id="b3b3f-129">Nome da Conexão Híbrida.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-129">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b3f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3b3f-130">-InputObject</span></span>
<span data-ttu-id="b3b3f-131">Objeto Relay AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b3f-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3b3f-132">-Name</span></span>
<span data-ttu-id="b3b3f-133">Nome de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b3f-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b3b3f-134">-Namespace</span></span>
<span data-ttu-id="b3b3f-135">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-135">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b3f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b3f-136">-ResourceGroupName</span></span>
<span data-ttu-id="b3b3f-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="b3b3f-138">-Direitos</span><span class="sxs-lookup"><span data-stu-id="b3b3f-138">-Rights</span></span>
<span data-ttu-id="b3b3f-139">Direitos, por exemplo, @("Ouvir";"Enviar";"Gerenciar")</span><span class="sxs-lookup"><span data-stu-id="b3b3f-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b3f-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b3b3f-140">-WcfRelay</span></span>
<span data-ttu-id="b3b3f-141">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-141">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b3f-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b3b3f-142">-Confirm</span></span>
<span data-ttu-id="b3b3f-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3b3f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b3f-144">-WhatIf</span></span>
<span data-ttu-id="b3b3f-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3b3f-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3b3f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b3f-147">CommonParameters</span></span>
<span data-ttu-id="b3b3f-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b3f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b3f-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3b3f-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b3f-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="b3b3f-150">INPUTS</span></span>

### <span data-ttu-id="b3b3f-151">System.String</span><span class="sxs-lookup"><span data-stu-id="b3b3f-151">System.String</span></span>

### <span data-ttu-id="b3b3f-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b3b3f-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="b3b3f-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b3b3f-153">System.String[]</span></span>

## <span data-ttu-id="b3b3f-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="b3b3f-154">OUTPUTS</span></span>

### <span data-ttu-id="b3b3f-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b3b3f-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b3b3f-156">Notas</span><span class="sxs-lookup"><span data-stu-id="b3b3f-156">NOTES</span></span>

## <span data-ttu-id="b3b3f-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3b3f-157">RELATED LINKS</span></span>
