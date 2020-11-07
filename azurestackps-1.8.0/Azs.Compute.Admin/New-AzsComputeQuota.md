---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffd2667f8c07c5b0594abe38f6cee5d40ce91a49
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774669"
---
# <span data-ttu-id="08a37-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="08a37-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="08a37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08a37-102">SYNOPSIS</span></span>
<span data-ttu-id="08a37-103">Crie uma nova cota de computação usada para limitar os recursos de computação.</span><span class="sxs-lookup"><span data-stu-id="08a37-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="08a37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08a37-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08a37-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08a37-105">DESCRIPTION</span></span>
<span data-ttu-id="08a37-106">Criar uma nova cota de computação.</span><span class="sxs-lookup"><span data-stu-id="08a37-106">Create a new compute quota.</span></span>

## <span data-ttu-id="08a37-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08a37-107">EXAMPLES</span></span>

### <span data-ttu-id="08a37-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="08a37-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="08a37-109">Criar uma nova cota de computação.</span><span class="sxs-lookup"><span data-stu-id="08a37-109">Create a new compute quota.</span></span>

## <span data-ttu-id="08a37-110">OS</span><span class="sxs-lookup"><span data-stu-id="08a37-110">PARAMETERS</span></span>

### <span data-ttu-id="08a37-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="08a37-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="08a37-112">Número de conjuntos de disponibilidade permitidos.</span><span class="sxs-lookup"><span data-stu-id="08a37-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a37-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="08a37-113">-CoresCount</span></span>
<span data-ttu-id="08a37-114">Número de núcleos permitidos.</span><span class="sxs-lookup"><span data-stu-id="08a37-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a37-115">-Local</span><span class="sxs-lookup"><span data-stu-id="08a37-115">-Location</span></span>
<span data-ttu-id="08a37-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="08a37-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a37-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="08a37-117">-Name</span></span>
<span data-ttu-id="08a37-118">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="08a37-118">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a37-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="08a37-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="08a37-120">Tamanho para discos gerenciados padrão e instantâneos permitidos.</span><span class="sxs-lookup"><span data-stu-id="08a37-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a37-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="08a37-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="08a37-122">Tamanho para discos gerenciados padrão e instantâneos permitidos.</span><span class="sxs-lookup"><span data-stu-id="08a37-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a37-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="08a37-123">-VirtualMachineCount</span></span>
<span data-ttu-id="08a37-124">Número de máquinas virtuais permitidas.</span><span class="sxs-lookup"><span data-stu-id="08a37-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a37-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="08a37-125">-VmScaleSetCount</span></span>
<span data-ttu-id="08a37-126">Número de conjuntos de escala permitidos.</span><span class="sxs-lookup"><span data-stu-id="08a37-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a37-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="08a37-127">-Confirm</span></span>
<span data-ttu-id="08a37-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08a37-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08a37-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08a37-129">-WhatIf</span></span>
<span data-ttu-id="08a37-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08a37-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08a37-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08a37-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08a37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a37-132">CommonParameters</span></span>
<span data-ttu-id="08a37-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08a37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a37-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08a37-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a37-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08a37-135">INPUTS</span></span>

## <span data-ttu-id="08a37-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08a37-136">OUTPUTS</span></span>

### <span data-ttu-id="08a37-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="08a37-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="08a37-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08a37-138">NOTES</span></span>

## <span data-ttu-id="08a37-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08a37-139">RELATED LINKS</span></span>

