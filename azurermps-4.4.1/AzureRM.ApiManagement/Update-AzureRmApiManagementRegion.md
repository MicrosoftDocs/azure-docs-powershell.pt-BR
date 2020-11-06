---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427009"
---
# <span data-ttu-id="a20a6-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a20a6-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="a20a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a20a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a20a6-103">Atualiza a região de implantação existente na instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a20a6-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a20a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a20a6-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a20a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a20a6-105">DESCRIPTION</span></span>
<span data-ttu-id="a20a6-106">O cmdlet **Update-AzureRmApiManagementRegion** atualiza uma instância existente do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** em uma coleção de objetos **AdditionalRegions** de uma instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="a20a6-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="a20a6-107">Esse cmdlet não implanta nada, mas atualiza uma instância de **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="a20a6-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="a20a6-108">Para atualizar uma implantação de um gerenciamento de API, use o **PsApiManagementInstance** modificado para o cmdlet Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="a20a6-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="a20a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a20a6-109">EXAMPLES</span></span>

## <span data-ttu-id="a20a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="a20a6-110">PARAMETERS</span></span>

### <span data-ttu-id="a20a6-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a20a6-111">-ApiManagement</span></span>
<span data-ttu-id="a20a6-112">Especifica a instância **PsApiManagement** para atualizar uma região de implantação existente no.</span><span class="sxs-lookup"><span data-stu-id="a20a6-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="a20a6-113">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="a20a6-113">-Capacity</span></span>
<span data-ttu-id="a20a6-114">Especifica o novo valor de capacidade de SKU para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="a20a6-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="a20a6-115">-Local</span><span class="sxs-lookup"><span data-stu-id="a20a6-115">-Location</span></span>
<span data-ttu-id="a20a6-116">Especifica o local da região de implantação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="a20a6-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="a20a6-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a20a6-117">Valid values are:</span></span>

- <span data-ttu-id="a20a6-118">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="a20a6-118">North Central US</span></span>
- <span data-ttu-id="a20a6-119">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="a20a6-119">South Central US</span></span>
- <span data-ttu-id="a20a6-120">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="a20a6-120">Central US</span></span>
- <span data-ttu-id="a20a6-121">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="a20a6-121">West Europe</span></span>
- <span data-ttu-id="a20a6-122">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="a20a6-122">North Europe</span></span>
- <span data-ttu-id="a20a6-123">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="a20a6-123">West US</span></span>
- <span data-ttu-id="a20a6-124">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="a20a6-124">East US</span></span>
- <span data-ttu-id="a20a6-125">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="a20a6-125">East US 2</span></span>
- <span data-ttu-id="a20a6-126">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="a20a6-126">Japan East</span></span>
- <span data-ttu-id="a20a6-127">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="a20a6-127">Japan West</span></span>
- <span data-ttu-id="a20a6-128">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="a20a6-128">Brazil South</span></span>
- <span data-ttu-id="a20a6-129">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="a20a6-129">Southeast Asia</span></span>
- <span data-ttu-id="a20a6-130">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="a20a6-130">East Asia</span></span>
- <span data-ttu-id="a20a6-131">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="a20a6-131">Australia East</span></span>
- <span data-ttu-id="a20a6-132">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="a20a6-132">Australia Southeast</span></span>

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

### <span data-ttu-id="a20a6-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="a20a6-133">-Sku</span></span>
<span data-ttu-id="a20a6-134">Especifica o novo valor de camada para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="a20a6-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="a20a6-135">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a20a6-135">Valid values are:</span></span>

- <span data-ttu-id="a20a6-136">Event</span><span class="sxs-lookup"><span data-stu-id="a20a6-136">Developer</span></span>
- <span data-ttu-id="a20a6-137">Oficial</span><span class="sxs-lookup"><span data-stu-id="a20a6-137">Standard</span></span>
- <span data-ttu-id="a20a6-138">Gratifica</span><span class="sxs-lookup"><span data-stu-id="a20a6-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a20a6-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a20a6-139">-VirtualNetwork</span></span>
<span data-ttu-id="a20a6-140">Especifica uma configuração de rede virtual para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="a20a6-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="a20a6-141">Passar $null removerá a configuração de rede virtual para a região.</span><span class="sxs-lookup"><span data-stu-id="a20a6-141">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="a20a6-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20a6-142">-DefaultProfile</span></span>
<span data-ttu-id="a20a6-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a20a6-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a20a6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20a6-144">CommonParameters</span></span>
<span data-ttu-id="a20a6-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20a6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20a6-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a20a6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20a6-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a20a6-147">INPUTS</span></span>

### <span data-ttu-id="a20a6-148">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a20a6-148">PsApiManagement</span></span>
<span data-ttu-id="a20a6-149">O parâmetro ' ApiManagement ' aceita o valor do tipo ' PsApiManagement ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a20a6-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="a20a6-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a20a6-150">OUTPUTS</span></span>

### <span data-ttu-id="a20a6-151">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a20a6-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a20a6-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a20a6-152">NOTES</span></span>

## <span data-ttu-id="a20a6-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a20a6-153">RELATED LINKS</span></span>

[<span data-ttu-id="a20a6-154">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a20a6-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="a20a6-155">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a20a6-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="a20a6-156">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a20a6-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
