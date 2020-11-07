---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8da912ed9751231a44c34b27df36abc62d55c4ab
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774655"
---
# <span data-ttu-id="bdcd2-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="bdcd2-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="bdcd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdcd2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcd2-103">Atualize uma cota de computação existente usando os parâmetros fornecidos.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="bdcd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdcd2-104">SYNTAX</span></span>

### <span data-ttu-id="bdcd2-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="bdcd2-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdcd2-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="bdcd2-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdcd2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bdcd2-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdcd2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdcd2-108">DESCRIPTION</span></span>
<span data-ttu-id="bdcd2-109">Atualize uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="bdcd2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdcd2-110">EXAMPLES</span></span>

### <span data-ttu-id="bdcd2-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bdcd2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="bdcd2-112">Atualize uma cota de computação.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-112">Update a compute quota.</span></span>

## <span data-ttu-id="bdcd2-113">OS</span><span class="sxs-lookup"><span data-stu-id="bdcd2-113">PARAMETERS</span></span>

### <span data-ttu-id="bdcd2-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="bdcd2-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="bdcd2-115">Número de conjuntos de disponibilidade permitidos.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="bdcd2-116">-CoresCount</span></span>
<span data-ttu-id="bdcd2-117">Número de núcleos permitidos.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdcd2-118">-InputObject</span></span>
<span data-ttu-id="bdcd2-119">Cota de computação possivelmente modificada Get-AzsComputeQuota de forma retornado.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-120">-Local</span><span class="sxs-lookup"><span data-stu-id="bdcd2-120">-Location</span></span>
<span data-ttu-id="bdcd2-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdcd2-122">-Name</span></span>
<span data-ttu-id="bdcd2-123">O nome da cota.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="bdcd2-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="bdcd2-125">Tamanho para discos gerenciados padrão e instantâneos permitidos.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdcd2-126">-ResourceId</span></span>
<span data-ttu-id="bdcd2-127">A ID da cota de computação do ARM.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="bdcd2-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="bdcd2-129">Tamanho para discos gerenciados padrão e instantâneos permitidos.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="bdcd2-130">-VirtualMachineCount</span></span>
<span data-ttu-id="bdcd2-131">Número de máquinas virtuais permitidas.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="bdcd2-132">-VmScaleSetCount</span></span>
<span data-ttu-id="bdcd2-133">Número de conjuntos de escala permitidos.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcd2-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bdcd2-134">-Confirm</span></span>
<span data-ttu-id="bdcd2-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdcd2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdcd2-136">-WhatIf</span></span>
<span data-ttu-id="bdcd2-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdcd2-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdcd2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcd2-139">CommonParameters</span></span>
<span data-ttu-id="bdcd2-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdcd2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdcd2-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdcd2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcd2-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdcd2-142">INPUTS</span></span>

## <span data-ttu-id="bdcd2-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdcd2-143">OUTPUTS</span></span>

### <span data-ttu-id="bdcd2-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="bdcd2-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="bdcd2-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdcd2-145">NOTES</span></span>

## <span data-ttu-id="bdcd2-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdcd2-146">RELATED LINKS</span></span>
