---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ebc1ebae40d6d1726ee6c23def6f82ff1efc8517
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775002"
---
# <span data-ttu-id="3491b-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="3491b-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="3491b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3491b-102">SYNOPSIS</span></span>
<span data-ttu-id="3491b-103">Exclui a cota de computação especificada.</span><span class="sxs-lookup"><span data-stu-id="3491b-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="3491b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3491b-104">SYNTAX</span></span>

### <span data-ttu-id="3491b-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="3491b-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3491b-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="3491b-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3491b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3491b-107">DESCRIPTION</span></span>
<span data-ttu-id="3491b-108">Excluir uma cota existente.</span><span class="sxs-lookup"><span data-stu-id="3491b-108">Delete an existing quota.</span></span>

## <span data-ttu-id="3491b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3491b-109">EXAMPLES</span></span>

### <span data-ttu-id="3491b-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3491b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="3491b-111">Remova uma cota de computação com todos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3491b-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="3491b-112">OS</span><span class="sxs-lookup"><span data-stu-id="3491b-112">PARAMETERS</span></span>

### <span data-ttu-id="3491b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3491b-113">-Force</span></span>
<span data-ttu-id="3491b-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3491b-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3491b-115">-Local</span><span class="sxs-lookup"><span data-stu-id="3491b-115">-Location</span></span>
<span data-ttu-id="3491b-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="3491b-116">Location of the resource.</span></span> <span data-ttu-id="3491b-117">Se não for especificado, ele será o local associado à assinatura do tenat.</span><span class="sxs-lookup"><span data-stu-id="3491b-117">If not given we default to the location bound to the tenat's subscription.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3491b-118">-Name</span></span>
<span data-ttu-id="3491b-119">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="3491b-119">Name of the quota.</span></span>

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

### <span data-ttu-id="3491b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3491b-120">-ResourceId</span></span>
<span data-ttu-id="3491b-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3491b-121">The resource id.</span></span>

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

### <span data-ttu-id="3491b-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3491b-122">-Confirm</span></span>
<span data-ttu-id="3491b-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3491b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3491b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3491b-124">-WhatIf</span></span>
<span data-ttu-id="3491b-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3491b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3491b-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3491b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3491b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3491b-127">CommonParameters</span></span>
<span data-ttu-id="3491b-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3491b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3491b-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3491b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3491b-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3491b-130">INPUTS</span></span>

## <span data-ttu-id="3491b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3491b-131">OUTPUTS</span></span>

## <span data-ttu-id="3491b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3491b-132">NOTES</span></span>

## <span data-ttu-id="3491b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3491b-133">RELATED LINKS</span></span>

