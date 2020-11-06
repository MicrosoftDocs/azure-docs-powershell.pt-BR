---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427012"
---
# <span data-ttu-id="93b0f-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="93b0f-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="93b0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="93b0f-103">Atualiza a implantação de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="93b0f-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93b0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93b0f-104">SYNTAX</span></span>

### <span data-ttu-id="93b0f-105">Serviço de gerenciamento de API específico (padrão)</span><span class="sxs-lookup"><span data-stu-id="93b0f-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93b0f-106">Atualizar a partir da instância PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="93b0f-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93b0f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93b0f-107">DESCRIPTION</span></span>
<span data-ttu-id="93b0f-108">O cmdlet **Update-AzureRmApiManagementDeployment** atualiza implantações atuais de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="93b0f-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="93b0f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93b0f-109">EXAMPLES</span></span>

### <span data-ttu-id="93b0f-110">Exemplo 1: atualizar uma implantação de uma instância do ApiManagement</span><span class="sxs-lookup"><span data-stu-id="93b0f-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="93b0f-111">Este comando atualiza a implantação de uma instância de gerenciamento de API para um padrão de capacidade de três unidades.</span><span class="sxs-lookup"><span data-stu-id="93b0f-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="93b0f-112">Exemplo 2: obter uma instância do ApiManagement e redimensioná-la</span><span class="sxs-lookup"><span data-stu-id="93b0f-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="93b0f-113">Este exemplo obtém uma instância de gerenciamento de API, a dimensiona para cinco unidades Premium e, em seguida, adiciona outras três unidades à região Premium.</span><span class="sxs-lookup"><span data-stu-id="93b0f-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="93b0f-114">Exemplo 3: implantação de atualização (VNET externa)</span><span class="sxs-lookup"><span data-stu-id="93b0f-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="93b0f-115">Este comando atualiza uma implantação de gerenciamento de API existente e se une a um *VpnType* externo.</span><span class="sxs-lookup"><span data-stu-id="93b0f-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="93b0f-116">Exemplo 4: implantação de atualização (VNET interna)</span><span class="sxs-lookup"><span data-stu-id="93b0f-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="93b0f-117">Este comando atualiza uma implantação de gerenciamento de API existente e se une a um *VpnType* interno.</span><span class="sxs-lookup"><span data-stu-id="93b0f-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="93b0f-118">OS</span><span class="sxs-lookup"><span data-stu-id="93b0f-118">PARAMETERS</span></span>

### <span data-ttu-id="93b0f-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="93b0f-119">-AdditionalRegions</span></span>
<span data-ttu-id="93b0f-120">Especifica regiões de implantação adicionais do gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="93b0f-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="93b0f-121">-ApiManagement</span></span>
<span data-ttu-id="93b0f-122">Especifica a instância **PsApiManagement** da qual obter a configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="93b0f-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="93b0f-123">Use esse parâmetro se a instância já tiver todas as alterações necessárias.</span><span class="sxs-lookup"><span data-stu-id="93b0f-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-124">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="93b0f-124">-Capacity</span></span>
<span data-ttu-id="93b0f-125">Especifica a capacidade de SKU da região mestra de implantação de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="93b0f-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-126">-Local</span><span class="sxs-lookup"><span data-stu-id="93b0f-126">-Location</span></span>
<span data-ttu-id="93b0f-127">Especifica o local da região de implantação de gerenciamento de API mestra.</span><span class="sxs-lookup"><span data-stu-id="93b0f-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="93b0f-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="93b0f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93b0f-129">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="93b0f-129">North Central US</span></span>
- <span data-ttu-id="93b0f-130">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="93b0f-130">South Central US</span></span>
- <span data-ttu-id="93b0f-131">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="93b0f-131">Central US</span></span>
- <span data-ttu-id="93b0f-132">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="93b0f-132">West Europe</span></span>
- <span data-ttu-id="93b0f-133">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="93b0f-133">North Europe</span></span>
- <span data-ttu-id="93b0f-134">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="93b0f-134">West US</span></span>
- <span data-ttu-id="93b0f-135">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="93b0f-135">East US</span></span>
- <span data-ttu-id="93b0f-136">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="93b0f-136">East US 2</span></span>
- <span data-ttu-id="93b0f-137">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="93b0f-137">Japan East</span></span>
- <span data-ttu-id="93b0f-138">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="93b0f-138">Japan West</span></span>
- <span data-ttu-id="93b0f-139">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="93b0f-139">Brazil South</span></span>
- <span data-ttu-id="93b0f-140">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="93b0f-140">Southeast Asia</span></span>
- <span data-ttu-id="93b0f-141">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="93b0f-141">East Asia</span></span>
- <span data-ttu-id="93b0f-142">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="93b0f-142">Australia East</span></span>
- <span data-ttu-id="93b0f-143">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="93b0f-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="93b0f-144">-Name</span></span>
<span data-ttu-id="93b0f-145">Especifica o nome do gerenciamento de API que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="93b0f-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93b0f-146">-PassThru</span></span>
<span data-ttu-id="93b0f-147">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="93b0f-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="93b0f-148">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="93b0f-148">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93b0f-149">-ResourceGroupName</span></span>
<span data-ttu-id="93b0f-150">Especifica o nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="93b0f-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="93b0f-151">-Sku</span></span>
<span data-ttu-id="93b0f-152">Especifica o nível da região de implantação mestra do Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="93b0f-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="93b0f-153">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="93b0f-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93b0f-154">Event</span><span class="sxs-lookup"><span data-stu-id="93b0f-154">Developer</span></span>
- <span data-ttu-id="93b0f-155">Oficial</span><span class="sxs-lookup"><span data-stu-id="93b0f-155">Standard</span></span>
- <span data-ttu-id="93b0f-156">Gratifica</span><span class="sxs-lookup"><span data-stu-id="93b0f-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="93b0f-157">-VirtualNetwork</span></span>
<span data-ttu-id="93b0f-158">Especifica a configuração de rede virtual da região mestra de implantação de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="93b0f-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="93b0f-159">-VpnType</span></span>
<span data-ttu-id="93b0f-160">Especifica o tipo de rede virtual da implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="93b0f-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="93b0f-161">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="93b0f-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93b0f-162">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="93b0f-162">None.</span></span>
<span data-ttu-id="93b0f-163">A implantação de gerenciamento de API não faz parte de nenhuma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="93b0f-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="93b0f-164">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="93b0f-164">This is the default value.</span></span> 
- <span data-ttu-id="93b0f-165">Externas.</span><span class="sxs-lookup"><span data-stu-id="93b0f-165">External.</span></span>
<span data-ttu-id="93b0f-166">A implantação de gerenciamento de API tem um endereço virtual de face externa.</span><span class="sxs-lookup"><span data-stu-id="93b0f-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="93b0f-167">Interno.</span><span class="sxs-lookup"><span data-stu-id="93b0f-167">Internal.</span></span>
<span data-ttu-id="93b0f-168">A implantação de gerenciamento de API tem um endereço virtual voltado para a intranet.</span><span class="sxs-lookup"><span data-stu-id="93b0f-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b0f-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b0f-169">-DefaultProfile</span></span>
<span data-ttu-id="93b0f-170">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93b0f-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93b0f-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b0f-171">CommonParameters</span></span>
<span data-ttu-id="93b0f-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b0f-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b0f-173">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b0f-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b0f-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93b0f-174">INPUTS</span></span>

### <span data-ttu-id="93b0f-175">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="93b0f-175">PsApiManagement</span></span>
<span data-ttu-id="93b0f-176">O parâmetro ' ApiManagement ' aceita o valor do tipo ' PsApiManagement ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="93b0f-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="93b0f-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93b0f-177">OUTPUTS</span></span>

### <span data-ttu-id="93b0f-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="93b0f-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="93b0f-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93b0f-179">NOTES</span></span>

## <span data-ttu-id="93b0f-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93b0f-180">RELATED LINKS</span></span>

[<span data-ttu-id="93b0f-181">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="93b0f-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


