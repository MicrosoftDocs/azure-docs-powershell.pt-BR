---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945372"
---
# <span data-ttu-id="02548-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="02548-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="02548-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02548-102">SYNOPSIS</span></span>
<span data-ttu-id="02548-103">Retorna a imagem solicitada da extensão da máquina virtual correspondente ao Publisher, ao tipo, a versão.</span><span class="sxs-lookup"><span data-stu-id="02548-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="02548-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02548-104">SYNTAX</span></span>

### <span data-ttu-id="02548-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="02548-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="02548-106">Obter</span><span class="sxs-lookup"><span data-stu-id="02548-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="02548-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="02548-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="02548-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02548-108">DESCRIPTION</span></span>
<span data-ttu-id="02548-109">Retorna a imagem solicitada da extensão da máquina virtual correspondente ao Publisher, ao tipo, a versão.</span><span class="sxs-lookup"><span data-stu-id="02548-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="02548-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02548-110">EXAMPLES</span></span>

### <span data-ttu-id="02548-111">Exemplo 1: obter todas as extensões de VM</span><span class="sxs-lookup"><span data-stu-id="02548-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="02548-112">Obtenha uma lista de todos os VMExtensions deixando todos os parâmetros em branco.</span><span class="sxs-lookup"><span data-stu-id="02548-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="02548-113">OS</span><span class="sxs-lookup"><span data-stu-id="02548-113">PARAMETERS</span></span>

### <span data-ttu-id="02548-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02548-114">-DefaultProfile</span></span>
<span data-ttu-id="02548-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02548-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02548-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02548-116">-InputObject</span></span>
<span data-ttu-id="02548-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="02548-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="02548-118">-Local</span><span class="sxs-lookup"><span data-stu-id="02548-118">-Location</span></span>
<span data-ttu-id="02548-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="02548-119">Location of the resource.</span></span>

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

### <span data-ttu-id="02548-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="02548-120">-Publisher</span></span>
<span data-ttu-id="02548-121">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="02548-121">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="02548-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02548-122">-SubscriptionId</span></span>
<span data-ttu-id="02548-123">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="02548-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="02548-124">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="02548-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="02548-125">-Digite</span><span class="sxs-lookup"><span data-stu-id="02548-125">-Type</span></span>
<span data-ttu-id="02548-126">Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="02548-126">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="02548-127">-Versão</span><span class="sxs-lookup"><span data-stu-id="02548-127">-Version</span></span>
<span data-ttu-id="02548-128">A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="02548-128">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="02548-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02548-129">CommonParameters</span></span>
<span data-ttu-id="02548-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02548-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02548-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02548-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02548-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02548-132">INPUTS</span></span>

### <span data-ttu-id="02548-133">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="02548-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="02548-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02548-134">OUTPUTS</span></span>

### <span data-ttu-id="02548-135">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="02548-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="02548-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02548-136">NOTES</span></span>

<span data-ttu-id="02548-137">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="02548-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02548-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02548-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="02548-139">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="02548-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02548-140">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="02548-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="02548-141">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="02548-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02548-142">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="02548-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="02548-143">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="02548-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="02548-144">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="02548-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="02548-145">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="02548-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="02548-146">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="02548-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="02548-147">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="02548-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="02548-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="02548-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="02548-149">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="02548-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="02548-150">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="02548-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="02548-151">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="02548-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="02548-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02548-152">RELATED LINKS</span></span>

