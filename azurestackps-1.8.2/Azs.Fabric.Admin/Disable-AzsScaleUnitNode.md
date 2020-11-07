---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946650"
---
# <span data-ttu-id="56aad-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="56aad-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="56aad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56aad-102">SYNOPSIS</span></span>
<span data-ttu-id="56aad-103">Inicie o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="56aad-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="56aad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56aad-104">SYNTAX</span></span>

### <span data-ttu-id="56aad-105">Desabilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="56aad-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56aad-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="56aad-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56aad-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56aad-107">DESCRIPTION</span></span>
<span data-ttu-id="56aad-108">Inicie o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="56aad-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="56aad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56aad-109">EXAMPLES</span></span>

### <span data-ttu-id="56aad-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="56aad-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="56aad-111">Habilite o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="56aad-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="56aad-112">OS</span><span class="sxs-lookup"><span data-stu-id="56aad-112">PARAMETERS</span></span>

### <span data-ttu-id="56aad-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="56aad-113">-Name</span></span>
<span data-ttu-id="56aad-114">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="56aad-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56aad-115">-Local</span><span class="sxs-lookup"><span data-stu-id="56aad-115">-Location</span></span>
<span data-ttu-id="56aad-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="56aad-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56aad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56aad-117">-ResourceGroupName</span></span>
<span data-ttu-id="56aad-118">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="56aad-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56aad-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56aad-119">-ResourceId</span></span>
<span data-ttu-id="56aad-120">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="56aad-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="56aad-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56aad-121">-AsJob</span></span>
<span data-ttu-id="56aad-122">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="56aad-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="56aad-123">-Force</span><span class="sxs-lookup"><span data-stu-id="56aad-123">-Force</span></span>
<span data-ttu-id="56aad-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="56aad-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="56aad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56aad-125">-WhatIf</span></span>
<span data-ttu-id="56aad-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56aad-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56aad-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56aad-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56aad-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="56aad-128">-Confirm</span></span>
<span data-ttu-id="56aad-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56aad-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56aad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56aad-130">CommonParameters</span></span>
<span data-ttu-id="56aad-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56aad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56aad-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56aad-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56aad-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56aad-133">INPUTS</span></span>

## <span data-ttu-id="56aad-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56aad-134">OUTPUTS</span></span>

## <span data-ttu-id="56aad-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56aad-135">NOTES</span></span>

## <span data-ttu-id="56aad-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56aad-136">RELATED LINKS</span></span>
