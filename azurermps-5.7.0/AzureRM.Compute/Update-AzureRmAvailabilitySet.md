---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426769"
---
# <span data-ttu-id="2d57a-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d57a-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="2d57a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d57a-102">SYNOPSIS</span></span>
<span data-ttu-id="2d57a-103">Atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="2d57a-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d57a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d57a-104">SYNTAX</span></span>

### <span data-ttu-id="2d57a-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d57a-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d57a-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="2d57a-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d57a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d57a-107">DESCRIPTION</span></span>
<span data-ttu-id="2d57a-108">O cmdlet **Update-AzureRmAvailabilitySet** atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="2d57a-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="2d57a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d57a-109">EXAMPLES</span></span>

### <span data-ttu-id="2d57a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d57a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="2d57a-111">Esse comando atualiza o conjunto de disponibilidade chamado ' AvSet01 ' no grupo de recursos chamado ' ResourceGroup01 ' para um conjunto de disponibilidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="2d57a-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="2d57a-112">OS</span><span class="sxs-lookup"><span data-stu-id="2d57a-112">PARAMETERS</span></span>

### <span data-ttu-id="2d57a-113">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="2d57a-113">-AvailabilitySet</span></span>
<span data-ttu-id="2d57a-114">Especifica o objeto do conjunto de disponibilidade a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="2d57a-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d57a-115">Gerenciados por</span><span class="sxs-lookup"><span data-stu-id="2d57a-115">-Managed</span></span>
<span data-ttu-id="2d57a-116">Conjunto de disponibilidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="2d57a-116">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d57a-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="2d57a-117">-Sku</span></span>
<span data-ttu-id="2d57a-118">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="2d57a-118">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d57a-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d57a-119">-Confirm</span></span>
<span data-ttu-id="2d57a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d57a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d57a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d57a-121">-WhatIf</span></span>
<span data-ttu-id="2d57a-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d57a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d57a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d57a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d57a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d57a-124">CommonParameters</span></span>
<span data-ttu-id="2d57a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d57a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d57a-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d57a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d57a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d57a-127">INPUTS</span></span>

### <span data-ttu-id="2d57a-128">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d57a-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="2d57a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d57a-129">OUTPUTS</span></span>

### <span data-ttu-id="2d57a-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d57a-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="2d57a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d57a-131">NOTES</span></span>

## <span data-ttu-id="2d57a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d57a-132">RELATED LINKS</span></span>

