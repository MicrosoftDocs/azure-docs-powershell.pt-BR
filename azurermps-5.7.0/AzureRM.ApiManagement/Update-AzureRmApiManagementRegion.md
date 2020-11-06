---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: d6c97ac0fc948ba3ee4f86a2e657a1386c693f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609983"
---
# <span data-ttu-id="7b7e8-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="7b7e8-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="7b7e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7e8-103">Atualiza a região de implantação existente na instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b7e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b7e8-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b7e8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b7e8-105">DESCRIPTION</span></span>
<span data-ttu-id="7b7e8-106">O cmdlet **Update-AzureRmApiManagementRegion** atualiza uma instância existente do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** em uma coleção de objetos **AdditionalRegions** de uma instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="7b7e8-107">Esse cmdlet não implanta nada, mas atualiza uma instância de **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="7b7e8-108">Para atualizar uma implantação de um gerenciamento de API, use o **PsApiManagementInstance** modificado para o cmdlet Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="7b7e8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b7e8-109">EXAMPLES</span></span>

## <span data-ttu-id="7b7e8-110">OS</span><span class="sxs-lookup"><span data-stu-id="7b7e8-110">PARAMETERS</span></span>

### <span data-ttu-id="7b7e8-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7b7e8-111">-ApiManagement</span></span>
<span data-ttu-id="7b7e8-112">Especifica a instância **PsApiManagement** para atualizar uma região de implantação existente no.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="7b7e8-113">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="7b7e8-113">-Capacity</span></span>
<span data-ttu-id="7b7e8-114">Especifica o novo valor de capacidade de SKU para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b7e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b7e8-115">-DefaultProfile</span></span>
<span data-ttu-id="7b7e8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="7b7e8-117">-Local</span><span class="sxs-lookup"><span data-stu-id="7b7e8-117">-Location</span></span>
<span data-ttu-id="7b7e8-118">Especifica o local da região de implantação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-118">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="7b7e8-119">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="7b7e8-120">Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="7b7e8-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b7e8-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="7b7e8-121">-Sku</span></span>
<span data-ttu-id="7b7e8-122">Especifica o novo valor de camada para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-122">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="7b7e8-123">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="7b7e8-123">Valid values are:</span></span>

- <span data-ttu-id="7b7e8-124">Event</span><span class="sxs-lookup"><span data-stu-id="7b7e8-124">Developer</span></span>
- <span data-ttu-id="7b7e8-125">Oficial</span><span class="sxs-lookup"><span data-stu-id="7b7e8-125">Standard</span></span>
- <span data-ttu-id="7b7e8-126">Gratifica</span><span class="sxs-lookup"><span data-stu-id="7b7e8-126">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b7e8-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7b7e8-127">-VirtualNetwork</span></span>
<span data-ttu-id="7b7e8-128">Especifica uma configuração de rede virtual para a região de implantação.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="7b7e8-129">Passar $null removerá a configuração de rede virtual para a região.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-129">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b7e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7e8-130">CommonParameters</span></span>
<span data-ttu-id="7b7e8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b7e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7e8-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b7e8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7e8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b7e8-133">INPUTS</span></span>

### <span data-ttu-id="7b7e8-134">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="7b7e8-134">PsApiManagement</span></span>
<span data-ttu-id="7b7e8-135">O parâmetro ' ApiManagement ' aceita o valor do tipo ' PsApiManagement ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7b7e8-135">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="7b7e8-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b7e8-136">OUTPUTS</span></span>

### <span data-ttu-id="7b7e8-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="7b7e8-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="7b7e8-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b7e8-138">NOTES</span></span>

## <span data-ttu-id="7b7e8-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b7e8-139">RELATED LINKS</span></span>

[<span data-ttu-id="7b7e8-140">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="7b7e8-140">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="7b7e8-141">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="7b7e8-141">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="7b7e8-142">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="7b7e8-142">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
