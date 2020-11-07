---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70ee408b65839e46e408256780a6d705c9881bde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774542"
---
# <span data-ttu-id="0e8dd-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="0e8dd-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="0e8dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e8dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8dd-103">Inicie o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="0e8dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e8dd-104">SYNTAX</span></span>

### <span data-ttu-id="0e8dd-105">Desabilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="0e8dd-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8dd-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="0e8dd-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e8dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e8dd-107">DESCRIPTION</span></span>
<span data-ttu-id="0e8dd-108">Inicie o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="0e8dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e8dd-109">EXAMPLES</span></span>

### <span data-ttu-id="0e8dd-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0e8dd-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="0e8dd-111">Habilite o modo de manutenção para um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="0e8dd-112">OS</span><span class="sxs-lookup"><span data-stu-id="0e8dd-112">PARAMETERS</span></span>

### <span data-ttu-id="0e8dd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e8dd-113">-AsJob</span></span>
<span data-ttu-id="0e8dd-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0e8dd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0e8dd-115">-Force</span></span>
<span data-ttu-id="0e8dd-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0e8dd-117">-Local</span><span class="sxs-lookup"><span data-stu-id="0e8dd-117">-Location</span></span>
<span data-ttu-id="0e8dd-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-118">Location of the resource.</span></span>

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

### <span data-ttu-id="0e8dd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e8dd-119">-Name</span></span>
<span data-ttu-id="0e8dd-120">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="0e8dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e8dd-122">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0e8dd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e8dd-123">-ResourceId</span></span>
<span data-ttu-id="0e8dd-124">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="0e8dd-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0e8dd-125">-Confirm</span></span>
<span data-ttu-id="0e8dd-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8dd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8dd-127">-WhatIf</span></span>
<span data-ttu-id="0e8dd-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8dd-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8dd-130">CommonParameters</span></span>
<span data-ttu-id="0e8dd-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e8dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8dd-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e8dd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8dd-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e8dd-133">INPUTS</span></span>

## <span data-ttu-id="0e8dd-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e8dd-134">OUTPUTS</span></span>

## <span data-ttu-id="0e8dd-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e8dd-135">NOTES</span></span>

## <span data-ttu-id="0e8dd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e8dd-136">RELATED LINKS</span></span>

