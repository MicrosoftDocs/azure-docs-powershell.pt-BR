---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: bed3165eee350f55470c0cbca575226e77ec9d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891732"
---
# <span data-ttu-id="d6a4f-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d6a4f-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="d6a4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a4f-103">Obtém a descrição de uma regra de autorização especificada para uma determinada entidade Relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="d6a4f-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d6a4f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d6a4f-104">SYNTAX</span></span>

### <span data-ttu-id="d6a4f-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d6a4f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6a4f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6a4f-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6a4f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6a4f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6a4f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d6a4f-108">DESCRIPTION</span></span>
<span data-ttu-id="d6a4f-109">O cmdlet **Get-AzRelayAuthorizationRule** obtém a descrição da regra de autorização especificada nas entidades Relay determinadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="d6a4f-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d6a4f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6a4f-110">EXAMPLES</span></span>

### <span data-ttu-id="d6a4f-111">Exemplo 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="d6a4f-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="d6a4f-112">Retorna a descrição da regra de autorização especificada para um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="d6a4f-113">Exemplo 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d6a4f-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="d6a4f-114">Retorna a descrição da regra de autorização especificada para um determinado WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="d6a4f-115">Exemplo 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d6a4f-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="d6a4f-116">Retorna a descrição da regra de autorização especificada para um determinado HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="d6a4f-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d6a4f-117">PARAMETERS</span></span>

### <span data-ttu-id="d6a4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a4f-118">-DefaultProfile</span></span>
<span data-ttu-id="d6a4f-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6a4f-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d6a4f-120">-HybridConnection</span></span>
<span data-ttu-id="d6a4f-121">Nome de HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="d6a4f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d6a4f-122">-Name</span></span>
<span data-ttu-id="d6a4f-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a4f-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d6a4f-124">-Namespace</span></span>
<span data-ttu-id="d6a4f-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-125">Namespace Name.</span></span>

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

### <span data-ttu-id="d6a4f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a4f-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6a4f-127">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="d6a4f-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d6a4f-128">-WcfRelay</span></span>
<span data-ttu-id="d6a4f-129">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="d6a4f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a4f-130">CommonParameters</span></span>
<span data-ttu-id="d6a4f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a4f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a4f-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a4f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a4f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6a4f-133">INPUTS</span></span>

### <span data-ttu-id="d6a4f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d6a4f-134">System.String</span></span>

## <span data-ttu-id="d6a4f-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d6a4f-135">OUTPUTS</span></span>

### <span data-ttu-id="d6a4f-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d6a4f-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d6a4f-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="d6a4f-137">NOTES</span></span>

## <span data-ttu-id="d6a4f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6a4f-138">RELATED LINKS</span></span>
