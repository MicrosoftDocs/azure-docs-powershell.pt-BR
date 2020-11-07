---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945341"
---
# <span data-ttu-id="aef4d-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="aef4d-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="aef4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aef4d-102">SYNOPSIS</span></span>
<span data-ttu-id="aef4d-103">Crie uma imagem de extensão da máquina virtual com o Publisher, versão.</span><span class="sxs-lookup"><span data-stu-id="aef4d-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="aef4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aef4d-104">SYNTAX</span></span>

### <span data-ttu-id="aef4d-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="aef4d-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="aef4d-106">Criados</span><span class="sxs-lookup"><span data-stu-id="aef4d-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="aef4d-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aef4d-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aef4d-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aef4d-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aef4d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aef4d-109">DESCRIPTION</span></span>
<span data-ttu-id="aef4d-110">Crie uma imagem de extensão da máquina virtual com o Publisher, versão.</span><span class="sxs-lookup"><span data-stu-id="aef4d-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="aef4d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aef4d-111">EXAMPLES</span></span>

### <span data-ttu-id="aef4d-112">Exemplo 1: Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="aef4d-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="aef4d-113">Use um link acessível publicamente para fornecer o local da extensão ou o URI para um blob do Azure usando o SasUri.</span><span class="sxs-lookup"><span data-stu-id="aef4d-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="aef4d-114">OS</span><span class="sxs-lookup"><span data-stu-id="aef4d-114">PARAMETERS</span></span>

### <span data-ttu-id="aef4d-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="aef4d-115">-ComputeRole</span></span>
<span data-ttu-id="aef4d-116">Função de computação</span><span class="sxs-lookup"><span data-stu-id="aef4d-116">Compute role</span></span>

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

### <span data-ttu-id="aef4d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef4d-117">-DefaultProfile</span></span>
<span data-ttu-id="aef4d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aef4d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aef4d-119">-Extensão</span><span class="sxs-lookup"><span data-stu-id="aef4d-119">-Extension</span></span>
<span data-ttu-id="aef4d-120">Parâmetros usados para criar uma nova imagem de extensão de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aef4d-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="aef4d-121">Para construir, consulte a seção observações para propriedades de extensão e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="aef4d-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="aef4d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aef4d-122">-InputObject</span></span>
<span data-ttu-id="aef4d-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="aef4d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aef4d-124">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="aef4d-124">-IsSystemExtension</span></span>
<span data-ttu-id="aef4d-125">Indica se a extensão é para o sistema.</span><span class="sxs-lookup"><span data-stu-id="aef4d-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef4d-126">-Local</span><span class="sxs-lookup"><span data-stu-id="aef4d-126">-Location</span></span>
<span data-ttu-id="aef4d-127">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="aef4d-127">Location of the resource.</span></span>

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

### <span data-ttu-id="aef4d-128">-PropertiesPublisher</span><span class="sxs-lookup"><span data-stu-id="aef4d-128">-PropertiesPublisher</span></span>
<span data-ttu-id="aef4d-129">O fornecedor da extensão da VM</span><span class="sxs-lookup"><span data-stu-id="aef4d-129">The publisher of the VM Extension</span></span>

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

### <span data-ttu-id="aef4d-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="aef4d-130">-ProvisioningState</span></span>
<span data-ttu-id="aef4d-131">Configuração do estado de extensão.</span><span class="sxs-lookup"><span data-stu-id="aef4d-131">Provisioning state of extension.</span></span>

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

### <span data-ttu-id="aef4d-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="aef4d-132">-Publisher</span></span>
<span data-ttu-id="aef4d-133">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="aef4d-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef4d-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="aef4d-134">-SourceBlob</span></span>
<span data-ttu-id="aef4d-135">URL para blob do Azure ou do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="aef4d-135">URI to Azure or AzureStack blob.</span></span>

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

### <span data-ttu-id="aef4d-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aef4d-136">-SubscriptionId</span></span>
<span data-ttu-id="aef4d-137">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aef4d-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aef4d-138">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aef4d-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aef4d-139">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="aef4d-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="aef4d-140">Verdadeiro se der suporte a várias extensões.</span><span class="sxs-lookup"><span data-stu-id="aef4d-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef4d-141">-Digite</span><span class="sxs-lookup"><span data-stu-id="aef4d-141">-Type</span></span>
<span data-ttu-id="aef4d-142">Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="aef4d-142">Type of extension.</span></span>

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

### <span data-ttu-id="aef4d-143">-Versão</span><span class="sxs-lookup"><span data-stu-id="aef4d-143">-Version</span></span>
<span data-ttu-id="aef4d-144">A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="aef4d-144">The version of the resource.</span></span>

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

### <span data-ttu-id="aef4d-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="aef4d-145">-VmOsType</span></span>
<span data-ttu-id="aef4d-146">Destino do tipo de sistema operacional da máquina virtual necessária para implantar o manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="aef4d-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="aef4d-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="aef4d-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="aef4d-148">Valor que indica se a extensão está habilitada para suporte ao conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aef4d-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef4d-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aef4d-149">-Confirm</span></span>
<span data-ttu-id="aef4d-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef4d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aef4d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aef4d-151">-WhatIf</span></span>
<span data-ttu-id="aef4d-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aef4d-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef4d-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aef4d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aef4d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef4d-154">CommonParameters</span></span>
<span data-ttu-id="aef4d-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef4d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef4d-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aef4d-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef4d-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aef4d-157">INPUTS</span></span>

### <span data-ttu-id="aef4d-158">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="aef4d-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="aef4d-159">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="aef4d-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="aef4d-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aef4d-160">OUTPUTS</span></span>

### <span data-ttu-id="aef4d-161">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="aef4d-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="aef4d-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aef4d-162">NOTES</span></span>

<span data-ttu-id="aef4d-163">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="aef4d-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aef4d-164">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aef4d-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="aef4d-165">EXTENSÃO <IVMExtensionParameters> : parâmetros usados para criar uma nova imagem de extensão de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aef4d-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="aef4d-166">`[ComputeRole <String>]`: Calcular função</span><span class="sxs-lookup"><span data-stu-id="aef4d-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="aef4d-167">`[IsSystemExtension <Boolean?>]`: Indica se a extensão é para o sistema.</span><span class="sxs-lookup"><span data-stu-id="aef4d-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="aef4d-168">`[ProvisioningState <ProvisioningState?>]`: Configurando o estado da extensão.</span><span class="sxs-lookup"><span data-stu-id="aef4d-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="aef4d-169">`[Publisher <String>]`: O fornecedor da extensão da VM</span><span class="sxs-lookup"><span data-stu-id="aef4d-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="aef4d-170">`[SourceBlobUri <String>]`: URI para blob do Azure ou AzureStack.</span><span class="sxs-lookup"><span data-stu-id="aef4d-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="aef4d-171">`[SupportMultipleExtension <Boolean?>]`: Verdadeiro se der suporte a várias extensões.</span><span class="sxs-lookup"><span data-stu-id="aef4d-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="aef4d-172">`[VMScaleSetEnabled <Boolean?>]`: Valor que indica se a extensão está habilitada para suporte ao conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aef4d-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="aef4d-173">`[VmosType <OSType?>]`: Destino do tipo de sistema operacional da máquina virtual necessária para implantar o manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="aef4d-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="aef4d-174">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="aef4d-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aef4d-175">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="aef4d-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="aef4d-176">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="aef4d-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aef4d-177">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="aef4d-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="aef4d-178">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="aef4d-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="aef4d-179">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="aef4d-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="aef4d-180">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="aef4d-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="aef4d-181">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="aef4d-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="aef4d-182">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="aef4d-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="aef4d-183">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aef4d-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aef4d-184">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aef4d-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="aef4d-185">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="aef4d-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="aef4d-186">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="aef4d-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="aef4d-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aef4d-187">RELATED LINKS</span></span>

