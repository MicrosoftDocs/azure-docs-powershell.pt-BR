---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
ms.openlocfilehash: 1049c4b69f0d64c9b18063618ee09018fd224196
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429335"
---
# Get-AzFunctionAppSetting

## Sinopse
Obtém as configurações do aplicativo para um aplicativo de função.

## SYNTAX

### ByName (padrão)
```
Get-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Get-AzFunctionAppSetting -InputObject <ISite> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRITIVO
Obtém as configurações do aplicativo para um aplicativo de função.

## EXEMPLOS

### Exemplo 1: obter as configurações do aplicativo de um aplicativo de função.
```powershell
PS C:\> Get-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName
```

Esse comando obtém as configurações do aplicativo de um aplicativo de função.

## OS

### -DefaultProfile


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
Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome do aplicativo da função.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos ao qual o recurso pertence.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da assinatura do Azure.

```yaml
Type: System.String[]
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. ISite

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. IStringDictionary

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTobject <ISite> : 
  - `Location <String>`: Local do recurso.
  - `CloningInfoSourceWebAppId <String>`: ID do recurso ARM do aplicativo de origem. A ID do recurso do aplicativo é do formulário/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} para slots de produção e/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} para outros slots.
  - `[Kind <String>]`: Tipo de recurso.
  - `[Tag <IResourceTags>]`: Marcas do recurso.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> para habilitar a afinidade do cliente; <code>false</code> para parar de enviar cookies de afinidade de sessão, que roteiam solicitações de cliente na mesma sessão para a mesma instância. O padrão é <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> para habilitar a autenticação de certificado de cliente (autenticação mútua do TLS); caso contrário, <code>false</code> . O padrão é <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: caminhos de exclusão separados por vírgula de autenticação de certificado do cliente
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Substituições de configuração de aplicativo para o aplicativo clonado. Se especificado, essas configurações substituirão as configurações clonadas do aplicativo de origem. Caso contrário, as configurações do aplicativo do aplicativo de origem serão mantidas.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> para clonar nomes de host personalizados do aplicativo de origem; caso contrário, <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> para clonar o controle de origem do aplicativo de origem; caso contrário, <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> para configurar o balanceamento de carga para o aplicativo de origem e de destino.
  - `[CloningInfoCorrelationId <String>]`: ID de correlação da operação de clonagem. Esse ID une várias operações de clonagem em conjunto para usar o mesmo instantâneo.
  - `[CloningInfoHostingEnvironment <String>]`: Ambiente de serviço de aplicativo.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> para substituir o aplicativo de destino; caso contrário, <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Local do aplicativo de origem por exemplo: Oeste EUA ou Europa norte
  - `[CloningInfoTrafficManagerProfileId <String>]`: ID do recurso ARM do perfil do Gerenciador de tráfego a ser usado, se existir. O ID do recurso do Gerenciador de tráfego tem o formato/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Nome do perfil do Gerenciador de tráfego a ser criado. Isso só é necessário se o perfil do Gerenciador de tráfego ainda não existe.
  - `[Config <ISiteConfig>]`: Configuração do aplicativo.
    - `IsPushEnabled <Boolean>`: Obtém ou define um sinalizador que indica se o ponto de extremidade de envio está habilitado.
    - `[ActionMinProcessExecutionTime <String>]`: Tempo mínimo que o processo deve executar antes de realizar a ação
    - `[ActionType <AutoHealActionType?>]`: Ação predefinida a ser executada.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> se a AlwaysOn estiver habilitada; caso contrário, <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: A URL da definição de API.
    - `[ApiManagementConfigId <String>]`: Identificador de APIM-Api.
    - `[AppCommandLine <String>]`: Linha de comando do aplicativo a ser iniciada.
    - `[AppSetting <INameValuePair[]>]`: Configurações do aplicativo.
      - `[Name <String>]`: Nome do par.
      - `[Value <String>]`: Emparelhar o valor.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> se a Rereparo automática estiver habilitada; caso contrário, <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Nome do slot de troca automática.
    - `[ConnectionString <IConnStringInfo[]>]`: Cadeias de conexão.
      - `[ConnectionString <String>]`: Valor da cadeia de conexão.
      - `[Name <String>]`: Nome da cadeia de conexão.
      - `[Type <ConnectionStringType?>]`: Tipo de banco de dados.
    - `[CorAllowedOrigin <String[]>]`: Obtém ou define a lista de origens que devem ser permitidas para fazer chamadas entre origens (por exemplo: http://example.com:12345) . Use "*" para permitir tudo.
    - `[CorSupportCredentials <Boolean?>]`: Obtém ou define se as solicitações CORS com credenciais são permitidas. Veja         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         mais detalhes.
    - `[CustomActionExe <String>]`: Executável a ser executado.
    - `[CustomActionParameter <String>]`: Parâmetros para o executável.
    - `[DefaultDocument <String[]>]`: Documentos padrão.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se o log de erros detalhado estiver habilitado; caso contrário, <code>false</code> .
    - `[DocumentRoot <String>]`: Raiz do documento.
    - `[DynamicTagsJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas dinâmicas que serão avaliadas de declarações de usuário no ponto de extremidade de registro Push.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Lista de regras de rampa.
      - `[ActionHostName <String>]`: Nome do host de um slot ao qual o tráfego será redirecionado se for decidido. :. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: O algoritmo de decisão personalizado pode ser fornecido na extensão de site do TiPCallback, a URL que pode ser especificada. Consulte extensão de site TiPCallback para o criam uma e contratos.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Especifica o intervalo em minutos para reavaliar o ReroutePercentage.
      - `[ChangeStep <Double?>]`: Em cenário de aumento automático, esta é a etapa a ser adicionada/removida <code>ReroutePercentage</code> até atingir \n <code>MinReroutePercentage</code> ou         <code>MaxReroutePercentage</code> . As métricas do site são verificadas a cada N minutos especificado no <code>ChangeIntervalInMinutes</code> algoritmo de decisão .\nCustom pode ser fornecido na extensão de site do TiPCallback na qual a URL pode ser especificada <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: Especifica o limite superior abaixo do qual o ReroutePercentage permanecerá.
      - `[MinReroutePercentage <Double?>]`: Especifica o limite inferior acima do qual o ReroutePercentage permanecerá.
      - `[Name <String>]`: Nome da regra de roteamento. O nome recomendado seria apontar para o slot, o que receberá o tráfego no experimento.
      - `[ReroutePercentage <Double?>]`: Porcentagem do tráfego que será redirecionado para <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: Estado do serviço de FTP/FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: Mapeamentos de manipuladores.
      - `[Argument <String>]`: Argumentos de linha de comando a serem passados para o processador de script.
      - `[Extension <String>]`: As solicitações com essa extensão serão manipuladas usando o aplicativo FastCGI especificado.
      - `[ScriptProcessor <String>]`: O caminho absoluto para o aplicativo FastCGI.
    - `[HealthCheckPath <String>]`: Caminho da verificação de integridade
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: configura um site da Web para permitir que os clientes se conectem via http 2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se o log http estiver habilitado; caso contrário, <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para Main.
      - `[Action <String>]`: Permitir ou negar acesso para este intervalo de IP.
      - `[Description <String>]`: Descrição da regra de restrição de IP.
      - `[IPAddress <String>]`: Endereço IP para o qual a restrição de segurança é válida.         Ela pode ser em forma de endereço IPv4 puro (Propriedade obrigatório submáscara de submáscara) ou de notação CIDR, como IPv4/máscara (correspondência de bit à esquerda). Para CIDR, a propriedade Máscara_de_Sub-máscara não deve ser especificada.
      - `[Name <String>]`: Nome da regra de restrição de IP.
      - `[Priority <Int32?>]`: Prioridade da regra de restrição de IP.
      - `[SubnetMask <String>]`: Máscara de sub-rede para o intervalo de endereços IP para o qual a restrição é válida.
      - `[SubnetTrafficTag <Int32?>]`: marca de tráfego de sub-rede (interna)
      - `[Tag <IPFilterTag?>]`: Define para que esse filtro de IP será usado. Isso é para dar suporte à filtragem de IP em proxies.
      - `[VnetSubnetResourceId <String>]`: ID do recurso de rede virtual
      - `[VnetTrafficTag <Int32?>]`: marca de tráfego de rede virtual (interna)
    - `[JavaContainer <String>]`: Contêiner Java.
    - `[JavaContainerVersion <String>]`: Versão do contêiner Java.
    - `[JavaVersion <String>]`: Versão Java.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Uso máximo de tamanho de disco permitido em MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Máximo de uso de memória permitido em MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Porcentagem máxima de uso de CPU permitida.
    - `[LinuxFxVersion <String>]`: Estrutura e versão do aplicativo Linux
    - `[LoadBalancing <SiteLoadBalancing?>]`: Balanceamento de carga do site.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> para habilitar o MySQL local; caso contrário, <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: O limite de tamanho do diretório de logs HTTP.
    - `[MachineKeyDecryption <String>]`: Algoritmo usado para decodificação.
    - `[MachineKeyDecryptionKey <String>]`: Chave de descriptografia.
    - `[MachineKeyValidation <String>]`: Validação de MachineKey.
    - `[MachineKeyValidationKey <String>]`: Chave de validação.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Modo de pipeline gerenciado.
    - `[ManagedServiceIdentityId <Int32?>]`: ID de identidade do serviço gerenciado
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura a versão mínima do TLS necessária para solicitações SSL
    - `[NetFrameworkVersion <String>]`: Versão do .NET Framework.
    - `[NodeVersion <String>]`: Versão do Node.js.
    - `[NumberOfWorker <Int32?>]`: Número de trabalhadores.
    - `[PhpVersion <String>]`: Versão do PHP.
    - `[PowerShellVersion <String>]`: Versão do PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Número de instâncias prequentes.         Essa configuração aplica-se somente aos planos de consumo e elástico
    - `[PublishingUsername <String>]`: Publicando o nome de usuário.
    - `[PushKind <String>]`: Tipo de recurso.
    - `[PythonVersion <String>]`: Versão do Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se a depuração remota estiver habilitada; caso contrário, <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Versão de depuração remota.
    - `[RequestCount <Int32?>]`: Contagem de solicitações.
    - `[RequestTimeInterval <String>]`: Intervalo de tempo.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> se o rastreamento de solicitação estiver habilitado; caso contrário, <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Solicitação de tempo de expiração do rastreamento.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para SCM.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Restrições de segurança IP para que o SCM use Main.
    - `[ScmType <ScmType?>]`: Tipo de SCM.
    - `[SlowRequestCount <Int32?>]`: Contagem de solicitações.
    - `[SlowRequestTimeInterval <String>]`: Intervalo de tempo.
    - `[SlowRequestTimeTaken <String>]`: Tempo deutilizado.
    - `[TagWhitelistJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que são brancas para uso pelo ponto de extremidade de registro Push.
    - `[TagsRequiringAuth <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que exigem que a autenticação do usuário seja usada no ponto de extremidade de registro Push.         As marcas podem consistir em caracteres alfanuméricos e o seguinte: ' _ ', ' @ ', ' # ', '. ', ': ', '-'.         A validação deve ser realizada no PushRequestHandler.
    - `[TracingOption <String>]`: Opções de rastreamento.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Uma regra com base em bytes particulares.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Uma regra com base em códigos de status.
      - `[Count <Int32?>]`: Contagem de solicitações.
      - `[Status <Int32?>]`: Código de status HTTP.
      - `[SubStatus <Int32?>]`: Solicitação de status de subscrição.
      - `[TimeInterval <String>]`: Intervalo de tempo.
      - `[Win32Status <Int32?>]`: Código de erro Win32.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> para usar o processo de trabalho de 32 bits; caso contrário, <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Aplicativos virtuais.
      - `[PhysicalPath <String>]`: Caminho físico.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> se o pré-carregamento estiver habilitado; caso contrário, <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Diretórios virtuais para o aplicativo virtual.
        - `[PhysicalPath <String>]`: Caminho físico.
        - `[VirtualPath <String>]`: Caminho para o aplicativo virtual.
      - `[VirtualPath <String>]`: Caminho virtual.
    - `[VnetName <String>]`: Nome da rede virtual.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket estiver habilitado; caso contrário, <code>false</code> .
    - `[WindowsFxVersion <String>]`: A estrutura e a versão do aplicativo Xenon
    - `[XManagedServiceIdentityId <Int32?>]`: ID de identidade do serviço explicitamente gerenciado
  - `[ContainerSize <Int32?>]`: Tamanho do contêiner da função.
  - `[DailyMemoryTimeQuota <Int32?>]`: Cota máxima permitida diária de tempo de memória (aplicável somente em aplicativos dinâmicos).
  - `[Enabled <Boolean?>]`: <code>true</code> se o aplicativo estiver habilitado; caso contrário, <code>false</code> . Definir esse valor como false desabilita o aplicativo (usa o aplicativo offline).
  - `[HostNameSslState <IHostNameSslState[]>]`: Os Estados SSL do nome do host são usados para gerenciar as associações SSL dos nomes de hosts do aplicativo.
    - `[HostType <HostType?>]`: Indica se o nome do host é um nome de host padrão ou de repositório.
    - `[Name <String>]`Hostname.
    - `[SslState <SslState?>]`: Tipo de SSL.
    - `[Thumbprint <String>]`: Impressão digital do certificado SSL.
    - `[ToUpdate <Boolean?>]`: Definido como <code>true</code> para atualizar o nome do host existente.
    - `[VirtualIP <String>]`: Endereço IP virtual atribuído ao nome do host se a SSL baseado em IP estiver habilitada.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> para desabilitar os nomes de host públicos do aplicativo; caso contrário, <code>false</code> .          Se <code>true</code> , o aplicativo estará acessível somente por meio do processo de gerenciamento de API.
  - `[HostingEnvironmentProfileId <String>]`: ID do recurso do ambiente do serviço de aplicativo.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: configura um site da Web para aceitar apenas solicitações HTTPS. Problemas de redirecionamento para solicitações http
  - `[HyperV <Boolean?>]`: Área restrita do Hyper-V.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Tipo de identidade de serviço gerenciado.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: A lista de identidades atribuídas pelo usuário associadas ao recurso. As referências de chave de dicionário de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[IsXenon <Boolean?>]`: Obsoleto: área restrita do Hyper-V.
  - `[RedundancyMode <RedundancyMode?>]`: Modo de redundância do site
  - `[Reserved <Boolean?>]`: <code>true</code> se reservada; caso contrário, <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> para interromper o site do SCM (KUDU) quando o aplicativo for interrompido; caso contrário, <code>false</code> . O padrão é <code>false</code> .
  - `[ServerFarmId <String>]`: ID do recurso do plano do serviço de aplicativo associado, formatada como: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## LINKS RELACIONADOS

