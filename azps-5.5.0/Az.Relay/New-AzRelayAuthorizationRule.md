---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118147"
---
# <span data-ttu-id="25ed4-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="25ed4-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="25ed4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="25ed4-103">Cria uma nova regra de autorização para as entidades de Retransmissão especificadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="25ed4-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="25ed4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25ed4-104">SYNTAX</span></span>

### <span data-ttu-id="25ed4-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25ed4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25ed4-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="25ed4-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25ed4-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="25ed4-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25ed4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="25ed4-108">DESCRIPTION</span></span>
<span data-ttu-id="25ed4-109">O cmdlet **New-AzRelayAuthorizationRule** cria uma nova regra de autorização para as entidades de Relay especificadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="25ed4-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="25ed4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25ed4-110">EXAMPLES</span></span>

### <span data-ttu-id="25ed4-111">Exemplo 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="25ed4-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="25ed4-112">Cria `AuthoRule1` com os **direitos** de Ouvir para o `TestNameSpace-Relay1` namespace.</span><span class="sxs-lookup"><span data-stu-id="25ed4-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="25ed4-113">Exemplo 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="25ed4-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="25ed4-114">Cria uma regra de `AuthoRule1` autorização **com** direitos de ouvir para o WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="25ed4-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="25ed4-115">Exemplo 3: Conexão Híbrida</span><span class="sxs-lookup"><span data-stu-id="25ed4-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="25ed4-116">Cria `AuthoRule1` com **direitos** de ouvir para a Conexão Híbrida. `TestHybridConnection`</span><span class="sxs-lookup"><span data-stu-id="25ed4-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="25ed4-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25ed4-117">PARAMETERS</span></span>

### <span data-ttu-id="25ed4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ed4-118">-DefaultProfile</span></span>
<span data-ttu-id="25ed4-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25ed4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25ed4-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="25ed4-120">-HybridConnection</span></span>
<span data-ttu-id="25ed4-121">Nome da Conexão Híbrida.</span><span class="sxs-lookup"><span data-stu-id="25ed4-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="25ed4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="25ed4-122">-Name</span></span>
<span data-ttu-id="25ed4-123">Nome de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="25ed4-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="25ed4-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="25ed4-124">-Namespace</span></span>
<span data-ttu-id="25ed4-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="25ed4-125">Namespace Name.</span></span>

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

### <span data-ttu-id="25ed4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ed4-126">-ResourceGroupName</span></span>
<span data-ttu-id="25ed4-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25ed4-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="25ed4-128">-Direitos</span><span class="sxs-lookup"><span data-stu-id="25ed4-128">-Rights</span></span>
<span data-ttu-id="25ed4-129">Direitos, por exemplo, "Ouvir","Enviar","Gerenciar"</span><span class="sxs-lookup"><span data-stu-id="25ed4-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="25ed4-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="25ed4-130">-WcfRelay</span></span>
<span data-ttu-id="25ed4-131">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="25ed4-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="25ed4-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="25ed4-132">-Confirm</span></span>
<span data-ttu-id="25ed4-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25ed4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ed4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ed4-134">-WhatIf</span></span>
<span data-ttu-id="25ed4-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="25ed4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25ed4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25ed4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ed4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ed4-137">CommonParameters</span></span>
<span data-ttu-id="25ed4-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25ed4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ed4-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25ed4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ed4-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="25ed4-140">INPUTS</span></span>

### <span data-ttu-id="25ed4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="25ed4-141">System.String</span></span>

### <span data-ttu-id="25ed4-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="25ed4-142">System.String[]</span></span>

## <span data-ttu-id="25ed4-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="25ed4-143">OUTPUTS</span></span>

### <span data-ttu-id="25ed4-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="25ed4-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="25ed4-145">Notas</span><span class="sxs-lookup"><span data-stu-id="25ed4-145">NOTES</span></span>

## <span data-ttu-id="25ed4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25ed4-146">RELATED LINKS</span></span>
