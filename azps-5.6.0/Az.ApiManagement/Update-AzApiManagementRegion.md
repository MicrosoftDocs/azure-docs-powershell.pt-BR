---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: c2e01d4a3f6ee3466151202a1c1d681c9f4e5486
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891891"
---
# <span data-ttu-id="51022-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="51022-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="51022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51022-102">SYNOPSIS</span></span>
<span data-ttu-id="51022-103">Atualiza a região de implantação existente na instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="51022-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="51022-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51022-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51022-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51022-105">DESCRIPTION</span></span>
<span data-ttu-id="51022-106">O cmdlet **Update-AzApiManagementRegion** atualiza uma instância existente do tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** em uma coleção de objetos **AdditionalRegions** de uma instância fornecida do tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="51022-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="51022-107">Este cmdlet não implanta nada, mas atualiza uma instância **de PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="51022-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="51022-108">Para atualizar uma implantação de um Gerenciamento de API, use o **PsApiManagementInstance** modificado para o cmdlet Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="51022-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="51022-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51022-109">EXAMPLES</span></span>

### <span data-ttu-id="51022-110">Exemplo 1: aumenta a capacidade de região adicional em uma instância PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="51022-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="51022-111">Este comando obtém o serviço SKU Premium de Gerenciamento de API, com regiões no Centro-Sul dos EUA e no Norte Central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="51022-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="51022-112">Em seguida, aumenta a capacidade da região norte-central dos EUA para 2 usando **o Set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="51022-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="51022-113">O próximo cmdlet **Set-AzApiManagement** aplica a alteração de configuração ao serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="51022-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

### <span data-ttu-id="51022-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="51022-114">Example 2</span></span>

<span data-ttu-id="51022-115">Atualiza a região de implantação existente na instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="51022-115">Updates existing deployment region in PsApiManagement instance.</span></span> <span data-ttu-id="51022-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="51022-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## <span data-ttu-id="51022-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51022-117">PARAMETERS</span></span>

### <span data-ttu-id="51022-118">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="51022-118">-ApiManagement</span></span>
<span data-ttu-id="51022-119">Especifica a **instância PsApiManagement** para atualizar uma região de implantação existente em.</span><span class="sxs-lookup"><span data-stu-id="51022-119">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="51022-120">-Capacity</span><span class="sxs-lookup"><span data-stu-id="51022-120">-Capacity</span></span>
<span data-ttu-id="51022-121">Especifica o novo valor de capacidade SKU para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="51022-121">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51022-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51022-122">-DefaultProfile</span></span>
<span data-ttu-id="51022-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="51022-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51022-124">-Location</span><span class="sxs-lookup"><span data-stu-id="51022-124">-Location</span></span>
<span data-ttu-id="51022-125">Especifica o local da região de implantação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="51022-125">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="51022-126">Especifica o local da nova região de implantação entre a região suportada para o serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="51022-126">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="51022-127">Para obter locais válidos, use o cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | onde {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object locais</span><span class="sxs-lookup"><span data-stu-id="51022-127">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51022-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="51022-128">-Sku</span></span>
<span data-ttu-id="51022-129">Especifica o novo valor de camada para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="51022-129">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="51022-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="51022-130">Valid values are:</span></span>
- <span data-ttu-id="51022-131">Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="51022-131">Developer</span></span>
- <span data-ttu-id="51022-132">Standard</span><span class="sxs-lookup"><span data-stu-id="51022-132">Standard</span></span>
- <span data-ttu-id="51022-133">Premium</span><span class="sxs-lookup"><span data-stu-id="51022-133">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51022-134">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51022-134">-VirtualNetwork</span></span>
<span data-ttu-id="51022-135">Especifica uma configuração de rede virtual para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="51022-135">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="51022-136">Passar $null removerá a configuração de rede virtual da região.</span><span class="sxs-lookup"><span data-stu-id="51022-136">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51022-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51022-137">CommonParameters</span></span>
<span data-ttu-id="51022-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51022-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51022-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51022-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51022-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51022-140">INPUTS</span></span>

### <span data-ttu-id="51022-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="51022-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="51022-142">System.String</span><span class="sxs-lookup"><span data-stu-id="51022-142">System.String</span></span>

### <span data-ttu-id="51022-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="51022-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="51022-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="51022-144">System.Int32</span></span>

### <span data-ttu-id="51022-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51022-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="51022-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51022-146">OUTPUTS</span></span>

### <span data-ttu-id="51022-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="51022-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="51022-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="51022-148">NOTES</span></span>

## <span data-ttu-id="51022-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51022-149">RELATED LINKS</span></span>

[<span data-ttu-id="51022-150">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="51022-150">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="51022-151">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="51022-151">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="51022-152">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="51022-152">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
