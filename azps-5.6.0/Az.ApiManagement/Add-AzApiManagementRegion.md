---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: ce1183588458dc0213bff77493caf41a9b1d2766
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890899"
---
# <span data-ttu-id="b1494-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b1494-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="b1494-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1494-102">SYNOPSIS</span></span>
<span data-ttu-id="b1494-103">Adiciona novas regiões de implantação a uma instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b1494-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="b1494-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b1494-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1494-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b1494-105">DESCRIPTION</span></span>
<span data-ttu-id="b1494-106">O cmdlet **Add-AzApiManagementRegion** adiciona nova instância do tipo **PsApiManagementRegion** à coleção **de AdditionalRegions** de instância fornecida do tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="b1494-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="b1494-107">Este cmdlet não implanta nada por si só, mas atualiza a instância **de PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="b1494-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="b1494-108">Para atualizar uma implantação de um Gerenciamento de API, passe a Instância **PsApiManagement** modificada para Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b1494-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="b1494-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1494-109">EXAMPLES</span></span>

### <span data-ttu-id="b1494-110">Exemplo 1: Adicionar novas regiões de implantação a uma instância PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1494-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="b1494-111">Este comando adiciona duas unidades SKU premium e a região chamada East US à **instância PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="b1494-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="b1494-112">Exemplo 2: adicionar novas regiões de implantação a uma instância PsApiManagement e atualizar a implantação</span><span class="sxs-lookup"><span data-stu-id="b1494-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="b1494-113">Esse comando obtém um **objeto PsApiManagement,** adiciona duas unidades SKU premium para a região chamada Leste dos EUA e atualiza a implantação.</span><span class="sxs-lookup"><span data-stu-id="b1494-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="b1494-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b1494-114">PARAMETERS</span></span>

### <span data-ttu-id="b1494-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1494-115">-ApiManagement</span></span>
<span data-ttu-id="b1494-116">Especifica a **instância PsApiManagement** à que este cmdlet adiciona regiões de implantação adicionais.</span><span class="sxs-lookup"><span data-stu-id="b1494-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1494-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="b1494-117">-Capacity</span></span>
<span data-ttu-id="b1494-118">Especifica a capacidade SKU da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="b1494-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1494-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1494-119">-DefaultProfile</span></span>
<span data-ttu-id="b1494-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b1494-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1494-121">-Location</span><span class="sxs-lookup"><span data-stu-id="b1494-121">-Location</span></span>
<span data-ttu-id="b1494-122">Especifica o local da nova região de implantação entre a região suportada para o serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="b1494-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="b1494-123">Para obter locais válidos, use o cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | onde {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object locais</span><span class="sxs-lookup"><span data-stu-id="b1494-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1494-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="b1494-124">-Sku</span></span>
<span data-ttu-id="b1494-125">Especifica a camada da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="b1494-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="b1494-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b1494-126">Valid values are:</span></span> 
- <span data-ttu-id="b1494-127">Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="b1494-127">Developer</span></span>
- <span data-ttu-id="b1494-128">Standard</span><span class="sxs-lookup"><span data-stu-id="b1494-128">Standard</span></span>
- <span data-ttu-id="b1494-129">Premium</span><span class="sxs-lookup"><span data-stu-id="b1494-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1494-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b1494-130">-VirtualNetwork</span></span>
<span data-ttu-id="b1494-131">Especifica uma configuração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b1494-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1494-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1494-132">CommonParameters</span></span>
<span data-ttu-id="b1494-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1494-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1494-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1494-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1494-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1494-135">INPUTS</span></span>

### <span data-ttu-id="b1494-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1494-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b1494-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b1494-137">OUTPUTS</span></span>

### <span data-ttu-id="b1494-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1494-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b1494-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="b1494-139">NOTES</span></span>
* <span data-ttu-id="b1494-140">O cmdlet grava a instância **PsApiManagement atualizada** no pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1494-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="b1494-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1494-141">RELATED LINKS</span></span>

[<span data-ttu-id="b1494-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b1494-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="b1494-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b1494-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="b1494-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1494-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


