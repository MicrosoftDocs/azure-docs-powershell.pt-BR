---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 8552592acb45702c866c8d918121b8dd61d126a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284338"
---
# <span data-ttu-id="00d21-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="00d21-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="00d21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00d21-102">SYNOPSIS</span></span>
<span data-ttu-id="00d21-103">Atualiza a região de implantação existente na instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="00d21-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="00d21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00d21-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00d21-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00d21-105">DESCRIPTION</span></span>
<span data-ttu-id="00d21-106">O cmdlet **Update-AzApiManagementRegion** atualiza uma instância existente do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** em uma coleção de objetos **AdditionalRegions** de uma instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="00d21-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="00d21-107">Esse cmdlet não implanta nada, mas atualiza uma instância de **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="00d21-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="00d21-108">Para atualizar uma implantação de um gerenciamento de API, use o **PsApiManagementInstance** modificado para o cmdlet Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="00d21-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="00d21-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00d21-109">EXAMPLES</span></span>

### <span data-ttu-id="00d21-110">Exemplo 1: aumenta a capacidade de região adicional em uma instância de PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="00d21-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="00d21-111">Esse comando obtém o serviço de gerenciamento de API Premium SKU, com regiões no centro-oeste dos EUA e centro norte.</span><span class="sxs-lookup"><span data-stu-id="00d21-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="00d21-112">Em seguida, ele aumenta a capacidade da região central norte dos EUA para 2 usando o **set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="00d21-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="00d21-113">O próximo cmdlet **set-AzApiManagement** aplica a alteração de configuração ao serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="00d21-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

### <span data-ttu-id="00d21-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="00d21-114">Example 2</span></span>

<span data-ttu-id="00d21-115">Atualiza a região de implantação existente na instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="00d21-115">Updates existing deployment region in PsApiManagement instance.</span></span> <span data-ttu-id="00d21-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="00d21-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## <span data-ttu-id="00d21-117">OS</span><span class="sxs-lookup"><span data-stu-id="00d21-117">PARAMETERS</span></span>

### <span data-ttu-id="00d21-118">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00d21-118">-ApiManagement</span></span>
<span data-ttu-id="00d21-119">Especifica a instância **PsApiManagement** para atualizar uma região de implantação existente no.</span><span class="sxs-lookup"><span data-stu-id="00d21-119">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="00d21-120">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="00d21-120">-Capacity</span></span>
<span data-ttu-id="00d21-121">Especifica o novo valor de capacidade de SKU para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="00d21-121">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="00d21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d21-122">-DefaultProfile</span></span>
<span data-ttu-id="00d21-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00d21-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00d21-124">-Local</span><span class="sxs-lookup"><span data-stu-id="00d21-124">-Location</span></span>
<span data-ttu-id="00d21-125">Especifica o local da região de implantação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="00d21-125">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="00d21-126">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="00d21-126">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="00d21-127">Para obter locais válidos, use o cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="00d21-127">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="00d21-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="00d21-128">-Sku</span></span>
<span data-ttu-id="00d21-129">Especifica o novo valor de camada para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="00d21-129">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="00d21-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="00d21-130">Valid values are:</span></span>
- <span data-ttu-id="00d21-131">Event</span><span class="sxs-lookup"><span data-stu-id="00d21-131">Developer</span></span>
- <span data-ttu-id="00d21-132">Oficial</span><span class="sxs-lookup"><span data-stu-id="00d21-132">Standard</span></span>
- <span data-ttu-id="00d21-133">Gratifica</span><span class="sxs-lookup"><span data-stu-id="00d21-133">Premium</span></span>

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

### <span data-ttu-id="00d21-134">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00d21-134">-VirtualNetwork</span></span>
<span data-ttu-id="00d21-135">Especifica uma configuração de rede virtual para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="00d21-135">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="00d21-136">Passar $null removerá a configuração de rede virtual para a região.</span><span class="sxs-lookup"><span data-stu-id="00d21-136">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="00d21-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d21-137">CommonParameters</span></span>
<span data-ttu-id="00d21-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d21-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d21-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00d21-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d21-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00d21-140">INPUTS</span></span>

### <span data-ttu-id="00d21-141">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="00d21-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="00d21-142">System. String</span><span class="sxs-lookup"><span data-stu-id="00d21-142">System.String</span></span>

### <span data-ttu-id="00d21-143">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="00d21-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="00d21-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="00d21-144">System.Int32</span></span>

### <span data-ttu-id="00d21-145">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00d21-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="00d21-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00d21-146">OUTPUTS</span></span>

### <span data-ttu-id="00d21-147">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="00d21-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="00d21-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00d21-148">NOTES</span></span>

## <span data-ttu-id="00d21-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00d21-149">RELATED LINKS</span></span>

[<span data-ttu-id="00d21-150">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="00d21-150">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="00d21-151">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="00d21-151">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="00d21-152">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="00d21-152">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
