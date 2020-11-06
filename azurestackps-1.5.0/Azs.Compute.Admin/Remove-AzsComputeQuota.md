---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b3fb659c1d11df734bdc95f554e4c100060e185
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425782"
---
# <span data-ttu-id="e5abd-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="e5abd-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="e5abd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5abd-102">SYNOPSIS</span></span>
<span data-ttu-id="e5abd-103">Exclui a cota de computação especificada.</span><span class="sxs-lookup"><span data-stu-id="e5abd-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="e5abd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5abd-104">SYNTAX</span></span>

### <span data-ttu-id="e5abd-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5abd-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5abd-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="e5abd-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5abd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5abd-107">DESCRIPTION</span></span>
<span data-ttu-id="e5abd-108">Excluir uma cota existente.</span><span class="sxs-lookup"><span data-stu-id="e5abd-108">Delete an existing quota.</span></span>

## <span data-ttu-id="e5abd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5abd-109">EXAMPLES</span></span>

### <span data-ttu-id="e5abd-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e5abd-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="e5abd-111">Remova uma cota de computação com todos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e5abd-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="e5abd-112">OS</span><span class="sxs-lookup"><span data-stu-id="e5abd-112">PARAMETERS</span></span>

### <span data-ttu-id="e5abd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e5abd-113">-Force</span></span>
<span data-ttu-id="e5abd-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e5abd-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e5abd-115">-Local</span><span class="sxs-lookup"><span data-stu-id="e5abd-115">-Location</span></span>
<span data-ttu-id="e5abd-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e5abd-116">Location of the resource.</span></span> <span data-ttu-id="e5abd-117">Se não for especificado, ele será o local associado à assinatura do tenat.</span><span class="sxs-lookup"><span data-stu-id="e5abd-117">If not given we default to the location bound to the tenat's subscription.</span></span>

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

### <span data-ttu-id="e5abd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5abd-118">-Name</span></span>
<span data-ttu-id="e5abd-119">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="e5abd-119">Name of the quota.</span></span>

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

### <span data-ttu-id="e5abd-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5abd-120">-ResourceId</span></span>
<span data-ttu-id="e5abd-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e5abd-121">The resource id.</span></span>

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

### <span data-ttu-id="e5abd-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e5abd-122">-Confirm</span></span>
<span data-ttu-id="e5abd-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5abd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5abd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5abd-124">-WhatIf</span></span>
<span data-ttu-id="e5abd-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5abd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5abd-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5abd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5abd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5abd-127">CommonParameters</span></span>
<span data-ttu-id="e5abd-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5abd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5abd-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5abd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5abd-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5abd-130">INPUTS</span></span>

## <span data-ttu-id="e5abd-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5abd-131">OUTPUTS</span></span>

## <span data-ttu-id="e5abd-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5abd-132">NOTES</span></span>

## <span data-ttu-id="e5abd-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5abd-133">RELATED LINKS</span></span>

