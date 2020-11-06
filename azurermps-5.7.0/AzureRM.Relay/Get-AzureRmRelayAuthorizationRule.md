---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 333e3eeaaf7655c78d557eb104fa4a349a0c05e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427453"
---
# <span data-ttu-id="3ddab-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3ddab-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="3ddab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ddab-102">SYNOPSIS</span></span>
<span data-ttu-id="3ddab-103">Obtém a descrição de uma regra de autorização especificada para uma determinada entidade de retransmissão (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3ddab-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ddab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ddab-104">SYNTAX</span></span>

### <span data-ttu-id="3ddab-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3ddab-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ddab-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ddab-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ddab-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ddab-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ddab-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ddab-108">DESCRIPTION</span></span>
<span data-ttu-id="3ddab-109">O cmdlet **Get-AzureRmRelayAuthorizationRule** Obtém a descrição da regra de autorização especificada em determinadas entidades de retransmissão (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3ddab-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3ddab-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ddab-110">EXAMPLES</span></span>

### <span data-ttu-id="3ddab-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="3ddab-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="3ddab-112">Retorna a descrição da regra de autorização especificada para um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="3ddab-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="3ddab-113">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3ddab-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

<span data-ttu-id="3ddab-114">Retorna a descrição da regra de autorização especificada para um determinado WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="3ddab-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="3ddab-115">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3ddab-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="3ddab-116">Retorna a descrição da regra de autorização especificada para um determinado HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="3ddab-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="3ddab-117">OS</span><span class="sxs-lookup"><span data-stu-id="3ddab-117">PARAMETERS</span></span>

### <span data-ttu-id="3ddab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ddab-118">-DefaultProfile</span></span>
<span data-ttu-id="3ddab-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ddab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ddab-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3ddab-120">-HybridConnection</span></span>
<span data-ttu-id="3ddab-121">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="3ddab-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="3ddab-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ddab-122">-Name</span></span>
<span data-ttu-id="3ddab-123">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="3ddab-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ddab-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3ddab-124">-Namespace</span></span>
<span data-ttu-id="3ddab-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="3ddab-125">Namespace Name.</span></span>

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

### <span data-ttu-id="3ddab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ddab-126">-ResourceGroupName</span></span>
<span data-ttu-id="3ddab-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ddab-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="3ddab-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3ddab-128">-WcfRelay</span></span>
<span data-ttu-id="3ddab-129">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="3ddab-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="3ddab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ddab-130">CommonParameters</span></span>
<span data-ttu-id="3ddab-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ddab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ddab-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ddab-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ddab-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ddab-133">INPUTS</span></span>

### <span data-ttu-id="3ddab-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ddab-134">-ResourceGroupName</span></span>
 <span data-ttu-id="3ddab-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3ddab-135">System.String</span></span> 

### <span data-ttu-id="3ddab-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="3ddab-136">-NamespaceName</span></span>
 <span data-ttu-id="3ddab-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3ddab-137">System.String</span></span> 
 

### <span data-ttu-id="3ddab-138">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="3ddab-138">-HybridConnectionsName</span></span>
 <span data-ttu-id="3ddab-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3ddab-139">System.String</span></span> 

### <span data-ttu-id="3ddab-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="3ddab-140">-WcfRelayName</span></span>
 <span data-ttu-id="3ddab-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3ddab-141">System.String</span></span> 

### <span data-ttu-id="3ddab-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ddab-142">-Name</span></span>
 <span data-ttu-id="3ddab-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3ddab-143">System.String</span></span>

## <span data-ttu-id="3ddab-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ddab-144">OUTPUTS</span></span>

### <span data-ttu-id="3ddab-145">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3ddab-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3ddab-146">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="3ddab-146">Example 1 - Namespace</span></span>
<span data-ttu-id="3ddab-147">Direitos: {Listen, Send} nome: AuthoRule1 tipo: ID Microsoft. Relay/AuthorizationRules:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span><span class="sxs-lookup"><span data-stu-id="3ddab-147">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span></span>

### <span data-ttu-id="3ddab-148">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3ddab-148">Example 2 - WcfRelay</span></span>
<span data-ttu-id="3ddab-149">Direitos: {Listen, Send} Name: AuthoRule1 tipo: Microsoft. rerelay/ID do AuthorizationRules:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="3ddab-149">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="3ddab-150">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3ddab-150">Example 3 - HybridConnection</span></span>
<span data-ttu-id="3ddab-151">Direitos: {Listen, Send} nome: AuthoRule1 tipo: ID Microsoft. Relay/AuthorizationRules:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="3ddab-151">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="3ddab-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ddab-152">NOTES</span></span>

## <span data-ttu-id="3ddab-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ddab-153">RELATED LINKS</span></span>

