---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440536"
---
# <span data-ttu-id="52760-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="52760-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="52760-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52760-102">SYNOPSIS</span></span>
<span data-ttu-id="52760-103">Cria uma implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="52760-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52760-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52760-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52760-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52760-105">DESCRIPTION</span></span>
<span data-ttu-id="52760-106">O cmdlet **New-AzureRmApiManagement** cria uma implantação de gerenciamento de API no gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="52760-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="52760-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52760-107">EXAMPLES</span></span>

### <span data-ttu-id="52760-108">Exemplo 1: criar um serviço de gerenciamento de API de camada de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="52760-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="52760-109">Esse comando cria um serviço de gerenciamento de API de camada de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="52760-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="52760-110">O comando especifica a organização e o endereço de administrador.</span><span class="sxs-lookup"><span data-stu-id="52760-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="52760-111">O comando não especifica o parâmetro *SKU* .</span><span class="sxs-lookup"><span data-stu-id="52760-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="52760-112">Portanto, o cmdlet usa o valor padrão do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="52760-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="52760-113">Exemplo 2: criar um serviço de camada padrão com três unidades</span><span class="sxs-lookup"><span data-stu-id="52760-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="52760-114">Esse comando cria um serviço de gerenciamento de API de camada padrão que tem três unidades.</span><span class="sxs-lookup"><span data-stu-id="52760-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="52760-115">Exemplo 3: criar um serviço de gerenciamento de API para uma rede virtual externa</span><span class="sxs-lookup"><span data-stu-id="52760-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="52760-116">Esse comando cria um serviço de gerenciamento de API de camada Premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway externo com uma região mestre nos EUA do oeste.</span><span class="sxs-lookup"><span data-stu-id="52760-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="52760-117">Exemplo 4: criar um serviço de gerenciamento de API para uma rede virtual interna</span><span class="sxs-lookup"><span data-stu-id="52760-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="52760-118">Esse comando cria um serviço de gerenciamento de API de camada Premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway de face interna com uma região mestre nos EUA do oeste.</span><span class="sxs-lookup"><span data-stu-id="52760-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="52760-119">OS</span><span class="sxs-lookup"><span data-stu-id="52760-119">PARAMETERS</span></span>

### <span data-ttu-id="52760-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="52760-120">-AdditionalRegions</span></span>
<span data-ttu-id="52760-121">Regiões de implantação adicionais do gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="52760-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52760-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="52760-122">-AdminEmail</span></span>
<span data-ttu-id="52760-123">Especifica o endereço de email de origem para todas as notificações que o sistema de gerenciamento de API envia.</span><span class="sxs-lookup"><span data-stu-id="52760-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="52760-124">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="52760-124">-Capacity</span></span>
<span data-ttu-id="52760-125">Especifica a capacidade de SKU do serviço de gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="52760-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="52760-126">O padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="52760-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52760-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52760-127">-DefaultProfile</span></span>
<span data-ttu-id="52760-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52760-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="52760-129">-Local</span><span class="sxs-lookup"><span data-stu-id="52760-129">-Location</span></span>
<span data-ttu-id="52760-130">Especifica o local para criar o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="52760-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="52760-131">Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="52760-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="52760-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="52760-132">-Name</span></span>
<span data-ttu-id="52760-133">Especifica um nome para a implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="52760-133">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="52760-134">-Organização</span><span class="sxs-lookup"><span data-stu-id="52760-134">-Organization</span></span>
<span data-ttu-id="52760-135">Especifica o nome de uma organização.</span><span class="sxs-lookup"><span data-stu-id="52760-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="52760-136">O gerenciamento de APIs usa esse endereço no portal do desenvolvedor em notificações por email.</span><span class="sxs-lookup"><span data-stu-id="52760-136">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="52760-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52760-137">-ResourceGroupName</span></span>
<span data-ttu-id="52760-138">Especifica o nome do grupo de recursos sob o qual esse cmdlet cria uma implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="52760-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="52760-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="52760-139">-Sku</span></span>
<span data-ttu-id="52760-140">Especifica a camada do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="52760-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="52760-141">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="52760-141">Valid values are:</span></span> 

- <span data-ttu-id="52760-142">Event</span><span class="sxs-lookup"><span data-stu-id="52760-142">Developer</span></span> 
- <span data-ttu-id="52760-143">Oficial</span><span class="sxs-lookup"><span data-stu-id="52760-143">Standard</span></span> 
- <span data-ttu-id="52760-144">Gratifica</span><span class="sxs-lookup"><span data-stu-id="52760-144">Premium</span></span> 

<span data-ttu-id="52760-145">O padrão é desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="52760-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52760-146">-Marca</span><span class="sxs-lookup"><span data-stu-id="52760-146">-Tag</span></span>
<span data-ttu-id="52760-147">Dicionário de marcas.</span><span class="sxs-lookup"><span data-stu-id="52760-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52760-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="52760-148">-VirtualNetwork</span></span>
<span data-ttu-id="52760-149">Configuração de rede virtual da região de implantação do gerenciamento de API do Azure mestre.</span><span class="sxs-lookup"><span data-stu-id="52760-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="52760-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="52760-150">-VpnType</span></span>
<span data-ttu-id="52760-151">Tipo de rede virtual da implantação do ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="52760-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="52760-152">Valores válidos são</span><span class="sxs-lookup"><span data-stu-id="52760-152">Valid Values are</span></span> 
- <span data-ttu-id="52760-153">"Nenhum" (valor padrão.</span><span class="sxs-lookup"><span data-stu-id="52760-153">"None" (Default Value.</span></span> <span data-ttu-id="52760-154">O ApiManagement não faz parte de uma rede virtual ")</span><span class="sxs-lookup"><span data-stu-id="52760-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="52760-155">"Externo" (a implantação do ApiManagement é configurada dentro de uma rede virtual com um ponto de extremidade voltado para a Internet)</span><span class="sxs-lookup"><span data-stu-id="52760-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="52760-156">"Internal" (a implantação do ApiManagement é configurada dentro de uma rede virtual com um ponto de extremidade voltado à intranet)</span><span class="sxs-lookup"><span data-stu-id="52760-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52760-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52760-157">CommonParameters</span></span>
<span data-ttu-id="52760-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52760-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52760-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52760-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52760-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52760-160">INPUTS</span></span>

### <span data-ttu-id="52760-161">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="52760-161">None</span></span>
<span data-ttu-id="52760-162">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="52760-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52760-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52760-163">OUTPUTS</span></span>

### <span data-ttu-id="52760-164">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="52760-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="52760-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52760-165">NOTES</span></span>

## <span data-ttu-id="52760-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52760-166">RELATED LINKS</span></span>

[<span data-ttu-id="52760-167">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="52760-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="52760-168">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="52760-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="52760-169">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="52760-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="52760-170">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="52760-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


