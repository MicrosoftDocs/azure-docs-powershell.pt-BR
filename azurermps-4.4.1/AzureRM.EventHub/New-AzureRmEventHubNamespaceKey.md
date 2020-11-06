---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441086"
---
# <span data-ttu-id="d6260-101">New-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="d6260-101">New-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="d6260-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6260-102">SYNOPSIS</span></span>
<span data-ttu-id="d6260-103">Cria uma nova chave primária ou secundária para a regra de autorização no namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="d6260-103">Creates a new primary or secondary key for the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6260-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6260-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d6260-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6260-105">DESCRIPTION</span></span>
<span data-ttu-id="d6260-106">O cmdlet New-AzureRmEventHubNamespaceKey regenera a chave primária ou secundária para a regra de autorização determinada no namespace dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="d6260-106">The New-AzureRmEventHubNamespaceKey cmdlet regenerates the primary or secondary key for the for the given authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="d6260-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6260-107">EXAMPLES</span></span>

### <span data-ttu-id="d6260-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6260-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

<span data-ttu-id="d6260-109">Regenera a chave primária para a regra de autorização \` MyAuthRuleName \` no namespace de hubs de eventos \` mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d6260-109">Regenerates the primary key for the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d6260-110">OS</span><span class="sxs-lookup"><span data-stu-id="d6260-110">PARAMETERS</span></span>

### <span data-ttu-id="d6260-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="d6260-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="d6260-112">Nome da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="d6260-112">Authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6260-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d6260-113">-NamespaceName</span></span>
<span data-ttu-id="d6260-114">O nome do namespace dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="d6260-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="d6260-115">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="d6260-115">-RegenerateKeys</span></span>
<span data-ttu-id="d6260-116">Chave para gerar novamente: \` PrimaryKey \` ou \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="d6260-116">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6260-117">-Resource</span><span class="sxs-lookup"><span data-stu-id="d6260-117">-ResourceGroup</span></span>
<span data-ttu-id="d6260-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6260-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6260-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6260-119">-Confirm</span></span>
<span data-ttu-id="d6260-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6260-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6260-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6260-121">-WhatIf</span></span>
<span data-ttu-id="d6260-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6260-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6260-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6260-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d6260-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6260-124">INPUTS</span></span>

### <span data-ttu-id="d6260-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d6260-125">System.String</span></span>

## <span data-ttu-id="d6260-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6260-126">OUTPUTS</span></span>

### <span data-ttu-id="d6260-127">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="d6260-127">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="d6260-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6260-128">NOTES</span></span>

## <span data-ttu-id="d6260-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6260-129">RELATED LINKS</span></span>

