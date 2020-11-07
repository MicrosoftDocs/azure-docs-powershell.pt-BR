---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946825"
---
# <span data-ttu-id="3932d-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="3932d-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="3932d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3932d-102">SYNOPSIS</span></span>
<span data-ttu-id="3932d-103">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="3932d-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="3932d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3932d-104">SYNTAX</span></span>

### <span data-ttu-id="3932d-105">Parar (padrão)</span><span class="sxs-lookup"><span data-stu-id="3932d-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3932d-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="3932d-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3932d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3932d-107">DESCRIPTION</span></span>
<span data-ttu-id="3932d-108">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="3932d-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="3932d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3932d-109">EXAMPLES</span></span>

### <span data-ttu-id="3932d-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="3932d-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="3932d-111">Desligar um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="3932d-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="3932d-112">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="3932d-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="3932d-113">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="3932d-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="3932d-114">OS</span><span class="sxs-lookup"><span data-stu-id="3932d-114">PARAMETERS</span></span>

### <span data-ttu-id="3932d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3932d-115">-Name</span></span>
<span data-ttu-id="3932d-116">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="3932d-116">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3932d-117">-Local</span><span class="sxs-lookup"><span data-stu-id="3932d-117">-Location</span></span>
<span data-ttu-id="3932d-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="3932d-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3932d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3932d-119">-ResourceGroupName</span></span>
<span data-ttu-id="3932d-120">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="3932d-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3932d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3932d-121">-ResourceId</span></span>
<span data-ttu-id="3932d-122">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="3932d-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="3932d-123">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="3932d-123">-Shutdown</span></span>
<span data-ttu-id="3932d-124">Se definido normalmente desliga o nó da unidade de escala; caso contrário, desligue o nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="3932d-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="3932d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3932d-125">-AsJob</span></span>
<span data-ttu-id="3932d-126">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3932d-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="3932d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3932d-127">-Force</span></span>
<span data-ttu-id="3932d-128">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3932d-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3932d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3932d-129">-WhatIf</span></span>
<span data-ttu-id="3932d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3932d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3932d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3932d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3932d-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3932d-132">-Confirm</span></span>
<span data-ttu-id="3932d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3932d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3932d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3932d-134">CommonParameters</span></span>
<span data-ttu-id="3932d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3932d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3932d-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3932d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3932d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3932d-137">INPUTS</span></span>

## <span data-ttu-id="3932d-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3932d-138">OUTPUTS</span></span>

## <span data-ttu-id="3932d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3932d-139">NOTES</span></span>

## <span data-ttu-id="3932d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3932d-140">RELATED LINKS</span></span>
