---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441084"
---
# <span data-ttu-id="1887d-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="1887d-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="1887d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1887d-102">SYNOPSIS</span></span>
<span data-ttu-id="1887d-103">Remove o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="1887d-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1887d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1887d-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1887d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1887d-105">DESCRIPTION</span></span>
<span data-ttu-id="1887d-106">O cmdlet Remove-AzureRmEventHub remove e exclui o Hub de eventos especificado do namespace fornecido.</span><span class="sxs-lookup"><span data-stu-id="1887d-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="1887d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1887d-107">EXAMPLES</span></span>

### <span data-ttu-id="1887d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1887d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="1887d-109">Remove o Hub de eventos \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="1887d-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="1887d-110">OS</span><span class="sxs-lookup"><span data-stu-id="1887d-110">PARAMETERS</span></span>

### <span data-ttu-id="1887d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1887d-111">-ResourceGroupName</span></span>
<span data-ttu-id="1887d-112">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1887d-112">Resource group name.</span></span>

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

### <span data-ttu-id="1887d-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1887d-113">-Confirm</span></span>
<span data-ttu-id="1887d-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1887d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1887d-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1887d-115">-WhatIf</span></span>
<span data-ttu-id="1887d-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1887d-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1887d-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1887d-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1887d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1887d-118">-Name</span></span>
<span data-ttu-id="1887d-119">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="1887d-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1887d-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1887d-120">-Namespace</span></span>
<span data-ttu-id="1887d-121">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="1887d-121">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="1887d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1887d-122">INPUTS</span></span>

### <span data-ttu-id="1887d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1887d-123">System.String</span></span>

## <span data-ttu-id="1887d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1887d-124">OUTPUTS</span></span>

### <span data-ttu-id="1887d-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="1887d-125">System.Object</span></span>

## <span data-ttu-id="1887d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1887d-126">NOTES</span></span>

## <span data-ttu-id="1887d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1887d-127">RELATED LINKS</span></span>

