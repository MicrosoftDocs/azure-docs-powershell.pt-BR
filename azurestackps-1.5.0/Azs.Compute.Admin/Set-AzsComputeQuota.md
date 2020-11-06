---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4caf955c25cd29c9cc9c09f1182454ee3a4d56df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426177"
---
# <span data-ttu-id="85dcc-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="85dcc-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="85dcc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="85dcc-103">Atualize uma cota de computação existente usando os parâmetros fornecidos.</span><span class="sxs-lookup"><span data-stu-id="85dcc-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="85dcc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85dcc-104">SYNTAX</span></span>

### <span data-ttu-id="85dcc-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="85dcc-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85dcc-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="85dcc-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85dcc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="85dcc-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85dcc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85dcc-108">DESCRIPTION</span></span>
<span data-ttu-id="85dcc-109">Atualize uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="85dcc-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="85dcc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85dcc-110">EXAMPLES</span></span>

### <span data-ttu-id="85dcc-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="85dcc-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="85dcc-112">Atualize uma cota de computação.</span><span class="sxs-lookup"><span data-stu-id="85dcc-112">Update a compute quota.</span></span>

## <span data-ttu-id="85dcc-113">OS</span><span class="sxs-lookup"><span data-stu-id="85dcc-113">PARAMETERS</span></span>

### <span data-ttu-id="85dcc-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="85dcc-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="85dcc-115">Número de conjuntos de disponibilidade permitidos.</span><span class="sxs-lookup"><span data-stu-id="85dcc-115">Number of availability sets allowed.</span></span>

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

### <span data-ttu-id="85dcc-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="85dcc-116">-CoresCount</span></span>
<span data-ttu-id="85dcc-117">Número de núcleos permitidos.</span><span class="sxs-lookup"><span data-stu-id="85dcc-117">Number of cores allowed.</span></span>

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

### <span data-ttu-id="85dcc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85dcc-118">-InputObject</span></span>
<span data-ttu-id="85dcc-119">Cota de computação possivelmente modificada Get-AzsComputeQuota de forma retornado.</span><span class="sxs-lookup"><span data-stu-id="85dcc-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

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

### <span data-ttu-id="85dcc-120">-Local</span><span class="sxs-lookup"><span data-stu-id="85dcc-120">-Location</span></span>
<span data-ttu-id="85dcc-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="85dcc-121">Location of the resource.</span></span>

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

### <span data-ttu-id="85dcc-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="85dcc-122">-Name</span></span>
<span data-ttu-id="85dcc-123">O nome da cota.</span><span class="sxs-lookup"><span data-stu-id="85dcc-123">The name of the quota.</span></span>

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

### <span data-ttu-id="85dcc-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="85dcc-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="85dcc-125">Tamanho para discos gerenciados padrão e instantâneos permitidos.</span><span class="sxs-lookup"><span data-stu-id="85dcc-125">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="85dcc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85dcc-126">-ResourceId</span></span>
<span data-ttu-id="85dcc-127">A ID da cota de computação do ARM.</span><span class="sxs-lookup"><span data-stu-id="85dcc-127">The ARM compute quota id.</span></span>

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

### <span data-ttu-id="85dcc-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="85dcc-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="85dcc-129">Tamanho para discos gerenciados padrão e instantâneos permitidos.</span><span class="sxs-lookup"><span data-stu-id="85dcc-129">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="85dcc-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="85dcc-130">-VirtualMachineCount</span></span>
<span data-ttu-id="85dcc-131">Número de máquinas virtuais permitidas.</span><span class="sxs-lookup"><span data-stu-id="85dcc-131">Number of virtual machines allowed.</span></span>

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

### <span data-ttu-id="85dcc-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="85dcc-132">-VmScaleSetCount</span></span>
<span data-ttu-id="85dcc-133">Número de conjuntos de escala permitidos.</span><span class="sxs-lookup"><span data-stu-id="85dcc-133">Number of scale sets allowed.</span></span>

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

### <span data-ttu-id="85dcc-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85dcc-134">-Confirm</span></span>
<span data-ttu-id="85dcc-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85dcc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85dcc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85dcc-136">-WhatIf</span></span>
<span data-ttu-id="85dcc-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85dcc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85dcc-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85dcc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85dcc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85dcc-139">CommonParameters</span></span>
<span data-ttu-id="85dcc-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85dcc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85dcc-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85dcc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85dcc-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85dcc-142">INPUTS</span></span>

## <span data-ttu-id="85dcc-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85dcc-143">OUTPUTS</span></span>

### <span data-ttu-id="85dcc-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="85dcc-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="85dcc-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85dcc-145">NOTES</span></span>

## <span data-ttu-id="85dcc-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85dcc-146">RELATED LINKS</span></span>

