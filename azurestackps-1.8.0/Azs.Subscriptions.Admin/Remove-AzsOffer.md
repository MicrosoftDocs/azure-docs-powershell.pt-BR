---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774578"
---
# <span data-ttu-id="3c445-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="3c445-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="3c445-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c445-102">SYNOPSIS</span></span>
<span data-ttu-id="3c445-103">Exclua a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="3c445-103">Delete the specified offer.</span></span>

## <span data-ttu-id="3c445-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c445-104">SYNTAX</span></span>

### <span data-ttu-id="3c445-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="3c445-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c445-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="3c445-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c445-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c445-107">DESCRIPTION</span></span>
<span data-ttu-id="3c445-108">Exclua a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="3c445-108">Delete the specified offer.</span></span>

## <span data-ttu-id="3c445-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c445-109">EXAMPLES</span></span>

### <span data-ttu-id="3c445-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c445-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="3c445-111">Exclua a oferta especificada.</span><span class="sxs-lookup"><span data-stu-id="3c445-111">Delete the specified offer.</span></span>

## <span data-ttu-id="3c445-112">OS</span><span class="sxs-lookup"><span data-stu-id="3c445-112">PARAMETERS</span></span>

### <span data-ttu-id="3c445-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3c445-113">-Force</span></span>
<span data-ttu-id="3c445-114">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="3c445-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="3c445-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c445-115">-Name</span></span>
<span data-ttu-id="3c445-116">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="3c445-116">Name of an offer.</span></span>

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

### <span data-ttu-id="3c445-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c445-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c445-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="3c445-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3c445-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c445-119">-ResourceId</span></span>
<span data-ttu-id="3c445-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3c445-120">The resource id.</span></span>

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

### <span data-ttu-id="3c445-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c445-121">-Confirm</span></span>
<span data-ttu-id="3c445-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c445-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c445-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c445-123">-WhatIf</span></span>
<span data-ttu-id="3c445-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c445-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c445-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c445-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c445-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c445-126">CommonParameters</span></span>
<span data-ttu-id="3c445-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c445-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c445-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c445-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c445-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c445-129">INPUTS</span></span>

## <span data-ttu-id="3c445-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c445-130">OUTPUTS</span></span>

## <span data-ttu-id="3c445-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c445-131">NOTES</span></span>

## <span data-ttu-id="3c445-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c445-132">RELATED LINKS</span></span>
