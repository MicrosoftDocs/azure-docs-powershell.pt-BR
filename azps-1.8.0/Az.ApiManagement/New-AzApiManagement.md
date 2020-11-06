---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 43393995fcc370e2b3ff2b20586ab696c39d059b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595656"
---
# <span data-ttu-id="6ddb6-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ddb6-101">New-AzApiManagement</span></span>

## <span data-ttu-id="6ddb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ddb6-102">SYNOPSIS</span></span>
<span data-ttu-id="6ddb6-103">Cria uma implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="6ddb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ddb6-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ddb6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ddb6-105">DESCRIPTION</span></span>
<span data-ttu-id="6ddb6-106">O cmdlet **New-AzApiManagement** cria uma implantação de gerenciamento de API no gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="6ddb6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ddb6-107">EXAMPLES</span></span>

### <span data-ttu-id="6ddb6-108">Exemplo 1: criar um serviço de gerenciamento de API de camada de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="6ddb6-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="6ddb6-109">Esse comando cria um serviço de gerenciamento de API de camada de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="6ddb6-110">O comando especifica a organização e o endereço de administrador.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="6ddb6-111">O comando não especifica o parâmetro *SKU* .</span><span class="sxs-lookup"><span data-stu-id="6ddb6-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="6ddb6-112">Portanto, o cmdlet usa o valor padrão do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="6ddb6-113">Exemplo 2: criar um serviço de camada padrão com três unidades</span><span class="sxs-lookup"><span data-stu-id="6ddb6-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="6ddb6-114">Esse comando cria um serviço de gerenciamento de API de camada padrão que tem três unidades.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="6ddb6-115">Exemplo 3: criar um serviço de gerenciamento de API para uma rede virtual externa</span><span class="sxs-lookup"><span data-stu-id="6ddb6-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="6ddb6-116">Esse comando cria um serviço de gerenciamento de API de camada Premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway externo com uma região mestre nos EUA do oeste.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="6ddb6-117">Exemplo 4: criar um serviço de gerenciamento de API para uma rede virtual interna</span><span class="sxs-lookup"><span data-stu-id="6ddb6-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="6ddb6-118">Esse comando cria um serviço de gerenciamento de API de camada Premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway de face interna com uma região mestre nos EUA do oeste.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="6ddb6-119">OS</span><span class="sxs-lookup"><span data-stu-id="6ddb6-119">PARAMETERS</span></span>

### <span data-ttu-id="6ddb6-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="6ddb6-120">-AdditionalRegions</span></span>
<span data-ttu-id="6ddb6-121">Regiões de implantação adicionais do gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="6ddb6-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="6ddb6-122">-AdminEmail</span></span>
<span data-ttu-id="6ddb6-123">Especifica o endereço de email de origem para todas as notificações que o sistema de gerenciamento de API envia.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="6ddb6-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6ddb6-124">-AssignIdentity</span></span>
<span data-ttu-id="6ddb6-125">Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="6ddb6-126">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="6ddb6-126">-Capacity</span></span>
<span data-ttu-id="6ddb6-127">Especifica a capacidade de SKU do serviço de gerenciamento de APIs do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="6ddb6-128">O padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="6ddb6-128">The default is one (1).</span></span>

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

### <span data-ttu-id="6ddb6-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ddb6-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="6ddb6-130">Configurações personalizadas de nome de host.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-130">Custom hostname configurations.</span></span> <span data-ttu-id="6ddb6-131">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-131">Default value is $null.</span></span> <span data-ttu-id="6ddb6-132">Ao passar $null, o nome do host padrão será definido.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-132">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ddb6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ddb6-133">-DefaultProfile</span></span>
<span data-ttu-id="6ddb6-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ddb6-135">-Local</span><span class="sxs-lookup"><span data-stu-id="6ddb6-135">-Location</span></span>
<span data-ttu-id="6ddb6-136">Especifica o local para criar o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="6ddb6-137">Para obter locais válidos, use o cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="6ddb6-137">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="6ddb6-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ddb6-138">-Name</span></span>
<span data-ttu-id="6ddb6-139">Especifica um nome para a implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="6ddb6-140">-Organização</span><span class="sxs-lookup"><span data-stu-id="6ddb6-140">-Organization</span></span>
<span data-ttu-id="6ddb6-141">Especifica o nome de uma organização.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="6ddb6-142">O gerenciamento de APIs usa esse endereço no portal do desenvolvedor em notificações por email.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="6ddb6-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ddb6-143">-ResourceGroupName</span></span>
<span data-ttu-id="6ddb6-144">Especifica o nome do grupo de recursos sob o qual esse cmdlet cria uma implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="6ddb6-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="6ddb6-145">-Sku</span></span>
<span data-ttu-id="6ddb6-146">Especifica a camada do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="6ddb6-147">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6ddb6-147">Valid values are:</span></span> 
- <span data-ttu-id="6ddb6-148">Event</span><span class="sxs-lookup"><span data-stu-id="6ddb6-148">Developer</span></span> 
- <span data-ttu-id="6ddb6-149">Oficial</span><span class="sxs-lookup"><span data-stu-id="6ddb6-149">Standard</span></span> 
- <span data-ttu-id="6ddb6-150">Premium o padrão é desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ddb6-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ddb6-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="6ddb6-152">Certificados emitidos pela CA interna a serem instalados no serviço.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="6ddb6-153">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-153">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ddb6-154">-Marca</span><span class="sxs-lookup"><span data-stu-id="6ddb6-154">-Tag</span></span>
<span data-ttu-id="6ddb6-155">Dicionário de marcas.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="6ddb6-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ddb6-156">-VirtualNetwork</span></span>
<span data-ttu-id="6ddb6-157">Configuração de rede virtual da região de implantação do gerenciamento de API do Azure mestre.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="6ddb6-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="6ddb6-158">-VpnType</span></span>
<span data-ttu-id="6ddb6-159">Tipo de rede virtual da implantação do ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="6ddb6-160">Valores válidos são</span><span class="sxs-lookup"><span data-stu-id="6ddb6-160">Valid Values are</span></span> 
- <span data-ttu-id="6ddb6-161">"Nenhum" (valor padrão.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-161">"None" (Default Value.</span></span> <span data-ttu-id="6ddb6-162">O ApiManagement não faz parte de uma rede virtual ")</span><span class="sxs-lookup"><span data-stu-id="6ddb6-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="6ddb6-163">"Externo" (a implantação do ApiManagement é configurada dentro de uma rede virtual com um ponto de extremidade voltado para a Internet)</span><span class="sxs-lookup"><span data-stu-id="6ddb6-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="6ddb6-164">"Internal" (a implantação do ApiManagement é configurada dentro de uma rede virtual com um ponto de extremidade voltado à intranet)</span><span class="sxs-lookup"><span data-stu-id="6ddb6-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="6ddb6-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ddb6-165">CommonParameters</span></span>
<span data-ttu-id="6ddb6-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ddb6-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ddb6-167">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ddb6-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ddb6-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ddb6-168">INPUTS</span></span>

### <span data-ttu-id="6ddb6-169">System. String</span><span class="sxs-lookup"><span data-stu-id="6ddb6-169">System.String</span></span>

### <span data-ttu-id="6ddb6-170">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. PowerShell. cmdlets. ApiManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6ddb6-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6ddb6-171">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6ddb6-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6ddb6-172">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ddb6-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="6ddb6-173">System. Collections. Generic. Dictionary ' 2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6ddb6-173">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6ddb6-174">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="6ddb6-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="6ddb6-175">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6ddb6-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="6ddb6-176">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="6ddb6-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="6ddb6-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ddb6-177">OUTPUTS</span></span>

### <span data-ttu-id="6ddb6-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ddb6-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="6ddb6-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ddb6-179">NOTES</span></span>

## <span data-ttu-id="6ddb6-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ddb6-180">RELATED LINKS</span></span>

[<span data-ttu-id="6ddb6-181">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ddb6-181">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="6ddb6-182">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ddb6-182">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="6ddb6-183">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ddb6-183">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="6ddb6-184">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ddb6-184">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="6ddb6-185">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ddb6-185">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


