---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118158"
---
# <span data-ttu-id="8799c-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8799c-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="8799c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8799c-102">SYNOPSIS</span></span>
<span data-ttu-id="8799c-103">Obtém a descrição de uma regra de autorização especificada para determinadas entidades relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8799c-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8799c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8799c-104">SYNTAX</span></span>

### <span data-ttu-id="8799c-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8799c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8799c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8799c-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8799c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8799c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8799c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8799c-108">DESCRIPTION</span></span>
<span data-ttu-id="8799c-109">O cmdlet **Get-AzRelayAuthorizationRule** obtém a descrição da regra de autorização especificada em determinadas entidades relay (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8799c-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8799c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8799c-110">EXAMPLES</span></span>

### <span data-ttu-id="8799c-111">Exemplo 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="8799c-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="8799c-112">Retorna a descrição da regra de autorização especificada para um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="8799c-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="8799c-113">Exemplo 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8799c-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="8799c-114">Retorna a descrição da regra de autorização especificada para um determinado WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="8799c-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="8799c-115">Exemplo 3: Conexão Híbrida</span><span class="sxs-lookup"><span data-stu-id="8799c-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="8799c-116">Retorna a descrição da regra de autorização especificada para uma determinada Conexão Híbrida.</span><span class="sxs-lookup"><span data-stu-id="8799c-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="8799c-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8799c-117">PARAMETERS</span></span>

### <span data-ttu-id="8799c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8799c-118">-DefaultProfile</span></span>
<span data-ttu-id="8799c-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8799c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8799c-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8799c-120">-HybridConnection</span></span>
<span data-ttu-id="8799c-121">Nome da Conexão Híbrida.</span><span class="sxs-lookup"><span data-stu-id="8799c-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="8799c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8799c-122">-Name</span></span>
<span data-ttu-id="8799c-123">Nome de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="8799c-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="8799c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8799c-124">-Namespace</span></span>
<span data-ttu-id="8799c-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="8799c-125">Namespace Name.</span></span>

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

### <span data-ttu-id="8799c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8799c-126">-ResourceGroupName</span></span>
<span data-ttu-id="8799c-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8799c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8799c-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8799c-128">-WcfRelay</span></span>
<span data-ttu-id="8799c-129">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="8799c-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="8799c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8799c-130">CommonParameters</span></span>
<span data-ttu-id="8799c-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8799c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8799c-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8799c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8799c-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="8799c-133">INPUTS</span></span>

### <span data-ttu-id="8799c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8799c-134">System.String</span></span>

## <span data-ttu-id="8799c-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="8799c-135">OUTPUTS</span></span>

### <span data-ttu-id="8799c-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8799c-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8799c-137">Notas</span><span class="sxs-lookup"><span data-stu-id="8799c-137">NOTES</span></span>

## <span data-ttu-id="8799c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8799c-138">RELATED LINKS</span></span>
