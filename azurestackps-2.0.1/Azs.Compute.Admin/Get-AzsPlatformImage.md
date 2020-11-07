---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945270"
---
# <span data-ttu-id="96e77-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="96e77-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="96e77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96e77-102">SYNOPSIS</span></span>
<span data-ttu-id="96e77-103">Retorna a imagem específica da plataforma correspondente ao fornecedor, oferta, SKUs e versão.</span><span class="sxs-lookup"><span data-stu-id="96e77-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="96e77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96e77-104">SYNTAX</span></span>

### <span data-ttu-id="96e77-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="96e77-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="96e77-106">Obter</span><span class="sxs-lookup"><span data-stu-id="96e77-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96e77-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96e77-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="96e77-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96e77-108">DESCRIPTION</span></span>
<span data-ttu-id="96e77-109">Retorna a imagem específica da plataforma correspondente ao fornecedor, oferta, SKUs e versão.</span><span class="sxs-lookup"><span data-stu-id="96e77-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="96e77-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96e77-110">EXAMPLES</span></span>

### <span data-ttu-id="96e77-111">Exemplo 1: obter todas as imagens da plataforma</span><span class="sxs-lookup"><span data-stu-id="96e77-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="96e77-112">Obtenha uma lista de todas as imagens da plataforma, deixando todos os parâmetros em branco.</span><span class="sxs-lookup"><span data-stu-id="96e77-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="96e77-113">Exemplo 2: obter uma imagem de plataforma específica</span><span class="sxs-lookup"><span data-stu-id="96e77-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="96e77-114">Especifique a oferta, o fornecedor, a localização, a SKU e a versão para recuperar uma imagem de plataforma.</span><span class="sxs-lookup"><span data-stu-id="96e77-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="96e77-115">OS</span><span class="sxs-lookup"><span data-stu-id="96e77-115">PARAMETERS</span></span>

### <span data-ttu-id="96e77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e77-116">-DefaultProfile</span></span>
<span data-ttu-id="96e77-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96e77-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96e77-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96e77-118">-InputObject</span></span>
<span data-ttu-id="96e77-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="96e77-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96e77-120">-Local</span><span class="sxs-lookup"><span data-stu-id="96e77-120">-Location</span></span>
<span data-ttu-id="96e77-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="96e77-121">Location of the resource.</span></span>

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

### <span data-ttu-id="96e77-122">-Oferta</span><span class="sxs-lookup"><span data-stu-id="96e77-122">-Offer</span></span>
<span data-ttu-id="96e77-123">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="96e77-123">Name of the offer.</span></span>

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

### <span data-ttu-id="96e77-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="96e77-124">-Publisher</span></span>
<span data-ttu-id="96e77-125">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="96e77-125">Name of the publisher.</span></span>

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

### <span data-ttu-id="96e77-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="96e77-126">-Sku</span></span>
<span data-ttu-id="96e77-127">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="96e77-127">Name of the SKU.</span></span>

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

### <span data-ttu-id="96e77-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96e77-128">-SubscriptionId</span></span>
<span data-ttu-id="96e77-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="96e77-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="96e77-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="96e77-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96e77-131">-Versão</span><span class="sxs-lookup"><span data-stu-id="96e77-131">-Version</span></span>
<span data-ttu-id="96e77-132">A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="96e77-132">The version of the resource.</span></span>

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

### <span data-ttu-id="96e77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e77-133">CommonParameters</span></span>
<span data-ttu-id="96e77-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e77-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96e77-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e77-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96e77-136">INPUTS</span></span>

### <span data-ttu-id="96e77-137">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="96e77-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="96e77-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96e77-138">OUTPUTS</span></span>

### <span data-ttu-id="96e77-139">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="96e77-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="96e77-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96e77-140">NOTES</span></span>

<span data-ttu-id="96e77-141">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="96e77-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96e77-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96e77-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="96e77-143">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="96e77-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96e77-144">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="96e77-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="96e77-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="96e77-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96e77-146">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="96e77-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="96e77-147">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="96e77-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="96e77-148">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="96e77-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="96e77-149">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="96e77-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="96e77-150">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="96e77-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="96e77-151">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="96e77-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="96e77-152">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="96e77-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="96e77-153">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="96e77-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="96e77-154">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="96e77-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="96e77-155">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="96e77-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="96e77-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96e77-156">RELATED LINKS</span></span>

