---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774891"
---
# <span data-ttu-id="308df-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="308df-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="308df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="308df-102">SYNOPSIS</span></span>
<span data-ttu-id="308df-103">Repara um nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="308df-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="308df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="308df-104">SYNTAX</span></span>

### <span data-ttu-id="308df-105">Reparar (padrão)</span><span class="sxs-lookup"><span data-stu-id="308df-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="308df-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="308df-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="308df-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="308df-107">DESCRIPTION</span></span>
<span data-ttu-id="308df-108">Repara um nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="308df-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="308df-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="308df-109">EXAMPLES</span></span>

### <span data-ttu-id="308df-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="308df-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="308df-111">Reparar um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="308df-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="308df-112">OS</span><span class="sxs-lookup"><span data-stu-id="308df-112">PARAMETERS</span></span>

### <span data-ttu-id="308df-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="308df-113">-Name</span></span>
<span data-ttu-id="308df-114">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="308df-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308df-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="308df-115">-BMCIPv4Address</span></span>
<span data-ttu-id="308df-116">Endereço BMC da máquina física.</span><span class="sxs-lookup"><span data-stu-id="308df-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308df-117">-Local</span><span class="sxs-lookup"><span data-stu-id="308df-117">-Location</span></span>
<span data-ttu-id="308df-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="308df-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="308df-119">-ResourceGroupName</span></span>
<span data-ttu-id="308df-120">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="308df-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308df-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="308df-121">-ResourceId</span></span>
<span data-ttu-id="308df-122">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="308df-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="308df-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="308df-123">-AsJob</span></span>
<span data-ttu-id="308df-124">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="308df-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="308df-125">-Force</span><span class="sxs-lookup"><span data-stu-id="308df-125">-Force</span></span>
<span data-ttu-id="308df-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="308df-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="308df-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="308df-127">-WhatIf</span></span>
<span data-ttu-id="308df-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="308df-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="308df-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="308df-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="308df-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="308df-130">-Confirm</span></span>
<span data-ttu-id="308df-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="308df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="308df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308df-132">CommonParameters</span></span>
<span data-ttu-id="308df-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="308df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308df-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="308df-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308df-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="308df-135">INPUTS</span></span>

## <span data-ttu-id="308df-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="308df-136">OUTPUTS</span></span>

## <span data-ttu-id="308df-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="308df-137">NOTES</span></span>

## <span data-ttu-id="308df-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="308df-138">RELATED LINKS</span></span>
