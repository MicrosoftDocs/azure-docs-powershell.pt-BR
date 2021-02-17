---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: aebcb8be906811607aefee7dbdc2c7630b9e391e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401174"
---
# <span data-ttu-id="dc6c2-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="dc6c2-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="dc6c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc6c2-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6c2-103">Adiciona novas regiões de implantação a uma instância PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="dc6c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc6c2-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc6c2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc6c2-105">DESCRIPTION</span></span>
<span data-ttu-id="dc6c2-106">O cmdlet **Add-AzApiManagementRegion** adiciona uma nova instância do tipo **PsApiManagementRegion** ao conjunto de **AdditionalRegions** da instância fornecida do tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="dc6c2-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="dc6c2-107">Este cmdlet não implanta nada sozinho, mas atualiza a instância do **PsApiManagement** na memória.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="dc6c2-108">Para atualizar uma implantação de um Gerenciamento de API, passe a Instância **PsApiManagement** modificada para Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="dc6c2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dc6c2-109">EXAMPLES</span></span>

### <span data-ttu-id="dc6c2-110">Exemplo 1: Adicionar novas regiões de implantação a uma instância PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc6c2-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="dc6c2-111">Esse comando adiciona duas unidades de SKU premium e a região chamada Leste dos EUA à **instância PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="dc6c2-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="dc6c2-112">Exemplo 2: Adicionar novas regiões de implantação a uma instância PsApiManagement e atualizar a implantação</span><span class="sxs-lookup"><span data-stu-id="dc6c2-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Set-AzApiManagement
```

<span data-ttu-id="dc6c2-113">Esse comando obtém um **objeto PsApiManagement,** adiciona duas unidades de SKU premium para a região chamada Leste dos EUA e atualiza a implantação.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="dc6c2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc6c2-114">PARAMETERS</span></span>

### <span data-ttu-id="dc6c2-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc6c2-115">-ApiManagement</span></span>
<span data-ttu-id="dc6c2-116">Especifica a **instância PsApiManagement à** que este cmdlet adiciona regiões de implantação.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="dc6c2-117">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="dc6c2-117">-Capacity</span></span>
<span data-ttu-id="dc6c2-118">Especifica a capacidade da SKU da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="dc6c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6c2-119">-DefaultProfile</span></span>
<span data-ttu-id="dc6c2-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc6c2-121">-Local</span><span class="sxs-lookup"><span data-stu-id="dc6c2-121">-Location</span></span>
<span data-ttu-id="dc6c2-122">Especifica o local da nova região de implantação entre a região com suporte para o serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="dc6c2-123">Para obter locais válidos, use o cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | onde {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object locais</span><span class="sxs-lookup"><span data-stu-id="dc6c2-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="dc6c2-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="dc6c2-124">-Sku</span></span>
<span data-ttu-id="dc6c2-125">Especifica o nível da região de implantação.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="dc6c2-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dc6c2-126">Valid values are:</span></span>
- <span data-ttu-id="dc6c2-127">Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="dc6c2-127">Developer</span></span>
- <span data-ttu-id="dc6c2-128">Padrão</span><span class="sxs-lookup"><span data-stu-id="dc6c2-128">Standard</span></span>
- <span data-ttu-id="dc6c2-129">Premium</span><span class="sxs-lookup"><span data-stu-id="dc6c2-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6c2-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dc6c2-130">-VirtualNetwork</span></span>
<span data-ttu-id="dc6c2-131">Especifica uma configuração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="dc6c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6c2-132">CommonParameters</span></span>
<span data-ttu-id="dc6c2-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6c2-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc6c2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6c2-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="dc6c2-135">INPUTS</span></span>

### <span data-ttu-id="dc6c2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc6c2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="dc6c2-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="dc6c2-137">OUTPUTS</span></span>

### <span data-ttu-id="dc6c2-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc6c2-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="dc6c2-139">Notas</span><span class="sxs-lookup"><span data-stu-id="dc6c2-139">NOTES</span></span>
* <span data-ttu-id="dc6c2-140">O cmdlet grava a instância **PsApiManagement atualizada** no pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc6c2-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="dc6c2-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc6c2-141">RELATED LINKS</span></span>

[<span data-ttu-id="dc6c2-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="dc6c2-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="dc6c2-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="dc6c2-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="dc6c2-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dc6c2-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


