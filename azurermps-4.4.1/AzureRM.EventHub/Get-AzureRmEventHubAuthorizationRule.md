---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441100"
---
# <span data-ttu-id="2f73c-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2f73c-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="2f73c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f73c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f73c-103">Obtém os detalhes de uma regra de autorização ou obtém uma lista de regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="2f73c-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f73c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f73c-104">SYNTAX</span></span>

### <span data-ttu-id="2f73c-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f73c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="2f73c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f73c-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="2f73c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f73c-107">DESCRIPTION</span></span>
<span data-ttu-id="2f73c-108">O cmdlet Get-AzureRmEventHubAuthorizationRule Obtém os detalhes de uma regra de autorização ou uma lista de todas as regras de autorização para um hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="2f73c-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="2f73c-109">Se o nome de uma regra de autorização for fornecido, os detalhes dessa única regra de autorização serão retornados.</span><span class="sxs-lookup"><span data-stu-id="2f73c-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="2f73c-110">Se o nome de uma regra de autorização não for fornecido, uma lista de todas as regras de autorização para o Hub de eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="2f73c-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="2f73c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f73c-111">EXAMPLES</span></span>

### <span data-ttu-id="2f73c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f73c-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="2f73c-113">Obtém a regra de autorização \` MyAuthRuleName \` no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="2f73c-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="2f73c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2f73c-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="2f73c-115">Obtém uma lista de todas as regras de autorização no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="2f73c-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="2f73c-116">OS</span><span class="sxs-lookup"><span data-stu-id="2f73c-116">PARAMETERS</span></span>

### <span data-ttu-id="2f73c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f73c-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f73c-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f73c-118">Resource group name.</span></span>

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

### <span data-ttu-id="2f73c-119">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="2f73c-119">-Eventhub</span></span>
<span data-ttu-id="2f73c-120">Nome do Eventhub.</span><span class="sxs-lookup"><span data-stu-id="2f73c-120">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f73c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f73c-121">-Name</span></span>
<span data-ttu-id="2f73c-122">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="2f73c-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f73c-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2f73c-123">-Namespace</span></span>
<span data-ttu-id="2f73c-124">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="2f73c-124">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="2f73c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f73c-125">INPUTS</span></span>

### <span data-ttu-id="2f73c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2f73c-126">System.String</span></span>

## <span data-ttu-id="2f73c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f73c-127">OUTPUTS</span></span>

### <span data-ttu-id="2f73c-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2f73c-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2f73c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f73c-129">NOTES</span></span>

## <span data-ttu-id="2f73c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f73c-130">RELATED LINKS</span></span>

