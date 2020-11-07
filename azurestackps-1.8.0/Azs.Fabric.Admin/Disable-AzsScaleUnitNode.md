---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774650"
---
# <span data-ttu-id="1a147-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1a147-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1a147-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a147-102">SYNOPSIS</span></span>
<span data-ttu-id="1a147-103">Inicie o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="1a147-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="1a147-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a147-104">SYNTAX</span></span>

### <span data-ttu-id="1a147-105">Desabilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="1a147-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a147-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="1a147-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a147-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a147-107">DESCRIPTION</span></span>
<span data-ttu-id="1a147-108">Inicie o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="1a147-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="1a147-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a147-109">EXAMPLES</span></span>

### <span data-ttu-id="1a147-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="1a147-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="1a147-111">Habilite o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="1a147-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="1a147-112">OS</span><span class="sxs-lookup"><span data-stu-id="1a147-112">PARAMETERS</span></span>

### <span data-ttu-id="1a147-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a147-113">-Name</span></span>
<span data-ttu-id="1a147-114">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="1a147-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="1a147-115">-Local</span><span class="sxs-lookup"><span data-stu-id="1a147-115">-Location</span></span>
<span data-ttu-id="1a147-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="1a147-116">Location of the resource.</span></span>

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

### <span data-ttu-id="1a147-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a147-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a147-118">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="1a147-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1a147-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a147-119">-ResourceId</span></span>
<span data-ttu-id="1a147-120">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="1a147-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="1a147-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a147-121">-AsJob</span></span>
<span data-ttu-id="1a147-122">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1a147-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1a147-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1a147-123">-Force</span></span>
<span data-ttu-id="1a147-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="1a147-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1a147-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a147-125">-WhatIf</span></span>
<span data-ttu-id="1a147-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a147-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a147-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a147-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a147-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a147-128">-Confirm</span></span>
<span data-ttu-id="1a147-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a147-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a147-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a147-130">CommonParameters</span></span>
<span data-ttu-id="1a147-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a147-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a147-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a147-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a147-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a147-133">INPUTS</span></span>

## <span data-ttu-id="1a147-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a147-134">OUTPUTS</span></span>

## <span data-ttu-id="1a147-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a147-135">NOTES</span></span>

## <span data-ttu-id="1a147-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a147-136">RELATED LINKS</span></span>
