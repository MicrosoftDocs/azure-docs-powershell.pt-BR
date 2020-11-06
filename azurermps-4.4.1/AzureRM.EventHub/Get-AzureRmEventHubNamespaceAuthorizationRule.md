---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610798"
---
# <span data-ttu-id="6b027-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6b027-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="6b027-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b027-102">SYNOPSIS</span></span>
<span data-ttu-id="6b027-103">Obtém os detalhes de uma regra de autorização de namespace Eventubs ou obtém uma lista de regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="6b027-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b027-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b027-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="6b027-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b027-105">DESCRIPTION</span></span>
<span data-ttu-id="6b027-106">O cmdlet Get-AzureRmEventHubNamespaceAuthorizationRule Obtém os detalhes de uma regra de autorização de namespace de hubs de eventos especificada ou uma lista de regras de autorização de namespace.</span><span class="sxs-lookup"><span data-stu-id="6b027-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="6b027-107">Se o nome da regra de autorização for fornecido, os detalhes de uma única regra de autorização serão retornados.</span><span class="sxs-lookup"><span data-stu-id="6b027-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="6b027-108">Se um nome de regra de autorização não for fornecido, uma lista de todas as regras de autorização no namespace será retornada.</span><span class="sxs-lookup"><span data-stu-id="6b027-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="6b027-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b027-109">EXAMPLES</span></span>

### <span data-ttu-id="6b027-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b027-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="6b027-111">Retorna a regra de autorização \` MyAuthRuleName \` no namespace de hubs de eventos \` mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6b027-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6b027-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6b027-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="6b027-113">Retorna a regra de autorização padrão \` RootManageSharedAccessKey \` no namespace de hubs de eventos \` mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6b027-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6b027-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6b027-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="6b027-115">Retorna todas as regras de autorização no namespace de hubs de evento \` Mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6b027-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6b027-116">OS</span><span class="sxs-lookup"><span data-stu-id="6b027-116">PARAMETERS</span></span>

### <span data-ttu-id="6b027-117">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="6b027-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="6b027-118">O nome da regra de autorização do namespace de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="6b027-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b027-119">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6b027-119">-NamespaceName</span></span>
<span data-ttu-id="6b027-120">O nome do namespace dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="6b027-120">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b027-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b027-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b027-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b027-122">Resource group name.</span></span>

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

## <span data-ttu-id="6b027-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b027-123">INPUTS</span></span>

### <span data-ttu-id="6b027-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6b027-124">System.String</span></span>

## <span data-ttu-id="6b027-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b027-125">OUTPUTS</span></span>

### <span data-ttu-id="6b027-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6b027-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6b027-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b027-127">NOTES</span></span>

## <span data-ttu-id="6b027-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b027-128">RELATED LINKS</span></span>

