---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441087"
---
# <span data-ttu-id="12d87-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="12d87-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="12d87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12d87-102">SYNOPSIS</span></span>
<span data-ttu-id="12d87-103">Cria uma nova chave primária ou secundária para a regra de autorização de hubs de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="12d87-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12d87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12d87-104">SYNTAX</span></span>

### <span data-ttu-id="12d87-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="12d87-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="12d87-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="12d87-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="12d87-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12d87-107">DESCRIPTION</span></span>
<span data-ttu-id="12d87-108">O cmdlet New-AzureRmEventHubKey regenera a chave SAS primária ou secundária para a regra de autorização de hubs de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="12d87-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="12d87-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12d87-109">EXAMPLES</span></span>

### <span data-ttu-id="12d87-110">Exemplo 1,1</span><span class="sxs-lookup"><span data-stu-id="12d87-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="12d87-111">Regenera a chave primária para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="12d87-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="12d87-112">Exemplo 1,2</span><span class="sxs-lookup"><span data-stu-id="12d87-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="12d87-113">Regenera a chave primária para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="12d87-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="12d87-114">Exemplo 2,1</span><span class="sxs-lookup"><span data-stu-id="12d87-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="12d87-115">Exemplo 2,2</span><span class="sxs-lookup"><span data-stu-id="12d87-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="12d87-116">Regenera a chave secundária para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="12d87-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="12d87-117">OS</span><span class="sxs-lookup"><span data-stu-id="12d87-117">PARAMETERS</span></span>

### <span data-ttu-id="12d87-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="12d87-118">-RegenerateKey</span></span>
<span data-ttu-id="12d87-119">Chave para gerar novamente: \` PrimaryKey \` ou \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="12d87-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d87-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12d87-120">-Confirm</span></span>
<span data-ttu-id="12d87-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d87-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12d87-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d87-122">-WhatIf</span></span>
<span data-ttu-id="12d87-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12d87-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12d87-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12d87-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12d87-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="12d87-125">-EventHub</span></span>
<span data-ttu-id="12d87-126">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="12d87-126">EventHub Name.</span></span>

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

### <span data-ttu-id="12d87-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="12d87-127">-Name</span></span>
<span data-ttu-id="12d87-128">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="12d87-128">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d87-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="12d87-129">-Namespace</span></span>
<span data-ttu-id="12d87-130">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="12d87-130">Namespace Name.</span></span>

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

### <span data-ttu-id="12d87-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d87-131">-ResourceGroupName</span></span>
<span data-ttu-id="12d87-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12d87-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="12d87-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12d87-133">INPUTS</span></span>

### <span data-ttu-id="12d87-134">System. String</span><span class="sxs-lookup"><span data-stu-id="12d87-134">System.String</span></span>

## <span data-ttu-id="12d87-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12d87-135">OUTPUTS</span></span>

### <span data-ttu-id="12d87-136">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="12d87-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="12d87-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12d87-137">NOTES</span></span>

## <span data-ttu-id="12d87-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12d87-138">RELATED LINKS</span></span>

