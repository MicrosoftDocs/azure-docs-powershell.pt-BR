---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945278"
---
# <span data-ttu-id="19d49-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="19d49-101">Get-AzsDisk</span></span>

## <span data-ttu-id="19d49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19d49-102">SYNOPSIS</span></span>
<span data-ttu-id="19d49-103">Retorna o disco.</span><span class="sxs-lookup"><span data-stu-id="19d49-103">Returns the disk.</span></span>

## <span data-ttu-id="19d49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19d49-104">SYNTAX</span></span>

### <span data-ttu-id="19d49-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="19d49-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19d49-106">Obter</span><span class="sxs-lookup"><span data-stu-id="19d49-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="19d49-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19d49-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="19d49-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19d49-108">DESCRIPTION</span></span>
<span data-ttu-id="19d49-109">Retorna o disco.</span><span class="sxs-lookup"><span data-stu-id="19d49-109">Returns the disk.</span></span>

## <span data-ttu-id="19d49-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19d49-110">EXAMPLES</span></span>

### <span data-ttu-id="19d49-111">Exemplo 1: obter todos os discos</span><span class="sxs-lookup"><span data-stu-id="19d49-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="19d49-112">Sem parâmetros, a `Get-AzsDisk` lista será listada em todos os discos.</span><span class="sxs-lookup"><span data-stu-id="19d49-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="19d49-113">Exemplo 2: obter um disco por nome</span><span class="sxs-lookup"><span data-stu-id="19d49-113">Example 2: Get a Disk by Name</span></span>
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="19d49-114">Especifique um disco por seu `Name` para recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="19d49-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="19d49-115">Exemplo 3: obter um número especificado de discos</span><span class="sxs-lookup"><span data-stu-id="19d49-115">Example 3: Get a Specified number of Disks</span></span>
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="19d49-116">Use o `Count` parâmetro para recuperar um número específico de discos.</span><span class="sxs-lookup"><span data-stu-id="19d49-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="19d49-117">Exemplo 4: obter todos os discos em um local específico</span><span class="sxs-lookup"><span data-stu-id="19d49-117">Example 4: Get all disks in specific location</span></span>
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

<span data-ttu-id="19d49-118">Usar o `ScaleUnit` `VolumeLabel` parâmetro ou para listar todos os discos em um local específico</span><span class="sxs-lookup"><span data-stu-id="19d49-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="19d49-119">OS</span><span class="sxs-lookup"><span data-stu-id="19d49-119">PARAMETERS</span></span>

### <span data-ttu-id="19d49-120">-Contagem</span><span class="sxs-lookup"><span data-stu-id="19d49-120">-Count</span></span>
<span data-ttu-id="19d49-121">O número máximo de discos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="19d49-121">The maximum number of disks to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="19d49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d49-122">-DefaultProfile</span></span>
<span data-ttu-id="19d49-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19d49-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19d49-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19d49-124">-InputObject</span></span>
<span data-ttu-id="19d49-125">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="19d49-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="19d49-126">-Local</span><span class="sxs-lookup"><span data-stu-id="19d49-126">-Location</span></span>
<span data-ttu-id="19d49-127">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="19d49-127">Location of the resource.</span></span>

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

### <span data-ttu-id="19d49-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="19d49-128">-Name</span></span>
<span data-ttu-id="19d49-129">A GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="19d49-129">The disk guid as identity.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="19d49-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="19d49-130">-ScaleUnit</span></span>
<span data-ttu-id="19d49-131">A unidade de escala à qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="19d49-131">The scale unit which the resource belongs to.</span></span>

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

### <span data-ttu-id="19d49-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="19d49-132">-SharePath</span></span>
<span data-ttu-id="19d49-133">O compartilhamento ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="19d49-133">The share which the resource belongs to.</span></span>

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

### <span data-ttu-id="19d49-134">-Início</span><span class="sxs-lookup"><span data-stu-id="19d49-134">-Start</span></span>
<span data-ttu-id="19d49-135">O índice inicial de discos na consulta.</span><span class="sxs-lookup"><span data-stu-id="19d49-135">The start index of disks in query.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="19d49-136">-Status</span><span class="sxs-lookup"><span data-stu-id="19d49-136">-Status</span></span>
<span data-ttu-id="19d49-137">Os parâmetros do estado do disco.</span><span class="sxs-lookup"><span data-stu-id="19d49-137">The parameters of disk state.</span></span>

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

### <span data-ttu-id="19d49-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19d49-138">-SubscriptionId</span></span>
<span data-ttu-id="19d49-139">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="19d49-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="19d49-140">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="19d49-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="19d49-141">-Usersubscriptionid</span><span class="sxs-lookup"><span data-stu-id="19d49-141">-UserSubscriptionId</span></span>
<span data-ttu-id="19d49-142">ID de assinatura de usuário à qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="19d49-142">User Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="19d49-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="19d49-143">-VolumeLabel</span></span>
<span data-ttu-id="19d49-144">O rótulo de volume do volume ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="19d49-144">The volume label of the volume which the resource belongs to.</span></span>

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

### <span data-ttu-id="19d49-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d49-145">CommonParameters</span></span>
<span data-ttu-id="19d49-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19d49-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d49-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19d49-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d49-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19d49-148">INPUTS</span></span>

### <span data-ttu-id="19d49-149">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="19d49-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="19d49-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19d49-150">OUTPUTS</span></span>

### <span data-ttu-id="19d49-151">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20180730Preview. IDisk</span><span class="sxs-lookup"><span data-stu-id="19d49-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="19d49-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19d49-152">NOTES</span></span>

<span data-ttu-id="19d49-153">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="19d49-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19d49-154">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19d49-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="19d49-155">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="19d49-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19d49-156">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="19d49-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="19d49-157">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="19d49-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19d49-158">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="19d49-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="19d49-159">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="19d49-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="19d49-160">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="19d49-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="19d49-161">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="19d49-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="19d49-162">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="19d49-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="19d49-163">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="19d49-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="19d49-164">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="19d49-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="19d49-165">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="19d49-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="19d49-166">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="19d49-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="19d49-167">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="19d49-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="19d49-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19d49-168">RELATED LINKS</span></span>

