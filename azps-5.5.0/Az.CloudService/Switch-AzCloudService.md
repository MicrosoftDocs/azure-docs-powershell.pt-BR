---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115495"
---
# Switch-AzCloudService

## Sinopse
Troca VIPs entre dois balanceadores de carga de serviço na nuvem (suporte estendido).

## Sintaxe

### CloudServiceName (Padrão)
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CloudService
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Descrição
Troca VIPs entre dois balanceadores de carga de serviço na nuvem (suporte estendido).

## Exemplos

### Exemplo 1: Alternar o serviço de nuvem usando o nome
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

O comando Acima invocará a operação vipswap no serviço de Nuvem com o nome 'BService' e executará a operação assim que o usuário confirmar a ação no prompt de confirmação.
'BService' com o serviço de nuvem permutável.

### Exemplo 2: Alternar o serviço de nuvem usando o objeto de serviço de nuvem
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

O comando Acima invocará a operação vipswap no serviço de Nuvem com o nome 'BService' e executará a operação assim que o usuário confirmar a ação no prompt de confirmação.
'BService' com o serviço de nuvem permutável.

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

### -Async


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

### -CloudService
Para construir, confira a seção ANOTAÇÕES para propriedades DE SERVIÇO NA NUVEM e crie uma tabela hash.

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

### -CloudServiceName


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

### -ResourceGroupName


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

## Saídas

### System.Boolean

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


SERVIÇO DE <CloudService> NUVEM: 
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
      - `[TypeHandlerVersion <String>]`: especifica a versão da extensão. Especifica a versão da extensão. Se esse elemento não for especificado ou um asterisco (*) for usado como valor, a versão mais recente da extensão será usada. Se o valor for especificado com um número de versão principal e um asterisco como o número da versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada. Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada. Se uma versão for especificada, uma atualização automática será executada na instância da função.
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
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências do cofre-chave no SourceVault que contêm certificados.
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

