---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945373"
---
# <span data-ttu-id="8a599-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="8a599-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="8a599-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a599-102">SYNOPSIS</span></span>
<span data-ttu-id="8a599-103">Obtenha uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="8a599-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="8a599-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a599-104">SYNTAX</span></span>

### <span data-ttu-id="8a599-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="8a599-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a599-106">Obter</span><span class="sxs-lookup"><span data-stu-id="8a599-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a599-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a599-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a599-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a599-108">DESCRIPTION</span></span>
<span data-ttu-id="8a599-109">Obtenha uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="8a599-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="8a599-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a599-110">EXAMPLES</span></span>

### <span data-ttu-id="8a599-111">Exemplo 1: obter todas as cotas de computação</span><span class="sxs-lookup"><span data-stu-id="8a599-111">Example 1: Get All Compute Quotas</span></span>
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

<span data-ttu-id="8a599-112">Executado sem `Get-AzsComputeQuota` parâmetros para obter uma lista de todas as cotas de computação.</span><span class="sxs-lookup"><span data-stu-id="8a599-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="8a599-113">Exemplo 2: obter a cota de computação por nome</span><span class="sxs-lookup"><span data-stu-id="8a599-113">Example 2: Get Compute Quota by Name</span></span>
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

<span data-ttu-id="8a599-114">Especifique o nome da cota na linha de comando para recuperar uma cota específica.</span><span class="sxs-lookup"><span data-stu-id="8a599-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="8a599-115">OS</span><span class="sxs-lookup"><span data-stu-id="8a599-115">PARAMETERS</span></span>

### <span data-ttu-id="8a599-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a599-116">-DefaultProfile</span></span>
<span data-ttu-id="8a599-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a599-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a599-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a599-118">-InputObject</span></span>
<span data-ttu-id="8a599-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8a599-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a599-120">-Local</span><span class="sxs-lookup"><span data-stu-id="8a599-120">-Location</span></span>
<span data-ttu-id="8a599-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8a599-121">Location of the resource.</span></span>

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

### <span data-ttu-id="8a599-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a599-122">-Name</span></span>
<span data-ttu-id="8a599-123">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="8a599-123">Name of the quota.</span></span>

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

### <span data-ttu-id="8a599-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a599-124">-SubscriptionId</span></span>
<span data-ttu-id="8a599-125">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8a599-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8a599-126">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8a599-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8a599-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a599-127">CommonParameters</span></span>
<span data-ttu-id="8a599-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a599-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a599-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a599-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a599-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a599-130">INPUTS</span></span>

### <span data-ttu-id="8a599-131">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8a599-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="8a599-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a599-132">OUTPUTS</span></span>

### <span data-ttu-id="8a599-133">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="8a599-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="8a599-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a599-134">NOTES</span></span>

<span data-ttu-id="8a599-135">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8a599-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a599-136">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a599-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8a599-137">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8a599-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a599-138">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="8a599-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="8a599-139">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8a599-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a599-140">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8a599-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8a599-141">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="8a599-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="8a599-142">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="8a599-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="8a599-143">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="8a599-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="8a599-144">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="8a599-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="8a599-145">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="8a599-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="8a599-146">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8a599-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8a599-147">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8a599-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8a599-148">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="8a599-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="8a599-149">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="8a599-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="8a599-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a599-150">RELATED LINKS</span></span>

