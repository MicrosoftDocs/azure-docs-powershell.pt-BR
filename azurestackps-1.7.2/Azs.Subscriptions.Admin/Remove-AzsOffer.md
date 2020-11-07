---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2ac9f85896c1ae0a8eb7e060600ba5b4eb0e792
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774486"
---
# <span data-ttu-id="7122e-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="7122e-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="7122e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7122e-102">SYNOPSIS</span></span>
<span data-ttu-id="7122e-103">Exclua a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="7122e-103">Delete the specified offer.</span></span>

## <span data-ttu-id="7122e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7122e-104">SYNTAX</span></span>

### <span data-ttu-id="7122e-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="7122e-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7122e-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="7122e-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7122e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7122e-107">DESCRIPTION</span></span>
<span data-ttu-id="7122e-108">Exclua a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="7122e-108">Delete the specified offer.</span></span>

## <span data-ttu-id="7122e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7122e-109">EXAMPLES</span></span>

### <span data-ttu-id="7122e-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7122e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="7122e-111">Exclua a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="7122e-111">Delete the specified offer.</span></span>

## <span data-ttu-id="7122e-112">OS</span><span class="sxs-lookup"><span data-stu-id="7122e-112">PARAMETERS</span></span>

### <span data-ttu-id="7122e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7122e-113">-Force</span></span>
<span data-ttu-id="7122e-114">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="7122e-114">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7122e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7122e-115">-Name</span></span>
<span data-ttu-id="7122e-116">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="7122e-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7122e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7122e-117">-ResourceGroupName</span></span>
<span data-ttu-id="7122e-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="7122e-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7122e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7122e-119">-ResourceId</span></span>
<span data-ttu-id="7122e-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7122e-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7122e-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7122e-121">-Confirm</span></span>
<span data-ttu-id="7122e-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7122e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7122e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7122e-123">-WhatIf</span></span>
<span data-ttu-id="7122e-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7122e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7122e-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7122e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7122e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7122e-126">CommonParameters</span></span>
<span data-ttu-id="7122e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7122e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7122e-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7122e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7122e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7122e-129">INPUTS</span></span>

## <span data-ttu-id="7122e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7122e-130">OUTPUTS</span></span>

## <span data-ttu-id="7122e-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7122e-131">NOTES</span></span>

## <span data-ttu-id="7122e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7122e-132">RELATED LINKS</span></span>

