---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: f7a2952bf466a0d964a8b9075832635d2560b6fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441360"
---
# <span data-ttu-id="b4d13-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b4d13-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="b4d13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4d13-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d13-103">Adiciona novas regiões de implantação a uma instância de PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b4d13-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4d13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4d13-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4d13-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4d13-105">DESCRIPTION</span></span>
<span data-ttu-id="b4d13-106">O cmdlet **Add-AzureRmApiManagementRegion** adiciona uma nova instância do tipo **PsApiManagementRegion** à coleção de **AdditionalRegions** da instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="b4d13-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="b4d13-107">Esse cmdlet não implanta algo sozinha, mas atualiza a instância do **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="b4d13-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="b4d13-108">Para atualizar uma implantação de um gerenciamento de API, passe a instância **PsApiManagement** modificada para Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="b4d13-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="b4d13-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4d13-109">EXAMPLES</span></span>

### <span data-ttu-id="b4d13-110">Exemplo 1: adicionar novas regiões de implantação a uma instância do PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d13-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="b4d13-111">Esse comando adiciona duas unidades de SKU Premium e a região chamada leste EUA à instância **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="b4d13-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="b4d13-112">Exemplo 2: adicionar novas regiões de implantação a uma instância do PsApiManagement e atualizar a implantação</span><span class="sxs-lookup"><span data-stu-id="b4d13-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="b4d13-113">Esse comando obtém um objeto **PsApiManagement** , adiciona duas unidades de SKU Premium para a região chamada leste EUA e atualiza a implantação.</span><span class="sxs-lookup"><span data-stu-id="b4d13-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="b4d13-114">OS</span><span class="sxs-lookup"><span data-stu-id="b4d13-114">PARAMETERS</span></span>

### <span data-ttu-id="b4d13-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d13-115">-ApiManagement</span></span>
<span data-ttu-id="b4d13-116">Especifica a instância **PsApiManagement** para a qual esse cmdlet adiciona mais regiões de implantação.</span><span class="sxs-lookup"><span data-stu-id="b4d13-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d13-117">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="b4d13-117">-Capacity</span></span>
<span data-ttu-id="b4d13-118">Especifica a capacidade de SKU da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="b4d13-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d13-119">-DefaultProfile</span></span>
<span data-ttu-id="b4d13-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d13-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d13-121">-Local</span><span class="sxs-lookup"><span data-stu-id="b4d13-121">-Location</span></span>
<span data-ttu-id="b4d13-122">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="b4d13-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>

<span data-ttu-id="b4d13-123">Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="b4d13-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d13-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="b4d13-124">-Sku</span></span>
<span data-ttu-id="b4d13-125">Especifica a camada da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="b4d13-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="b4d13-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b4d13-126">Valid values are:</span></span> 

- <span data-ttu-id="b4d13-127">Event</span><span class="sxs-lookup"><span data-stu-id="b4d13-127">Developer</span></span>
- <span data-ttu-id="b4d13-128">Oficial</span><span class="sxs-lookup"><span data-stu-id="b4d13-128">Standard</span></span>
- <span data-ttu-id="b4d13-129">Gratifica</span><span class="sxs-lookup"><span data-stu-id="b4d13-129">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d13-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b4d13-130">-VirtualNetwork</span></span>
<span data-ttu-id="b4d13-131">Especifica uma configuração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b4d13-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d13-132">CommonParameters</span></span>
<span data-ttu-id="b4d13-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d13-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d13-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d13-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4d13-135">INPUTS</span></span>

### <span data-ttu-id="b4d13-136">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d13-136">PsApiManagement</span></span>
<span data-ttu-id="b4d13-137">O parâmetro ' ApiManagement ' aceita o valor do tipo ' PsApiManagement ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b4d13-137">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="b4d13-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4d13-138">OUTPUTS</span></span>

### <span data-ttu-id="b4d13-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b4d13-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b4d13-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4d13-140">NOTES</span></span>
* <span data-ttu-id="b4d13-141">O cmdlet grava a instância do **PsApiManagement** atualizado em pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4d13-141">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="b4d13-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4d13-142">RELATED LINKS</span></span>

[<span data-ttu-id="b4d13-143">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b4d13-143">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="b4d13-144">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b4d13-144">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="b4d13-145">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="b4d13-145">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


