---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426193"
---
# <span data-ttu-id="70e99-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="70e99-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="70e99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70e99-102">SYNOPSIS</span></span>
<span data-ttu-id="70e99-103">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="70e99-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="70e99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70e99-104">SYNTAX</span></span>

### <span data-ttu-id="70e99-105">Parar (padrão)</span><span class="sxs-lookup"><span data-stu-id="70e99-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70e99-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="70e99-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70e99-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70e99-107">DESCRIPTION</span></span>
<span data-ttu-id="70e99-108">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="70e99-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="70e99-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70e99-109">EXAMPLES</span></span>

### <span data-ttu-id="70e99-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="70e99-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="70e99-111">Desligar um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="70e99-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="70e99-112">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="70e99-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="70e99-113">Desligue um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="70e99-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="70e99-114">OS</span><span class="sxs-lookup"><span data-stu-id="70e99-114">PARAMETERS</span></span>

### <span data-ttu-id="70e99-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70e99-115">-AsJob</span></span>
<span data-ttu-id="70e99-116">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="70e99-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="70e99-117">-Force</span><span class="sxs-lookup"><span data-stu-id="70e99-117">-Force</span></span>
<span data-ttu-id="70e99-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="70e99-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="70e99-119">-Local</span><span class="sxs-lookup"><span data-stu-id="70e99-119">-Location</span></span>
<span data-ttu-id="70e99-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="70e99-120">Location of the resource.</span></span>

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

### <span data-ttu-id="70e99-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="70e99-121">-Name</span></span>
<span data-ttu-id="70e99-122">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="70e99-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="70e99-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e99-123">-ResourceGroupName</span></span>
<span data-ttu-id="70e99-124">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="70e99-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="70e99-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70e99-125">-ResourceId</span></span>
<span data-ttu-id="70e99-126">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="70e99-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="70e99-127">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="70e99-127">-Shutdown</span></span>
<span data-ttu-id="70e99-128">Se definido normalmente desliga o nó da unidade de escala; caso contrário, desligue o nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="70e99-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="70e99-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="70e99-129">-Confirm</span></span>
<span data-ttu-id="70e99-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70e99-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70e99-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70e99-131">-WhatIf</span></span>
<span data-ttu-id="70e99-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70e99-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70e99-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70e99-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70e99-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e99-134">CommonParameters</span></span>
<span data-ttu-id="70e99-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e99-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e99-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70e99-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e99-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70e99-137">INPUTS</span></span>

## <span data-ttu-id="70e99-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70e99-138">OUTPUTS</span></span>

## <span data-ttu-id="70e99-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70e99-139">NOTES</span></span>

## <span data-ttu-id="70e99-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70e99-140">RELATED LINKS</span></span>

