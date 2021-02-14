---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServiceNetworkInterfaces
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
ms.openlocfilehash: 7f8a51c518bd034e51d8c25d5029bb57b3e38caf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115964"
---
# <span data-ttu-id="bc258-101">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="bc258-101">Get-AzCloudServiceNetworkInterfaces</span></span>

## <span data-ttu-id="bc258-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc258-102">SYNOPSIS</span></span>
<span data-ttu-id="bc258-103">Obter as interfaces de rede de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-103">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="bc258-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc258-104">SYNTAX</span></span>

### <span data-ttu-id="bc258-105">CloudServiceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bc258-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bc258-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="bc258-106">CloudService</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## <span data-ttu-id="bc258-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc258-107">DESCRIPTION</span></span>
<span data-ttu-id="bc258-108">Obter as interfaces de rede de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-108">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="bc258-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc258-109">EXAMPLES</span></span>

### <span data-ttu-id="bc258-110">Exemplo 1: Obter interfaces de rede por um nome de serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="bc258-110">Example 1: Get network interfaces by a cloud service name</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="bc258-111">Obtém todas as interfaces de rede para um determinado nome de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-111">Gets all the network interfaces for a given cloud service name.</span></span>

### <span data-ttu-id="bc258-112">Exemplo 2: Obter interfaces de rede por um objeto de serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="bc258-112">Example 2: Get network interfaces by a cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

<span data-ttu-id="bc258-113">Obtém todas as interfaces de rede para um determinado objeto de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-113">Gets all the network interfaces for a given cloud service object.</span></span>

### <span data-ttu-id="bc258-114">Exemplo 3: Obter interfaces de rede por um objeto de serviço de nuvem e nome de instância de função.</span><span class="sxs-lookup"><span data-stu-id="bc258-114">Example 3: Get network interfaces by a cloud service object and role instance name.</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

<span data-ttu-id="bc258-115">Obtém todas as interfaces de rede para um determinado objeto de serviço de nuvem e nome de instância de função.</span><span class="sxs-lookup"><span data-stu-id="bc258-115">Gets all the network interfaces for a given cloud service object and role instance name.</span></span>

## <span data-ttu-id="bc258-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc258-116">PARAMETERS</span></span>

### <span data-ttu-id="bc258-117">-CloudService</span><span class="sxs-lookup"><span data-stu-id="bc258-117">-CloudService</span></span>
<span data-ttu-id="bc258-118">Instância do CloudService.</span><span class="sxs-lookup"><span data-stu-id="bc258-118">CloudService instance.</span></span>
<span data-ttu-id="bc258-119">Para construir, confira a seção ANOTAÇÕES para propriedades DE SERVIÇO NA NUVEM e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="bc258-119">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc258-120">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="bc258-120">-CloudServiceName</span></span>
<span data-ttu-id="bc258-121">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="bc258-121">CloudServiceName.</span></span>

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

### <span data-ttu-id="bc258-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc258-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc258-123">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="bc258-123">ResourceGroupName.</span></span>

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

### <span data-ttu-id="bc258-124">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="bc258-124">-RoleInstanceName</span></span>
<span data-ttu-id="bc258-125">RoleInstanceName.</span><span class="sxs-lookup"><span data-stu-id="bc258-125">RoleInstanceName.</span></span>

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

### <span data-ttu-id="bc258-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc258-126">-SubscriptionId</span></span>
<span data-ttu-id="bc258-127">Assinatura.</span><span class="sxs-lookup"><span data-stu-id="bc258-127">Subscription.</span></span>

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

### <span data-ttu-id="bc258-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc258-128">CommonParameters</span></span>
<span data-ttu-id="bc258-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc258-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc258-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc258-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc258-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="bc258-131">INPUTS</span></span>

## <span data-ttu-id="bc258-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="bc258-132">OUTPUTS</span></span>

## <span data-ttu-id="bc258-133">Notas</span><span class="sxs-lookup"><span data-stu-id="bc258-133">NOTES</span></span>

<span data-ttu-id="bc258-134">Aliases</span><span class="sxs-lookup"><span data-stu-id="bc258-134">ALIASES</span></span>

<span data-ttu-id="bc258-135">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="bc258-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc258-136">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="bc258-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc258-137">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc258-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc258-138"><CloudService>CLOUDSERVICE: instância de CloudService.</span><span class="sxs-lookup"><span data-stu-id="bc258-138">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="bc258-139">`Location <String>`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc258-139">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="bc258-140">`[Configuration <String>]`: especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-140">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="bc258-141">`[ConfigurationUrl <String>]`: especifica uma URL que se refere ao local da configuração do serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="bc258-141">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="bc258-142">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bc258-142">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="bc258-143">Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="bc258-143">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="bc258-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: descreve um perfil de extensão de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="bc258-145">`[Extension <IExtension[]>]`: Lista de extensões do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-145">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="bc258-146">`[AutoUpgradeMinorVersion <Boolean?>]`: especifique explicitamente se a plataforma pode atualizar automaticamente o tipoHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bc258-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="bc258-147">`[ForceUpdateTag <String>]`: Marque para forçar a aplicação das configurações públicas e protegidas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="bc258-147">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="bc258-148">Alterar o valor da marca permite executar a extensão de forma a executar a extensão sem alterar as configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="bc258-148">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="bc258-149">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="bc258-149">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="bc258-150">Se nem forçarUpdateTag nem nenhuma das configurações públicas ou protegidas mudar, a extensão fluiria para a instância de função com o mesmo número de sequência, e a implementação de manipuladores decidirá se a executará ou não.</span><span class="sxs-lookup"><span data-stu-id="bc258-150">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="bc258-151">`[Name <String>]`: o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="bc258-151">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="bc258-152">`[ProtectedSetting <String>]`: Configurações protegidas para a extensão que são criptografadas antes de enviar para a instância de função.</span><span class="sxs-lookup"><span data-stu-id="bc258-152">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="bc258-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="bc258-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="bc258-154">`[Publisher <String>]`: o nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="bc258-154">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="bc258-155">`[RolesAppliedTo <String[]>]`: Lista opcional de funções para aplicar essa extensão.</span><span class="sxs-lookup"><span data-stu-id="bc258-155">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="bc258-156">Se a propriedade não for especificada ou '\*' for especificada, a extensão será aplicada a todas as funções no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-156">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="bc258-157">`[Setting <String>]`: Configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="bc258-157">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="bc258-158">Para extensões JSON, essas são as configurações JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="bc258-158">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="bc258-159">Para Extensão XML (como RDP), essa é a configuração XML para a extensão.</span><span class="sxs-lookup"><span data-stu-id="bc258-159">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="bc258-160">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="bc258-160">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="bc258-161">`[Type <String>]`: especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="bc258-161">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="bc258-162">`[TypeHandlerVersion <String>]`: especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="bc258-162">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="bc258-163">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="bc258-163">Specifies the version of the extension.</span></span> <span data-ttu-id="bc258-164">Se esse elemento não for especificado ou um asterisco (\*) for usado como valor, a versão mais recente da extensão será usada.</span><span class="sxs-lookup"><span data-stu-id="bc258-164">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="bc258-165">Se o valor for especificado com um número de versão principal e um asterisco como o número da versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada.</span><span class="sxs-lookup"><span data-stu-id="bc258-165">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="bc258-166">Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada.</span><span class="sxs-lookup"><span data-stu-id="bc258-166">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="bc258-167">Se uma versão for especificada, uma atualização automática será executada na instância da função.</span><span class="sxs-lookup"><span data-stu-id="bc258-167">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="bc258-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Perfil de Rede do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="bc258-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: a lista de configurações de balanceador de carga para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="bc258-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP</span><span class="sxs-lookup"><span data-stu-id="bc258-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="bc258-171">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="bc258-171">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="bc258-172">`[PrivateIPAddress <String>]`: O endereço IP particular referenciado pelo serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-172">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="bc258-173">`[PublicIPAddressId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="bc258-173">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="bc258-174">`[SubnetId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="bc258-174">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="bc258-175">`[Name <String>]`: Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="bc258-175">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="bc258-176">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="bc258-176">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="bc258-177">`[Id <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="bc258-177">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="bc258-178">`[OSProfile <ICloudServiceOSProfile>]`: descreve o perfil do sistema operacional para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-178">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="bc258-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: especifica o conjunto de certificados que devem ser instalados nas instâncias de função.</span><span class="sxs-lookup"><span data-stu-id="bc258-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="bc258-180">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="bc258-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="bc258-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências do cofre-chave no SourceVault que contêm certificados.</span><span class="sxs-lookup"><span data-stu-id="bc258-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="bc258-182">`[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado para o Cofre de Chaves como um segredo.</span><span class="sxs-lookup"><span data-stu-id="bc258-182">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="bc258-183">`[PackageUrl <String>]`: especifica uma URL que se refere ao local do pacote de serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="bc258-183">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="bc258-184">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bc258-184">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="bc258-185">Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="bc258-185">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="bc258-186">`[RoleProfile <ICloudServiceRoleProfile>]`: descreve o perfil de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="bc258-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="bc258-188">`[Name <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc258-188">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="bc258-189">`[SkuCapacity <Int64?>]`: especifica o número de instâncias de função no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-189">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="bc258-190">`[SkuName <String>]`: o nome da sKU.</span><span class="sxs-lookup"><span data-stu-id="bc258-190">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="bc258-191">OBSERVAÇÃO: se a nova SKU não for suportada no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para a SKU antiga.</span><span class="sxs-lookup"><span data-stu-id="bc258-191">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="bc258-192">`[SkuTier <String>]`: especifica o nível do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-192">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="bc258-193">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="bc258-193">Possible Values are</span></span> <br /><br /> <span data-ttu-id="bc258-194">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="bc258-194">**Standard**</span></span> <br /><br /> <span data-ttu-id="bc258-195">**Basic**</span><span class="sxs-lookup"><span data-stu-id="bc258-195">**Basic**</span></span>
  - <span data-ttu-id="bc258-196">`[StartCloudService <Boolean?>]`: (Opcional) Indica se o serviço de nuvem deve ser iniciar imediatamente após sua criação.</span><span class="sxs-lookup"><span data-stu-id="bc258-196">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="bc258-197">O valor padrão é `true` .</span><span class="sxs-lookup"><span data-stu-id="bc258-197">The default value is `true`.</span></span>         <span data-ttu-id="bc258-198">Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="bc258-198">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="bc258-199">Em vez disso, o serviço é PoweredOff até que você ligue para Iniciar, momento em que o serviço será iniciado.</span><span class="sxs-lookup"><span data-stu-id="bc258-199">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="bc258-200">Um serviço implantado ainda incorre em encargos, mesmo que ele esteja desligado.</span><span class="sxs-lookup"><span data-stu-id="bc258-200">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="bc258-201">`[Tag <ICloudServiceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="bc258-201">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="bc258-202">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="bc258-202">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bc258-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Modo de atualização para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="bc258-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="bc258-204">As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado.</span><span class="sxs-lookup"><span data-stu-id="bc258-204">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="bc258-205">As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização.</span><span class="sxs-lookup"><span data-stu-id="bc258-205">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="bc258-206">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="bc258-206">Possible Values are</span></span> <br /><br /><span data-ttu-id="bc258-207">**Automático**</span><span class="sxs-lookup"><span data-stu-id="bc258-207">**Auto**</span></span><br /><br /><span data-ttu-id="bc258-208">**Manual**</span><span class="sxs-lookup"><span data-stu-id="bc258-208">**Manual**</span></span> <br /><br /><span data-ttu-id="bc258-209">**Simultânea**</span><span class="sxs-lookup"><span data-stu-id="bc258-209">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="bc258-210">Se não especificado, o valor padrão será Automático. Se definido como Manual, PUT UpdateDomain deverá ser chamado para aplicar a atualização.</span><span class="sxs-lookup"><span data-stu-id="bc258-210">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="bc258-211">Se definido como Automático, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.</span><span class="sxs-lookup"><span data-stu-id="bc258-211">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="bc258-212">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc258-212">RELATED LINKS</span></span>

