---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: ed26538e54cef189837bd36bf9e6f561df3541f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427320"
---
# <span data-ttu-id="43786-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="43786-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="43786-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43786-102">SYNOPSIS</span></span>
<span data-ttu-id="43786-103">Atualiza a região de implantação existente na instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="43786-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43786-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43786-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43786-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43786-105">DESCRIPTION</span></span>
<span data-ttu-id="43786-106">O cmdlet **Update-AzureRmApiManagementRegion** atualiza uma instância existente do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** em uma coleção de objetos **AdditionalRegions** de uma instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="43786-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="43786-107">Esse cmdlet não implanta nada, mas atualiza uma instância de **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="43786-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="43786-108">Para atualizar uma implantação de um gerenciamento de API, use o **PsApiManagementInstance** modificado para o cmdlet Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="43786-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="43786-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43786-109">EXAMPLES</span></span>

## <span data-ttu-id="43786-110">OS</span><span class="sxs-lookup"><span data-stu-id="43786-110">PARAMETERS</span></span>

### <span data-ttu-id="43786-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="43786-111">-ApiManagement</span></span>
<span data-ttu-id="43786-112">Especifica a instância **PsApiManagement** para atualizar uma região de implantação existente no.</span><span class="sxs-lookup"><span data-stu-id="43786-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="43786-113">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="43786-113">-Capacity</span></span>
<span data-ttu-id="43786-114">Especifica o novo valor de capacidade de SKU para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="43786-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="43786-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43786-115">-DefaultProfile</span></span>
<span data-ttu-id="43786-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43786-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43786-117">-Local</span><span class="sxs-lookup"><span data-stu-id="43786-117">-Location</span></span>
<span data-ttu-id="43786-118">Especifica o local da região de implantação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="43786-118">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="43786-119">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="43786-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="43786-120">Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="43786-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="43786-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="43786-121">-Sku</span></span>
<span data-ttu-id="43786-122">Especifica o novo valor de camada para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="43786-122">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="43786-123">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="43786-123">Valid values are:</span></span>
- <span data-ttu-id="43786-124">Event</span><span class="sxs-lookup"><span data-stu-id="43786-124">Developer</span></span>
- <span data-ttu-id="43786-125">Oficial</span><span class="sxs-lookup"><span data-stu-id="43786-125">Standard</span></span>
- <span data-ttu-id="43786-126">Gratifica</span><span class="sxs-lookup"><span data-stu-id="43786-126">Premium</span></span>

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

### <span data-ttu-id="43786-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="43786-127">-VirtualNetwork</span></span>
<span data-ttu-id="43786-128">Especifica uma configuração de rede virtual para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="43786-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="43786-129">Passar $null removerá a configuração de rede virtual para a região.</span><span class="sxs-lookup"><span data-stu-id="43786-129">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="43786-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43786-130">CommonParameters</span></span>
<span data-ttu-id="43786-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43786-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43786-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43786-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43786-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43786-133">INPUTS</span></span>

### <span data-ttu-id="43786-134">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="43786-134">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="43786-135">Parâmetros: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43786-135">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="43786-136">System. String</span><span class="sxs-lookup"><span data-stu-id="43786-136">System.String</span></span>

### <span data-ttu-id="43786-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="43786-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="43786-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="43786-138">System.Int32</span></span>

### <span data-ttu-id="43786-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="43786-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="43786-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43786-140">OUTPUTS</span></span>

### <span data-ttu-id="43786-141">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="43786-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="43786-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43786-142">NOTES</span></span>

## <span data-ttu-id="43786-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43786-143">RELATED LINKS</span></span>

[<span data-ttu-id="43786-144">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="43786-144">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="43786-145">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="43786-145">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="43786-146">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="43786-146">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
