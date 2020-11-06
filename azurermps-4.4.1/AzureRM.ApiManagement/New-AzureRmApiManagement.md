---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431243"
---
# <span data-ttu-id="526ff-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="526ff-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="526ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="526ff-102">SYNOPSIS</span></span>
<span data-ttu-id="526ff-103">Cria uma implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="526ff-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="526ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="526ff-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="526ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="526ff-105">DESCRIPTION</span></span>
<span data-ttu-id="526ff-106">O cmdlet **New-AzureRmApiManagement** cria uma implantação de gerenciamento de API no gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="526ff-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="526ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="526ff-107">EXAMPLES</span></span>

### <span data-ttu-id="526ff-108">Exemplo 1: criar um serviço de gerenciamento de API de camada de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="526ff-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="526ff-109">Esse comando cria um serviço de gerenciamento de API de camada de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="526ff-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="526ff-110">O comando especifica a organização e o endereço de administrador.</span><span class="sxs-lookup"><span data-stu-id="526ff-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="526ff-111">O comando não especifica o parâmetro *SKU* .</span><span class="sxs-lookup"><span data-stu-id="526ff-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="526ff-112">Portanto, o cmdlet usa o valor padrão do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="526ff-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="526ff-113">Exemplo 2: criar um serviço de camada padrão com três unidades</span><span class="sxs-lookup"><span data-stu-id="526ff-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="526ff-114">Esse comando cria um serviço de gerenciamento de API de camada padrão que tem três unidades.</span><span class="sxs-lookup"><span data-stu-id="526ff-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="526ff-115">Exemplo 3: criar um serviço de gerenciamento de API para uma rede virtual externa</span><span class="sxs-lookup"><span data-stu-id="526ff-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="526ff-116">Esse comando cria um serviço de gerenciamento de API de camada Premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway externo com uma região mestre nos EUA do oeste.</span><span class="sxs-lookup"><span data-stu-id="526ff-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="526ff-117">Exemplo 4: criar um serviço de gerenciamento de API para uma rede virtual interna</span><span class="sxs-lookup"><span data-stu-id="526ff-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="526ff-118">Esse comando cria um serviço de gerenciamento de API de camada Premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway de face interna com uma região mestre nos EUA do oeste.</span><span class="sxs-lookup"><span data-stu-id="526ff-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="526ff-119">OS</span><span class="sxs-lookup"><span data-stu-id="526ff-119">PARAMETERS</span></span>

### <span data-ttu-id="526ff-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="526ff-120">-AdditionalRegions</span></span>
<span data-ttu-id="526ff-121">Regiões de implantação adicionais do gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="526ff-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526ff-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="526ff-122">-AdminEmail</span></span>
<span data-ttu-id="526ff-123">Especifica o endereço de email de origem para todas as notificações que o sistema de gerenciamento de API envia.</span><span class="sxs-lookup"><span data-stu-id="526ff-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="526ff-124">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="526ff-124">-Capacity</span></span>
<span data-ttu-id="526ff-125">Especifica a capacidade de SKU do serviço de gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="526ff-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="526ff-126">O padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="526ff-126">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526ff-127">-Local</span><span class="sxs-lookup"><span data-stu-id="526ff-127">-Location</span></span>
<span data-ttu-id="526ff-128">Especifica o local em que esse cmdlet cria uma implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="526ff-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="526ff-129">Para obter locais válidos, use os cmdlets Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="526ff-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="526ff-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="526ff-130">Valid values are:</span></span> 

- <span data-ttu-id="526ff-131">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="526ff-131">North Central US</span></span>
- <span data-ttu-id="526ff-132">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="526ff-132">South Central US</span></span>
- <span data-ttu-id="526ff-133">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="526ff-133">Central US</span></span>
- <span data-ttu-id="526ff-134">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="526ff-134">West Europe</span></span>
- <span data-ttu-id="526ff-135">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="526ff-135">North Europe</span></span>
- <span data-ttu-id="526ff-136">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="526ff-136">West US</span></span>
- <span data-ttu-id="526ff-137">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="526ff-137">East US</span></span>
- <span data-ttu-id="526ff-138">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="526ff-138">East US 2</span></span>
- <span data-ttu-id="526ff-139">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="526ff-139">Japan East</span></span>
- <span data-ttu-id="526ff-140">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="526ff-140">Japan West</span></span>
- <span data-ttu-id="526ff-141">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="526ff-141">Brazil South</span></span>
- <span data-ttu-id="526ff-142">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="526ff-142">Southeast Asia</span></span>
- <span data-ttu-id="526ff-143">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="526ff-143">East Asia</span></span>
- <span data-ttu-id="526ff-144">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="526ff-144">Australia East</span></span>
- <span data-ttu-id="526ff-145">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="526ff-145">Australia Southeast</span></span>

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

### <span data-ttu-id="526ff-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="526ff-146">-Name</span></span>
<span data-ttu-id="526ff-147">Especifica um nome para a implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="526ff-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="526ff-148">-Organização</span><span class="sxs-lookup"><span data-stu-id="526ff-148">-Organization</span></span>
<span data-ttu-id="526ff-149">Especifica o nome de uma organização.</span><span class="sxs-lookup"><span data-stu-id="526ff-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="526ff-150">O gerenciamento de APIs usa esse endereço no portal do desenvolvedor em notificações por email.</span><span class="sxs-lookup"><span data-stu-id="526ff-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="526ff-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="526ff-151">-ResourceGroupName</span></span>
<span data-ttu-id="526ff-152">Especifica o nome do grupo de recursos sob o qual esse cmdlet cria uma implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="526ff-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="526ff-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="526ff-153">-Sku</span></span>
<span data-ttu-id="526ff-154">Especifica a camada do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="526ff-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="526ff-155">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="526ff-155">Valid values are:</span></span> 

- <span data-ttu-id="526ff-156">Event</span><span class="sxs-lookup"><span data-stu-id="526ff-156">Developer</span></span> 
- <span data-ttu-id="526ff-157">Oficial</span><span class="sxs-lookup"><span data-stu-id="526ff-157">Standard</span></span> 
- <span data-ttu-id="526ff-158">Gratifica</span><span class="sxs-lookup"><span data-stu-id="526ff-158">Premium</span></span> 

<span data-ttu-id="526ff-159">O padrão é desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="526ff-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526ff-160">-Marcas</span><span class="sxs-lookup"><span data-stu-id="526ff-160">-Tags</span></span>
<span data-ttu-id="526ff-161">Especifica um dicionário de marcas.</span><span class="sxs-lookup"><span data-stu-id="526ff-161">Specifies a dictionary of tags.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526ff-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="526ff-162">-VirtualNetwork</span></span>
<span data-ttu-id="526ff-163">Configuração de rede virtual da região de implantação do gerenciamento de API do Azure mestre.</span><span class="sxs-lookup"><span data-stu-id="526ff-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="526ff-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="526ff-164">-VpnType</span></span>
<span data-ttu-id="526ff-165">Tipo de rede virtual da implantação do ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="526ff-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="526ff-166">Valores válidos são</span><span class="sxs-lookup"><span data-stu-id="526ff-166">Valid Values are</span></span> 
- <span data-ttu-id="526ff-167">"Nenhum" (valor padrão.</span><span class="sxs-lookup"><span data-stu-id="526ff-167">"None" (Default Value.</span></span> <span data-ttu-id="526ff-168">O ApiManagement não faz parte de uma rede virtual ")</span><span class="sxs-lookup"><span data-stu-id="526ff-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="526ff-169">"Externo" (a implantação do ApiManagement é configurada dentro de uma rede virtual com um ponto de extremidade voltado para a Internet)</span><span class="sxs-lookup"><span data-stu-id="526ff-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="526ff-170">"Internal" (a implantação do ApiManagement é configurada dentro de uma rede virtual com um ponto de extremidade voltado à intranet)</span><span class="sxs-lookup"><span data-stu-id="526ff-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526ff-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="526ff-171">-DefaultProfile</span></span>
<span data-ttu-id="526ff-172">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="526ff-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="526ff-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="526ff-173">CommonParameters</span></span>
<span data-ttu-id="526ff-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="526ff-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="526ff-175">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="526ff-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="526ff-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="526ff-176">INPUTS</span></span>

## <span data-ttu-id="526ff-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="526ff-177">OUTPUTS</span></span>

### <span data-ttu-id="526ff-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="526ff-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="526ff-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="526ff-179">NOTES</span></span>

## <span data-ttu-id="526ff-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="526ff-180">RELATED LINKS</span></span>

[<span data-ttu-id="526ff-181">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="526ff-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="526ff-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="526ff-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="526ff-183">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="526ff-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="526ff-184">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="526ff-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


