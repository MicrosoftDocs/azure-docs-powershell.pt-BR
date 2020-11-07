---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955203"
---
# <span data-ttu-id="79a07-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="79a07-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="79a07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79a07-102">SYNOPSIS</span></span>
<span data-ttu-id="79a07-103">Adiciona novas regiões de implantação a uma instância de PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="79a07-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="79a07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79a07-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79a07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79a07-105">DESCRIPTION</span></span>
<span data-ttu-id="79a07-106">O cmdlet **Add-AzApiManagementRegion** adiciona uma nova instância do tipo **PsApiManagementRegion** à coleção de **AdditionalRegions** da instância fornecida do tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="79a07-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="79a07-107">Esse cmdlet não implanta algo sozinha, mas atualiza a instância do **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="79a07-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="79a07-108">Para atualizar uma implantação de um gerenciamento de API, passe a instância **PsApiManagement** modificada para Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="79a07-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="79a07-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79a07-109">EXAMPLES</span></span>

### <span data-ttu-id="79a07-110">Exemplo 1: adicionar novas regiões de implantação a uma instância do PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="79a07-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="79a07-111">Esse comando adiciona duas unidades de SKU Premium e a região chamada leste EUA à instância **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="79a07-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="79a07-112">Exemplo 2: adicionar novas regiões de implantação a uma instância do PsApiManagement e atualizar a implantação</span><span class="sxs-lookup"><span data-stu-id="79a07-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="79a07-113">Esse comando obtém um objeto **PsApiManagement** , adiciona duas unidades de SKU Premium para a região chamada leste EUA e atualiza a implantação.</span><span class="sxs-lookup"><span data-stu-id="79a07-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="79a07-114">OS</span><span class="sxs-lookup"><span data-stu-id="79a07-114">PARAMETERS</span></span>

### <span data-ttu-id="79a07-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="79a07-115">-ApiManagement</span></span>
<span data-ttu-id="79a07-116">Especifica a instância **PsApiManagement** para a qual esse cmdlet adiciona mais regiões de implantação.</span><span class="sxs-lookup"><span data-stu-id="79a07-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="79a07-117">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="79a07-117">-Capacity</span></span>
<span data-ttu-id="79a07-118">Especifica a capacidade de SKU da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="79a07-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="79a07-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a07-119">-DefaultProfile</span></span>
<span data-ttu-id="79a07-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79a07-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79a07-121">-Local</span><span class="sxs-lookup"><span data-stu-id="79a07-121">-Location</span></span>
<span data-ttu-id="79a07-122">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="79a07-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="79a07-123">Para obter locais válidos, use o cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="79a07-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="79a07-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="79a07-124">-Sku</span></span>
<span data-ttu-id="79a07-125">Especifica a camada da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="79a07-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="79a07-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="79a07-126">Valid values are:</span></span> 
- <span data-ttu-id="79a07-127">Event</span><span class="sxs-lookup"><span data-stu-id="79a07-127">Developer</span></span>
- <span data-ttu-id="79a07-128">Oficial</span><span class="sxs-lookup"><span data-stu-id="79a07-128">Standard</span></span>
- <span data-ttu-id="79a07-129">Gratifica</span><span class="sxs-lookup"><span data-stu-id="79a07-129">Premium</span></span>

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

### <span data-ttu-id="79a07-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="79a07-130">-VirtualNetwork</span></span>
<span data-ttu-id="79a07-131">Especifica uma configuração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="79a07-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="79a07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a07-132">CommonParameters</span></span>
<span data-ttu-id="79a07-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a07-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79a07-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a07-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79a07-135">INPUTS</span></span>

### <span data-ttu-id="79a07-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="79a07-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="79a07-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79a07-137">OUTPUTS</span></span>

### <span data-ttu-id="79a07-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="79a07-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="79a07-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79a07-139">NOTES</span></span>
* <span data-ttu-id="79a07-140">O cmdlet grava a instância do **PsApiManagement** atualizado em pipeline.</span><span class="sxs-lookup"><span data-stu-id="79a07-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="79a07-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79a07-141">RELATED LINKS</span></span>

[<span data-ttu-id="79a07-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="79a07-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="79a07-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="79a07-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="79a07-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="79a07-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


