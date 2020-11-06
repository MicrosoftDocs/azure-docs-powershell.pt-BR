---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432223"
---
# <span data-ttu-id="67fe7-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="67fe7-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="67fe7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="67fe7-103">Remove o namespace especificado dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="67fe7-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67fe7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67fe7-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="67fe7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67fe7-105">DESCRIPTION</span></span>
<span data-ttu-id="67fe7-106">O cmdlet Remove-AzureRmEventHubNamespace remove e exclui o namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="67fe7-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="67fe7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67fe7-107">EXAMPLES</span></span>

### <span data-ttu-id="67fe7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67fe7-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="67fe7-109">Remove o namespace de hubs de evento \` Mynamespacename \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="67fe7-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="67fe7-110">OS</span><span class="sxs-lookup"><span data-stu-id="67fe7-110">PARAMETERS</span></span>

### <span data-ttu-id="67fe7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67fe7-111">-ResourceGroupName</span></span>
<span data-ttu-id="67fe7-112">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="67fe7-112">Resource group name.</span></span>

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

### <span data-ttu-id="67fe7-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67fe7-113">-Confirm</span></span>
<span data-ttu-id="67fe7-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67fe7-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67fe7-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67fe7-115">-WhatIf</span></span>
<span data-ttu-id="67fe7-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67fe7-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67fe7-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67fe7-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67fe7-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="67fe7-118">-Name</span></span>
<span data-ttu-id="67fe7-119">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="67fe7-119">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="67fe7-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67fe7-120">INPUTS</span></span>

### <span data-ttu-id="67fe7-121">System. String</span><span class="sxs-lookup"><span data-stu-id="67fe7-121">System.String</span></span>

## <span data-ttu-id="67fe7-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67fe7-122">OUTPUTS</span></span>

### <span data-ttu-id="67fe7-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="67fe7-123">System.Object</span></span>

## <span data-ttu-id="67fe7-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67fe7-124">NOTES</span></span>

## <span data-ttu-id="67fe7-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67fe7-125">RELATED LINKS</span></span>

