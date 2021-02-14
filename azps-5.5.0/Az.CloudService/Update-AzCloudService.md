---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: e0f9ad794f1631c5c8615480c6074f040f7fe749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111169"
---
# Update-AzCloudService

## Sinopse
Criar ou atualizar um serviço de nuvem.
Observe que algumas propriedades podem ser definidas somente durante a criação de serviços na nuvem.

## Sintaxe

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Descrição
Criar ou atualizar um serviço de nuvem.
Observe que algumas propriedades podem ser definidas somente durante a criação de serviços na nuvem.

## Exemplos

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

## Parâmetros

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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
Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.

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
Executar o comando assíncrona

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

### -Parâmetro
Descreve o serviço de nuvem.
Para construir, confira a seção ANOTAÇÕES para as propriedades PARÂMETRO e crie uma tabela hash.

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

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

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
Mostra o que acontece se o cmdlet for executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity

## Saídas

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: Caminho de identidade de recursos
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: Nome da instância da função.
  - `[RoleName <String>]`: nome da função.
  - `[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura faz parte do URI para cada chamada de serviço.
  - `[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização. Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.

PARÂMETRO: <ICloudService> descreve o serviço de nuvem.
  - `Location <String>`: Local do recurso.
  - `[Configuration <String>]`: especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.
  - `[ConfigurationUrl <String>]`: especifica uma URL que se refere ao local da configuração do serviço no serviço Blob. A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.         Essa é uma propriedade somente gravação e não é retornada em chamadas GET.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: descreve um perfil de extensão de serviço de nuvem.
    - `[Extension <IExtension[]>]`: Lista de extensões do serviço de nuvem.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: especifique explicitamente se a plataforma pode atualizar automaticamente o tipoHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.
      - `[ForceUpdateTag <String>]`: Marque para forçar a aplicação das configurações públicas e protegidas fornecidas.         Alterar o valor da marca permite executar a extensão de forma a executar a extensão sem alterar as configurações públicas ou protegidas.         Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.         Se nem forçarUpdateTag nem nenhuma das configurações públicas ou protegidas mudar, a extensão fluiria para a instância de função com o mesmo número de sequência, e a implementação de manipuladores decidirá se a executará ou não.
      - `[Name <String>]`: o nome da extensão.
      - `[ProtectedSetting <String>]`: Configurações protegidas para a extensão que são criptografadas antes de enviar para a instância de função.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: o nome do editor do manipulador de extensão.
      - `[RolesAppliedTo <String[]>]`: Lista opcional de funções para aplicar essa extensão. Se a propriedade não for especificada ou '*' for especificada, a extensão será aplicada a todas as funções no serviço de nuvem.
      - `[Setting <String>]`: Configurações públicas para a extensão. Para extensões JSON, essas são as configurações JSON para a extensão. Para Extensão XML (como RDP), essa é a configuração XML para a extensão.
      - `[SourceVaultId <String>]`: ID do Recurso
      - `[Type <String>]`: especifica o tipo da extensão.
      - `[TypeHandlerVersion <String>]`: especifica a versão da extensão. Especifica a versão da extensão. Se esse elemento não for especificado ou um asterisco (*) for usado como o valor, a versão mais recente da extensão será usada. Se o valor for especificado com um número de versão principal e um asterisco como o número da versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada. Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada. Se uma versão for especificada, uma atualização automática será executada na instância da função.
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: Perfil de Rede do serviço de nuvem.
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: a lista de configurações de balanceador de carga para o serviço de nuvem.
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`: O endereço IP particular referenciado pelo serviço de nuvem.
        - `[PublicIPAddressId <String>]`: ID do Recurso
        - `[SubnetId <String>]`: ID do Recurso
      - `[Name <String>]`: Nome do Recurso
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`: ID do Recurso
  - `[OSProfile <ICloudServiceOSProfile>]`: descreve o perfil do sistema operacional para o serviço de nuvem.
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: especifica o conjunto de certificados que devem ser instalados nas instâncias de função.
      - `[SourceVaultId <String>]`: ID do Recurso
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências chave do cofre no SourceVault que contêm certificados.
        - `[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado para o Cofre de Chaves como um segredo.
  - `[PackageUrl <String>]`: especifica uma URL que se refere ao local do pacote de serviço no serviço Blob. A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.         Essa é uma propriedade somente gravação e não é retornada em chamadas GET.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: descreve o perfil de função do serviço de nuvem.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções do serviço de nuvem.
      - `[Name <String>]`: Nome do recurso.
      - `[SkuCapacity <Int64?>]`: especifica o número de instâncias de função no serviço de nuvem.
      - `[SkuName <String>]`: o nome da sKU. OBSERVAÇÃO: se a nova SKU não for suportada no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para a SKU antiga.
      - `[SkuTier <String>]`: especifica o nível do serviço de nuvem. Os valores possíveis são <br /><br /> **Padrão** <br /><br /> **Basic**
  - `[StartCloudService <Boolean?>]`: (Opcional) Indica se o serviço de nuvem deve ser iniciar imediatamente após sua criação. O valor padrão é `true` .         Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente. Em vez disso, o serviço é PoweredOff até que você ligue para Iniciar, momento em que o serviço será iniciado. Um serviço implantado ainda incorre em encargos, mesmo que ele esteja desligado.
  - `[Tag <ICloudServiceTags>]`: Marcas de recurso.
    - `[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: Modo de atualização para o serviço de nuvem. As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado. As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização.         Os valores possíveis são <br /><br />**Automático**<br /><br />**Manual** <br /><br />**Simultânea**<br /><br />         Se não especificado, o valor padrão será Automático. Se definido como Manual, PUT UpdateDomain deverá ser chamado para aplicar a atualização. Se definido como Automático, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.

## LINKS RELACIONADOS

