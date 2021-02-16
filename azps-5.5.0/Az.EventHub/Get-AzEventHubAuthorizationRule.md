---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117667"
---
# <span data-ttu-id="eb819-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eb819-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="eb819-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb819-102">SYNOPSIS</span></span>
<span data-ttu-id="eb819-103">Obtém os detalhes de uma regra de autorização ou obtém uma lista de regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="eb819-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="eb819-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb819-104">SYNTAX</span></span>

### <span data-ttu-id="eb819-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eb819-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb819-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb819-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb819-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb819-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb819-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb819-108">DESCRIPTION</span></span>
<span data-ttu-id="eb819-109">O Get-AzEventHubAuthorizationRule cmdlet obtém os detalhes de uma regra de autorização ou uma lista de todas as regras de autorização para um Hub de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="eb819-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="eb819-110">Se o nome de uma regra de autorização for fornecido, os detalhes dessa única regra de autorização serão retornados.</span><span class="sxs-lookup"><span data-stu-id="eb819-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="eb819-111">Se o nome de uma regra de autorização não for fornecido, uma lista de todas as regras de autorização para o Hub de Eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="eb819-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="eb819-112">Se o nome do alias (Recuperação de Desastres) for fornecido, os detalhes da regra de autorização do Namespace para Alias configurado serão retornados.</span><span class="sxs-lookup"><span data-stu-id="eb819-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="eb819-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eb819-113">EXAMPLES</span></span>

### <span data-ttu-id="eb819-114">Exemplo 1: AuthorizationRule para namespace</span><span class="sxs-lookup"><span data-stu-id="eb819-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="eb819-115">Obtém a regra de \` autorização MyAuthRuleName \` no namespace \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="eb819-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="eb819-116">Exemplo 2: AuthorizationRules para namespace</span><span class="sxs-lookup"><span data-stu-id="eb819-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="eb819-117">Obtém uma lista de todas as regras de autorização no namespace \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="eb819-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="eb819-118">Exemplo 3: AuthorizationRule para EventHub</span><span class="sxs-lookup"><span data-stu-id="eb819-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="eb819-119">Obtém a regra de autorização MyAuthRuleName no Hub de Eventos MyEventHubName, que é escopo pelo \` \` \` \` namespace \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="eb819-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="eb819-120">Exemplo 4: AuthorizationRules para EventHub</span><span class="sxs-lookup"><span data-stu-id="eb819-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="eb819-121">Obtém regras de autorização de lista no Hub de Eventos MyEventHubName, que é escopo pelo \` \` namespace \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="eb819-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="eb819-122">Exemplo 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="eb819-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="eb819-123">Obtém a regra de \` autorização MyAuthRuleName \` no namespace \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="eb819-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="eb819-124">Exemplo 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="eb819-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="eb819-125">Obtém uma lista de todas as regras de autorização \` MyAuthRuleName \` no namespace \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="eb819-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="eb819-126">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb819-126">PARAMETERS</span></span>

### <span data-ttu-id="eb819-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="eb819-127">-AliasName</span></span>
<span data-ttu-id="eb819-128">Nome do Alias</span><span class="sxs-lookup"><span data-stu-id="eb819-128">Alias Name</span></span>

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

### <span data-ttu-id="eb819-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb819-129">-DefaultProfile</span></span>
<span data-ttu-id="eb819-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb819-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb819-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="eb819-131">-Eventhub</span></span>
<span data-ttu-id="eb819-132">Nome eventhub</span><span class="sxs-lookup"><span data-stu-id="eb819-132">Eventhub Name</span></span>

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

### <span data-ttu-id="eb819-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb819-133">-Name</span></span>
<span data-ttu-id="eb819-134">Nome de AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eb819-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="eb819-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eb819-135">-Namespace</span></span>
<span data-ttu-id="eb819-136">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="eb819-136">Namespace Name</span></span>

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

### <span data-ttu-id="eb819-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb819-137">-ResourceGroupName</span></span>
<span data-ttu-id="eb819-138">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="eb819-138">Resource Group Name</span></span>

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

### <span data-ttu-id="eb819-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb819-139">CommonParameters</span></span>
<span data-ttu-id="eb819-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb819-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb819-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb819-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb819-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="eb819-142">INPUTS</span></span>

### <span data-ttu-id="eb819-143">System.String</span><span class="sxs-lookup"><span data-stu-id="eb819-143">System.String</span></span>

## <span data-ttu-id="eb819-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="eb819-144">OUTPUTS</span></span>

### <span data-ttu-id="eb819-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="eb819-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="eb819-146">Notas</span><span class="sxs-lookup"><span data-stu-id="eb819-146">NOTES</span></span>

## <span data-ttu-id="eb819-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb819-147">RELATED LINKS</span></span>
