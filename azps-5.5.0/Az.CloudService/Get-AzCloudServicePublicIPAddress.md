---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: 2a3b643a9ad9d9c588589003e5edb24ceddc4ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112168"
---
# <span data-ttu-id="2de3e-101">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="2de3e-101">Get-AzCloudServicePublicIPAddress</span></span>

## <span data-ttu-id="2de3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2de3e-102">SYNOPSIS</span></span>
<span data-ttu-id="2de3e-103">Obter o endereço IP público de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-103">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="2de3e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2de3e-104">SYNTAX</span></span>

### <span data-ttu-id="2de3e-105">CloudServiceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2de3e-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### <span data-ttu-id="2de3e-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="2de3e-106">CloudService</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="2de3e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2de3e-107">DESCRIPTION</span></span>
<span data-ttu-id="2de3e-108">Obter o endereço IP público de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-108">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="2de3e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2de3e-109">EXAMPLES</span></span>

### <span data-ttu-id="2de3e-110">Exemplo 1: Obter endereços IP públicos de nível de instância para um determinado nome de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-110">Example 1: Get instance level public IP addresses for a given cloud service name.</span></span>
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="2de3e-111">Obtém o nível de instância de endereços IP públicos para um determinado nome de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-111">Gets the instance level public IP addresses for a given cloud service name.</span></span>

### <span data-ttu-id="2de3e-112">Exemplo 2: Obter endereços IP públicos de nível de instância para um determinado objeto de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-112">Example 2: Get instance level public IP addresses for a given cloud service object.</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

<span data-ttu-id="2de3e-113">Obtém o nível de instância de endereços IP públicos para um determinado objeto de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-113">Gets the instance level public IP addresses for a given cloud service object.</span></span>

## <span data-ttu-id="2de3e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2de3e-114">PARAMETERS</span></span>

### <span data-ttu-id="2de3e-115">-CloudService</span><span class="sxs-lookup"><span data-stu-id="2de3e-115">-CloudService</span></span>
<span data-ttu-id="2de3e-116">Instância do CloudService.</span><span class="sxs-lookup"><span data-stu-id="2de3e-116">CloudService instance.</span></span>
<span data-ttu-id="2de3e-117">Para construir, confira a seção ANOTAÇÕES para propriedades DE SERVIÇO NA NUVEM e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="2de3e-117">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="2de3e-118">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="2de3e-118">-CloudServiceName</span></span>
<span data-ttu-id="2de3e-119">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="2de3e-119">CloudServiceName.</span></span>

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

### <span data-ttu-id="2de3e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de3e-120">-ResourceGroupName</span></span>
<span data-ttu-id="2de3e-121">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2de3e-121">ResourceGroupName.</span></span>

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

### <span data-ttu-id="2de3e-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2de3e-122">-SubscriptionId</span></span>
<span data-ttu-id="2de3e-123">Assinatura.</span><span class="sxs-lookup"><span data-stu-id="2de3e-123">Subscription.</span></span>

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

### <span data-ttu-id="2de3e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de3e-124">CommonParameters</span></span>
<span data-ttu-id="2de3e-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de3e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de3e-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2de3e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de3e-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="2de3e-127">INPUTS</span></span>

## <span data-ttu-id="2de3e-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="2de3e-128">OUTPUTS</span></span>

## <span data-ttu-id="2de3e-129">Notas</span><span class="sxs-lookup"><span data-stu-id="2de3e-129">NOTES</span></span>

<span data-ttu-id="2de3e-130">Aliases</span><span class="sxs-lookup"><span data-stu-id="2de3e-130">ALIASES</span></span>

<span data-ttu-id="2de3e-131">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="2de3e-131">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2de3e-132">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2de3e-132">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2de3e-133">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2de3e-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2de3e-134"><CloudService>CLOUDSERVICE: instância de CloudService.</span><span class="sxs-lookup"><span data-stu-id="2de3e-134">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="2de3e-135">`Location <String>`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2de3e-135">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="2de3e-136">`[Configuration <String>]`: especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-136">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="2de3e-137">`[ConfigurationUrl <String>]`: especifica uma URL que se refere ao local da configuração do serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="2de3e-137">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="2de3e-138">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2de3e-138">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="2de3e-139">Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="2de3e-139">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="2de3e-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: descreve um perfil de extensão de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="2de3e-141">`[Extension <IExtension[]>]`: Lista de extensões do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-141">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="2de3e-142">`[AutoUpgradeMinorVersion <Boolean?>]`: especifique explicitamente se a plataforma pode atualizar automaticamente o tipoHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2de3e-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="2de3e-143">`[ForceUpdateTag <String>]`: Marque para forçar a aplicação das configurações públicas e protegidas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="2de3e-143">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="2de3e-144">Alterar o valor da marca permite executar a extensão de forma a executar a extensão sem alterar as configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="2de3e-144">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="2de3e-145">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="2de3e-145">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="2de3e-146">Se nem forçarUpdateTag nem nenhuma das configurações públicas ou protegidas mudar, a extensão fluiria para a instância de função com o mesmo número de sequência, e a implementação de manipuladores decidirá se a executará ou não.</span><span class="sxs-lookup"><span data-stu-id="2de3e-146">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="2de3e-147">`[Name <String>]`: o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="2de3e-147">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="2de3e-148">`[ProtectedSetting <String>]`: Configurações protegidas para a extensão que são criptografadas antes de enviar para a instância de função.</span><span class="sxs-lookup"><span data-stu-id="2de3e-148">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="2de3e-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2de3e-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="2de3e-150">`[Publisher <String>]`: o nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="2de3e-150">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="2de3e-151">`[RolesAppliedTo <String[]>]`: Lista opcional de funções para aplicar essa extensão.</span><span class="sxs-lookup"><span data-stu-id="2de3e-151">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="2de3e-152">Se a propriedade não for especificada ou '\*' for especificada, a extensão será aplicada a todas as funções no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-152">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="2de3e-153">`[Setting <String>]`: Configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="2de3e-153">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="2de3e-154">Para extensões JSON, essas são as configurações JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="2de3e-154">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="2de3e-155">Para Extensão XML (como RDP), essa é a configuração XML para a extensão.</span><span class="sxs-lookup"><span data-stu-id="2de3e-155">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="2de3e-156">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="2de3e-156">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="2de3e-157">`[Type <String>]`: especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="2de3e-157">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="2de3e-158">`[TypeHandlerVersion <String>]`: especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="2de3e-158">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="2de3e-159">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="2de3e-159">Specifies the version of the extension.</span></span> <span data-ttu-id="2de3e-160">Se esse elemento não for especificado ou um asterisco (\*) for usado como valor, a versão mais recente da extensão será usada.</span><span class="sxs-lookup"><span data-stu-id="2de3e-160">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="2de3e-161">Se o valor for especificado com um número de versão principal e um asterisco como o número da versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada.</span><span class="sxs-lookup"><span data-stu-id="2de3e-161">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="2de3e-162">Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada.</span><span class="sxs-lookup"><span data-stu-id="2de3e-162">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="2de3e-163">Se uma versão for especificada, uma atualização automática será executada na instância da função.</span><span class="sxs-lookup"><span data-stu-id="2de3e-163">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="2de3e-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Perfil de Rede do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="2de3e-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: a lista de configurações de balanceador de carga para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="2de3e-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP</span><span class="sxs-lookup"><span data-stu-id="2de3e-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="2de3e-167">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2de3e-167">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="2de3e-168">`[PrivateIPAddress <String>]`: O endereço IP particular referenciado pelo serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-168">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="2de3e-169">`[PublicIPAddressId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="2de3e-169">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="2de3e-170">`[SubnetId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="2de3e-170">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="2de3e-171">`[Name <String>]`: Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="2de3e-171">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="2de3e-172">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="2de3e-172">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="2de3e-173">`[Id <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="2de3e-173">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="2de3e-174">`[OSProfile <ICloudServiceOSProfile>]`: descreve o perfil do sistema operacional para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-174">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="2de3e-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: especifica o conjunto de certificados que devem ser instalados nas instâncias de função.</span><span class="sxs-lookup"><span data-stu-id="2de3e-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="2de3e-176">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="2de3e-176">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="2de3e-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências do cofre-chave no SourceVault que contêm certificados.</span><span class="sxs-lookup"><span data-stu-id="2de3e-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="2de3e-178">`[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado para o Cofre de Chaves como um segredo.</span><span class="sxs-lookup"><span data-stu-id="2de3e-178">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="2de3e-179">`[PackageUrl <String>]`: especifica uma URL que se refere ao local do pacote de serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="2de3e-179">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="2de3e-180">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2de3e-180">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="2de3e-181">Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="2de3e-181">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="2de3e-182">`[RoleProfile <ICloudServiceRoleProfile>]`: descreve o perfil de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="2de3e-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="2de3e-184">`[Name <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2de3e-184">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="2de3e-185">`[SkuCapacity <Int64?>]`: especifica o número de instâncias de função no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-185">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="2de3e-186">`[SkuName <String>]`: o nome da sKU.</span><span class="sxs-lookup"><span data-stu-id="2de3e-186">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="2de3e-187">OBSERVAÇÃO: se a nova SKU não for suportada no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para a SKU antiga.</span><span class="sxs-lookup"><span data-stu-id="2de3e-187">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="2de3e-188">`[SkuTier <String>]`: especifica o nível do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-188">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="2de3e-189">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="2de3e-189">Possible Values are</span></span> <br /><br /> <span data-ttu-id="2de3e-190">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="2de3e-190">**Standard**</span></span> <br /><br /> <span data-ttu-id="2de3e-191">**Basic**</span><span class="sxs-lookup"><span data-stu-id="2de3e-191">**Basic**</span></span>
  - <span data-ttu-id="2de3e-192">`[StartCloudService <Boolean?>]`: (Opcional) Indica se o serviço de nuvem deve ser iniciar imediatamente após sua criação.</span><span class="sxs-lookup"><span data-stu-id="2de3e-192">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="2de3e-193">O valor padrão é `true` .</span><span class="sxs-lookup"><span data-stu-id="2de3e-193">The default value is `true`.</span></span>         <span data-ttu-id="2de3e-194">Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="2de3e-194">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="2de3e-195">Em vez disso, o serviço é PoweredOff até que você ligue para Iniciar, momento em que o serviço será iniciado.</span><span class="sxs-lookup"><span data-stu-id="2de3e-195">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="2de3e-196">Um serviço implantado ainda incorre em encargos, mesmo que ele esteja desligado.</span><span class="sxs-lookup"><span data-stu-id="2de3e-196">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="2de3e-197">`[Tag <ICloudServiceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="2de3e-197">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="2de3e-198">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="2de3e-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2de3e-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Modo de atualização para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="2de3e-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="2de3e-200">As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado.</span><span class="sxs-lookup"><span data-stu-id="2de3e-200">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="2de3e-201">As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização.</span><span class="sxs-lookup"><span data-stu-id="2de3e-201">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="2de3e-202">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="2de3e-202">Possible Values are</span></span> <br /><br /><span data-ttu-id="2de3e-203">**Automático**</span><span class="sxs-lookup"><span data-stu-id="2de3e-203">**Auto**</span></span><br /><br /><span data-ttu-id="2de3e-204">**Manual**</span><span class="sxs-lookup"><span data-stu-id="2de3e-204">**Manual**</span></span> <br /><br /><span data-ttu-id="2de3e-205">**Simultânea**</span><span class="sxs-lookup"><span data-stu-id="2de3e-205">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="2de3e-206">Se não especificado, o valor padrão será Automático. Se definido como Manual, PUT UpdateDomain deverá ser chamado para aplicar a atualização.</span><span class="sxs-lookup"><span data-stu-id="2de3e-206">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="2de3e-207">Se definido como Automático, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.</span><span class="sxs-lookup"><span data-stu-id="2de3e-207">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="2de3e-208">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2de3e-208">RELATED LINKS</span></span>

