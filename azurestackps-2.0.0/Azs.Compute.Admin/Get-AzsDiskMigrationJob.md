---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777188"
---
# <span data-ttu-id="93600-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="93600-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="93600-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93600-102">SYNOPSIS</span></span>
<span data-ttu-id="93600-103">Retorna o trabalho de migração de disco solicitado.</span><span class="sxs-lookup"><span data-stu-id="93600-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="93600-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93600-104">SYNTAX</span></span>

### <span data-ttu-id="93600-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="93600-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93600-106">Obter</span><span class="sxs-lookup"><span data-stu-id="93600-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93600-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93600-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="93600-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93600-108">DESCRIPTION</span></span>
<span data-ttu-id="93600-109">Retorna o trabalho de migração de disco solicitado.</span><span class="sxs-lookup"><span data-stu-id="93600-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="93600-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93600-110">EXAMPLES</span></span>

### <span data-ttu-id="93600-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="93600-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="93600-112">Retorna uma lista de trabalhos de migração de disco gerenciados no local local.</span><span class="sxs-lookup"><span data-stu-id="93600-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="93600-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="93600-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="93600-114">Obtenha um trabalho específico de migração de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="93600-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="93600-115">OS</span><span class="sxs-lookup"><span data-stu-id="93600-115">PARAMETERS</span></span>

### <span data-ttu-id="93600-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93600-116">-DefaultProfile</span></span>
<span data-ttu-id="93600-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93600-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93600-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93600-118">-InputObject</span></span>
<span data-ttu-id="93600-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="93600-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="93600-120">-Local</span><span class="sxs-lookup"><span data-stu-id="93600-120">-Location</span></span>
<span data-ttu-id="93600-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="93600-121">Location of the resource.</span></span>

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

### <span data-ttu-id="93600-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="93600-122">-Name</span></span>
<span data-ttu-id="93600-123">O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="93600-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="93600-124">-Status</span><span class="sxs-lookup"><span data-stu-id="93600-124">-Status</span></span>
<span data-ttu-id="93600-125">Os parâmetros do status do trabalho de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="93600-125">The parameters of disk migration job status.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="93600-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93600-126">-SubscriptionId</span></span>
<span data-ttu-id="93600-127">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="93600-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="93600-128">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="93600-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="93600-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93600-129">CommonParameters</span></span>
<span data-ttu-id="93600-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93600-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93600-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93600-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93600-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93600-132">INPUTS</span></span>

### <span data-ttu-id="93600-133">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="93600-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="93600-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93600-134">OUTPUTS</span></span>

### <span data-ttu-id="93600-135">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="93600-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="93600-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93600-136">NOTES</span></span>

<span data-ttu-id="93600-137">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="93600-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93600-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93600-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="93600-139">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="93600-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93600-140">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="93600-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="93600-141">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="93600-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93600-142">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="93600-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="93600-143">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="93600-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="93600-144">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="93600-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="93600-145">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="93600-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="93600-146">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="93600-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="93600-147">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="93600-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="93600-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="93600-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="93600-149">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="93600-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="93600-150">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="93600-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="93600-151">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="93600-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="93600-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93600-152">RELATED LINKS</span></span>

