---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945371"
---
# <span data-ttu-id="6247b-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="6247b-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="6247b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6247b-102">SYNOPSIS</span></span>
<span data-ttu-id="6247b-103">Cria ou atualiza uma cota de computação com os parâmetros de cota fornecidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="6247b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6247b-104">SYNTAX</span></span>

### <span data-ttu-id="6247b-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="6247b-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6247b-106">Criados</span><span class="sxs-lookup"><span data-stu-id="6247b-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6247b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6247b-107">DESCRIPTION</span></span>
<span data-ttu-id="6247b-108">Cria ou atualiza uma cota de computação com os parâmetros de cota fornecidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="6247b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6247b-109">EXAMPLES</span></span>

### <span data-ttu-id="6247b-110">Exemplo 1: criar uma cota de computação com parâmetros padrão</span><span class="sxs-lookup"><span data-stu-id="6247b-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="6247b-111">Todos os parâmetros que não forem especificados serão definidos como o parâmetro padrão, mostrado acima.</span><span class="sxs-lookup"><span data-stu-id="6247b-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="6247b-112">Exemplo 2: criar uma cota de computação com parâmetros personalizados</span><span class="sxs-lookup"><span data-stu-id="6247b-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="6247b-113">Personalize a cota com parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6247b-113">Customize Quota with parameters.</span></span> <span data-ttu-id="6247b-114">Qualquer parâmetro não especificado terá o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="6247b-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="6247b-115">OS</span><span class="sxs-lookup"><span data-stu-id="6247b-115">PARAMETERS</span></span>

### <span data-ttu-id="6247b-116">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="6247b-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="6247b-117">Número máximo de conjuntos de disponibilidade permitidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="6247b-118">-CoresCount</span></span>
<span data-ttu-id="6247b-119">Número máximo de núcleos permitido.</span><span class="sxs-lookup"><span data-stu-id="6247b-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6247b-120">-DefaultProfile</span></span>
<span data-ttu-id="6247b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6247b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-122">-Local</span><span class="sxs-lookup"><span data-stu-id="6247b-122">-Location</span></span>
<span data-ttu-id="6247b-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6247b-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="6247b-124">-Location1</span></span>
<span data-ttu-id="6247b-125">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6247b-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="6247b-126">-Name</span></span>
<span data-ttu-id="6247b-127">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="6247b-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-128">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="6247b-128">-NewQuota</span></span>
<span data-ttu-id="6247b-129">Armazena informações de cota de computação usadas para controlar a alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="6247b-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="6247b-130">Para construir, consulte a seção notas para propriedades NEWQUOTA e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6247b-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="6247b-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="6247b-132">Número máximo de discos gerenciados e instantâneos do tipo Premium permitidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-133">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="6247b-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="6247b-134">Número máximo de discos gerenciados e instantâneos do tipo padrão permitidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6247b-135">-SubscriptionId</span></span>
<span data-ttu-id="6247b-136">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6247b-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6247b-137">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6247b-137">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="6247b-138">-VirtualMachineCount</span></span>
<span data-ttu-id="6247b-139">Número máximo de máquinas virtuais permitidas.</span><span class="sxs-lookup"><span data-stu-id="6247b-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="6247b-140">-VMScaleSetCount</span></span>
<span data-ttu-id="6247b-141">Número máximo de conjuntos de escala permitidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6247b-142">-Confirm</span></span>
<span data-ttu-id="6247b-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6247b-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6247b-144">-WhatIf</span></span>
<span data-ttu-id="6247b-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6247b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6247b-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6247b-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6247b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6247b-147">CommonParameters</span></span>
<span data-ttu-id="6247b-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6247b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6247b-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6247b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6247b-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6247b-150">INPUTS</span></span>

### <span data-ttu-id="6247b-151">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="6247b-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="6247b-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6247b-152">OUTPUTS</span></span>

### <span data-ttu-id="6247b-153">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="6247b-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="6247b-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6247b-154">NOTES</span></span>

<span data-ttu-id="6247b-155">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6247b-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6247b-156">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6247b-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6247b-157">NEWQUOTA <IQuota> : armazena informações de cota de computação usadas para controlar a alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="6247b-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="6247b-158">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6247b-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6247b-159">`[AvailabilitySetCount <Int32?>]`: Número máximo de conjuntos de disponibilidade permitidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="6247b-160">`[CoresLimit <Int32?>]`: Número máximo de núcleos permitidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="6247b-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Número máximo de discos gerenciados e instantâneos do tipo Premium permitidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="6247b-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: O número máximo de discos gerenciados e instantâneos do tipo padrão são permitidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="6247b-163">`[VMScaleSetCount <Int32?>]`: Número máximo de conjuntos de escala permitidos.</span><span class="sxs-lookup"><span data-stu-id="6247b-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="6247b-164">`[VirtualMachineCount <Int32?>]`: Número máximo de máquinas virtuais permitidas.</span><span class="sxs-lookup"><span data-stu-id="6247b-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="6247b-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6247b-165">RELATED LINKS</span></span>

