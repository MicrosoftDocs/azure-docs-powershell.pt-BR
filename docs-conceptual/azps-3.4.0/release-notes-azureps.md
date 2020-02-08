---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002666"
---
# <a name="azure-powershell-release-notes"></a>Notas sobre a versão do Azure PowerShell

## <a name="340---february-2020"></a>3.4.0 – fevereiro de 2020
### <a name="highlights-since-the-last-major-release"></a>Destaques desde a última versão principal
* Lançamento da versão 0.1.0 inicial do Az.CosmosDB
* Adição do suporte do ConnectionMonitor V2 do Az.Network

#### <a name="azaccounts"></a>Az.Accounts
* Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível
* Atualize a referência ao Azure Powershell Common para 1.3.5-preview

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct*** e **Set-AzApiManagementProduct**
  - Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472
* **Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet

#### <a name="azcompute"></a>Az.Compute
* Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.
* Adicionar o cmdlet Update-AzDiskEncryptionSet
* Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:
    - New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig
* Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.

#### <a name="azdatafactory"></a>Az.DataFactory
* Atualizar a versão do SDK do .NET do ADF para 4.7.0

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Adiciona operações LIST para recursos
* Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade

#### <a name="azhdinsight"></a>Az.HDInsight
* Corrija o erro de documento de New-AzHDInsightCluster.

#### <a name="azkeyvault"></a>Az.KeyVault
* Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.

#### <a name="aznetwork"></a>Az.Network
* Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.
* Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento
    - Atualizado o cmdlet New-AzFirewall:
        - Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público
        - Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'
* Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.
* Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.
* Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo
    - Novos cmdlets adicionados:
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - Atualização de cmdlets com o parâmetro opcional – UrlConfiguration
        - New-AzApplicationGatewayRewriteRuleActionSet
* Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir
    - Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation
* Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política
* Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Suporte do Azure Site Recovery para remover um disco replicado.
* O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.

#### <a name="azresources"></a>Az.Resources
* Torne -Scope opcional em cmdlets *-AzPolicyAssignment com padrão para a assinatura de contexto
* Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave

#### <a name="azsql"></a>Az.Sql
Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.

#### <a name="azstorage"></a>Az.Storage
* Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento
    - New-AzStorageAccount
* Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation
* Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState
* Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão

## <a name="330---january-2020"></a>3.3.0 – Janeiro de 2020
#### <a name="azaccounts"></a>Az.Accounts
* Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix

#### <a name="azcdn"></a>Az.Cdn
* Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint

#### <a name="azcompute"></a>Az.Compute
* Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'
  - Obter o Contêiner de armazenamento do Edge
* Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'
  - Criar Contêiner de armazenamento do Edge
* Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'
  - Remover o Contêiner de armazenamento do Edge
* Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'
  - Invocar ação para atualizar dados no Contêiner de armazenamento do Edge
* Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'
  - Obter a Conta de armazenamento do Edge
* Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'
  - Criar uma Conta de armazenamento do Edge
* Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'
  - Remover a Conta de armazenamento do Edge
* Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'
  - Invocar ação para atualizar dados no compartilhamento
* Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'
  - Definir a credencial de conta de armazenamento az databoxedge

#### <a name="azdatafactory"></a>Az.DataFactory
* Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime
* Atualizar a versão do SDK do .NET do ADF para 4.6.0
* Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md

#### <a name="azeventhub"></a>Az.EventHub
* Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace

#### <a name="azhdinsight"></a>Az.HDInsight
* Corrigir o erro Invoke-AzHDInsightHiveJob.md.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível
  - Get-AzMlOpCluster
  - Get-AzMlOpClusterKey
  - New-AzMlOpCluster
  - Remove-AzMlOpCluster
  - Set-AzMlOpCluster
  - Test-AzMlOpClusterSystemServicesUpdateAvailability
  - Update-AzMlOpClusterSystemService

#### <a name="aznetwork"></a>Az.Network
* Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.
* Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.
* Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.
* Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.

#### <a name="azresources"></a>Az.Resources
* Corrija um erro no documento de ajuda de 'Remove-AzTag'.

#### <a name="azsql"></a>Az.Sql
* Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.
* Corrija um erro ao criar um grupo de failover da instância do SQL

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Adicionar DR como um novo tipo de licença válida

#### <a name="azstorage"></a>Az.Storage
* Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura
    - Update-AzStorageAccountNetworkRuleSet
* Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats 
    - Get-AzureRMStorageAccount

## <a name="320---december-2019"></a>3.2.0 – Dezembro de 2019

### <a name="general"></a>Geral
* Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos

#### <a name="azaccounts"></a>Az.Accounts
* Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia
* Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia

#### <a name="azbatch"></a>Az.Batch
* Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.

#### <a name="azdatafactory"></a>Az.DataFactory
* Atualizar a versão do SDK do .NET do ADF para 4.5.0

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Adicionado suporte à exclusão de regras gerenciadas do WAF
* Adicionado SocketAddr para preenchimento automático

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Tratamento de exceção

#### <a name="azkeyvault"></a>Az.KeyVault
* Corrigido erro ao acessar o valor que potencialmente não está definido
* Gerenciamento de certificado de criptografia de curva elíptica
    - Adicionado suporte para especificar o KeySize para Políticas de Certificado

#### <a name="azmonitor"></a>Az.Monitor
* Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico. Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como tipo de dados dedicado)

#### <a name="aznetwork"></a>Az.Network
* Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.

#### <a name="azresources"></a>Az.Resources
* Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.
* Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.

#### <a name="azsql"></a>Az.Sql
* Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2

#### <a name="azstorage"></a>Az.Storage
* Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth
    - New-AzStorageContainerSASToken
    - New-AzStorageBlobSASToken
* Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados
    - Revoke-AzStorageAccountUserDelegationKeys
* Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.
* Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'. 
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'
    - Set-AzStorageShareQuota
* Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada
    - Set-AzStorageContainerAcl

## <a name="310---november-2019"></a>3.1.0 – Novembro de 2019
### <a name="highlights-since-the-last-major-release"></a>Destaques desde a última versão principal
* Az.DataBoxEdge 1.0.0 lançado
* Az.SqlVirtualMachine 1.0.0 lançado

#### <a name="azcompute"></a>Az.Compute
* Recurso Reapply da VM
    - Adicionar parâmetro Reapply ao cmdlet Set-AzVM
* Recurso AutomaticRepairs do conjunto de dimensionamento da VM:
    - Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss
* Suporte de imagem da galeria entre locatários para New-AzVM
* Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss
* Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk
* Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional
* Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion
* Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition
* Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Cmdlet `Get-AzDataBoxEdgeOrder` adicionado
    - Obter a ordem
* Cmdlet `New-AzDataBoxEdgeOrder` adicionado
    - Criar ordem
* Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado
    - Remover a ordem
* Alterar no cmdlet `New-AzDataBoxEdgeShare`
    - Agora cria o Compartilhamento Local
* Cmdlet `Set-AzDataBoxEdgeRole` adicionado
    - Agora IotRole pode ser mapeado para Compartilhar
* Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado
    - Invocar atualização da verificação e do download e instalar as atualizações no dispositivo
* Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado
    - Obtém as informações sobre Gatilhos
* Cmdlet `New-AzDataBoxEdgeTrigger` adicionado
    - Criar gatilhos
* Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado
    - Remover os gatilhos

#### <a name="azdatafactory"></a>Az.DataFactory
* Atualizar a versão do SDK do .NET do ADF para 4.4.0
* Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem

#### <a name="azeventhub"></a>Az.EventHub
* Correção para o problema 10301: corrigir o formato de data do Token SAS

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject
* Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject
* Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.

#### <a name="azprivatedns"></a>Az.PrivateDns
* SDK do .NET PrivateDns atualizado para a versão 1.0.0

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.
* Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.
* Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.

#### <a name="azrediscache"></a>Az.RedisCache
* Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'. Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.
* Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'

#### <a name="azresources"></a>Az.Resources
- Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.
- Exemplo de ajuda de criar definição de política atualizado
- Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.
- Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.
- Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.

#### <a name="azsql"></a>Az.Sql
* Suporte para o banco de dados ReadReplicaCount adicionado.
* Set-AzSqlDatabase corrigido quando a redundância de zona não está definida

## <a name="300---november-2019"></a>3.0.0 – novembro de 2019
### <a name="general"></a>Geral
* Az.PrivateDns 1.0.0 liberado

#### <a name="azaccounts"></a>Az.Accounts
* Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.

#### <a name="azadvisor"></a>Az.Advisor
* Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.

#### <a name="azbatch"></a>Az.Batch
* `CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`. Também há um novo `LowPriorityCoreQuota`.
  - Isso afeta o **Get-AzBatchAccount**.
* O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.
* Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos. Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.
  - Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:
    - Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.
    - Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.
* Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.
  - Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**. Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* `ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.
  - `ApplicationId` agora é um alias de `ApplicationName`.
* Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.
* `Version` renomeado para `Name` em `PSApplicationPackage`.
* `BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.
* A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.
* O **Set-AzBatchPoolOSVersion** removido. Não há mais suporte para esta operação.
* `TargetOSVersion` removido de `PSCloudServiceConfiguration`.
* `CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.
* `DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.
* O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**. 
  - **Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.
  - Novas imagens não verificadas agora também são retornadas. Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.
* Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.
* Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego. Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.
* Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote. Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.
* Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`. Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.
* Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).
* Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).

#### <a name="azcdn"></a>Az.Cdn
* UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.
* Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.

#### <a name="azcompute"></a>Az.Compute
* Recurso do Conjunto de Criptografia de Disco
    - Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile        
        Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk
    - Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig
* Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig
* Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida
* Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss
* Alterações de quebra
    - O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado
    - PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion

#### <a name="azdatafactory"></a>Az.DataFactory
* Atualizar a versão do SDK do .NET do ADF para 4.3.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções
* Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.
* Exposição da configuração por tempo limite da solicitação em adlsclient
* Correção da passagem do syncflag original para a recuperação do badoffset
* Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada
* Correção do bug Concat

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Diversos erros de digitação corrigidos no módulo

#### <a name="azhdinsight"></a>Az.HDInsight
* Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.
* Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.
* O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0
* Cinco cmdlets removidos:
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* Três cmdlets adicionados:
    - Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.
    - Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.
    - Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.
* Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.
* Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.
* Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.
* O Tipo de saída dos seguintes cmdlets foi alterado:
*  - O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.
*  - O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.
*  - O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.
* Alguns casos de teste de cenário foram adicionados.
* Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.

#### <a name="aziothub"></a>Az.IotHub
* Alterações da falha:
    - O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.
    - O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.
    - O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.
    - O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.
    - A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.
    - A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.
    - O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.
    - O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.
    - O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.
    - O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.
    - O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.
    - O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.
* Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.
* Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.
* Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.
* Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.
* Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.
* Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.
* Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.
* Recurso SoftDelete adicionado para VM e testes adicionados para softdelete

#### <a name="azresources"></a>Az.Resources
* Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2

#### <a name="aznetwork"></a>Az.Network
* Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.
    - Atualização do cmdlet:
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Set-AzPrivateEndpointConnection
* Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.
    - Novo cmdlet:
        - Get-AzPrivateLinkResource
* Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.
    - Adicionar a propriedade EnableProxyProtocol em PrivateLinkService
    - Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection
    - New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.
* Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'
* Novos cmdlets para dar suporte à política de firewall do Azure
* Adicionar suporte para o recurso filho RouteTables do VirtualHub
    - Novos cmdlets adicionados:
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan
    - Cmdlets atualizados com parâmetros opcionais:
        - New-AzVirtualHub: parâmetro SKU adicionado
        - Update-AzVirtualHub: parâmetro SKU adicionado
        - New-AzVirtualWan: parâmetro VirtualWANType adicionado
        - Update-AzVirtualWan: parâmetro VirtualWANType adicionado
* Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection
    - Novos cmdlets adicionados:
        - Update-AzureRmVirtualHubVnetConnection
    - Cmdlets atualizados com parâmetros opcionais:
        - New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado
        - New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado
        - Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado
        - New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado
        - Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado
* Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall
    - Novos cmdlets adicionados:
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - Cmdlets atualizados com parâmetros opcionais:
        - New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados
* Suporte adicionado para o operador de correspondência geográfica no CustomRule
    - GeoMatch adicionado para o operador no FirewallCondition
* Suporte adicionado para a política de Firewall perListener e perSite
    - Cmdlets atualizados com parâmetros opcionais:
        - New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados
        - New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados
* Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas
* Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure
* Adicionar suporte para os recursos de nível superior RouteTables do IpGroup
    - Novos cmdlets adicionados:
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.

#### <a name="azsql"></a>Az.Sql
* Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.
* Preterido dos cmdlets de auditoria antiga de código.
* Foram removidos os aliases preteridos:
* Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)
* Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)
* Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy
* Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos
* Substituir os cmdlets de configurações de detecção avançada de ameaças 
* Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.

#### <a name="azstorage"></a>Az.Storage
* O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle
    
## <a name="280---october-2019"></a>2.8.0 – outubro de 2019
### <a name="general"></a>Geral
* Az.HealthcareApis versão 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet
    - Correção do problema https://github.com/Azure/azure-powershell/issues/10068

#### <a name="azautomation"></a>Az.Automation
* Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux. 

#### <a name="azbatch"></a>Az.Batch
* **Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.

#### <a name="azcompute"></a>Az.Compute
* Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss
* Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey
* Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension. 
* Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.

#### <a name="azdatafactory"></a>Az.DataFactory
* Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.
* Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.
* Atualizar a versão do SDK do .NET do ADF para 4.2.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Atualização da versão do PowerShell para 1.0.0
* Atualização da versão do SDK para 1.0.2
* Atualizar em testes para referir-se à nova versão do SDK
* Atualização da estrutura de saída de aninhada para nivelada.

#### <a name="aziothub"></a>Az.IotHub
* Adicionar nova fonte de roteamento: DigitalTwinChangeEvents
* Correção de bug secundária: Get-AzIothub não está retornando subscriptionId 

#### <a name="azmonitor"></a>Az.Monitor
* Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver
* Usar esquema de alerta comum habilitado para os receptores. Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz
* Agora o Webhooks dá suporte à autenticação do Azure Active Directory.

#### <a name="aznetwork"></a>Az.Network
* Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.
* Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual
    - Novos cmdlets adicionados:
        - New-AzureRmTrafficSelectorPolicy
    - Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection
* Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede
    - Cmdlets atualizados:
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Melhorar o tratamento de exceções em cmdlets Cortex
* Novas gerações e SKUs de VirtualNetworkGateways
  - Introduzir novas gerações para VirtualNetworkGateways.
  - Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.

#### <a name="azrediscache"></a>Az.RedisCache
* Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'

#### <a name="azsql"></a>Az.Sql
* Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada

#### <a name="azstorage"></a>Az.Storage
* Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0
* Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink
    -  Get-AzRmStorageContainer
* Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando

## <a name="270---september-2019"></a>2.7.0 – Setembro de 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'
* Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência. Em vez disso, use 'Set-AzApiManagement'.

#### <a name="azautomation"></a>Az.Automation
* Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'
* Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode
* Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.

#### <a name="azcompute"></a>Az.Compute
* Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig
* Inclusão do parâmetro Incremental no New-AzSnapshotConfig
* Adicione um recurso de máquina virtual de baixa prioridade:
    - Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.
    - O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.
* Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.
* Correção da exceção nula para Get-AzRemoteDesktopFile.
* Correção do método VHD Seek para posição relativa ao final.
* Correção do problema do UltraSSD para New-AzVM e Update-AzVM.

#### <a name="azdatafactory"></a>Az.DataFactory
* Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus
* Atualização da versão do SDK do ADF .Net para 4.1.3

#### <a name="azhdinsight"></a>Az.HDInsight
* Chamar as alterações de falha

#### <a name="aziothub"></a>Az.IotHub
* Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.
* Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT. Os novos cmdlets são:
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1
   - Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores. São cmdlets somente leitura, então não haveria alteração na entrada deles.
   - A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**. Os testes de cenário foram atualizados para acomodar essa alterar.
   - Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**. No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets. **OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.
   - A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior. Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.
   - A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior. Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.
* Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2
    - New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico
    - Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico
* Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)
 - Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)
 - Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda
 - Inclusão de exemplos para o parâmetro opcional 'ActionGroup'
 - Melhoria geral nos arquivos de ajuda
* Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'

#### <a name="aznetwork"></a>Az.Network
* Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway' 
* Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote
* Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente
* Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes
* Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK
* Correção do mapeamento incorreto dos modelos de Regra de Segurança
* Inclusão de propriedades de adaptador de rede para recurso de IP privado
    - Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface
    - Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration
    - Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation
* Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure
* Compatibilidade com MultiLink na WAN Virtual
    - Novos cmdlets
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - Atualização do cmdlet:
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount
* Inclusão de testes de política de VM e restauração de conta de armazenamento original

#### <a name="azresources"></a>Az.Resources
* Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'
* Inclusão de novos cmdlets para gerenciar aplicativos e serviços:
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.

#### <a name="azsignalr"></a>Az.SignalR
* Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage

#### <a name="azsql"></a>Az.Sql
* Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'
* Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).
* Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy
* Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.
* Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).

#### <a name="azstorage"></a>Az.Storage
* Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'
* No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.
    -  Set-AzStorageBlobContent
* Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP
* Correção do Publish-AzureWebapp para funcionar no Linux e no Windows
* Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'

## <a name="260---august-2019"></a>2.6.0 – Agosto de 2019
#### <a name="general"></a>Geral
* Correção de erros de digitação diversos em vários módulos

#### <a name="azaccounts"></a>Az.Accounts
* Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)

#### <a name="azaks"></a>Az.Aks
* Corrigir problema com a saída de 'Get-AzAks'
    * Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* Correção do problema https://github.com/Azure/azure-powershell/issues/9351
    - Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId
* **Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752
* Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'

#### <a name="azbatch"></a>Az.Batch
* Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula

#### <a name="azcdn"></a>Az.Cdn
* Correção de um erro de digitação no auxiliar de conversão do módulo CDN

#### <a name="azcompute"></a>Az.Compute
* Adicionar VmssId ao cmdlet New-AzVMConfig
* Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss
* Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM
* Adicionar os recursos Host e HostGroup
    - Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM
* Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto
* Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'

#### <a name="azdatafactory"></a>Az.DataFactory
* Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'
* Atualização para a versão 4.1.2 do SDK do ADF .Net
* Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime
* Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.

#### <a name="azeventhub"></a>Az.EventHub
* Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet
* Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT
* adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace
* Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas

#### <a name="azmonitor"></a>Az.Monitor
* Correção de nomes de parâmetro incorretos na documentação de ajuda

#### <a name="aznetwork"></a>Az.Network
* Atualização de New-AzPrivateLinkServiceIpConfig
    - Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.
    - Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.
* Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave
* Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6. 
* Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.
* Atualização da descrição do parâmetro Location para AzNetworkServiceTag

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'
    - Adição de exemplo
    - Atualização da descrição do parâmetro '-Name'
* Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource
* Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'

#### <a name="azresources"></a>Az.Resources
* Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource
    - Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades
    - Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo
* Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda

#### <a name="azservicebus"></a>Az.ServiceBus
* Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet
* Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta
* Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico 

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Corrigir bugs de cmdlet do tipo de nó de adição:
    - bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric. Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681
    - Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster. corrige o problema: https://github.com/Azure/azure-powershell/issues/8407
    - Preterição do cmdlet Add-AzServiceFabricApplicationCertificate

#### <a name="azsql"></a>Az.Sql
* Atualizar a documentação dos antigos cmdlets de auditoria.

#### <a name="azstorage"></a>Az.Storage
* Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro
* Dar suporte a StandardBlobTier em blob de upload e de cópia
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Dar suporte à Prioridade de Reidratação no blob de cópia
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot

## <a name="250---july-2019"></a>2.5.0 – julho de 2019
#### <a name="azaccounts"></a>Az.Accounts
* Atualizar código comum para usar a versão mais recente do ClientRuntime

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey' 

#### <a name="azautomation"></a>Az.Automation
* Corrigir erros de digitação na cadeia de recursos 

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Suporte a NetworkRuleSet adicionado.

#### <a name="azcompute"></a>Az.Compute
* Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação
    - Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633

#### <a name="azdatafactory"></a>Az.DataFactory
* Versão do SDK do ADF .Net para 4.1.0 atualizada
* Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’

#### <a name="azeventhub"></a>Az.EventHub
* Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken
* verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído

#### <a name="azkeyvault"></a>Az.KeyVault
* Suporte adicionado para especificar o KeySize para Políticas de Certificado

#### <a name="azlogicapp"></a>Az.LogicApp
* Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa
    - Novo parâmetro MapType adicionado para filtragem

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Suporte adicionado para a versão da API 2019-06-01 (GA)

#### <a name="aznetwork"></a>Az.Network
* Adicionar suporte para ponto de extremidade e serviço de link privados
    - Novos cmdlets
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork
    - New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado
        - Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.
        - Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.
* O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores
* Habilitar protocolo ICMP para configurações de regra de segurança de rede
    - Cmdlets atualizados
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection
* Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration
    - Atualização do cmdlet:
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação
    - New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end. Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* A versão padrão atualizada para pesquisas salvas é 1. 
* Manipulação regex nula de log personalizado corrigida

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Atualizar 'Get-AzRecoveryServicesBackupJob.md'
* Atualizar 'Get-AzRecoveryServicesBackupContainer.md'
* Atualizar 'Get-AzRecoveryServicesVault.md'
* Atualizar 'Wait-AzRecoveryServicesBackupJob.md'
* Atualizar 'Set-AzRecoveryServicesVaultContext.md'
* Atualizar 'Get-AzRecoveryServicesBackupItem.md'
* Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'
* Atualizar 'Restore-AzRecoveryServicesBackupItem.md'
* Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure
* Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'

#### <a name="azresources"></a>Az.Resources
- Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'
- Cmdlets de política atualizados para usar a nova versão da api 2019-01-01

#### <a name="azservicebus"></a>Az.ServiceBus
* Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken
* verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído

#### <a name="azsql"></a>Az.Sql
* Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary
* Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email
* Corrigir um pequeno erro de digitação em uma mensagem de aviso.

#### <a name="azstorage"></a>Az.Storage
* Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto

#### <a name="azstoragesync"></a>Az.StorageSync
* Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.
* Corrigir o problema 9551 para honrar TierFilesOlderThanDays

#### <a name="azwebsites"></a>Az.Websites
* Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp
* Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp
* Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots

## <a name="240---july-2019"></a>2.4.0 – Julho de 2019
#### <a name="azaccounts"></a>Az.Accounts
* Adição de suporte para cmdlets de perfil
* Adição de suporte para ambientes e planos de dados nos cmdlets gerados
* Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell

#### <a name="azadvisor"></a>Az.Advisor
* Versão de GA do Az.Advisor
* Agora esse módulo está incluído como parte do módulo `Az` de rollup

#### <a name="azapimanagement"></a>Az.ApiManagement
* Correção do problema https://github.com/Azure/azure-powershell/issues/8671
    - **Get-AzApiManagementSubscription**
        - Adicionado suporte para consultar as assinaturas por usuário e produto
        - Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'
* Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432
    - **Import-AzApiManagementApi**
        - Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs

#### <a name="azautomation"></a>Az.Automation
* Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.

#### <a name="azcompute"></a>Az.Compute
* Adição do parâmetro HyperVGeneration ao New-AzImageConfig

#### <a name="azdatafactory"></a>Az.DataFactory
* Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.

#### <a name="azeventgrid"></a>Az.EventGrid
* Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'

#### <a name="aziothub"></a>Az.IotHub
* Adição de suporte para regenerar as chaves da política de autorização.

#### <a name="aznetwork"></a>Az.Network
* Adicionado 'RoutingPreference' às marcas de IP público
* Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Correção do problema de referência nula no Get-AzPolicyState
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Correção do comando get-policy para as VMs de IaaS

#### <a name="azresources"></a>Az.Resources
    - Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top
    - Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias
    - Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject
    - Algumas atualizações de documentos e exemplos para cmdlets do Policy

#### <a name="azservicebus"></a>Az.ServiceBus
* Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes

#### <a name="azsql"></a>Az.Sql
* Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública
* Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* Remoção das restrições de email das configurações de avaliação da vulnerabilidade

#### <a name="azstorage"></a>Az.Storage
* Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:
    -  Enable-AzStorageStaticWebsite
* Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo
* Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException
* Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Agora esse módulo está incluído como parte do módulo `Az` de rollup

## <a name="232---june-2019"></a>2.3.2 – Junho de 2019
#### <a name="azaccounts"></a>Az.Accounts
* Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983
* Correção de problema com aliases do AzureRM para cmdlets do Az
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.
* Correção de erro de digitação na documentação de referência 'New-AzVM'

#### <a name="azdns"></a>Az.Dns
* Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.

#### <a name="azeventgrid"></a>Az.EventGrid
* Atualização para usar a versão de API 2019-06-01.
* Novos cmdlets:
    - New-AzureRmEventGridDomain
        - Cria um novo Domínio na Grade de Eventos do Azure.
    - Get-AzureRmEventGridDomain
        - Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.
    - Remove-AzureRmEventGridDomain
        - Remove um Domínio da Grade de Eventos do Azure.
    - New-AzureRmEventGridDomainKey
        - Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.
    - Get-AzureRmEventGridDomainKey
        - Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.
    - New-AzureRmEventGridDomainTopic:
        - Cria um novo Tópico de Domínio da Grade de Eventos do Azure.
    - Get-AzureRmEventGridDomainTopic
        - Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual 
    - Remove-AzureRmEventGridDomainTopic:
        - Remove um Tópico de Domínio da Grade de Eventos do Azure existente.
* Cmdlets atualizados:
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:
        - Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.
        - Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.
        - Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).
        - Adição de novos parâmetros opcionais para especificar:
            - Data de validade da assinatura de evento,
            - Parâmetros de filtragem avançada.
        - Adição de nova enumeração para o servicebusqueue como destino.
        - Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por 
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:
        - Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.
    - Remove-AzureRmEventGridSubscription
        - Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.
        - Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)
* New-AzFrontDoorWafManagedRuleObject
    - Adição de novos valores de preenchimento automático

#### <a name="aznetwork"></a>Az.Network
* Adição de suporte para o recurso de gateway de rede virtual
    - Novos cmdlets
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* Adição de AvailablePrivateEndpointType
    - Novos cmdlets 
        - Get-AzAvailablePrivateEndpointType
* Adição de PrivatePrivateLinkService
    - Novos cmdlets 
        - Get-AzPrivateLinkService 
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* Adição de PrivateEndpoint
    - Novos cmdlets
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection
    - Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.
    - Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.
* Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.
* Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.
* Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit
* Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration
* Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.
* Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration
* Corrigidos cmdlets de Get do Cortex para listar todas as partes
* Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway
* Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway
* Adicionado o cmdlet Get-AzNetworkServiceTag
* Adição de suporte para vários endereços IP públicos para o Firewall do Azure
    - Atualizado o cmdlet New-AzFirewall:
        - Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público
        - Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual
        - Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada
        - Preteridos os parâmetros -PublicIpName e -VirtualNetworkName 
* Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual. 
    - New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.
    - Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.
    - Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'

#### <a name="azresources"></a>Az.Resources
* Suporte para opções adicionais de exportação de modelo
    - Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup
    - Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup
    - Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos

#### <a name="azsql"></a>Az.Sql
* Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças
* A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças
* Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento
    - New-AzStorageAccount
* Esclarecida a descrição do cmdlet de imutabilidade de blob
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente
* Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot

## <a name="220---june-2019"></a>2.2.0 – junho de 2019
#### <a name="azcdn"></a>Az.Cdn
* Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.

#### <a name="azcompute"></a>Az.Compute
* Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.
    - Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas
* Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName

#### <a name="aznetwork"></a>Az.Network
* Atualização de ResourceId e InputObject para o Gateway do NAT
    - Adição de alias a ResourceId e InputObject

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Correção do problema de referência nula em Get-AzPolicyEvent

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7

#### <a name="azservicebus"></a>Az.ServiceBus
* Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'
* Correção do caractere ausente em cmdlines do Service Fabric

#### <a name="azsql"></a>Az.Sql
* Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.
* Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy
* Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças
* Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.

#### <a name="azwebsites"></a>Az.Websites
* correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas

## <a name="210---may-2019"></a>2.1.0 – maio de 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API
    - **Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API
    - **New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API
    - **New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo
    - **New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.
    - **New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico
    - **Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API
    - **Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API
* Criação de cmdlets para gerenciar o cache no serviço ApiManagement
    - **Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches
    - **New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure
    - **Remove-AzApiManagementCache** – remover um cache
    - **Update-AzApiManagementCache** – atualizar um cache
* Criação de cmdlets para gerenciar o esquema da API
    - **New-AzApiManagementSchema** – criar um esquema para uma API
    - **Get-AzApiManagementSchema** – configurar os esquemas na API
    - **Remove-AzApiManagementSchema** – remover o esquema configurado na API
    - **Set-AzApiManagementSchema** – atualizar o esquema configurado na API
* Criação de um cmdlet para gerar um token de usuário. 
    - **New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./
* Criação de um cmdlet para recuperar o status da rede
    - **Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende. Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.
* Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement 
    - Adição de suporte para o novo SKU de 'Consumo'
    - Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'
    - O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'. Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.
    - Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.
* Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada
* Atualização do cmdlet para exibir mensagens de erro embutidas 
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]
* Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'
* Atualização do cmdlet **Import-AzApiManagementApi**
    - Para importar a API da especificação de documento 'OpenApi 3.0'
    - Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').
    - Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.
* Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'
* Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'
* Atualização do cmdlet **New-AzApiManagementApi** 
    - Para configurar a API com o servidor de autorização 'OpenId'.
    - Para criar uma API em um 'ApiVersionSet'
    - Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.
    - Capacidade de configurar 'SubscriptionRequired' no escopo da API. 
* Atualização do cmdlet **Set-AzApiManagementApi**
    - Para configurar a API com o servidor de autorização 'OpenId'.
    - Para atualizar uma API em um 'ApiVersionSet'    
    - Capacidade de configurar 'SubscriptionRequired' no escopo da API. 
* Atualização do cmdlet **New-AzApiManagementRevision**
    - Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'. A nova revisão pressupõe o uso da 'ApiId' do pai.
    - Para fornecer um 'ApiRevisionDescription'
    - Para substituir a 'ServiceUrl' ao clonar uma API.
* Atualização do cmdlet **New-AzApiManagementIdentityProvider**
    - Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'
    - Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'
* Atualização do cmdlet **New-AzApiManagementSubscription**
    - Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'
    - Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'
    - Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.
* Atualização do cmdlet **Set-AzApiManagementSubscription**
    - Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'
    - Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'
    - Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.
* Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada
    - 'New-AzApiManagementContext'
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - 'Get-AzApiManagementApiRelease'
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - 'Get-AzApiManagementApiVersionSet'
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - 'Get-AzApiManagementAuthorizationServer'
    - 'Get-AzApiManagementBackend'
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - 'Get-AzApiManagementCertificate' 
    - 'Remove-AzApiManagementApiVersionSet'
    - 'Remove-AzApiManagementSubscription'

#### <a name="azautomation"></a>Az.Automation
* Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.
    - Correção do problema https://github.com/Azure/azure-powershell/issues/7977
    - Correção do problema https://github.com/Azure/azure-powershell/issues/8600
* Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.
    * Correção do problema https://github.com/Azure/azure-powershell/issues/8347
* Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós. Agora, ele retorna somente o nó correspondente.

#### <a name="azcompute"></a>Az.Compute
* Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.
* O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure

#### <a name="azmonitor"></a>Az.Monitor
* Correção de nomes de parâmetro incorretos nos exemplos da Ajuda

#### <a name="aznetwork"></a>Az.Network
* Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas
    - Atualização do cmdlet:
        - Get-AzEffectiveRouteTable
* Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate

#### <a name="azresources"></a>Az.Resources
* Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação

#### <a name="azsql"></a>Az.Sql
* Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão

## <a name="200---may-2019"></a>2.0.0 - maio de 2019
#### <a name="azaccounts"></a>Az.Accounts
* Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.
* Corrija o erro quando falha a criação da conta.

#### <a name="azcompute"></a>Az.Compute
* Recurso de grupo de posicionamento de proximidade.
    - Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.
* O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.
* O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss       
* Alterações de quebra
    - Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.
    - Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure

#### <a name="azdns"></a>Az.Dns
* Delegação automática de NameServer do DNS
    - Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.
    - Adicione os registros NS na zona pai para a zona filho recém-criada.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Primeira versão disponível dos cmdlets FrontDoor do Azure
* Renomear os cmdlets do WAF para incluir 'Waf'
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* Removidos os dois cmdlets:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess
* Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:
    - Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.
    - Os usuários com função de operador do HDInsight não serão afetados.

#### <a name="azmonitor"></a>Az.Monitor
* Novos cmdlets para a API SQR (Regra de Consulta Agendada)  
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - [Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR
    - Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)

#### <a name="aznetwork"></a>Az.Network
* Adicionar suporte para o recurso de Gateway Nat
    - Novos cmdlets
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Cmdlets atualizados
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.
    - New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.
    - Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Suporte para consultar detalhes da avaliação de política.
    - Adicione o parâmetro '-Expand' ao Get-AzPolicyState. Suporte a '-Expand PolicyEvaluationDetails'.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Suporte para Assinatura cruzada do Azure do Azure Site Recovery.
* Marcação das alterações de falhas futuras para o Azure Site Recovery.
* Correção de plano de ação final do plano de recuperação do Azure Site Recovery.
* Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.
* Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.
* Outras correções secundárias.

#### <a name="azrelay"></a>Az.Relay
* Corrigir erros de digitação nas mensagens voltadas ao cliente

#### <a name="azservicebus"></a>Az.ServiceBus
* Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace

#### <a name="azstorage"></a>Az.Storage
* Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')
* Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.
* O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'
    - New-AzStorageAccount
* Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp
* Get-AzWebApp*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos

## <a name="180---april-2019"></a>1.8.0 – abril de 2019
### <a name="highlights-since-the-last-major-release"></a>Destaques desde a última versão principal
* Disponibilidade geral do módulo `Az`
* Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce
* Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network
* Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1
* Suporte adicionado para runbooks do Python 2 em Az.Automation
* Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote

#### <a name="azaccounts"></a>Az.Accounts
* Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac

#### <a name="azbatch"></a>Az.Batch
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azcdn"></a>Az.Cdn
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azcompute"></a>Az.Compute
* Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.
* Corrigir a documentação para caracteres curinga

#### <a name="azdatafactory"></a>Az.DataFactory
* Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azeventgrid"></a>Az.EventGrid
* Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.

#### <a name="azeventhub"></a>Az.EventHub
* Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace 

#### <a name="azhdinsight"></a>Az.HDInsight
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="aziothub"></a>Az.IotHub
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azkeyvault"></a>Az.KeyVault
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.
* Corrigir a documentação para caracteres curinga

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azmedia"></a>Az.Media
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azmonitor"></a>Az.Monitor
  * Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * SDK do Monitor atualizado para versão 0.22.0-preview

#### <a name="aznetwork"></a>Az.Network
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.
* Corrigir a documentação para caracteres curinga

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.
* Formato de tabela atualizado para SQL na VM do Azure
* Método alternativo adicionado para buscar o local no AzureFileShare
* ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário

#### <a name="azrediscache"></a>Az.RedisCache
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.

#### <a name="azresources"></a>Az.Resources
* Corrigir a documentação para caracteres curinga

#### <a name="azsql"></a>Az.Sql
* Substituir a dependência no SDK do Monitor por código comum
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.
* Processo de classificação de várias colunas aprimorado.
* Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.
* Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.
* Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.
* Corrigir a documentação para caracteres curinga

#### <a name="azwebsites"></a>Az.Websites
* Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução
* Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.
* Atualizado o SDK de Sites.
* Removida a propriedade AdminSiteName de PSAppServicePlan.

## <a name="170---april-2019"></a>1.7.0 - abril de 2019
### <a name="highlights-since-the-last-major-release"></a>Destaques desde a última versão principal
* Disponibilidade geral do módulo `Az`
* Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce
* Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network
* Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1
* Suporte adicionado para runbooks do Python 2 em Az.Automation
* Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote

#### <a name="azaccounts"></a>Az.Accounts
* Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original
* Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha

#### <a name="azautomation"></a>Az.Automation
* Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões. Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.
* Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure

#### <a name="azcompute"></a>Az.Compute
* Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig
* Permitir a criação de VM com a imagem da galeria de outros locatários. 

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita

#### <a name="azdatafactory"></a>Az.DataFactory
* Atualizada a versão do SDK do ADF .NET para 3.0.2
* Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.

#### <a name="azresources"></a>Az.Resources
* Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”
* Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'
    - Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856
* Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* Classificação de Dados no Banco de Dados de Suporte.

#### <a name="azstorage"></a>Az.Storage
* Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure
    - New-AzStorageContext
* Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 - março de 2019
### <a name="highlights-since-the-last-major-release"></a>Destaques desde a última versão principal
* Disponibilidade geral do módulo `Az`
* Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce
* Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network
* Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1
* Suporte adicionado para runbooks do Python 2 em Az.Automation
* Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote

#### <a name="azautomation"></a>Az.Automation
* Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:
    * Agrupamento dinâmico
    * Script de pré-publicação
    * Configuração da Reinicialização

#### <a name="azcompute"></a>Az.Compute
* Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData
* Atualize a biblioteca de clientes de Computação para 25.0.0.

#### <a name="azkeyvault"></a>Az.KeyVault
* Suporte a caracteres curinga adicionado aos cmdlets do KeyVault

#### <a name="aznetwork"></a>Az.Network
* Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure
* Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo
* Suporte do pipe adicionado para cancelar o registro do contêiner

#### <a name="azresources"></a>Az.Resources
* Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup
* Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM

#### <a name="azsql"></a>Az.Sql
* parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.

#### <a name="azstorage"></a>Az.Storage
* Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots” 

## <a name="150---march-2019"></a>1.5.0 - março de 2019
#### <a name="azaccounts"></a>Az.Accounts
* Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest
* Exemplos de atualização para Connect-AzAccount

#### <a name="azautomation"></a>Az.Automation
* Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure
* Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós. Agora ele retorna todos os nós

#### <a name="azcdn"></a>Az.Cdn
* Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos

#### <a name="azcompute"></a>Az.Compute
* Adicionar suporte de caracteres curinga aos cmdlets Get

#### <a name="azdatafactory"></a>Az.DataFactory
* Versão SDK do ADF .Net atualizada para 3.0.1

#### <a name="azlogicapp"></a>Az.LogicApp
* Correção para ListWorkflows recuperando apenas a primeira página de resultados

#### <a name="aznetwork"></a>Az.Network
* Adicionar suporte de caracteres curinga aos cmdlets Network

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* SQL Server adicionado no suporte de VM do Azure
* Atualização do SDK
* Verificação do VMappContainer removida no Get-ProtectableItem
* Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem

#### <a name="azresources"></a>Az.Resources
* Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933
* Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240
* Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* Atualizando AuditingEndpointsCommunicator.
    - Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.

#### <a name="azstorage"></a>Az.Storage
* Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 – Fevereiro de 2019
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Preterimento do cmdlet AddAzureASAccount

#### <a name="azautomation"></a>Az.Automation
* Atualização da ajuda para Import-AzAutomationDscNodeConfiguration
* Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration
* Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.

#### <a name="azcompute"></a>Az.Compute
* Correção do problema com conjuntos de parâmetros de ID
* Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido
* Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage
* Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados

#### <a name="azeventhub"></a>Az.EventHub
* Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub 

#### <a name="azkeyvault"></a>Az.KeyVault
* Correção da marcação em Set-AzKeyVaultSecret

#### <a name="azlogicapp"></a>Az.LogicApp
* Adição de SKU básico para contas de integração
* Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map
* Novos cmdlets para assemblies de conta de integração
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* Novos cmdlets para configuração de lote da conta de integração
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* Atualização do SDK de aplicativo lógico da versão 4.1.0

#### <a name="azmonitor"></a>Az.Monitor
* Atualização da ajuda para Get-AzMetric

#### <a name="aznetwork"></a>Az.Network
* Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Suporte adicional para fonte de dados do ApplicationInsights Get e New.
    - Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado. 
    - Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name. 

#### <a name="azresources"></a>Az.Resources
* Correção do problema https://github.com/Azure/azure-powershell/issues/8166
* Correção do problema https://github.com/Azure/azure-powershell/issues/8235
* Correção do problema https://github.com/Azure/azure-powershell/issues/6219
* Correção de bug que impede a criação repetida de KeyCredentials

#### <a name="azsql"></a>Az.Sql
* Adição de suporte para a camada de Hiperescala do banco de dados SQL
* Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração

#### <a name="azwebsites"></a>Az.Websites
* Correção do exemplo em Get-AzWebAppSlotMetrics

## <a name="130---february-2019"></a>1.3.0 – Fevereiro de 2019
#### <a name="azaccounts"></a>Az.Accounts
* Atualização para a versão mais recente do ClientRuntime

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Disponibilidade geral do módulo Az.AnalysisServices.

#### <a name="azcompute"></a>Az.Compute
* Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80
* Atualização da descrição da ajuda para Set-AzVMBootDiagnostics
* Atualização da descrição de ajuda e do exemplo para Update-AzImage

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Disponibilidade geral do módulo Az.RecoveryServices.

#### <a name="azresources"></a>Az.Resources
* Correção da marcação dos grupos de recursos 
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166
* Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction 
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy
* Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL
* Correção da exceção de referência nula em Get-AzSqlCapability

## <a name="121---january-2019"></a>1.2.1 – Janeiro de 2019
#### <a name="azaccounts"></a>Az.Accounts
* Versão com a versão correta de autenticação

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Versão com a dependência de autenticação atualizada

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Versão com a dependência de autenticação atualizada

## <a name="120---january-2019"></a>1.2.0 – Janeiro de 2019
#### <a name="azaccounts"></a>Az.Accounts
* Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1
* Atualização de URLs incorretas da ajuda online
* Adição de mensagem de aviso no PS Core para Uninstall-AzureRm

#### <a name="azaks"></a>Az.Aks
* Atualização de URLs incorretas da ajuda online

#### <a name="azautomation"></a>Az.Automation
* Adicionado suporte aos runbooks do Python 2
* Atualização de URLs incorretas da ajuda online

#### <a name="azcdn"></a>Az.Cdn
* Atualização de URLs incorretas da ajuda online

#### <a name="azcompute"></a>Az.Compute
* Adição do cmdlet Invoke-AzVMReimage
* Adição do parâmetro TempDisk ao Set-AzVmss
* Correção da mensagem de aviso do New-AzVM

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Atualização de URLs incorretas da ajuda online

#### <a name="azdatafactory"></a>Az.DataFactory
* Atualizada a versão do SDK do ADF .NET para 3.0.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Correção do problema com o ponto de extremidade do ADLS ao usar o MSI
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462
* Atualização de URLs incorretas da ajuda online

#### <a name="aziothub"></a>Az.IotHub
* Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.

#### <a name="azkeyvault"></a>Az.KeyVault
* Atualização de URLs incorretas da ajuda online

#### <a name="aznetwork"></a>Az.Network
* Atualização de URLs incorretas da ajuda online

#### <a name="azresources"></a>Az.Resources
* Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'
* Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos
* Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode
* Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522
* Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747
* Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932
* Correção de mensagens de erro.
* Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.
* Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.

#### <a name="azsignalr"></a>Az.SignalR
* Atualização de URLs incorretas da ajuda online

#### <a name="azsql"></a>Az.Sql
* Atualização de URLs incorretas da ajuda online
* Atualizada a descrição do parâmetro LicenseType com os valores possíveis
* Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada
* Suporte para ordenação personalizada em instâncias gerenciadas

#### <a name="azstorage"></a>Az.Storage
* Atualização de URLs incorretas da ajuda online
* Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Atualização de URLs incorretas da ajuda online

#### <a name="azwebsites"></a>Az.Websites
* Atualização de URLs incorretas da ajuda online
* Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.
* Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo

## <a name="110---january-2019"></a>1.1.0 – Janeiro de 2019
#### <a name="azaccounts"></a>Az.Accounts
* Adição de escopo 'Local' ao Enable-AzureRmAlias

#### <a name="azcompute"></a>Az.Compute
* Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage
* Atualização da descrição de ID em arquivos de ajuda
* Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.
    - Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono

#### <a name="azeventgrid"></a>Az.EventGrid
* Atualização para usar a versão de API 2019-01-01.
* Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01
    - New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:
        - Evento Vida útil
        - Número máximo de tentativas de entrega para os eventos
        - Ponto de extremidade de mensagens mortas
    - Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:
        - Evento Vida útil
        - Número máximo de tentativas de entrega para os eventos
        - Ponto de extremidade de mensagens mortas
* Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.
* A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.

#### <a name="aziothub"></a>Az.IotHub
* Atualizado para a versão mais recente do SDK do IotHub

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzLogicApp lista tudo sem especificação de nome

#### <a name="azresources"></a>Az.Resources
* Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875
* Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition
* Correção do erro de digitação na documentação de New-AzDeployment
* Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'
    - Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts

#### <a name="azsql"></a>Az.Sql
* Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.

#### <a name="azstorage"></a>Az.Storage
* Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous
    - New-AzStorageContext
* Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* Correção de um bug de análise de data no 'Get-AzDeletedWebApp'
* Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts

## <a name="100---december-2018"></a>1.0.0 - Dezembro de 2018
### <a name="general"></a>Geral

- Disponibilidade geral do Módulo Az
- Ajuda online para cada módulo
- Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)
- Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM

### <a name="azaccounts"></a>Az.Accounts
- Alterado de Az.Profile
- Corrigidos os formatos de tabela para tipos de perfil e contexto

### <a name="azapimanagement"></a>Az.ApiManagement
- Correções para #7002
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azbatch"></a>Az.Batch
- Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.
- O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azbilling"></a>Az.Billing
- Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azcognitivservices"></a>Az.CognitivServices
- Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount
- Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- Adicionado suporte para ManagedIdentity

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azmonitor"></a>Az.Monitor
- Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azkeyvault"></a>Az.KeyVault
- Removida a propriedade “PurgeDisabled” preterida dos tipos de saída

### <a name="azmachinelearning"></a>Az.MachineLearning
- Incluídos os cmdlets do módulo Az.MachineLearningCompute

### <a name="azmedia"></a>Az.Media
- Removido o alias -Tags de New-AzMediaService

### <a name="aznetwork"></a>Az.Network
Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo
    - Novos cmdlets adicionados:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.
    - Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azprofile"></a>Az.Profile
- Nome do módulo alterado para Az.Accounts

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azresources"></a>Az.Resources
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azservicefabric"></a>Az.ServiceFabric
- Suporte para especificação de certificado pelo nome comum e impressão digital
- Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azsignalr"></a>Az.SIgnalR
- Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR

### <a name="azsql"></a>Az.Sql
- Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças
- Exemplos de documentação atualizados para cmdlets de auditoria do SQL
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azstorage"></a>Az.Storage
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

### <a name="azwebsites"></a>Az.Websites
- Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes

## <a name="070---december-2018"></a>0.7.0 - Dezembro de 2018

### <a name="general"></a>Geral

* Pequenas alterações para a futura transição de AzureRM para Az

### <a name="azcompute"></a>Az.Compute

* Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Corrigida a barra à direita do domínio da conta do ADLS

### <a name="azfrontdoor"></a>Az.FrontDoor

* Corrigidos alguns links desfeitos
    - Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.
    - No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.
* Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.

### <a name="azresources"></a>Az.Resources

* Correção para https://github.com/Azure/azure-powershell/issues/7679
    - Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.

### <a name="azsql"></a>Az.Sql

* Pequenas alterações para a futura transição de AzureRM para Az
* Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet
* Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.

### <a name="azstorage"></a>Az.Storage

* Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount
* Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext
    - Start-AzureStorageFileCopy
* Suporte para a Configuração do Site Estático
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp e Set-AzureRmWebAppSlot 
    - Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux. Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.

## <a name="061---november-2018"></a>0.6.1 - Novembro de 2018

### <a name="azapimanagement"></a>Az.ApiManagement
* Atualizar as dependências para o problema de mapeamento do tipo

### <a name="azautomation"></a>Az.Automation
* Cmdlets de Automação do Azure baseados no Swagger
* Cmdlets de Gerenciamento de Atualizações Adicionados
* Cmdlets de Controle do Código-fonte adicionados
* Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado
* Corrigido o comando de Nó do Registro de DSC

### <a name="azcompute"></a>Az.Compute
* Problema de identidade corrigido para a identidade SystemAssigned
* Atualizar as dependências para o problema de mapeamento do tipo

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Atualizar as dependências para o problema de mapeamento do tipo

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* atualizar a descrição de exemplos dos cmdlets do marketplace

### <a name="aznetwork"></a>Az.Network
* Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados
* ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte
* Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta. 
* Corrigir problemas com o uso da memória no mapa VirtualNetwork

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Corrigir para modificar a política para um compartilhamento de arquivos protegido.
* Fuso horário da política convertido em letras maiúsculas.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem
* Atualizar as dependências para o problema de mapeamento do tipo

### <a name="azrelay"></a>Az.Relay
* Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.

### <a name="azresources"></a>Az.Resources
* Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`
* Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata
* Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703

### <a name="azservicefabric"></a>Az.ServiceFabric
* Adicionar mensagens preteridas para futuras alterações da falha

### <a name="azsql"></a>Az.Sql
* Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.
    - Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.
    - Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento

## <a name="050---november-2018"></a>0.5.0 - Novembro de 2018
#### <a name="general"></a>Geral
* Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente

#### <a name="azprofile"></a>Az.Profile
* Atualizar código comum para usar a versão mais recente do ClientRuntime
* Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId
* Atualizada a descrição de TenantId atualizada para Connect-AzAccount
* Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário
    - https://github.com/Azure/azure-powershell/issues/6936
* Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário
    - https://github.com/Azure/azure-powershell/issues/7453
* Corrigir o problema com pontos de extremidade DataLake ao usar o MSI
    - https://github.com/Azure/azure-powershell/issues/7462
* Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Adicionada a operação Get-AzCognitiveServicesAccountSkus.

#### <a name="azcompute"></a>Az.Compute
* Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk
* Get-AzVMImage mostra AutomaticOSUpgradeProperties
* Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Atualizar o pacote de DataLake para 1.1.10.
* Adicionar o padrão de Simultaneidade às operações multi-threaded.

#### <a name="azinsights"></a>Az.Insights
* Correção do problema #7267 (área de dimensionamento automático)
    - Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).
* Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração
    - Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado

#### <a name="aznetwork"></a>Az.Network
* Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Adicionados cmdlets de correção de política

#### <a name="azresources"></a>Az.Resources
* Correção para https://github.com/Azure/azure-powershell/issues/7402
    - Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”

#### <a name="azservicebus"></a>Az.ServiceBus
* Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correção do certificado de adição para Vmss do Linux.
* Corrigido “Add-AzServiceFabricClusterCertificate”
    - Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).
    - Exibir exceções corretamente (Azure/service-fabric-issues#1054).
* Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.

## <a name="040---october-2018"></a>0.4.0 - Outubro de 2018
#### <a name="azprofile"></a>Az.Profile
* Corrigido o problema com Get-AzSubscription no CloudShell
* Atualizar código comum para usar a versão mais recente do ClientRuntime

#### <a name="azcompute"></a>Az.Compute
* Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”
* Adicionado o finalizador do argumento ResourceName para todos os cmdlets.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Adicionar suporte às Regras da Rede Virtual
    - Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.
    - Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.
    - Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.
    - Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.

#### <a name="aznetwork"></a>Az.Network
* Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.
* Adicionado o finalizador do argumento ResourceName para todos os cmdlets.

#### <a name="azresources"></a>Az.Resources
* Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário. Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.

## <a name="030---october-2018"></a>0.3.0 - Outubro de 2018
#### <a name="azurestorage"></a>Azure.Storage
* Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.
    - Get-AzStorageUsage
    
#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.

#### <a name="azcompute"></a>Az.Compute
* Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário
* Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.
* Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* Atualizada a versão do SDK do ADF .NET para 2.3.0.

#### <a name="aznetwork"></a>Az.Network
* Adicionada a funcionalidade NetworkProfile. Novos cmdlets adicionados
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Link de associação de serviço adicionado no modelo de sub-rede
* Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap
* Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig

#### <a name="azrediscache"></a>Az.RedisCache
* Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante. Adição do P5 na pop-up PSArgumentCompleter

#### <a name="azresources"></a>Az.Resources
* Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition
* Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário

#### <a name="azsql"></a>Az.Sql
* Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure

#### <a name="azwebsites"></a>Az.Websites
* Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner
* Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows

## <a name="020---september-2018"></a>0.2.0 - Setembro de 2018
 Versão inicial
