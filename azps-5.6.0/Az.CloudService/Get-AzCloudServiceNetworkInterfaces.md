---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-AzCloudServiceNetworkInterfaces
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
ms.openlocfilehash: ae6bb602e90fd86334a28a804deed2be429347ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892665"
---
# <span data-ttu-id="18aab-101">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="18aab-101">Get-AzCloudServiceNetworkInterfaces</span></span>

## <span data-ttu-id="18aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18aab-102">SYNOPSIS</span></span>
<span data-ttu-id="18aab-103">Obter as interfaces de rede de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-103">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="18aab-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="18aab-104">SYNTAX</span></span>

### <span data-ttu-id="18aab-105">CloudServiceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18aab-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### <span data-ttu-id="18aab-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="18aab-106">CloudService</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## <span data-ttu-id="18aab-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="18aab-107">DESCRIPTION</span></span>
<span data-ttu-id="18aab-108">Obter as interfaces de rede de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-108">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="18aab-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18aab-109">EXAMPLES</span></span>

### <span data-ttu-id="18aab-110">Exemplo 1: Obter interfaces de rede por um nome de serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="18aab-110">Example 1: Get network interfaces by a cloud service name</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="18aab-111">Obtém todas as interfaces de rede para um determinado nome de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-111">Gets all the network interfaces for a given cloud service name.</span></span>

### <span data-ttu-id="18aab-112">Exemplo 2: Obter interfaces de rede por um objeto de serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="18aab-112">Example 2: Get network interfaces by a cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

<span data-ttu-id="18aab-113">Obtém todas as interfaces de rede de um determinado objeto de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-113">Gets all the network interfaces for a given cloud service object.</span></span>

### <span data-ttu-id="18aab-114">Exemplo 3: Obter interfaces de rede por um objeto de serviço de nuvem e nome de instância de função.</span><span class="sxs-lookup"><span data-stu-id="18aab-114">Example 3: Get network interfaces by a cloud service object and role instance name.</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

<span data-ttu-id="18aab-115">Obtém todas as interfaces de rede para um determinado objeto de serviço de nuvem e nome de instância de função.</span><span class="sxs-lookup"><span data-stu-id="18aab-115">Gets all the network interfaces for a given cloud service object and role instance name.</span></span>

## <span data-ttu-id="18aab-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="18aab-116">PARAMETERS</span></span>

### <span data-ttu-id="18aab-117">-CloudService</span><span class="sxs-lookup"><span data-stu-id="18aab-117">-CloudService</span></span>
<span data-ttu-id="18aab-118">Instância do CloudService.</span><span class="sxs-lookup"><span data-stu-id="18aab-118">CloudService instance.</span></span>
<span data-ttu-id="18aab-119">Para construir, consulte a seção NOTES para propriedades DO CLOUDSERVICE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="18aab-119">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18aab-120">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="18aab-120">-CloudServiceName</span></span>
<span data-ttu-id="18aab-121">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="18aab-121">CloudServiceName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18aab-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18aab-122">-ResourceGroupName</span></span>
<span data-ttu-id="18aab-123">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="18aab-123">ResourceGroupName.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18aab-124">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="18aab-124">-RoleInstanceName</span></span>
<span data-ttu-id="18aab-125">RoleInstanceName.</span><span class="sxs-lookup"><span data-stu-id="18aab-125">RoleInstanceName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18aab-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18aab-126">-SubscriptionId</span></span>
<span data-ttu-id="18aab-127">Assinatura.</span><span class="sxs-lookup"><span data-stu-id="18aab-127">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18aab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18aab-128">CommonParameters</span></span>
<span data-ttu-id="18aab-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18aab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18aab-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18aab-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18aab-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18aab-131">INPUTS</span></span>

## <span data-ttu-id="18aab-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="18aab-132">OUTPUTS</span></span>

## <span data-ttu-id="18aab-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="18aab-133">NOTES</span></span>

<span data-ttu-id="18aab-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="18aab-134">ALIASES</span></span>

<span data-ttu-id="18aab-135">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="18aab-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18aab-136">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="18aab-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18aab-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18aab-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18aab-138">CLOUDSERVICE <CloudService> : Instância do CloudService.</span><span class="sxs-lookup"><span data-stu-id="18aab-138">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="18aab-139">`Location <String>`: Localização do recurso.</span><span class="sxs-lookup"><span data-stu-id="18aab-139">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="18aab-140">`[Configuration <String>]`: Especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-140">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="18aab-141">`[ConfigurationUrl <String>]`: Especifica uma URL que se refere ao local da configuração do serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="18aab-141">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="18aab-142">A URL do pacote de serviço pode ser URI de Assinatura de Acesso Compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="18aab-142">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="18aab-143">Esta é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="18aab-143">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="18aab-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Descreve um perfil de extensão do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="18aab-145">`[Extension <IExtension[]>]`: Lista de extensões para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-145">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="18aab-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Especifique explicitamente se a plataforma pode atualizar automaticamente typeHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="18aab-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="18aab-147">`[ForceUpdateTag <String>]`: Marca para forçar a aplicação das configurações públicas e protegidas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="18aab-147">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="18aab-148">Alterar o valor da marca permite executar a extensão sem alterar nenhuma das configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="18aab-148">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="18aab-149">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="18aab-149">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="18aab-150">Se nem forceUpdateTag nem nenhuma das configurações públicas ou protegidas mudarem, a extensão fluirá para a instância de função com o mesmo número de sequência e a implementação do manipulador decidirá se a executará ou não.</span><span class="sxs-lookup"><span data-stu-id="18aab-150">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="18aab-151">`[Name <String>]`: O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="18aab-151">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="18aab-152">`[ProtectedSetting <String>]`: Configurações protegidas para a extensão que são criptografadas antes de enviadas para a instância de função.</span><span class="sxs-lookup"><span data-stu-id="18aab-152">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="18aab-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="18aab-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="18aab-154">`[Publisher <String>]`: O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="18aab-154">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="18aab-155">`[RolesAppliedTo <String[]>]`: Lista opcional de funções para aplicar essa extensão.</span><span class="sxs-lookup"><span data-stu-id="18aab-155">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="18aab-156">Se a propriedade não for especificada ou '\*' for especificada, a extensão será aplicada a todas as funções no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-156">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="18aab-157">`[Setting <String>]`: Configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="18aab-157">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="18aab-158">Para extensões JSON, essas são as configurações JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="18aab-158">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="18aab-159">Para Extensão XML (como RDP), esta é a configuração XML da extensão.</span><span class="sxs-lookup"><span data-stu-id="18aab-159">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="18aab-160">`[SourceVaultId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="18aab-160">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="18aab-161">`[Type <String>]`: Especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="18aab-161">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="18aab-162">`[TypeHandlerVersion <String>]`: Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="18aab-162">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="18aab-163">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="18aab-163">Specifies the version of the extension.</span></span> <span data-ttu-id="18aab-164">Se esse elemento não for especificado ou um asterisco (\*) for usado como o valor, a versão mais recente da extensão será usada.</span><span class="sxs-lookup"><span data-stu-id="18aab-164">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="18aab-165">Se o valor for especificado com um número de versão principal e um asterisco como o número de versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada.</span><span class="sxs-lookup"><span data-stu-id="18aab-165">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="18aab-166">Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada.</span><span class="sxs-lookup"><span data-stu-id="18aab-166">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="18aab-167">Se uma versão for especificada, uma atualização automática será realizada na instância de função.</span><span class="sxs-lookup"><span data-stu-id="18aab-167">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="18aab-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Perfil de rede para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="18aab-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: A lista de configurações do balanceador de carga para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="18aab-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP</span><span class="sxs-lookup"><span data-stu-id="18aab-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="18aab-171">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="18aab-171">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="18aab-172">`[PrivateIPAddress <String>]`: O endereço IP privado referenciado pelo serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-172">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="18aab-173">`[PublicIPAddressId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="18aab-173">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="18aab-174">`[SubnetId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="18aab-174">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="18aab-175">`[Name <String>]`: Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="18aab-175">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="18aab-176">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="18aab-176">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="18aab-177">`[Id <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="18aab-177">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="18aab-178">`[OSProfile <ICloudServiceOSProfile>]`: Descreve o perfil do sistema operacional para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-178">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="18aab-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Especifica o conjunto de certificados que devem ser instalados nas instâncias de função.</span><span class="sxs-lookup"><span data-stu-id="18aab-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="18aab-180">`[SourceVaultId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="18aab-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="18aab-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências do cofre de chaves em SourceVault que contêm certificados.</span><span class="sxs-lookup"><span data-stu-id="18aab-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="18aab-182">`[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado no Cofre de Chaves como um segredo.</span><span class="sxs-lookup"><span data-stu-id="18aab-182">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="18aab-183">`[PackageUrl <String>]`: Especifica uma URL que se refere ao local do pacote de serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="18aab-183">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="18aab-184">A URL do pacote de serviço pode ser URI de Assinatura de Acesso Compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="18aab-184">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="18aab-185">Esta é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="18aab-185">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="18aab-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Descreve o perfil de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="18aab-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="18aab-188">`[Name <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="18aab-188">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="18aab-189">`[SkuCapacity <Int64?>]`: Especifica o número de instâncias de função no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-189">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="18aab-190">`[SkuName <String>]`: O nome sku.</span><span class="sxs-lookup"><span data-stu-id="18aab-190">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="18aab-191">OBSERVAÇÃO: se o novo SKU não tiver suporte no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para o sku antigo.</span><span class="sxs-lookup"><span data-stu-id="18aab-191">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="18aab-192">`[SkuTier <String>]`: Especifica a camada do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-192">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="18aab-193">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="18aab-193">Possible Values are</span></span> <br /><br /> <span data-ttu-id="18aab-194">**Standard**</span><span class="sxs-lookup"><span data-stu-id="18aab-194">**Standard**</span></span> <br /><br /> <span data-ttu-id="18aab-195">**Básico**</span><span class="sxs-lookup"><span data-stu-id="18aab-195">**Basic**</span></span>
  - <span data-ttu-id="18aab-196">`[StartCloudService <Boolean?>]`: (Opcional) Indica se deve iniciar o serviço de nuvem imediatamente após a criação.</span><span class="sxs-lookup"><span data-stu-id="18aab-196">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="18aab-197">O valor padrão é `true` .</span><span class="sxs-lookup"><span data-stu-id="18aab-197">The default value is `true`.</span></span>         <span data-ttu-id="18aab-198">Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="18aab-198">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="18aab-199">Em vez disso, o serviço é PoweredOff até que você chame Start, momento em que o serviço será iniciado.</span><span class="sxs-lookup"><span data-stu-id="18aab-199">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="18aab-200">Um serviço implantado ainda incorre em encargos, mesmo que seja desligado.</span><span class="sxs-lookup"><span data-stu-id="18aab-200">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="18aab-201">`[Tag <ICloudServiceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="18aab-201">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="18aab-202">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="18aab-202">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="18aab-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Modo de atualização para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="18aab-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="18aab-204">As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado.</span><span class="sxs-lookup"><span data-stu-id="18aab-204">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="18aab-205">As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização.</span><span class="sxs-lookup"><span data-stu-id="18aab-205">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="18aab-206">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="18aab-206">Possible Values are</span></span> <br /><br /><span data-ttu-id="18aab-207">**Automático**</span><span class="sxs-lookup"><span data-stu-id="18aab-207">**Auto**</span></span><br /><br /><span data-ttu-id="18aab-208">**Manual**</span><span class="sxs-lookup"><span data-stu-id="18aab-208">**Manual**</span></span> <br /><br /><span data-ttu-id="18aab-209">**Simultâneo**</span><span class="sxs-lookup"><span data-stu-id="18aab-209">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="18aab-210">Se não for especificado, o valor padrão será Auto. Se definido como Manual, PUT UpdateDomain deve ser chamado para aplicar a atualização.</span><span class="sxs-lookup"><span data-stu-id="18aab-210">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="18aab-211">Se definido como Auto, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.</span><span class="sxs-lookup"><span data-stu-id="18aab-211">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="18aab-212">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18aab-212">RELATED LINKS</span></span>

