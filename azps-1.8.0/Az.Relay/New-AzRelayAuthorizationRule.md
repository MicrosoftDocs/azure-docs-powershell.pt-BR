---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: dbfecc8eaca271cf025f84a3f042684075ee98b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599507"
---
# <span data-ttu-id="3a262-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3a262-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="3a262-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a262-102">SYNOPSIS</span></span>
<span data-ttu-id="3a262-103">Cria uma nova regra de autorização para as entidades de retransmissão especificadas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3a262-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3a262-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a262-104">SYNTAX</span></span>

### <span data-ttu-id="3a262-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3a262-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a262-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a262-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a262-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a262-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a262-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a262-108">DESCRIPTION</span></span>
<span data-ttu-id="3a262-109">O cmdlet **New-AzRelayAuthorizationRule** cria uma nova regra de autorização para as entidades de retransmissão especificadas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3a262-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3a262-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a262-110">EXAMPLES</span></span>

### <span data-ttu-id="3a262-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="3a262-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="3a262-112">Cria `AuthoRule1` com direitos de **escuta** para o namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="3a262-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="3a262-113">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3a262-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="3a262-114">Cria uma regra `AuthoRule1` de autorização com direitos de **escuta** para o WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="3a262-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="3a262-115">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3a262-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="3a262-116">Cria `AuthoRule1` com direitos de **escuta** para a conexão híbrida `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="3a262-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="3a262-117">OS</span><span class="sxs-lookup"><span data-stu-id="3a262-117">PARAMETERS</span></span>

### <span data-ttu-id="3a262-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a262-118">-DefaultProfile</span></span>
<span data-ttu-id="3a262-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a262-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a262-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3a262-120">-HybridConnection</span></span>
<span data-ttu-id="3a262-121">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="3a262-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="3a262-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a262-122">-Name</span></span>
<span data-ttu-id="3a262-123">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="3a262-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3a262-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3a262-124">-Namespace</span></span>
<span data-ttu-id="3a262-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="3a262-125">Namespace Name.</span></span>

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

### <span data-ttu-id="3a262-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a262-126">-ResourceGroupName</span></span>
<span data-ttu-id="3a262-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a262-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="3a262-128">-Direitos</span><span class="sxs-lookup"><span data-stu-id="3a262-128">-Rights</span></span>
<span data-ttu-id="3a262-129">Direitos, como "escutar", "enviar", "gerenciar"</span><span class="sxs-lookup"><span data-stu-id="3a262-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="3a262-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3a262-130">-WcfRelay</span></span>
<span data-ttu-id="3a262-131">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="3a262-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="3a262-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a262-132">-Confirm</span></span>
<span data-ttu-id="3a262-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a262-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a262-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a262-134">-WhatIf</span></span>
<span data-ttu-id="3a262-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a262-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a262-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a262-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a262-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a262-137">CommonParameters</span></span>
<span data-ttu-id="3a262-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a262-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a262-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a262-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a262-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a262-140">INPUTS</span></span>

### <span data-ttu-id="3a262-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3a262-141">System.String</span></span>

### <span data-ttu-id="3a262-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="3a262-142">System.String[]</span></span>

## <span data-ttu-id="3a262-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a262-143">OUTPUTS</span></span>

### <span data-ttu-id="3a262-144">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3a262-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3a262-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a262-145">NOTES</span></span>

## <span data-ttu-id="3a262-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a262-146">RELATED LINKS</span></span>
