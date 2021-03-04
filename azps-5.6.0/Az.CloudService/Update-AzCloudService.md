---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: bb67420e3fbb4479a79c7a837aad3b9a65635d88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892549"
---
# Update-AzCloudService

## SYNOPSIS
Criar ou atualizar um serviço de nuvem.
Observe que algumas propriedades só podem ser definidas durante a criação do serviço na nuvem.

## SINTAXE

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Criar ou atualizar um serviço de nuvem.
Observe que algumas propriedades só podem ser definidas durante a criação do serviço na nuvem.

## EXEMPLOS

### Exemplo 1: Adicionar extensão RDP ao serviço de nuvem existente
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

O conjunto de comandos acima adiciona uma extensão RDP ao serviço de nuvem já existente chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.

### Exemplo 2: Remover todas as extensões do serviço de nuvem
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

O conjunto de comandos acima remove todas as extensões do serviço de nuvem existente chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.

### Exemplo 3: Remover extensão RDP do serviço de nuvem
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

O conjunto de comandos acima remove a extensão RDP do serviço de nuvem existente chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.

### Exemplo 4: Scale-Out /Scale-In de função
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

O conjunto de comandos acima mostra como dimensionar e dimensionar a contagem de instâncias de função para o serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.

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

### -InputObject
Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Parameter
Descreve o serviço de nuvem.
Para construir, consulte a seção NOTES para propriedades PARAMETER e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT <ICloudServiceIdentity> : Parâmetro Identity
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: Caminho da identidade do recurso
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: Nome da instância da função.
  - `[RoleName <String>]`: Nome da função.
  - `[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura faz parte do URI para cada chamada de serviço.
  - `[UpdateDomain <Int32?>]`: Especifica um valor inteiro que identifica o domínio de atualização. Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.

PARÂMETRO <ICloudService> : Descreve o serviço de nuvem.
  - `Location <String>`: Localização do recurso.
  - `[Configuration <String>]`: Especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.
  - `[ConfigurationUrl <String>]`: Especifica uma URL que se refere ao local da configuração do serviço no serviço Blob. A URL do pacote de serviço pode ser URI de Assinatura de Acesso Compartilhado (SAS) de qualquer conta de armazenamento.         Esta é uma propriedade somente gravação e não é retornada em chamadas GET.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: Descreve um perfil de extensão do serviço de nuvem.
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
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: Perfil de rede para o serviço de nuvem.
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: A lista de configurações do balanceador de carga para o serviço de nuvem.
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`: O endereço IP privado referenciado pelo serviço de nuvem.
        - `[PublicIPAddressId <String>]`: ID de recurso
        - `[SubnetId <String>]`: ID de recurso
      - `[Name <String>]`: Nome do Recurso
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`: ID de recurso
  - `[OSProfile <ICloudServiceOSProfile>]`: Descreve o perfil do sistema operacional para o serviço de nuvem.
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Especifica o conjunto de certificados que devem ser instalados nas instâncias de função.
      - `[SourceVaultId <String>]`: ID de recurso
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências do cofre de chaves em SourceVault que contêm certificados.
        - `[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado no Cofre de Chaves como um segredo.
  - `[PackageUrl <String>]`: Especifica uma URL que se refere ao local do pacote de serviço no serviço Blob. A URL do pacote de serviço pode ser URI de Assinatura de Acesso Compartilhado (SAS) de qualquer conta de armazenamento.         Esta é uma propriedade somente gravação e não é retornada em chamadas GET.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: Descreve o perfil de função do serviço de nuvem.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções para o serviço de nuvem.
      - `[Name <String>]`: Nome do recurso.
      - `[SkuCapacity <Int64?>]`: Especifica o número de instâncias de função no serviço de nuvem.
      - `[SkuName <String>]`: O nome sku. OBSERVAÇÃO: se o novo SKU não tiver suporte no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para o sku antigo.
      - `[SkuTier <String>]`: Especifica a camada do serviço de nuvem. Os valores possíveis são <br /><br /> **Standard** <br /><br /> **Básico**
  - `[StartCloudService <Boolean?>]`: (Opcional) Indica se deve iniciar o serviço de nuvem imediatamente após a criação. O valor padrão é `true` .         Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente. Em vez disso, o serviço é PoweredOff até que você chame Start, momento em que o serviço será iniciado. Um serviço implantado ainda incorre em encargos, mesmo que seja desligado.
  - `[Tag <ICloudServiceTags>]`: Marcas de recurso.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: Modo de atualização para o serviço de nuvem. As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado. As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização.         Os valores possíveis são <br /><br />**Automático**<br /><br />**Manual** <br /><br />**Simultâneo**<br /><br />         Se não for especificado, o valor padrão será Auto. Se definido como Manual, PUT UpdateDomain deve ser chamado para aplicar a atualização. Se definido como Auto, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.

## LINKS RELACIONADOS

