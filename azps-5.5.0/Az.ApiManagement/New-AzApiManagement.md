---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114841"
---
# <span data-ttu-id="2de46-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2de46-101">New-AzApiManagement</span></span>

## <span data-ttu-id="2de46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2de46-102">SYNOPSIS</span></span>
<span data-ttu-id="2de46-103">Cria uma implantação de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2de46-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="2de46-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2de46-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2de46-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2de46-105">DESCRIPTION</span></span>
<span data-ttu-id="2de46-106">O **cmdlet New-AzApiManagement cria** uma implantação de Gerenciamento de API no Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2de46-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="2de46-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2de46-107">EXAMPLES</span></span>

### <span data-ttu-id="2de46-108">Exemplo 1: Criar um serviço de Gerenciamento de API de nível de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="2de46-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="2de46-109">Esse comando cria um serviço de Gerenciamento de API de nível de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="2de46-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="2de46-110">O comando especifica a organização e o endereço do administrador.</span><span class="sxs-lookup"><span data-stu-id="2de46-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="2de46-111">O comando não especifica o parâmetro *SKU.*</span><span class="sxs-lookup"><span data-stu-id="2de46-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="2de46-112">Portanto, o cmdlet usa o valor padrão de Desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="2de46-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="2de46-113">Exemplo 2: Criar um serviço de camada padrão que tenha três unidades</span><span class="sxs-lookup"><span data-stu-id="2de46-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="2de46-114">Esse comando cria um serviço de Gerenciamento de API de nível padrão que tem três unidades.</span><span class="sxs-lookup"><span data-stu-id="2de46-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="2de46-115">Exemplo 3: Criar um serviço de camada consumo</span><span class="sxs-lookup"><span data-stu-id="2de46-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="2de46-116">Esse comando cria um serviço de Gerenciamento de API de nível de consumo com Certificado de Cliente habilitado no oeste da Europa.</span><span class="sxs-lookup"><span data-stu-id="2de46-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="2de46-117">Exemplo 4: Criar um serviço de Gerenciamento de API para uma rede virtual externa</span><span class="sxs-lookup"><span data-stu-id="2de46-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="2de46-118">Esse comando cria um serviço de Gerenciamento de API de nível premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway voltado para externo com uma região mestra no Oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="2de46-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="2de46-119">Exemplo 5: Criar um serviço de Gerenciamento de API para uma rede virtual interna</span><span class="sxs-lookup"><span data-stu-id="2de46-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="2de46-120">Esse comando cria um serviço de Gerenciamento de API de nível premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway voltado para interno com uma região mestra no Oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="2de46-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="2de46-121">Exemplo 6: Criar um serviço de gerenciamento de API e habilitar o protocolo TLS 1.0</span><span class="sxs-lookup"><span data-stu-id="2de46-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="2de46-122">Esse comando cria um serviço de Gerenciamento de Api SKU Padrão e Habilita o TLS 1.0 no cliente Frontend para o cliente ApiManagement Gateway e Backend entre ApiManagement Gateway e Backend.</span><span class="sxs-lookup"><span data-stu-id="2de46-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="2de46-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2de46-123">PARAMETERS</span></span>

### <span data-ttu-id="2de46-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="2de46-124">-AdditionalRegions</span></span>
<span data-ttu-id="2de46-125">Regiões de implantação adicionais do Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2de46-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="2de46-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="2de46-126">-AdminEmail</span></span>
<span data-ttu-id="2de46-127">Especifica o endereço de email de origem para todas as notificações que o sistema de Gerenciamento de API envia.</span><span class="sxs-lookup"><span data-stu-id="2de46-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="2de46-128">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="2de46-128">-Capacity</span></span>
<span data-ttu-id="2de46-129">Especifica a capacidade da SKU do serviço de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2de46-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="2de46-130">O padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="2de46-130">The default is one (1).</span></span>

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

### <span data-ttu-id="2de46-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2de46-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="2de46-132">Configurações personalizadas do nome do host.</span><span class="sxs-lookup"><span data-stu-id="2de46-132">Custom hostname configurations.</span></span> <span data-ttu-id="2de46-133">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="2de46-133">Default value is $null.</span></span> <span data-ttu-id="2de46-134">Passar $null definirá o nome de host padrão.</span><span class="sxs-lookup"><span data-stu-id="2de46-134">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="2de46-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de46-135">-DefaultProfile</span></span>
<span data-ttu-id="2de46-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2de46-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2de46-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2de46-137">-EnableClientCertificate</span></span>
<span data-ttu-id="2de46-138">O sinalizador só deve ser usado para o Serviço de ApiManagement SKU de Consumo.</span><span class="sxs-lookup"><span data-stu-id="2de46-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="2de46-139">Isso impõe que um certificado de cliente seja apresentado em cada solicitação ao gateway.</span><span class="sxs-lookup"><span data-stu-id="2de46-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="2de46-140">Isso também permite autenticar o certificado na política no gateway.</span><span class="sxs-lookup"><span data-stu-id="2de46-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="2de46-141">-Local</span><span class="sxs-lookup"><span data-stu-id="2de46-141">-Location</span></span>
<span data-ttu-id="2de46-142">Especifica o local para criar o serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="2de46-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="2de46-143">Para obter locais válidos, use o cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | onde {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object locais</span><span class="sxs-lookup"><span data-stu-id="2de46-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="2de46-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="2de46-144">-Name</span></span>
<span data-ttu-id="2de46-145">Especifica um nome para a implantação de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2de46-145">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="2de46-146">-Organização</span><span class="sxs-lookup"><span data-stu-id="2de46-146">-Organization</span></span>
<span data-ttu-id="2de46-147">Especifica o nome de uma organização.</span><span class="sxs-lookup"><span data-stu-id="2de46-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="2de46-148">O Gerenciamento de API usa esse endereço no portal do desenvolvedor em notificações por email.</span><span class="sxs-lookup"><span data-stu-id="2de46-148">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="2de46-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de46-149">-ResourceGroupName</span></span>
<span data-ttu-id="2de46-150">Especifica o nome do grupo de recursos no qual esse cmdlet cria uma implantação de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2de46-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="2de46-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="2de46-151">-Sku</span></span>
<span data-ttu-id="2de46-152">Especifica o nível do serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="2de46-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="2de46-153">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="2de46-153">Valid values are:</span></span> 
- <span data-ttu-id="2de46-154">Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="2de46-154">Developer</span></span> 
- <span data-ttu-id="2de46-155">Padrão</span><span class="sxs-lookup"><span data-stu-id="2de46-155">Standard</span></span> 
- <span data-ttu-id="2de46-156">Premium O padrão é Desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="2de46-156">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de46-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="2de46-157">-SslSetting</span></span>
<span data-ttu-id="2de46-158">A Configuração SSL do Serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2de46-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="2de46-159">O valor padrão é $null</span><span class="sxs-lookup"><span data-stu-id="2de46-159">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de46-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2de46-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="2de46-161">Gere e atribua uma Identidade do Azure Active Directory para esse servidor para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2de46-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2de46-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2de46-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="2de46-163">Certificados emitidos pela CA interna para serem instalados no serviço.</span><span class="sxs-lookup"><span data-stu-id="2de46-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="2de46-164">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="2de46-164">Default value is $null.</span></span>

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

### <span data-ttu-id="2de46-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="2de46-165">-Tag</span></span>
<span data-ttu-id="2de46-166">Dicionário de marcas.</span><span class="sxs-lookup"><span data-stu-id="2de46-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="2de46-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2de46-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="2de46-168">Atribua identidades de usuário a este servidor para uso com os principais serviços de gerenciamento, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2de46-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de46-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2de46-169">-VirtualNetwork</span></span>
<span data-ttu-id="2de46-170">Configuração de Rede Virtual da região de implantação mestra do Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="2de46-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="2de46-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="2de46-171">-VpnType</span></span>
<span data-ttu-id="2de46-172">Tipo de Rede Virtual da Implantação apiManagement.</span><span class="sxs-lookup"><span data-stu-id="2de46-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="2de46-173">Valores Válidos são</span><span class="sxs-lookup"><span data-stu-id="2de46-173">Valid Values are</span></span> 
- <span data-ttu-id="2de46-174">"Nenhum" (Valor Padrão.</span><span class="sxs-lookup"><span data-stu-id="2de46-174">"None" (Default Value.</span></span> <span data-ttu-id="2de46-175">ApiManagement não faz parte de nenhuma Rede Virtual")</span><span class="sxs-lookup"><span data-stu-id="2de46-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="2de46-176">"Externo" (a Implantação apiManagement é configurada dentro de uma Rede Virtual com um Ponto de Extremidade Voltado para a Internet)</span><span class="sxs-lookup"><span data-stu-id="2de46-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="2de46-177">"Interno" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span><span class="sxs-lookup"><span data-stu-id="2de46-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="2de46-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de46-178">CommonParameters</span></span>
<span data-ttu-id="2de46-179">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de46-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de46-180">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2de46-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de46-181">Entradas</span><span class="sxs-lookup"><span data-stu-id="2de46-181">INPUTS</span></span>

### <span data-ttu-id="2de46-182">System.String</span><span class="sxs-lookup"><span data-stu-id="2de46-182">System.String</span></span>

### <span data-ttu-id="2de46-183">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0,0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2de46-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2de46-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2de46-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2de46-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2de46-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="2de46-186">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2de46-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2de46-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span><span class="sxs-lookup"><span data-stu-id="2de46-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="2de46-188">Microsoft.Azure.Commands.ApiManagement.Models.PsAPIManagementCustomHostNameConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="2de46-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="2de46-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span><span class="sxs-lookup"><span data-stu-id="2de46-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="2de46-190">Saídas</span><span class="sxs-lookup"><span data-stu-id="2de46-190">OUTPUTS</span></span>

### <span data-ttu-id="2de46-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2de46-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2de46-192">Notas</span><span class="sxs-lookup"><span data-stu-id="2de46-192">NOTES</span></span>

## <span data-ttu-id="2de46-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2de46-193">RELATED LINKS</span></span>

[<span data-ttu-id="2de46-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2de46-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="2de46-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2de46-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="2de46-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2de46-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="2de46-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2de46-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="2de46-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2de46-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


