---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114537"
---
# <span data-ttu-id="1d51b-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1d51b-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="1d51b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d51b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d51b-103">Obtém os detalhes de uma regra de autorização ou obtém uma lista de regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="1d51b-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="1d51b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d51b-104">SYNTAX</span></span>

### <span data-ttu-id="1d51b-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1d51b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d51b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d51b-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d51b-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d51b-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d51b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d51b-108">DESCRIPTION</span></span>
<span data-ttu-id="1d51b-109">O cmdlet Get-AzEventHubAuthorizationRule Obtém os detalhes de uma regra de autorização ou uma lista de todas as regras de autorização para um hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="1d51b-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="1d51b-110">Se o nome de uma regra de autorização for fornecido, os detalhes dessa única regra de autorização serão retornados.</span><span class="sxs-lookup"><span data-stu-id="1d51b-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="1d51b-111">Se o nome de uma regra de autorização não for fornecido, uma lista de todas as regras de autorização para o Hub de eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="1d51b-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="1d51b-112">Se o nome do alias fornecido (recuperação de desastre) fornecido, os detalhes da regra de autorização do namespace para alias configurado serão retornados.</span><span class="sxs-lookup"><span data-stu-id="1d51b-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="1d51b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d51b-113">EXAMPLES</span></span>

### <span data-ttu-id="1d51b-114">Exemplo 1: AuthorizationRule para namespace</span><span class="sxs-lookup"><span data-stu-id="1d51b-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="1d51b-115">Obtém a regra de autorização \` MyAuthRuleName \` no namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="1d51b-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="1d51b-116">Exemplo 2: AuthorizationRules para namespace</span><span class="sxs-lookup"><span data-stu-id="1d51b-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="1d51b-117">Obtém uma lista de todas as regras de autorização no namespace \` Mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="1d51b-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="1d51b-118">Exemplo 3: AuthorizationRule para o EventHub</span><span class="sxs-lookup"><span data-stu-id="1d51b-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="1d51b-119">Obtém a regra de autorização \` MyAuthRuleName \` no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="1d51b-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="1d51b-120">Exemplo 4: AuthorizationRules para o EventHub</span><span class="sxs-lookup"><span data-stu-id="1d51b-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="1d51b-121">Obtém as regras de autorização de lista no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="1d51b-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="1d51b-122">Exemplo 5: AuthorizationRule para alias (configuração georecuperação)</span><span class="sxs-lookup"><span data-stu-id="1d51b-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="1d51b-123">Obtém a regra de autorização \` MyAuthRuleName \` no namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="1d51b-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="1d51b-124">Exemplo 6: AuthorizationRules para alias (configuração de georecuperação)</span><span class="sxs-lookup"><span data-stu-id="1d51b-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="1d51b-125">Obtém uma lista de todos os MyAuthRuleName de regra de autorização \` \` no namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="1d51b-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="1d51b-126">OS</span><span class="sxs-lookup"><span data-stu-id="1d51b-126">PARAMETERS</span></span>

### <span data-ttu-id="1d51b-127">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="1d51b-127">-AliasName</span></span>
<span data-ttu-id="1d51b-128">Nome do alias</span><span class="sxs-lookup"><span data-stu-id="1d51b-128">Alias Name</span></span>

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

### <span data-ttu-id="1d51b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d51b-129">-DefaultProfile</span></span>
<span data-ttu-id="1d51b-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d51b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d51b-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="1d51b-131">-Eventhub</span></span>
<span data-ttu-id="1d51b-132">Nome do Eventhub</span><span class="sxs-lookup"><span data-stu-id="1d51b-132">Eventhub Name</span></span>

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

### <span data-ttu-id="1d51b-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d51b-133">-Name</span></span>
<span data-ttu-id="1d51b-134">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1d51b-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="1d51b-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1d51b-135">-Namespace</span></span>
<span data-ttu-id="1d51b-136">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="1d51b-136">Namespace Name</span></span>

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

### <span data-ttu-id="1d51b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d51b-137">-ResourceGroupName</span></span>
<span data-ttu-id="1d51b-138">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1d51b-138">Resource Group Name</span></span>

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

### <span data-ttu-id="1d51b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d51b-139">CommonParameters</span></span>
<span data-ttu-id="1d51b-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d51b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d51b-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d51b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d51b-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d51b-142">INPUTS</span></span>

### <span data-ttu-id="1d51b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1d51b-143">System.String</span></span>

## <span data-ttu-id="1d51b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d51b-144">OUTPUTS</span></span>

### <span data-ttu-id="1d51b-145">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1d51b-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1d51b-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d51b-146">NOTES</span></span>

## <span data-ttu-id="1d51b-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d51b-147">RELATED LINKS</span></span>
