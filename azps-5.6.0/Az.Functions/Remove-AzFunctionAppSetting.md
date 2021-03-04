---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: d6c0269fd0db63160e7258124bb605b43bcc5f97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901478"
---
# Remove-AzFunctionAppSetting

## SYNOPSIS
Remove as configurações do aplicativo de um aplicativo de função.

## SINTAXE

### ByName (Padrão)
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Remove as configurações do aplicativo de um aplicativo de função.

## EXEMPLOS

### Exemplo 1: Remover configurações de aplicativo em um aplicativo de função.
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

Este comando remove as configurações do aplicativo em um aplicativo de função.

## PARÂMETROS

### -AppSettingName
Lista de configurações de aplicativo de função a serem removidas do aplicativo de função.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Force
Força o cmdlet a remover a configuração do aplicativo de função sem solicitar confirmação.

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
Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.

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

### -Name
Nome do aplicativo de função.

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
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT <ISite> : 
  - `Location <String>`: Localização do Recurso.
  - `CloningInfoSourceWebAppId <String>`: ARM ID de recurso do aplicativo de origem. A ID de recurso do aplicativo é do formulário /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} para slots de produção e /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} para outros slots.
  - `[Kind <String>]`: Tipo de recurso.
  - `[Tag <IResourceTags>]`: Marcas de recurso.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[ClientAffinityEnabled <Boolean?>]`: para habilitar a afinidade do cliente; para parar de enviar cookies de afinidade de sessão, que encaminham solicitações de cliente na mesma sessão <code>true</code> <code>false</code> para a mesma instância. O padrão é <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> para habilitar a autenticação de certificado do cliente (autenticação mútua TLS); caso contrário, <code>false</code> . O padrão é <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: caminhos de exclusão separados por vírgulas de autenticação de certificado do cliente
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: A configuração do aplicativo substitui o aplicativo clonado. Se especificado, essas configurações substituem as configurações clonadas do aplicativo de origem. Caso contrário, as configurações do aplicativo de origem são mantidas.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> para clonar nomes de host personalizados do aplicativo de origem; caso contrário, <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> para clonar o controle de origem do aplicativo de origem; caso contrário, <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> para configurar o balanceamento de carga para o aplicativo de origem e destino.
  - `[CloningInfoCorrelationId <String>]`: ID de correlação da operação de clonagem. Essa ID vincula várias operações de clonagem para usar o mesmo instantâneo.
  - `[CloningInfoHostingEnvironment <String>]`: Ambiente de Serviço de Aplicativo.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> para substituir o aplicativo de destino; caso contrário, <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Local do aplicativo de origem ex: Oeste dos EUA ou norte da Europa
  - `[CloningInfoTrafficManagerProfileId <String>]`: ARM ID de recurso do perfil do Gerenciador de Tráfego a ser usado, se existir. A ID de recurso do Gerenciador de Tráfego é do formulário /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Nome do perfil do Gerenciador de Tráfego a ser criado. Isso só será necessário se o perfil do Gerenciador de Tráfego ainda não existir.
  - `[Config <ISiteConfig>]`: Configuração do aplicativo.
    - `IsPushEnabled <Boolean>`: Obtém ou define um sinalizador indicando se o ponto de extremidade push está habilitado.
    - `[ActionMinProcessExecutionTime <String>]`: Tempo mínimo em que o processo deve ser executado antes de executar a ação
    - `[ActionType <AutoHealActionType?>]`: Ação predefinida a ser tomada.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> se Always On estiver habilitado; caso contrário, <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: A URL da definição da API.
    - `[ApiManagementConfigId <String>]`: APIM-Api Identificador.
    - `[AppCommandLine <String>]`: Linha de comando do aplicativo a ser lançada.
    - `[AppSetting <INameValuePair[]>]`: Configurações do aplicativo.
      - `[Name <String>]`: Nome do par.
      - `[Value <String>]`: Valor do par.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> se a Cura Automática estiver habilitada; caso contrário, <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Nome do slot de troca automática.
    - `[ConnectionString <IConnStringInfo[]>]`: Cadeias de caracteres de conexão.
      - `[ConnectionString <String>]`: Valor da cadeia de caracteres de conexão.
      - `[Name <String>]`: Nome da cadeia de caracteres de conexão.
      - `[Type <ConnectionStringType?>]`: Tipo de banco de dados.
    - `[CorAllowedOrigin <String[]>]`: Obtém ou define a lista de origens que devem ser permitidas para fazer chamadas de origem cruzada (por exemplo: http://example.com:12345) . Use "*" para permitir tudo.
    - `[CorSupportCredentials <Boolean?>]`: Obtém ou define se solicitações CORS com credenciais são permitidas. Confira         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         mais detalhes.
    - `[CustomActionExe <String>]`: Executável a ser executado.
    - `[CustomActionParameter <String>]`: Parâmetros para o executável.
    - `[DefaultDocument <String[]>]`: Documentos padrão.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se o log de erros detalhado estiver habilitado; caso contrário, <code>false</code> .
    - `[DocumentRoot <String>]`: Raiz do documento.
    - `[DynamicTagsJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas dinâmicas que serão avaliadas a partir de declarações do usuário no ponto de extremidade de registro por push.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Lista de regras de rampa.
      - `[ActionHostName <String>]`: Nome do host de um slot para o qual o tráfego será redirecionado se decidir. Por exemplo, myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Algoritmo de decisão personalizado pode ser fornecido na extensão de site TiPCallback qual URL pode ser especificada. Consulte Extensão de site TiPCallback para o scaffold e contratos.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Especifica o intervalo em minutos para reavaliar ReroutePercentage.
      - `[ChangeStep <Double?>]`: No cenário de rampa automática, esta é a etapa para adicionar/remover até atingir <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> ou         <code>MaxReroutePercentage</code> . As métricas de site são verificadas a cada N minutos especificado no algoritmo de decisão .\nCustom pode ser fornecido na extensão de <code>ChangeIntervalInMinutes</code> site TiPCallback, que URL pode ser especificada em <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: Especifica o limite superior abaixo do qual ReroutePercentage ficará.
      - `[MinReroutePercentage <Double?>]`: Especifica o limite inferior acima do qual ReroutePercentage ficará.
      - `[Name <String>]`: Nome da regra de roteamento. O nome recomendado seria apontar para o slot que receberá o tráfego no experimento.
      - `[ReroutePercentage <Double?>]`: Porcentagem do tráfego que será redirecionado para <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: Estado do serviço FTP/FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: Mapeamentos de manipuladores.
      - `[Argument <String>]`: Argumentos de linha de comando a serem passados para o processador de script.
      - `[Extension <String>]`: As solicitações com essa extensão serão tratadas usando o aplicativo FastCGI especificado.
      - `[ScriptProcessor <String>]`: O caminho absoluto para o aplicativo FastCGI.
    - `[HealthCheckPath <String>]`: Caminho de verificação de saúde
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: configura um site para permitir que os clientes se conectem por http2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se o log HTTP estiver habilitado; caso contrário, <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para principal.
      - `[Action <String>]`: Permitir ou negar acesso a esse intervalo DE IP.
      - `[Description <String>]`: Descrição da regra de restrição de IP.
      - `[IPAddress <String>]`: Endereço IP para o que a restrição de segurança é válida.         Ele pode estar em forma de endereço ipv4 puro (propriedade SubnetMask necessária) ou notação CIDR, como ipv4/mask (combinação de bits à frente). Para CIDR, a propriedade SubnetMask não deve ser especificada.
      - `[Name <String>]`: Nome da regra de restrição de IP.
      - `[Priority <Int32?>]`: Prioridade da regra de restrição de IP.
      - `[SubnetMask <String>]`: Máscara de sub-rede para o intervalo de endereços IP para o que a restrição é válida.
      - `[SubnetTrafficTag <Int32?>]`: (interna) Marca de tráfego de sub-rede
      - `[Tag <IPFilterTag?>]`: Define para que esse filtro IP será usado. Isso é para dar suporte à filtragem de IP em proxies.
      - `[VnetSubnetResourceId <String>]`: ID de recurso de rede virtual
      - `[VnetTrafficTag <Int32?>]`: marca de tráfego Vnet (interna)
    - `[JavaContainer <String>]`: Java contêiner.
    - `[JavaContainerVersion <String>]`: Java versão do contêiner.
    - `[JavaVersion <String>]`: Java versão.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Uso máximo permitido do tamanho do disco em MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Uso máximo permitido de memória em MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Percentual máximo permitido de uso da CPU.
    - `[LinuxFxVersion <String>]`: Estrutura e versão do aplicativo Linux
    - `[LoadBalancing <SiteLoadBalancing?>]`: Balanceamento de carga do site.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> para habilitar MySQL local; caso contrário, <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: Http registra o limite de tamanho do diretório.
    - `[MachineKeyDecryption <String>]`: Algoritmo usado para descriptografia.
    - `[MachineKeyDecryptionKey <String>]`: Chave de descriptografia.
    - `[MachineKeyValidation <String>]`: Validação MachineKey.
    - `[MachineKeyValidationKey <String>]`: Chave de validação.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Modo de pipeline gerenciado.
    - `[ManagedServiceIdentityId <Int32?>]`: ID de Identidade de Serviço Gerenciado
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura a versão mínima do TLS necessária para solicitações SSL
    - `[NetFrameworkVersion <String>]`: .NET Framework versão.
    - `[NodeVersion <String>]`: Versão do Node.js.
    - `[NumberOfWorker <Int32?>]`: Número de funcionários.
    - `[PhpVersion <String>]`: Versão do PHP.
    - `[PowerShellVersion <String>]`: Versão do PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Número de instâncias pré-armas.         Essa configuração só se aplica aos Planos de Consumo e Elástica
    - `[PublishingUsername <String>]`: Nome de usuário de publicação.
    - `[PushKind <String>]`: Tipo de recurso.
    - `[PythonVersion <String>]`: Versão do Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se a depuração remota estiver habilitada; caso contrário, <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Versão de depuração remota.
    - `[RequestCount <Int32?>]`: Contagem de solicitação.
    - `[RequestTimeInterval <String>]`: Intervalo de tempo.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> se o rastreamento de solicitação estiver habilitado; caso contrário, <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Solicitar o tempo de expiração do rastreamento.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para scm.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Restrições de segurança IP para scm usar principal.
    - `[ScmType <ScmType?>]`: Tipo SCM.
    - `[SlowRequestCount <Int32?>]`: Contagem de solicitação.
    - `[SlowRequestTimeInterval <String>]`: Intervalo de tempo.
    - `[SlowRequestTimeTaken <String>]`: Tempo de vida.
    - `[TagWhitelistJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que estão listadas em branco para uso pelo ponto de extremidade de registro por push.
    - `[TagsRequiringAuth <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que exigem que a autenticação do usuário seja usada no ponto de extremidade de registro por push.         As marcas podem consistir em caracteres alfanuméricos e os seguintes: '_', '@', '#', '.', ':', '-'.         A validação deve ser realizada no PushRequestHandler.
    - `[TracingOption <String>]`: Opções de rastreamento.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Uma regra baseada em bytes privados.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Uma regra baseada em códigos de status.
      - `[Count <Int32?>]`: Contagem de solicitação.
      - `[Status <Int32?>]`: Código de status HTTP.
      - `[SubStatus <Int32?>]`: Solicitar Sub Status.
      - `[TimeInterval <String>]`: Intervalo de tempo.
      - `[Win32Status <Int32?>]`: Código de erro win32.
    - `[Use32BitWorkerProcess <Boolean?>]`: para usar o processo de trabalho de <code>true</code> 32 bits; caso contrário, <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Aplicativos virtuais.
      - `[PhysicalPath <String>]`: Caminho físico.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> se o pré-carregamento estiver habilitado; caso contrário, <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Diretórios virtuais para aplicativo virtual.
        - `[PhysicalPath <String>]`: Caminho físico.
        - `[VirtualPath <String>]`: Caminho para aplicativo virtual.
      - `[VirtualPath <String>]`: Caminho virtual.
    - `[VnetName <String>]`: Nome da Rede Virtual.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket estiver habilitado; caso contrário, <code>false</code> .
    - `[WindowsFxVersion <String>]`: Estrutura e versão do aplicativo xenónio
    - `[XManagedServiceIdentityId <Int32?>]`: Id de Identidade de Serviço Gerenciado Explícito
  - `[ContainerSize <Int32?>]`: Tamanho do contêiner de função.
  - `[DailyMemoryTimeQuota <Int32?>]`: Cota máxima permitida diária de tempo de memória (aplicável somente a aplicativos dinâmicos).
  - `[Enabled <Boolean?>]`: <code>true</code> se o aplicativo estiver habilitado; caso contrário, <code>false</code> . Definir esse valor como false desabilita o aplicativo (faz com que o aplicativo seja offline).
  - `[HostNameSslState <IHostNameSslState[]>]`: Os estados SSL do nome do host são usados para gerenciar as vinculações SSL para nomes de host do aplicativo.
    - `[HostType <HostType?>]`: Indica se o nome do host é um nome de host padrão ou de repositório.
    - `[Name <String>]`: Nomedo host.
    - `[SslState <SslState?>]`: Tipo SSL.
    - `[Thumbprint <String>]`: Impressão digital do certificado SSL.
    - `[ToUpdate <Boolean?>]`: De definida <code>true</code> como para atualizar o nome de host existente.
    - `[VirtualIP <String>]`: Endereço IP virtual atribuído ao nome do host se O SSL baseado em IP estiver habilitado.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> para desabilitar os nomes de host públicos do aplicativo; caso contrário, <code>false</code> .          Se <code>true</code> , o aplicativo só está acessível por meio do processo de gerenciamento de API.
  - `[HostingEnvironmentProfileId <String>]`: ID de recurso do ambiente de serviço de aplicativo.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: configura um site para aceitar apenas solicitações https. Problemas de redirecionamento para solicitações http
  - `[HyperV <Boolean?>]`: Área de ressufla do Hyper-V.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Tipo de identidade de serviço gerenciado.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: A lista de identidades atribuídas pelo usuário associadas ao recurso. As referências de chave do dicionário de identidade do usuário serão ARM ids de recurso no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[IsXenon <Boolean?>]`: Obsoleto: área de ressufla do Hyper-V.
  - `[RedundancyMode <RedundancyMode?>]`: Modo de redundância de site
  - `[Reserved <Boolean?>]`: <code>true</code> se reservado; caso contrário, <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> para interromper o site do SCM (KUDU) quando o aplicativo for interrompido; caso contrário, <code>false</code> . O padrão é <code>false</code> .
  - `[ServerFarmId <String>]`: ID de recurso do plano de Serviço de Aplicativo associado, formatado como: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## LINKS RELACIONADOS

