---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7fa3b4780e4c25dd716b851fd80c698b8d98d0b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941824"
---
# <span data-ttu-id="cf8d3-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf8d3-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="cf8d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8d3-103">Obtém os detalhes de uma regra de autorização ou obtém uma lista de regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="cf8d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf8d3-104">SYNTAX</span></span>

### <span data-ttu-id="cf8d3-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf8d3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf8d3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cf8d3-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf8d3-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="cf8d3-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf8d3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf8d3-108">DESCRIPTION</span></span>
<span data-ttu-id="cf8d3-109">O cmdlet Get-AzEventHubAuthorizationRule Obtém os detalhes de uma regra de autorização ou uma lista de todas as regras de autorização para um hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="cf8d3-110">Se o nome de uma regra de autorização for fornecido, os detalhes dessa única regra de autorização serão retornados.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="cf8d3-111">Se o nome de uma regra de autorização não for fornecido, uma lista de todas as regras de autorização para o Hub de eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="cf8d3-112">Se o nome do alias fornecido (recuperação de desastre) fornecido, os detalhes da regra de autorização do namespace para alias configurado serão retornados.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="cf8d3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf8d3-113">EXAMPLES</span></span>

### <span data-ttu-id="cf8d3-114">Exemplo 1,0-AuthorizationRule para namespace</span><span class="sxs-lookup"><span data-stu-id="cf8d3-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="cf8d3-115">Obtém a regra de autorização \` MyAuthRuleName \` no namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="cf8d3-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="cf8d3-116">Exemplo 1,1-AuthorizationRules para namespace</span><span class="sxs-lookup"><span data-stu-id="cf8d3-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="cf8d3-117">Obtém uma lista de todas as regras de autorização no namespace \` Mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="cf8d3-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="cf8d3-118">Exemplo 2,0-AuthorizationRule para EventHub</span><span class="sxs-lookup"><span data-stu-id="cf8d3-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="cf8d3-119">Obtém a regra de autorização \` MyAuthRuleName \` no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="cf8d3-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="cf8d3-120">Exemplo 2,1-AuthorizationRules para EventHub</span><span class="sxs-lookup"><span data-stu-id="cf8d3-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="cf8d3-121">Obtém as regras de autorização de lista no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="cf8d3-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="cf8d3-122">Exemplo 3,0-AuthorizationRule para alias (configuração georecuperação)</span><span class="sxs-lookup"><span data-stu-id="cf8d3-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="cf8d3-123">Obtém a regra de autorização \` MyAuthRuleName \` no namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="cf8d3-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="cf8d3-124">Exemplo 3,1-AuthorizationRules para alias (configuração georecuperação)</span><span class="sxs-lookup"><span data-stu-id="cf8d3-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="cf8d3-125">Obtém uma lista de todos os MyAuthRuleName de regra de autorização \` \` no namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="cf8d3-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="cf8d3-126">OS</span><span class="sxs-lookup"><span data-stu-id="cf8d3-126">PARAMETERS</span></span>

### <span data-ttu-id="cf8d3-127">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="cf8d3-127">-AliasName</span></span>
<span data-ttu-id="cf8d3-128">Nome do alias</span><span class="sxs-lookup"><span data-stu-id="cf8d3-128">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8d3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8d3-129">-DefaultProfile</span></span>
<span data-ttu-id="cf8d3-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf8d3-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="cf8d3-131">-Eventhub</span></span>
<span data-ttu-id="cf8d3-132">Nome do Eventhub</span><span class="sxs-lookup"><span data-stu-id="cf8d3-132">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8d3-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf8d3-133">-Name</span></span>
<span data-ttu-id="cf8d3-134">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf8d3-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8d3-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cf8d3-135">-Namespace</span></span>
<span data-ttu-id="cf8d3-136">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="cf8d3-136">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8d3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf8d3-137">-ResourceGroupName</span></span>
<span data-ttu-id="cf8d3-138">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cf8d3-138">Resource Group Name</span></span>

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

### <span data-ttu-id="cf8d3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8d3-139">CommonParameters</span></span>
<span data-ttu-id="cf8d3-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8d3-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf8d3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8d3-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf8d3-142">INPUTS</span></span>

### <span data-ttu-id="cf8d3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cf8d3-143">System.String</span></span>

## <span data-ttu-id="cf8d3-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf8d3-144">OUTPUTS</span></span>

### <span data-ttu-id="cf8d3-145">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cf8d3-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cf8d3-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf8d3-146">NOTES</span></span>

## <span data-ttu-id="cf8d3-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf8d3-147">RELATED LINKS</span></span>
