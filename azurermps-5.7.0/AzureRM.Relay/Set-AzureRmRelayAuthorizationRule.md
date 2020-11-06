---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 91f37ad2ed49b4c1bd39306be803776ddce9ecff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439828"
---
# <span data-ttu-id="334df-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="334df-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="334df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="334df-102">SYNOPSIS</span></span>
<span data-ttu-id="334df-103">Atualiza a descrição da regra de autorização especificada para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="334df-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="334df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="334df-104">SYNTAX</span></span>

### <span data-ttu-id="334df-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="334df-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334df-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="334df-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334df-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="334df-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334df-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="334df-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="334df-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="334df-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="334df-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="334df-110">DESCRIPTION</span></span>
<span data-ttu-id="334df-111">O cmdlet **set-AzureRmRelayAuthorizationRule** atualiza a descrição da regra de autorização especificada das entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="334df-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="334df-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="334df-112">EXAMPLES</span></span>

### <span data-ttu-id="334df-113">Exemplo 1,1-namespace com InputObject</span><span class="sxs-lookup"><span data-stu-id="334df-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="334df-114">Adiciona **Enviar** dos direitos de acesso da regra de autorização `AuthoRule1` no namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="334df-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="334df-115">Exemplo 1,2-namespace com parâmetro de direitos</span><span class="sxs-lookup"><span data-stu-id="334df-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="334df-116">Adiciona **Enviar** dos direitos de acesso da regra de autorização `AuthoRule1` no namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="334df-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="334df-117">Exemplo 2,1-WcfRelay com InputObject</span><span class="sxs-lookup"><span data-stu-id="334df-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="334df-118">Adiciona **Enviar** aos direitos de acesso da regra de autorização `AuthoRule1` da WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="334df-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="334df-119">Exemplo 2,2-WcfRelay com o parâmetro Rights</span><span class="sxs-lookup"><span data-stu-id="334df-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="334df-120">Adiciona **Enviar** aos direitos de acesso da regra de autorização `AuthoRule1` da WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="334df-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="334df-121">Exemplo 3,1-HybridConnection com InputObject</span><span class="sxs-lookup"><span data-stu-id="334df-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="334df-122">Adiciona **Enviar** aos direitos de acesso da regra de autorização `AuthoRule1` da HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="334df-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="334df-123">Exemplo 3,2-HybridConnection com o parâmetro Rights</span><span class="sxs-lookup"><span data-stu-id="334df-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="334df-124">Adiciona **Enviar** aos direitos de acesso da regra de autorização `AuthoRule1` da HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="334df-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="334df-125">OS</span><span class="sxs-lookup"><span data-stu-id="334df-125">PARAMETERS</span></span>

### <span data-ttu-id="334df-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="334df-126">-DefaultProfile</span></span>
<span data-ttu-id="334df-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="334df-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334df-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="334df-128">-HybridConnection</span></span>
<span data-ttu-id="334df-129">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="334df-129">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="334df-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="334df-130">-InputObject</span></span>
<span data-ttu-id="334df-131">Retransmitir objeto AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="334df-131">Relay AuthorizationRule Object</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334df-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="334df-132">-Name</span></span>
<span data-ttu-id="334df-133">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="334df-133">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="334df-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="334df-134">-Namespace</span></span>
<span data-ttu-id="334df-135">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="334df-135">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="334df-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="334df-136">-ResourceGroupName</span></span>
<span data-ttu-id="334df-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="334df-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="334df-138">-Direitos</span><span class="sxs-lookup"><span data-stu-id="334df-138">-Rights</span></span>
<span data-ttu-id="334df-139">Direitos, por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="334df-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334df-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="334df-140">-WcfRelay</span></span>
<span data-ttu-id="334df-141">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="334df-141">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="334df-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="334df-142">-Confirm</span></span>
<span data-ttu-id="334df-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="334df-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="334df-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="334df-144">-WhatIf</span></span>
<span data-ttu-id="334df-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="334df-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="334df-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="334df-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="334df-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334df-147">CommonParameters</span></span>
<span data-ttu-id="334df-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="334df-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334df-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="334df-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334df-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="334df-150">INPUTS</span></span>

### <span data-ttu-id="334df-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="334df-151">-ResourceGroupName</span></span>
 <span data-ttu-id="334df-152">System. String</span><span class="sxs-lookup"><span data-stu-id="334df-152">System.String</span></span> 

### <span data-ttu-id="334df-153">-Namespace</span><span class="sxs-lookup"><span data-stu-id="334df-153">-Namespace</span></span>
 <span data-ttu-id="334df-154">System. String</span><span class="sxs-lookup"><span data-stu-id="334df-154">System.String</span></span> 
 

### <span data-ttu-id="334df-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="334df-155">-WcfRelay</span></span>
 <span data-ttu-id="334df-156">System. String</span><span class="sxs-lookup"><span data-stu-id="334df-156">System.String</span></span> 

### <span data-ttu-id="334df-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="334df-157">-HybridConnection</span></span>
 <span data-ttu-id="334df-158">System. String</span><span class="sxs-lookup"><span data-stu-id="334df-158">System.String</span></span> 
 

### <span data-ttu-id="334df-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="334df-159">-Name</span></span>
 <span data-ttu-id="334df-160">System. String</span><span class="sxs-lookup"><span data-stu-id="334df-160">System.String</span></span>

### <span data-ttu-id="334df-161">-InputObject</span><span class="sxs-lookup"><span data-stu-id="334df-161">-InputObject</span></span>
 <span data-ttu-id="334df-162">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="334df-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="334df-163">-Direitos</span><span class="sxs-lookup"><span data-stu-id="334df-163">-Rights</span></span>
 <span data-ttu-id="334df-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="334df-164">System.String []</span></span>

## <span data-ttu-id="334df-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="334df-165">OUTPUTS</span></span>

### <span data-ttu-id="334df-166">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="334df-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="334df-167">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="334df-167">Example 1 - Namespace</span></span>
<span data-ttu-id="334df-168">Direitos: {Listen, Send} Name: AuthoRule1 tipo: Microsoft. rerelay/ID do AuthorizationRules:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="334df-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="334df-169">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="334df-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="334df-170">Direitos: {Listen, Send} Name: AuthoRule1 tipo: Microsoft. rerelay/ID do AuthorizationRules:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="334df-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="334df-171">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="334df-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="334df-172">Direitos: {Listen, Send} Name: AuthoRule1 tipo: Microsoft. rerelay/ID do AuthorizationRules:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="334df-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="334df-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="334df-173">NOTES</span></span>

## <span data-ttu-id="334df-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="334df-174">RELATED LINKS</span></span>

