---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 24e90ebae59c9d9a4449c57270b7ca69f9b05b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116576"
---
# <span data-ttu-id="db0c2-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="db0c2-101">New-AzCloudService</span></span>

## <span data-ttu-id="db0c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="db0c2-103">Criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-103">Create or update a cloud service.</span></span>
<span data-ttu-id="db0c2-104">Observe que algumas propriedades podem ser definidas somente durante a criação de serviços na nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="db0c2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db0c2-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="db0c2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="db0c2-106">DESCRIPTION</span></span>
<span data-ttu-id="db0c2-107">Criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-107">Create or update a cloud service.</span></span>
<span data-ttu-id="db0c2-108">Observe que algumas propriedades podem ser definidas somente durante a criação de serviços na nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="db0c2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db0c2-109">EXAMPLES</span></span>

### <span data-ttu-id="db0c2-110">Exemplo 1: Criar novo serviço de nuvem com uma única função</span><span class="sxs-lookup"><span data-stu-id="db0c2-110">Example 1: Create new cloud service with single role</span></span>
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

<span data-ttu-id="db0c2-111">O conjunto de comandos acima cria um serviço de nuvem com uma única função</span><span class="sxs-lookup"><span data-stu-id="db0c2-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="db0c2-112">Exemplo 2: Criar novo serviço de nuvem com uma única função e extensão RDP</span><span class="sxs-lookup"><span data-stu-id="db0c2-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
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

<span data-ttu-id="db0c2-113">O conjunto de comandos acima cria um serviço de nuvem com uma única função e extensão RDP</span><span class="sxs-lookup"><span data-stu-id="db0c2-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="db0c2-114">Exemplo 3: Criar novo serviço de nuvem com uma única função e certificado do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="db0c2-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
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

<span data-ttu-id="db0c2-115">O conjunto de comandos acima cria um serviço de nuvem com uma única função e certificado do cofre de teclas.</span><span class="sxs-lookup"><span data-stu-id="db0c2-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="db0c2-116">Exemplo 4: Criar novo serviço de nuvem com várias funções e extensões</span><span class="sxs-lookup"><span data-stu-id="db0c2-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
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

<span data-ttu-id="db0c2-117">O conjunto de comandos acima cria um serviço de nuvem com uma única função e certificado do cofre de teclas.</span><span class="sxs-lookup"><span data-stu-id="db0c2-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="db0c2-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db0c2-118">PARAMETERS</span></span>

### <span data-ttu-id="db0c2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db0c2-119">-AsJob</span></span>
<span data-ttu-id="db0c2-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="db0c2-120">Run the command as a job</span></span>

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

### <span data-ttu-id="db0c2-121">-Configuração</span><span class="sxs-lookup"><span data-stu-id="db0c2-121">-Configuration</span></span>
<span data-ttu-id="db0c2-122">Especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

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

### <span data-ttu-id="db0c2-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="db0c2-123">-ConfigurationUrl</span></span>
<span data-ttu-id="db0c2-124">Especifica uma URL que se refere ao local da configuração do serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="db0c2-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="db0c2-125">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento. Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="db0c2-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="db0c2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db0c2-126">-DefaultProfile</span></span>
<span data-ttu-id="db0c2-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db0c2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db0c2-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="db0c2-128">-ExtensionProfile</span></span>
<span data-ttu-id="db0c2-129">Descreve um perfil de extensão de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="db0c2-130">Para construir, confira a seção ANOTAÇÕES para propriedades EXTENSIONPROFILE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="db0c2-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="db0c2-131">-Local</span><span class="sxs-lookup"><span data-stu-id="db0c2-131">-Location</span></span>
<span data-ttu-id="db0c2-132">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="db0c2-132">Resource location.</span></span>

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

### <span data-ttu-id="db0c2-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="db0c2-133">-Name</span></span>
<span data-ttu-id="db0c2-134">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-134">Name of the cloud service.</span></span>

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

### <span data-ttu-id="db0c2-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="db0c2-135">-NetworkProfile</span></span>
<span data-ttu-id="db0c2-136">Perfil de Rede para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="db0c2-137">Para construir, consulte a seção ANOTAÇÕES para propriedades NETWORKPROFILE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="db0c2-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="db0c2-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="db0c2-138">-NoWait</span></span>
<span data-ttu-id="db0c2-139">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="db0c2-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="db0c2-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="db0c2-140">-OSProfile</span></span>
<span data-ttu-id="db0c2-141">Descreve o perfil do sistema operacional para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="db0c2-142">Para construir, consulte a seção ANOTAÇÕES para propriedades DO OSPROFILE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="db0c2-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="db0c2-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="db0c2-143">-PackageUrl</span></span>
<span data-ttu-id="db0c2-144">Especifica uma URL que se refere ao local do pacote de serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="db0c2-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="db0c2-145">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento. Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="db0c2-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="db0c2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db0c2-146">-ResourceGroupName</span></span>
<span data-ttu-id="db0c2-147">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db0c2-147">Name of the resource group.</span></span>

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

### <span data-ttu-id="db0c2-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="db0c2-148">-RoleProfile</span></span>
<span data-ttu-id="db0c2-149">Descreve o perfil de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="db0c2-150">Para construir, consulte a seção ANOTAÇÕES para propriedades ROLEPROFILE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="db0c2-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="db0c2-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="db0c2-151">-StartCloudService</span></span>
<span data-ttu-id="db0c2-152">(Opcional) Indica se você deve iniciar o serviço de nuvem imediatamente depois que ele for criado.</span><span class="sxs-lookup"><span data-stu-id="db0c2-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="db0c2-153">O valor padrão é `true` . Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="db0c2-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="db0c2-154">Em vez disso, o serviço é PoweredOff até que você ligue para Iniciar, momento em que o serviço será iniciado.</span><span class="sxs-lookup"><span data-stu-id="db0c2-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="db0c2-155">Um serviço implantado ainda incorre em encargos, mesmo que ele esteja desligado.</span><span class="sxs-lookup"><span data-stu-id="db0c2-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

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

### <span data-ttu-id="db0c2-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db0c2-156">-SubscriptionId</span></span>
<span data-ttu-id="db0c2-157">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db0c2-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="db0c2-158">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="db0c2-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="db0c2-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="db0c2-159">-Tag</span></span>
<span data-ttu-id="db0c2-160">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="db0c2-160">Resource tags.</span></span>

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

### <span data-ttu-id="db0c2-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="db0c2-161">-UpgradeMode</span></span>
<span data-ttu-id="db0c2-162">Modo de atualização para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="db0c2-163">As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado.</span><span class="sxs-lookup"><span data-stu-id="db0c2-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="db0c2-164">As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização. Os Valores \<br /\> \<br /\> **Possíveis são o Simultâneo** \<br /\> \<br /\> **Manual Automático** Se não \<br /\> \<br /\>  \<br /\> \<br /\> especificado, o valor padrão é Automático. Se definido como Manual, PUT UpdateDomain deverá ser chamado para aplicar a atualização.</span><span class="sxs-lookup"><span data-stu-id="db0c2-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="db0c2-165">Se definido como Automático, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.</span><span class="sxs-lookup"><span data-stu-id="db0c2-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

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

### <span data-ttu-id="db0c2-166">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="db0c2-166">-Confirm</span></span>
<span data-ttu-id="db0c2-167">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db0c2-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db0c2-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db0c2-168">-WhatIf</span></span>
<span data-ttu-id="db0c2-169">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="db0c2-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db0c2-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db0c2-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db0c2-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db0c2-171">CommonParameters</span></span>
<span data-ttu-id="db0c2-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db0c2-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db0c2-173">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db0c2-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db0c2-174">Entradas</span><span class="sxs-lookup"><span data-stu-id="db0c2-174">INPUTS</span></span>

## <span data-ttu-id="db0c2-175">Saídas</span><span class="sxs-lookup"><span data-stu-id="db0c2-175">OUTPUTS</span></span>

### <span data-ttu-id="db0c2-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="db0c2-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="db0c2-177">Notas</span><span class="sxs-lookup"><span data-stu-id="db0c2-177">NOTES</span></span>

<span data-ttu-id="db0c2-178">Aliases</span><span class="sxs-lookup"><span data-stu-id="db0c2-178">ALIASES</span></span>

<span data-ttu-id="db0c2-179">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="db0c2-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db0c2-180">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="db0c2-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db0c2-181">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db0c2-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db0c2-182">EXTENSIONPROFILE: <ICloudServiceExtensionProfile> descreve um perfil de extensão de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="db0c2-183">`[Extension <IExtension[]>]`: Lista de extensões do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="db0c2-184">`[AutoUpgradeMinorVersion <Boolean?>]`: especifique explicitamente se a plataforma pode atualizar automaticamente o typeHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="db0c2-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="db0c2-185">`[ForceUpdateTag <String>]`: Marque para forçar a aplicação das configurações públicas e protegidas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="db0c2-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="db0c2-186">Alterar o valor da marca permite executar a extensão de forma a executar a extensão sem alterar as configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="db0c2-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="db0c2-187">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="db0c2-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="db0c2-188">Se nenhuma das configurações públicas ou protegidas for de forçaUpdateTag, a extensão fluirá para a instância de função com o mesmo número de sequência, e a implementação do manipulador decidirá se a executará ou não.</span><span class="sxs-lookup"><span data-stu-id="db0c2-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="db0c2-189">`[Name <String>]`: o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="db0c2-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="db0c2-190">`[ProtectedSetting <String>]`: Configurações protegidas para a extensão que são criptografadas antes de enviar para a instância de função.</span><span class="sxs-lookup"><span data-stu-id="db0c2-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="db0c2-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="db0c2-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="db0c2-192">`[Publisher <String>]`: o nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="db0c2-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="db0c2-193">`[RolesAppliedTo <String[]>]`: Lista opcional de funções para aplicar essa extensão.</span><span class="sxs-lookup"><span data-stu-id="db0c2-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="db0c2-194">Se a propriedade não for especificada ou '\*' for especificada, a extensão será aplicada a todas as funções no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="db0c2-195">`[Setting <String>]`: Configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="db0c2-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="db0c2-196">Para extensões JSON, essas são as configurações JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="db0c2-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="db0c2-197">Para Extensão XML (como RDP), essa é a configuração XML para a extensão.</span><span class="sxs-lookup"><span data-stu-id="db0c2-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="db0c2-198">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="db0c2-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="db0c2-199">`[Type <String>]`: especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="db0c2-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="db0c2-200">`[TypeHandlerVersion <String>]`: especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="db0c2-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="db0c2-201">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="db0c2-201">Specifies the version of the extension.</span></span> <span data-ttu-id="db0c2-202">Se esse elemento não for especificado ou um asterisco (\*) for usado como o valor, a versão mais recente da extensão será usada.</span><span class="sxs-lookup"><span data-stu-id="db0c2-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="db0c2-203">Se o valor for especificado com um número de versão principal e um asterisco como o número da versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada.</span><span class="sxs-lookup"><span data-stu-id="db0c2-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="db0c2-204">Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada.</span><span class="sxs-lookup"><span data-stu-id="db0c2-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="db0c2-205">Se uma versão for especificada, uma atualização automática será executada na instância da função.</span><span class="sxs-lookup"><span data-stu-id="db0c2-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="db0c2-206">NETWORKPROFILE: <ICloudServiceNetworkProfile> Perfil de Rede para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="db0c2-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: a lista de configurações de balanceador de carga para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="db0c2-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP</span><span class="sxs-lookup"><span data-stu-id="db0c2-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="db0c2-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="db0c2-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="db0c2-210">`[PrivateIPAddress <String>]`: O endereço IP particular referenciado pelo serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="db0c2-211">`[PublicIPAddressId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="db0c2-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="db0c2-212">`[SubnetId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="db0c2-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="db0c2-213">`[Name <String>]`: Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="db0c2-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="db0c2-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="db0c2-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="db0c2-215">`[Id <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="db0c2-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="db0c2-216">OSPROFILE: <ICloudServiceOSProfile> descreve o perfil do sistema operacional para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="db0c2-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: especifica o conjunto de certificados que devem ser instalados nas instâncias de função.</span><span class="sxs-lookup"><span data-stu-id="db0c2-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="db0c2-218">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="db0c2-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="db0c2-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências chave do cofre no SourceVault que contêm certificados.</span><span class="sxs-lookup"><span data-stu-id="db0c2-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="db0c2-220">`[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado para o Cofre de Chaves como um segredo.</span><span class="sxs-lookup"><span data-stu-id="db0c2-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="db0c2-221">ROLEPROFILE: <ICloudServiceRoleProfile> descreve o perfil de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="db0c2-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="db0c2-223">`[Name <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="db0c2-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="db0c2-224">`[SkuCapacity <Int64?>]`: especifica o número de instâncias de função no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="db0c2-225">`[SkuName <String>]`: o nome da sKU.</span><span class="sxs-lookup"><span data-stu-id="db0c2-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="db0c2-226">OBSERVAÇÃO: se a nova SKU não for suportada no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para a SKU antiga.</span><span class="sxs-lookup"><span data-stu-id="db0c2-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="db0c2-227">`[SkuTier <String>]`: especifica o nível do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="db0c2-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="db0c2-228">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="db0c2-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="db0c2-229">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="db0c2-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="db0c2-230">**Basic**</span><span class="sxs-lookup"><span data-stu-id="db0c2-230">**Basic**</span></span>

## <span data-ttu-id="db0c2-231">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db0c2-231">RELATED LINKS</span></span>

