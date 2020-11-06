---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440242"
---
# <span data-ttu-id="0e91b-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0e91b-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="0e91b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e91b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e91b-103">Adiciona novas regiões de implantação a uma instância de PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0e91b-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e91b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e91b-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e91b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e91b-105">DESCRIPTION</span></span>
<span data-ttu-id="0e91b-106">O cmdlet **Add-AzureRmApiManagementRegion** adiciona uma nova instância do tipo **PsApiManagementRegion** à coleção de **AdditionalRegions** da instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="0e91b-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="0e91b-107">Esse cmdlet não implanta algo sozinha, mas atualiza a instância do **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="0e91b-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="0e91b-108">Para atualizar uma implantação de um gerenciamento de API, passe a instância **PsApiManagement** modificada para Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="0e91b-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="0e91b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e91b-109">EXAMPLES</span></span>

### <span data-ttu-id="0e91b-110">Exemplo 1: adicionar novas regiões de implantação a uma instância do PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e91b-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="0e91b-111">Esse comando adiciona duas unidades de SKU Premium e a região chamada leste EUA à instância **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="0e91b-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="0e91b-112">Exemplo 2: adicionar novas regiões de implantação a uma instância do PsApiManagement e atualizar a implantação</span><span class="sxs-lookup"><span data-stu-id="0e91b-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="0e91b-113">Esse comando obtém um objeto **PsApiManagement** , adiciona duas unidades de SKU Premium para a região chamada leste EUA e atualiza a implantação.</span><span class="sxs-lookup"><span data-stu-id="0e91b-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="0e91b-114">OS</span><span class="sxs-lookup"><span data-stu-id="0e91b-114">PARAMETERS</span></span>

### <span data-ttu-id="0e91b-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e91b-115">-ApiManagement</span></span>
<span data-ttu-id="0e91b-116">Especifica a instância **PsApiManagement** para a qual esse cmdlet adiciona mais regiões de implantação.</span><span class="sxs-lookup"><span data-stu-id="0e91b-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="0e91b-117">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="0e91b-117">-Capacity</span></span>
<span data-ttu-id="0e91b-118">Especifica a capacidade de SKU da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="0e91b-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="0e91b-119">-Local</span><span class="sxs-lookup"><span data-stu-id="0e91b-119">-Location</span></span>
<span data-ttu-id="0e91b-120">Especifica o local da nova região de implantação.</span><span class="sxs-lookup"><span data-stu-id="0e91b-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="0e91b-121">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0e91b-121">Valid values are:</span></span> 

- <span data-ttu-id="0e91b-122">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="0e91b-122">North Central US</span></span>
- <span data-ttu-id="0e91b-123">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="0e91b-123">South Central US</span></span>
- <span data-ttu-id="0e91b-124">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="0e91b-124">Central US</span></span>
- <span data-ttu-id="0e91b-125">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="0e91b-125">West Europe</span></span>
- <span data-ttu-id="0e91b-126">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="0e91b-126">North Europe</span></span>
- <span data-ttu-id="0e91b-127">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="0e91b-127">West US</span></span>
- <span data-ttu-id="0e91b-128">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="0e91b-128">East US</span></span>
- <span data-ttu-id="0e91b-129">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="0e91b-129">East US 2</span></span>
- <span data-ttu-id="0e91b-130">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="0e91b-130">Japan East</span></span>
- <span data-ttu-id="0e91b-131">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="0e91b-131">Japan West</span></span>
- <span data-ttu-id="0e91b-132">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="0e91b-132">Brazil South</span></span>
- <span data-ttu-id="0e91b-133">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="0e91b-133">Southeast Asia</span></span>
- <span data-ttu-id="0e91b-134">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="0e91b-134">East Asia</span></span>
- <span data-ttu-id="0e91b-135">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="0e91b-135">Australia East</span></span>
- <span data-ttu-id="0e91b-136">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="0e91b-136">Australia Southeast</span></span>

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

### <span data-ttu-id="0e91b-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="0e91b-137">-Sku</span></span>
<span data-ttu-id="0e91b-138">Especifica a camada da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="0e91b-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="0e91b-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0e91b-139">Valid values are:</span></span> 

- <span data-ttu-id="0e91b-140">Event</span><span class="sxs-lookup"><span data-stu-id="0e91b-140">Developer</span></span>
- <span data-ttu-id="0e91b-141">Oficial</span><span class="sxs-lookup"><span data-stu-id="0e91b-141">Standard</span></span>
- <span data-ttu-id="0e91b-142">Gratifica</span><span class="sxs-lookup"><span data-stu-id="0e91b-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e91b-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0e91b-143">-VirtualNetwork</span></span>
<span data-ttu-id="0e91b-144">Especifica uma configuração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0e91b-144">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="0e91b-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e91b-145">-DefaultProfile</span></span>
<span data-ttu-id="0e91b-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e91b-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e91b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e91b-147">CommonParameters</span></span>
<span data-ttu-id="0e91b-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e91b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e91b-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e91b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e91b-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e91b-150">INPUTS</span></span>

### <span data-ttu-id="0e91b-151">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e91b-151">PsApiManagement</span></span>
<span data-ttu-id="0e91b-152">O parâmetro ' ApiManagement ' aceita o valor do tipo ' PsApiManagement ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0e91b-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="0e91b-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e91b-153">OUTPUTS</span></span>

### <span data-ttu-id="0e91b-154">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e91b-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0e91b-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e91b-155">NOTES</span></span>
* <span data-ttu-id="0e91b-156">O cmdlet grava a instância do **PsApiManagement** atualizado em pipeline.</span><span class="sxs-lookup"><span data-stu-id="0e91b-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="0e91b-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e91b-157">RELATED LINKS</span></span>

[<span data-ttu-id="0e91b-158">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0e91b-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="0e91b-159">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0e91b-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="0e91b-160">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="0e91b-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


