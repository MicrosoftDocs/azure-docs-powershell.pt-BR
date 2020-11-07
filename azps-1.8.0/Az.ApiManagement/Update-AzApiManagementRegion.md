---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: fce2d356b7da56d2b93fa8634e737f96f54da178
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771316"
---
# <span data-ttu-id="4838f-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4838f-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="4838f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4838f-102">SYNOPSIS</span></span>
<span data-ttu-id="4838f-103">Atualiza a região de implantação existente na instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4838f-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="4838f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4838f-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4838f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4838f-105">DESCRIPTION</span></span>
<span data-ttu-id="4838f-106">O cmdlet **Update-AzApiManagementRegion** atualiza uma instância existente do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** em uma coleção de objetos **AdditionalRegions** de uma instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="4838f-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="4838f-107">Esse cmdlet não implanta nada, mas atualiza uma instância de **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="4838f-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="4838f-108">Para atualizar uma implantação de um gerenciamento de API, use o **PsApiManagementInstance** modificado para o cmdlet Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="4838f-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="4838f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4838f-109">EXAMPLES</span></span>

### <span data-ttu-id="4838f-110">Exemplo 1: aumenta a capacidade de região adicional em uma instância de PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4838f-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="4838f-111">Esse comando obtém o serviço de gerenciamento de API Premium SKU, com regiões no centro-oeste dos EUA e centro norte.</span><span class="sxs-lookup"><span data-stu-id="4838f-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="4838f-112">Em seguida, ele aumenta a capacidade da região central norte dos EUA para 2 usando a **atualização-AzApiManagementRegion**.</span><span class="sxs-lookup"><span data-stu-id="4838f-112">It then increases the Capacity of the North Central US region to 2 using the **Update-AzApiManagementRegion**.</span></span> <span data-ttu-id="4838f-113">O próximo cmdlet Set-AzApiManagement aplica a alteração de configuração ao serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4838f-113">The next cmdlet Set-AzApiManagement applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="4838f-114">OS</span><span class="sxs-lookup"><span data-stu-id="4838f-114">PARAMETERS</span></span>

### <span data-ttu-id="4838f-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4838f-115">-ApiManagement</span></span>
<span data-ttu-id="4838f-116">Especifica a instância **PsApiManagement** para atualizar uma região de implantação existente no.</span><span class="sxs-lookup"><span data-stu-id="4838f-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="4838f-117">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="4838f-117">-Capacity</span></span>
<span data-ttu-id="4838f-118">Especifica o novo valor de capacidade de SKU para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="4838f-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="4838f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4838f-119">-DefaultProfile</span></span>
<span data-ttu-id="4838f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4838f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4838f-121">-Local</span><span class="sxs-lookup"><span data-stu-id="4838f-121">-Location</span></span>
<span data-ttu-id="4838f-122">Especifica o local da região de implantação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="4838f-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="4838f-123">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4838f-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="4838f-124">Para obter locais válidos, use o cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="4838f-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="4838f-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="4838f-125">-Sku</span></span>
<span data-ttu-id="4838f-126">Especifica o novo valor de camada para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="4838f-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="4838f-127">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="4838f-127">Valid values are:</span></span>
- <span data-ttu-id="4838f-128">Event</span><span class="sxs-lookup"><span data-stu-id="4838f-128">Developer</span></span>
- <span data-ttu-id="4838f-129">Oficial</span><span class="sxs-lookup"><span data-stu-id="4838f-129">Standard</span></span>
- <span data-ttu-id="4838f-130">Gratifica</span><span class="sxs-lookup"><span data-stu-id="4838f-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4838f-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4838f-131">-VirtualNetwork</span></span>
<span data-ttu-id="4838f-132">Especifica uma configuração de rede virtual para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="4838f-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="4838f-133">Passar $null removerá a configuração de rede virtual para a região.</span><span class="sxs-lookup"><span data-stu-id="4838f-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="4838f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4838f-134">CommonParameters</span></span>
<span data-ttu-id="4838f-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4838f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4838f-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4838f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4838f-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4838f-137">INPUTS</span></span>

### <span data-ttu-id="4838f-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4838f-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="4838f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4838f-139">System.String</span></span>

### <span data-ttu-id="4838f-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="4838f-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="4838f-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4838f-141">System.Int32</span></span>

### <span data-ttu-id="4838f-142">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4838f-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="4838f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4838f-143">OUTPUTS</span></span>

### <span data-ttu-id="4838f-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4838f-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="4838f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4838f-145">NOTES</span></span>

## <span data-ttu-id="4838f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4838f-146">RELATED LINKS</span></span>

[<span data-ttu-id="4838f-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4838f-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="4838f-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4838f-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="4838f-149">Update-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="4838f-149">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)
