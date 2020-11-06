---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc92bcc617c771c15330d1a24e8ed24466f7ffc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425884"
---
# <span data-ttu-id="380a5-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="380a5-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="380a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="380a5-102">SYNOPSIS</span></span>
<span data-ttu-id="380a5-103">Crie uma nova cota de computação usada para limitar os recursos de computação.</span><span class="sxs-lookup"><span data-stu-id="380a5-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="380a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="380a5-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="380a5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="380a5-105">DESCRIPTION</span></span>
<span data-ttu-id="380a5-106">Criar uma nova cota de computação.</span><span class="sxs-lookup"><span data-stu-id="380a5-106">Create a new compute quota.</span></span>

## <span data-ttu-id="380a5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="380a5-107">EXAMPLES</span></span>

### <span data-ttu-id="380a5-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="380a5-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="380a5-109">Criar uma nova cota de computação.</span><span class="sxs-lookup"><span data-stu-id="380a5-109">Create a new compute quota.</span></span>

## <span data-ttu-id="380a5-110">OS</span><span class="sxs-lookup"><span data-stu-id="380a5-110">PARAMETERS</span></span>

### <span data-ttu-id="380a5-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="380a5-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="380a5-112">Número de conjuntos de disponibilidade permitidos.</span><span class="sxs-lookup"><span data-stu-id="380a5-112">Number  of availability sets allowed.</span></span>

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

### <span data-ttu-id="380a5-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="380a5-113">-CoresCount</span></span>
<span data-ttu-id="380a5-114">Número de núcleos permitidos.</span><span class="sxs-lookup"><span data-stu-id="380a5-114">Number  of cores allowed.</span></span>

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

### <span data-ttu-id="380a5-115">-Local</span><span class="sxs-lookup"><span data-stu-id="380a5-115">-Location</span></span>
<span data-ttu-id="380a5-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="380a5-116">Location of the resource.</span></span>

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

### <span data-ttu-id="380a5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="380a5-117">-Name</span></span>
<span data-ttu-id="380a5-118">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="380a5-118">Name of the quota.</span></span>

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

### <span data-ttu-id="380a5-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="380a5-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="380a5-120">Tamanho para discos gerenciados padrão e instantâneos permitidos.</span><span class="sxs-lookup"><span data-stu-id="380a5-120">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="380a5-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="380a5-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="380a5-122">Tamanho para discos gerenciados padrão e instantâneos permitidos.</span><span class="sxs-lookup"><span data-stu-id="380a5-122">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="380a5-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="380a5-123">-VirtualMachineCount</span></span>
<span data-ttu-id="380a5-124">Número de máquinas virtuais permitidas.</span><span class="sxs-lookup"><span data-stu-id="380a5-124">Number  of virtual machines allowed.</span></span>

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

### <span data-ttu-id="380a5-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="380a5-125">-VmScaleSetCount</span></span>
<span data-ttu-id="380a5-126">Número de conjuntos de escala permitidos.</span><span class="sxs-lookup"><span data-stu-id="380a5-126">Number  of scale sets allowed.</span></span>

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

### <span data-ttu-id="380a5-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="380a5-127">-Confirm</span></span>
<span data-ttu-id="380a5-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380a5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="380a5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="380a5-129">-WhatIf</span></span>
<span data-ttu-id="380a5-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="380a5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="380a5-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="380a5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="380a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380a5-132">CommonParameters</span></span>
<span data-ttu-id="380a5-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380a5-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="380a5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380a5-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="380a5-135">INPUTS</span></span>

## <span data-ttu-id="380a5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="380a5-136">OUTPUTS</span></span>

### <span data-ttu-id="380a5-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="380a5-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="380a5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="380a5-138">NOTES</span></span>

## <span data-ttu-id="380a5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="380a5-139">RELATED LINKS</span></span>
