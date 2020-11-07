---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777187"
---
# <span data-ttu-id="be75f-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="be75f-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="be75f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be75f-102">SYNOPSIS</span></span>
<span data-ttu-id="be75f-103">Obtenha uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="be75f-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="be75f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be75f-104">SYNTAX</span></span>

### <span data-ttu-id="be75f-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="be75f-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="be75f-106">Obter</span><span class="sxs-lookup"><span data-stu-id="be75f-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="be75f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="be75f-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="be75f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be75f-108">DESCRIPTION</span></span>
<span data-ttu-id="be75f-109">Obtenha uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="be75f-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="be75f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be75f-110">EXAMPLES</span></span>

### <span data-ttu-id="be75f-111">Exemplo 1: obter todas as cotas de computação</span><span class="sxs-lookup"><span data-stu-id="be75f-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="be75f-112">Executado sem `Get-AzsComputeQuota` parâmetros para obter uma lista de todas as cotas de computação.</span><span class="sxs-lookup"><span data-stu-id="be75f-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="be75f-113">Exemplo 2: obter a cota de computação por nome</span><span class="sxs-lookup"><span data-stu-id="be75f-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

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

<span data-ttu-id="be75f-114">Especifique o nome da cota na linha de comando para recuperar uma cota específica.</span><span class="sxs-lookup"><span data-stu-id="be75f-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="be75f-115">OS</span><span class="sxs-lookup"><span data-stu-id="be75f-115">PARAMETERS</span></span>

### <span data-ttu-id="be75f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be75f-116">-DefaultProfile</span></span>
<span data-ttu-id="be75f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be75f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be75f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be75f-118">-InputObject</span></span>
<span data-ttu-id="be75f-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="be75f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="be75f-120">-Local</span><span class="sxs-lookup"><span data-stu-id="be75f-120">-Location</span></span>
<span data-ttu-id="be75f-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="be75f-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="be75f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="be75f-122">-Name</span></span>
<span data-ttu-id="be75f-123">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="be75f-123">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="be75f-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be75f-124">-SubscriptionId</span></span>
<span data-ttu-id="be75f-125">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be75f-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="be75f-126">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="be75f-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="be75f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be75f-127">CommonParameters</span></span>
<span data-ttu-id="be75f-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be75f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be75f-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be75f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be75f-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be75f-130">INPUTS</span></span>

### <span data-ttu-id="be75f-131">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="be75f-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="be75f-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be75f-132">OUTPUTS</span></span>

### <span data-ttu-id="be75f-133">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="be75f-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="be75f-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be75f-134">NOTES</span></span>

<span data-ttu-id="be75f-135">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="be75f-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be75f-136">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be75f-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="be75f-137">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="be75f-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be75f-138">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="be75f-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="be75f-139">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="be75f-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be75f-140">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="be75f-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="be75f-141">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="be75f-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="be75f-142">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="be75f-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="be75f-143">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="be75f-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="be75f-144">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="be75f-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="be75f-145">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="be75f-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="be75f-146">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be75f-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="be75f-147">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="be75f-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="be75f-148">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="be75f-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="be75f-149">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="be75f-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="be75f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be75f-150">RELATED LINKS</span></span>

