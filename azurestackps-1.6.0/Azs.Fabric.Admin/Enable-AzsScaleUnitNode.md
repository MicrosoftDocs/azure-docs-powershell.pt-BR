---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 932d0b77fc6df9a88a2ee13ad92856727db82f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425619"
---
# <span data-ttu-id="e53ee-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e53ee-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="e53ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e53ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e53ee-103">Parar o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="e53ee-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="e53ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e53ee-104">SYNTAX</span></span>

### <span data-ttu-id="e53ee-105">Habilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="e53ee-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53ee-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="e53ee-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e53ee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e53ee-107">DESCRIPTION</span></span>
<span data-ttu-id="e53ee-108">Parar o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="e53ee-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="e53ee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e53ee-109">EXAMPLES</span></span>

### <span data-ttu-id="e53ee-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e53ee-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="e53ee-111">Parar o modo de manutenção em um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="e53ee-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="e53ee-112">OS</span><span class="sxs-lookup"><span data-stu-id="e53ee-112">PARAMETERS</span></span>

### <span data-ttu-id="e53ee-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e53ee-113">-AsJob</span></span>
<span data-ttu-id="e53ee-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e53ee-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e53ee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e53ee-115">-Force</span></span>
<span data-ttu-id="e53ee-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e53ee-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e53ee-117">-Local</span><span class="sxs-lookup"><span data-stu-id="e53ee-117">-Location</span></span>
<span data-ttu-id="e53ee-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e53ee-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e53ee-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e53ee-119">-Name</span></span>
<span data-ttu-id="e53ee-120">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="e53ee-120">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e53ee-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e53ee-121">-ResourceGroupName</span></span>
<span data-ttu-id="e53ee-122">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="e53ee-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e53ee-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e53ee-123">-ResourceId</span></span>
<span data-ttu-id="e53ee-124">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="e53ee-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="e53ee-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e53ee-125">-Confirm</span></span>
<span data-ttu-id="e53ee-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e53ee-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e53ee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e53ee-127">-WhatIf</span></span>
<span data-ttu-id="e53ee-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e53ee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e53ee-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e53ee-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e53ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53ee-130">CommonParameters</span></span>
<span data-ttu-id="e53ee-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e53ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53ee-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e53ee-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53ee-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e53ee-133">INPUTS</span></span>

## <span data-ttu-id="e53ee-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e53ee-134">OUTPUTS</span></span>

## <span data-ttu-id="e53ee-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e53ee-135">NOTES</span></span>

## <span data-ttu-id="e53ee-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e53ee-136">RELATED LINKS</span></span>
