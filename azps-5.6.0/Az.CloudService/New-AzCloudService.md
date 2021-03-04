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
# New-AzCloudService

## SYNOPSIS
Criar ou atualizar um serviço de nuvem.
Observe que algumas propriedades só podem ser definidas durante a criação do serviço na nuvem.

## SINTAXE

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
Criar ou atualizar um serviço de nuvem.
Observe que algumas propriedades só podem ser definidas durante a criação do serviço na nuvem.

## EXEMPLOS

### Exemplo 1: Criar novo serviço de nuvem com função única
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

Acima do conjunto de comandos cria um serviço de nuvem com função única

### Exemplo 2: Criar novo serviço de nuvem com uma única função e extensão RDP
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

Acima, o conjunto de comandos cria um serviço de nuvem com uma única função e extensão RDP

### Exemplo 3: Criar novo serviço de nuvem com função única e certificado do cofre de chaves
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

O conjunto de comandos acima cria um serviço de nuvem com função única e certificado do cofre de chaves.

### Exemplo 4: Criar novo serviço de nuvem com várias funções e extensões
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

O conjunto de comandos acima cria um serviço de nuvem com função única e certificado do cofre de chaves.

## PARÂMETROS

### -AsJob
Executar o comando como um trabalho

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

### -Configuration
Especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.

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

### -ConfigurationUrl
Especifica uma URL que se refere ao local da configuração do serviço no serviço Blob.
A URL do pacote de serviço pode ser URI de Assinatura de Acesso Compartilhado (SAS) de qualquer conta de armazenamento. Esta é uma propriedade somente gravação e não é retornada em chamadas GET.

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

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -ExtensionProfile
Descreve um perfil de extensão do serviço de nuvem.
Para construir, consulte a seção NOTES para propriedades EXTENSIONPROFILE e crie uma tabela de hash.

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

### -Location
Local do recurso.

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

### -Name
Nome do serviço de nuvem.

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

### -NetworkProfile
Perfil de rede para o serviço de nuvem.
Para construir, consulte a seção NOTES para propriedades NETWORKPROFILE e crie uma tabela de hash.

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

### -NoWait
Executar o comando de forma assíncrona

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

### -OSProfile
Descreve o perfil do sistema operacional para o serviço de nuvem.
Para construir, consulte a seção NOTES para propriedades OSPROFILE e crie uma tabela de hash.

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

### -PackageUrl
Especifica uma URL que se refere ao local do pacote de serviço no serviço Blob.
A URL do pacote de serviço pode ser URI de Assinatura de Acesso Compartilhado (SAS) de qualquer conta de armazenamento. Esta é uma propriedade somente gravação e não é retornada em chamadas GET.

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

### -ResourceGroupName
Nome do grupo de recursos.

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

### -RoleProfile
Descreve o perfil de função do serviço de nuvem.
Para construir, consulte a seção NOTES para propriedades ROLEPROFILE e crie uma tabela de hash.

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

### -StartCloudService
(Opcional) Indica se deve iniciar o serviço de nuvem imediatamente após a criação.
O valor padrão é `true` . Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente.
Em vez disso, o serviço é PoweredOff até que você chame Start, momento em que o serviço será iniciado.
Um serviço implantado ainda incorre em encargos, mesmo que seja desligado.

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

### -SubscriptionId
Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura faz parte do URI para cada chamada de serviço.

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

### -Tag
Marcas de recurso.

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

### -UpgradeMode
Modo de atualização para o serviço de nuvem.
As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado.
As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização. Valores possíveis \<br /\> \<br /\> **são Auto** \<br /\> \<br /\> **Manual** \<br /\> \<br /\>  \<br /\> \<br /\> Simultâneo Se não especificado, o valor padrão é Auto. Se definido como Manual, PUT UpdateDomain deve ser chamado para aplicar a atualização.
Se definido como Auto, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.

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

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


EXTENSIONPROFILE <ICloudServiceExtensionProfile> : descreve um perfil de extensão de serviço de nuvem.
  - `[Extension <IExtension[]>]`: Lista de extensões para o serviço de nuvem.
    - `[AutoUpgradeMinorVersion <Boolean?>]`: Especifique explicitamente se a plataforma pode atualizar automaticamente typeHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.
    - `[ForceUpdateTag <String>]`: Marca para forçar a aplicação das configurações públicas e protegidas fornecidas.         Alterar o valor da marca permite executar a extensão sem alterar nenhuma das configurações públicas ou protegidas.         Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.         Se nem forceUpdateTag nem nenhuma das configurações públicas ou protegidas mudarem, a extensão fluirá para a instância de função com o mesmo número de sequência e a implementação do manipulador decidirá se a executará ou não.
    - `[Name <String>]`: O nome da extensão.
    - `[ProtectedSetting <String>]`: Configurações protegidas para a extensão que são criptografadas antes de enviadas para a instância de função.
    - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
    - `[Publisher <String>]`: O nome do editor do manipulador de extensão.
    - `[RolesAppliedTo <String[]>]`: Lista opcional de funções para aplicar essa extensão. Se a propriedade não for especificada ou '*' for especificada, a extensão será aplicada a todas as funções no serviço de nuvem.
    - `[Setting <String>]`: Configurações públicas para a extensão. Para extensões JSON, essas são as configurações JSON para a extensão. Para Extensão XML (como RDP), esta é a configuração XML da extensão.
    - `[SourceVaultId <String>]`: ID de recurso
    - `[Type <String>]`: Especifica o tipo da extensão.
    - `[TypeHandlerVersion <String>]`: Especifica a versão da extensão. Especifica a versão da extensão. Se esse elemento não for especificado ou um asterisco (*) for usado como o valor, a versão mais recente da extensão será usada. Se o valor for especificado com um número de versão principal e um asterisco como o número de versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada. Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada. Se uma versão for especificada, uma atualização automática será realizada na instância de função.

NETWORKPROFILE <ICloudServiceNetworkProfile> : Perfil de rede para o serviço de nuvem.
  - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: A lista de configurações do balanceador de carga para o serviço de nuvem.
    - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP
      - `[Name <String>]`: 
      - `[PrivateIPAddress <String>]`: O endereço IP privado referenciado pelo serviço de nuvem.
      - `[PublicIPAddressId <String>]`: ID de recurso
      - `[SubnetId <String>]`: ID de recurso
    - `[Name <String>]`: Nome do Recurso
  - `[SwappableCloudService <ISubResource>]`: 
    - `[Id <String>]`: ID de recurso

OSPROFILE <ICloudServiceOSProfile> : descreve o perfil do sistema operacional para o serviço de nuvem.
  - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Especifica o conjunto de certificados que devem ser instalados nas instâncias de função.
    - `[SourceVaultId <String>]`: ID de recurso
    - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências do cofre de chaves em SourceVault que contêm certificados.
      - `[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado no Cofre de Chaves como um segredo.

ROLEPROFILE <ICloudServiceRoleProfile> : Descreve o perfil de função do serviço de nuvem.
  - `[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções para o serviço de nuvem.
    - `[Name <String>]`: Nome do recurso.
    - `[SkuCapacity <Int64?>]`: Especifica o número de instâncias de função no serviço de nuvem.
    - `[SkuName <String>]`: O nome sku. OBSERVAÇÃO: se o novo SKU não tiver suporte no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para o sku antigo.
    - `[SkuTier <String>]`: Especifica a camada do serviço de nuvem. Os valores possíveis são <br /><br /> **Standard** <br /><br /> **Básico**

## LINKS RELACIONADOS

