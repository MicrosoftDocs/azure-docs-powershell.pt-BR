---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429106"
---
# <span data-ttu-id="9b733-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9b733-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="9b733-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b733-102">SYNOPSIS</span></span>
<span data-ttu-id="9b733-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="9b733-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b733-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b733-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b733-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b733-105">DESCRIPTION</span></span>
<span data-ttu-id="9b733-106">O cmdlet **Remove-AzureRmServiceBusNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="9b733-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="9b733-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b733-107">EXAMPLES</span></span>

### <span data-ttu-id="9b733-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b733-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="9b733-109">Remove o namespace de barramento do serviço `SB-Example1` do grupo de recursos especificado `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="9b733-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="9b733-110">OS</span><span class="sxs-lookup"><span data-stu-id="9b733-110">PARAMETERS</span></span>

### <span data-ttu-id="9b733-111">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9b733-111">-NamespaceName</span></span>
<span data-ttu-id="9b733-112">O nome do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="9b733-112">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="9b733-113">-Resource</span><span class="sxs-lookup"><span data-stu-id="9b733-113">-ResourceGroup</span></span>
<span data-ttu-id="9b733-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b733-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b733-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b733-115">-Confirm</span></span>
<span data-ttu-id="9b733-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b733-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b733-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b733-117">-WhatIf</span></span>
<span data-ttu-id="9b733-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b733-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b733-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b733-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b733-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b733-120">CommonParameters</span></span>
<span data-ttu-id="9b733-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b733-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b733-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b733-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b733-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b733-123">INPUTS</span></span>

### <span data-ttu-id="9b733-124">-Resource</span><span class="sxs-lookup"><span data-stu-id="9b733-124">-ResourceGroup</span></span>
 <span data-ttu-id="9b733-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9b733-125">System.String</span></span>

### <span data-ttu-id="9b733-126">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9b733-126">-NamespaceName</span></span>
 <span data-ttu-id="9b733-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9b733-127">System.String</span></span>

## <span data-ttu-id="9b733-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b733-128">OUTPUTS</span></span>

### <span data-ttu-id="9b733-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="9b733-129">System.Object</span></span>

## <span data-ttu-id="9b733-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b733-130">NOTES</span></span>

## <span data-ttu-id="9b733-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b733-131">RELATED LINKS</span></span>

