---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.openlocfilehash: d8a891673df343551cbd805016c2d25ee4e31c8c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

## <a name="20170925---version-440"></a>2017.09.25 - Versão 4.4.0
* AnalysisServices
  * Adicionado um novo cmdlet de plano de dados para permitir a sincronização dos bancos de dados da instância de leitura-gravação para instâncias de somente leitura
    - Arquivo de ajuda incluído para o cmdlet
    - Adicionados testes na memória e um cenário de teste (somente dinâmico)
  * Corrigidos os bugs no cmdlet Add-AzureAsAccount
* Automação
  * Corrigidos os documentos de ajuda para cmdlets corrigidos na versão anterior.
  * Adicionados 4 novos cmdlets para prestar suporte à distribuição em etapas das configurações de nó DSC.
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * Integrar ao SDK de Gerenciamento dos Serviços Cognitivos versão 2.0.0.
  * Get-AzureRmCognitiveServicesAccount agora pode dar suporte corretamente à paginação.
* Computação
  * Recurso Executar Comando:
    - Novo cmdlet: 'Invoke-AzureRmVMRunCommand' invoca um comando de execução em uma máquina virtual
    - Novo cmdlet: 'Get-AzureRmVMRunCommandDocument' mostra os documentos de comando de execução disponíveis
  * Adicionar o parâmetro 'StorageAccountType' ao cmdlet Set-AzureRmDataDisk
  * Suporte à Zona de Disponibilidade da máquina virtual, o conjunto de dimensionamento da VM, e ao disco
    - Novo parâmetro: 'Zone' adicionado aos cmdlets New-AzureRmVM, New-AzureRmVMConfig, New-AzureRmVmssConfig, New-AzureRmDiskConfig
  * Recurso de atualização sem interrupção do conjunto de dimensionamento da VM:
    - Novo cmdlet: 'Start-AzureRmVmssRollingOSUpgrade' invoca a atualização sem interrupção do sistema operacional do conjunto de dimensionamento da VM
    - Novo cmdlet: 'Set-AzureRmVmssRollingUpgradePolicy' define a política para atualização sem interrupção do conjunto de dimensionamento da VM.
    - Novo cmdlet: 'Stop-AzureRmVmssRollingUpgrade' cancela a atualização sem interrupção do conjunto de dimensionamento da VM
    - Novo cmdlet: 'Get-AzureRmVmssRollingUpgrade' mostra o status da atualização sem interrupção do conjunto de dimensionamento da VM.
  * O parâmetro de opção AssignIdentity é introduzido para identidade atribuída do sistema.
    - Novo parâmetro: 'AssignIdentity' é adicionado aos cmdlets New-AzureRmVMConfig, New-AzureRmVmssConfig e Update-AzureRmVM
  * Recurso de criptografia de disco Vmss:
    - Novo cmdlet: 'Set-AzureRmVmssDiskEncryptionExtension' permite a criptografia de disco no conjunto de dimensionamento da VM
    - Novo cmdlet: 'Disable-AzureRmVmssDiskEncryption' desativa a criptografia de disco no conjunto de dimensionamento da VM
    - Novo cmdlet: 'Get-AzureRmVmssDiskEncryptionStatus' mostra o status da criptografia de disco de um conjunto de dimensionamento da VM
    - Novo cmdlet: 'Get-AzureRmVmssVMDiskEncryptionStatus' mostra o status da criptografia de disco das VMs de um conjunto de dimensionamento da VM
* ContainerInstance
  * Adicionar cmdlets do PowerShell à Instância de Contêiner do Azure
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* Insights
  * Novo cmdlet Disable-AzureRmActivityLogAlert
    - Um novo cmdlet para desabilitar um alerta de log de atividades existente.
    - Opcionalmente, as Marcas também são configuráveis com esse cmdlet.
  * Novo cmdlet Enable-AzureRmActivityLogAlert
    - Um novo cmdlet para habilitar um alerta de log de atividades existente.
    - Opcionalmente, as Marcas também são configuráveis com esse cmdlet.
  * Novo cmdlet Get-AzureRmActivityLogAlert
    - Um novo cmdlet para recuperar um ou mais alertas de log de atividades.
    - Os alertas podem ser recuperados por nome, grupo de recursos ou assinatura.
  * Novo cmdlet New-AzureRmActionGroup
    - Um novo cmdlet para criar um objeto de ActionGroup na memória (nenhuma solicitação envolvida).
  * Novo cmdlet New-AzureRmActivityLogAlertCondition
    - Um novo cmdlet para criar um objeto de condição de folha do alerta de log de atividades na memória (nenhuma solicitação envolvida).
  * Novo cmdlet Set-AzureRmActivityLogAlert
    - Um novo cmdlet para criar ou atualizar um alerta do log de atividades.
  * Novo cmdlet Remove-AzureRmActivityLogAlert
    - Um novo cmdlet para remover um alerta do log de atividades.
  * Novo cmdlet Set-AzureRmActionGroup
    - Um novo cmdlet para criar um novo ou atualizar um grupo de ação existente.
  * Novo cmdlet Get-AzureRmActionGroup
    - Um novo cmdlet para recuperar um ou mais grupos de ação.
    - Os grupos de ação podem ser recuperados por nome, grupo de recursos ou assinatura.
  * Novo cmdlet Remove-AzureRmActionGroup
    - Um novo cmdlet para remover um grupo de ação.
  * Novo cmdlet New-AzureRmActionGroupReceiver
    - Um novo cmdlet para criar um novo receptor do grupo de ação na memória.
* KeyVault
  * Cmdlets novos/atualizados para dar suporte à exclusão temporária para certificados de KeyVault
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* Rede
  * Adicionado suporte para serviços de ponto de extremidade às sub-redes de rede virtual
    - Atualizado o cmdlet Add-AzureRmVirtualSubnetConfig: Adicionado o parâmetro opcional -ServiceEndpoint
    - Atualizado o cmdlet New-AzureRmVirtualSubnetConfig: Adicionado o parâmetro opcional -ServiceEndpoint
    - Atualizado o cmdlet Set-AzureRmVirtualSubnetConfig: Adicionado o parâmetro opcional -ServiceEndpoint
  * Adicionado o cmdlet para listar os serviços do ponto de extremidade disponíveis no local
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * Adicionada a capacidade de configurar a autenticação P2S baseada em RADIUS externa para os seguintes commandlets
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * Adicionado o cmdlet para permitir a geração de VpnProfiles para P2S baseada em RADIUS externo
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * Adicionado suporte para o parâmetro SKU de endereços IP públicos e Balanceadores de Carga
    - Atualizado o cmdlet New-AzureRMLoadBalancer: Adicionado o parâmetro opcional -Sku
    - Atualizado o cmdlet New-AzureRMPublicIpAddress: Adicionado o parâmetro opcional -Sku
  * Adicionado suporte para DisableOutboundSNAT para as Regras do Balanceador de Cargas
    - Atualizado o cmdlet New-AzureRMLoadBalancerRuleConfig: Adicionado o parâmetro opcional DisableOutboundSNAT
    - Atualizado o cmdlet Add-AzureRMLoadBalancerRuleConfig: Adicionado o parâmetro opcional DisableOutboundSNAT
    - Atualizado o cmdlet Set-AzureRMLoadBalancerRuleConfig: Adicionado o parâmetro opcional DisableOutboundSNAT
  * Adicionado suporte para IkeV2 P2S
    - Atualizado o cmdlet New-AzureRmVirtualNetworkGateway: Adicionado o parâmetro opcional -VpnClientProtocol, o padrão é [ "SSTP", "IkeV2" ]
    - Atualizado o cmdlet Set-AzureRmVirtualNetworkGateway: Adicionado o parâmetro opcional -VpnClientProtocol
  * Adicionado suporte às Regras de Segurança de Rede e Regras de Segurança de Rede Efetivas para regras MultiValued
    - Atualizado o Add-AzureRmNetworkSecurityRuleConfig: atualizados os parâmetros SourcePortRange, DestinationPortRange, SourceAddressPrefix para aceitar uma lista de cadeias de caracteres
    - Atualizado o New-AzureRmNetworkSecurityRuleConfig: atualizados os parâmetros SourcePortRange, DestinationPortRange, SourceAddressPrefix para aceitar uma lista de cadeias de caracteres
    - Atualizado o Set-AzureRmNetworkSecurityRuleConfig: Atualizados os parâmetros SourcePortRange, DestinationPortRange, SourceAddressPrefix para aceitar uma lista de cadeias de caracteres
    - Atualizado o Add-AzureRmNetworkSecurityRuleConfig: atualizados os parâmetros SourcePortRange, DestinationPortRange, SourceAddressPrefix para aceitar uma lista de cadeias de caracteres
    - Atualizado o cmdlet New-AzureRmNetworkSecurityGroup : atualizados os parâmetros SecurityRules parameter to accept SourcePortRange, DestinationPortRange, SourceAddressPrefix que são uma lista de cadeia de caracteres no objeto PSSecurityRule
    - Atualizado o cmdlet Get-AzureRmEffectiveNetworkSecurityGroup: Adicionado o parâmetro TagMap
    - Atualizado o Get-AzureRmEffectiveNetworkSecurityGroup: atualizado o objeto PSEffectiveSecurityRule retornado com os parâmetros SourcePortRange, DestinationPortRange, SourceAddressPrefix que são uma lista de cadeia de caracteres.
  * Adicionado suporte para proteção contra DDoS para redes virtuais
    - Adicionado o cmdlet New-AzureRmVirtualNetwork: Adicionados os parâmetros de opção EnableDDoSProtection e EnableVmProtection
    - Adicionadas as propriedades EnableDDoSProtection e EnableVmProtection no objeto PSVirtualNetwork
  * Adicionado suporte ao Balanceador de Carga Interno Altamente Disponível
    - Atualizado o cmdlet Add-AzureRmLoadBalancerRuleConfig: Adicionado All como um valor aceitável para o parâmetro Protocol
    - Atualizado o cmdlet New-AzureRmLoadBalancerRuleConfig: Adicionado All como um valor aceitável para o parâmetro Protocol
    - Atualizado o cmdlet Set-AzureRmLoadBalancerRuleConfig: Adicionado All como um valor aceitável para o parâmetro Protocol
  * Adicionado suporte aos Grupos de Segurança do Aplicativo
    - Adicionado o cmdlet New-AzureRmApplicationSecurityGroup
    - Adicionado o cmdlet Get-AzureRmApplicationSecurityGroup
    - Adicionado o cmdlet Remove-AzureRmApplicationSecurityGroup
    - Atualizado o cmdlet New-AzureRmNetworkInterface: Adicionados os parâmetros opcionais ApplicationSecurityGroup e ApplicationSecurityGroupId
    - Atualizado o cmdlet New-AzureRmNetworkInterfaceIpConfig: Adicionados os parâmetros opcionais ApplicationSecurityGroup e ApplicationSecurityGroupId
    - Atualizado o cmdlet Add-AzureRmNetworkInterfaceIpConfig: Adicionados os parâmetros opcionais ApplicationSecurityGroup e ApplicationSecurityGroupId
    - Atualizado o cmdlet Set-AzureRmNetworkInterfaceIpConfig: Adicionados os parâmetros opcionais ApplicationSecurityGroup e ApplicationSecurityGroupId
    - Atualizado o cmdlet New-AzureRmNetworkSecurityRuleConfig: Adicionados os parâmetros opcionais SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup e DestinationApplicationSecurityGroupId
    - Atualizado o cmdlet Add-AzureRmNetworkSecurityRuleConfig: Adicionados os parâmetros opcionais SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup e DestinationApplicationSecurityGroupId
    - Atualizado o cmdlet Set-AzureRmNetworkSecurityRuleConfig: Adicionados os parâmetros opcionais SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup e DestinationApplicationSecurityGroupId
  * Adicionado novos comandos para scripts de VpnDeviceConfiguration
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* Perfil
  * Suporte de Start-Job para cmdlets AzureRm.
    * Todos os AzureRmCmdlets adicionam o parâmetro -AzureRmContext, que pode aceitar um contexto (a saída de um cmdlet Context).
      - Padrão comum para trabalhos com a persistência de contexto DESABILITADA:`Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - Padrão comum para trabalhos com a persistência de contexto HABILITADA:`Start-Job {New-AzureRmVM [... other parameters]}`
  * Persistência das informações de logon nas sessões, novos cmdlets:
    - Enable-AzureRmContextAutosave - Habilita a persistência de logon nas sessões.
    - Disable-AzureRmContextAutosave - Desabilita a persistência de logon nas sessões.
  * Gerenciar informações de contexto, novos cmdlets
    - Select-AzureRmContext - Seleciona o contexto nomeado ativo.
    - Rename-AzureRmContext - Renomeia um contexto existente para facilitar a referência.
    - Remove-AzureRmContext - Remove um contexto existente.
    - Remove-AzureRmAccount - Remove todas as credenciais, assinaturas e locatários associados a uma conta.
  * Gerenciar informações de contexto, alterações de cmdlet:
    - Adicionado Scope = (Process | CurrentUser) para todos os cmdlets que alteram credenciais
    - Get-AzureRmContext - Adicionado o parâmetro ListAvailable para listar todos os contextos salvos
* Recursos
  * Adicionar os cmdlets PolicySetDefinition
    - Cmdlet New-AzureRmPolicySetDefinition para criar uma definição de conjunto de políticas
    - Cmdlet Get-AzureRmPolicySetDefinition para listar todas as definições de conjunto de políticas ou para obter uma definição de conjunto de políticas específico
    - Cmdlet Remove-AzureRmPolicySetDefinition para excluir uma definição de conjunto de políticas
    - Cmdlet Set-AzureRmPolicySetDefinition para atualizar uma definição de conjunto de políticas existente
  * Adicionar os parâmetros -PolicySetDefinition, -Sku e -NotScope aos cmdlets New-AzureRmPolicyAssignment e Set-AzureRmPolicyAssignment
  * Adicionar suporte para passar na url de política para os cmdlets New-AzureRmPolicyDefinition e Set-AzureRmPolicyDefinition
  * Adicionar o parâmetro -Mode ao cmdlet New-AzureRmPolicyDefinition
  * Adicionar suporte para remoção de atribuição de função usando o objeto PSRoleAssignment
    - Os usuários podem usar agora o objeto de entrada PSRoleassignmnet com o commandlet Remove-AzureRMRoleAssignment para remover a atribuição de função.
  * Adicionar os cmdlets ManagedApplication
    - Cmdlet New-AzureRmManagedApplication para criar um aplicativo gerenciado
    - Cmdlet Get-AzureRmManagedApplication para listar todos os aplicativos gerenciados em uma assinatura ou para obter um aplicativo gerenciado específico
    - Cmdlet Remove-AzureRmManagedApplication para excluir um aplicativo gerenciado
    - Cmdlet Set-AzureRmManagedApplication para atualizar um aplicativo gerenciado existente
  * Adicionar os cmdlets ManagedApplicationDefinition
    - Cmdlet New-AzureRmManagedApplicationDefinition para criar uma definição de aplicativo gerenciado usando um uri de arquivo zip ou os arquivos json mainTemplate e createUiDefinition
    - Cmdlet Get-AzureRmManagedApplicationDefinition para listar todas as definições de aplicativo gerenciado em um grupo de recursos ou para obter uma definição de aplicativo gerenciado específica
    - Cmdlet Remove-AzureRmManagedApplicationDefinition para excluir uma definição de aplicativo gerenciado
    - Cmdlet Set-AzureRmManagedApplicationDefinition para atualizar uma definição de aplicativo gerenciado existente
* Sql
  * Adicionar suporte às Regras de Rede Virtual
    - Adicionar o cmdlet Get-AzureRmSqlServerVirtualNetworkRule que obtém as regras de rede virtual através do nome de uma regra específica ou uma lista de regras de rede virtual em um SQL Server do Azure.
    - Adicionar o cmdlet Set-AzureRmSqlServerVirtualNetworkRule que altera a rede virtual para a qual a regra aponta.
    - Adicionar o cmdlet Remove-AzureRmSqlServerVirtualNetworkRule que remove uma regra de rede virtual para um SQL Server do Azure.
    - Adicionar o cmdlet New-AzureRmSqlServerVirtualNetworkRule que cria uma regra de rede virtual para um SQL Server do Azure.
* Sites
  * Adicionar camada PremiumV2 para Planos de Serviço de Aplicativo
* Azure.Storage
  * Atualizar para a Biblioteca do Cliente do Armazenamento do Azure 8.4.0 e a Biblioteca de Movimentação de Dados do Armazenamento do Azure 0.6.1
  * Adicionar Suporte a PremiumPageBlobTier na API de Carregar e Copiar Blob
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * Refinar o Formato de Saída do Console de AzureStorageContainer, AzureStorageBlob, AzureStorageQueue, AzureStorageTable
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>10/08/2017 – Versão 4.3.1
  * Atualização para corrigir o problema de assinatura de assembly

## <a name="20170807---version-430"></a>07/08/2017 – Versão 4.3.0
* AnalysisServices
  * Bug corrigido em Set-AzureRmAnalysisServciesServer
    - Quando o administrador não for fornecido, o administrador será removido.
  * BackupBlobContainerUri foi incluído em New-AzureRmAnalysisServicesServer e em Set-AzureRmAnalysisServicesServer
    - Habilitar para definir/desabilitar o contêiner de blobs de backup para backup/restauração do Azure Analysis Services Server
  * A pesquisa de SKU foi atualizada em New-AzureRmAnalysisServicesServer e em Set-AzureRmAnalysisServicesServer
    - A SKU embutida em código foi alterada para consulta dinâmica.
  * Add-AzureAnalysisServicesAccount para dar suporte a logon com entidade de serviço
* Automação
  * Foram feitas alterações nos cmdlets AutomationDSC* para efetuar pull de mais de 100 registros
  * Foi resolvido o problema em que os fluxos detalhados param de funcionar depois de chamar alguns cmdlets de Automação (por exemplo, Get-AzureRmAutomationVariable, Get-AzureRmAutomationJob).
  * Foi incluído suporte para controle de versão de build de NodeConfiguration em StartAzureAutomationDscCompilationJob e em ImportAzureAutomationDscNodeConfiguration
  * Correções de bug de problemas existentes – corrige o problema de alias n° 3775 e o alias runOn e o suporte para HybridWorkers.
* Computação
  * Set-AzureRmVMAEMExtension: adicionar suporte para novos tamanhos de disco Premium
  * Set-AzureRmVMAEMExtension: adicionar suporte para a série M
  * Adicionar o parâmetro ForceUpdateTag em AzureRmVmssExtension
  * Adicionar o parâmetro primário em New-AzureRmVmssIpConfig
  * Adicionar o parâmetro EnableAcceleratedNetworking em Add-AzureRmVmssNetworkInterfaceConfig
  * Adicionar InstanceId em Set-AzureRmVmss
  * Expor MaintenanceRedeployStatus para a saída de Get-AzureRmVM -Status
  * Expor a restrição e a capacidade para o formato de tabela de Get-AzureRmComputeResourceSku
* DataLakeStore
  * Correção do problema: https://github.com/Azure/azure-powershell/issues/4323
* EventHub
  * A propriedade ResourceGroup foi adicionada em NamespaceAttributes
    - 'ResourceGroup' obtém o nome do grupo de recursos em que o Namespace está
  * Os cmdlets foram atualizados com Parametersets para Namespace e EventHub para a operação de AuthorizationRule
    - New-AzureRmEventHubAuthorizationRule – adiciona uma nova AuthorizationRule no NameSpace ou do EventHub existente.
    - Get-AzureRmEventHubAuthorizationRule – obtém a AuthorizationRule/Lista de AuthorizationRules do NameSpace ou do EventHub atual.
    - Set-AzureRmEventHubAuthorizationRule – atualiza as propriedades da AuthorizationRule existente do NameSpace do EventHub.
    - Remove-AzureRmEventHubAuthorizationRule – exclui a AuthorizationRule existente do NameSpace ou do EventHub existente.
    - New-AzureRmEventHubKey – gera uma nova chave primária/secundária para AuthorizationRule do NameSpace ou do EventHub existente.
    - Get-AzureRmEventHubKey – Obtém a chave primária/secundária da AuthorizationRule do NameSpace ou do EventHub existente.
* Rede
    * Foi adicionado o suporte para IPv6 e o novo parâmetro opcional -PeerAddressType
      * New-AzureRmExpressRouteCircuitPeeringConfig:
      * Set-AzureRmExpressRouteCircuitPeeringConfig: foi adicionado o suporte para IPv6. Novo parâmetro opcional adicional
      * Remove-AzureRmExpressRouteCircuitPeeringConfig: foi adicionado o suporte para IPv6. Novo parâmetro opcional adicional
    * O parâmetro -ProbeEnabled foi marcado como obsoleto
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* Perfil
    * A coleta de dados foi habilitada por padrão. Os dados de uso são coletados pela Microsoft para aprimorar a experiência do usuário. Os dados são anônimos e não incluem os valores de argumento da linha de comando.
      - Use o cmdlet Disable-AzureRmDataCollection para desativar o recurso
      - Use o cmdlet Enable-AzureRmDataCollection para ativar esse recurso
* Recursos
    * Adicionar suporte para validação de escopos para os seguintes commandlets, roledefinition e roleassignment antes de enviar a solicitação para ARM
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
    * Foram adicionados os novos commandlets abaixo para AuthorizationRules de NameSpace, Fila e Tópico. de acordo com o conjunto de parâmetros, as operações de regra de autorização são executadas.
     - New-AzureRmServiceBusAuthorizationRule – adiciona uma nova AuthorizationRule para o NameSpace/a Fila/o Tópico do ServiceBus existente.
     - Get-AzureRmServiceBusAuthorizationRule – Obtém a AuthorizationRule/Lista de AuthorizationRules para o NameSpace/a Fila/o Tópico do ServiceBus existente.
     - Set-AzureRmServiceBusAuthorizationRule – atualiza as propriedades da AuthorizationRule existente do NameSpace/da Fila/do Tópico do Servicebus.
     - New-AzureRmServiceBusKey – gera uma nova chave primária/secundária para AuthorizationRule do NameSpace/da Fila/do Tópico do ServiceBus existente.
     - Get-AzureRmServiceBusKey – obtém a chave primária/secundária para AuthorizationRule do NameSpace/da Fila/do Tópico do ServiceBus existente.
     - Remove-AzureRmServiceBusNamespaceAuthorizationRule – exclui a AuthorizationRule existente do NameSpace/da Fila/do Tópico do ServiceBus.
    * Foi adicionada a propriedade do grupo de recursos em NamespceAttributes
* Sql
    * Set-AzureRmSqlServerTransparentDataEncryptionProtector está sendo atualizado para exibir um aviso e solicitar a confirmação se o tipo de protetor de criptografia estiver sendo definido como AzureKeyVault
    * Novo cmdlets atualizados foram adicionados nas configurações de auditoria
      - O cmdlet Get-AzureRmSqlDatabaseAuditing que obtém as configurações de auditoria de um banco de dados SQL do Azure.
      - O cmdlet Get-AzureRmSqlServerAuditing que obtém as configurações de auditoria de um SQL Server do Azure.
      - O cmdlet Set-AzureRmSqlDatabaseAuditing que altera as configurações de auditoria de um banco de dados SQL do Azure.
      - O cmdlet Set-AzureRmSqlServerAuditing que altera as configurações de auditoria de um SQL Server do Azure.
    * Os cmdlets de política de auditoria existentes foram preteridos
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * A análise do arquivo de esquema de Update-AzureRmSqlSyncGroup não diferencia mais maiúsculas de minúsculas.
* Armazenamento
    * Adicionar suporte a NeworkRule para cmdlets de conta de armazenamento de modo de recurso
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>17/07/2017 – Versão 4.2.1
* Computação
    - Corrigir problema com o Disco da VM e com cmdlets de atualização e de criação de instantâneo do Disco da VM, (link): [https://github.com/azure/azure-powershell/issues/4309]
      - New-AzureRmDisk
      - New-AzureRmSnapshot
      - Update-AzureRmDisk
      - Update-AzureRmSnapshot
* Perfil
    - Corrija o problema com a autenticação de usuário não interativo no RDFE (link) [https://github.com/Azure/azure-powershell/issues/4299]
* ServiceManagement
    - Corrija o problema com a autenticação de usuário não interativo (link) [https://github.com/Azure/azure-powershell/issues/4299]

## <a name="2017711---version-420"></a>11/07/2017 – Versão 4.2.0
* AnalysisServices
    * Adicionar nova API de plano de dados
        - Introduzida API para buscar log do servidor AS: Export-AzureAnalysisServicesInstanceLog
* Automação
    * Configuração adequada do valor TimeZone nas agendas Semanal e Mensal de New-AzureRmAutomationSchedule
        - Mais informações podem ser encontradas neste problema: https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - Adicionado novo cmdlet Get-AzureBatchJobPreparationAndReleaseTaskStatus.
    - Adicionado início e término do intervalo de bytes aos parâmetros Get-AzureBatchNodeFileContent.
* CognitiveServices
    * Integrar ao SDK de Gerenciamento dos Serviços Cognitivos versão 1.0.0.
    * Corrigir um bug de verificação do comprimento do nome da conta.
* Computação
    * Suporte do tipo de conta de armazenamento para disco de imagem:
        - O parâmetro 'StorageAccountType' foi adicionado a Set-AzureRmImageOsDisk e a Add-AzureRmImageDataDisk
    * Recurso PrivateIP e PublicIP na Configuração de IP de Vmss:
        - Os nomes 'PrivateIPAddressVersion', 'PublicIPAddressConfigurationName', 'PublicIPAddressConfigurationIdleTimeoutInMinutes' e 'DnsSetting' foram adicionados a New-AzureRmVmssIpConfig
        - O parâmetro 'PrivateIPAddressVersion' para especificar IPv4 ou IPv6 foi adicionado a New-AzureRmVmssIpConfig
    * Recurso Manutenção de Desempenho:
        - O parâmetro da opção 'PerformMaintenance' foi adicionado a Restart-AzureRmVM.
        - Get-AzureRmVM -Status mostra as informações de manutenção de desempenho da VM em questão
    * Recurso Identidade da Máquina Virtual:
        - O parâmetro 'IdentityType' foi adicionado a New-AzureRmVMConfig e a UpdateAzureRmVM
        - Get-AzureRmVM mostra as informações da identidade da VM em questão
    * Recurso Identidade de Vmss:
        - O parâmetro 'IdentityType' foi adicionado a New-AzureRmVmssConfig
        - Get-AzureRmVmss mostra as informações da identidade do Vmss em questão
    * Recurso Diagnóstico de Inicialização de Vmss:
        - Novo cmdlet para configurar o diagnóstico de inicialização do objeto Vmss: Set-AzureRmVmssBootDiagnostics
        - O parâmetro 'BootDiagnostic' foi adicionado a New-AzureRmVmssConfig
    * Recurso LicenseType de Vmss:
        - O parâmetro 'LicenseType' foi adicionado a New-AzureRmVmssConfig
    * Suporte a RecoveryPolicyMode:
        - O parâmetro 'RecoveryPolicyMode' foi adicionado a New-AzureRmVmssConfig
    * Recurso SKU de Recurso de Computação:
        - Novo cmdlet 'Get-AzureRmComputeResourceSku' lista todas as SKUs dos recursos de computação
* DataFactories
    * Preterir New-AzureRmDataFactoryGatewayKey
    * Introduzir recurso de chave de autorização de gateway adicionando New-AzureRmDataFactoryGatewayAuthKey e Get-AzureRmDataFactoryGatewayAuthKey
* DataLakeAnalytics
    * Adicionar suporte ao CRUD da Política de Computação por meio dos comandos a seguir:
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * Adicionar suporte aos metadados de relação de trabalho para obter ajuda com trabalhos recorrentes e pipelines de trabalhos. Os comandos a seguir foram atualizados ou adicionados:
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * Atualizado o público do token para que as APIs de trabalho e de catálogo usem o público específico correto do Data Lake, em vez do público do Recurso do Azure.
* DataLakeStore
    * Suporte adicionado para rotações de chave do KeyVault gerenciado pelo usuário no cmdlet Set-AzureRMDataLakeStoreAccount
    * Adicionada uma atualização de qualidade de vida para disparar automaticamente uma chamada a `enableKeyVault` quando um KeyVault gerenciado pelo usuário for adicionado ou uma chave for girada.
    * Atualizado o público do token para que as APIs de trabalho e de catálogo usem o público específico correto do Data Lake, em vez do público do Recurso do Azure.
    * Corrigido o bug que limitava o tamanho dos arquivos criados/anexados usando os seguintes cmdlets:
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* DNS
    * Corrigir bug no cenário de direcionamento para Get-AzureRmDnsZone
        - Encontre mais informações aqui: https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * Suporte adicionado para habilitar/desabilitar o OMS (Operations Management Suite)
    * Novos cmdlets
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * Adicionar novos parâmetros para definir configurações personalizadas do Spark a Add-AzureRmHDInsightConfigValues
        - Parâmetros SparkDefaults e SparkThriftConf para Spark 1.6
        - Parâmetros Spark2Defaults e Spark2ThriftConf para Spark 2.0
* Insights
    * O problema nº 4215 (solicitação de alteração) removeu o limite de 15 dias na janela de tempo do cmdlet Get-AzureRmLog. Além de pequenas alterações nos nomes dos testes de unidades.
    * Problema nº 3957 corrigido para Get-AzureRmLog
        - Problema nº 1: o back-end retorna os registros nas páginas de 200 registros cada, vinculados pelo token de continuação à próxima página. Os clientes viram o cmdlet retornando somente 200 registros quando sabiam que havia mais. Isso estava ocorrendo independentemente do valor definido para MaxEvents, a menos que o valor fosse menor que 200.
        - Problema nº 2: a documentação continha dados incorretos sobre esse cmdlet, por exemplo: a janela de tempo padrão era de uma hora.
        - Correção nº 1: O cmdlet agora segue o token de continuação retornado pelo back-end até atingir MaxEvents ou até o fim do conjunto.<br>O valor padrão de MaxEvents é 1000 e o máximo é 100000. Qualquer valor de MaxEvents menor que 1 é ignorado e o padrão é usado em vez disso. Esses valores e o comportamento não foram alterados. Agora eles são documentados corretamente.<br>Um alias para MaxEvents foi adicionado, MaxRecords, uma vez que o nome do cmdlet não fala mais sobre os eventos, mas somente sobre os Logs.
        - Correção nº 2: A documentação contém informações corretas e mais detalhadas: novo alias, janela de tempo correta, padrão correto e valores mínimo e máximo.
* KeyVault
    * Remover endereço de email da consulta de diretório quando -UserPrincipalName for especificado para os cmdlets Set-AzureRMKeyVaultAccessPolicy e Remove-AzureRMKeyVaultAccessPolicy.
      - Ambos os cmdlets agora tem um parâmetro -EmailAddress que pode ser usado em vez do parâmetro -UserPrincipalName quando consultar pelo endereço de email for apropriado.  Se houver mais de um endereço de email correspondente no diretório, o cmdlet falhará.
* Rede
    * New-AzureRmIpsecPolicy: SALifeTimeSeconds e SADataSizeKilobytes não são mais parâmetros obrigatórios
        - O padrão de SALifeTimeSeconds é 27000 segundos
        - O padrão de SADataSizeKilobytes é 102400000 KB
    * Suporte adicionado para configuração do conjunto de criptografia personalizada usando a política de SSL e listando todas as APIs de opções de SSL no Gateway de Aplicativo
        - Parâmetro opcional adicionado: -PolicyType, -PolicyName, -MinProtocolVersion e -Ciphersuite
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - Adicionado Get-AzureRmApplicationGatewayAvailableSslOptions (Alias: List-AzureRmApplicationGatewayAvailableSslOptions)
        - Adicionado Get-AzureRmApplicationGatewaySslPredefinedPolicy (Alias: List-AzureRmApplicationGatewaySslPredefinedPolicy)
    * Suporte a redirecionamento adicionado ao Gateway de Aplicativo
        - Adicionado Add-AzureRmApplicationGatewayRedirectConfiguration
        - Adicionado Get-AzureRmApplicationGatewayRedirectConfiguration
        - Adicionado New-AzureRmApplicationGatewayRedirectConfiguration
        - Adicionado Remove-AzureRmApplicationGatewayRedirectConfiguration
        - Adicionado Set-AzureRmApplicationGatewayRedirectConfiguration
        - Parâmetro opcional adicionado: -RedirectConfiguration
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - Parâmetro opcional adicionado: -DefaultRedirectConfiguration
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - Parâmetro opcional adicionado: -RedirectConfiguration
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - Parâmetro opcional adicionado: -RedirectConfigurations
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Suporte adicionado aos Sites do Azure no Gateway de Aplicativo
        - Adicionado New-AzureRmApplicationGatewayProbeHealthResponseMatch
        - Parâmetros opcionais adicionados: -PickHostNameFromBackendHttpSettings, -MinServers e -Match
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - Parâmetros opcionais adicionados: -PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled e -Path
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * Atualizar Get-AzureRmPublicIPaddress para recuperar recursos de endereço público criados por meio do Conjunto de Dimensionamento de VMs
    * Adicionado cmdlet para obter uso atual da rede virtual
        - Get-AzureRmVirtualNetworkUsageList
* Perfil
    * Erro ao usar Import-AzureRmContext ou Save-AzureRmContext corrigido
        - Mais informações podem ser encontradas neste problema: https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * Introdução de novo módulo para operações do Azure Site Recovery.
        - Todos os cmdlets começam com AzureRmRecoveryServicesAsr*
* Sql
    * Adicionar Cmdlets do PowerShell de Sincronização de Dados ao AzureRM.Sql
    * Cmdlets do AzureRmSqlServer atualizados para usar nova versão da API REST que evita esgotamento de tempo limite ao criar servidor.
    * Cmdlets de atualização de servidor preteridos porque a versão antiga do servidor (2.0) não existe mais.
    * Adicionar novo parâmetro de opção opcional "AssignIdentity" aos cmdlets New-AzureRmSqlServer e Set-AzureRmSqlServer para dar suporte ao provisionamento de uma identidade de recurso para o recurso do SQL Server
    * O parâmetro ResourceGroupName agora é opcional para Get-AzureRmSqlServer
        - Mais informações podem ser encontradas no seguinte problema: https://github.com/Azure/azure-powershell/issues/635
* ServiceManagement para ExpressRoute:
    * Cmdlet New-AzureBgpPeering atualizado para adicionar as seguintes novas opções:
        - PeerAddressType: os valores de "IPv4" ou de "IPv6" podem ser especificados para criar um emparelhamento via protocolo BGP do tipo de família do endereço correspondente
    * Cmdlet Set-AzureBgpPeering atualizado para adicionar as seguintes novas opções:
        - PeerAddressType: os valores de "IPv4" ou de "IPv6" podem ser especificados para atualizar o emparelhamento via protocolo BGP do tipo de família do endereço correspondente
    * Cmdlet Remove-AzureBgpPeering atualizado para adicionar as seguintes novas opções:
        - PeerAddressType: os valores de "IPv4", de "IPv6" ou de Todos podem ser especificados para remover o emparelhamento via protocolo BGP do tipo de família do endereço correspondente ou de todos eles

## <a name="20170607---version-410"></a>07/06/2017 – Versão 4.1.0
* AnalysisServices
    * Novas SKUs adicionadas: B1, B2 e S0
    * Suporte adicionado para aumentar/reduzir
* CognitiveServices
    * Atualizar exibição detalhada dos contratos de licença ao criar recursos dos Serviços Cognitivos
* Computação
    * Corrigir Test-AzureRmVMAEMExtension para máquinas virtuais com vários discos gerenciados
    * Set-AzureRmVMAEMExtension atualizado: adicionar informações de cache para discos gerenciados Premium
    * Add-AzureRmVhd: o limite de tamanho no VHD aumentou para 4 TB.
    * Stop-AzureRmVM: esclarecer documentação para o parâmetro STayProvisioned
    * New-AzureRmDiskUpdateConfig
      * Parâmetros preteridos: CreateOption, StorageAccountId, ImageReference, SourceUri e SourceResourceId
    * Set-AzureRmDiskUpdateImageReference: cmdlet preterido
    * New-AzureRmSnapshotUpdateConfig
      * Parâmetros preteridos: CreateOption, StorageAccountId, ImageReference, SourceUri e SourceResourceId
    * Set-AzureRmSnapshotUpdateImageReference: cmdlet preterido
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * Habilitar criptografia gerenciada do KeyVault para um DataLake Store
* DevTestLabs
    * Atualizar cmdlets para funcionar com a versão atual e atualizada da API do DevTest Labs.
* IotHub
    * Adicionar suporte a roteamento aos cmdlets IoTHub
* KeyVault
  * Novos cmdlets para dar suporte a chaves de conta de armazenamento gerenciado do KeyVault
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* Rede
    * Get-AzureRmNetworkUsage: novo cmdlet para mostrar detalhes de capacidade e de uso de rede
    * Adicionadas novas opções de GatewaySku para VirtualNetworkGateways
        * VpnGw1, VpnGw2 e VpnGw3 são as novas SKUs adicionadas aos gateways de VPN
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * Exemplos de ajuda corrigidos
* NotificationHubs
    * Atualização transparente para os cmdlets NotificationHubs da nova API
* Perfil
    * Resolve-AzureRmError
      * Novo cmdlet para mostrar os detalhes das exceções e dos erros gerados pelos cmdlets, incluindo dados de solicitação/resposta do servidor
    * Send-Feedback
      * Habilitado o envio de comentários sem fazer logon
    * Get-AzureRmSubscription
      * Corrigir bug ao recuperar assinaturas de CSP
* Recursos
    * Problema corrigido no qual o Get-AzureRMRoleAssignment resultaria em uma Solicitação Inválida se o número de atribuições de função fosse maior que 1000
        * Os usuários agora poderão usar Get-AzureRMRoleAssignment mesmo se o número de atribuições de função retornado for maior que 1000
* Sql
    * Restore-AzureRmSqlDatabase: atualizar exemplo de documentação
* Armazenamento
    * Adicionar suporte à configuração AssignIdentity aos cmdlets de conta de armazenamento no modo de recurso
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * Adicionar Suporte à Chave do Cliente aos cmdlets de conta de armazenamento no modo de recurso
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * Novas configurações de Monitor: 'MonitorIntervalInSeconds', 'MonitorTimeoutInSeconds' e 'MonitorToleratedNumberOfFailures'
    * Novo protocolo 'TCP' do Monitor
* ServiceManagement
    * Add-AzureVhd: o limite de tamanho no VHD aumentou para 4 TB.
    * New-AzureBGPPeering: suporte a LegacyMode
* Azure.Storage
    * Atualizar ajuda para os parâmetros que aceitam caracteres curinga e atualizar o tipo StorageContext

## <a name="20170523---version-402"></a>23/05/2017 – Versão 4.0.2
* Perfil
    * Add-AzureRmAccount
      * Adicionado alias do parâmetro `-EnvironmentName` para compatibilidade com versões anteriores 2.x do AzureRM.profile

## <a name="20170512---version-401"></a>12/05/2017 – Versão 4.0.1
 * Corrija o problema com New-AzureStorageContext em cenários offline: https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>10/05/2017 – Versão 4.0.0


* Esta versão contém alterações de última hora. Consulte o [guia de migração](https://aka.ms/azps-migration-guide) para obter os detalhes de alteração e saber o impacto sobre os scripts existentes.
* ApiManagement
  - Suporte adicionado para configurar grupos externos no New-AzureRmApiManagementGroup.
* Cobrança
  - Novo cmdlet Get-AzureRmBillingPeriod
    + Cmdlet para recuperar períodos de cobrança de assinatura do Azure.
  - Atualizar o cmdlet Get-AzureRmBillingInvoice
  - nova propriedade BillingPeriodNames
  - saída em modo de exibição de lista
* Computação
  - Os cmdlets atualizados AzureRmVMAEMExtension e Test-AzureRmVMAEMExtension oferecem suporte ao Managed Disks Premium
  - Configurações de criptografia de backup para VMs de IaaS e restauração em caso de falha
  - A opção ChefServiceInterval foi renomeada como ChefDaemonInterval. No entanto, a antiga opção continuará funcionando.
  - Remover as propriedades duplicadas DataDiskNames e NetworkInterfaceIDs do objeto PS da VM.
  - Tornar os parâmetros DataDiskNames e NetworkInterfaceIDs opcionais em Remove-AzureRmVMDataDisk e Remove-AzureRmVMNetworkInterface, respectivamente.
  - Corrigir o problema de direcionamento dos cmdlets Get quando eles retornarem um objeto de lista.
  - Os cmdlets que entraram em conflito com os cmdlets RDFE foram renomeados. Consulte o problema https://github.com/Azure/azure-powershell/issues/2917 para obter mais detalhes
    + `New-AzureVMSqlServerAutoBackupConfig` foi renomeado para `New-AzureRmVMSqlServerAutoBackupConfig`
    + `New-AzureVMSqlServerAutoPatchingConfig` foi renomeado para `New-AzureRmVMSqlServerAutoPatchingConfig`
    + `New-AzureVMSqlServerKeyVaultCredentialConfig` foi renomeado para `New-AzureRmVMSqlServerKeyVaultCredentialConfig`
* Consumo
  - Novo cmdlet Get-AzureRmConsumptionUsageDetail
    + Cmdlet para recuperar detalhes de uso da assinatura.
* ContainerRegistry
  - Adicionar cmdlets do PowerShell ao Registro de Contêiner do Azure
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - Adicionar suporte aos pacotes de catálogo get e list
  - Adicionar suporte à listagem dos seguintes itens de catálogo de ancestrais mais antigos:
    + Tabela
    + TVF
    + Visualizar
    + Estatísticas
* DataLakeStore
  - O registro de rastreamento de `Import-AzureRMDataLakeStoreItem` e `Export-AzureRMDataLakeStoreItem` foi desabilitado por padrão para melhorar o desempenho. Caso registro de rastreamento seja desejável, utilize os parâmetros `-DiagnosticLogLevel` e `-DiagnosticLogPath`
  - O bug que ocasionalmente fazia com que o PowerShell falhasse ao fazer o upload de vários arquivos pequenos para o ADLS foi corrigido.
* EventHub
  - Correção de bug:
    + Correção do erro do cmdlet Set-AzureRmEventHubNamespace – 'Tier' não pode ser null, quando deve ser 'SkuName'
    + Set-AzureRmEventHub – Correção do erro “A referência do objeto não está definida como uma instância de um objeto” ao atualizar o EventHub
* Insights
  - Add-AzureRm*AlertRule
    + Retorna um único objeto: newResource, statusCode, requestId
  - Get-AzureRmAlertRule
    + Agora, a saída é numerada, em vez de considerada um único objeto. O tipo não foi alterado, ainda é uma lista.
  - Remove-AzureRmAlertRule
    + O statusCode segue o código de status retornado pela solicitação, antes era sempre Ok.
  - Add-AzureRmAutoscaleSetting
    + Agora, retorna um objeto único (e não uma lista, como antes) que contém statusCode, requestId e o recurso criado/atualizado recentemente.
    + O código de status segue o status retornado pela solicitação, antes era sempre Ok.
  - New-AzureRmAutoscaleRule
    + O parâmetro ScaleActionType foi estendido e agora recebe os seguintes valores: ChangeCount, PercentChangeCount e ExactCount.
  - Remove-AzureRmAutoscaleSetting
    + O statusCode na saída segue o statusCode retornado pela solicitação. Antes, era sempre Ok.
  - Get-AzureRMLogProfile
    + Agora, a saída é enumerada. Antes, ela era considerada um objeto único. O tipo da saída ainda é uma lista, como antes.
  - Remove-AzureRmLogProfile
    + O parâmetro PassThru foi implementado.
  - API de Métrica
    + Agora, o SDK recupera métrica do MDM.
  - Get-AzureRmMetricDefinition
    + A saída ainda é uma lista, mas a estrutura dessa lista foi alterada.
  - Get-AzureRmMetric
    + A chamada foi alterada. Esta é a nova sintaxe: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]
    + A saída é uma lista e a estrutura de seus elementos foi alterada.
* KeyVault
  - Adicionar suporte de backup/restauração aos segredos do KeyVault
    + É possível fazer backup e restaurar os segredos, de acordo com a funcionalidade que dá suporte para as Chaves atualmente

  - Os cmdlets de backup para Chaves e Segredos agora aceitam um objeto correspondente como um parâmetro de entrada
    + O chamador pode encadear operações de backup e recuperação: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - Agora, os cmdlets de backup oferecem suporte a um comutador -Force para substituir um arquivo existente
    + Observe que a tentativa de substituir um arquivo existente não lançará mais e, em vez disso, solicitará que o usuário escolha como proceder.
* LogicApp
  - Novos parâmetros para os cmdlets de recuperação de desastre de Número de Controle de Intercâmbio:
    + Parâmetro opcional -AgreementType (“X12” ou “Edifact”) para especificar os números de controle relevantes
* MachineLearning
  - Use a nova versão do SDK .Net do Azure Machine Learning e adicione um novo cmdlet
    + Add-AzureRmMlWebServiceRegionalProperty
  - Pequenas correções de palavras no texto de ajuda.
* Rede
  - Cmdlet Test-AzureRmNetworkWatcherConnectivity
    + Retorna informações de conectividade para uma VM de origem especificada e um destino
    + Se a conectividade entre a origem e o destino não puder ser estabelecida, o cmdlet retornará detalhes sobre o problema
* Perfil
  - O cmdlet Send-Feedback adicionado: permite que o usuário inicie um conjunto de prompts que enviam comentários à equipe do Azure PowerShell.
  - Os aliases a seguir foram removidos, pois entravam em conflito com os nomes de cmdlet existentes no módulo do Azure:
    + `Enable-AzureDataCollection` (com suporte de `Enable-AzureRmDataCollection`)
    + `Disable-AzureDataCollection` (com suporte de `Disable-AzureRmDataCollection`)
* Retransmissão
  - Adiciona cmdlets à Retransmissão do Azure, o que permite que os usuários criem e gerenciem todos os recursos da Retransmissão do Azure.
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* Recursos
  - Suporte para implantações de grupo de recursos cruzados do New-AzureRmResourceGroupDeployment
    + Agora, os usuários podem usar implantações aninhadas para implantar grupos de recursos diferentes.
* ServiceBus

  - Correção de bug: Os valores de propriedade do objeto de fila ServiceBus foram definidos como null, o objeto é utilizado como parâmetro de entrada no cmdlet Set-AzureRmServiceBusQueue para atualizar a fila.
   - As propriedades afetadas são LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount e MessageCount
* ServiceFabric

  - Cmdlets adicionadas ao Service Fabric
    + Add-AzureRmServiceFabricApplicationCertificate Adiciona um certificado que será utilizado como certificado de aplicativo
    + Add-AzureRmServiceFabricClientCertificate Adiciona um nome comum ou impressão digital às configurações do cluster para a autenticação de cliente
    + Add-AzureRmServiceFabricClusterCertificate Adiciona um certificado de cluster secundário ao cluster a fim de sobrepor o certificado existente
    + Add-AzureRmServiceFabricNodes Adiciona nós/VMs de um tipo específico de nó a um cluster
    + Add-AzureRmServiceFabricNodeType Adiciona um tipo de nó/VMs a um cluster existente
    + Get-AzureRmServiceFabricCluster       Obtém os detalhes do recurso do cluster
    + New-AzureRmServiceFabricCluster Cria um novo cluster ServiceFabric. Esse comando tem muitas sobrecargas para cobrir vários cenários
    + Remove-AzureRmServiceFabricClientCertificate       Impede que um certificado de cliente seja usado para acessar um cluster
    + Remove-AzureRmServiceFabricClusterCertificate       Impede que um certificado de cluster seja usado para a segurança de um cluster
    + Remove-AzureRmServiceFabricNodes Remove nós de um tipo de nó específico de um cluster
    + Remove-AzureRmServiceFabricNodeType       Remove um tipo de nó de um cluster
    + Remove-AzureRmServiceFabricSettings       Remove uma ou mais configurações do ServiceFabric de um cluster
    + Set-AzureRmServiceFabricSettings       Adiciona ou atualiza uma ou mais configurações do ServiceFabric de um cluster
    + Set-AzureRmServiceFabricUpgradeType Altera o tipo de atualização do ServiceFabric de um cluster
    + Update-AzureRmServiceFabricDurability Altera a camada de durabilidade de um cluster
    + Update-AzureRmServiceFabricReliability Altera a camada de confiabilidade de um cluster
* Sql
  - Parâmetro -SampleName adicionado ao New-AzureRmSqlDatabase
  - Atualizações para os cmdlets de Grupo de Failover
  - Remover os parâmetros 'Tag'
  - Remover os parâmetros 'PartnerResourceGroupName' e 'PartnerServerName' do cmdlet Remove-AzureRmSqlDatabaseFailoverGroup
  - Adicionar o parâmetro 'GracePeriodWithDataLossHours' aos cmdlets New- e Set-, que no devido tempo substituirão 'GracePeriodWithDataLossHour'
  - A documentação foi elaborada e atualizada
  - Alterar a formatação de objetos retornados e corrigir alguns bugs em que os campos nem sempre foram preenchidos
  - Adicionar as propriedades 'DatabaseNames' e 'PartnerLocation' ao objeto Grupo de Failover
  - Corrigir o bug, fazendo com que o cmdlet Switch- retorne imediatamente, em vez de aguardar a conclusão da operação
  - Corrigir o bug de estouro do inteiro quando os valores do período de carência forem utilizados
  - Ajustar o período de carência para um mínimo de 1 hora se um valor menor for fornecido
  - Remover "Usage_Anomaly" dos valores aceitos do parâmetro "ExcludedDetectionType" dos cmdlets Set-AzureRmSqlDatabaseThreatDetectionPolicy e Set-AzureRmSqlServerThreatDetectionPolicy.
* Armazenamento
  - Atualizar o SDK da política SRP para 6.3.0
  - New/Set-AzureRmStorageAccount: Adicionar um novo parâmetro com suporte para EnableHttpsTrafficOnly
  - New/Set/Get-AzureRmStorageAccount: A conta de armazenamento retornada contém um novo atributo EnableHttpsTrafficOnly
* Azure.Storage
  - Atualizar para a Biblioteca do Cliente do Armazenamento do Azure 8.1.1 e Biblioteca de Movimentação de Dados do Armazenamento do Azure 0.5.1
  - Adicionar um novo cmdlet para oferecer suporte ao recurso de Cópia Incremental do blob
