---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: ed95b9aa2e914d8f7c37132c372c4c1acaeafca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773384"
---
# <span data-ttu-id="1585b-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1585b-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="1585b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1585b-102">SYNOPSIS</span></span>
<span data-ttu-id="1585b-103">Atualiza a descrição da regra de autorização especificada para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1585b-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1585b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1585b-104">SYNTAX</span></span>

### <span data-ttu-id="1585b-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1585b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1585b-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1585b-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1585b-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1585b-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1585b-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1585b-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1585b-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1585b-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1585b-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1585b-110">DESCRIPTION</span></span>
<span data-ttu-id="1585b-111">O cmdlet **set-AzRelayAuthorizationRule** atualiza a descrição da regra de autorização especificada das entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1585b-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1585b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1585b-112">EXAMPLES</span></span>

### <span data-ttu-id="1585b-113">Exemplo 1,1-namespace com InputObject</span><span class="sxs-lookup"><span data-stu-id="1585b-113">Example 1.1 - Namespace with InputObject</span></span>
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

<span data-ttu-id="1585b-114">Adiciona **Enviar** dos direitos de acesso da regra de autorização `AuthoRule1` no namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="1585b-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="1585b-115">Exemplo 1,2-namespace com parâmetro de direitos</span><span class="sxs-lookup"><span data-stu-id="1585b-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="1585b-116">Adiciona **Enviar** dos direitos de acesso da regra de autorização `AuthoRule1` no namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="1585b-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="1585b-117">Exemplo 2,1-WcfRelay com InputObject</span><span class="sxs-lookup"><span data-stu-id="1585b-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="1585b-118">Adiciona **Enviar** aos direitos de acesso da regra de autorização `AuthoRule1` da WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="1585b-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="1585b-119">Exemplo 2,2-WcfRelay com o parâmetro Rights</span><span class="sxs-lookup"><span data-stu-id="1585b-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="1585b-120">Adiciona **Enviar** aos direitos de acesso da regra de autorização `AuthoRule1` da WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="1585b-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="1585b-121">Exemplo 3,1-HybridConnection com InputObject</span><span class="sxs-lookup"><span data-stu-id="1585b-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="1585b-122">Adiciona **Enviar** aos direitos de acesso da regra de autorização `AuthoRule1` da HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="1585b-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="1585b-123">Exemplo 3,2-HybridConnection com o parâmetro Rights</span><span class="sxs-lookup"><span data-stu-id="1585b-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="1585b-124">Adiciona **Enviar** aos direitos de acesso da regra de autorização `AuthoRule1` da HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="1585b-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="1585b-125">OS</span><span class="sxs-lookup"><span data-stu-id="1585b-125">PARAMETERS</span></span>

### <span data-ttu-id="1585b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1585b-126">-DefaultProfile</span></span>
<span data-ttu-id="1585b-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1585b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1585b-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1585b-128">-HybridConnection</span></span>
<span data-ttu-id="1585b-129">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="1585b-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="1585b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1585b-130">-InputObject</span></span>
<span data-ttu-id="1585b-131">Retransmitir objeto AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="1585b-131">Relay AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="1585b-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="1585b-132">-Name</span></span>
<span data-ttu-id="1585b-133">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="1585b-133">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="1585b-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1585b-134">-Namespace</span></span>
<span data-ttu-id="1585b-135">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="1585b-135">Namespace Name.</span></span>

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

### <span data-ttu-id="1585b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1585b-136">-ResourceGroupName</span></span>
<span data-ttu-id="1585b-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1585b-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="1585b-138">-Direitos</span><span class="sxs-lookup"><span data-stu-id="1585b-138">-Rights</span></span>
<span data-ttu-id="1585b-139">Direitos, por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="1585b-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="1585b-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1585b-140">-WcfRelay</span></span>
<span data-ttu-id="1585b-141">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="1585b-141">WcfRelay Name.</span></span>

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

### <span data-ttu-id="1585b-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1585b-142">-Confirm</span></span>
<span data-ttu-id="1585b-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1585b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1585b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1585b-144">-WhatIf</span></span>
<span data-ttu-id="1585b-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1585b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1585b-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1585b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1585b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1585b-147">CommonParameters</span></span>
<span data-ttu-id="1585b-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1585b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1585b-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1585b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1585b-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1585b-150">INPUTS</span></span>

### <span data-ttu-id="1585b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1585b-151">System.String</span></span>

### <span data-ttu-id="1585b-152">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1585b-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="1585b-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="1585b-153">System.String[]</span></span>

## <span data-ttu-id="1585b-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1585b-154">OUTPUTS</span></span>

### <span data-ttu-id="1585b-155">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1585b-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1585b-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1585b-156">NOTES</span></span>

## <span data-ttu-id="1585b-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1585b-157">RELATED LINKS</span></span>
