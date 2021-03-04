---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 607ac4e9854f3871c4a9a0f2859c6f1fe555f392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889311"
---
# <span data-ttu-id="47ff7-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="47ff7-101">New-AzCloudService</span></span>

## <span data-ttu-id="47ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="47ff7-103">Criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-103">Create or update a cloud service.</span></span>
<span data-ttu-id="47ff7-104">Observe que algumas propriedades só podem ser definidas durante a criação do serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="47ff7-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="47ff7-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="47ff7-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="47ff7-106">DESCRIPTION</span></span>
<span data-ttu-id="47ff7-107">Criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-107">Create or update a cloud service.</span></span>
<span data-ttu-id="47ff7-108">Observe que algumas propriedades só podem ser definidas durante a criação do serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="47ff7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47ff7-109">EXAMPLES</span></span>

### <span data-ttu-id="47ff7-110">Exemplo 1: Criar novo serviço de nuvem com função única</span><span class="sxs-lookup"><span data-stu-id="47ff7-110">Example 1: Create new cloud service with single role</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

<span data-ttu-id="47ff7-111">Acima do conjunto de comandos cria um serviço de nuvem com função única</span><span class="sxs-lookup"><span data-stu-id="47ff7-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="47ff7-112">Exemplo 2: Criar novo serviço de nuvem com uma única função e extensão RDP</span><span class="sxs-lookup"><span data-stu-id="47ff7-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

<span data-ttu-id="47ff7-113">Acima, o conjunto de comandos cria um serviço de nuvem com uma única função e extensão RDP</span><span class="sxs-lookup"><span data-stu-id="47ff7-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="47ff7-114">Exemplo 3: Criar novo serviço de nuvem com função única e certificado do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="47ff7-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

<span data-ttu-id="47ff7-115">O conjunto de comandos acima cria um serviço de nuvem com função única e certificado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="47ff7-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="47ff7-116">Exemplo 4: Criar novo serviço de nuvem com várias funções e extensões</span><span class="sxs-lookup"><span data-stu-id="47ff7-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

<span data-ttu-id="47ff7-117">O conjunto de comandos acima cria um serviço de nuvem com função única e certificado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="47ff7-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="47ff7-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="47ff7-118">PARAMETERS</span></span>

### <span data-ttu-id="47ff7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47ff7-119">-AsJob</span></span>
<span data-ttu-id="47ff7-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="47ff7-120">Run the command as a job</span></span>

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

### <span data-ttu-id="47ff7-121">-Configuration</span><span class="sxs-lookup"><span data-stu-id="47ff7-121">-Configuration</span></span>
<span data-ttu-id="47ff7-122">Especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

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

### <span data-ttu-id="47ff7-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="47ff7-123">-ConfigurationUrl</span></span>
<span data-ttu-id="47ff7-124">Especifica uma URL que se refere ao local da configuração do serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="47ff7-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="47ff7-125">A URL do pacote de serviço pode ser URI de Assinatura de Acesso Compartilhado (SAS) de qualquer conta de armazenamento. Esta é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="47ff7-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="47ff7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ff7-126">-DefaultProfile</span></span>
<span data-ttu-id="47ff7-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47ff7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="47ff7-128">-ExtensionProfile</span></span>
<span data-ttu-id="47ff7-129">Descreve um perfil de extensão do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="47ff7-130">Para construir, consulte a seção NOTES para propriedades EXTENSIONPROFILE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="47ff7-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-131">-Location</span><span class="sxs-lookup"><span data-stu-id="47ff7-131">-Location</span></span>
<span data-ttu-id="47ff7-132">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="47ff7-132">Resource location.</span></span>

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

### <span data-ttu-id="47ff7-133">-Name</span><span class="sxs-lookup"><span data-stu-id="47ff7-133">-Name</span></span>
<span data-ttu-id="47ff7-134">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-134">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47ff7-135">-NetworkProfile</span></span>
<span data-ttu-id="47ff7-136">Perfil de rede para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="47ff7-137">Para construir, consulte a seção NOTES para propriedades NETWORKPROFILE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="47ff7-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="47ff7-138">-NoWait</span></span>
<span data-ttu-id="47ff7-139">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="47ff7-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="47ff7-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="47ff7-140">-OSProfile</span></span>
<span data-ttu-id="47ff7-141">Descreve o perfil do sistema operacional para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="47ff7-142">Para construir, consulte a seção NOTES para propriedades OSPROFILE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="47ff7-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="47ff7-143">-PackageUrl</span></span>
<span data-ttu-id="47ff7-144">Especifica uma URL que se refere ao local do pacote de serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="47ff7-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="47ff7-145">A URL do pacote de serviço pode ser URI de Assinatura de Acesso Compartilhado (SAS) de qualquer conta de armazenamento. Esta é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="47ff7-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="47ff7-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47ff7-146">-ResourceGroupName</span></span>
<span data-ttu-id="47ff7-147">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="47ff7-147">Name of the resource group.</span></span>

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

### <span data-ttu-id="47ff7-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="47ff7-148">-RoleProfile</span></span>
<span data-ttu-id="47ff7-149">Descreve o perfil de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="47ff7-150">Para construir, consulte a seção NOTES para propriedades ROLEPROFILE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="47ff7-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="47ff7-151">-StartCloudService</span></span>
<span data-ttu-id="47ff7-152">(Opcional) Indica se deve iniciar o serviço de nuvem imediatamente após a criação.</span><span class="sxs-lookup"><span data-stu-id="47ff7-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="47ff7-153">O valor padrão é `true` . Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="47ff7-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="47ff7-154">Em vez disso, o serviço é PoweredOff até que você chame Start, momento em que o serviço será iniciado.</span><span class="sxs-lookup"><span data-stu-id="47ff7-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="47ff7-155">Um serviço implantado ainda incorre em encargos, mesmo que seja desligado.</span><span class="sxs-lookup"><span data-stu-id="47ff7-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

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

### <span data-ttu-id="47ff7-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47ff7-156">-SubscriptionId</span></span>
<span data-ttu-id="47ff7-157">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47ff7-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="47ff7-158">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="47ff7-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47ff7-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="47ff7-159">-Tag</span></span>
<span data-ttu-id="47ff7-160">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="47ff7-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="47ff7-161">-UpgradeMode</span></span>
<span data-ttu-id="47ff7-162">Modo de atualização para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="47ff7-163">As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado.</span><span class="sxs-lookup"><span data-stu-id="47ff7-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="47ff7-164">As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização. Valores possíveis \<br /\> \<br /\> **são Auto** \<br /\> \<br /\> **Manual** \<br /\> \<br /\>  \<br /\> \<br /\> Simultâneo Se não especificado, o valor padrão é Auto. Se definido como Manual, PUT UpdateDomain deve ser chamado para aplicar a atualização.</span><span class="sxs-lookup"><span data-stu-id="47ff7-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="47ff7-165">Se definido como Auto, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.</span><span class="sxs-lookup"><span data-stu-id="47ff7-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47ff7-166">-Confirm</span></span>
<span data-ttu-id="47ff7-167">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47ff7-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ff7-168">-WhatIf</span></span>
<span data-ttu-id="47ff7-169">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47ff7-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ff7-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47ff7-170">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ff7-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ff7-171">CommonParameters</span></span>
<span data-ttu-id="47ff7-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ff7-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ff7-173">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47ff7-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ff7-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47ff7-174">INPUTS</span></span>

## <span data-ttu-id="47ff7-175">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="47ff7-175">OUTPUTS</span></span>

### <span data-ttu-id="47ff7-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="47ff7-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="47ff7-177">NOTES</span><span class="sxs-lookup"><span data-stu-id="47ff7-177">NOTES</span></span>

<span data-ttu-id="47ff7-178">ALIASES</span><span class="sxs-lookup"><span data-stu-id="47ff7-178">ALIASES</span></span>

<span data-ttu-id="47ff7-179">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="47ff7-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47ff7-180">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="47ff7-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47ff7-181">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47ff7-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47ff7-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile> : descreve um perfil de extensão de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="47ff7-183">`[Extension <IExtension[]>]`: Lista de extensões para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="47ff7-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Especifique explicitamente se a plataforma pode atualizar automaticamente typeHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="47ff7-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="47ff7-185">`[ForceUpdateTag <String>]`: Marca para forçar a aplicação das configurações públicas e protegidas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="47ff7-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="47ff7-186">Alterar o valor da marca permite executar a extensão sem alterar nenhuma das configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="47ff7-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="47ff7-187">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="47ff7-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="47ff7-188">Se nem forceUpdateTag nem nenhuma das configurações públicas ou protegidas mudarem, a extensão fluirá para a instância de função com o mesmo número de sequência e a implementação do manipulador decidirá se a executará ou não.</span><span class="sxs-lookup"><span data-stu-id="47ff7-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="47ff7-189">`[Name <String>]`: O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="47ff7-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="47ff7-190">`[ProtectedSetting <String>]`: Configurações protegidas para a extensão que são criptografadas antes de enviadas para a instância de função.</span><span class="sxs-lookup"><span data-stu-id="47ff7-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="47ff7-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="47ff7-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="47ff7-192">`[Publisher <String>]`: O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="47ff7-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="47ff7-193">`[RolesAppliedTo <String[]>]`: Lista opcional de funções para aplicar essa extensão.</span><span class="sxs-lookup"><span data-stu-id="47ff7-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="47ff7-194">Se a propriedade não for especificada ou '\*' for especificada, a extensão será aplicada a todas as funções no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="47ff7-195">`[Setting <String>]`: Configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="47ff7-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="47ff7-196">Para extensões JSON, essas são as configurações JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="47ff7-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="47ff7-197">Para Extensão XML (como RDP), esta é a configuração XML da extensão.</span><span class="sxs-lookup"><span data-stu-id="47ff7-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="47ff7-198">`[SourceVaultId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="47ff7-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="47ff7-199">`[Type <String>]`: Especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="47ff7-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="47ff7-200">`[TypeHandlerVersion <String>]`: Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="47ff7-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="47ff7-201">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="47ff7-201">Specifies the version of the extension.</span></span> <span data-ttu-id="47ff7-202">Se esse elemento não for especificado ou um asterisco (\*) for usado como o valor, a versão mais recente da extensão será usada.</span><span class="sxs-lookup"><span data-stu-id="47ff7-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="47ff7-203">Se o valor for especificado com um número de versão principal e um asterisco como o número de versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada.</span><span class="sxs-lookup"><span data-stu-id="47ff7-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="47ff7-204">Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada.</span><span class="sxs-lookup"><span data-stu-id="47ff7-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="47ff7-205">Se uma versão for especificada, uma atualização automática será realizada na instância de função.</span><span class="sxs-lookup"><span data-stu-id="47ff7-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="47ff7-206">NETWORKPROFILE <ICloudServiceNetworkProfile> : Perfil de rede para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="47ff7-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: A lista de configurações do balanceador de carga para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="47ff7-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP</span><span class="sxs-lookup"><span data-stu-id="47ff7-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="47ff7-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="47ff7-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="47ff7-210">`[PrivateIPAddress <String>]`: O endereço IP privado referenciado pelo serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="47ff7-211">`[PublicIPAddressId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="47ff7-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="47ff7-212">`[SubnetId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="47ff7-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="47ff7-213">`[Name <String>]`: Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="47ff7-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="47ff7-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="47ff7-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="47ff7-215">`[Id <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="47ff7-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="47ff7-216">OSPROFILE <ICloudServiceOSProfile> : descreve o perfil do sistema operacional para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="47ff7-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Especifica o conjunto de certificados que devem ser instalados nas instâncias de função.</span><span class="sxs-lookup"><span data-stu-id="47ff7-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="47ff7-218">`[SourceVaultId <String>]`: ID de recurso</span><span class="sxs-lookup"><span data-stu-id="47ff7-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="47ff7-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências do cofre de chaves em SourceVault que contêm certificados.</span><span class="sxs-lookup"><span data-stu-id="47ff7-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="47ff7-220">`[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado no Cofre de Chaves como um segredo.</span><span class="sxs-lookup"><span data-stu-id="47ff7-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="47ff7-221">ROLEPROFILE <ICloudServiceRoleProfile> : Descreve o perfil de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="47ff7-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="47ff7-223">`[Name <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="47ff7-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="47ff7-224">`[SkuCapacity <Int64?>]`: Especifica o número de instâncias de função no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="47ff7-225">`[SkuName <String>]`: O nome sku.</span><span class="sxs-lookup"><span data-stu-id="47ff7-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="47ff7-226">OBSERVAÇÃO: se o novo SKU não tiver suporte no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para o sku antigo.</span><span class="sxs-lookup"><span data-stu-id="47ff7-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="47ff7-227">`[SkuTier <String>]`: Especifica a camada do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="47ff7-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="47ff7-228">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="47ff7-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="47ff7-229">**Standard**</span><span class="sxs-lookup"><span data-stu-id="47ff7-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="47ff7-230">**Básico**</span><span class="sxs-lookup"><span data-stu-id="47ff7-230">**Basic**</span></span>

## <span data-ttu-id="47ff7-231">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47ff7-231">RELATED LINKS</span></span>

