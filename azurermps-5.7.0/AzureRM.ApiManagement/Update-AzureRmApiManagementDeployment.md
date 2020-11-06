---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: 62400acbb9fb70f05772bd9749e39e3d7d62cc62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430539"
---
# <span data-ttu-id="2a530-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2a530-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="2a530-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a530-102">SYNOPSIS</span></span>
<span data-ttu-id="2a530-103">Atualiza a implantação de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2a530-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a530-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a530-104">SYNTAX</span></span>

### <span data-ttu-id="2a530-105">UpdateSpecificService (padrão)</span><span class="sxs-lookup"><span data-stu-id="2a530-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a530-106">UpdateFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="2a530-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a530-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a530-107">DESCRIPTION</span></span>
<span data-ttu-id="2a530-108">O cmdlet **Update-AzureRmApiManagementDeployment** atualiza implantações atuais de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2a530-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="2a530-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a530-109">EXAMPLES</span></span>

### <span data-ttu-id="2a530-110">Exemplo 1: atualizar uma implantação de uma instância do ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2a530-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="2a530-111">Este comando atualiza a implantação de uma instância de gerenciamento de API para um padrão de capacidade de três unidades.</span><span class="sxs-lookup"><span data-stu-id="2a530-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="2a530-112">Exemplo 2: obter uma instância do ApiManagement e redimensioná-la</span><span class="sxs-lookup"><span data-stu-id="2a530-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="2a530-113">Este exemplo obtém uma instância de gerenciamento de API, a dimensiona para cinco unidades Premium e, em seguida, adiciona outras três unidades à região Premium.</span><span class="sxs-lookup"><span data-stu-id="2a530-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="2a530-114">Exemplo 3: implantação de atualização (VNET externa)</span><span class="sxs-lookup"><span data-stu-id="2a530-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="2a530-115">Este comando atualiza uma implantação de gerenciamento de API existente e se une a um *VpnType* externo.</span><span class="sxs-lookup"><span data-stu-id="2a530-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="2a530-116">Exemplo 4: implantação de atualização (VNET interna)</span><span class="sxs-lookup"><span data-stu-id="2a530-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="2a530-117">Este comando atualiza uma implantação de gerenciamento de API existente e se une a um *VpnType* interno.</span><span class="sxs-lookup"><span data-stu-id="2a530-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="2a530-118">OS</span><span class="sxs-lookup"><span data-stu-id="2a530-118">PARAMETERS</span></span>

### <span data-ttu-id="2a530-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="2a530-119">-AdditionalRegions</span></span>
<span data-ttu-id="2a530-120">Especifica regiões de implantação adicionais do gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a530-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2a530-121">-ApiManagement</span></span>
<span data-ttu-id="2a530-122">Especifica a instância **PsApiManagement** da qual obter a configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="2a530-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="2a530-123">Use esse parâmetro se a instância já tiver todas as alterações necessárias.</span><span class="sxs-lookup"><span data-stu-id="2a530-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-124">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="2a530-124">-Capacity</span></span>
<span data-ttu-id="2a530-125">Especifica a capacidade de SKU da região mestra de implantação de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a530-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a530-126">-DefaultProfile</span></span>
<span data-ttu-id="2a530-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a530-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2a530-128">-Local</span><span class="sxs-lookup"><span data-stu-id="2a530-128">-Location</span></span>
<span data-ttu-id="2a530-129">Especifica o local da região de implantação de gerenciamento de API mestra.</span><span class="sxs-lookup"><span data-stu-id="2a530-129">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="2a530-130">Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="2a530-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a530-131">-Name</span></span>
<span data-ttu-id="2a530-132">Especifica o nome do gerenciamento de API que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="2a530-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a530-133">-PassThru</span></span>
<span data-ttu-id="2a530-134">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2a530-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a530-135">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="2a530-135">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a530-136">-ResourceGroupName</span></span>
<span data-ttu-id="2a530-137">Especifica o nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2a530-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="2a530-138">-Sku</span></span>
<span data-ttu-id="2a530-139">Especifica o nível da região de implantação mestra do Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="2a530-139">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="2a530-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2a530-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a530-141">Event</span><span class="sxs-lookup"><span data-stu-id="2a530-141">Developer</span></span>
- <span data-ttu-id="2a530-142">Oficial</span><span class="sxs-lookup"><span data-stu-id="2a530-142">Standard</span></span>
- <span data-ttu-id="2a530-143">Gratifica</span><span class="sxs-lookup"><span data-stu-id="2a530-143">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a530-144">-VirtualNetwork</span></span>
<span data-ttu-id="2a530-145">Especifica a configuração de rede virtual da região mestra de implantação de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a530-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="2a530-146">-VpnType</span></span>
<span data-ttu-id="2a530-147">Especifica o tipo de rede virtual da implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2a530-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="2a530-148">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2a530-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a530-149">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="2a530-149">None.</span></span>
<span data-ttu-id="2a530-150">A implantação de gerenciamento de API não faz parte de nenhuma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2a530-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="2a530-151">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="2a530-151">This is the default value.</span></span> 
- <span data-ttu-id="2a530-152">Externas.</span><span class="sxs-lookup"><span data-stu-id="2a530-152">External.</span></span>
<span data-ttu-id="2a530-153">A implantação de gerenciamento de API tem um endereço virtual de face externa.</span><span class="sxs-lookup"><span data-stu-id="2a530-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="2a530-154">Interno.</span><span class="sxs-lookup"><span data-stu-id="2a530-154">Internal.</span></span>
<span data-ttu-id="2a530-155">A implantação de gerenciamento de API tem um endereço virtual voltado para a intranet.</span><span class="sxs-lookup"><span data-stu-id="2a530-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a530-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a530-156">CommonParameters</span></span>
<span data-ttu-id="2a530-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a530-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a530-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a530-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a530-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a530-159">INPUTS</span></span>

### <span data-ttu-id="2a530-160">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2a530-160">PsApiManagement</span></span>
<span data-ttu-id="2a530-161">O parâmetro ' ApiManagement ' aceita o valor do tipo ' PsApiManagement ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2a530-161">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="2a530-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a530-162">OUTPUTS</span></span>

### <span data-ttu-id="2a530-163">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2a530-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2a530-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a530-164">NOTES</span></span>

## <span data-ttu-id="2a530-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a530-165">RELATED LINKS</span></span>

[<span data-ttu-id="2a530-166">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2a530-166">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


