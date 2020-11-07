---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774607"
---
# <span data-ttu-id="71c61-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="71c61-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="71c61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71c61-102">SYNOPSIS</span></span>
<span data-ttu-id="71c61-103">Repara um nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="71c61-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="71c61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71c61-104">SYNTAX</span></span>

### <span data-ttu-id="71c61-105">Reparar (padrão)</span><span class="sxs-lookup"><span data-stu-id="71c61-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71c61-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="71c61-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71c61-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71c61-107">DESCRIPTION</span></span>
<span data-ttu-id="71c61-108">Repara um nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="71c61-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="71c61-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71c61-109">EXAMPLES</span></span>

### <span data-ttu-id="71c61-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="71c61-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="71c61-111">Reparar um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="71c61-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="71c61-112">OS</span><span class="sxs-lookup"><span data-stu-id="71c61-112">PARAMETERS</span></span>

### <span data-ttu-id="71c61-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="71c61-113">-Name</span></span>
<span data-ttu-id="71c61-114">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="71c61-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="71c61-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="71c61-115">-BMCIPv4Address</span></span>
<span data-ttu-id="71c61-116">Endereço BMC da máquina física.</span><span class="sxs-lookup"><span data-stu-id="71c61-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="71c61-117">-Local</span><span class="sxs-lookup"><span data-stu-id="71c61-117">-Location</span></span>
<span data-ttu-id="71c61-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="71c61-118">Location of the resource.</span></span>

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

### <span data-ttu-id="71c61-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c61-119">-ResourceGroupName</span></span>
<span data-ttu-id="71c61-120">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="71c61-120">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="71c61-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71c61-121">-ResourceId</span></span>
<span data-ttu-id="71c61-122">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="71c61-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="71c61-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71c61-123">-AsJob</span></span>
<span data-ttu-id="71c61-124">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="71c61-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="71c61-125">-Force</span><span class="sxs-lookup"><span data-stu-id="71c61-125">-Force</span></span>
<span data-ttu-id="71c61-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="71c61-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="71c61-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71c61-127">-WhatIf</span></span>
<span data-ttu-id="71c61-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71c61-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71c61-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71c61-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71c61-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71c61-130">-Confirm</span></span>
<span data-ttu-id="71c61-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71c61-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71c61-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c61-132">CommonParameters</span></span>
<span data-ttu-id="71c61-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c61-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c61-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c61-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c61-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71c61-135">INPUTS</span></span>

## <span data-ttu-id="71c61-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71c61-136">OUTPUTS</span></span>

## <span data-ttu-id="71c61-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71c61-137">NOTES</span></span>

## <span data-ttu-id="71c61-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71c61-138">RELATED LINKS</span></span>
