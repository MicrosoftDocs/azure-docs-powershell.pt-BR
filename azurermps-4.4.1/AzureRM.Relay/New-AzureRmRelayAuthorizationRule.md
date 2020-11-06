---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 9e4eecad543346efa60dfb0b9a20e31c47a59036
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429137"
---
# <span data-ttu-id="b0f06-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b0f06-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="b0f06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0f06-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f06-103">Cria uma nova regra de autorização para as entidades de retransmissão especificadas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b0f06-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0f06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0f06-104">SYNTAX</span></span>

### <span data-ttu-id="b0f06-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0f06-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0f06-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b0f06-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0f06-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b0f06-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0f06-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0f06-108">DESCRIPTION</span></span>
<span data-ttu-id="b0f06-109">O cmdlet **New-AzureRmRelayAuthorizationRule** cria uma nova regra de autorização para as entidades de retransmissão especificadas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b0f06-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b0f06-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0f06-110">EXAMPLES</span></span>

### <span data-ttu-id="b0f06-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="b0f06-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="b0f06-112">Cria `AuthoRule1` com direitos de **escuta** para o namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b0f06-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="b0f06-113">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b0f06-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="b0f06-114">Cria uma regra `AuthoRule1` de autorização com direitos de **escuta** para o WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="b0f06-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="b0f06-115">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b0f06-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="b0f06-116">Cria `AuthoRule1` com direitos de **escuta** para o namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b0f06-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="b0f06-117">OS</span><span class="sxs-lookup"><span data-stu-id="b0f06-117">PARAMETERS</span></span>

### <span data-ttu-id="b0f06-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0f06-118">-Confirm</span></span>
<span data-ttu-id="b0f06-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0f06-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0f06-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b0f06-120">-HybridConnection</span></span>
<span data-ttu-id="b0f06-121">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="b0f06-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="b0f06-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0f06-122">-Name</span></span>
<span data-ttu-id="b0f06-123">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b0f06-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b0f06-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b0f06-124">-Namespace</span></span>
<span data-ttu-id="b0f06-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="b0f06-125">Namespace Name.</span></span>

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

### <span data-ttu-id="b0f06-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f06-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0f06-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0f06-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0f06-128">-Direitos</span><span class="sxs-lookup"><span data-stu-id="b0f06-128">-Rights</span></span>
<span data-ttu-id="b0f06-129">Direitos, como "escutar", "enviar", "gerenciar"</span><span class="sxs-lookup"><span data-stu-id="b0f06-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f06-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b0f06-130">-WcfRelay</span></span>
<span data-ttu-id="b0f06-131">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="b0f06-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b0f06-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f06-132">-WhatIf</span></span>
<span data-ttu-id="b0f06-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0f06-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0f06-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0f06-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0f06-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f06-135">-DefaultProfile</span></span>
<span data-ttu-id="b0f06-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0f06-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0f06-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f06-137">CommonParameters</span></span>
<span data-ttu-id="b0f06-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f06-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f06-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0f06-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f06-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0f06-140">INPUTS</span></span>

### <span data-ttu-id="b0f06-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f06-141">-ResourceGroupName</span></span>
 <span data-ttu-id="b0f06-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b0f06-142">System.String</span></span> 

### <span data-ttu-id="b0f06-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b0f06-143">-Namespace</span></span>
 <span data-ttu-id="b0f06-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b0f06-144">System.String</span></span> 
 

### <span data-ttu-id="b0f06-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b0f06-145">-WcfRelay</span></span>
 <span data-ttu-id="b0f06-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b0f06-146">System.String</span></span> 

### <span data-ttu-id="b0f06-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b0f06-147">-HybridConnection</span></span>
 <span data-ttu-id="b0f06-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b0f06-148">System.String</span></span> 
 

### <span data-ttu-id="b0f06-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0f06-149">-Name</span></span>
 <span data-ttu-id="b0f06-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b0f06-150">System.String</span></span>
 

### <span data-ttu-id="b0f06-151">-Direitos</span><span class="sxs-lookup"><span data-stu-id="b0f06-151">-Rights</span></span>
 <span data-ttu-id="b0f06-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="b0f06-152">System.String []</span></span>

## <span data-ttu-id="b0f06-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0f06-153">OUTPUTS</span></span>

### <span data-ttu-id="b0f06-154">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b0f06-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="b0f06-155">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="b0f06-155">Example 1 - Namespace</span></span>
<span data-ttu-id="b0f06-156">Direitos: {Listen} nome: AuthoRule1 tipo: Microsoft. rerelay/ID do AuthorizationRules:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="b0f06-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="b0f06-157">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b0f06-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="b0f06-158">Direitos: {Listen} nome: AuthoRule1 tipo: Microsoft. rerelay/ID do AuthorizationRules:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="b0f06-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="b0f06-159">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b0f06-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="b0f06-160">Direitos: {Listen} nome: AuthoRule1 tipo: Microsoft. rerelay/ID do AuthorizationRules:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="b0f06-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="b0f06-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0f06-161">NOTES</span></span>

## <span data-ttu-id="b0f06-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0f06-162">RELATED LINKS</span></span>

