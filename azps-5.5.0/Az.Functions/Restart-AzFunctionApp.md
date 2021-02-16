---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: 408adc74257e1260e97c47b24d91cf437b915a5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113638"
---
# Restart-AzFunctionApp

## Sinopse
Reinicia um aplicativo de função.

## Sintaxe

### RestartByName (Padrão)
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## Descrição
Reinicia um aplicativo de função.

## Exemplos

### Exemplo 1: Obter um aplicativo de função por nome e reiniciá-lo.
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

Esse comando obtém um aplicativo de função por nome e o reinicia.

### Exemplo 2: Reinicie um aplicativo de função por nome.
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Esse comando reinicia um aplicativo de função por nome.

## Parâmetros

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

### -Forçar
Força o cmdlet a reiniciar o aplicativo de função sem solicitar confirmação.

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

### -InputObject
Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.

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
O nome do aplicativo de função.

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Retorna verdadeiro quando o comando é bem-sucedido.

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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID de assinatura do Azure.

```yaml
Type: System.String
Parameter Sets: RestartByName
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

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## Saídas

### System.Boolean

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT: <ISite> 
  - `Location <String>`: Localização do Recurso.
  - `CloningInfoSourceWebAppId <String>`: ID do recurso ARM do aplicativo de origem. A ID do recurso de aplicativo é do formulário /assinaturas/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} para slots de produção e /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} para outros slots.
  - `[Kind <String>]`: Tipo de recurso.
  - `[Tag <IResourceTags>]`: Marcas de recurso.
    - `[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.
  - `[ClientAffinityEnabled <Boolean?>]`: para habilitar a afiliação do cliente; para parar de enviar cookies de afiliação de sessão, que roteam solicitações de cliente na mesma sessão <code>true</code> <code>false</code> para a mesma instância. O padrão é <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> para habilitar a autenticação de certificado do cliente (autenticação mútuo TLS); caso contrário, <code>false</code> . O padrão é <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: caminhos de exclusão separados por vírgulas separados por autenticação de certificado do cliente
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: A configuração do aplicativo substitui o aplicativo clonado. Se especificado, essas configurações substituem as configurações clonadas do aplicativo de origem. Caso contrário, as configurações do aplicativo de origem são mantidas.
    - `[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> para clonar nomes de host personalizados do aplicativo de origem; caso contrário, <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> para clonar o controle de origem do aplicativo de origem; caso contrário, <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> para configurar o balanceamento de carga para o aplicativo de origem e destino.
  - `[CloningInfoCorrelationId <String>]`: ID de correlação da operação de clonagem. Esta ID vincula várias operações de clonagem para usar o mesmo instantâneo.
  - `[CloningInfoHostingEnvironment <String>]`: Ambiente de Serviço de Aplicativos.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> para substituir o aplicativo de destino; caso contrário, <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: localização do aplicativo de origem, por ex: Oeste dos EUA ou Norte da Europa
  - `[CloningInfoTrafficManagerProfileId <String>]`: ID do recurso ARM do perfil do Gerenciador de Tráfego a ser usado, se ele existir. A ID de recurso do Gerenciador de Tráfego é do formulário /assinaturas/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Nome do perfil do Gerenciador de Tráfego para criar. Isso só será necessário se o perfil do Gerenciador de Tráfego ainda não existir.
  - `[Config <ISiteConfig>]`: Configuração do aplicativo.
    - `IsPushEnabled <Boolean>`: Obtém ou define um sinalizador indicando se o ponto de extremidade push está habilitado.
    - `[ActionMinProcessExecutionTime <String>]`: Tempo mínimo em que o processo deve ser executado antes de executar a ação
    - `[ActionType <AutoHealActionType?>]`: Ação predefinida a ser tomada.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> se Always On estiver habilitado; caso contrário, <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: A URL da definição da API.
    - `[ApiManagementConfigId <String>]`: APIM-Api Identificador.
    - `[AppCommandLine <String>]`: Linha de comando do aplicativo para iniciar.
    - `[AppSetting <INameValuePair[]>]`: Configurações do aplicativo.
      - `[Name <String>]`: Nome do par.
      - `[Value <String>]`: Valor do par.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> se AutoCarros estiver habilitado; caso contrário, <code>false</code> .
    - `[AutoSwapSlotName <String>]`: nome do slot de troca automática.
    - `[ConnectionString <IConnStringInfo[]>]`: cadeias de conexão.
      - `[ConnectionString <String>]`: valor da cadeia de conexão.
      - `[Name <String>]`: Nome da cadeia de conexão.
      - `[Type <ConnectionStringType?>]`: Tipo de banco de dados.
    - `[CorAllowedOrigin <String[]>]`: obtém ou define a lista de origens que devem ser permitidas para fazer chamadas de origem cruzada (por exemplo: http://example.com:12345) . Use "*" para permitir tudo.
    - `[CorSupportCredentials <Boolean?>]`: Obtém ou define se as solicitações do CORS com credenciais são permitidas. Veja         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         mais detalhes.
    - `[CustomActionExe <String>]`: Executável para ser executado.
    - `[CustomActionParameter <String>]`: Parâmetros para o executável.
    - `[DefaultDocument <String[]>]`: Documentos padrão.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se o log de erros detalhado estiver habilitado; caso contrário, <code>false</code> .
    - `[DocumentRoot <String>]`: raiz do documento.
    - `[DynamicTagsJson <String>]`: Obtém ou define uma cadeia de caracteres JSON contendo uma lista de marcas dinâmicas que serão avaliadas a partir de reclamações de usuários no ponto de extremidade de registro por push.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Lista de regras de aumento.
      - `[ActionHostName <String>]`: Nome do host de um slot para o qual o tráfego será redirecionado se decidir. E.g. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Algoritmo de decisão personalizado pode ser fornecido na extensão de site TiPCallback qual URL pode ser especificada. Consulte a extensão do site TiPCallback para o cadapasta e contratos.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Especifica o intervalo em minutos para reavaliar ReroutePercentage.
      - `[ChangeStep <Double?>]`: No cenário de aumento automático, esta é a etapa a ser seguida para adicionar/remover até <code>ReroutePercentage</code> atingir \n <code>MinReroutePercentage</code> ou         <code>MaxReroutePercentage</code> . As métricas do site são verificadas a cada N minutos especificado no algoritmo de decisão .\nCustom pode ser fornecido na extensão do site TiPCallback em que a URL pode ser <code>ChangeIntervalInMinutes</code> <code>ChangeDecisionCallbackUrl</code> especificada.
      - `[MaxReroutePercentage <Double?>]`: especifica o limite superior abaixo do qual o RedirecionamentoPercentage ficará.
      - `[MinReroutePercentage <Double?>]`: especifica o limite inferior acima do qual o RedirecionamentoPercentagem ficará.
      - `[Name <String>]`: Nome da regra de roteamento. O nome recomendado seria apontar para o slot que receberá o tráfego no experimento.
      - `[ReroutePercentage <Double?>]`: porcentagem do tráfego para o qual será <code>ActionHostName</code> redirecionado.
    - `[FtpsState <FtpsState?>]`: Estado do serviço FTP/FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: Mapeamentos de manipuladores.
      - `[Argument <String>]`: argumentos de linha de comando a serem passados para o processador de script.
      - `[Extension <String>]`: As solicitações com essa extensão serão tratadas usando o aplicativo FastCGI especificado.
      - `[ScriptProcessor <String>]`: o caminho absoluto para o aplicativo FastCGI.
    - `[HealthCheckPath <String>]`: Caminho de verificação de saúde
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: configura um site para permitir que os clientes se conectem por http2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se o log HTTP estiver habilitado; caso contrário, <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: restrições de segurança IP para principal.
      - `[Action <String>]`: Permitir ou Negar acesso a este intervalo IP.
      - `[Description <String>]`: descrição da regra de restrição de IP.
      - `[IPAddress <String>]`: endereço IP para o que a restrição de segurança é válida.         Pode ser em forma de endereço ipv4 puro (propriedade Desprot. de SubnetMask necessária) ou notação CIDR, como ipv4/mask (bit match à frente). Para CIDR, a propriedade SubnetMask não deve ser especificada.
      - `[Name <String>]`: nome da regra de restrição de IP.
      - `[Priority <Int32?>]`: Prioridade da regra de restrição de IP.
      - `[SubnetMask <String>]`: A máscara de sub-rede para o intervalo de endereços IP para a restrição é válida.
      - `[SubnetTrafficTag <Int32?>]`: marca de tráfego da sub-rede (interna)
      - `[Tag <IPFilterTag?>]`: define para que esse filtro IP será usado. Isso é para dar suporte à filtragem de IP em proxies.
      - `[VnetSubnetResourceId <String>]`: ID do recurso de rede virtual
      - `[VnetTrafficTag <Int32?>]`: (interno) marca de tráfego da Vnet
    - `[JavaContainer <String>]`: contêiner Java.
    - `[JavaContainerVersion <String>]`: Versão do contêiner Java.
    - `[JavaVersion <String>]`: Versão Java.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Uso máximo de tamanho de disco permitido em MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Uso máximo permitido de memória em MB.
    - `[LimitMaxPercentageCpu <Double?>]`: porcentagem máxima de uso da CPU permitida.
    - `[LinuxFxVersion <String>]`: Linux App Framework e versão
    - `[LoadBalancing <SiteLoadBalancing?>]`: Balanceamento de carga do site.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> para habilitar o MySQL local; caso contrário, <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: limite de tamanho de diretório de logs HTTP.
    - `[MachineKeyDecryption <String>]`: Algoritmo usado para descriptografia.
    - `[MachineKeyDecryptionKey <String>]`: Chave de descriptografia.
    - `[MachineKeyValidation <String>]`: Validação do MachineKey.
    - `[MachineKeyValidationKey <String>]`: Chave de validação.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Modo de pipeline gerenciado.
    - `[ManagedServiceIdentityId <Int32?>]`: ID de Identidade de Serviço Gerenciado
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura a versão mínima de TLS necessária para solicitações SSL
    - `[NetFrameworkVersion <String>]`: .NET Framework versão.
    - `[NodeVersion <String>]`: Versão do Node.js.
    - `[NumberOfWorker <Int32?>]`: Número de trabalhadores.
    - `[PhpVersion <String>]`: Versão do PHP.
    - `[PowerShellVersion <String>]`: Versão do PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Número de instâncias pré-requisitos.         Essa configuração se aplica somente aos Planos de Consumo e Elástica
    - `[PublishingUsername <String>]`: Nome de usuário de publicação.
    - `[PushKind <String>]`: Tipo de recurso.
    - `[PythonVersion <String>]`: Versão do Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se a depuração remota estiver habilitada; caso contrário, <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Versão de depuração remota.
    - `[RequestCount <Int32?>]`: Solicitar Contagem.
    - `[RequestTimeInterval <String>]`: Intervalo de tempo.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> se o rastreamento de solicitação estiver habilitado; caso contrário, <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Solicitar o rastreamento do tempo de expiração.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: restrições de segurança IP para scm.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: restrições de segurança IP para scm usar principal.
    - `[ScmType <ScmType?>]`: tipo de SCM.
    - `[SlowRequestCount <Int32?>]`: Solicitar Contagem.
    - `[SlowRequestTimeInterval <String>]`: Intervalo de tempo.
    - `[SlowRequestTimeTaken <String>]`: Tempo de tomada.
    - `[TagWhitelistJson <String>]`: Obtém ou define uma cadeia de caracteres JSON contendo uma lista de marcas listadas em branco para uso pelo ponto de extremidade de registro por push.
    - `[TagsRequiringAuth <String>]`: Obtém ou define uma cadeia de caracteres JSON contendo uma lista de marcas que exigem que a autenticação do usuário seja usada no ponto de extremidade de registro por push.         As marcas podem consistir em caracteres alfanuméricos e os seguintes: '_', '@', '#', '.', ':', '-'.         A validação deve ser realizada no PushRequestHandler.
    - `[TracingOption <String>]`: Opções de rastreamento.
    - `[TriggerPrivateBytesInKb <Int32?>]`: uma regra baseada em bytes particulares.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: uma regra baseada em códigos de status.
      - `[Count <Int32?>]`: Solicitar Contagem.
      - `[Status <Int32?>]`: código de status HTTP.
      - `[SubStatus <Int32?>]`: Solicitar Sub Status.
      - `[TimeInterval <String>]`: Intervalo de tempo.
      - `[Win32Status <Int32?>]`: código de erro Win32.
    - `[Use32BitWorkerProcess <Boolean?>]`: para usar o processo de trabalhador de <code>true</code> 32 bits; caso contrário, <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Aplicativos virtuais.
      - `[PhysicalPath <String>]`: Caminho físico.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> se o pré-carregamento estiver habilitado; caso contrário, <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Diretórios virtuais para aplicativos virtuais.
        - `[PhysicalPath <String>]`: Caminho físico.
        - `[VirtualPath <String>]`: Caminho para o aplicativo virtual.
      - `[VirtualPath <String>]`: Caminho virtual.
    - `[VnetName <String>]`: Nome da Rede Virtual.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket estiver habilitado; caso contrário, <code>false</code> .
    - `[WindowsFxVersion <String>]`: Framework e versão do aplicativo Dedados
    - `[XManagedServiceIdentityId <Int32?>]`: Identificação explícita de identidade de serviço gerenciado
  - `[ContainerSize <Int32?>]`: Tamanho do contêiner de função.
  - `[DailyMemoryTimeQuota <Int32?>]`: cota máxima permitida diária de tempo de memória (aplicável somente a aplicativos dinâmicos).
  - `[Enabled <Boolean?>]`: <code>true</code> se o aplicativo estiver habilitado; caso contrário, <code>false</code> . Definir esse valor como falso desabilita o aplicativo (o aplicativo fica offline).
  - `[HostNameSslState <IHostNameSslState[]>]`: Os estados SSL do nome do host são usados para gerenciar as ligações SSL para os nomes de host do aplicativo.
    - `[HostType <HostType?>]`: indica se o nome do host é um nome de host padrão ou de repositório.
    - `[Name <String>]`: Nome do host.
    - `[SslState <SslState?>]`: Tipo de SSL.
    - `[Thumbprint <String>]`: impressão de miniatura do certificado SSL.
    - `[ToUpdate <Boolean?>]`: Definido para <code>true</code> atualizar o nome de host existente.
    - `[VirtualIP <String>]`: Endereço IP virtual atribuído ao nome do host se SSL baseado em IP estiver habilitado.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> para desabilitar os nomes de host públicos do aplicativo; caso contrário, <code>false</code> .          Em <code>true</code> caso afirmativo, o aplicativo só pode ser acessado por meio de um processo de gerenciamento de API.
  - `[HostingEnvironmentProfileId <String>]`: ID do recurso do Ambiente de Serviço de Aplicativos.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: configura um site para aceitar apenas solicitações https. Problemas redirecionados para solicitações http
  - `[HyperV <Boolean?>]`: áreas de areia hiperv.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Tipo de identidade de serviço gerenciado.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: a lista de identidades atribuídas pelo usuário associada ao recurso. As referências de chave do dicionário de identidade do usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: indica que qualquer propriedade pode ser adicionada a este objeto.
  - `[IsXenon <Boolean?>]`: Obsoletas: área de areia hiperv.
  - `[RedundancyMode <RedundancyMode?>]`: Modo de redundância do site
  - `[Reserved <Boolean?>]`: <code>true</code> se reservada; caso contrário, <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> para interromper o site do SCM (KUDU) quando o aplicativo for interrompido; caso contrário, <code>false</code> . O padrão é <code>false</code> .
  - `[ServerFarmId <String>]`: ID de recurso do plano de Serviço de Aplicativo associado, formatado como: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## LINKS RELACIONADOS

