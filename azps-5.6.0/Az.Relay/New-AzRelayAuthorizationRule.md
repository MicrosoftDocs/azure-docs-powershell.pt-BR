---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: d0faea052141420db88f58fd6513c2d6822f56c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891723"
---
# <span data-ttu-id="9dd5c-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9dd5c-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="9dd5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd5c-103">Cria uma nova regra de autorização para as entidades relay especificadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="9dd5c-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9dd5c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9dd5c-104">SYNTAX</span></span>

### <span data-ttu-id="9dd5c-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9dd5c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dd5c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9dd5c-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dd5c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9dd5c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dd5c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9dd5c-108">DESCRIPTION</span></span>
<span data-ttu-id="9dd5c-109">O cmdlet **New-AzRelayAuthorizationRule** cria uma nova regra de autorização para as entidades de Retransmissão especificadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="9dd5c-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9dd5c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9dd5c-110">EXAMPLES</span></span>

### <span data-ttu-id="9dd5c-111">Exemplo 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="9dd5c-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="9dd5c-112">Cria `AuthoRule1` com **Direitos** de Escuta para o namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="9dd5c-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="9dd5c-113">Exemplo 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9dd5c-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="9dd5c-114">Cria uma regra de `AuthoRule1` autorização **com direitos** de escuta para o WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="9dd5c-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="9dd5c-115">Exemplo 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9dd5c-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="9dd5c-116">Cria `AuthoRule1` com **Direitos** de Escuta para a Conexão Híbrida `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="9dd5c-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="9dd5c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9dd5c-117">PARAMETERS</span></span>

### <span data-ttu-id="9dd5c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd5c-118">-DefaultProfile</span></span>
<span data-ttu-id="9dd5c-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dd5c-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9dd5c-120">-HybridConnection</span></span>
<span data-ttu-id="9dd5c-121">Nome de HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="9dd5c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9dd5c-122">-Name</span></span>
<span data-ttu-id="9dd5c-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9dd5c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9dd5c-124">-Namespace</span></span>
<span data-ttu-id="9dd5c-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-125">Namespace Name.</span></span>

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

### <span data-ttu-id="9dd5c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd5c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9dd5c-127">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="9dd5c-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="9dd5c-128">-Rights</span></span>
<span data-ttu-id="9dd5c-129">Direitos, por exemplo, "Listen","Send","Manage"</span><span class="sxs-lookup"><span data-stu-id="9dd5c-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd5c-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9dd5c-130">-WcfRelay</span></span>
<span data-ttu-id="9dd5c-131">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="9dd5c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dd5c-132">-Confirm</span></span>
<span data-ttu-id="9dd5c-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dd5c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd5c-134">-WhatIf</span></span>
<span data-ttu-id="9dd5c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dd5c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dd5c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd5c-137">CommonParameters</span></span>
<span data-ttu-id="9dd5c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd5c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd5c-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dd5c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd5c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dd5c-140">INPUTS</span></span>

### <span data-ttu-id="9dd5c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9dd5c-141">System.String</span></span>

### <span data-ttu-id="9dd5c-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9dd5c-142">System.String[]</span></span>

## <span data-ttu-id="9dd5c-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9dd5c-143">OUTPUTS</span></span>

### <span data-ttu-id="9dd5c-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9dd5c-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9dd5c-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="9dd5c-145">NOTES</span></span>

## <span data-ttu-id="9dd5c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dd5c-146">RELATED LINKS</span></span>
