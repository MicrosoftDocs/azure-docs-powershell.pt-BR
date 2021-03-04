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
# Get-AzCloudServiceNetworkInterfaces

## SYNOPSIS
Obter as interfaces de rede de um serviço de nuvem.

## SINTAXE

### CloudServiceName (Padrão)
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### CloudService
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## DESCRIPTION
Obter as interfaces de rede de um serviço de nuvem.

## EXEMPLOS

### Exemplo 1: Obter interfaces de rede por um nome de serviço de nuvem
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

Obtém todas as interfaces de rede para um determinado nome de serviço de nuvem.

### Exemplo 2: Obter interfaces de rede por um objeto de serviço de nuvem
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

Obtém todas as interfaces de rede de um determinado objeto de serviço de nuvem.

### Exemplo 3: Obter interfaces de rede por um objeto de serviço de nuvem e nome de instância de função.
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

Obtém todas as interfaces de rede para um determinado objeto de serviço de nuvem e nome de instância de função.

## PARÂMETROS

### -CloudService
Instância do CloudService.
Para construir, consulte a seção NOTES para propriedades DO CLOUDSERVICE e crie uma tabela de hash.

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
CloudServiceName.

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

### -ResourceGroupName
ResourceGroupName.

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

### -RoleInstanceName
RoleInstanceName.

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

### -SubscriptionId
Assinatura.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


CLOUDSERVICE <CloudService> : Instância do CloudService.
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

