---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946910"
---
# <span data-ttu-id="9e32f-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="9e32f-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="9e32f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e32f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e32f-103">Cria uma nova plataforma de plataforma com o Publisher, a oferta, os SKUs e a versão fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9e32f-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="9e32f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e32f-104">SYNTAX</span></span>

### <span data-ttu-id="9e32f-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e32f-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9e32f-106">Criados</span><span class="sxs-lookup"><span data-stu-id="9e32f-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9e32f-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9e32f-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9e32f-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9e32f-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9e32f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e32f-109">DESCRIPTION</span></span>
<span data-ttu-id="9e32f-110">Cria uma nova plataforma de plataforma com o Publisher, a oferta, os SKUs e a versão fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9e32f-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="9e32f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e32f-111">EXAMPLES</span></span>

### <span data-ttu-id="9e32f-112">Exemplo 1: Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="9e32f-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="9e32f-113">Adicionar uma imagem de plataforma do armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="9e32f-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="9e32f-114">Use o SasUri para especificar o local do PlatformImage ou use uma URL acessível publicamente.</span><span class="sxs-lookup"><span data-stu-id="9e32f-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="9e32f-115">OS</span><span class="sxs-lookup"><span data-stu-id="9e32f-115">PARAMETERS</span></span>

### <span data-ttu-id="9e32f-116">Mensagem de exceção</span><span class="sxs-lookup"><span data-stu-id="9e32f-116">Exception.Message</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-117">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="9e32f-117">-BillingPartNumber</span></span>
<span data-ttu-id="9e32f-118">O número da peça é usado para cobrar pelos custos do software.</span><span class="sxs-lookup"><span data-stu-id="9e32f-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-119">-Datadisks</span><span class="sxs-lookup"><span data-stu-id="9e32f-119">-DataDisks</span></span>
<span data-ttu-id="9e32f-120">Discos de dados usados pela imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="9e32f-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="9e32f-121">Para construir, consulte a seção notas para propriedades de datadisks e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9e32f-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e32f-122">-DefaultProfile</span></span>
<span data-ttu-id="9e32f-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e32f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e32f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e32f-124">-InputObject</span></span>
<span data-ttu-id="9e32f-125">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9e32f-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-126">-Local</span><span class="sxs-lookup"><span data-stu-id="9e32f-126">-Location</span></span>
<span data-ttu-id="9e32f-127">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9e32f-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="9e32f-128">-NewImage</span></span>
<span data-ttu-id="9e32f-129">Parâmetros usados para criar uma nova imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="9e32f-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="9e32f-130">Para construir, consulte a seção notas para propriedades NEWIMAGE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9e32f-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9e32f-131">-NoWait</span></span>
<span data-ttu-id="9e32f-132">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="9e32f-132">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-133">-Oferta</span><span class="sxs-lookup"><span data-stu-id="9e32f-133">-Offer</span></span>
<span data-ttu-id="9e32f-134">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="9e32f-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="9e32f-135">-OsType</span></span>
<span data-ttu-id="9e32f-136">Tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9e32f-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="9e32f-137">-OsUri</span></span>
<span data-ttu-id="9e32f-138">Local do disco.</span><span class="sxs-lookup"><span data-stu-id="9e32f-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="9e32f-139">-ProvisioningState</span></span>
<span data-ttu-id="9e32f-140">Status de provisionamento da imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="9e32f-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-141">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9e32f-141">-Publisher</span></span>
<span data-ttu-id="9e32f-142">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9e32f-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="9e32f-143">-Sku</span></span>
<span data-ttu-id="9e32f-144">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="9e32f-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e32f-145">-SubscriptionId</span></span>
<span data-ttu-id="9e32f-146">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e32f-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9e32f-147">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e32f-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-148">-Versão</span><span class="sxs-lookup"><span data-stu-id="9e32f-148">-Version</span></span>
<span data-ttu-id="9e32f-149">A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="9e32f-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e32f-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9e32f-150">-Confirm</span></span>
<span data-ttu-id="9e32f-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e32f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e32f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e32f-152">-WhatIf</span></span>
<span data-ttu-id="9e32f-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e32f-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e32f-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e32f-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="9e32f-155">Mensagem de exceção</span><span class="sxs-lookup"><span data-stu-id="9e32f-155">Exception.Message</span></span>

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

### <span data-ttu-id="9e32f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e32f-156">CommonParameters</span></span>
<span data-ttu-id="9e32f-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e32f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e32f-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e32f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e32f-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e32f-159">INPUTS</span></span>

### <span data-ttu-id="9e32f-160">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20151201Preview. IPlatformImageParameters</span><span class="sxs-lookup"><span data-stu-id="9e32f-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="9e32f-161">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9e32f-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="9e32f-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e32f-162">OUTPUTS</span></span>

### <span data-ttu-id="9e32f-163">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="9e32f-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="9e32f-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e32f-164">NOTES</span></span>

<span data-ttu-id="9e32f-165">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9e32f-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e32f-166">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e32f-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9e32f-167">Datadisks <IDataDisk [] >: discos de dados usados pela imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="9e32f-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="9e32f-168">`[Lun <Int32?>]`: Número de unidade lógica.</span><span class="sxs-lookup"><span data-stu-id="9e32f-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="9e32f-169">`[Uri <String>]`: Local do modelo de disco.</span><span class="sxs-lookup"><span data-stu-id="9e32f-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="9e32f-170">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="9e32f-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e32f-171">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="9e32f-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="9e32f-172">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9e32f-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e32f-173">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9e32f-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9e32f-174">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="9e32f-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="9e32f-175">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="9e32f-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="9e32f-176">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9e32f-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="9e32f-177">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="9e32f-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9e32f-178">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="9e32f-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="9e32f-179">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e32f-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9e32f-180">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e32f-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9e32f-181">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="9e32f-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="9e32f-182">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="9e32f-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="9e32f-183">NEWIMAGE <IPlatformImageParameters> : parâmetros usados para criar uma nova imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="9e32f-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="9e32f-184">`[DataDisk <IDataDisk[]>]`: Discos de dados usados pela imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="9e32f-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="9e32f-185">`[Lun <Int32?>]`: Número de unidade lógica.</span><span class="sxs-lookup"><span data-stu-id="9e32f-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="9e32f-186">`[Uri <String>]`: Local do modelo de disco.</span><span class="sxs-lookup"><span data-stu-id="9e32f-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="9e32f-187">`[DetailBillingPartNumber <String>]`: O número da peça é usado para cobrar pelos custos do software.</span><span class="sxs-lookup"><span data-stu-id="9e32f-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="9e32f-188">`[OSDiskOstype <OSType?>]`: Tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9e32f-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="9e32f-189">`[OSDiskUri <String>]`: Local do disco.</span><span class="sxs-lookup"><span data-stu-id="9e32f-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="9e32f-190">`[ProvisioningState <ProvisioningState?>]`: Status de provisionamento da imagem da plataforma.</span><span class="sxs-lookup"><span data-stu-id="9e32f-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="9e32f-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e32f-191">RELATED LINKS</span></span>

