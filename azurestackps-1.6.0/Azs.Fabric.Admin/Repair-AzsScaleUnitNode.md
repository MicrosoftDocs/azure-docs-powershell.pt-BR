---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ad784757210273cd2e456069c8d3a759e973a0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425648"
---
# <span data-ttu-id="b6c56-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b6c56-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b6c56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6c56-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c56-103">Repara um nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="b6c56-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="b6c56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6c56-104">SYNTAX</span></span>

### <span data-ttu-id="b6c56-105">Reparar (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6c56-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6c56-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="b6c56-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6c56-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6c56-107">DESCRIPTION</span></span>
<span data-ttu-id="b6c56-108">Repara um nó do cluster.</span><span class="sxs-lookup"><span data-stu-id="b6c56-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="b6c56-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6c56-109">EXAMPLES</span></span>

### <span data-ttu-id="b6c56-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b6c56-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="b6c56-111">Reparar um nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b6c56-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="b6c56-112">OS</span><span class="sxs-lookup"><span data-stu-id="b6c56-112">PARAMETERS</span></span>

### <span data-ttu-id="b6c56-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6c56-113">-AsJob</span></span>
<span data-ttu-id="b6c56-114">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b6c56-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b6c56-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="b6c56-115">-BMCIPv4Address</span></span>
<span data-ttu-id="b6c56-116">Endereço BMC da máquina física.</span><span class="sxs-lookup"><span data-stu-id="b6c56-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="b6c56-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b6c56-117">-Force</span></span>
<span data-ttu-id="b6c56-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b6c56-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b6c56-119">-Local</span><span class="sxs-lookup"><span data-stu-id="b6c56-119">-Location</span></span>
<span data-ttu-id="b6c56-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b6c56-120">Location of the resource.</span></span>

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

### <span data-ttu-id="b6c56-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6c56-121">-Name</span></span>
<span data-ttu-id="b6c56-122">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b6c56-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="b6c56-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6c56-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6c56-124">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="b6c56-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b6c56-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c56-125">-ResourceId</span></span>
<span data-ttu-id="b6c56-126">ID do recurso do nó de unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="b6c56-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="b6c56-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6c56-127">-Confirm</span></span>
<span data-ttu-id="b6c56-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c56-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6c56-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6c56-129">-WhatIf</span></span>
<span data-ttu-id="b6c56-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6c56-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6c56-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6c56-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6c56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c56-132">CommonParameters</span></span>
<span data-ttu-id="b6c56-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c56-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6c56-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c56-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6c56-135">INPUTS</span></span>

## <span data-ttu-id="b6c56-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6c56-136">OUTPUTS</span></span>

## <span data-ttu-id="b6c56-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6c56-137">NOTES</span></span>

## <span data-ttu-id="b6c56-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6c56-138">RELATED LINKS</span></span>

