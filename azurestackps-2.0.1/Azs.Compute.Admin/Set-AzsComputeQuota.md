---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945360"
---
# <span data-ttu-id="cb00e-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="cb00e-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="cb00e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb00e-102">SYNOPSIS</span></span>


## <span data-ttu-id="cb00e-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb00e-103">SYNTAX</span></span>

### <span data-ttu-id="cb00e-104">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="cb00e-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb00e-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="cb00e-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb00e-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="cb00e-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="cb00e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb00e-107">DESCRIPTION</span></span>
<span data-ttu-id="cb00e-108">Atualizar uma cota de computação</span><span class="sxs-lookup"><span data-stu-id="cb00e-108">Update a Compute Quota</span></span>

## <span data-ttu-id="cb00e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb00e-109">EXAMPLES</span></span>

### <span data-ttu-id="cb00e-110">Exemplo 1: definir propriedades em uma cota de computação existente</span><span class="sxs-lookup"><span data-stu-id="cb00e-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="cb00e-111">Defina os parâmetros especificados na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="cb00e-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="cb00e-112">Todos os parâmetros não definidos serão padronizados como 0</span><span class="sxs-lookup"><span data-stu-id="cb00e-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="cb00e-113">OS</span><span class="sxs-lookup"><span data-stu-id="cb00e-113">PARAMETERS</span></span>

### <span data-ttu-id="cb00e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb00e-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="cb00e-115">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="cb00e-115">-NewQuota</span></span>
<span data-ttu-id="cb00e-116">Para construir, consulte a seção notas para propriedades NEWQUOTA e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cb00e-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cb00e-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb00e-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="cb00e-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb00e-118">-Confirm</span></span>
<span data-ttu-id="cb00e-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb00e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb00e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb00e-120">-WhatIf</span></span>
<span data-ttu-id="cb00e-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb00e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb00e-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb00e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb00e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb00e-123">CommonParameters</span></span>
<span data-ttu-id="cb00e-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb00e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb00e-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb00e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb00e-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb00e-126">INPUTS</span></span>

### <span data-ttu-id="cb00e-127">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="cb00e-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="cb00e-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb00e-128">OUTPUTS</span></span>

### <span data-ttu-id="cb00e-129">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="cb00e-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="cb00e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb00e-130">NOTES</span></span>

<span data-ttu-id="cb00e-131">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="cb00e-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb00e-132">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb00e-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cb00e-133">NEWQUOTA <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="cb00e-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="cb00e-134">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="cb00e-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cb00e-135">`[AvailabilitySetCount <Int32?>]`: Número máximo de conjuntos de disponibilidade permitidos.</span><span class="sxs-lookup"><span data-stu-id="cb00e-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="cb00e-136">`[CoresLimit <Int32?>]`: Número máximo de núcleos permitidos.</span><span class="sxs-lookup"><span data-stu-id="cb00e-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="cb00e-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Número máximo de discos gerenciados e instantâneos do tipo Premium permitidos.</span><span class="sxs-lookup"><span data-stu-id="cb00e-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="cb00e-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: O número máximo de discos gerenciados e instantâneos do tipo padrão são permitidos.</span><span class="sxs-lookup"><span data-stu-id="cb00e-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="cb00e-139">`[VMScaleSetCount <Int32?>]`: Número máximo de conjuntos de escala permitidos.</span><span class="sxs-lookup"><span data-stu-id="cb00e-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="cb00e-140">`[VirtualMachineCount <Int32?>]`: Número máximo de máquinas virtuais permitidas.</span><span class="sxs-lookup"><span data-stu-id="cb00e-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="cb00e-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb00e-141">RELATED LINKS</span></span>

